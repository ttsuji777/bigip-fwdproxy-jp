DNSリゾルバの設定
===========================

BIG-IPのConfiguration Utilityで、DNSリゾルバを設定します。


Network >> DNS Resolverを選択して、DNSリゾルバを作成します。下図の例では"dns_resolover"という名前のDNSリゾルバを作成しています。

.. figure:: images/mod2-3-1.png
   :scale: 80%
   :align: center


作成したDNSリゾルバにおいて、Forward Zoneを選択します。

.. figure:: images/mod2-3-2.png
   :scale: 80%
   :align: center


Forward　Zoneの名前を". (ドット)"と指定して、BIG-IPがクライアントとして名前解決を行うDNSサーバのアドレスを入力します。

.. figure:: images/mod2-3-3.png
   :scale: 60%
   :align: center
