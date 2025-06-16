---
title: 網頁效用效果筆記（持續更
date: 2024-07-28 00:00:00
categories: 
    - 技經肯綮
---
### 刪除綫
|                |     Display     | 
| :---           |     :----:      | 
|Source code     |``` ~~akane~~ ```|
|Rendering effect|    ~~akane~~    |

參考資料： <https://markdown.com.cn>
### 萌娘百科黑幕實現
在\source\css\main.css中加入以下内容:
<!-- more -->
```
.heimu,
.heimu rt{
    background-color:#252525;
}
 
.heimu,
.heimu a,
a .heimu,
a.new .heimu,
span.heimu a.new,
span.heimu a.external,
span.heimu a.external:visited,
span.heimu a.extiw,
span.heimu a.extiw:visited,
span.heimu a.mw-disambig,
span.heimu a.mw-redirect{
    transition:color 0.13s linear;
    color:#252525;
    text-shadow:none;
}
 
span.heimu:hover,
span.heimu:active{
    color:white;
}
 
span.heimu:hover a,
a:hover span.heimu{
    color:lightblue;
}
 
span.heimu:hover a:visited,
a:visited:hover span.heimu{
    color:#C5CAE9;
}
 
span.heimu:hover a.new,
a.new:hover span.heimu{
    color:#FCC;
}
 
span.heimu a.new:hover:visited,
a.new:hover:visited span.heimu{
    color:#EF9A9A;
}
 
span.heimu:hover a.extiw:visited,
a.extiw:visited:hover span.heimu{
    color:#D1C4E9;
}

阅读更多：https://zh.moegirl.org.cn/MediaWiki:Gadget-site-styles.css
本文引自萌娘百科(https://zh.moegirl.org.cn )，文字内容默认使用《知识共享 署名-非商业性使用-相同方式共享 3.0 中国大陆》协议。
```
就可以在文章中使用
e.g.：<span class='heimu' title=你知道的太多了>其實我是男娘</span>
```
<span class='heimu' title=你知道的太多了>其實我是男娘</span>
```

參考資料： <https://zh.moegirl.org.cn/MediaWiki:Gadget-site-styles.css> 326-376行