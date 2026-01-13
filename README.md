# 研究ノート
[研究ノートURL](https://arare-bot.github.io/note/)

## 2025 4/7 授業 3H
卒研の説明を受けた後、研究内容をどうするか吉田先生と話し合った。とりあえず伊島のアプリの経路を選択するアルゴリズムを研究することにした。プロコンにも出したいので、資料も作る必要がある。


## 4/8 授業 3H
### 地図アプリに使われているアルゴリズム
地図アプリに使われているアルゴリズムについて調べた。最短経路問題を解くアルゴリズムのダイクストラ法が使われていることがわかった。どういうアルゴリズムか理解することができた。 [ダイクストラ法の説明](https://nw.tsuda.ac.jp/lec/dijkstra/)


### 高専プロコンの資料　
課題がわかりやすいほうがいい
- 解決したい離島での問題
    - 防災(地震、大雨など)
        - ネットがつながらない中で見知らぬ離島で遭難したら大変
    - 観光促進
        - 人口が少ない
- アプリにする利点
    - ローカルで保存しつつ、アップデートで最新の情報も表示できる。


## 4/9 授業 4.5H
### ダイクストラ法のお試し
ダイクストラ法をjsで実装してみた。Clude3.7の力を借りて実装した。
### 来週に向けてやること
- 計算量がO(N**2)なので、もっと高速化したい(時間があれば)
- データの入力をもっとスムーズにしたい
- jsではなくて、Kotlinで実装したい
- プロコンの資料を作る


### アドバイス
- 残った時間で回れる場所を案内する
- タイムキーパー機能


## 4/10 授業　3H
### 伊島アプリの起動
Gitで地図機能を改良するための新しいブランチを作って、アプリをエミュレーターで動かそうとしたが、起動中で止まってしまい、起動できなかった。


## 4/11 授業1.5H
### 伊島アプリの起動
ThinkPadにAndroidStudioを入れて、伊島のアプリを動かすことができた。昨日動かなかった原因はGitHubからクローンした後に、gradleの同期ができていなかったからということがわかった。


## 4/12 
### 卒研アイデア
どの時間のフェリーで帰るかを選択すると、現在の時刻とフェリーの時刻から逆算しておすすめの経路を提案してくれる。自分の身体能力を設定できるようにする。研究の評価は、GoogleMapやYamapが提案するルートと、伊島のアプリが提案するルートを比較する。実際に使ってもらって評価してもらう。




## 4/15 3H
### プロコンの資料作成
過去のプロコンの資料を参考にしながら、作成した。機能を箇条書きで書いた。


## 4/16
### 来週に向けてやること
- プロコンの資料を作る。
- 伊島のアプリの地図機能の部分を違うファイルに分割する。
- ダイクストラ法をアプリで実装する。
- 経路を提案しくれるアルゴリズムを調べる


### アドバイス
プロコンの資料を優先的に作って、月ゼミでプロコンの資料のことを発表する。


## 4/17
### プロコンの資料作成
yamapやgoogleMapなどの類似ステムを調べた。
離島の人口の推移などを調べた。
[国土交通省の離島の資料](https://www.mlit.go.jp/policy/shingikai/content/001478618.pdf)




## 4/23
### 来週に向けてやること
- 月ゼミの資料を作成する。
- プロコンの資料を作成する
- 伊島のアプリの地図機能の部分を違うファイルに分割する。


## 4/24
### 避難確認のアイデア
マイナンバーカードや免許証で本人確認をしたアプリに、避難できたかどうかを確認する機能を付ければ確実。LINEやYouTubeなどの誰もがインストールしているアプリにその機能が付けば実用的。


## 4/28 1.5H
### プロコンの資料作成
システム構成図を作成した。


## 4/30
### 来週に向けてやること
- プロコンの資料を作成する


## 5/1
### プロコンの資料作成
- レイアウトを変えたり、説明を短くしたりした。


## 5/7
- 卒研の内容を考える


## 5/14 1H
### 地図アプリ作成
- AndroidStudioで使える地図アプリのライブラリを探した。[Map Libre Native](https://github.com/maplibre/maplibre-native?tab=readme-ov-file)がクロスプラットフォーム対応で、オープンソースなのでよさそう。


### 来週に向けてやること
- MapLibreNativeなどを試して、ユーザーが遊歩道を作ることができるアプリを作成する。


## 5/15 3.0H
### MapLibreのお試し
MapLibreはオープンソースの地図描画ライブラリで、OSM(OpenStreetMap)の地図データを表示することができることがわかった。実際に動かしてみるために、AndroidStudioの依存関係に
```kotlin
implementation ("org.maplibre.gl:android-sdk:11.8.7")
```
を追加して、layoutフォルダに
```xml
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
        android:layout_height="match_parent">
    <org.maplibre.android.maps.MapView
        android:id="@+id/mapView"
        android:layout_width="match_parent"
        android:layout_height="match_parent" />


</RelativeLayout>
```
を書き込んで使おうとしたが、アプリがストップして開くことができなかった。


## 5/21
### 来週に向けてやること
- MapLibreを動かせるようにする
- AndroidStudioの理解していないところを調べる(res/layoutの役割など)
- 月ゼミの資料作成
- プロコン資料(特許)


## 5/27
### 月ゼミアドバイス
使えない道を選択して道案内できる
人によってエッジの重みを変える
地図を作る機能で難易度を設定できるように
避難所とフェリー乗り場までの時間を表示


## 5/28
### 来週に向けてやること
- MapLibreを動かせるようにする
- AndroidStudioの理解していないところを調べる(res/layoutの役割など)


## 5/29
### 地図アプリの地図を表示する手順
1. 地図データ
    - 地図データには緯度経度の点であるノードやノードを複数つないだ線がある。オープンソースのOSMの地図データ(.osm、XML形式)やクローズドなGoogleの地図データなどがある。
2. タイルサーバー
    - 地図データを地図の画像に変換したり、ベクタータイル(.pbf)を提供するサーバー。ベクタータイルとは道路や建物、公園、川などの形・位置・属性情報が“データ（ベクター＝線や多角形、属性）”として入っているもの。
3. 地図描画用ライブラリ
    - タイルサーバーとやり取りしてベクタータイルを取得して、画面に表示するライブラリ。


## 6/11 
### 地図アプリロードマップ
1. オフラインで地図を表示
    1. オフラインで地図を表示
    2. ピンを表示して情報を表示できるように
    3. 現在地を表示できるように
2. Ishimapとマージ
3. 道案内機能の実装
    1. 現在地と目的地から最短経路を表示
    2. 道の難易度によって重みをつけて案内
    3. 使えない道を選択できるように
    4. 現在地から避難所とフェリー乗り場までの時間を表示
4. ユーザーが地図を追加できる機能の実装


## 7/2
### 地図をオフラインで表示


[神戸のベクタータイルデータ](https://data.maptiler.com/downloads/dataset/osm/asia/japan/kobe/#9.39/34.7888/135.123)
試しに神戸の地図データ(pbf)をダウンロードして、オフラインで表示しようとしたが、エラーが出て、表示されない。


```log
2025-07-02 10:55:03.163 10697-10738 Mbgl com.example.maplibretest E {RenderThread 81}[Style]: Failed to load tile 11/1792/813=>11 for source vector-tiles: unknown pbf field type exception
```


コードやダウンロードした地図データを確認したが特に問題は見当たらなかった。ネット上を探して問題を見つけていく。無理そうだったら、別の地図データを使ってアプリを作ってみる。

## 7/3
### 地図をオフラインで表示
[MapLibreのドキュメント](https://maplibre.org/maplibre-native/android/api/)
公式ドキュメントを見てみたが、APIの説明をしているだけで、よくわからなかった。そのためGitHubで参考になりそうなプロジェクトを探すことにした。

[map-libre-demo](https://github.com/TonyGnk/map-libre-demo)
探した結果、このプロジェクトが見つかった。Ramani MapsというMap LibreのAndroid向けのラッパーを使って、オフラインで地図を表示している。このプロジェクトを参考にオフライン地図を作っていく。

オフラインで地図を表示するために必要な手順をまとめる。Android Studioで新しいプロジェクトを作成したら、build.gradle.ktsに次の依存関係を追加する。
```kotlin
implementation("org.ramani-maps:ramani-maplibre:0.7.0")
```
そして、map-libre-demoのMainAcctivity.ktとMapStyleManager.ktを作成する。その後、app/src/mainにassetsフォルダを作成し、プロジェクトの中身をコピペする。
これでアプリを起動すると、マルタの地図がオフラインで表示される。
別の地図をオフラインで表示させたい場合
 - 表示させたい地図データ(.mbtiles )assets内に置く
 - MapStyleManager.ktのMBTILES_FILENAMEを変更する(例えばKobe.mbtiles)
``` kotlin
companion object {  
    private const val STYLE_FILENAME = "style.json"  
  private const val MBTILES_FILENAME = "Kobe.mbtiles"  
  private const val FILE_URI_PLACEHOLDER = "___FILE_URI___"  
}
```

## 7/8
###  地図データの切り出し
[日本の地図データ](https://data.maptiler.com/downloads/asia/japan/)
このサイトで日本の地図データをダウンロードすることができる。しかし、このままでは容量が1.83GBもあるため、必要な場所だけを切り出す必要がある。
必要な場所を切り出すには、Dockerをインストールした後に、切り出したい.mbtilesがあるディレクトリで次のコマンドを実行すればできる。(Windowsの場合)
```bash
docker run --rm -v "%cd%":/data openmaptiles/openmaptiles-tools mbtiles-tools copy /data/tiles.mbtiles /data/extract.mbtiles --reset --auto-minmax --bbox=...
```
- tiles: .mbtilesを切り出したいデータの名前
- extract: .mbtilesを切り出した後に着けたい名前
- --bbox: 緯度経度の四隅をW,S,E,Nの順で指定

OpenMapTiles Toolを使っている。

### 現在地の表示
Ramani Mapsで地図上にピンを立てるには、MapLibre()を呼び出すときのコールバック関数にSymbol()を渡して、その中でいろいろと設定する。
```kotlin
MapLibre(  
    modifier = modifier,  
    styleBuilder = styleBuilder,  
    cameraPosition = cameraPosition  
) {  
  // 現在地が取得できたらマーカーを表示  
  currentLocation?.let { loc ->  
  Symbol(  
            center = LatLng(loc.latitude, loc.longitude),  
            size = 0.1f,  
            color = "#00AAFF",  
            isDraggable = false,  
            imageId = R.drawable.images // 任意のマーカー画像  
  )  
}  
```
ピンの位置は次のように設定する。
```kotlin
center = LatLng(緯度,軽度)
```
今回は2秒ごとに位置情報を取得して、反映させるようにした。
<video src="https://drive.google.com/uc?export=download&id=1aJ3UdbF2FT0oPhAXRCsZ18ywcEDCVRm4" controls></video>

[デモ動画](https://drive.google.com/file/d/1aJ3UdbF2FT0oPhAXRCsZ18ywcEDCVRm4/view?usp=sharing)

## 7/11
### 地点の追加
まず、地図データは .mbtilesという拡張子。阿南の地図データなら、Anan.mbtilesという感じ。ここにデータを追加したいが、このままだとバイナリ形式なので、読み書きが難しい。そこで、一度 .geojsonというJSONのような拡張子に変換する。そこでデータを編集した後に、再度 .mbtilesに戻せばよい。下は阿南高専を示すGeoJSONの例。
```json
{ "type": "Feature", "id": 3145034231, "properties": { "class": "school", "name": "徳島県立阿南工業高等学校", "name:ja": "徳島県立阿南工業高等学校", "name:latin": "tokushimaken ritsu anan kougyou koutougakkou", "name:nonlatin": "徳島県立阿南工業高等学校", "name_de": "徳島県立阿南工業高等学校", "name_en": "徳島県立阿南工業高等学校", "name_int": "tokushimaken ritsu anan kougyou koutougakkou", "rank": 1, "subclass": "school" }, "geometry": { "type": "Point", "coordinates": [ 134.639559, 33.925179 ] } }
```
このためにtippecanoeというツールを使う。  
[tippecanoe](https://github.com/felt/tippecanoe?tab=readme-ov-file)  
試しに、GeoJSONに変換して地点を追加して、元に戻そうとしたが、元に戻すときに1時間以上かかってしまい戻すことができなかった。

## 7/17
### 地点の追加(レイヤー)
阿南の地図データに点を追加、Anan.mbtiles → GeoJSON → mbtiles をしようとすると、うまくいかなかった。調べたところ、このような変換は推奨されていないことがわかった。Mbtilesにはいくつものレイヤーがあるが、この変換をしてしまうと、そのレイヤーが1つになってしまう。  
そこで、新しいMbtilesを作って、Anan.mbtilesに重ねて表示する方法を試した。下のようなnew_points.geojsonというファイルを使って、阿南高専の近くに新しい地点を追加してみた。

```json
{
  "type": "Feature",
  "id": 9999999999,
  "properties": {
    "class": "college",
    "name": "Test Point",
    "name:ja": "テスト地点",
    "rank": 1,
    "subclass": "college"
  },
  "geometry": {
    "type": "Point",
    "coordinates": [134.667983, 33.897995]
  }
}
```
しかし、地図上には新しい地点が表示されることはなかった、、、変換に時間がかかることもなく、エラーも出なかった。  
何が原因なのか予想がつかないので、ネット上でうまくいっている事例を探して、原因を見つけていく。

## 9/6
### 地図機能で作るもの
- gpkgに新しく追加した、地点、道、POI をgeojsonにして、出力。

## 10/3
### チェックイン機能
避難所と観光地点と港でここに来たボタンを押せるようにした。gpsの現在位置の距離が何Mに近づいたらボタンを有効化する、という設定をした。

## 10/6
### POIの更新
ユーザーが追加した観光ポイントがアプリに反映されるようにした。サーバからGeoJsonを取得して、それを描画している。
使用する関数を別のファイルに分けた。data/GeoJsonPoiParser.kt　と data/PoiRepository.kt というファイルを作成した。GeoJsonPoiParser はjsonをkotlinのPOI(地図上の特定のポイント)オブジェクトに変換するための関数をまとめたもの。
PoiRepository は POI の情報をサーバから取得して、キャッシュに保存するもの。
これらの関数を地図を描画する際に呼び出して、観光ポイントを更新するようにした。

## 10/10
### ルート更新ボタン
現在地に戻るボタン、POI,ルートの更新ボタンを実装した。ETag　というものを使い、データに変更があった場合のみ取得して、保存するようにしようとしたが、毎回保存されてしまう。サーバ側でGASを使っているのが問題だと思う。

## 10/11
### ルーティングファイルの修正
阿南市と松江市を合体させたルーティングファイルで、伊島のデータが壊れていた。伊島に新しい道を追加した状態で、松江市のデータと合体させるときに壊れたようだ。初期状態の阿南市と松江市のデータを合体させた後に、新しい道を追加するようにしたら、この問題は解決した。

新しい道には ID や、どこの地点同士をつなぐかなどの情報が入っておらず、Python で自動補完する仕組みになっている。これが原因で合成が上手くいかなかったのだろう。

## 10/21
## 地図の変更
MapStyleManager の setupStyle関数の引数で、使用する地図の名前を受け取って、それを適用するようにした。これをassets内から読み取って使用している。

次は、ユーザーがボタンを押して指定した地図をsetupStyle関数の引数に渡して、それを描画するようにしたい。その後、地域ごとにディレクトリを作成して、その地域のデータをまとめておくようにしたい。最後にサーバーと連携できるようにする。

### 今週やること
- 10/31 までにSICE の予稿を作る
- ボタンで地図が選べるようにする
- (できれば) アプリ内でGPXデータが取れるようにする

## 11/12
### 地図の選択
アプリ内にボタンを配置して、表示する地図を切り替えられるようにした。阿南市と、松江市の地図を切り替えられることが確認できた。

次のような selectedMbtilesName という状態付き変数を定義した。ボタンを押すとこの値が変化し、地図が再描画される。

```kotlin
var selectedMbtilesName by remember {
    mutableStateOf("anan_minami_tokushima.mbtiles")
}
```
## 11/19
### 大きくなったコードを分割
MapScreen.ktという地図を表示させているファイルが1000行を超えてきて、どういった処理をしているのかわかりづらくなってきた。そこで、機能ごとにファイルを分割してわかりやすくしようと思った。

Kotlin でのアプリ開発では View Model というクラスを作って機能を分割する。ViewModel は、画面に必要な状態（State）と、その状態を更新するための処理をまとめて管理するクラスである。要するに、11/12 のノートで書いたような状態付き変数とボタンを押したときの処理のようなものを別ファイルに書くということである。

試しに MenuSheet というメニュー画面で使用している状態付き変数とボタンを押した後の動作を View Model の別ファイルに移動させた。 _MapScreenViewModel.kt_ というファイルを作り、ここにまとめた。これからもViewModelのほうにコードを移行させていき、保守管理しやすくしていきたい。


## 12/10
### 週ゼミ
年末までにアンケートをやる。年明けから論文を書いていく感じ。

## 12/15
### 地点の削除、編集
実際にアプリを使ってもらうにあたって、今のままでは地点の追加しかできないため不便だ。間違って追加した地点を消したり、編集したりすることができない。そこで削除編集できるようにする。

### サーバー側の問題
今はさくらインターネットのサーバーで地図関連のapiを動かしている。そのままでは https 通信ができないので、GAS をサーバとアプリの間に置くことで https 通信を実現している。しかしこの状態では1度に通信できる容量に制限があったり、json形式でしか送れないため、画像をBASE64で送り、デコードする必要がある。そこで、サーバーもさくらのものではなく、無料のホスティングサービスを利用して、 https 通信できるようにする。

### 構成
- API : Vercel
- データベース : Supabase
- フレームワーク : Next.js

いくつかサービスを比較してみた結果、apiの配信先として Vercel 、データベースとして Supabase を使用することにした。どのサービスも同じようなことができたが、使ったことがあり、人気だったので選んだ。

## 1/5 
### POI を取得するの URL
 - 全取得 (GET) : https://poi-api.vercel.app/api/pois
 - 新規作成 (POST) :  https://poi-api.vercel.app/api/pois
 - 特定のidのデータを取得 (GET) :  https://poi-api.vercel.app/api/pois/[id]
 - 更新 (PATCH) :  https://poi-api.vercel.app/api/pois/[id]
 - 削除 (DELETE) :  https://poi-api.vercel.app/api/pois/[id]

アプリの全取得URLを Vercel のものに変更したが、アプリにPOIのピンが表示されない。おそらく、 ID が UUID になっているのが原因だと思う。


