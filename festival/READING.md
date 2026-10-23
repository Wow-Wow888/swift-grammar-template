# 読解ノート：自分のアプリのコード3箇所

> **氏名：** team footprint (アンドレオッティ　アントワン, 宮本彩月, やだなーウー)
> **AI利用レベル：** 1（質問のみ。説明は自分の言葉で書く）
> **最終更新：** 2026-10-19

生成AIに書いてもらったコードでも、自分で書いたコードでもかまいません。自分のアプリの中から3箇所を選んで、次の3つの問いに答えてください。分からないところは、生成AIに「この行は何をしていますか」「この行を消すとどうなりますか」と聞いてかまいません。ただし、書くのは自分の言葉です。

> 💡 担任の先生の指示で、項目が増えることがあります。

---

## 箇所1：（例：品名を追加するボタンの処理）

```swift
func checkAnswer(_ input: String) -> Bool {
    guard let question = currentQuestion, isPlaying else { return false }
    
    let validAnswers = question.allAnswers
    let formattedInput = input.trimmingCharacters(in: .whitespacesAndNewlines).lowercased()
    
    let isCorrect = validAnswers.contains { answer in
        answer.trimmingCharacters(in: .whitespacesAndNewlines).lowercased() == formattedInput
    }
    
    if isCorrect {
        isCorrectAnswer = true
        correctCount += 1
        return true
    }
    return false
}
```

何をしているか：
入力された文字が正解かどうかを確かめる関数です。スペースや大文字を整えてから正解リストと比べ、合っていれば true、違っていれば false を返します。

なぜこう書くのか：
そのまま比べるのではなく、trimmingCharacters と lowercased() を使っているのは、「Japan」と「japan」の違いや、間違えて入れたスペースで不正解にならないようにするためです。

もしこう書かなかったら：
整える処理を消して、語尾にスペースを入れた「japan 」と入力して試しました。正解なのに不正解になってしまったので、元に戻しました。
---

## 箇所2：（見出し）

```swift
// コードを貼る
```

**何をしているか：**

**なぜこう書くのか：**

**もしこう書かなかったら：**

---

## 箇所3：（見出し）

```swift
// コードを貼る
```

**何をしているか：**

**なぜこう書くのか：**

**もしこう書かなかったら：**

---

## 自分ではまだ説明できない箇所（正直に）

（アプリの中で「動いているけれど何をしているか分からない」ところを書く。ここに書いたものは、後期の文法の授業で分かるようになります。）
