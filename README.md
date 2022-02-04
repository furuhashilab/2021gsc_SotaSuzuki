## 2021gsc_SotaSuzuki
2021年度古橋ゼミ卒論用リポジトリ 鈴木颯汰

# 神奈川県内二郎系ラーメン地理空間情報オープンデータ化の実践

2021年度ゼミ論

青山学院大学 地球社会共生学部 地球社会共生学科

鈴木颯汰/SOTA SUZUKI

学生番号 1A119090

指導教員 古橋大地 教授

© Furuhashi Laboratory/Sota Suzuki, CC BY 4.0

## Abstraction

本研究は2018年度卒業生である渡邊結南氏の卒業論文「日本全国ラーメン二郎店舗位置情報オープン化の実践」に着想を得て、神奈川県内の「二郎系ラーメン」店舗の地理空間情報を、OpenStreetMap（以下OSM）
データベース内に登録し、だれもが自由に二郎系ラーメンのデータにアクセスし、二次利用が可能な状態を構築することが目的である。

## Introduction

本来、中国由来の麺文化である「拉麺（らーめん）」は、日本に伝播する過程の中で独自の進化を遂げ、日本の「ラーメン」という食文化を確立し、2021年現在、代表的な日本の文化の象徴として、広く親しまれている。その中で、1968年に創業した東京都港区三田を拠点としている「ラーメン二郎」というラーメンブランドが存在する。こってりとした味付けと、満腹感を重視したコストパフォーマスの良いラーメンを提供する店舗だ。ラーメン二郎は、三田での創業以降、独特の味つけと提供方法で、日本のラーメンの中で、「二郎系」という１つのジャンルを確立した。2021年現在、ラーメン二郎は日本に41店舗存在し、暖簾分けシステムというシステムの中で、日本各地に店舗を広げている。これらの二郎系ラーメン愛好家は「ジロリアン」と呼ばれ、各地の二郎系店舗を食べ歩き、その情報共有ウェブサイトも数多く存在する。 一方で、2021年の段階ではラーメン店舗マップとして二郎系ラーメンの位置情報が日本全国網羅され、二次利用可能なオープンデータ化がされている例は見当たらないことから、二郎系ラーメンのアプリやマップを作る上で、そのデータをオープンに公開・共有することは車輪の再発明と呼ばれる現地調査重複の無駄を省き、ジロリアンらの活動を支える基礎資料となる。併せて、それらのデータを共有するために必要なプラットフォームには何を選択すべきか検討を行い、OSMデータベース内への格納が現実的であると判断し、現地調査によって得られた日本全国のラーメン二郎店舗情報をマッピングを渡辺氏が、その研究のデータ更新やタギングルールの統一を依田氏が行ったことで、OSMのオープンな地理空間情報プラットフォームを用いて、日本全国のラーメン二郎店舗データ、およびそのメタデータを整理、網羅することによって、誰もが自由にラーメン二郎店舗データにアクセスし、再利用することが可能な状況が構築構築された。 以上のことから、本研究ではOSMでの神奈川県内に存在する「ラーメン二郎」以外の「二郎系ラーメン」の店舗データ、およびそのメタデータを整理していく。

## Method

現在営業をしている二郎系ラーメン54件（2021年12月時点）の店舗データをOSM上で編集、追加を行い公開する。

情報源は現地調査を行うことができた店舗にのみsource=surveyを記入した。ほかは更新が行われている公式Twitterなどを参照したほか、DMなどで連絡し、実際に情報を伺った。

その結果OSM上では、

1. もとから店舗データが存在したのは11店舗、
2. 1のうちamenity=fastfoodとなっていたものは3件
3. 1のうちamenity=restaurantとなっていたものは8件
4. 1のうちcuisine=ramenとなっていたものは8件、他は未入力
5. 1のうちOpening_hoursの記載がないものが9件
6. データのないものが43件

このほかにも本来とは異なる場所に登録されている店舗など問題が多く見受けられた。

![スクリーンショット (58)](https://user-images.githubusercontent.com/72395572/152494561-6a2a4c1b-4ff1-4de2-9a85-47db7214c2ee.png)

## Result

OSM上で整理されていなかった神奈川県内の二郎系ラーメンの店舗データを整理した。

- 店舗データが未入力の店舗を入力

- 全店舗の住所を入力

- 全店舗のOpening_hoursを入力

- amenity=fastfoodに統一

- cuisine=ramen;jiroに統一

- delivery=yes/no

- takeout=yes/no

- drive_through=no

- outdoor_seating=no

- branch=支店の場合入力

- source=survey（筆者が現地調査を行うことができた店舗のみ）

![スクリーンショット (60)](https://user-images.githubusercontent.com/72395572/152494771-cf9e3783-b450-42cf-beb3-1be9afcc1e52.png)

<br>
<br>

これらのタギングルールでデータを入力する前に、「二郎系ラーメン店」の定義を定める必要があった。特に自らの店を二郎系以外の別種のラーメン店であると語りながら、メニューの一部に二郎系ラーメンを含んでいる店舗をOSM上のタギングでcuisine=ramen;jiroと入力すること、例として二郎系ラーメンをメニューの一部に含む家系ラーメン店に、この店の提供する料理は二郎系であると設定してしまうのは不当である。このことから、本研究では「二郎系ラーメン店」を二郎系ラーメンをメインメニューとして提供している店舗と定め、データの収集、編集を行った。

## Discussion

## Conclusion

## 先行研究

https://furuhashilab.github.io/www4yunawatanabe/

https://github.com/furuhashilab/2020gsc_shunsuke-yoda

https://moyashi-ramen-map.herokuapp.com/ / https://qiita.com/paulxll/items/121efb33930c73da1b4f

## 参考文献

参考文献リスト：

https://docs.google.com/spreadsheets/d/1F2YjalmIeecwX4Tb0CkXDuo2kZZ8PqftyySTB4uzjCQ/edit?usp=sharing

## レポート

- Medium

- グラレコ![saisyugurareco](https://user-images.githubusercontent.com/72395572/152490276-e6802f7f-730b-4597-bb27-7230b0632fce.jpg)


## 謝辞

本研究を進めるにあたり、青山学院大学地球社会共生学部教授の古橋大地氏をはじめ、先行研究を行った渡邊結南氏、依田峻輔氏、現地調査に協力していただいた柴山息吹氏にこの場をお借りして深く感謝申し上げます。















