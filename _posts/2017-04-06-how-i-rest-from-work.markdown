---
layout: post
title: 在区块链上建网站
date: 2017-09-12 13:32:20 +0300
description: 90's yr crucifix, selvage 8-bit listicle forage cliche shoreditch hammock microdosing synth. 
img: o-five.jpg # Add image post (optional)
fig-caption: # Add figcaption (optional)
excerpt: I am happy to join with you today in what will go down in history as the greatest demonstration for freedom in the history of our nation.
tags: [Holidays, Hawaii]
---
Fam据Bitcoin消息，近日，BCH爱好者Donald Mulders在社交媒体网络Yours.org上发表文章，详细描述了他试图利用Bitdb 2.0应用程序在BCH链上建立一个网站。<!-- more -->
之后在BCH开发者Unwriter和一个名为“Cryptograffitiweb”的工具的帮助下，Mulders的链上网站“Bitcoin Cash Hoarder”现在可以在任何浏览器上看到。Mulders表示：“如果有人能在不需要像维基解密这样的组织的情况下发布敏感信息，那么任何人都可以匿名发布信息，而不会危及自己或任何中间人。”据悉，Bitdb 2.0是一个平台，可接受比特币交易并将其放入结构化的可读文档或者在Donald Mulders此次使用的HTML代码中。



