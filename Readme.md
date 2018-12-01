# flex-boxについて書きます

# sample1

## sample1単純に幅を指定してみました。
![WS000704.JPG](.\img\WS000704.JPG)


# sample5

##５つの箱にsampleと同様に箱を指定しました。


![WS000707.JPG](.\img\WS000707.JPG)

## これを一列に並べたい場合、最近だとflex-boxを使います。

```
display: flex;
```
![WS000708.JPG](.\img\WS000708.JPG)


## この例だと問題があります。一列に並べたいために`flex`が自動で幅を調整してくれています。

![WS000710.JPG](.\img\WS000710.JPG)
↑自動で184pxになってる

## コノヤロウ！って人のために`flex-wrap:wrap`とすると自動で調整されなくなります。
```
display: flex;
flex-wrap:wrap
```

![WS000711.JPG](.\img\WS000711.JPG)


※ちなみに、ここのflexの中のそれぞれの、中身はフレックスアイテムっていいます。(sample5とか,sample6とかのことですね。)これらをくるんでるもの全体はフレックスコンテナっていいます。これはdockerやってる人ならなんとなくイメージつくはずです！

# sample7
## 一番左からスタートしてるけど、それは嫌で右からスタートしたい人のために`justify-content:flex-end`ってのがあります。

![WS000713.JPG](.\img\WS000713.JPG)

## 真ん中にもしたいって人はいるよねってことで`justify-content:flex-center`

![WS000714.JPG](.\img\WS000714.JPG)

※ほかにも3個ほど、別の値があるので調べてみてください


# sample9
## liタグの一番最初だけ高さをあげてみました。

![WS000715.JPG](.\img\WS000715.JPG)
## 上揃えが嫌な人！！`align-items: flex-end;`こうなります。
![WS000716.JPG](.\img\WS000716.JPG)

※割愛しますが、これも色々できます、真ん中寄席にしたり。。。


# sample11
## ボックスの順番指定するには`order`を使います。


![WS000718.JPG](.\img\WS000718.JPG)

![WS000719.JPG](.\img\WS000719.JPG)
```
#sample11 li:first-of-type {
	order:11
}

#sample11 li:nth-child(2) {
	order:10
}
#sample11 li:nth-child(3) {
	order:9
}
#sample11 li:nth-child(4) {
	order:8
}
#sample11 li:nth-child(5) {
	order:7
}
#sample11 li:nth-child(6) {
	order:6
}
#sample11 li:nth-child(7) {
aporder:5
}
#sample11 li:nth-child(8) {
	order:4
}
#sample11 li:nth-child(9) {
	order:3
}
#sample11 li:nth-child(10) {
	order:2
}
#sample11 li:last-of-type {
    order:1
}
```

こんな感じでやってみました。

※注意点として、`order`プロパティで値を指定しない場合は値が0となってしまうので、指定をする際はすべて上記のように指定してあげる必要があります。


# sample13
## 今まではwidthで指定してたけど、flex-boxの中では`flex-basis`で幅が指定できます。


![WS000720.JPG](.\img\WS000720.JPG)

![WS000721.JPG](.\img\WS000721.JPG)

※かなり柔軟設計になります。

# sample15
## 余白を空けたくない！！！あなた。`flex-glow`をつかいます。

![WS000722.JPG](.\img\WS000722.JPG)


![WS000723.JPG](.\img\WS000723.JPG)
## ２番目のフレックスアイテムだけ広くしたい場合は、`flex-grow:5`などして調整ができます。(これ結構便利です)

![WS000725.JPG](.\img\WS000725.JPG)

今回の例だとこんな感じ
```
#sample15 li:nth-child(2) {
	flex-basis:100px;
	flex-grow: 5;
}
```

# sample17
## フレックスアイテムが大きくて、小さくしたい場合(flex-growの逆)、`flex-shrink`を使います。

![WS000726.JPG](.\img\WS000726.JPG)

※わかりづらいですが、`display-flex`の地点で勝手に1行で収まるように調整してくれてるので、みてくれは変わりません。(写真も割愛)

## liの2番目だけ狭めたいとすると、flex-grow同様にできます！


![WS000727.JPG](.\img\WS000727.JPG)

