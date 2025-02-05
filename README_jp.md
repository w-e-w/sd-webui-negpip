# NegPiP - Negative Prompt in Prompt
[English](README.md) | 日本語 | [中文](README_cn.md)

負の効果を持つプロンプトを使えるようになります  

# 概要
この拡張は、stable diffusion web-uiのプロンプトおよびクロスアテンションを拡張して、負の効果を持つプロンプトをプロンプト内で、正の効果を持つプロンプトをネガティブプロンプト内で使用できるようにします。通常、描きたくないものはネガティブプロンプトに書かれますが、ネガティブプロンプトの計算上、あまり効果が現れないことがあります。この拡張では、プロンプトと同程度の効果を持つ負のプロンプトを使用できるようにします。これにより、以前はネガティブプロンプトに置いて値を大きくしすぎて崩壊していたような単語でも、プロンプトに負の効果を持たせることができ、より強い効果が期待できます。

# 使い方
Activeにチェックを入れることで有効になります。プロンプト入力画面において (word:-1)のようにマイナスの値を入れることで負の効果を持つようになります。ネガティブプロンプトでも有効で、この場合は正の効果を持ちます。値は1より大きな値を入力しないと効果が現れない場合があります。

これはgothic dressというプロンプトで作りました。ネガティブプロンプトに`(black:1.8)`と入れているにもかかわらず黒いですね。gothicの黒を消しきれないです。  
![image1](https://github.com/hako-mikan/sd-webui-negpip/blob/imgs/sample.jpg)

これはNegPiPでプロンプトに`(black:-1.8)`を入れました。黒くなくなりましたね。
![image2](https://github.com/hako-mikan/sd-webui-negpip/blob/imgs/sample2.jpg)

ちなみに、NegPiPもネガティブプロンプトも使わないとこうなります。
![image3](https://github.com/hako-mikan/sd-webui-negpip/blob/imgs/sample3.jpg)

## マジカルダンディ
マジカルダンディはマジカルなダンディです。マジカルなダンディを呼び出すことはとても難しいです。それはmagical girlとdandyを共存させる必要があるからです。でもダンディは弱いです。girlは強いです。とても強いです。なのでダンディは負けてしまいます。ネガティブプロンプトに`(girl:1.8)`って入れても出てきません。
![](https://github.com/hako-mikan/sd-webui-negpip/blob/imgs/sample4.jpg)

なのでプロンプトの方に`(girl:-1.6)`と入れてgirlを消す必要があるんじゃんよ。
![](https://github.com/hako-mikan/sd-webui-negpip/blob/imgs/sample5.jpg)