（[中文来源：币世界](http://www.bishijie.com/kuaixun_118500)）（英文来源 [bitcoin news: Launching a Website on the Bitcoin Cash Network Is Now a Reality](https://news.bitcoin.com/)）

这篇文章翻译的就是Donald Mulders在yours上发的文章来源：[Hosting a website on the BCH blockchain with bitdb 2.0. I am close but no sigar.](https://www.yours.org/content/hosting-a-website-on-the-bch-blockchain-with-bitdb-20----------i-am-5b8346293439)由于口水话太多，没有逐一翻译。

------

I can do a little HTML and I can mess around a littble bit in existing code I take from others. I am just starting to learn and had only about 2 lessons so far. With a lot of trial and error, I can make a simple website, but that's about it. I still have a long long way to go in mastering the art of programming. But I am taking baby steps towards this goal. Inspired by the BitDB 2.0 from [Unwriter](https://www.yours.org/@unwriter) (<https://www.yours.org/content/introducing-bitdb-20-e8c17c845939>) I just started working on a idea, but needless to say for now I am way over my head. 

作者说自己会一点html，编程属于初学者，然后在bitdb2.0 的启发下，动手做了一个简单的网站。

Anyway I started playing around with an idea to see how far I could take it. The idea is to host a simple HTML website on the bitcoin cash blockchain that easily could be viewed in a browser. In such a way that even my own mother is able to view it as if it was just an ordinairy website. Is there a use case? Does this even need blockchain? Well imagine if someone could publish sensitive information without the need for organisation’s such as WikiLeaks, readable as a ordinairy website for anyone in the world. This way anyone could publish information anonymous without endangering themselfs or any middleman. People like Julian Assange are hard to find nowadays, and I do not expect that there are many people who dare to take on such a role in the future. Freedom of expression, freedom of information, free journalism and a secure way to publish information for whistleblowers. This is the use case.

作者打算在区块链上建一个简单的可以通过浏览器访问的html网站，这样即使是他妈妈也会以为这是一个普通的网站，这样有个好处，人们可以匿名发布一些敏感信息而不用通过维基泄密那样的组织。

[^1]: 这里的原理没有说明，为什么可以匿名，以及可以做到多大程度上的匿名。

，同时免于可能的危险。

To see how far I could take this idea I made a very simple website in HTML and I included a snake game in JavaScript just to see if it would work. Lean and mean. This is how the site would look like. 

作者在网页里用JavaScript写了一个贪吃蛇游戏。

![](E:\git_project\blockchain\assets\img\Bitcoin_Cash_Hoarder.jpg)

Yes it is just snake but I renamed it Bitcoin Cash Hoarder, because it sound way cooler, and made it green and orange. I used [https://www.cryptograffiti.info](https://www.mttr.app/) to upload the code to the blockchain. This is easy as pie.

作者用[https://www.cryptograffiti.info](https://www.mttr.app/)上传代码到区块链

 The best way to explain what happens is that just like with [https://memo.cash](https://simpleledger.cash/), you make a OpReturn transaction where text is inserted, but since my text does not fit into a single transaction, it creates many transactions a bit similar to [https://www.scale.cash](https://chrome.google.com/webstore/detail/memo%2B%2B/efbehadlmgmkdflmmfjnadbnfamloeie) (the stress test tool) and it inserts small pieces of text with each transaction until it is finished. 

就像使用[https://memo.cash](https://simpleledger.cash/)（memo是一个基于区块链的活动资金筹集工具）一样，你使用了一个opreturn 交易，在文本被插入的地方，但由于我的文本没有适合一个单笔交易，所以他创造了许多交易，这有点像[https://www.scale.cash](https://chrome.google.com/webstore/detail/memo%2B%2B/efbehadlmgmkdflmmfjnadbnfamloeie)（压力测试工具），在完成前它在每一笔交易中插入了文本的小片段。

Here you can see my transaction on a bitcoin cash explorer: <https://explorer.bitcoin.com/bch/tx/fa69fb53bb45cd9df375f93f6cca52d044e4505eda5ce1b9504ae2c6a999ae27> 

 

你可以在比特币浏览器上看到我的交易记录。

The HTML code is now stored on the blockchain. 

现在Html 代码已经被储存在区块链上。

Step 1 is easy, anyone could do this. But how can I extract this information from the blockchain and display it as a website. I hoped bitdb could help me with this problem. If you go to the bitdb explorer ([https://bitdb.network/explorer](http://www.memopay.xyz/)) anyone should be able to extract the HTML code form the blockchain. 

第一步，如果你使用bitdb浏览器([https://bitdb.network/explorer](http://www.memopay.xyz/))，就可以从区块链中提取html代码。

This is the promise. As instructed on the bitdb website I used some standard code available and included the correct bitcoin cash address. This is the code I used for the query:

照着bitdb网站上给的指导，我用了一些标准代码，其中包括正确的比特币地址。下面是我查询时用的代码

```
{ "v": 2, 

"q": 

{ "find": {

 "in.e.a": "qqfse6sldawf742ydclj2n2uwgy7pxnd4ctlnph68a" 

}, 

"limit": 10 

}

 }
```

 

When you paste this code in the bitdb explorer and run the query you are able to find my HTML code. Just look at “out” & “s2” and follow every box below. There it is. 

当你把代码粘贴到bitdb浏览器并运行查询，你就能够看到我的html代码。在out和s2里，如下

![](E:\git_project\blockchain\assets\img\HTML_code.jpg)

But this is not even near being a website. Whatever I tried, I was not able to make the HTML more readable, let alone, display it in a browser. Just to say it again, I am a noob and lacking such skills.

但这还不能叫做一个网站，不管我怎么试，我也不能是html更具可读性。因为我只是一个初学者。

 I did look into GitHub to see if the code of sites like memo and matter could help me out but I couldn’t make enough sense of it to replicate such a activity. 

我在GitHub上找了找看看有没有和我网站的代码相似的，但没找到。

I should actually should start with lesson 3 and 4 of my HTML course because I am stuck. Step 2 is a lot harder for me.

我应该开始进一步学习一下html课程。第二步有点难对于我来说。

But not giving up yet and looking for a workaround. I went back to [cryptograffiti.info](https://t.me/joinchat/HH1DDQ8pZlSlsdNcKgIcxw) to see if I could extract my code from the blockchain here. 

但还没有放弃。我又回到[cryptograffiti.info](https://t.me/joinchat/HH1DDQ8pZlSlsdNcKgIcxw)去看我是否能从区块链上提取我的代码。

 

As you can see on this website it shows many text messages. Your text could become hard to find over time as new messages are posted. 

 

正如你在这个网站上看到的，它展示了很多的文本信息。随着新信息不断发布出现，你的文本会难以被找到。

 

I also looked on GitHub for the code of cryptograffiti and after reading some instruction, I figured out a simple hack. 

## Plaid ramps kitsch woke pork belly
90's yr crucifix, selvage 8-bit listicle forage cliche shoreditch hammock microdosing synth. Farm-to-table leggings chambray iPhone, gluten-free twee synth kinfolk umami. Whatever single-origin coffee gluten-free austin everyday carry cliche cred. Plaid ramps kitsch woke pork belly organic. Trust fund whatever coloring book kombucha brooklyn. Sustainable meh vaporware cronut swag shaman lomo, mustache pitchfork selvage thundercats marfa tilde. Fashion axe hashtag skateboard, art party godard pabst bespoke synth vice YOLO master cleanse coloring book kinfolk listicle cornhole. Try-hard mixtape umami fanny pack man bun gastropub franzen tbh. Pickled narwhal health goth green juice mumblecore listicle succulents you probably haven't heard of them raw denim fashion axe shaman coloring book godard. Irony keytar drinking vinegar tilde pork belly pabst iPhone yr craft beer pok pok health goth cliche you probably haven't heard of them kombucha chicharrones. Direct trade hella roof party chia. Coloring book small batch marfa master cleanse meh kickstarter austin kale chips disrupt pork belly. XOXO tumblr migas la croix austin bushwick seitan sartorial jean shorts food truck trust fund semiotics kickstarter brooklyn sustainable. Umami knausgaard mixtape marfa. Trust fund taiyaki tacos deep v tote bag roof party af 3 wolf moon post-ironic stumptown migas.

![I and My friends]({{site.baseurl}}/assets/img/we-in-rest.jpg)

Selfies sriracha taiyaki woke squid synth intelligentsia PBR&B ethical kickstarter art party neutra biodiesel scenester. Health goth kogi VHS fashion axe glossier disrupt, vegan quinoa. Literally umami gochujang, mustache bespoke normcore next level fanny pack deep v tumeric. Shaman vegan affogato chambray. Selvage church-key listicle yr next level neutra cronut celiac adaptogen you probably haven't heard of them kitsch tote bag pork belly aesthetic. Succulents wolf stumptown art party poutine. Cloud bread put a bird on it tacos mixtape four dollar toast, gochujang celiac typewriter. Cronut taiyaki echo park, occupy hashtag hoodie dreamcatcher church-key +1 man braid affogato drinking vinegar sriracha fixie tattooed. Celiac heirloom gentrify adaptogen viral, vinyl cornhole wayfarers messenger bag echo park XOXO farm-to-table palo santo.

>Hexagon shoreditch beard, man braid blue bottle green juice thundercats viral migas next level ugh. Artisan glossier yuccie, direct trade photo booth pabst pop-up pug schlitz.

Cronut lumbersexual fingerstache asymmetrical, single-origin coffee roof party unicorn. Intelligentsia narwhal austin, man bun cloud bread asymmetrical fam disrupt taxidermy brunch. Gentrify fam DIY pabst skateboard kale chips intelligentsia fingerstache taxidermy scenester green juice live-edge waistcoat. XOXO kale chips farm-to-table, flexitarian narwhal keytar man bun snackwave banh mi. Semiotics pickled taiyaki cliche cold-pressed. Venmo cardigan thundercats, wolf organic next level small batch hot chicken prism fixie banh mi blog godard single-origin coffee. Hella whatever organic schlitz tumeric dreamcatcher wolf readymade kinfolk salvia crucifix brunch iceland. Literally meditation four loko trust fund. Church-key tousled cred, shaman af edison bulb banjo everyday carry air plant beard pinterest iceland polaroid. Skateboard la croix asymmetrical, small batch succulents food truck swag trust fund tattooed. Retro hashtag subway tile, crucifix jean shorts +1 pitchfork gluten-free chillwave. Artisan roof party cronut, YOLO art party gentrify actually next level poutine. Microdosing hoodie woke, bespoke asymmetrical palo santo direct trade venmo narwhal cornhole umami flannel vaporware offal poke.

* Hexagon shoreditch beard
* Intelligentsia narwhal austin
* Literally meditation four
* Microdosing hoodie woke

Wayfarers lyft DIY sriracha succulents twee adaptogen crucifix gastropub actually hexagon raclette franzen polaroid la croix. Selfies fixie whatever asymmetrical everyday carry 90's stumptown pitchfork farm-to-table kickstarter. Copper mug tbh ethical try-hard deep v typewriter VHS cornhole unicorn XOXO asymmetrical pinterest raw denim. Skateboard small batch man bun polaroid neutra. Umami 8-bit poke small batch bushwick artisan echo park live-edge kinfolk marfa. Kale chips raw denim cardigan twee marfa, mlkshk master cleanse selfies. Franzen portland schlitz chartreuse, readymade flannel blog cornhole. Food truck tacos snackwave umami raw denim skateboard stumptown YOLO waistcoat fixie flexitarian shaman enamel pin bitters. Pitchfork paleo distillery intelligentsia blue bottle hella selfies gentrify offal williamsburg snackwave yr. Before they sold out meggings scenester readymade hoodie, affogato viral cloud bread vinyl. Thundercats man bun sriracha, neutra swag knausgaard jean shorts. Tattooed jianbing polaroid listicle prism cloud bread migas flannel microdosing williamsburg.

Echo park try-hard irony tbh vegan pok pok. Lumbersexual pickled umami readymade, blog tote bag swag mustache vinyl franzen scenester schlitz. Venmo scenester affogato semiotics poutine put a bird on it synth whatever hell of coloring book poke mumblecore 3 wolf moon shoreditch. Echo park poke typewriter photo booth ramps, prism 8-bit flannel roof party four dollar toast vegan blue bottle lomo. Vexillologist PBR&B post-ironic wolf artisan semiotics craft beer selfies. Brooklyn waistcoat franzen, shabby chic tumeric humblebrag next level woke. Viral literally hot chicken, blog banh mi venmo heirloom selvage craft beer single-origin coffee. Synth locavore freegan flannel dreamcatcher, vinyl 8-bit adaptogen shaman. Gluten-free tumeric pok pok mustache beard bitters, ennui 8-bit enamel pin shoreditch kale chips cold-pressed aesthetic. Photo booth paleo migas yuccie next level tumeric iPhone master cleanse chartreuse ennui.
