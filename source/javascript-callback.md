---
title: JavaScriptコールバック関数
date: 2020-07-12
tags: ["JavaScript", "コールバック関数"]
excerpt: JSのコールバック関数の復習
---
![free-to-use-sounds-kgn8H0jMSIk-unsplash](https://user-images.githubusercontent.com/62282502/87250271-b17f2c80-c49e-11ea-9c09-ff35c5046d8a.jpg)

## はやく梅雨あけてくれー！
ここのところ、梅雨で毎日雨ばかりで気持ちが落ち込みやすい時期ですね＾＾；

「このままではアカン！！」と思い、筋トレを一昨日から再開。

といっても、Youtubeののがちゃんねるの腹筋2分＋ワークアウト4分だけですが…！

これ。

[【4分だけ】マンションでも！有酸素より効率よく脂肪を落とそう(HIIT)](https://youtu.be/SMw4XrBzTB8)
[【毎日2分】30日で腹筋を割るトレーニング](https://youtu.be/fuMOxAZOlLI)

**これだけでもけっこう汗かきます。**

朝起きて、水飲んで、ベッドのシーツを整えて、これをやります。
筋トレやると気持ち的にも前向きになるんですよね。

この朝の筋トレは、3ヶ月継続→プログラミングスクールに入ってパタッと止めてしまってたんですが。
三日坊主にならないように、また習慣化を意識してやっていこうと思います。


全然関係ない内容になってしまいましたが、
今日は、JavaScriptとUdemyで基本情報技術者試験の進数について学習しました。


## JavaScript(コールバック関数)
今日は手始めに、ProgateでJavaScriptのコールバック関数について復習。

ちょっと概念がわかりにくいところです。

```javascript
// (読み込み2) callback()によって、次に引数に渡した関数が呼び出されて実行される
const printName = () => {
  console.log("私の名前は、Mayumiです。");
 };
 
 // (読み込み1) 関数callがまず先に実行される
 const call = (callback) => {
  console.log("コールバック関数を呼び出します。");
  callback();
 };
 
 call(printName);
```

**引数に関数が入ります。**

上記は少し遠回りな書き方。
コールバック関数を引数の中で定義もできる。

```javascript
const printName = () => {
  console.log("私の名前は、Mayumiです。");
};

const call = (callback) => {
  console.log("コールバック関数を呼び出します。");
  callback();
};

call(printName);

// 引数の中で定義する
call(() => {
  console.log("私の名前は、Yasuyukiです。");
});
```

コールバック関数に引数を渡すことができます。
以下のように、引数は2つなど複数も可能です。


> [!WARNING]
> 呼び出し元とコールバック関数の引数の数は、同じでなければいけない。


```javascript
const call = (callback) => {
  callback("こてつ", 5);
};

call((name, age) => {
  console.log(`${name}は${age}歳です。`);
});
```



## 2進数＋基礎数学

基本情報技術者試験の学習で冒頭に出てくるやつです。

動画だと、やっぱり断然わかりやすいですね。

２進数と10進数の変換方法や、足し算・引き算などの計算方法は、慣れてしまえば結構簡単かなと思いました。

これは演習あるのみですね。
明日はここを復習して、**基礎数学＆論理回路**のところをひととおりやろうかと思います。