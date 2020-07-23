# spreadsheet-podcast

スプレッドシートに記載した情報からポッドキャストのfeed作成と公開

# 使い方

claspやGoogleAppsScriptsを使った事がある人向けの解説

    $ cd /path/to/repo
    $ npm install
    $ clasp create
    ? Create which script?
      standalone
      docs
    ❯ sheets
      slides
      forms
      webapp
      api
    $ vi src/Code.ts

以下の指定を変更

```
// xmlファイルの出力フォルダーのID指定
var FOLDER_ID = "<xmlファイルの出力フォルダーのID指定>";
```

    $ clasp push

スプレッドシート名「Spreadsheet-podcast」が作成されているので
1行目が「title, pubDate, audioUrl, size, type, url」の並びのシート名を作成。ポッドキャストとして出力したい情報を記載


関数「run」を実行(トリガーとして追加がおすすめ)、出力された「podcast.xml」ファイルのIDを控える

```
https://drive.google.com/uc?export=view&id=<ファイルID>
```

がRSSフィードURLになっているので各種ポッドキャストアプリで購読を行う
