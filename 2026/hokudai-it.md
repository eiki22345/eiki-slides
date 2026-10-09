---
marp: true
theme: default
paginate: true
size: 16:9
header: "夏休みにやったこと | 松森瑛己"
footer: "2026-10-09 | 北大IT LT"
style: |
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;700;900&family=Noto+Sans+JP:wght@400;700;900&family=JetBrains+Mono:wght@500;700&display=swap');

  section {
    --main: #9acd00;   /* 黄緑（文字には使わない） */
    --pale: #f3f9dc;
    --black: #1f2319;
    --gray: #80857a;

    font-family: Inter, 'Noto Sans JP', sans-serif;
    background: #fff; color: var(--black);
    font-size: 40px; line-height: 1.65;
    padding: 90px 90px 80px 100px;
    border-left: 16px solid var(--main);
    justify-content: center;
  }
  section > header, section > footer { color: var(--gray); font-size: 18px; left: 100px; right: 90px; }
  section > header { top: 28px; }
  section > footer { bottom: 26px; }
  section::after { content: attr(data-marpit-pagination) ' / ' attr(data-marpit-pagination-total); color: var(--gray); font-size: 18px; right: 90px; bottom: 26px; }

  h1 { font-size: 80px; font-weight: 900; line-height: 1.3; margin: 0 0 20px; }
  h2 { font-size: 56px; font-weight: 900; line-height: 1.4; margin: 0 0 28px; }
  h3 { font-size: 36px; font-weight: 700; color: var(--gray); margin: 0 0 12px; }
  /* 強調は文字色ではなく黄緑のマーカー下線 */
  strong { font-weight: 900; background: linear-gradient(transparent 60%, var(--main) 60%); }
  code { font-family: 'JetBrains Mono', monospace; background: var(--pale); color: var(--black); padding: 2px 10px; border-radius: 6px; }
  ul, ol { padding-left: 1.2em; }
  li::marker { color: var(--main); }
  blockquote { margin: 20px 0; padding: 6px 32px; border-left: 10px solid var(--main); font-size: 52px; font-weight: 900; line-height: 1.5; }
  blockquote strong { background: none; }

  section.lead { text-align: center; }
  section.title { text-align: left; }

  .red, .green, .blue { font-weight: 900; background: linear-gradient(transparent 60%, var(--main) 60%); }
  .small { font-size: 0.62em; line-height: 1.5; }
  .muted { color: var(--gray); font-size: .65em; }
  .big { font-size: 1.4em; font-weight: 900; }
  .term { font-family: 'JetBrains Mono', monospace; font-size: 34px; background: var(--black); color: #fff; border-radius: 12px; padding: 24px 36px; text-align: center; }
  .p { color: var(--main); }
  /* 文章＋画像/動画の横並び */
  .media { display: flex; gap: 48px; align-items: center; }
  .media > div { flex: 1; }
  .media img, .media video { width: 100%; border-radius: 10px; box-shadow: 0 6px 24px rgba(0,0,0,.2); }
  .media.wide > div:first-child { flex: 0 0 34%; }
  img.photo, .photo img { border-radius: 8px; box-shadow: 0 4px 16px rgba(0,0,0,.15); }
---

<!-- _class: lead title -->
<!-- _paginate: false -->

# 夏休みにやったこと<br>いろいろ
### 〜インターン,linux入門,ターミナルすけすけ界隈〜

<span class="muted">北大IT LT / 北海学園大学３年 / 松森瑛己</span>

---

## 自己紹介

松森瑛己 / 北海学園大学英米文化学科３年

- 最近、シャニマスの曲を聞くのにハマっている
- お気に入りは day the sky、シャイノグラフィ

---

<!-- _class: "" -->
## 本日のアジェンダ（目次）

<div class="small">

1. 土日14時間寝て終わった話
2. 東京のインターンに参加
3. 職業エンジニアの難しさと楽しさ（命名・慣習・費用対効果）
4. 穏やかな先輩が飲み会で突然Linuxを語り出した件
   〜Thinkpadを取り出して~
5. 先輩の話を聞いて、インターン中にUbuntuインストール
6. apt?snap?なんじゃそれ
7. VirtualBoxとメモリ使用量との格闘
8. ターミナルすけすけ界隈との遭遇
9. Ghosttyの描画が早すぎてキモい話
10. Herdrによる複数エージェント並列管理
11. Neovim (LazyVim) 入門
12. まとめ ＆ Linux元年の幕開け

</div>

---

<!-- _class: lead -->
## 安心してください、**つまみます！**

<span class="muted">（※ 5〜10分で駆け抜けます）</span>

---

<!-- _class: lead -->
## 東京に**インターン**に<br>行ってきた

<!--
写真案: 東京の写真
![bg right:35%](images/tokyo.jpg)
-->

---

<!-- _class: lead -->
## インターンで得たこと

### 職業エンジニアとして働く<br>**難しさ**と**楽しさ**

---

## **難しさ**：作れたら終わりじゃない

- 他人が見てわかる**命名**か？
- 既存の**慣習**に従っているか？
- **費用対効果**は合っているか？

---

## **楽しさ**：難しいことが<br>できたときの面白さ

- 難しいこともある
- でも、課題を解決したら楽しい。

---

## **学んだこと**

- 自分の**現在のレベル**がわかる
- すごい人がたくさんいる
- **面白い人**（と変人）に出会える

---

![bg right:44%](images/thinkpad.jpg)

## チーム懇親会で、<br>落ち着いてる先輩に異変

> 「おい、お前らLinuxを使え。<br>**Linuxはいいぞ**」

---

<!-- _class: lead -->
## 実は前から、<br>Linuxの導入を**検討**していた

---

<!-- _class: lead -->
## 先輩の話を聞いて、<br>**インターン中**に **Ubuntu** を導入

---

<!-- _class: lead -->
## apt? snap?

---

## 使いたいアプリが動かない

- 最新版が降ってこない
- どんなアプリを探すのが楽しい
- エラーが出た際自分で解決する必要がある
- 最悪`VirtualBox`

<!--
写真案: Ubuntuのデスクトップ
![bg right:35%](images/ubuntu.png)
-->

---

## でも、なぜか**楽しい**

- メモリ消費が少なくて動作が軽い！
- 無駄なアプリがないスッキリ感
- 自分のPCを完全に掌握している<br>**Linux使ってるでドヤ!「アイデンティティ」** の獲得 ✨

---

## 先輩の画面が<br>**すけすけ**だった

> 背景が透けてて、ペインが4分割…！？<br>かっこよすぎ…

---

## 爆速ターミナル **Ghostty**

<div class="media wide">
<div>

- 描画が早すぎてキモい（褒め言葉）
- gnomeと違って綺麗に背景をすけさせられる！

[https://ghostty.org/](https://ghostty.org/)

</div>
<div>
<img src="images/gohsty_crop.png">
</div>
</div>

---

## **Herdr** で並列管理

<div class="media wide">
<div>

- AIエージェントを複数走らせるとき<br>タブ移動不要
- 画面一覧で把握できて便利

</div>
<div>
<img src="images/herdr_crop.png">
</div>
</div>

---

<!-- _class: lead -->
![bg right:36% fit](images/lazy.png)

## 夢：<br>**思考の速度**でコーディング

### Neovim (LazyVim)

キーバインドがバチッと決まったときの快感は異常。

---

<!-- _class: lead -->
## 現実：<br>コマンドを思い出せずカーソルが止まる

今のタイピング速度：**「速度おじいちゃん」** 👵


---

<!-- _class: lead -->
## インターンは、お金ももらえるし<br>**東京で遊べる！**

---

<!-- _class: lead -->
## 💡 おわりに

「……というわけで駆け抜けてきましたが、」

---

<!-- _class: lead -->

### 最初のアジェンダ12個、
## 1個ずつバラせば何回かLTできましたね。

<span class="muted">（1回の発表でネタを全放出しすぎた）</span>

---

<!-- _class: lead -->
<!-- _paginate: false -->
## 皆さんもLinuxを入れて、<br>**Linux元年**を始めましょう！

### ご清聴ありがとうございました！ 🐧
