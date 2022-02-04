## 2021gsc_SotaSuzuki
2021年度古橋ゼミ卒論用リポジトリ 鈴木颯汰

# 神奈川県内二郎系ラーメン地理空間情報オープンデータ化の実践

2021年度ゼミ論

青山学院大学 地球社会共生学部 地球社会共生学科

鈴木颯汰/SOTA SUZUKI

学生番号 1A119090

指導教員 古橋大地 教授

© Furuhashi Laboratory/Sota Suzuki, CC BY 4.0

## Abstract

本研究は2018年度卒業生である渡邊結南氏の卒業論文「日本全国ラーメン二郎店舗位置情報オープン化の実践」に着想を得て、神奈川県内の「二郎系ラーメン」店舗の地理空間情報を、OpenStreetMap（以下OSM）
データベース内に登録し、だれもが自由に二郎系ラーメンのデータにアクセスし、二次利用が可能な状態を構築することが目的である。

## Introduction

本来、中国由来の麺文化である「拉麺（らーめん）」は、日本に伝播する過程の中で独自の進化を遂げ、日本の「ラーメン」という食文化を確立し、2021年現在、代表的な日本の文化の象徴として、広く親しまれている。その中で、1968年に創業した東京都港区三田を拠点としている「ラーメン二郎」というラーメンブランドが存在する。こってりとした味付けと、満腹感を重視したコストパフォーマスの良いラーメンを提供する店舗だ。ラーメン二郎は、三田での創業以降、独特の味つけと提供方法で、日本のラーメンの中で、「二郎系」という１つのジャンルを確立した。2021年現在、ラーメン二郎は日本に41店舗存在し、暖簾分けシステムというシステムの中で、日本各地に店舗を広げている。これらの二郎系ラーメン愛好家は「ジロリアン」と呼ばれ、各地の二郎系店舗を食べ歩き、その情報共有ウェブサイトも数多く存在する。 一方で、2021年の段階ではラーメン店舗マップとして二郎系ラーメンの位置情報が日本全国網羅され、二次利用可能なオープンデータ化がされている例は見当たらないことから、二郎系ラーメンのアプリやマップを作る上で、そのデータをオープンに公開・共有することは車輪の再発明と呼ばれる現地調査重複の無駄を省き、ジロリアンらの活動を支える基礎資料となる。併せて、それらのデータを共有するために必要なプラットフォームには何を選択すべきか検討を行い、OSMデータベース内への格納が現実的であると判断し、現地調査によって得られた日本全国のラーメン二郎店舗情報をマッピングを渡辺氏が、その研究のデータ更新やタギングルールの統一を依田氏が行ったことで、OSMのオープンな地理空間情報プラットフォームを用いて、日本全国のラーメン二郎店舗データ、およびそのメタデータを整理、網羅することによって、誰もが自由にラーメン二郎店舗データにアクセスし、再利用することが可能な状況が構築構築された。 以上のことから、本研究ではOSMでの神奈川県内に存在する「ラーメン二郎」以外の「二郎系ラーメン」の店舗データ、およびそのメタデータを整理していく。

## Method

現在営業をしている二郎系ラーメン54件（2021年12月時点）の店舗データをOSM上で編集、追加を行い公開する。

情報源は現地調査を行うことができた店舗にのみsource=surveyを記入した。ほかは更新が行われている公式Twitterなどを参照したほか、DMなどで連絡し、実際に情報の聞き込みを行った。

その結果OSM上では、

1. もとから店舗データが存在したのは11店舗、
2. 1のうちamenity=fastfoodとなっていたものは3件
3. 1のうちamenity=restaurantとなっていたものは8件
4. 1のうちcuisine=ramenとなっていたものは8件、他は未入力
5. 1のうちOpening_hoursの記載がないものが9件
6. データのないものが43件
7. 閉業していたものが2件

存在した

このほかにも本来とは異なる場所に登録されている店舗など問題が多く見受けられた。

