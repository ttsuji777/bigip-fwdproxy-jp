HTTP Profile設定
===========================

Explicit Forward Proxyを構成するHTTP Profileを設定します。

Local Traffic >> Profiles >> Servicesを選択して、HTTP Profileを作成します。

- General Propertiesのセクションで以下の設定を行います。

  - Proxy Mode: "Explicit"を選択
  - Parent Profile: "http-explicit"を選択

  .. figure:: images/mod2-5-1.png
     :scale: 80%
     :align: center

 - Explicit Proxyのセクションで以下の設定を行います。

  - DNS Resolver: "DNSリゾルバの設定"の項で作成したものを選択します。
  - Tunnel Names: "TLSをサポートするTCPトンネルの設定"の項で作成したものを選択します。

  .. figure:: images/mod2-5-2.png
     :scale: 80%
     :align: center


   