# 映えコーチ カメラ

スマホのブラウザで開くと、ライブ映像に枠線と撮影アドバイスを重ねるWebアプリ。映像は端末内だけで処理します。

- 水平・傾き(スマホのセンサー)
- 暗さ・白飛び
- ブレ・ピンボケ
- 主役の位置(三分割の交点)
- 15秒動画(カットごとの指示つき)

カメラはHTTPSのページでのみ動きます。GitHub Pagesで公開して使います。

## 画面サイズの根拠

- フィードの写真: 幅1080px以上、縦横比 1.91:1〜4:5 が対象(Instagramヘルプ「Image resolution of photos you share on Instagram」)。同ヘルプの別版では下限が3:4と書かれていて、版によって表記が異なる。
- リールの安全な範囲: 上14% 下35% 左右6%(Meta Ads Guide、広告向けの案内)。
- ストーリーの安全な範囲: 上14% 下20%(Meta Ads Guide、Instagramヘルプ)。
- プロフィールのグリッド3:4: 公式の記載を確認できなかったため、アプリからは外した(4:5で撮れば公式の範囲内)。

## 撮り方のコツの根拠

検索で確認できたもの(アプリ内では「✔考え方は資料で確認」と表示):

- 料理: 立体的な皿は斜め45°、平たい料理は真上、背の高い層のある料理(バーガーなど)は正面寄り。光は窓からの横光、カメラ側からの正面光は平らに写る。
  - [PetaPixel: Food Photography Guide](https://petapixel.com/food-photography-guide/)
  - [Expert Photography: 6 Best Food Photography Angles](https://expertphotography.com/best-camera-angles-food-photography)
  - [Canon: Tips for Amazing Food Photography](https://www.usa.canon.com/learning/training-articles/training-articles-list/cooking-with-the-camera-tips-for-amazing-food-photography)
- 建物・鳥居: カメラを上に向けると垂直線がすぼまる。カメラを水平に保ち、一歩下がる。標準のiPhoneカメラの水平器は横の傾きだけを示し、前後の傾きは示さない。
  - [Photo Ephemeris: Architectural Photography Part 1](https://photoephemeris.com/en/articles/architectural-photography-part-1-perspective)
  - [Digital Camera World: converging verticals](https://digitalcameraworld.com/features/what-are-converging-verticals-and-how-can-you-fix-them)
- 空・夕焼け: 明るい所をタップして露出を合わせ、スライダーで少し下げる。太陽を画面に入れると空が白く飛ぶ。暗い前景はシルエットにする。
  - [Apple: Use iPhone camera tools to set up your shot](https://support.apple.com/guide/iphone/set-up-your-shot-iph3dc593597/ios)
  - [Picture Correct: Photograph Sunsets on Your Phone](https://www.picturecorrect.com/?p=107179)
  - [Sony: Shoot Skyscapes](https://www.sony.ca/en/electronics/support/e-mount-body-ilce-1-series/articles/00223366)
- 花・近接: 背景は無地に近い場所、逆光で花びらが透ける、近づくと手ブレしやすい。
  - [Expert Photography: Smartphone Flower Photos](https://expertphotography.com/smartphone-flower-photos)
  - [Adobe: macro photography iPhone tips](https://www.adobe.com/creativecloud/photography/hub/guides/macro-photography-iphone-tips)
- リール動画: 冒頭の1〜3秒で引きつける、一番伝えたいことを早く出す、1本1テーマ、縦で撮る(第三者の解説記事に基づく)。
  - [Hootsuite](https://blog.hootsuite.com/instagram-tv/) / [Social Media Today](https://socialmediatoday.com/news/instagram-shares-tips-on-video-creation/827172)

確認できていないもの(アプリ内では「経験則」と表示):

- 各被写体の目標の角度の数値(おにぎり35°など)、15秒動画のカット割り、小物や人物の細かいコツ。
- 以前入れていた「近接は5〜10cm」は資料で確認できなかったため削除した。
- スマホの最短ピント距離の数値は見つからなかった。

## 他のカメラアプリから取り入れた機能

- いまやること1つを大きく表示(Pixel 10 の Camera Coach の「1つずつ順に案内する」方式を参考)
- 白飛び表示(ゼブラ)とピント表示(フォーカスピーキング)(Halide を参考)
- 全部OKになったら振動で知らせる(Android のみ)、シャッターが緑になる(Halide・Foodie を参考)
- オート撮影: 条件が全部OKのまま1秒保つと自動で撮る(真上撮りでシャッターを押す手ブレを防ぐ)
- お手本を重ねる: 写真を選ぶか、撮った写真を半透明で重ねて同じ構図を再現(ゴースト表示のカメラアプリを参考)
- ズームとライト: 対応する端末(主に Android Chrome)でだけ表示。iPhone の Safari では出ない
