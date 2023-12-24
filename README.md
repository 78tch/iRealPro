# iRealPro
コード進行を入力して「テンポ」や曲調の「スタイル」を指定すると、自動でバッキング演奏してくれるソフト。  
曲の練習、スケールの練習、さまざまな練習のバッキングが手早く作れます。  
コード進行の入力方法や、繰り返し記号の設定方法が独特なので、使い方のコツをまとめます。  
  
1. コード記号や構成音の一覧は[こちら](./cordsymbols.md)
2. 繰り返し記号や実際の進行の例の一覧は[こちら](./repeatmark.md)
3. 最初から入っている「練習曲50曲」の一覧は[こちら](./library.md)

## 1.概要
1. App Store版（iPhone&iPad用）、Google Play版（Android 用）、amazon appstore版（Fire タブレット、Windows用）、Mac 用、の４種類があります。これらは、購入情報が共有されないので、それぞれ個別に買う必要があります。
2. Windows用、というのはないので、Windowsパソコンでは、amazon appstore 版を使います。Windowsパソコンに「Amazonアプリストア」アプリをインストールし、そのなかでiRealPro を購入して開くと、Fire タブレット 用のiRealPro がWindows 上で動きます。  https://blogs.windows.com/windows-insider/2021/10/20/introducing-android-apps-on-windows-11-to-windows-insiders/
3. 曲を用意する方法は、「１．[練習曲50曲](./library.md)を使う」「２．フォーラムで検索してダウンロードして取り込む」「３．自分で作る」「４．知り合いからもらって取り込む」のおおよそ４通りあります。
4. 取り込んだ曲が、細かいところで希望と違っても、テンポやキーは曲の設定で変えられますし、曲の内容の編集も、慣れれば簡単です。
5. 曲のエクスポート、インポートは、「iRealPro形式」というHTMLファイルでします。曲ファイルをブラウザで開くと、曲名のリンクがあり、リンクをタップすると、iRealProが立ち上がり、曲を取り込めます。「曲データ」の実体は、コード名や各種記号を英数字記号にした文字列であり、HTML内のリンク部分に文字列のまま格納されています。慣れてくれば、この文字列を直接編集することで、曲を編集することも可能です。
6. 公式の説明では、「Windowsパソコンでは曲のインポートができない」と書いてありますが、パソコンのどこかに曲ファイルを置いて、ブラウザで開いて、曲名のリンクをクリックすると、iRealProが立ち上がり、インポートできました。エクスポートは、「ダウンロード」フォルダに置かれます。
7. 作った曲や、取り込んだ曲は、「ライブラリー」の「曲」などから開けます。
8. よく使う曲は、「プレイリスト」を作って、まとめて管理すれば、呼び出すのに便利です。
9.  最初から入っている「練習曲」は、削除しても復元できます。最初は参考になりますが、慣れてきたら邪魔なので、消したいこともあると思います。まず、自分の作った曲や取り込んだ曲があれば、それをバックアップしたうえで、「設定 -> ユーティリティー -> すべてのコンテンツと設定を消去する」で消すと、ライブラリがカラになります。バックアップだけを戻せば、すっきりします。削除した「練習曲」を復元するには、「設定 -> ユーティリティー -> 練習曲を復元する」です。
10. 曲をMIDI形式でエクスポートすれば、Garageband などに読み込んで、さらに編集することもできます。（未検証）
  
