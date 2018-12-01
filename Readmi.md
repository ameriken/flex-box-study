# flex-boxについて書きます

#sample1

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

