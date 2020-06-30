#. HTTP Profileの種類
===========================

Proxy Modeを指定するHTTP Profileは、下表の通りです。

.. csv-table::
   :header: "Proxy Mode","説明"
   :widths: 30, 30

   "Reverse (デフォルト)","リバースプロキシとして利用"
   "Explicit","明示プロキシとして利用"
   "Transparent","透過プロキシとして利用"

アウトバウンド (=内部からインターネットへのアクセス)通信処理を行う際には、Explicit/Transparentを指定したHTTP Profileを割り当てます。