## 2.基本的な使い方
1. トップ画面の「+」ボタンは、「新規プレイリスト」ボタンです。新しい「曲」を作るには、「曲」や「プレイリスト」を開いて、その画面の「+」ボタンからやります。
2. 「新しい曲」での指定項目は、「①タイトル」「②作曲者」「③スタイル」「④調」「⑤テンプレート」の５項目です。これらをあとで変更するには、その曲の編集中に、「情報」（「i」アイコン）から編集します。
3. 「テンプレート」は、曲構成のひな型であり、「①空白」「②32小節AABA」「③32小節ABAC」「④48小節」「⑤96小節」の５種類あります。「①空白」から作業を始めると、小節を付け足していく作業がかなり面倒なので、作成しようとしている曲の構成に近いテンプレートを選ぶか、曲の構成に合うテンプレートがない場合は、小節は、足すよりも消す方が簡単なので、ひとまず「④48小節」か「⑤96小節」を使うとよいでしょう。
4. iRealProでは、1小節を4マス（拍）や2マス（拍）に分解して小節の途中の拍でコードチェンジができます。１曲あたり最大で192マス（拍）まで（1行16マス12行まで）扱うことができます。1小節あたり4マス（拍）で取ると、1行が4小節となり、12行で「④48小節」です。1小節あたり2マス（拍）で取ると、1行が8小節となり、12行で「⑤96小節」になります。13行目を足して使うことはできません。
5. 「⑤96小節」よりも長い曲であっても、繰り返し記号を使って再現することが可能です。繰り返し記号を使っても12行で収められないような曲は、iRealProでは扱いきれません。
6. 曲の再生時に指定できる設定として、「①BPM」「②全体の繰り返し回数」「③曲のキー」「④スタイル」があります。「①BPM」で練習用にテンポを下げたりできます。「③曲のキー」でキーを変えれば自動でコードが移調されます。曲自体のキーを変えたいが移調させたいわけじゃない場合は、その曲の編集中に、「情報」（「i」アイコン）から編集しましょう。

## 3.画面上のボタンの詳細
1. 「コード」:入力モード「レギュラーコード」「小代理のコード」
2. 「・・・」:[コード記号](./cordsymbols.md)の一覧ボタン
3. 「ABC」:[ダカーポ、ダルセーニョ](./repeatmark.md)の一覧ボタン
4. 「<-」:マス（拍）を消して詰める。空白小節はスキップされるので、体裁を整えるのに使えます。
5. 「+>」マス（拍）を足して挿入する。
6. 「-」:minor（m3）
7. 「o」:ディミニッシュ（b5）
8. 「ø」:ハーフディミニッシュ(min7b5)
9. 「∆」:Major7（^7）
10. 「4/4」:拍子
11. 「％」:リピート
12. 「sus」:sus4
13. 「add」:add
14. 「alt」:alt
15. 「+」:オーギュメント（#5）
16. 「/」:分数コード
17. 「S」:コードサイズ（1小節を2マスにする時に）
18. 「↓」:改行
19. 「┌1.」:リピート記号
20. 「A」:リハーサル記号
21. 「coda」:[コーダ](./repeatmark.md)
22. 「| 」:小節線（左）
23. 「 |」:小節線（右）

## 4.特に掘り下げて
1. [コード記号](./cordsymbols.md)
2. [繰り返し記号と、繰り返し記号による進行の例](./repeatmark.md)
3. [ライブラリーに最初から入っている曲](./library.md)

## 5.公式情報源
1. FAQ: https://www.irealpro.com/support
2. ビデオチュートリアル（Android）: https://www.irealpro.com/video-tutorials/android
3. ビデオチュートリアル（iPhone&iPad）: https://www.irealpro.com/video-tutorials/ios
4. ビデオチュートリアル（Mac）: https://www.irealpro.com/video-tutorials/mac
5. Chord symbols: https://technimo.helpshift.com/hc/en/3-ireal-pro/faq/88-chord-symbols-used-in-ireal-pro/?p=android
6. Editor's Buttons: https://technimo.helpshift.com/hc/en/3-ireal-pro/faq/245-editor-s-buttons/?p=android
7. Repeat endings & texts: https://technimo.helpshift.com/hc/en/3-ireal-pro/faq/100-repeat-endings-texts-d-s-d-c-al-coda/?p=android

## 6.詳しくて参考になるサイト
1. https://koyonoto.jp/category/ireal-pro-howto/
2. https://miseruit.com/category/%e9%9f%b3%e6%a5%bd%e5%ae%a4/ireal-pro/
3. https://imokoyuki.com/irealpro/
4. https://fueobake.blog/music/077garageband/