HTTP Profile設定 (Explicit Forward Proxy)
===========================

Explicit Forward Proxyを構成するクライアントおよびサーバSSL Profileを設定します。

- クライアントSSL Profile

  - Local Traffic >> Profiles >> SSL >> Clientを選択して、クライアントSSL Profileを作成します (この例では"clientssl_proxy")。親プロファイル (Parent Profile)として、clientsslを指定します。
  .. image:: images/mod2-5-1.png
     :scale: 100


　- SSL Forward Proxyのセクションで以下の設定を行います。
    
    - SSL Forward Proxy: 有効 (Enabled)
    - CA Certificate Key Chain: "CA証明書の設定"の項で作成したCA証明書およびキーを指定
    - SSL Forward Proxy Bypass: 有効 (Enabled)
  .. image:: images/mod2-5-2.png
     :scale: 100


- サーバSSL Profile

  - Local Traffic >> Profiles >> SSL >> Serverを選択して、サーバSSL Profileを作成します (この例では"serverssl_proxy")。親プロファイル (Parent Profile)として、serversslを指定します。合わせて、以下の設定を行います。
    
    - SSL Forward Proxy: 有効 (Enabled)
    - SSL Forward Proxy Bypass: 有効 (Enabled)
  .. image:: images/mod2-5-3.png
     :scale: 100
  
  - Server Authenticationのセクションで以下の設定を行います。
    
    - Server Certificate: "require..."を選択
    - Trusted Bundled Authority: "ca-bundle.crt"を選択
  .. image:: images/mod2-5-4.png
     :scale: 100


