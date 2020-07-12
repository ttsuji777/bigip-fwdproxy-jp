CA証明書の設定例
===========================

SSL Forward Proxyを構成する場合は、BIG-IPにCA証明書と秘密鍵をインストールします。ここでは、BIG−IP上での設定手順を紹介します。

.. code-block:: bash

   # Create files and directories needed for openssl
   mkdir /config/ca
   cd /config/ca
   mkdir /config/ca/newcerts
   mkdir /config/ca/private
   mkdir /config/ca/crl
   touch /config/ca/index.txt
   echo 01 > /config/ca/serial
 
   # Create a copy of openssl configuration files 
   cp /etc/pki/tls/openssl.cnf /config/ca
 
   # Enable use of multiple certificates with same subject and configure homedir
   # uncomment “#unique_subject = no” in [ CA_default ] section 
   vi /config/ca/openssl.cnf
   unique_subject  = no   
   dir             = /config/ca
 
   # create CA certificate and key used when SSL proxy is re-signing certificate from web servers (common name proxy_ca.example.com))
   openssl req -x509 -nodes -days 3650 -newkey rsa:2048 -out proxy_ca.pem -outform PEM -keyout proxy_ca.key
 
   # Verify ca certificate
   openssl x509 -in proxy_ca.pem -noout -text
 
   # Import CA key and cert into BIG-IP filestore
   tmsh install sys crypto cert proxy_ca.crt from-local-file /config/ca/proxy_ca.pem
   tmsh install sys crypto key proxy_ca.key from-local-file /config/ca/proxy_ca.key

