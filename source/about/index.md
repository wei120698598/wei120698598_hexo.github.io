---
layout: "about"
title: "About"
date: 2016-04-21 04:48:33
description: "Wish for the Best, Prepare for the Worst"
header-img: "img/header_img/Iron-Man-3.jpg"
comments: true
---

<!-- Language Selector -->
<select class="sel-lang" onchange="onLanChange(this.options[this.options.selectedIndex].value)">
    <option value="0" selected> 中文 Chinese</option>
    <option value="1"> 英文 English</option>
</select>

<!-- Chinese Version -->
<div class="zh post-container">

    <!--copied from markdown -->
    <blockquote><p>心中志比天高</p></blockquote>

    <p>Hey，我是<strong>魏树鑫(shuxin.wei)</strong>，目前在北京从事Android应用开发</p>

    <p>主要在Android应用层架构方面进行研究开发，对应用层普遍使用的技术有一定的了解，并不断地深入</p>

    <p>工作之余，喜欢将工作中遇到的问题和研究的成果通过博客记录下来，并分享给更多开发者</p>

    <p>同时也创建了个人的公众号，并不定时的推送行业、技术等相关精华文章，扫描下方二维码即可关注</p>
    <img src="/img/sub/qrcode_344.jpg" width="200" height="200">

    <h5>Talks</h5>

    <ul>
        <li><a href="https://github.com">GitHub</a></li>
        <li><a href="http://jekyll.com.cn/">jekyll</a></li>
        <li><a href="https://pages.github.com/">GitHub Pages</a></li>
    </ul>
</div>

<!-- English Version -->
<div class="en post-container">
    <!--copied from markdown -->
    <blockquote><p>心中志比天高</p></blockquote>

    <p>Hey，我是<strong>魏树鑫(shuxin.wei)</strong>，目前在北京从事Android应用开发</p>

    <p>主要在Android应用层架构方面进行研究开发，对应用层普遍使用的技术有一定的了解，并不断地深入</p>

    <p>工作之余，喜欢将工作中遇到的问题和研究的成果通过博客记录下来，并分享给更多开发者</p>

    <p>同时也创建了个人的公众号，并不定时的推送行业、技术等相关精华文章，扫描下方二维码即可关注</p>
    <img src="/img/sub/qrcode_344.jpg" width="200" height="200">


    <h5>Talks</h5>

    <ul>
        <li><a href="https://github.com">GitHub</a></li>
        <li><a href="http://jekyll.com.cn/">jekyll</a></li>
        <li><a href="https://pages.github.com/">GitHub Pages</a></li>
    </ul>
</div>

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