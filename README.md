# GameLauncherの説明
筐体用のゲームランチャー。<br>
Dxライブラリでできています。

## ディレクトリ構造
root/<br>
├ readme.md<br>
├ GameLauncher.exe<br>
├ system.properties<br>
├ readme.md<br>
├ GameDatas/<br>
　└ (各ゲームのディレクトリ)<br>
　　├ .gamelauncher<br>
　　├ 実行ファイル.exe<br>
　　├ サムネ画像.png<br>
　　├ デモ動画.mp4<br>
　　└ readme.txt<br>

## .gamelauncher ファイルの説明
ゲームランチャーに各ゲームを登録する為のjson形式のファイルです。<br>
このファイルで指定するファイルは、各ゲームのディレクトリからの相対パスで指定してください。

### 各変数の説明
- 必須のもの<br>
	- "title"<br>
		サムネ部分に表示されるタイトル名を指定
	- "exe"<br>
		実行ﾌｧｲﾙを指定
- 無くても大丈夫なもの
	- "thumbnail"<br>
		サムネ用の画像ファイルを指定
	- "movie"<br>
		デモ動画ファイルを指定
	- "textFile"<br>
		説明欄に表示する内容のテキストファイルを指定
	- "text"<br>
		説明欄に表示する内容を.gamelauncherで直書きする。<br>
		textFileがある場合はそちらが優先される
	- "isDummy"<br>ダミー指定用です。この変数を書くことで、ランチャーに登録されません。

## system.properties ファイルの説明
ゲームランチャー本体の設定用jsonファイルです。

### 変数の説明
- "afktime"<br>
	一定時間無操作の場合にミュートするまでの時間を秒単位で指定(実数)。Away From Kyoutai