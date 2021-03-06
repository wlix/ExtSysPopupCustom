【ソフト名】 ExtSysPopupCustom
【著作権者】 Copyright (C) 2014-2021 tapetums, wlix
【種　　別】 TTBase プラグイン
【動作環境】 Windows Vista/7/8/8.1/10 32/64-bit
【開発環境】 Visual Studio Community 2019


【注意】
このプラグインは tapetums さん制作の ExtSysPopup プラグインを自分用に少し書き換えたものです。
特定ボタン上での右クリックをする場合以外は tapetums さん制作の ExtSysPopup をお使い下さい。
https://github.com/tapetums/ExtSysPopup/releases/latest


【概要】
ウィンドウの特定の領域を右クリックすると、いくつかのメニューを持ったポップアップメニューが開きます。
TTBase もしくは 互換プログラムのプラグインとして動作します。

・常に手前に表示する
・アプリケーションのインストールフォルダを開く
・透明度の設定
・優先度の設定
・設定ファイルの再読み込み

以下は、peach と hako で動作を確認しています。

・本体を終了する
・本体の設定
・本体のバージョン情報
・プラグインの再読み込み

このプラグインは、ExMenu.dll の模倣ソフトです。

【カスタム版変更点】
iniファイルにて、modeを1にしたとき、タイトルバー・最小化ボタン・最大化ボタン・閉じるボタンで
ポップアップメニューが出るように変更しました。


【インストール】
本体となるプログラムによります。
TTBase の場合は、本体のインストールフォルダ以下の場所に配置してください。

本体が 32-bit版 の場合は x86\ExtSysPopupCustom.dll を、
本体が 64-bit版 の場合は x64\ExtSysPopupCustom.dll を それぞれお使いください。


【アンインストール】
DLLファイル 及び .iniファイルを削除してください。
常駐型のプラグインのため、本体を一旦終了させる必要があります。


【使用方法】
ExtSysPopupCustom.ini というファイルを同梱しています。メモ帳などで編集できます。
mode というパラメータで特定の領域に設定するか、タイトルバー・最大化ボタン・最小化ボタン・閉じるボタン
にするかを指定します。

・modeが0の場合
x, y, w, h というパラメータで、右クリックした時にメニューを表示させたい領域を指定します。

x が x座標、
y が y座標、
w が 幅、
h が 高さ
です。

x もしくは y にマイナスの値を指定すると、それぞれウィンドウの右端もしくは下端からの相対座標となります。
例えば閉じるボタンの付近に設定したいときは、

x = -32, y = 0, w = 32, h = 32

などと指定します。お好みに合わせて .iniファイルを編集し、数値を変えて下さい。

・modeが1の場合
title, min, max, close というパラメータで、右クリックした時にメニューを表示させたい領域を指定します。

title を 1 にするとタイトルバー、
min を 1 にすると最小化ボタン、
max を 1 にすると最大化ボタン、
close を 1 にすると閉じるボタン
です。

「設定ファイルの再読み込み」メニューを選択すると、再起動することなく値が反映されます。


【ライセンス】
NYSL Version 0.9982 です。このプラグラムを使用したことによる一切の影響は関知しません。
http://www.kmonos.net/nysl/


【謝辞】
TTBase を生み出された K2 さん、peach を 公開されている U さん、TTBaseCpp の作者さん、
hako および ExtSysPopup プラグイン を 公開されている tapetums さんを始め、
数多くのプラグインを作られたそれぞれの作者さんたちに深い敬意と感謝を表します。
https://osdn.jp/projects/ttbase/
http://seesaawiki.jp/ttbase/d/
http://white2.php.xdomain.jp/?page_id=27
http://ttbase.coresv.com/uploader/
https://github.com/tapetums/


【更新履歴】
2021.02.10 v1.0.0.0
・公開

【オリジナル (tapetumsさん作成) 更新履歴】
2016.03.11 v1.3.1.0
・バグ修正

2016.03.06 v1.3.0.0
・現在の透明度と優先度を取得して、チェックマークが付くようにした

2016.02.17 v1.2.0.0
・安定性を向上
・ホットキーでもポップアップメニューを表示できるように

2016.02.14 v1.1.0.0
・ポップアップメニュー領域以外の場所をクリックするとフリーズするバグを修正
・右クリック位置の検出方法を変更
・透明度の設定を実装
・優先度の設定を実装

2016.01.30 v1.0.0.2
・開発環境を Visual Studio Community 2015 に変更
・細かなバグを修正

2014.10.06 v1.0.0.1
 ・「プラグインの再読み込み」を行うと初期化に失敗するのを修正

2014.10.04 v1.0.0.0
 ・初版作成


【文責】
wlix
https://github.com/wlix