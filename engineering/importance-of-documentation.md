# ドキュメント作成の重要性 Importance of Documentation

### 導入 Introduction
`Design Doc`はシステム設計の際に用いられる設計ドキュメントスタイルですが、Design Docについての解説を見ていくと、「設計」ではないその他の場面でも、いかにドキュメントが大切であるかについてが述べられています。

<br>

A "Design Doc" is a design document style used during system design. However, when looking at explanations about Design Docs, it is also discussed how important documentation is in various other contexts beyond just "design."

<br>

現代の開発には、GitHubが広く使われています。リポジトリに配置する`README`もひとつのドキュメントとして考えることができると思いますので、その重要性を再確認することは開発生産性向上の観点でとても重要なことであると考えます。

<br>

GitHub is widely used in modern development practices. I believe that the README file, which is placed in a repository, can be considered as one form of documentation. Therefore, reaffirming its importance is crucial from the perspective of improving development productivity.

In contemporary development, GitHub is widely utilized. The README file, which can be placed in a repository, can also be regarded as a type of documentation. Therefore, I believe that reconfirming its significance is essential for enhancing development productivity.

<br>

---

### 参考 Reference

<br>

> *Googleではプルジェクトの立ち上げ時に１〜２週間ほどかけてドキュメントを作成する*<br>
参考：[BppLOG「【翻訳】Googleのエンジニアがソフトウェア開発する時に必ず書くドキュメント「Design Docs at Google」」](https://tkybpp.hatenablog.com/entry/2020/08/03/090000)

<br>

[Kelsey Hightowerのツイート](https://twitter.com/kelseyhightower/status/1374372209439895574?s=20)<br>
![kelsey-hightower-tweet](kelsey-hightower-tweet.png "kelsey-hightower-tweet")

---

### Desing Docとは？ What is DesignDoc?
<br>

Desing Docは、Googleなどの最先端の技術企業で取り入れられている設計ドキュメントのスタイルです。エンジニアが開発しようとしているソフトウェア設計の基本的な要点「`何を（What）`」、「`何のために（Whey）`」、「`どのように作るのか（How）`」を説明するために書くドキュメントです。プロジェクトの背景や目的、設計、検討した代案などをドキュメント化します。作成したDesing Docを関係者と共有、議論を行うことによって事前に全体を考察し、精度を高め開発後の`手戻りを減らすことが主な目的`になります。

<br>


A Design Doc is a style of design document adopted by cutting-edge technology companies like Google. It is a document written by engineers to explain the fundamental aspects of the software design they intend to develop, including "What," "Why," and "How." It documents the project's background, objectives, design, and alternative considerations. The main purpose of creating a Design Doc is to share it with stakeholders, engage in discussions, and thoroughly consider the entire project in advance, thereby increasing accuracy and minimizing post-development rework.

<br>

アジャイル方式など繰り返し型の開発や、メンバー全員が１カ所に集まらない分散型のチーム運営など、今どきの開発スタイルを使うチームに導入してもDesign Docは効果を発揮する。

<br>

Design Docs can be effective even when introduced to teams using modern development styles such as Agile methodologies and distributed team management, where development follows an iterative approach and team members may not be physically located in the same place.

<br>

> 開発業務において、ドキュメント作成というのは古来から存在していた。<br>
ここ数年で重要視され始めたのは、開発生産性の向上に注視する組織が増えたことや、開発スタイルの変化によるものも影響していそう。<br>
<br>
Document creation has been a longstanding practice in software development. In recent years, it has gained increasing importance due to organizations focusing on improving development productivity and the impact of changes in development styles.



---

### 意識 Focus

<br>

Design Docまわりの話を聞いたときに、自分の環境に持ち込めるものは何か考えたが、主に次の通り。
1. ドキュメント管理の重要性を再確認する
1. チームにドキュメント管理の文化を根付かせる
1. ドキュメント管理の習慣をつける（つまり、開発フローに組み込む）
1. ドキュメント作成を思考の整理の機会として扱う

<br>

When I heard discussions about Design Docs, I thought about what I could bring to my own environment. Primarily, the following points came to mind:

1. Reaffirming the importance of document management.
1. Cultivating a culture of document management within the team.
1. Developing the habit of document management (i.e., integrating it into the development workflow).
1. Treating document creation as an opportunity for organizing thoughts.

<br>

開発生産性の向上には、いろいろな手段があげられると思いますが、ドキュメント管理を徹底することだけでも効果は高そう。
* ドキュメント作成時に対応不足、仕様漏れに気付くことができる
* コミュニケーションコストの削減することができる
* 認識の齟齬を減らすことができる
* 開発時間の確保につながる

<br>

Improving development productivity can be achieved through various means, but thorough document management alone seems highly effective.Benefits of enforcing document management:

* Detecting inadequate coverage and specification omissions during document creation.
* Reducing communication costs.
* Minimizing discrepancies in understanding.
* Allocating time for development.

<br>

### 開発におけるドキュメントの種類
* 要件定義所
* 基本設計書
* テスト仕様書
* 運用マニュアル（⭐️）
* etc（⭐️）

<br>

Types of documents in development:
* Requirements definition.
* High-level design documents.
* Test specifications.
* Operation manuals (⭐️).
* And more (⭐️).

<br>

### 知識の呪い
* 「人間は他人が自分と同じ知識をもっていると思い込んでいる」（1980年代後半、ハーバード大学）
* 耳慣れない専門用語と使う
* 簡単に見つけられると思ってAPIポイントを示し忘れる

<br>

The curse of knowledge:
* "People tend to assume that others have the same knowledge as they do." (Late 1980s, Harvard University)
* Using unfamiliar jargon without explanation.
* Forgetting to provide API references, assuming they can be easily found.

<br>

*2023.6.19*
