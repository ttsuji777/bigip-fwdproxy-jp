1. CA証明書の設定
===========================

本セットアップガイドにて BIG-IP Local Traffic Manager（以下、LTM）の設定方法についてご案内します。
BIG-IP LTM のサーバ負荷分散ををはじめとして SSLのオフロードやコンテンツスイッチング、また圧縮やキャッシュなど多彩な機能を搭載し、アプリケーションサービスの可用性を高め快適なユーザエクスペリエンスを提供するのに役立ちます。
本ガイドでは、BIG-IP LTM をご購入いただいてすぐに使い始められるように、サーバ負荷分散を実現するのに必要となる典型的なセットアップ手法を豊富なスクリーンショットを交えて解説します。
これにより、ネットワークを構成し、クライアント－サーバ間での簡単な WEB の負荷分散環境を構築することができますので、セットアップ時の手引きとしてご活用ください。また、管理用のマネージメント IP アドレスは設定済みである前提としております。
GitHub is a web-based platform used mainly for software code version control. You will use it to store content for your documentation project and manage it in the same way as code. 

1.1 LTM 動作概要
------------
LTM は以下䛾ような流れで動作します。