![ayumu](https://user-images.githubusercontent.com/72395572/152496585-9b2616f1-4ea6-49f3-9495-6066ef3af15b.png)

## Result

OSM上で整理されていなかった神奈川県内の二郎系ラーメンの店舗データを整理した。

- 店舗データが未入力の店舗を入力

- 全店舗の住所を入力

- 全店舗のOpening_hoursを入力

- 全店舗のopening_hours:covid19を入力

- amenity=fastfoodに統一

- cuisine=ramen;jiroに統一

- delivery=yes/no

- takeout=yes/no

- drive_through=no

- outdoor_seating=no

- branch=支店の場合入力

- source=survey（筆者が現地調査を行うことができた店舗のみ）

![editor](https://user-images.githubusercontent.com/72395572/152496616-469b0406-8f4a-44c3-afe2-9afc9c07443a.png)

<br>
<br>

これらのタギングルールでデータを入力する前に、「二郎系ラーメン店」の定義を定める必要があった。特に自らの店を二郎系以外の別種のラーメン店であると語りながら、メニューの一部に二郎系ラーメンを含んでいる店舗をOSM上のタギングでcuisine=ramen;jiroと入力すること、例として二郎系ラーメンをメニューの一部に含む家系ラーメン店に、この店の提供する料理は二郎系であると設定してしまうのは不当である。このことから、本研究では「二郎系ラーメン店」を二郎系ラーメンをメインメニューとして提供している店舗と定め、データの収集、編集を行った。

## Discussion

主な論点は以下の3点である。

1. 二郎系ラーメンに適したcuisineタグのvalueの検討を行った結果、渡邊氏のリファレンスによればcuisine=ramen;jiroは「ラーメン二郎」のみを指すタグではなく、あくまで「二郎系」を指すものであったことから、cuisine=ramen;jiroという組み合わせのタグセットを選択した。

2. 複雑な営業時間をしている店舗のOpening_hoursの表記を検討した。中でもラーメン岩佐　下鶴間店の営業時間は11:00 ~ 15:30 / 17:30 ~ 23:00、金土は23:30まで営業、土日祝は中休みなしの通し営業、月曜定休で月曜日が祝日の場合翌日火曜が休みというとても複雑なものがあり、土日祝の表記についてFacebookのOSM Communityにて質問をしたところ回答を得られた。

<img src="https://user-images.githubusercontent.com/72395572/152511055-b334b4ef-c10e-4fea-99ff-015f6b9e1ebe.jpg" width="40%">

また、 新型コロナウイルスが猛威を振るっている現在、Opening_hoursのタグのほかに新たにOpening_hours:covid19が存在していた。そのため、神奈川県蔓延防止等重点措置の要請に応じて時短営業を実施している店舗の営業時間が普段と異なる点に注意を払い、通常の営業時間をOpening_hoursに、時短の営業時間をOpening_hours:covid19にそれぞれ入力した。

3. ラーメン二郎とは異なり、お持ち帰りやUberEatsなどのデリバリーのサービスを実施している店舗が存在することから、その情報の収集を漏らさないようにし、delivery、takeawayのタグにその有無を記入した。

## Conclusion

本研究を通じて、筆者が現地調査と聞き込み行った神奈川県内の二郎系ラーメン54店舗分の地理空間情報をOSMデータベース内に登録し、既存のデータの見直しを行った。また、渡邊氏のリファレンスにのっとり新たな「二郎系ラーメン」の店舗のメタデータをOSM上で編集、追加し、公開することができた。しかしながら、新型コロナウイルスの影響で新たにお持ち帰りのサービスを始める店舗が多く出てくることが予想され、その情報をどのように素早く反映するか、また現地調査を実施することのできていない店舗が多く残ったことや、コロナ期間前の営業時間についてデータを得られなかったことが課題であり、今後徐々に入力していく必要があると考えている。

## 先行研究

https://furuhashilab.github.io/www4yunawatanabe/

https://github.com/furuhashilab/2020gsc_shunsuke-yoda

https://moyashi-ramen-map.herokuapp.com/ / https://qiita.com/paulxll/items/121efb33930c73da1b4f

## 参考文献

リスト：

https://docs.google.com/spreadsheets/d/1F2YjalmIeecwX4Tb0CkXDuo2kZZ8PqftyySTB4uzjCQ/edit?usp=sharing

## レポート

- 発表スライド

https://docs.google.com/presentation/d/1ZACPmiuHIaMFY765dK9UGhdXVn9lRvfLKUUAnlpBgdY/edit?usp=sharing

- Medium

https://medium.com/furuhashilab/%E4%BA%8C%E9%83%8E%E7%B3%BBmap-353e693162b8

- グラレコ![saisyugurareco](https://user-images.githubusercontent.com/72395572/152490276-e6802f7f-730b-4597-bb27-7230b0632fce.jpg)


## 謝辞

本研究を進めるにあたり、青山学院大学地球社会共生学部教授の古橋大地氏をはじめ、先行研究を行った渡邊結南氏に助言を賜ったほか、依田峻輔氏、現地調査に協力していただいた柴山息吹氏にこの場をお借りして深く感謝申し上げます。















