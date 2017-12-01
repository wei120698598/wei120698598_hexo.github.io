---
layout: "about"
title: "About"
date: 2016-04-21 04:48:33
description: "天再高又怎样，踮起脚尖就更接近阳光。"
header-img: "img/header_img/about_bg.jpg"
comments: true
---
<!-- Language Selector -->
<select class="sel-lang" onchange="onLanChange(this.options[this.options.selectedIndex].value)">
    <option value="0" selected> 中文 Chinese</option>
    <option value="1"> 英文 English</option>
</select>

<!-- Chinese Version -->

> 心中志比天高

<div class="zh post-container">
Hey，我是<strong>魏树鑫(shuxin.wei)</strong>，目前在北京从事Android应用开发
主要在Android应用层架构方面进行研究开发，对应用层普遍使用的技术有一定的了解，并不断地深入
工作之余，喜欢将工作中遇到的问题和研究的成果通过博客记录下来，并分享给更多开发者
同时也创建了个人的公众号，并不定时的推送行业、技术等相关精华文章，扫描下方二维码即可关注
</div>

<div class="en post-container">
Hey，我是<strong>魏树鑫(shuxin.wei)</strong>，目前在北京从事Android应用开发
主要在Android应用层架构方面进行研究开发，对应用层普遍使用的技术有一定的了解，并不断地深入
工作之余，喜欢将工作中遇到的问题和研究的成果通过博客记录下来，并分享给更多开发者
同时也创建了个人的公众号，并不定时的推送行业、技术等相关精华文章，扫描下方二维码即可关注
</div>

<img src="/img/sub/qrcode_344.jpg" width="200" height="200">

# Talks #

-  [Github](https://github.com)
-  [Jekyll](http://jekyll.com.cn/)
-  [GithubPages](https://pages.github.com)

<!-- Handle Language Change -->
<script type="text/javascript">
    // get nodes
    var $zh = document.querySelector(".zh");
    var $en = document.querySelector(".en");
    var $select = document.querySelector("select");

    // bind hashchange event
    window.addEventListener('hashchange', _render);

    // handle render
    function _render() {
        var _hash = window.location.hash;
        // en
        if (_hash == "#en") {
            $select.selectedIndex = 1;
            $en.style.display = "block";
            $zh.style.display = "none";
            // zh by default
        } else {
            // not trigger onChange, otherwise cause a loop call.
            $select.selectedIndex = 0;
            $zh.style.display = "block";
            $en.style.display = "none";
        }
    }

    // handle select change
    function onLanChange(index) {
        if (index == 0) {
            window.location.hash = "#zh"
        } else {
            window.location.hash = "#en"
        }
    }

    // init
    _render();
</script>