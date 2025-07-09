# 研究ノート
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
- tiles.mbtilesを切り出したいデータの名前
- extract.mbtilesを切り出した後に着けたい名前
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
<video src="https://drive.google.com/file/d/1aJ3UdbF2FT0oPhAXRCsZ18ywcEDCVRm4/view?usp=drive_link" controls></video>

[デモ動画](https://drive.google.com/file/d/1aJ3UdbF2FT0oPhAXRCsZ18ywcEDCVRm4/view?usp=drive_link)