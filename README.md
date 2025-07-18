<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE html>
<html b:css='false' b:defaultwidgetversion='2' b:layoutsVersion='3' b:responsive='true' b:templateVersion='1.0.0' expr:class='data:blog.languageDirection' expr:dir='data:blog.languageDirection' xmlns='http://www.w3.org/1999/xhtml' xmlns:b='http://www.google.com/2005/gml/b' xmlns:data='http://www.google.com/2005/gml/data' xmlns:expr='http://www.google.com/2005/gml/expr'>
 
<head>

    <b:include data='blog' name='all-head-content'/>

<b:if cond='data:blog.pageType == &quot;index&quot;'>
<title><data:blog.pageTitle/></title>
<b:else/>
<b:if cond='data:blog.pageType != &quot;error_page&quot;'>
<title><data:blog.pageName/> - <data:blog.title/></title>
</b:if></b:if>
<b:if cond='data:blog.pageType == &quot;error_page&quot;'>
<title>Page Not Found - <data:blog.title/></title>
<meta content='20;/' http-equiv='refresh'/>
</b:if>

<!-- [ Social Media meta tag ] -->
<b:if cond='data:blog.url == data:blog.homepageUrl'> 
<b:if cond='data:blog.pageType == &quot;item&quot;'> 
<b:if cond='data:blog.pageType == &quot;static_page&quot;'>  
<b:if cond='data:blog.url'>
<meta expr:content='data:blog.url' property='og:url'/>
</b:if>
<meta expr:content='data:blog.title' property='og:site_name'/>
<b:if cond='data:blog.pageName'>
<meta expr:content='data:blog.pageName' property='og:title'/>
</b:if></b:if></b:if></b:if>
 
<b:if cond='data:blog.pageType == &quot;item&quot;'>
<meta content='article' property='og:type'/>
<b:else/>
<meta content='website' property='og:type'/>
</b:if>

<meta expr:content='data:blog.title' property='og:site_name'/>
<meta content='en_US' property='og:locale'/>
 
<!-- Customize meta tags here -->

<b:if cond='data:blog.url == data:blog.homepageUrl'>
<meta content='YOUR-KEYWORD-HERE' name='keywords'/>
<meta content='AUTHOR-NAME-HERE' name='Author'/>
<link href='AUTHOR-URL-HERE' rel='author'/>
</b:if>

<meta content='GOOGLE-META-TAG' name='google-site-verification'/>
<meta content='BING-META-TAG' name='msvalidate.01'/>
<meta content='ALEXA-META-TAG' name='alexaVerifyID'/>

<meta content='IE=9; IE=8; IE=7; IE=EDGE; chrome=1' http-equiv='X-UA-Compatible'/>
<meta content='true' name='HandheldFriendly'/>

<meta content='width=device-width, initial-scale=1, minimum-scale=1, maximum-scale=1' name='viewport'/>

<link href='https://fonts.googleapis.com/css?family=Open+Sans:400,600,700&amp;display=swap' rel='stylesheet'/>

<script src='http://ajax.googleapis.com/ajax/libs/jquery/1.8.2/jquery.min.js' type='text/javascript'/>

<link href='https://stackpath.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css' rel='stylesheet'/>

<include expiration='7d' path='*.css'/>
<include expiration='7d' path='*.js'/>
<include expiration='3d' path='*.gif'/>
<include expiration='3d' path='*.jpeg'/>
<include expiration='3d' path='*.jpg'/>
<include expiration='3d' path='*.png'/>

<link href='//ajax.googleapis.com' rel='dns-prefetch'/>
<link href='//stackpath.bootstrapcdn.com' rel='dns-prefetch'/>
<link href='//fonts.googleapis.com' rel='dns-prefetch'/>
<link href='//1.bp.blogspot.com' rel='dns-prefetch'/>
<link href='//2.bp.blogspot.com' rel='dns-prefetch'/>
<link href='//3.bp.blogspot.com' rel='dns-prefetch'/>
<link href='//4.bp.blogspot.com' rel='dns-prefetch'/>
<link href='//w3.org' rel='dns-prefetch'/>

    <b:skin version='1.3.0'><![CDATA[/*
---*****************************

Platform: Blogger
Name:     SOUQ Store Blogger Template
Designer: Naveed Iqbal
URL:      http://www.bloggertheme9.com
License: Free Version 

---*****************************/

/*
<!-- Variable definitions -->
<Variable name="keycolor" description="Main Color" type="color" default="$(main.color)" value="#7D4998"/>
<Variable name="followByEmail" description="Follow By Email Text" type="string" default="Get all latest content delivered straight to your inbox." value="Get all latest content delivered straight to your inbox."/>

<Group description="Theme Colors" selector="body">
 <Variable name="main.color" description="Theme Color" type="color" default="#f12020" value="#7d4998"/>
  <Variable name="dark.color" description="Dark Color" type="color" default="#111111" value="#000000"/>
  <Variable name="menu.bg" description="Menu Background" type="color" default="$(main.color)" value="#7D4998"/>
  <Variable name="menu.color" description="Menu Color" type="color" default="#ffffff" value="#ffffff"/>
  <Variable name="title.color" description="Title Color" type="color" default="#111111" value="#000000"/>
  <Variable name="footer.color" description="Footer Color" type="color" default="#f1ffff" value="#f9ffed"/>
</Group>

<Group description="Theme Body" selector="body">
  <Variable name="body.background.color" description="Body Background Color" type="color" default="#f8f8f8"  value="#f6f6f6"/>
  <Variable name="body.background" description="Background" type="background" color="$(body.background.color)" default="$(color) url() repeat fixed top left" value="$(color) url() repeat fixed top left"/>
  <Variable name="body.text.color" description="Text Color" type="color" default="#656565"  value="#595959"/>
  <Variable name="body.link.color" description="Link Color" type="color" default="$(main.color)"  value="#7D4998"/>
</Group>
 
<!-- Extra Variables -->
<Variable name="body.text.font" description="Font" hideEditor="true" type="font" default="14px Open Sans, sans-serif"  value="14px Open Sans, sans-serif"/>
<Variable name="posts.background.color" description="Post background color" hideEditor="true" type="color" default="#ffffff"  value="#ffffff"/>
<Variable name="tabs.font" description="Font 2" hideEditor="true" type="font" default="14px Open Sans, sans-serif"  value="14px Open Sans, sans-serif"/>
<Variable name="posts.title.color" description="Post title color" hideEditor="true" type="color" default="#111111"  value="#000000"/>
<Variable name="posts.text.color" description="Post text color" hideEditor="true" type="color" default="#656565"  value="#595959"/>
<Variable name="posts.icons.color" description="Post icons color" hideEditor="true" type="color" default="$(main.color)"  value="#f12020"/>
<Variable name="labels.background.color" description="Label background color" hideEditor="true" type="color" default="$(main.color)"  value="#f12020"/>
*/

/* New interface B - ver 3
----------------------------------------------- */

html, body, div, span, applet, object, iframe, h1, h2, h3, h4, h5, h6, p, blockquote, pre, a, abbr, acronym, address, big, cite, code,
del, dfn, em, font, img, ins, kbd, q, s, samp, small, strike, strong, sub, sup, tt, var, dl, dt, dd, ol, ul, li, fieldset, form, label, legend, table, caption, tbody, tfoot, thead, tr, th, td, figure { margin: 0; padding: 0;}
article,aside,details,figcaption,figure,footer,header,hgroup,menu,nav,section {display:block;}
ins{text-decoration:underline}
del{text-decoration:line-through}

*, *:before, *:after, html {-moz-box-sizing: border-box; -webkit-box-sizing: border-box; box-sizing: border-box;}

table {margin:15px 0; font-family: arial, sans-serif; font-size:13px; border-collapse: collapse; width: 100%;}
td, th {border: 1px solid #eee; text-align: left; padding:8px 10px;}
tr:nth-child(odd) {background: #F4F4F4;}*{outline: none;}

caption {background: #eee; text-align:center; padding: 4px 10px 4px}
dl {margin: 0 0 20px 0}
dl dt {font-weight: bold}
dd {margin-left: 20px}
pre {margin: 20px 0; white-space: pre}
pre, code, tt {font: 13px 'andale mono', 'lucida console', monospace; line-height: 18px}

blockquote:before, blockquote:after,
q:before, q:after {content: "";}
blockquote, q {quotes: "" "";}
sup{ vertical-align: super; font-size:smaller; }
code{ font-family: 'Courier New', Courier, monospace; font-size:12px; color:#272727; }
a img{border: none;}
ul ul, ol ol { padding: 0; }

ol, ul { padding: 0px;  margin: 0; }
ol li { list-style-type: none;  padding:0;  }
ul li { list-style-type: none;  padding: 0;  }

/* Theme color change
----------------------------------------------- */
a,a:hover,.post-title a:hover, .sidebar-wrapper a:hover,#related-article h4 a:hover, .sidebar-wrapper a:hover, .cart-description .item-quantity, .cart-description .item-total, .fourthing i, .footer-credits a:hover, .PopularPosts .post-title a:hover{color:$(main.color);}
.no-posts-message,.share-buttons li .sharing-platform-button:focus, .share-buttons li .sharing-platform-button:hover,.post-filter-message,#blog-pager a, .showpagePoint, .search-submit-container button, .cart-description .item-decrement a:hover,.cart-description .item-increment a:hover, .cart-details, .cart-description .simpleCart_checkout, .menu-bg{background-color:$(main.color);}

h1, h2, h3, h4, h5, h6 {color: #555; font-family: 'Open Sans',sans-serif; font-weight:600;}

h2{ font-size: 17px; line-height: 23px;}
h3{ font-size: 17px; line-height: 23px;}
h4{ font-size: 16px; line-height: 22px; }
h5, h6{ font-size: 16px; line-height: 22px; }
.post-body h2, .post-body h3, .post-body h4, .post-body h5, .post-body h6{ margin:6px 0;}

a{ color: ; outline:none; text-decoration: none; }
a:hover { color: ; text-decoration:none; }
body {background-color: #fff; color:#666; font:14px/1.7em 'Open Sans',sans-serif; letter-spacing:.1px; overflow-wrap: break-word; word-break: break-word; word-wrap: break-word; margin:0; padding:0;} 

.ct-wrapper {padding:0px 0px 0; position:relative; margin: 0px auto;}
.outer-wrapper {margin:0; position: relative;}
.main-wrapper{background:#fff; float:left; overflow:hidden; width:calc(100% - 285px); word-wrap:break-word; padding:0 0px; margin:0 0 20px;}
.sidebar-wrapper{float:right; overflow:hidden; width:260px; word-wrap:break-word; padding:0 0px; margin:0;}
.contained {margin: 0 auto; padding: 0 20px; position: relative; clear:both; max-width:1190px;}

.ct-wrapper, .crossy, .post, .sidebar-wrapper{overflow:hidden;}

#header{margin:0px 0 0; float:left; min-width:260px;}
#header h1, #header h2 {font-size: 27px; margin: 0; padding: 0; font-weight:600; line-height:36px; text-overflow: ellipsis; white-space: nowrap;}
#header h1 a, #header h2 a{}
#header h1 a:hover, #header h2 a:hover{opacity:.8;}
.header-logo img{max-width:100%; max-height:47px; margin:0;}
.Header p {display:none; color: #fff; font-weight:300; font-size:14.7px; line-height:1.7; margin: 6px 0 0; padding: 0;}
.header-wrapper{padding:16px 0; float: left; width: 100%;}

.PopularPosts .popular-posts-snippet, .Header p{font-family:Merriweather,Georgia,serif; font-style:italic;}

.hidden {display: none;}
.invisible {visibility: hidden;}

.top{margin-top:30px;}

.color{background-image: -webkit-gradient(linear,right top,left top,from(#CD4033),to(#FFB100)); background-image: linear-gradient(to left,#CD4033,#FFB100);}

.clear { clear: both;}

.main-heading {position: absolute; clip: rect(1px,1px,1px,1px); padding: 0; border: 0; height: 1px; width: 1px; overflow: hidden;}
.blogger-logo, .svg-icon-24.blogger-logo {fill: #ff9800; opacity: 1;}

.item-control {display: none;}

.BLOG_mobile_video_class {display: none;}
.bg-photo {background-attachment: scroll !important;}

.tred{background:#F4F4F4; float:left; width:100%; padding:6px 0; font-size:13.4px;}

.socal, .slogy{float:left; }
.socal a{background:#ddd; display:block; float:left; width:34px; height:34px; line-height:34px; overflow:hidden; color: #fff !important; text-align:center; margin:0 4px 6px; font-size:15px; border-radius: 2px;}

.socal a.fb-ic{background:#3B5998; color:#fff;}
.socal a.tw-ic{background:#19BFE5; color:#fff;}
.socal a.ig-ic{background:linear-gradient(15deg,#ffb13d,#dd277b,#4d5ed4); color:#fff;}
.socal a.yt-ic{background:#ca2127; color:#fff;}
.socal a.rs-ic{background:#0077b5; color:#fff;}

.apploads{margin:14px 0 0; float:left; }
.apploads a {background-color: #5d5d5d; display: inline-block; border-radius: 4px; padding: 6px 10px; margin:0 4px 6px; font-size: 15px; color:#fff !important; font-family: 'Open Sans',sans-serif;}
.apploads a i{}
.apploads a:hover, .socal a:hover{opacity:.8; }

.cates {display: block; float:right; }
.cates li {display: inline-block; border-left:2px solid #e1e1e1; }
.cates li a {color: #666; padding:0 12px; }
.cates li a:hover {color:#333;}
.cates li:first-child {border:none;}
.cates i{font-size:19px; margin:0 3px 0 0px;}

a.menu-btn { display: none; color: #fff; background-color: #333; padding: 18px 15px 18px 55px; font-size: 15px; font-weight: 600;}
.menu-bg {background-color:; float: left; width: 100%;}
.menu { float: left; margin: 0 -10px; -webkit-transition: all 0.3s ease; -moz-transition: all 0.3s ease; -ms-transition: all 0.3s ease; transition: all 0.3s ease; }
.menu ul {padding: 0px; margin: 0px; list-style: none; position: relative; }
.menu > li > ul.sub-menu {min-width: 10em; padding: 4px 0;	background-color: #f4f4f4; border: 1px solid #CCC; }
.menu ul li {z-index: 10; position:relative;}
.menu > ul > li { display: inline-block; }
.menu ul li > a { display: block; color: #fff; font-size: 15px; padding:0px 20px; line-height:50px;}

.menub ul ul {display:none;position: absolute; top:100%; min-width: 0px; background-color: #fff; box-shadow: 0 5px 8px rgba(0, 0, 0, 0.25); z-index:9; visibility: hidden; opacity: 0; transform: translate(0,25px); transition: all 0.2s ease-out;}
.menug ul li:hover > ul {visibility: visible; opacity: 1; transform: translate(0,0);}

.menu ul li > ul{display:none;}
.menu ul li a:hover > ul {display:block;}
 
.megamenuid li div.megasubmenu{background:#F8F8F8; position:absolute; width:870px; left:0; top:100%; overflow:hidden; min-height:0px; visibility:hidden; opacity:0; color:#888; 
-moz-transform:translate(0,30px); -webkit-transform:translate(0,30px); -o-transform:translate(0,30px); transform:translate(0,30px);
transform-origin:50% 0; box-shadow:0 10px 7px -7px rgba(0,0,0,0.1); transition:all 0.3s ease-in-out; }
.megamenuid li:hover div.megasubmenu{visibility:visible; opacity:1; -moz-transform:translate(0,0); -webkit-transform:translate(0,0); -o-transform:translate(0,0); transform:translate(0,0); }

.leftmenulist{float:left; background: #f4f4f4; border-right: 1px solid #e4e4e4; min-height: 222px; width:168px; }
.leftmenulist li a {display: block; transition: all 0.3s ease-in-out;}

.rightmenulist{display: flex; flex-wrap: wrap; margin-left: -12px; margin-right: -12px;}
.rightmenulist li{-moz-box-flex: 0; float:left; width: calc(100% / 4); padding:14px 12px;}
.rightmenulist li a {font-weight: 600; font-size: 14px; }
.thumb-container{width:100%; overflow: hidden; display: block; height: 194px;}
.thumb-container img{width:100%; height:142px; border:1px solid #eee;}

.menu ul ul > li { position: relative; }
.menu ul ul ul { position: absolute; left: 100%; top:0; }
.menu ul ul > li a {color:#555; }
.menu ul ul > li a:hover {color: #222; }
.menu ul li a:hover{color: #fff;}

.with-ul:after {border-color: #ddd transparent transparent; border-image: none; border-style: solid; border-width: 4px; content: ""; position: absolute; top: 50%; right:5px;}

ul.megamenuid .loading-icon{background:url('http://2.bp.blogspot.com/-N9HNU11nhiA/Va-NLcGF0lI/AAAAAAAALW4/HzSlCK7PGeY/s1600/wait.gif') no-repeat scroll 0 0 transparent;width:22px;height:22px;position:absolute;top:50%;margin-top:-11px;right:5
px}
ul.megamenuid .menu-icon{border-bottom:4px solid transparent;border-top:4px solid transparent;border-left:4px solid #777;display:block;height:0;margin-top:-4px;position:absolute;right:11px;top:50%;width:0}

#megamenuid h5{font-size:16px;margin-top:70px;text-align:center}
#megamenuid h5:before{content:"";position:absolute;top:50px;left:50%;width:5px;height:2px;margin-left:-4px;border-left:2px solid black;border-right:2px solid black}
#megamenuid h5:after{content:"";position:absolute;top:55px;left:50%;width:10px;height:5px;margin-left:-7px;border-top:2px solid black;border-left:2px solid black;border-right:2px solid black;border-radius:8px 8px 0px 0px}

.hamburger {float: left; width: 20px; height: 20px; position: absolute; left: 45px; top: 28px;}
.hamburger > div {position: relative; width: 100%; height: 3px; background: #fff; align-items: center; justify-content: center; transition: all 0.4s ease;}
.hamburger > div::before,.hamburger > div::after {content: ''; position: absolute; z-index: 1; top: -8px; width: 100%; height: 3px; background: inherit;}
.hamburger > div::after {top: 8px;}

.base1{background-color: #354058; height:60px; float: left; width: 100%;}
.base2{background-color: #ddd; float: left; width: 100%;}
.white{background:#E9EFF9; float: left; width: 100%;}
.sidebar-wrapper .widget{overflow:hidden; clear: both; margin-bottom: 25px;}
.sidebar-wrapper li{border-bottom: 1px solid #ddd; margin: 0; padding: 7px 0 7px 7px; text-transform: capitalize;}
.sidebar-wrapper li:last-child, .footer li:last-child{border-bottom:none !important;}
.footer li:first-child, .PopularPosts ul li:first-child{padding-top:2px !important;}
.sidebar-wrapper h3{margin: 0 0 10px; padding: 0;}
.sidebar-wrapper a:hover{}

.post-body ol,.post-body ul { padding: 10px 0 20px;  margin: 0 0 0 25px;  text-align: left;  }
.post-body ol li { list-style-type: decimal;  padding:0 0 5px;  }
.post-body ul li { list-style-type: square;  padding: 0 0 5px;  }
.post-body img{max-width:100%; height:auto;}

.post-body iframe {max-width: 100%;}
.post-body a[imageanchor="1"] {display: inline-block;}
.post-body{margin:0 0 20px;}

.bow {display: flex; flex-wrap: wrap; margin-left: -12px; margin-right: -12px;}
.half, .brox, .banner2{-moz-box-flex: 0; width: calc(100% / 2); padding-left: 12px; padding-right: 12px;}
.third,.delate, .banner3 {-moz-box-flex: 0; width: calc(100% / 3); padding-left: 12px; padding-right: 12px;}
.quart, .fourthing {-moz-box-flex: 0; width: calc(100% / 4); padding-left: 12px; padding-right: 12px;}
.fifth, .related-posts li {-moz-box-flex: 0; width: calc(100% / 5); padding-left: 12px; padding-right: 12px;}
.producting li {-moz-box-flex: 0; width: calc(100% / 6); padding-left: 12px; padding-right: 12px;}
.post-header{margin:5px 0; font-weight:500; font-size:14px; color:#a1a1a1;}

.soothing, a, .product-buy-buttons a, .cart-buttons a{transition: all .5s ease-out; -webkit-transition: all .5s ease-out; -moz-transition: all .5s ease-out; -ms-transition: all .5s ease-out; -o-transition: all .5s ease-out;}

.byline {margin-right: 1em;}
.byline:last-child {margin-right: 0;}

.byline.reactions iframe {height: 20px;}

.no-posts-message {line-height: 40px; text-align: center; margin: 10px 0; background-color:; color:#fff;}

.crossy .widget-content{text-align:center; float:left; margin:20px 0 0; width:100%;}

.fn:before{font-family:fontawesome; content:"\f007"; font-style:normal; color:#777; float: left; margin: 0 6px 0 0;}
.publisheds:before{font-family:fontawesome; content:"\f133"; font-style:normal; color:#777; margin: 0 3px 0 0;}

.fb_iframe_widget {display: inline-block; position: absolute; margin: -6px 0 0 -25px;}

.feet-icons{margin: 0 0 0px;}
.feet-icons span{float:left; font-size:13px; }
.feet-icons a{float:left; width:28px; height:30px; line-height:25px; overflow:hidden; text-align:center; }
.feet-icons a i{font-size:15px; color:rgba(0,0,0,.6);}
.feet-icons a:hover{opacity:.8; }

a.face-ico i{color:#3B5998;}
a.twi-ico i{color:#19BFE5;}
a.pint-ico i{color:#ca2127;}
a.bitz-ico i{color:#23A215;}
a.link-ico i{color:#0077b5;}

.title-secondary{width: 99%; color: #888888; background: url(//2.bp.blogspot.com/-5feHh8DpM_k/U88bANmcxnI/AAAAAAAAB40/69FQdxpYqb0/s1600/title_pat.png) center left repeat-x;
padding-left: 2%; clear: both; height: 63px; font-size: 14px; line-height: 63px; font-weight:600; overflow: hidden; white-space: nowrap; text-overflow: ellipsis}
.post-author, .post-date{background: #fff; margin-right: 10px; padding: 7px; }

.title-secondary img {background:#fff; vertical-align: middle; padding:6px; float: left; width: 50px; height: 50px; margin: 4px 8px 0 0; border-radius: 50%;}

.producting{color:#fff;}
.producting li{float:left; position:relative; margin:0 0 10px;}
.producting h3{background: #fff; top: -9px; padding-right: 1.2%; margin: 0 0 25px; position: absolute; }
.producting .product_off {right:22px; }
.producting em{margin: 3px 0 14px; float: left; height: 12px; width: 100%; position: relative; font-style:unset;
background-image: -webkit-repeating-linear-gradient(135deg, #eaeaea, #eaeaea 1px, transparent 2px, transparent 2px, #eaeaea, #eaeaea 3px);
background-image: -moz-repeating-linear-gradient(135deg, #eaeaea, #eaeaea 1px, transparent 2px, transparent 2px, #eaeaea, #eaeaea 3px);
background-image: -o-repeating-linear-gradient(135deg, #eaeaea, #eaeaea 1px, transparent 2px, transparent 2px, #eaeaea, #eaeaea 3px);
background-image: repeating-linear-gradient(135deg, #eaeaea, #eaeaea 1px, transparent 2px, transparent 2px, #eaeaea, #eaeaea 3px);
-webkit-background-size: 4px 4px; -moz-background-size: 4px 4px; background-size: 4px 4px; }

.product-header{position:relative; width:100%; background-color:#f8f8f8; overflow:hidden; border:1px solid #eee; padding:15px; margin:0 0 20px; }
.col-left{position:relative; float:left; width:300px; }
.col-left .post-image-wrap{position:relative; margin:0; width:100%; height:auto; }
.col-right{position:relative; float:right; width:calc(100% - 315px)}
.col-left .post-thumb:hover{transform: scale(1); -ms-transform: scale(1); -webkit-transform: scale(1);}

.tier-price{margin:0 0 14px; color: $(main.color); font-size: 25px; font-weight:600; }

.reviews{margin:0 0 14px;}
.reviews i{color: #ddd; }
.reviews .checked {color: #FFD700;}

.product-buy-buttons{display:block; overflow:hidden; margin:0 0 20px}
.product-buy-buttons a{float:left; background-color:$(main.color); font-size:13.2px; color:#fff; font-weight:600; padding:6px 15px; margin:0px 12px 0 0; border-radius:2px; }
.product-buy-buttons a.cart-payment{background-color:#4d4d4d;}
.product-buy-buttons a i{margin:0 5px 0 0}
.product-buy-buttons a:hover{opacity:.9;}
.item_add .product_added,.item_add.productad .add_product{display:none}
.item_add.productad .product_added{display:block}

.product_off{position:absolute; top:10px; right:10px; height:24px; background-color:#F2616E; font-size:11px; color:#fff; font-weight:600; text-align:center; line-height:24px; z-index:2; padding:0 8px;  letter-spacing:.5px; }
.index-post .product_off,.FeaturedPost .product_off,.product-header .product_off{visibility:hidden;opacity:0;transition:all .17s ease}
.index-post .product_off.show,.FeaturedPost .product_off.show,.product-header .product_off.show{visibility:visible;opacity:1}

.post-thumb {display: block; position: relative; width: 100%; height: 100%; z-index: 1; transition: transform 1s; margin: 0 auto;}
.post-image-wrap{position:relative; margin: 0 0 8px; width: 100%; height: auto; overflow: hidden; border:1px solid #eee;}

.post-thumb:hover {transform: scale(1.2); -ms-transform: scale(1.2); -webkit-transform: scale(1.2);}

.dab{margin:20px 0 0px;}
.banner2, .banner3{margin:0 0 10px;}
.banner2 img, .banner3 img{width:100%; height:auto; border:1px solid rgba(0, 0, 0, 0.13);}
.banner2 .title, .banner2 .caption, .banner3 .title, .banner3 .caption{display:none; }

.gap{margin:0 0 15px; float:left; width:100%; }
.fourthing {margin:20px 0 0px; position:relative; }
.fourthing i{position:absolute; left:10px; top:2px; font-size:26px; width:55px; height:55px; line-height:55px; background:#eee; text-align:center; border-radius:50%; }
.ico-fourth {float:left; padding-left:67px;} 
.fourthing h5{margin:0 0 2px;}
.fourthing p{}

.my-comments {background: #FAFAFA; float:left; width:100%; margin: 0 0 25px; }
.my-comments h5 {margin: 0 0 4px; }
#comments .comment-form {}
#commentsHolder{border:1px solid #ddd; }
.comment-form iframe{margin:0 0 10px;}
body.item-view #comments .comment-form h4 {position: absolute; clip: rect(1px,1px,1px,1px); padding: 0; border: 0; height: 1px; width: 1px; overflow: hidden;}
#comment-holder .continue {display: none;}
#comments .comment-thread ol {margin: 0; padding-left: 0;}
#comments .comment-thread ol {padding-left: 0;}
#comments .comment-thread .comment-replies, #comments .comment .comment-replybox-single {margin-left: 60px;}
#comments .comment-thread .thread-count {display: none;}
#comments .comment {position: relative;}
.comments-content{float:left; width:100%; }
#comments .comment .comment {padding-bottom: 8px;}
.comment .avatar-image-container {position: absolute;}
.comment .avatar-image-container img {border-radius: 50%;}
.avatar-image-container svg, .comment .avatar-image-container .avatar-icon {border-radius: 50%; border: solid 1px #999; box-sizing: border-box; fill: #999; height: 35px; margin: 0; padding: 7px; width: 35px;}
.comment .comment-block {background: #fff; border: 1px solid #ddd; border-radius: 4px; margin: 0 0 25px 48px; padding: 12px 16px;}
.deleted-comment {background: #eee; border-radius: 3px; color: #999; font-size: 13px; padding: 10px;}
#comments .comment-author-header-wrapper {margin-left: 40px;}
#comments .comment .thread-expanded .comment-block {padding-bottom: 20px;}
.user a {color: #666; font-size: 15px; text-decoration: none;}
.comments .comments-content .user {font-style: normal;font-weight: bold;}
#comments .comment .comment-actions a{background: #fdfdfd; border: 1px solid #ccc; border-radius: 2px; color: #999; display: inline-block; font-size: 10.6px; height: 18px; line-height: 19px; margin: 0 6px 0 0; text-align: center; width: 36px;}
.comment-actions .item-control a {position: absolute; right: 5px; top: 10%;}
#comments .comment .comment-actions>* {margin-right: 8px;}
#comments .comment .comment-header .datetime {display: inline-block;}
#comments .comment .comment-header .datetime { margin-left: 8px;}
.datetime a {color: #666; font-size: 11px; font-weight: 400; opacity: 0.9; padding: 1px 6px; text-align: center; text-transform: none;}
#comments .comment .comment-header, #comments .comment .comment-footer .comment-timestamp a {color: rgba(0,0,0,0.54);}
.comments .comments-content .comment-content {color: #666; font-size: 14px; line-height: 1.6em; margin: 0; overflow-wrap: break-word; text-align: justify; padding: 12px 0; word-break: break-word; position: relative; transition: all 0.3s ease-out 0s;}
.comment-body {margin-bottom: 12px;}
#comments.embed[data-num-comments="0"] {}
#comments.embed[data-num-comments="0"] #comment-post-message, #comments.embed[data-num-comments="0"] div.comment-form>p, #comments.embed[data-num-comments="0"] p.comment-footer {display: none;}
#comment-editor-src {display: none;}
.comments .comments-content .loadmore.loaded {max-height: 0; opacity: 0; overflow: hidden;}

.svg-icon-24, .svg-icon-24-button {cursor: pointer; height: 24px; width: 24px; min-width: 24px;}

.snippet-container {margin: 0; position: relative; overflow: hidden;}
.snippet-fade {bottom: 0; box-sizing: border-box; position: absolute; width: 96px;}
.snippet-fade {right: 0;}
.snippet-fade:after {content: '\2026';}
.snippet-fade:after {float: right;}

.rating {border:none; float:left; margin: 0 0 10px;}
.rating > input { display: none; } 
.rating > label:before {margin: 0 5px 0 0; font-size: 1.13em; font-family: FontAwesome; display: inline-block; content: "\f005"; }
.rating > .half:before {content: "\f089"; position: absolute; }
.rating > label {color: #ddd; float: right; }
.rating > input:checked ~ label, .rating:not(:checked) > label:hover, .rating:not(:checked) > label:hover ~ label { color: #FFD700;  } 
.rating > input:checked + label:hover, .rating > input:checked ~ label:hover, .rating > label:hover ~ input:checked ~ label, .rating > input:checked ~ label:hover ~ label { color: #FFED85;  } 

.share-buttons .svg-icon-24, .centered-bottom .share-buttons .svg-icon-24 {fill: #fff;}
.sharing-open.touch-icon-button:focus .touch-icon, .sharing-open.touch-icon-button:active .touch-icon {background-color: transparent;}
.share-buttons {background: #444; color: #fff; border-radius: 2px; box-shadow: 0 2px 2px 0 rgba(0,0,0,.14) , 0 3px 1px -2px rgba(0,0,0,.2) , 0 1px 5px 0 rgba(0,0,0,.12); color: #fff; margin: 0; position: absolute; top: -11px; min-width: 160px; z-index: 101;}
.share-buttons.hidden {display: none;}
.sharing-button {background: transparent; border: none; margin:14px 0; outline: none; padding: 0; cursor: pointer;}
.share-buttons li {margin: 0; height: 38px;}
.share-buttons li:last-child {margin-bottom: 0;}
.share-buttons li .sharing-platform-button {box-sizing: border-box; cursor: pointer; display: block; height: 100%; margin-bottom: 0; padding: 0 14px; position: relative; width: 100%;}
.share-buttons li .sharing-platform-button:focus, .share-buttons li .sharing-platform-button:hover {background-color:; outline: none;}
.share-buttons li svg[class^="sharing-"], .share-buttons li svg[class*=" sharing-"] { position: absolute; top: 7px;}
.share-buttons li span.sharing-platform-button, .share-buttons li span.sharing-platform-button {position: relative; top: 0;}
.share-buttons li .platform-sharing-text {display: block; font-size: 16px; line-height: 38px; white-space: nowrap;}
.share-buttons li .platform-sharing-text {margin-left: 40px;}

blockquote {color: #424242; font: italic 300 x-large Ubuntu,sans-serif; margin: 7px 0; text-align: center;}

.post .thumb {float: left; height: 20%; width: 20%;}

.blog-pager {text-align: center;}

.post-title{font-size: 22px; line-height: 28px; font-weight:600; margin:0 0 14px; }
.sidebar-wrapper a, .post-title a:hover {color:#555;}
.sidebar-wrapper a:hover {}

.related-posts li{float:left; margin: 0 0 18px;}
.related-item h2{font-size:13.5px; line-height: 22px; font-weight:600; margin: 0 0 2px; }
.related-item .meta-price{font-weight:600; color:#444; font-size:13.5px; }

.post-snippet .snippet-fade {bottom: 0; position: absolute;}
.post-snippet{margin:12px 0 0;}

.post-filter-message {background-color:; width:100%; color: #fff; font-size:15.5px; letter-spacing:.9px; margin:0px 0 25px; padding: 12px 16px;}
.post-filter-message a {color: #fff; cursor: pointer; padding-left: 30px; white-space: nowrap;}
.post-filter-message .search-label, .post-filter-message .search-query {font-style: italic; quotes: "\201c" "\201d" "\2018" "\2019";}
.post-filter-message .search-label:before, .post-filter-message .search-query:before {content: open-quote;}
.post-filter-message .search-label:after, .post-filter-message .search-query:after {content: close-quote;}
.post-filter-message .show-more{float:right;}

.error-home{color: #111111; padding: 10px 0 20px;}
.error-home h3{font-size: 26px; line-height: 1; margin: 0 0 16px; padding:16px 0; border-bottom:1px solid #ccc;}
.error-home h4, .error-home p{font-size:17px; line-height: 1; font-weight:400; }
.error-home h4{margin:0 0 25px;}
.error-home p{margin:0 0 18px; }
.error-home a{border: 1px solid #999; background:#f1f1f1; opacity:.8; padding: 8px 12px; color:#666; font-size: 15px; font-weight:600; display:inline-block; border-radius:4px;}
.error-home a:hover{opacity:1;}

.post-labels{width:100%; margin:0 0 20px; float:left; }
.post-labels span, .post-labels a {height: 22px; font-size: 13px; line-height: 22px; font-weight: 400; margin: 0; }
.post-labels a {margin: 0 0 0px; color:#777; display:inline-block; transition: all .17s ease;}
.post-labels span, .feet-icons span{color:#444; }
.post-labels span{float:left; margin-right:4px;}

.post-labels a::after {content: ", "; }
.post-labels a:last-child::after {content: ""; }

body.feed-view .byline.post-labels a, body.feed-view .labels-more a {background-color: #ffffff; box-shadow: 0 0 2px 0 rgba(0, 0, 0, 0.18);  opacity: 0.9;}
.post .labels-container a {display: inline-block; max-width: calc(100% - 16px); overflow-x: hidden; text-overflow: ellipsis; vertical-align: top; white-space: nowrap;}
.post .labels-outer-container {margin: 0 -4px; position: absolute; top: 12px; transition: opacity 0.2s ease 0s; width: calc(100% - 2 * 16px);}

#blog-pager {float:left; width:100%; margin:0 0 20px;}
#blog-pager a {color: #fff; background: ; cursor: pointer; text-transform: uppercase;}

.PopularPosts .post{overflow:hidden;margin:20px 0 0}
.PopularPosts .post:first-child{padding:0;margin:0;border:0}
.PopularPosts .post-image-link{position:relative;width:80px; float:left;overflow:hidden;display:block;vertical-align:middle; border:1px solid #eee; margin:0 12px 0 0}

.PopularPosts .post-thumb {display: block; position: relative; width: 100%; height: 100%; object-fit: cover; z-index: 1;}
.PopularPosts .post-info{overflow:hidden}
.PopularPosts .post-title{font-size:15px; line-height:21px; font-weight:600; margin:0 0 5px; }
.PopularPosts .post-title a{display:block; transition:color .17s}
.PopularPosts .post-title a:hover{}
.PopularPosts .post-date{font-size:13px;}

.snipter{float:left; max-height: calc(21px * 6); overflow: hidden; }

.topper{display: flex;}
.topper li{list-style:none;}
.tableft{}
.tabmid{flex-grow: 1;}
.tabright{}

.search {float: left; margin: 0 20px;}
.search h3{display:none;}
.search-submit-container button {border: 0 none; font-family:'Open Sans',sans-serif; color: #fff; letter-spacing: .6px; cursor: pointer; font-size: 14px; margin: 1px 0 0 -72px; padding:12px 13px; position: absolute; overflow: hidden; border-radius:0px 5px 5px 0px;}
.search-input input {border:2px solid #e6e6e6; padding:5px 5px; height:45px; text-indent:3px; border-radius:5px; width:550px; float:left; font-size:15px;  }
.search-input input::placeholder {color:#7e7e7e; font-family:'Open Sans',sans-serif; }
.search-input{padding:0 10px; margin:0 0;}
.search-submit-container button:hover{opacity:.9;}

.menu-page {float:right; }
.menu-page li{float:left; }
.menu-page a:hover{opacity:.9;}
a.cart-details:hover{color:#fff;}

.showpageNum a, .showpage a, .showpagePoint {cursor: pointer; font-size: 13.4px; font-weight: 500; padding: 6px 12px; display: inline-block; border-radius:4px; transition:all .5s ease-out}
.showpageNum a:hover, .showpage a:hover, .showpagePoint {opacity:.8; color:#fff;  }
.showpageOf {display:none; margin-right:30px; margin-left:8px; }
.showpagePoint, .showpage a, .showpageNum a { margin: 0 3px 0; }

.breadcrumbs{color:#b8b8b8; margin:0 0 6px; overflow:hidden; white-space:nowrap; text-overflow:ellipsis;}
.breadcrumbs a{color:#b8b8b8; margin:0 0; line-height:normal; font-size:14px; }
.breadcrumbs .breadhome a{margin:0 5px 0 0}
.breadlabel a{}
.breadlabel:before { content: "/"; padding-right: 3px; color: #d2d2d2;}
.breadlabel:first-child:before { content: ""; padding-right: 0; }
.breadcrumbs a:hover{}

.post-wrapper {position: relative;}

body.feed-view .post-wrapper .snippet-thumbnail {display: block; background-position: center; background-size: cover; width: 100%;}

#related-article{display: block; margin: 2px 0 16px; float: left; width: 100%;}
#related-article ul {}
#related-article ul li{margin:0 0px 16px; }
#related-article h4 a{margin:8px 0 0; color:#606060; font-size:16px; line-height:22px; font-weight:400; display:block; transition:all .3s;}
#related-article h4 a:hover{color:;}
#related-article img{transition:all .3s ease-out; border: 1px solid #ddd; width: 99%; height:100%;}
.bimb {height: 135px; position: relative;}
#related-article h5 {font-size: 16px; text-transform: uppercase; line-height:26px; margin: 0 0 25px; padding-bottom: 15px; font-weight: 700; letter-spacing: 1px; text-align: center; position: relative;}
#related-article h5:after {content: ''; position: absolute; width: 4px; height: 4px; background: #aaa; border-radius: 50%; bottom: 0; left: 47%; box-shadow: 1em 0 0 0 #aaa,2em 0 0 0 #aaa;}

#related-article img:hover{opacity:0.7; }

.bukshan img{height:100%; width: 100%; }
.bukshan{width:315px; height:198px; margin:0 4% 12px 0; float:left; transition:all 0.3s ease-out 0s;}

#footer {padding:20px 0 0; overflow:hidden; z-index:200; position:relative;}
#footer h3 { margin:0 0 18px; font-size: 18px;}

.footer-wrapper{margin:0 -10px; border-top:1px solid #ddd; border-bottom:1px solid #ddd; padding: 18px 0px; overflow:hidden; }
.footer{width: calc(100% / 5); box-sizing: border-box; float:left; padding: 0 10px;} 
.footer .widget{ clear: both; margin: 0px 0px 20px; }
.footer li {border-bottom: 1px solid #ddd; list-style: none; margin: 0 !important; padding: 8px 8px !important; text-transform: capitalize;}
.footer a { color:#666; }
.footer a:hover, .footer-credits a, .med-lab a:hover{color:$(main.color);}

.footer-credits {margin:0 -10px; border-top:1px solid #ddd; z-index:200; position:relative; padding:18px 10px; text-transform:uppercase; font-size:12.4px;}
.img-payments{float:right; }
.logo-footer .widget-title{padding-left:50px; }
.logo-footer:before{font-family:'FontAwesome'; content:"\f07a"; font-size: 40px; position:absolute; color:$(main.color);}
.logo-footer h3{font-size:22px !important; }
.bukshan:hover, .PopularPosts .item-thumbnail img:hover, .brick li img:hover{opacity:.6;}

.footer-credits a{color:#3f3f3f; font-weight:600; }

.dlab{padding:20px 0 10px; float:left; width:100%; }
.med-lab{margin:0 0 14px; float:left; width:100%; }
.med-lab h3{font-size: 14px; display: inline-block; color:#444; margin-bottom: 0; padding-right: 5px; float:left; }
.med-lab .widget-content li{display: inline-block; padding: 0 10px; float:left; position:relative; }
.med-lab .widget-content li:after{position: absolute; top: 50%; transform: translateY(-50%); right: 0; height: 12px; width: 1px; content: ""; background-color: #666;}
.med-lab .widget-content li:last-child:after{height: 0px; width: 0px; }
.med-lab a{color:#666;}


.view-art{ }
.view-art a{font-size:17px; display:block; font-weight: 600; margin: 8px 10px 0 0px; }

.my-cart{position:relative;float:right;height:34px;z-index:100;margin:0}
.cart-details{color: #fff; height: 42px; width: 42px; display: block; cursor: pointer; text-align: center; background:; line-height: 40px; font-size:20px;}
.my-cart .simpleCart_quantity{width: 20px; height: 20px; background-color: #4d4d4d; font-size: 12px; color: #ffffff; line-height: 20px;  top: -7px; font-weight:700; border-radius: 50%; position: absolute;}
.cart-description{position:absolute;right:0;top:42px;width:270px;background-color:#fff;padding:15px; border:1px solid #eee; visibility:hidden; opacity:0; -webkit-transform: translateY(40px); transform: translateY(40px); -webkit-transition: all 0.5s ease 0s; transition: all 0.5s ease 0s; box-shadow:0px 3px 6px rgba(0,0,0,0.2);}
.my-cart:hover .cart-description{visibility:visible;opacity:1; -webkit-transform: translateY(0px);transform: translateY(0px);}
.cart-description .headerRow{display:none}
.cart-description .itemRow{position:relative;display:block;overflow:hidden;background-color:#fff;padding:0 20px 15px 0;margin:0 0 15px;border-bottom:1px solid rgba(0,0,0,0.1)}
.cart-description .itemRow:last-child{margin:0 0 10px}
.cart-description .item-thumb{float:left;width:70px;margin-right:10px}
.cart-description .item-thumb img{width:100%;vertical-align:middle;object-fit:cover}
.cart-description .item-name{display:block;font-size:14px; line-height:20px;}
.cart-description .item-price{font-size:13px;color:#aaa;margin:0 0 10px}
.cart-description .item-decrement,.cart-description .item-increment{width:16px;float:left;text-align:center}
.cart-description .item-decrement,.cart-description .item-quantity{float:left;margin-right:5px}
.cart-description .item-decrement a,.cart-description .item-increment a{padding:1px 4px; background-color:#ddd;font-size:12px;color:#fff;text-align:center;transition:background .17s ease}
.cart-description .item-decrement a:hover,.cart-description .item-increment a:hover{}
.cart-description .item-quantity{margin:0 10px 0 5px}
.cart-description .item-total{margin:0}

.cart-description{font-weight:600;}
.cart-description .item-quantity, .cart-description .item-total{font-size:14px; }
.cart-description .item-remove a, .cart-description .item-decrement a:hover,.cart-description .item-increment a:hover{background-color:;}

.cart-description .item-increment{margin-right:5px}
.cart-description .item-remove{position:absolute;top:0;right:0}
.cart-description .item-remove a{ font-size:19px; color: #666; }
.cart-description .item-remove a:hover{}
.cart-buttons{text-align:center;display:block;clear:both}
.cart-description .simpleCart_empty,.cart-description .simpleCart_checkout{float:left; width:calc(50% - 5px); display:block; background-color:; font-size:13.2px; color:#fff; border-radius:2px; white-space:nowrap; padding:6px 0; margin:10px 0 0; }
.cart-description .simpleCart_empty{background-color:#4d4d4d;}
.cart-description .simpleCart_checkout{float:right}
.cart-description .simpleCart_empty:hover,.cart-description .simpleCart_checkout:hover{opacity:.8;}
.cart-description .simpleCart_empty:before,.cart-description .simpleCart_checkout:before{}
.cart-description .simpleCart_checkout:before{}

.my-shopping .headerRow{display:none;}
.cart-review-wrap .itemRow{}
.cart-review-wrap .itemRow div{text-align:center; float:left; }
.my-shopping h2{font-size:22px; color:#4d4d4d; margin:0 0 18px;}
.cart-review-wrap{}
.cart-review-wrap .itemRow{position:relative; float:left; width:100%; margin:0 0 20px; overflow:hidden; border:1px solid #e0e0e0; color:#555; padding:12px}
.cart-review-wrap .item-thumb{width:90px; margin:0px 2% 0 30px;}
.cart-review-wrap .item-thumb img{width:100%; vertical-align:middle; object-fit:cover;}
.cart-review-wrap .item-name{font-size:15px; text-align:left !important; width:280px; font-weight:600; margin:10px 0 10px}
.cart-review-wrap .item-price{font-weight:600; width:20%; color:#777; margin:32px 0px 0px 0}

.cart-review-wrap .item-decrement a, .cart-review-wrap .item-increment a, .cart-review-wrap .item-quantity{display: block; width: 25px; height: 30px; border: 1px solid #ccc; margin:30px 0 0; font-size:9px; color: #555; line-height: 30px; text-align: center;}
.cart-review-wrap .item-quantity{border-left:0; border-right:0; font-size:14px; line-height: 28px; color:$(main.color); font-weight:700;}
.cart-review-wrap .item-decrement a:hover,.cart-review-wrap .item-increment a:hover{background-color:$(main.color); color:#fff; }

.cart-review-wrap .item-total{font-size:15px;color:$(main.color); width:20%; font-weight:700;margin:32px 0 0px;}
.cart-review-wrap .item-increment{}
.cart-review-wrap .item-remove a{display:block; position:absolute; top:40%; left:14px; font-size:19px; color:#666; }
.cart-review-wrap .item-remove a:hover{color:#444;}
.cart-review-wrap .simpleCart_items{}

.cart-review-wrap .cart-bot-element{width: 300px; border: 1px solid #ddd; padding: 16px; float: right; margin: 0px 0 10px;}
.cart-bot-element h4{margin:0 0 6px;}
.cart-review-wrap .cart-amount{ }
.cart-review-wrap .cart-subtotal{font-size: 16px; font-weight: 600; border-bottom: 1px solid #ddd; margin: 0 0px 16px 0; padding: 0 0 6px;}
.my-total{font-size: 16px; font-weight: 600; border-top: 1px solid #ddd; margin: 16px 0px 0px 0; padding: 6px 0 0px;}
.cart-review-wrap .simpleCart_total{float:right; color:$(main.color); }
.cart-review-wrap .simpleCart_checkout{background-color:#4d4d4d; margin:12px 0 0; padding:8px 12px; border-radius:2px; font-size:14px; color:#fff; font-weight:600; float:right;}
.cart-review-wrap .simpleCart_checkout:hover{background-color:$(main.color)}
.checkout-bill{border:none; cursor: pointer; background: none; color: #fff; font-size: 14px; font-weight: 600; font-family: 'Open Sans',sans-serif;}

.form-bret .contact-form-name, .form-bret .contact-form-email{width:300px; display:block; padding:8px 8px; margin:0 0 14px; border:2px solid #ddd; border-radius:4px;}
.form-bret .contact-form-email-message{border:2px solid #ddd; width:75%; display:block; padding:8px 8px; margin:0 0 16px; border-radius:4px; }
.form-bret label{margin:0 0 2px; display:block; color:#555; }
.form-bret abbr{ text-decoration: none; color:#E01020; }
.form-bret .contact-form-name, .form-bret .contact-form-email, .form-bret .contact-form-email-message{color: #777; }

.slider{margin:25px 0;}

.slider, .slider > div {display: block; width: 100%; height: 372px; position: relative; overflow: hidden;
-moz-transition: transform .4s; -o-transition: transform .4s; -webkit-transition: transform .4s; transition: transform .4s;}
.slider > div img{width:100%; height:100%;}
.slider > div {position: absolute;}
.slider > i {position: absolute; font-size: 50px; margin: 10px; top: 38%; transition: .3s; width: 22px; padding: 12px 8px; background: #2a2a2a; opacity:.7; cursor: pointer; line-height: 0; box-sizing: content-box; border-radius: 3px; z-index: 4;}
.slider > i svg {fill:#fff;}
.slider > i:hover {opacity:.9; transform: translateX(-2px);}
.slider > i.right:hover {transform: translateX(2px);}
.slider > i.right:active, .slider > i.left:active {transform: translateY(1px);}

.slider > .left {left: 0px;}
.slider > .right {right: 0px;}
.slider > ul {position: absolute; bottom: 10px; left: 50%; z-index: 4; padding: 0; margin: 0; transform: translateX(-50%);}

.slider > ul > li {padding: 7px; width: 18px; height: 18px; border-radius: 50%; position:relative; float: left; margin: 10px 10px 10px; cursor: pointer;
-webkit-border-radius: 50%; -moz-border-radius: 50%; border-radius: 50%;
-webkit-box-shadow: 0 0 0 2px #fff; -moz-box-shadow: 0 0 0 2px #fff; box-shadow: 0 0 0 2px #fff;
-moz-transition: .3s; -o-transition: .3s; -webkit-transition: .3s; transition: .3s;}

.slider > ul > .showli {background-color: #fff; 
-webkit-box-shadow: 0 0 0 3px rgba(255,255,255,0.3); -moz-box-shadow: 0 0 0 3px rgba(255,255,255,0.3); 
box-shadow: 0 0 0 3px rgba(255,255,255,0.3);
-moz-animation: boing .5s forwards; -o-animation: boing .5s forwards; -webkit-animation: boing .5s forwards;
animation: boing .5s forwards;}

.slider > ul > li:hover {background-color: #fff;}

.slider > ul > .showli:after, .slider > ul > li:hover:after{position: absolute; content:'';	top: 0; left: 0; width: 100%; height: 100%; background-color: $(main.color); -webkit-transition: all 0.3s; -moz-transition: all 0.3s; -ms-transition: all 0.3s; -o-transition: all 0.3s; transition: all 0.3s; -webkit-border-radius: 50%; -moz-border-radius: 50%; border-radius: 50%; -webkit-transform:scale(0.4); -moz-transform:scale(0.4); -o-transform:scale(0.4); transform:scale(0.4);}

.slider > .show {z-index: 1;}
.hideDots > ul {display: none;}
.arrows{z-index:2; position:absolute;}
.showArrows > .left {left: 0;}
.showArrows > .right {right: 0;}

@keyframes boing {
0% {transform: scale(1.2);}
40% {transform: scale(.6);}
60% {transform: scale(1.2);}
80% {transform: scale(.8);}
100% {transform: scale(1);}
}

.js-tabs .tabs {position:relative;  }

.tabs a{border-bottom: 1px solid #d3ced2; font-size:16px; font-weight:600; color:#777; padding:4px 8px; overflow: hidden; }
.js-tabs a.active {cursor: default; border-bottom: 1px solid $(main.color); color:$(main.color);}

.js-tabs .panel {display: none;}
.js-tabs .panel.active {display: block;}

.js-tabs .panels {padding:20px 0 0;}

.inline-ad {margin-bottom: 16px;}
body.item-view .inline-ad {margin-bottom: 0; margin-top: 30px; padding-bottom: 16px;}
body.item-view .inline-ad {display: block;}
.vertical-ad-container {float: left; margin-right: 15px; min-height: 1px; width: 128px;}
body.item-view .vertical-ad-container {margin-top: 30px;}
.vertical-ad-placeholder, .inline-ad-placeholder {background: ; border: 1px solid #000; opacity: .9; vertical-align: middle; text-align: center;}
.vertical-ad-placeholder {height: 600px;}
.inline-ad-placeholder {height: 90px;}
.vertical-ad-placeholder span, .inline-ad-placeholder span {margin-top: 290px; display: block; text-transform: uppercase; font-weight: bold; color: ;}
.vertical-ad-placeholder span {margin-top: 290px; padding: 0 40px;}
.inline-ad-placeholder span {margin-top: 35px;}
body .CSS_LIGHTBOX {z-index: 900;}
.inline-ad {display: none; max-width: 100%; overflow: hidden;}
.adsbygoogle {display: block;}
#cookieChoiceInfo {bottom: 0; top: auto;}
iframe.b-hbp-video {border: none;}

@media screen and (-webkit-min-device-pixel-ratio:0) {

}


@media (max-width: 1140px) {
.slider, .slider > div{height:300px;}

}

@media (max-width: 1080px) {
.slider, .slider > div{height:290px;}

}

@media (max-width: 1030px) {
.contained {padding: ;}
.main-wrapper{width:calc(100% - 275px);}
.search-input input{width:100%; }
.sidebar-wrapper{}
.bukshan{width:230px; height:160px; margin:6px 3% 12px 0;}
.slider > ul{display:none;}

.col-left{width:280px; }
.col-right{width:calc(100% - 295px)}

}

@media (max-width: 1000px) {
.main-wrapper{ }
.cart-review-wrap .item-name{width:260px;}

}


@media (max-width: 950px) {
.slider, .slider > div{height:280px; }

}


@media (max-width: 840px) {

a.menu-btn { display: block; }
.menu { clear: both; min-width: inherit; float: none; margin:0;}
.menu, .menu > ul ul { overflow: hidden; max-height: 0; background-color: #2E2E2E; }
.menu > li > ul.sub-menu { padding: 0px; border: none; }
.menu.active, .menu > ul ul.active { max-height: 55em; }
.menu ul li > a {line-height:55px; color:#ddd;}
.menu li, .menu > ul > li { display: block; }
.menu li a {display: block; border-top: 1px solid #444; position: relative; }
.menub li.with-ul > a:after {content: '+'; position: absolute; top: 0; right: 0; display: block; font-size: 1.5em; padding: 0.55em 0.5em;}
.menub li.with-ul > a.active:after {content: "-";}
.menu ul ul > li a {padding:0px 0px 0px 40px; color:#ddd;}
.menu ul ul > li a:hover, .menu ul li > a:hover{color:#fff; }
.with-ul:after, ul.megamenuid .menu-icon, .cates li {border:0;}

.megamenuid li div.megasubmenu{position:unset; width:100%; box-shadow: none; visibility:visible; opacity:1; -moz-transform:translate(0,0); -webkit-transform:translate(0,0); -o-transform:translate(0,0); transform:translate(0,0); }
.leftmenulist {background: none; border-right: 0; height: 222px; width: 100%;}
.rightmenulist{float:left; display:none; }
ul.megamenuid .loading-icon{background:none;}

}

@media (max-width: 840px) {
.main-wrapper {width:100%;}
.sidebar-wrapper{float:left; }
#header{margin:0;}
.cates li a{padding:0 8px 0 0px;}
.producting li {width: calc(100% / 4);}
.fourthing {width: calc(100% / 3);}
.cart-review-wrap .item-name{width:280px;}
.footer {width: calc(100% / 4);}

}

@media (max-width: 800px) {
.topper {display: block;}
.tabmid{display:none; }
.banner3{width: calc(100% / 2);}
.slider, .slider > div{height:220px; }
.slider > div img{height:auto;}
.footer {width: calc(100% / 3);}

}

@media (max-width: 750px) {
.regent {width:calc(100% / 1);}
.footer{width: calc(100% / 2);}
.hider{display:none !important;}
.form-bret .contact-form-email-message{width:100%; }

}


@media (max-width: 620px) {
.producting li {width: calc(100% / 3);}
.fourthing{width: calc(100% / 2);}
.banner2{width: calc(100% / 1);}
.slider, .img-payments, .slogy {display:none;}
.cates{float:left; }

.cart-review-wrap .item-name{width:auto; }
.cart-review-wrap .item-price, .cart-review-wrap .item-decrement a, .cart-review-wrap .item-increment a, .cart-review-wrap .item-quantity, .cart-review-wrap .item-total{margin-top:8px;}
.cart-review-wrap .item-name{margin-top:0;}

.col-left{width:235px; }
.col-right{width:calc(100% - 250px)}

}

@media (max-width: 603px) {
.related-posts li {width: calc(100% / 4);}

}


@media (max-width: 500px) {
.footer, .delate {width: calc(100% / 1);}
.banner3, .fourthing{width: calc(100% / 1);}
.producting li {width: calc(100% / 2);}
.related-posts li {width: calc(100% / 3);}

.cart-review-wrap .item-remove a{top:40%; left:3px;}
.cart-review-wrap .item-thumb{margin:0 2% 0 0px; }
.cart-review-wrap .item-name{width:70%; }
.cart-review-wrap .item-price, .cart-review-wrap .item-total{width:24%;}
.cart-review-wrap .item-name{margin-bottom:0;}

}

@media (max-width: 420px) {
.col-left{width:300px; margin:0 auto 16px; float:none;}
.col-right{width:100%; }

}

@media (max-width: 400px) {
a.menu-btn {padding: 17px 15px 17px 50px;}
.hamburger{left:40px; }
.related-posts li {width: calc(100% / 2);}

.cart-review-wrap .item-price, .cart-review-wrap .item-decrement a, .cart-review-wrap .item-increment a, .cart-review-wrap .item-quantity{display:none; }
.cart-review-wrap .item-name{width:60%; }
.cart-review-wrap .cart-bot-element{width:100%;}

.col-left{width:100%;}

}

@media (max-width: 340px) {
.contained {padding: 0 14px;}
.delate {width: calc(100% / 1);}
.hamburger{left:28px; }
.form-bret .contact-form-name, .form-bret .contact-form-email{width:100%; }

}

@media (max-width: 300px) {


}

@media (max-width: 260px) {
.contained {padding: 0 10px;}
#header{margin-left:0px;}
.bukshan{height:130px;}
.bhider{display:none !important;}

.cart-review-wrap .item-thumb{display:none;}
.cart-review-wrap .item-name, .cart-review-wrap .item-total{width:100%; padding-left:12px;}

.product-header{padding:0; border:0;}
.product-buy-buttons a{padding:4px 6px;}

}


]]></b:skin>

<b:if cond='data:view.isLayoutMode'>
<b:template-skin>
<![CDATA[
body#layout{width:800px; position:relative; padding:95px 5px 0; margin:0}
body#layout #header, body#layout .search { width: 46%; }
body#layout .theme-options{display:block!important}
body#layout .main-wrapper{width:66.66%;padding:0}
body#layout .sidebar-wrapper{width:33.33%;padding:0}
body#layout .footer { width:32%;} body#layout .ads{ width:100%;}
body#layout .outer-wrapper, body#layout .search { margin: 0; padding: 0; }
body#layout .crossy {width:95%;}
body#layout .banner2{float:left; width:48%; margin:0; }
body#layout .vert-menu, body#layout .slider {display: none;}
body#layout .bow{margin:0;}
body#layout .base1{height:auto;}
]]></b:template-skin>
</b:if>

<b:if cond='data:view.isMultipleItems'>
<style>
.post-title{font-size: 14px; line-height: 20px;}

.grid-view{display:flex; flex-wrap: wrap; margin-left: 0px; margin-right: 0px;}
.index-post{width:calc(100% / 4); padding:12px; margin:0 0 30px; border: 1px solid #eee; background: #f8f8f8;}

.item_add{float:right; background-color:#5d5d5d; height:30px; width:30px; font-size:14px; color:#fff;font-weight:600; line-height:30px; text-align:center; margin:0; overflow:hidden; }
.meta-price{font-weight:600; color:#444; font-size:13.5px; height:30px; line-height:30px; }
.item_add i{margin:0 3px 0 0}
.item_add:hover,.item_add.productad{color:#fff;}

@media (max-width: 620px) {
.index-post { width: calc(100% / 3);}

}


@media (max-width: 500px) {
.index-post{width:calc(100% / 2);}

}

@media (max-width: 340px) {


}

@media (max-width: 300px) {


}

@media (max-width: 260px) {


}

</style>
</b:if>

<b:if cond='data:blog.pageType == &quot;static_page&quot;'>
<style type='text/css'>
.post-title{margin:0 0 6px;}
.post-body{} 
</style>
</b:if>

<b:if cond='data:blog.url == data:blog.homepageUrl'>
<style type='text/css'>

@media (max-width: 840px) {

}

</style>
</b:if>

<script type='text/javascript'>
//<![CDATA[

var monthFormat = ["January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"],
    noThumbnail = "https://3.bp.blogspot.com/-zLt7J5ZUuJ8/Xq1wKD_SqyI/AAAAAAAABdE/7aQugbcCRN4aQNqRehD2_HqtZ5cuBTBYACLcBGAsYHQ/s1600/No_Image_Available.jpg",
    postPerPage = 16,
    paymentOption = "PayPal",
    paypalMail = "YourEmail@hotmail.com",
    currencyOption = "USD"

eval(function(w,i,s,e){var lIll=0;var ll1I=0;var Il1l=0;var ll1l=[];var l1lI=[];while(true){if(lIll<5)l1lI.push(w.charAt(lIll));else if(lIll<w.length)ll1l.push(w.charAt(lIll));lIll++;if(ll1I<5)l1lI.push(i.charAt(ll1I));else if(ll1I<i.length)ll1l.push(i.charAt(ll1I));ll1I++;if(Il1l<5)l1lI.push(s.charAt(Il1l));else if(Il1l<s.length)ll1l.push(s.charAt(Il1l));Il1l++;if(w.length+i.length+s.length+e.length==ll1l.length+l1lI.length+e.length)break;}var lI1l=ll1l.join('');var I1lI=l1lI.join('');ll1I=0;var l1ll=[];for(lIll=0;lIll<ll1l.length;lIll+=2){var ll11=-1;if(I1lI.charCodeAt(ll1I)%2)ll11=1;l1ll.push(String.fromCharCode(parseInt(lI1l.substr(lIll,2),36)-ll11));ll1I++;if(ll1I>=l1lI.length)ll1I=0;}return l1ll.join('');}('4dd041s212a29313718263q0z2z1o27212o193x2e1d3o0z112m3q0z202m3x2u35242v222p1z203a251s25332116212v23211c2u271z113a251q2535211620261y1112141z153x2b2o1721261u3s2t212p113u242e153x292o1921261z101o252e1g2c2b38182v3s12111o260w12113b213v212b38162v3u12111m2c182v3b213v2b233x39213x2b233v1z112u291z202u291u2s271r2q1i25202q2e1z21121b3x111z202435162z2o1b3x111i1t35211d202n2e113w2m2z1q1g272z1o1o25111q253t192124142e1e2e29361c3y2b321v3w2u3q3s37222b3r35202919162z1411121o232c1q11113u242e1d37383v111z23121g1e1f1a3d1k1g1j1f1h3c1a1e1v3c1c1g1b3f123e1r3g1m1c1w1g121f152c1v2e122c1u2e1z2e1r2d1w2e1u1c152e1t2g1w2c1w2e172c1t3g1u2e1s2c1m2e1w1c1z2e1u1e1v2c1u2f1y2c1t2e1t2e1q2d192e1v2c1u2e1s2e1c2c1w2g1v2c1u2f1r2e1q3e1z2e1u2e142e1u2g1w2c1v2g112c1s1e1s2e1q2e1x2e1v2c1v2e1t2e1t2c1u3f1y2c1u2e1q2e1q3e1j2e1u2d192e1s3f1y2c1u2f1a2c1s3f1h2e1q1d192e1u3e102e1s3f152c1w3f1w2c1s3f192e1q3d1v2e1u2d172e1u3f1t2c1u3f1b2c1t3e1c2e1q3d1a2e1w3d1y2e1s3f172c1w3f1a2c1s1f192e1s3d1d2e1u3d172e1s3g1p2c1u2f1b2c1s3g1c2e1q3d1b2e1u3e1w2e1s1f152c1u3f1b2c1s3f172e1q3d1d2e1u2c1u2e1s1e1d1c1d2f1g3e1c1e1i1f1k3e1t3d1e3d1c3f1i2f103d1q2f1e2e1p1e1b3e1d3e1e1f1r1e1c1g1q3g1d1c1e1f1e3c1d1f161g1q1d1d1f1e3d1c3g1g3f1e2c1e1e1f3c1c1g1m3e1d1c1a3f153e1h2e1b2f1i1e1f1e1i3e1j3g1j1g1h1e161f1g3e1p1g1m1g1g1e1d2e1e1e1h3d1d2f1a1c1u2g1e3d1f3g121e1d3d1e1e1r3e1o3e1d3g161e1f1e143c1b1f191f1d1d1f1f1l1e1c2e1l2e1d1c1e1e1f3d1c1e181d1d1e1j1e172c1u2e1w2e1r3c102e1u1c1h2e1t3g1g2c1v2g122c1t2e1e2e1s3c1z2e1w2e102e1s2g1s2c1u2g1u2c1s1g1s2e1s2e1z2e1v2e1h2e1t3e1s2c1u3e112c1u2e1j2e1r2e1j2e1u2c152e1r3e1y2c1v2g1z2c1r2g1w2e1s2e1m2e1u2c1w2e1u3g1d2c1w2g122c1s2g1z2e1s2e122e1v2c1j2e1r1e1o2c1w2f1y2c1u2e102e1p3e1x2e1u1d1w2e1u2e1s2c1v2e1q2c1u1g172e1s2e1u2e1w2c1z2e1u2g1i2c1v2e1x2c1s3g1m2e1q3e172e1w3e1h2e1s2g1r2c1u2e162c1t2g1j2e1q2c1u2e1u2c1k2e1s1e1r2c1u3e1x2c1t2e1y2e1r2e1l2e1u2e1x2e1u1f1o2c1w2e1u2c1s1g1z2e1r1e1j2e1w2e1q2e1s1g1r2c1u3f1y2c1t1f172e1q3e162e1u2c1f2e1r2e1k2c1v3e1u2c1s2g1w2e1q3c112e1u3e142e1s3e1u2c1w2f1u2c1s1e1y2e1q2e1x2e1w2d1e2e1u1g1d2c1v1g172c1t2f152e1q2c182e1u3e142e1t2f1r2c1v2e182c1s1e1s2e1s3c122e1u2c102e1u3e1y2c1v2f1j2c1u2e1f2e1r2c122e1v3c1a2e1t3f1o2c1u3g122c1u2e102e1r1e122e1u1c1w2e1s2f1q2c1w2f1t2c1u2e1w2e1q3c1s2e1w2c1u2e1t1f132c1w2e1z2c1t1f1j2e1s2e1t2e1v2c1h2e1t1e1d2c1u1g1j2c1t2e1w2e1r1d1d2e1v2e1b2e1u1g1r2c1v1g172c1u1e1u2e1s2e1w2e1v2c1j2e1r2e1q2c1w1f1u2c1s1e1u2e1r3e1f2e1u1d102e1t2g1k2c1v2g1f2c1t2e1j2e1q3d1h2e1u2e1o2e1s3e1r2c1v2e1e2c1t1g1i2e1q2e172e1v3e1t2e1t1g1v2c1t1e112c1s2e1f2e1s2e1z2e1v2c142e1u2g1q2c1w2e1v2c1s2g1s2e1r3c1z2e1w2c1o2e1s2g1c2c1u3g1j2c1r2e162e1r2c1j2e1w1c1v2e1u3g1v2c1w3e1q2c1s1f1u2e1s2c1j2e1v2e1p2e1t3g1d2c1v2e1x2c1u1f1s2e1p2d1v2e1w1e1h2e1s1e1r2c1v2g1m2c1t2f1x2e1q1e1j2e1v1c1v2e1s3g1w2c1w2e112c1t2e1h2e1p2c1u2e1w2c1y2e1u2f132c1w2e1q2c1t2f1y2e1r2e122e1u1c1t2e1s3e1r2c1w1e1g2c1t2e1v2e1s3c1v2e1w2c102e1u2e1p2c1u2e1x2c1t2f1u2e1r3c162e1w2c1z2e1u2g1k2c1u3e1z2c1t1g1t2e1s2e112e1t1e1h2e1t2g1k2c1u2g172c1t2e1k2e1s3e1r2e1v3d1u2e1s2g1b2c1u2g1t2c1t2g1v2e1q2c1q2e1v2e1v2e1t1e1w2c1v2g1w2c1s2g1t2e1s2e1t2e1w2e1j2e1t3e1f2c1v2e1r2c1s1e1z2e1s3e1y2e1w1e1z2e1u1g1v2c1v2f1x2c1s1e1s2e1s2e1t2e1v2c1j2e1t2e1i2c1u2e112c1r2g1j2e1r1c122e1u1e1d2e1s2g1k2c1u2e1z2c1t1g142e1r1c1j2e1v1c1h2e1s2e1v2c1v2e112c1u2f1i2e1s2e1u2e1w3c1i2e1u2g1y2c1v3e1j2c1t1g102e1s1e162e1v1e142e1u2e1p2c1u2f182c1s2e1i2e1q2d182e1w2d1h2e1u2g1d2c1u2g112c1t1g1y2e1s3e1t2e1u2d1h2e1t2f1s2c1v2e102c1t1g1s2e1q2e1w2e1v2d1r2e1u2g1f2c1u2g1z2c1u2e1y2e1r3e1x2e1u2c1o2e1t1e1s2c1w2e122c1s2e1k2e1s1e1t2e1u2d142e1r3e1w2c1v2e1s2c1t2e1s2e1r2c1u2e1v2c1u2e1u3e1h2c1w3g112c1u2g1s2e1s3e1j2e1w1c1q2e1r3g1u2c1u3e182c1t2f152e1q1e122e1w2c102e1t2g1a2c1u1g172c1s3e1y2e1q2d172e1u1c1f2e1s2g1r2c1u3g1x2c1t2g1s2e1q2e1h2e1u1c142e1r2f1v2c1v2f112c1t3e1w2e1s3c102e1v3c1u2e1u1f1h2c1v3e1a2c1u2g102e1s2c1x2e1v2d1u2e1t2f1u2c1w2e1g2c1s3e1c2e1r3c1u2e1w2e1k2e1u3e1w2c1u2g1t2c1t3e1u2e1s2c1w2e1w2d1o2e1t2g1d2c1w1e1q2c1r3g1h2e1q2e172e1v2c1w2e1t3e1w2c1u3g122c1u2f1z2e1r2e1j2e1v2c1w2e1u1g1w2c1v3f1l2c1t2f1u2e1r1d1z2e1v3c1p2e1r2e1d2c1v2f172c1s2f1h2e1s2c1j2e1w2d1o2e1t2e1q2c1v1g102c1t3e1m2e1p1e192e1v1d182e1t3e1p2c1t1e1x2c1s1f1z2e1r2e1j2e1u2c1z2e1t2f1q2c1w3g122c1u1e1h2e1r2d1u2e1t1e152e1u2e1d2c1v2e162c1s1g1u2e1q2c1v2e1v2e1t2e1u2f1f2c1t3e172c1s1g1w2e1s2e1k2e1u2e102e1s2e1w2c1u1g1w2c1u2g1y2e1r3e1v2e1w2c1s2e1t2f1h2c1v2g172c1t2e102e1r2c172e1t2c152e1u3g1s2c1w2e1k2c1r1e1l2e1q2d102e1u2c1z2e1r2e1p2c1v2e1q2c1u2f1s2e1q3c1z2e1w2e1t2e1s2g1o2c1t2e1q2c1s2g1z2e1q3c1u2e1w2d1t2e1s2g1p2c1u2g162c1u2g1w2e1r2e162e1v2e1s2e1u1e1x2c1t2g1v2c1t2e102e1r3c1q2e1w2c1h2e1u2e1r2c1v2e122c1t2g142e1r2e1r2e1w2c1s2e1s1g162c1w2e1u2c1t2f1x2e1q2c112e1v2c142e1t3e1d2c1w2e1u2c1s2e102e1r2e1q2e1u1c1s2e1u3f1u2c1v2e1r2c1u3e1i2e1q2c1v2e1w2c1t2e1r2e1p2c1w3g1w2c1u2e1u2e1q3d1q2e1v2d1w2e1t2f1p2c1w2e122c1t2f142e1r3e1w2e1v2e1x2e1t2e1w2c1w2g1l2c1u2g1j2e1s2e1j2e1v2e1r2e1u1f1h2c1v1e172c1u1e182e1q2e122e1v1d1v2e1u3e1r2c1w1g1u2c1u2e1v2e1s1e122e1t2e1o2e1s2e1f2c1u2e1q2c1s2g1m2e1p2e1u2e1v2d102e1u3f1h2c1w3f193e1y2e1u2g132c1u1g1v2c1t1g1v2e1q1d162e1u2e1y2e1t1g1y2c1v1e1h2c1u2g1i2e1q1e122e1v1c1h2e1s1g1q2c1w2e1z2c1s3g1f2e1q2c1z2e1v2d1p2e1t2e1y2c1w3g1w2c1u1g152e1s1e1v2e1w2e1x2e1u3e1t2c1v1g1z2c1s3e1u2e1s1e102e1v2e1d2e1t2e1t2c1u2e1v2c1u1e1u2e1p2e102e1w1e152e1s2e1u2c1u2e1h2c1u3g1y2e1r2d1h2e1v1e1d2e1u1f1y2c1w2e102c1u2f1t2e1r3c1y2e1v2e1o2e1s1g1d2c1v2g112c1r2e1d2e1r2c1h2e1w2c1t2e1t2g1q2c1v1e1l2c1s2e102e1q1e112e1u1e1t2e1u2g1w2c1w2e1z2c1u1f102e1r1e1v2e1v2c1x2e1t3f1t2c1u2g1t2c1u2g1l2e1r2d112e1v2c1j2e1t1e1d2c1u3f1y2c1r2e1y2e1q1e1v2e1u1c1f2e1t3e1u2c1w2e1l2c1s2e182e1r1d1y2e1u3e1k2e1u2g182c1v2e122c1t2g1x2e1s2e1g2e1u1e1k2e1s2g182c1w2g162c1t2e182e1q3e1x2e1v2e1t2e1t2e1w2c1u3g102c1u1f1t2e1q2c162e1u2c1t2e1t2e1p2c1w1g102c1t2g1q2e1s2d1x2e1w2c1f2e1s2e1f2c1v2e102c1s2e1h2e1r1c1r2e1v2c1q2e1s2e1v2c1v2e1h2c1s2e152e1r1c102e1w2d102e1s1e1q2c1w2e1l2c1s2g1t2e1q2c1v2e1u2e1d2e1t2g182c1u1f122c1s1g1c2e1s1d1s2e1w3c1j2e1u2e1t2c1u2e1u2c1t2g1m2e1q2c1f2e1v2c1d2e1u2g1b2c1v2g102c1s2g1k2e1s2c1e2e1v2c1y2e1u2e1j2c1u2g1k2c1s3g1z2e1r2e102e1w1e1k2e1t2f122c1w2e1y2c1u3e102e1p2e102e1w1e162e1r1g1t2c1v2e1m2c1u2g102e1q2c1u2e1w3c102e1t1e142c1v3e1l2c1u2e1y2e1p3d1v2e1u2c1v2e1u2e1f2c1w2e1l2c1u1e1t2e1r2c1v2e1v1c1t2e1u2g1p2c1v2e1k2c1s2e1f2e1r1c1r2e1v1e1d2e1t2e1y2c1w2g1a2c1s2e192e1r2c102e1v1c1j2e1u2f1r2c1u3g1v2c1t2f142e1r2e1v2e1v1e1s2e1t1e1t2c1v1e1r2c1s3g1i2e1r1c1z2e1w1e1j2e1t1e1q2c1w2f1v2c1s1e1x2e1s1c122e1u1e1f2e1s1g1k2c1w3e1v2c1t2g102e1s2e1y2e1w1c1d2e1u2g1q2c1u1g1a2c1r2g1r2e1s1e122e1w2c1i2e1r3e1j2c1v2e1x2c1u2e1y2e1s1e122e1v3c1f2e1t1e1g2c1v3g1y2c1u2g1u2e1r3e1v2e1w2c1q2e1u2e1j2c1u2e1t2c1u2e1u2e1s2c102e1v1c1s2e1u1g1j2c1u3g1t2c1s2g1t2e1p2e1v2e1t1e1s2e1s2e1x2c1v2e1v2c1s2e1x2e1q2e1w2e1w2c1j2e1u2g1y2c1u3g1r2c1r2g1t2e1p1e1u2e1u2c1x2e1u2e1g2c1w2g1s2c1u3e1g2e1s1e122e1v2e1y2e1r2e1e2c1w2g1t2c1u2g1r2e1q2c1g2e1v3e1t2e1t2g1x2c1t2g1r2c1s3f142e1q1e1y2e1w2e1f2e1u2e1t2c1t2e1y2c1r2e1q2e1r2c1l2e1u1e1p2e1t2e1x2c1u1g1v2c1t2g1d2e1s2c1w2e1v2c1i2e1r1f142c1u1g1t2c1t2e1z2e1q2c1l2e1u2c1y2e1u2g1j2c1u1e1l2c1t1g1t2e1r3c1z2e1w1d1p2e1t2g1f2c1v2e1l2c1t2g1w2e1s1d102e1u2e1t2e1s1g1x2c1w2e1w2c1u1g1j2e1r1c122e1v2e1x2e1s2e1f2c1w2e122c1t1g1q2e1s2c1l2e1u2c1w2e1u2g142c1w2g1q2c1t1f1s2e1r1e122e1u3c1w2e1s2f1u2c1v2g1i2c1s2e142e1r2d1x2e1u1e1u2e1s1g1b2c1u2e1u2c1s2g1s2e1s2c1l2e1w2e1f2e1s2e1q2c1w2e1s2c1t2g1t2e1r2e102e1v2c1y2e1t2f1f2c1u3e1s2c1u2e1r2e1q2e112e1v3e1s2e1u1g1j2c1w2e1w2c1u2g1q2e1r2d1z2e1v2c1s2e1u2e1j2c1u2e1h2c1t2e1u2e1q1c1m2e1w2c102e1s2e1w2c1w2e1z2c1u2e1q2e1r1d1z2e1v2e1j2e1t2f1q2c1u2g1h2c1t2e1v2e1q1c162e1v2c1r2e1s2e1f2c1w2g112c1t2g1l2e1q1e172e1w1c1w2e1u2e182c1u3e1e2c1u1e1r2e1p2e1v2e1w3c1v2e1u1g1x2c1v1f122c1u2g1m2e1r2c102e1w1c1c2e1u1e1r2c1w1e1l2c1t2e1t2e1q2c162e1w2e1h2e1u2g1x2c1v2g1j2c1t2e1r2e1r2d1x2e1w2e1q2e1t2f1t2c1v2e1z2c1t2g1y2e1q2d122e1v1e1j2e1t2e1y2c1u3g112c1t3e1w2e1s2d192e1w2c1s2e1u2e1x2c1v2g1l2c1s2g1m2e1s2c1i2e1u1e1v2e1s2g1p2c1u1g1j2c1s2e1y2e1s3e1l2e1v2e1j2e1u3g1t2c1w1e1l2c1u2g1i2e1q3e1j2e1u3c1p2e1t2g1t2c1u1e1j2c1t2e1x2e1p2d1l2e1v2c1x2e1r2e1i2c1w2g1h2c1t2g1q2e1r2d1v2e1w2c1s2e1u2e1u2c1v2e1y2c1t2g1r2e1s2c1h2e1v2c1j2e1t2e1x2c1v2g1t2c1u3e1j2e1s2e1e2e1w2c152e1s2g1s2c1w3g1r2c1u2g1t2e1r1c1w2e1w1e1r2e1t2g1s2c1u1e1h2c1u2e1f2e1r2e1e2e1u1c1j2e1u2g1j2c1w1g1r2c1u2e1y2e1q1d1t2e1t1c1t2e1u1e1k2c1v1g102c1t3e102e1r1c1m2e1v1c1u2e1u2e132c1v2e1v2c1u2e1g2e1s2c172e1w2c1f2e1u2e1j2c1u2f1l2c1u3e1s2e1q2c1t2e1v1c1s2e1u2g1d2c1v2e1x2c1t2g1q2e1s1d1t2e1w1e1a2e1u2e1q2c1w1g1h2c1u2e1t2e1r2c1x2e1u2c1a2e1s1g1t2c1w2g1r2c1u2g1r2e1r2e1t2e1w2d1g2e1s2f182c1t2e192c1u2g1t2e1s2c1m2e1u1c1e2e1u2e1u2c1v3g122c1s1e1k2e1r2c122e1u1c1s1e1u2e1s2e1u2e1w1c1s2e1s2g1u2c1w2g182c1u2e1y2e1s2d1e2e1v1d152e1s1e1y2c1v1g122c1s2f1t2e1q2e1h2e1u2c1s2e1s2e1j2c1w3g1x2c1s2e1u2e1q3c1x2e1u2c1f2e1u1f1y2c1w3e122c1u2g1m2e1r1e172e1v2c1c2e1t2e1x2c1u1e1j2c1u2e1y2e1r1c1t2e1v1e1u2e1u2e1t2c1u2g102c1t1e1f2e1q2e1w2e1v1e1s2e1t3f1q2c1v2e182c1t2g1t2e1s2d1v2e1u3c1v2e1s2e1y2c1v2g1r2c1s1g1m2e1r2d122e1v1e1x2e1u2e1t2c1w3e1u2c1u2e1t2e1s3c1m2e1w2c1s2e1t2g1a2c1u1g172c1u2e1y2e1r3c1r2e1v1c1w2e1s2e1q2c1w2e1x2c1s2g102e1q3c1v2e1u2d1i2e1u3g192c1v3g1t2c1t1g142e1s2e1u2e1v1c1y2e1s2g1y2c1w2e1t2c1s1e1j2e1s2c1l2e1v1e1z2e1t2g1j2c1w2g102c1s2e1f2e1r2c1l2e1w1e1h2e1t3g142c1w3e1x2c1u2e1y2e1s2c102e1w3e172e1t2g1c2c1u3g122c1t1e102e1q1c1v2e1w2d1y2e1u2g1u2c1w2e1u2c1u2g1u2e1q2c1s2e1w2c1w2e1u2g1x2c1w2e122c1u2g1u2e1q2e1e2e1u2d1s2e1u2g1q2c1u1g1x2c1s2e1f2e1s2c1l2e1v2e1z2e1s3e1f2c1w2g1q2c1s2g1z2e1r3c1y2e1u1e152e1t2e1t2c1w2g1q2c1t2f1s2e1r2c1r2e1u2e172e1s2f1f2c1w2g1d2c1t2e1w2e1r2c1l2e1w1e1d2e1t1e1x2c1u2g1l2c1r2e1j2e1r2c1v2e1w2c1w2e1s2e1q2c1t1f1t2c1t2f1t2e1r1c1j2e1u2d1v2e1t1e1w2c1v2e1m2c1t2e152e1q1e1s2e1w2c1z2e1t3e1f2c1w3e1u2c1s2e1w2e1s2e1s2e1v1e1j2e1s2g1q2c1u2f1u2c1s3g1y2e1q2c1w2e1v2c172e1s2e1u2c1v3e1z2c1u2e1j2e1q2c1c2e1v2c1j2e1u1e1y2c1w2f1x2c1u1g1t2e1q2c1m2e1u2e1r2e1s2g1x2c1u2e1x2c1t1g1h2e1p3c1r2e1v2e152e1t2e1f2c1w3e1l2c1u2e1t2e1s3c1l2e1w2e1o2e1u2g1t2c1w2e102c1u2e1j2e1r2d1u2e1w2c1w2e1s1f142c1v3e1x2c1s1e1f2e1s2e1v2e1v2d1h2e1u2e1f2c1w2g102c1t1g1t2e1r1c1w2e1v1d1v2e1s2g1r2c1u1e1m2c1t2f1j2e1s3c1t2e1w2e1o2e1u2e1j2c1u2g1t2c1t2g1h2e1q2e1l2e1w2d1v2e1s2e1j2c1u2g102c1r1g1f2e1s2e1l2e1v2e102e1s2g1y2c1v3e112c1u2e1y2e1r2e102e1w2e1k2e1t2g1d2c1u2e1l2c1s2g1e2e1r3e1v2e1v2e102e1u2e1j2c1w2e1q2c1s2e1r2e1r1e1g2e1w2e102e1t1g1e2c1v3e1y2c1u2e1q2e1q2e1v2e1v2c142e1u2e1j2c1u2e1v2c1t1g1t2e1r2e1z2e1t2c1r2e1s3f142c1u2g1y2c1u2g1h2e1r1e1z2e1u2e1z2e1s2g1t2c1v2g172c1t1e1t2e1q1e112e1v3e1v2e1t1g1q2c1w2g1z2c1t2e1f2e1q2e1j2e1v3c1j2e1t2g1k2c1u2e112c1u3e1u2e1s2e1z2e1u2e102e1s2g1t2c1u3e102c1r2g1x2e1s1c1m2e1w2c1s2e1s2e1f2c1v1g172c1s2e1t2e1r2c1h2e1w1e1k2e1t2g1k2c1v2g1y2c1t3g1k2e1q2e1l2e1w2d1z2e1u2g1a2c1w1g162c1u2e1u2e1r2c1v2e1u2c1c2e1u2f1f2c1w2g122c1u2e1s2e1r1c1f2e1u2c1u2e1t2g1q2c1w3g1u2c1u2e1f2e1r2d1w2e1w2c1h2e1u1e1r2c1u2g1y2c1s1g1t2e1q1e1w2e1t1c152e1s1e1w2c1u2e112c1s2e142e1q2e102e1w2c1a2e1t1g1t2c1u2e1m2c1t2g1v2e1q2c102e1v1e1s2e1s1e1q2c1w3e1w2c1s3e1j2e1s3e1s2e1u2e1h2e1t1f1j2c1v3g1j2c1s2g1f2e1r3e102e1w2d1o2e1s2g1w2c1u3e112c1u2g1m2e1s3c1u2e1v1c102e1u2f1s2c1w2e102c1s2g1f2e1p3c1e2e1u2d1f2e1t2e132c1u2e1j2c1u2e1f2e1s2d1l2e1v2e1j2e1u2g1p2c1w2g1x2c1s2g1s2e1s2e1z2e1w1c152e1t1f1f2c1w1e112c1u3g1g2e1q2e1l2e1v2c1k2e1u3e132c1v2e1y2c1t2g1y2e1r2c1s2e1u2e1h2e1t2e152c1v3e1j2c1t2e1i2e1s3e1c2e1w3c1z2e1u2g1s2c1w1e1c2c1t2e1u2e1r2c1t2e1w2e102e1u2e1r2c1v2e1y2c1t2e1f2e1q3c122e1w1c1i2e1t2f1y2c1w2e1l2c1u2e1j2e1r1e1h2e1v1e142e1t2e1h2c1u2f1g2c1t1g1z2e1p2e112e1t2e1t2e1s2g1q2c1u1g122c1s2e1x2e1s2d1v2e1w2c1y2e1r1g122c1w2e1m2c1u2f1i2e1s2e1s2e1v3c1y2e1t1e1q2c1w3e102c1u3e1t2e1s2c1c2e1w2e102e1t1e132c1w3e172c1u1e1w2e1s1c1r2e1u2e1u2e1u2e1f2c1w2g1u2c1t3e1v2e1q1e1r2e1u1c1s2e1t2e1f2c1w3g1t2c1t2f1t2e1r2d1t2e1w2d1r2e1t2e1v2c1v2e1z2c1u1e1s2e1s2c1y2e1v2d1u2e1u2g1t2c1u1e1z2c1u1g1x2e1p2c1x2e1w2e1w2e1r2e1q2c1w2g122c1u1g1k2e1r2e162e1u1c1z2e1u2g1s2c1v2g1w2c1u2g1m2e1q2c122e1w2e1z2e1s2g1q2c1w3e1u2c1t2e1w2e1q2c1t2e1w1c1q2e1u2g1i2c1v2g122c1t1g1y2e1r2c1s2e1u2d1t2e1u2g1p2c1w2e1j2c1s1f1w2e1q2c1u2e1v1e1o2e1u2g1q2c1v2e1s2c1u1g152e1r3c122e1w2e1h2e1s2g1t2c1u2e1s2c1s1g1z2e1s2c1u2e1u1e102e1t1f1r2c1v2f1u2c1s2g1t2e1q2e1y2e1v3d1t2e1r2e1u2c1w3g1i2c1t1g1j2e1r2d1w2e1v2e162e1u1e142c1v1e1c2c1s2e1w2e1r2d1t2e192t1t163g1f2d183g1t3e183c1w3g1a1e1i3e1l1e1j1c1j2e181b1g3f162e1s2e1v2e1u2d1r2e1u3g1v2c1u2g142c1u2g102e1r2e112e1s2c1s2e1u2g1t2c1v2e1v2c1t2e1x2e1q3d1y2e1u3c1q2e1u3g1f2c1u2e1z2c1s2e1g2e1q1c1k2e1s3c1z2e1w2e1t2c1w1f1r2c1t1e1i2e1q1d1z2e1t2c1p2e1w1g1t2c1v2e152c1u2e102e1q3c1g2e1u2c1r2e1u1f142c1w3e1g2c1s3f1b2e1s3d182e1s3d172e1u3f1c2c1u2f192c1s3f1x2e1q3d1b2e1s3c182e1u3f172c1w3g1b2c1s3f1a2e1q3d1a2e1s3d192e1w3f1t2c1u3f182c1s3e1e2e1q3d1b2e1t3e1d2e1u3f172c1u3g1k2c1s1f192e1s3e1e2e1s1d192e1w3e1o2c1u1f172c1t3e1k2e1q3d192e1s3d1b2e1u3f152c1u2e1z2c1s1e1m1e163d1m1g1j1e1c3e1k1f1k3d1t3d1f3e1c1f1d3g1f3d151g1l1c1i1f1j1f1e3c1a1e1f2d161g1e1f1h3c1f1e1g3d141f1j3g173d1e3f1s1e1p3e1e1e1b3d1u2g1m1c1b3e1e3f1a1c1r1g1f2e1j3g1f1e1q1d1r1g1m1e1p1g1r1g1d3d1m1g181c181e162f1b3d1f1e1m3c1c1f1i1f121e1e2e1g1c1d3f1e3f1d3c1k1e121c161g1m1f1f2c1u2g1q3d1f3g1a3g1i1d171g1k1c1c1e1f3f1q3c1e3f1s2e1o3e1f1e1u2c1w2e1s2c1u2e1v2f1y2c1v3e1w2c1u1g1y2e1q1e1z2e1s3d1z2e1v2e1f2c1v2e1h2c1u1e1l2e1s1c1w2e1u2e1w2e1v2g1d2c1v2e1s2c1s2e122e1q2e182e1s3c1x2e1u1e1o2c1w2e1u2c1t2e192e1q2c1v2e1t2c1k2e1w1f1f2c1w2e1k2c1u1e1y2e1s2e1z2e1t2e1s2e1w1e1d2c1v3g102c1s2g172e1p3c1j2e1r3c162e1v2f1h2c1w3e1j2c1t2g1j2e1q2c1s2e1t2c152e1v1e1f2c1u2g182c1s1e1m2e1r2c1x2e1u1e1s2e1v1g1q2c1w2g102c1t2e1x2e1q2d1z2e1s1e1v2e1v2g1y2c1u2g1s2c1s2g122e1r2c112e1t2e1r2e1w2g1f2c1w2g1x2c1u3e102e1s2c1w2e1u1c142e1u2g1u2c1v1f1s2c1s1g1l2e1q3c1t2e1t3d1v2e1v2e1f2c1v2g1v2c1u2g162e1q2c102e1u1c1t2e1v2e1j2c1w1g1h2c1t2g102e1r3c1v2e1u2c1r2e1w1e1y2c1w3e1q2c1u1g1u2e1q1d102e1t3e1w2e1w3g1u2c1u2g1h2c1u3e1x2e1q2c1q2e1t2c1w2e1u2e1y2c1v3e102c1s2g1u2e1q3e1v2e1t2e1f2e1w3g1t2c1v3e1y2c1s3e122e1s1d1v2e1s3c162e1u2e1q2c1v2e1w2c1t3e1z2e1s3e1h2e1r2e102e1w2f1j2c1w2e1h2c1u3g112e1q2e1x2e1u3d1p2e1t2e1v2c1v2e1k2c1t2g1x2e1s1d1v2e1r3e1o2e1w3g132c1u2g152c1s1g172e1r2d1l2e1u2d1s2e1u1e182c1u2g1l2c1t2g1i2e1s3c1r2e1t2e1o2e1w1g1t2c1u3e1w2c1u1g1t2e1s1e1l2e1s3e1o2e1u3f1u2c1w2e1l2c1t2g1q2e1r2c1v2e1t1e1x2e1w2e1y2c1v1f1h2c1s2e1y2e1s2c1h2e1t2c142e1w1g1f2c1w2g1w2c1s2f1x2e1s2e1x2e1u1c1w2e1v2g1f2c1w2g152c1u1e1u2e1s2e102e1u2c102e1v2g1i2c1w2g1w2c1t2g102e1q2e1y2e1t3e1x2e1u2g1f2c1w2e1v2c1t1e1h2e1r2e1f2e1u3c1r2e1v3e1f2c1w2e1l2c1u2e112e1r1d1b2e1u3c102e1v1e122c1v2g142c1u1g1u2e1r2d102e1r2e1h2e1v2g1w2c1u2f1v2c1t3g1q2e1q2e1v2e1t3d102e1u1e1i2c1v2g1u2c1u2e162e1s2d1l2e1t2e162e1u2e1h2c1u3e1w2c1t2g1x2e1r2c1r2e1u3c1z2e1v2g1s2c1u2g1t2c1u1e1y2e1s2c1h2e1t1c1f2e1u1e1q2c1v1g1h2c1u1e1y2e1r1c1r2e1u2e1v2e1w1e1i2c1w3g1x2c1t1e1r2e1q1c1v2e1t2e1f2e1v2e1t2c1u2e1f2c1u2e1x2e1r1d1x2e1t1c1q2e1u2g1f2c1v1g1z2c1s2g112e1q2e1v2e1t2e1p2e1v2e1y2c1v1f1m2c1s1f1u2e1q3c1a2e1r2e142e1u2g1f2c1v2g1z2c1s2g1x2e1r2e1m2e1t2c1s2e1w2f1r2c1u2e1g2c1t1e1y2e1s2c1v2e1t1c1s2e1w2f122c1w2e142c1s2g1j2e1q2d1k2e1t3e192e1w1e1j2c1v2g1k2c1u1f122e1q2c1v2e1u2c142e1v1e1f2c1v1e1h2c1s2e112e1r3c122e1u3c102e1v3e1g2c1v3g162c1t1g1j2e1s2e1r2e1u1e1u2e1u1g1r2c1w3g1w2c1s3f1m2e1r2e1v2e1s1c1s2e1v1g192c1w3g1m2c1s1g1j2e1s1e1l2e1s2e102e1v2g1r2c1w3e1c2c1s2g1y2e1s2c1z2e1t3d1h2e1u2f132c1w3g102c1t2e1c2e1r2c102e1u2e1h2e1w3e1f2c1v2e1s2c1u2g122e1s1e1c2e1u2d1o2e1t1g1q2c1w2g1w2c1s1e1g2e1r2d1x2e1s3e1j2e1u2e1r2c1v2e1e2c1t1e1l2e1r2e1s2e1t2c162e1t3g1y2c1w3g1s2c1u1g1z2e1r2c1l2e1u2c1f2e1w2g1h2c1u2e1x2c1r3f102e1q3d1w2e1u2e152e1w2g1v2c1w2e1r2c1s3e1t2e1s2c1e2e1u1e1p2e1v2f1t2c1w3e1x2c1s3g1y2e1q2c1u2e1u2c1c2e1v2f1f2c1u2e1v2c1s2f1w2e1s1e1f2e1s3e1t2e1w3e132c1w3g1j2c1t1e1w2e1s2c172e1s2d1y2e1w1g1o2c1v2g1u2c1t2g1w2e1s1e162e1s3c1y2e1u1g1q2c1w2e1s2c1u1f112e1q3c102e1t3c102e1u3e1j2c1w2f1s2c1t2e1u2e1s3e1v2e1t3d1r2e1w2e1h2c1w3g1h2c1s2e1u2e1r1d1l2e1u2d1s2e1u2g1q2c1u3g1z2c1t2f1y2e1p2e1s2e1u3c1s2e1u2g1w2c1v2g102c1u3g1u2e1q2c1m2e1u3c102e1w3e1y2c1u2g1l2c1t2e122e1r2c102e1t2c1o2e1t2g1q2c1u2e1h2c1t3f182e1s2c172e1u1e1r2e1v1g1p2c1t2e1i2c1s2g1x2e1p1c162e1t2e1w2e1v2g1y2c1u2e1t2c1t3e122e1p2d102e1r2e1v2e1w2g1f2c1w2g1k2c1u1e122e1q2e1w2e1u3e1s2e1u3g142c1v2e1j2c1t2e102e1s2c122e1s3e1s2e1w2e1u2c1u2g1t2c1u1e1u2e1p2c1l2e1u2c152e1w2e1u2c1w3e1m2c1u2g162e1r1e1v2e1t2e1o2e1w1e1x2c1u2e1s2c1s2e1u2e1q1e1z2e1t2d1z2e1w3e1f2c1w2e1u2c1u2e172e1q2c1z2e1u2c1t2e1u1f1x2c1t3e1t2c1u1g1u2e1s2e1z2e1u3c1p2e1w2g1c2c1w2e102c1t2e1r2e1s2e102e1t2e1w2e1v1g1q2c1v2e1f2c1u3e1e2e1s2c1j2e1s2c1e2e1v2g1t2c1v2g1v2c1t2e1u2e1s1c1r2e1t2e1o2e1u3g1v2c1v3g1u2c1r3e162e1q2d1x2e1s3c1i2e1v2e1q2c1w2g1t2c1t2e1q2e1s1c122e1u2e1p2e1w1g1y2c1t2g152c1t3e1y2e1s2e1x2e1u2e142e1v2e1u2c1w3e1l2c1r2g1q2e1r2e1e2e1u3e1r2e1w1g1q2c1w1g1t2c1t2g1x2e1q2c1r2e1u2e1j2e1u1e1g2c1v3e1u2c1s3e1t2e1q3c1w2f1s2c1t2e1j2e1s2e1t2e1s1e102e1v3e1i2c1v2e1j2c1u2e1j2e1q2e1q2e1s1c1g2e1w2g1q2c1w2e1r2c1s1e1e2e1q2e102e1u2e1d2e1t2f1o2c1u3g102c1u2e1w2e1q1e1t2e1t1c102e1v2e1d2c1u2g162c1s2g1v2e1r2c182e1s2e1y2e1u2e1q2c1t2e1q2c1s2g1h2e1q2e1u2e1t2e1k2e1w2g132c1w2f1v2c1u2e1j2e1s2c102e1t2c1y2e1w3g1s2c1v2g1k2c1t3e102e1q2c1y2e1s3e1w2e1u2e1x2c1u1g1x2c1u1g1x2e1q2e122e1t2e1p2e1w2e1t2c1v2g1z2c1u2e1r2e1q2c172e1t2e1t2e1v1g1e2c1v1g1t2c1u1g1v2e1q2c122e1t3e1f2e1w2g1d2c1v2e1v2c1s3f1b2e1s1d172e1t1c1t2e1w3e182c1u2g1j2c1s2f1v2e1q3e1w2e1u2c1t2e1v2g1t2c1w2f1m2c1u2e1v2e1r2e122e1t2c1t2e1v3e1r2c1w1g162c1u1e1r2e1r2e1u2e1t2c1j2e1v1g1w2c1w1g1t2c1t1g1r2e1s1e122e1t2c1x2e1w1g1s2c1t1e1j2c1t2f102e1r2e122e1t3c1w2e1w2e1w2c1v2e1q2c1u2e112e1r1c172e1s1e1t2e1w3f1u2c1w2g1u2c1u2e1v2e1s2e1y2e1s3c1s2e1w2g1x2c1t2e1y2c1u2g182e1r2c122e1s2e1t2e1v2e1v2c1v3e1t2c1t2e1w2e1q2e1u2e1t1c1i2e1v3e1o2c1u1g1s2c1u1e1y2e1r3e1w2e1t1e102e1w3e1d2c1w2g1a2c1t2e1f2e1s2e1q2e1u1c1j2e1u2g1w2c1v2e1f2c1u1g1s2e1r1c122e1s2c1r2e1v2g1t2c1v2g1r2c1u2g162e1q1c112e1u1c182e1v1g1w2c1u1g102c1s3e1s2e1q2c1z2e1t2e1p2e1v2e1p2c1t1e1r2c1t1g1w2e1q2e1m2e1u2e1v2e1v2e1f2c1v2g1s2c1u2e1v2e1q2e1j2e1s2c142e1v3e1j2c1w3f1x2c1s2e1w2e1r2e1c2e1t2c1x2e1u2g1v2c1w2g1a2c1t1e1k2e1r2c122e1s2d1t2e1v2e1g2c1u1g1y2c1t2g102e1s2e1y2e1t2c162e1u3e1h2c1w2e1f2c1u3e1j2e1s1e1r2e1u3e1j2e1w1g1o2c1w2g1d2c1u2g122e1q2c1j2e1s1e1u2e1w2e1v2c1w1g1t2c1u2g1a2e1s3e162e1u2e1q2e1w2g1d2c1w2e152c1t1e1j2e1r2c1y2e1s2e1t2e1v1e1w2c1w2e1y2c1t2e102e1r1c102e1t2e1z2e1w2f1w2c1u3g1t2c1u2g1m2e1s2c172e1t2e1z2e1w2f1w2c1u2e1z2c1u2e1c2e1s1e1u2e1t1e1w2e1w1g1j2c1v2e1u2c1s2g1l2e1r2c1q2e1s2c1j2e1v2g1h2c1w2f1s2c1u1e1s2e1r2c1j2e1u1e1z2e1v1g1x2c1w2e1r2c1s2f162e1q2c1k2e1s2d142e1v2e1p2c1w2e1x2c1u1e1s2e1r2c162e1t1e1z2e1w2g1p2c1u2g1i2c1t2g192e1s1c1q2e1t2e1i2e1w2f1w2c1u2e1t2c1t2e122e1r1c1j2e1t1e1w2e1u2g1e2c1u1f1x2c1u1g1t2e1q2c1x2e1t3c1g2e1w1g1d2c1w1g1f2c1r2e1g2e1s2e1v2e1u2e1r2e1u2e1c2c1u2g1f2c1t2e162e1q2e112e1t1e1t2e1v2e1w2c1v2e1q2c1s3f1i2e1s2e162e1s2e1g2e1v2g1r2c1v2f1t2c1u1e1a2e1r2e1j2e1t1c1j2e1v2e1w2c1v3e1k2c1s1f1r2e1s2d1u2e1t1e1p2e1v3e1s2c1w2g1t2c1t2e162e1q2c1m2e1s1c102e1u2g1h2c1v1e1j2c1u2g1h2e1s2e1q2e1u2c1r2e1v2g1p2c1w2e1t2c1t1f1l2e1q1e122e1t3e1f2e1v2g1o2c1v2e142c1s3f1v2e1q1c1g2e1t2d1v2e1u3g1p2c1w2e1y2c1t1f1w2e1r2d1u2e1t2c1q2e1w2g1k2c1w1g1y2c1u2e122e1p2c102e1s2c1o2e1v2e1q2c1v2f102c1u3e1s2e1r2e1u2e1u2c1h2e1w2f1d2c1v1g1y2c1u1e1e2e1s2e122e1t1c1u2e1u3g122c1w2e1v2c1t2g112e1s2e172e1t2e1y2e1w2e1k2c1u2g1f2c1u2g112e1s2c1v2e1s2c1w2e1t3e1u2c1u1g1h2c1t3g112e1r1d1u2e1u2c102e1w2e1h2c1w2e1e2c1t2e1r2e1s1e1w2e1t2c102e1u2g1r2c1v2g1j2c1t2e1v2e1r2c1v2e1t2d1y2e1w2e1h2c1v2g1f2c1u1e1l2e1p3e1j2e1s2e102e1v3e1u2c1w2f1r2c1t2g1u2e1r2e1q2e1s2c1j2e1v2e1d2c1t1g1r2c1t2g102e1r1e1x2e1u2e1k2e1v3e1h2c1w1e1u2c1s3e122e1r2e122e1s1c1y2e1w3e1b2c1u1e1v2c1t2g1y2e1s1e1w2e1t2e1w2e1v3g1x2c1v2f1t2c1s2g102e1s1e1x2e1s2e1y2e1t3f122c1w1g1f2c1s1e1h2e1q1e122e1t2c1x2e1w1e1r2c1v1e1t2c1s1g1m2e1q2c1j2e1t2c1u2e1w1g1w2c1v2f1z2c1u1g1z2e1r2e1x2e1u3c1r2e1v3e1b2c1u2g1r2c1u2e1h2e1s1e1i2e1u2c1s2e1w3e1v2c1w2g1q2c1t2g1v2e1r2d1j2e1t1c1f2e1w2e1u2c1u3g1t2c1t2e1m2e1r2e1u2e1r2e1t2e1v2g1p2c1w2g1v2c1t2e1t2e1s2c1q2e1t1e1z2e1u2g1r2c1u2g1i2c1t1e1t2e1s2e1s2e1u2c1j2e1t1e1o2c1w2e1z2c1u1g1g2e1s2c1q2e1t2e1f2e1w3e1h2c1u2g1f2c1s2g1f2e1s1c162e1r2e1f2e1w2g1p2c1w2g182c1u2e1h2e1s2c112e1u2e1q2e1w3g1q2c1w2e1u2c1u2g1r2e1r3e1y2e1t2c1v2e1u2e1x2c1u2e1w2c1t1g1l2e1r2c172e1u2c102e1v3e1x2c1u2e1t2c1u2e1w2e1r2c1u2e1s2c1t2e1u3e1r2c1w2f1t2c1t1g1x2e1q2e1r2e1t2c102e1u2e1p2c1v3g1m2c1u3g1s2e1s2e1y2e1r1c142e1u2f1i2c1v2e1g2c1u2g1s2e1q2e1w2e1t2e1p2e1v3e1p2c1m2e1u2c1w2e1u1e1o2c1w3e1f2c1t2g102e1s1c1u2e1s2c1k2e1w3g1q2c1u3e1s2c1r2e1y2e1q2c1t2e1u3c1v2e1w2e1v2c1u2g1l2c1u2e1q2e1s2c1u2e1s2e1t2e1v2g1d2c1w2f1k2c1t3e122e1q2c1y2e1s1e152e1w2f1r2c1u2e1d2c1u2f1k2e1s2c1u2e1s2e1z2e1u3e1o2c1v2f1t2c1u2f1u2e1s1d122e1u2e1o2e1u2g1c2c1v2e1u2c1s3e1z2e1q2c1h2e1s2e152e1t3e1y2c1v2g1v2c1s2g1q2e1q1c1z2e1t1c1v2e1u3e1h2c1u1e1f2c1u2e1u2e1r2d172e1s3c1o2e1u3e1g2c1u2e1m2c1s1e1u2e1q1e122e1u2e1o2e1v2g1i2c1w2g1y2c1s2g1s2e1s2c1l2e1t2e1w2e1u2f1o2c1u3e1l2c1u1e1y2e1q2d182e1s2e142e1w1f132c1w2e1z2c1u1f1t2e1s2c1t2e1u3c1w2e1v2e1r2c1v2e1t2c1t2e1e2e1s1e1t2e1u3e1r2e1u3e1d2c1v1f1j2c1u1g1y2e1s2e1e2e1s2d1x2e1v3e1h2c1w1g102c1t2e1w2e1s2e1q2e1s3c1j2e1w2g1k2c1w3e1u2c1u1g1v2e1q2e1j2e1u2c1b2e1u3g1v2c1v2g1s2c1u1e122e1s2c1y2e1u2c1o2e1u2e1b2c1v3e1j2c1t2g1q2e1r1e1z2e1u2e1r2e1w3g1y2c1u1f1q2c1u2g1y2e1q2c162e1s2c1h2e1v2f1w2c1v1g1s2c1t2e1k2e1s1c122e1u3c1v2e1v2f132c1w2e1v2c1u3g1u2e1p2e172e1t2e1s2e1t3g1h2c1w2g1q2c1s2g1w2e1q1c1q2e1u2e102e1v3e1s2c1v2f1i2c1s2g162e1r3c1l2e1t3c1y2e1v2f1r2c1v3e1z2c1s2f102e1s2d1j2e1r2c1w2e1u2g1d2c1u2f1x2c1s2e1u2e1s2e1v2e1s2e142e1w2e1r2c1w2g1y2c1t2g1z2e1s3c1y2e1s2c1r2e1v2g1r2c1u3f1v2c1u2e1l2e1r2e1j2e1u2e152e1v2f1s2c1v2g1j2c1r2g1y2e1r3e1q2e1t1e1s2e1v2g1c2c1w1e1t2c1u1f1l2e1r2e1h2e1t2c1o2e1v2e1w2c1w2f1y2c1s2g1t2e1s2c1x2e1u2e1z2e1v3e1w2c1u2e1f2c1s1e112e1r2c122e1s2e1p2e1w3e132c1v2g1s2c1t3e1r2e1s2c122e1u2e1v2e1w2e1h2c1v3e1t2c1u2e102e1s2c162e1s1c1v2e1v2g1o2c1u3e182c1t1e122e1s2c1u2e1s3c1e2e1u2e1f2c1u1e1e2c1t2g1k2e1s1e162e1u1c1z2e1v2e1d2c1w3e1f2c1u2g1k2e1s1e1j2e1t1e1h2e1w1g1u2c1w1e1q2c1u1g1q2e1r2e1c2e1t2e102e1w2g1q2c1v2g1v2c1t1e102e1r2c1x2e1u2c152e1v2g1v2c1u2g1y2c1r2e102e1p2c1u2e1t2c1o2e1u1g1k2c1v2e1x2c1s1g1u2e1s2c1x2e1u3c1s2e1w2g1v2c1u3e1s2c1r2e1u2e1r2c1q2e1s1c1z2e1w2g1p2c1u2e1t2c1t3f1k2e1s1e122e1t1e1z2e1t2g1p2c1v1g1r2c1u1g1u2e1q1d112e1r2e1j2e1v1e1w2c1u1g1e2c1s2g1t2e1q2e1t2e1t2c1k2e1v1g1v2c1u2g1x2c1s2g1x2e1r2e1r2e1t2c102e1v1f1i2c1w2e1y2c1s1g1j2e1s2e102e1u1e1t2e1u2g142c1v2e1q2c1t2e1q2e1s1e1w2e1t2c142e1v2g1r2c1v1e1t2c1t1g182e1s2e122e1t2e1o2e1w1e1r2c1u3e1x2c1u1g1e2e1s1e112e1u2e1o2e1u2g182c1w2e1d2c1u3e1w2e1r2e112e1t2e102e1w2f1o2c1v2f1r2c1r1g1v2e1s1e1j2e1s3d1o2e1w3g1v2c1u2e1m2c1t2e1u2e1s1c122e1t2e1b2e1w1g1a2c1w2g1q2c1t2e182e1r2e102e1s3c162e1u1e1p2c1v3e1w2c1u2e102e1r2c1j2e1s2c152e1w3g1s2c1w2e1t2c1t2e1h2e1s2c1c2e1s2c1p2e1t2g1j2c1v2f1w2c1s3e1v2e1p2c102e1u2e1h2e1v1f1q2c1v3f1f2c1s1g1h2e1s2c1z2e1t2c1s2e1w2g1o2c1w2g1d2c1t3g1a2e1s2c1c2e1t2e1h2e1w2e1o2c1w3g1q2c1u2g1u2e1r2c1t2e1u2c1j2e1w3e1d2c1u2g1k2c1s1g1j2e1q1c112e1u2e1t2e1w1e1h2c1u2g1t2c1u3e1t2e1r2c102e1u2c102e1w2e1p2c1w3g1u2c1s2f1u2e1s2c1u2e1t1d1z2e1v2g1h2c1v2f1q2c1s2g1q2e1q2d192e1u3e1w2e1v2g1w2c1u2e1r2c1u1g1u2e1q2e1u2e1s2c1u2e1v2g182c1w2e1x2c1u2e1j2e1s2c122e1t2c1u2e1w3g1h2c1v2f1j2c1t3f1w2e1s2c162e1u3c1h2e1w2g1p2c1w1g1j2c1s2e182e1q3d112e1u2c1w2e1v2f1q2c1w2g1w2c1u2g1v2e1q1c182e1s2c1t2e1w3e1p2c1w2g1y2c1s2e112e1p2e1h2e1r3e1t2e1w1e1s2c1w3g1w2c1u2g1j2e1s2e122e1s2e1p2e1t3g1t2c1w2e1x2c1u2g1w2e1s2e1w2e1u2c1o2e1v2e1h2c1w1e1y2c1u2f1q2e1r1c1z2e1t3c1h2e1w1g1h2c1w3e1d2c1u2g1y2e1q1e1z2e1u3c1x2e1v3e1y2c1w3e102c1u2e112e1s2d172e1t3c1s2e1v2g1p2c1u3f1v2c1u1g1z2e1s2c1q2e1u1e1t2e1v2e1o2c1u1g1j2c1u2g1i2e1s1c1w2e1s2c1o2e1w2e1e2c1v2f1a2c1u2g1u2e1r2c1u2e1t2c152e1w2g1q2c1v2g1t2c1t2g1t2e1r2e1s2e1u2e1w2e1v2e1d2c1w2g1r2c1u1g1j2e1q1c1w2e1s2c1u2e1w3e1t2c1v3e1y2c1t2f1q2e1q2e1x2e1u3e1w2e1u2f1f2c1u2e1m2c1u2e1u2e1q2c1s2e1s1e1q2e1v2e1h2c1u2g1y2c1t1e122e1s2e112e1s1e1u2e1w2e1h2c1v2g142c1t3e1u2e1r3c1v2e1u2e1h2e1u2e1q2c1u3g1w2c1t2g1t2e1q1e1y2e1t1c1u2e1w3e1f2c1u2e1i2c1u2e182e1r2c191e102c162e1b3f171c142e2f1e1e1g3g1w1e1j1f1b1e1h1d191f1h1d1d1e1j1e1s1e1l3e1u3d1e2e1s1e1g2c1s3e112c1u1e1v2e1s1d1r2e1v1c1g2e1s1f1v2c1t2e1r2c1u1g1v2e1r2c152e1w2c1y2e1s3e1c2c1u2e1t2c1s1f162e1q2c1u2e1u2e1k2e1t2e1x2c1u2g102c1t2e1y2e1q3d1k2e1u2c182e1s3e1p2c1u2e1s2c1t1e1g2e1s2c142e1w2c1z2e1s2e192c1u2g1g2c1t3g1j2e1q2d182e1u3c1c2e1s3f172c1s3g1d2c1s3f182e1r3c192e1u3d172e1s3e1f2c1s2f1a2c1u3e1d2e1q1d192e1u3c1h2e1s3f162c1u3f1b2c1s3f192e1q3c1z2e1u2d192e1s3f1c2c1s1f1b2c1s3g1c2e1q1d172e1v3e1b2e1s2f162c1s3f1a2c1s2f172e1r3c1j2e1u2d182e1s3f172c1s3f192c1s3f1t2e1q2c1u2e1h1c1f3d143g1d2d182g1e2e1c1e1i3g1k3e1y2g1e2c1c1g1c3g1f1c1b2f1m1d183f1d3e181e1g3g161d1h3g121g1u2d1j3f1a3c121d1f1f1c3e1m1e1d3c1d3g1j3f111e1l1e1k1d1h3f1g2e161c1f2f181e1s1f1j3e161c181e1a1c181e1s3g1h1c1a1e1c1e123d1f3g1a1c1i2f1e3d1f3e121g123e1d3e1e3d1e3g1j1g1d2c192f161d1c1e1f3e1d2d1i3f1c1e1g1f1f3g1i1e1h2e1u3d1j3g152f1c3e142f1g2d1c1e1f2f1s2c1u2e1v2c1u3e1z2e1p2e1k2e1v1e102e1t1e1t2c1t3g1w2c1t2e1s2e1s3c1t2e1t2c1s2e1t2g1w2c1t1g102c1s1e1w2e1s2e172e1w2c102e1u1e1q2c1t2g1l2c1u2g1z2e1q2d1r2e1u2c1x2e1t2e1f2c1t2e102c1u3g1w2e1s2c102e1w2e1u2e1u1e1q2c1s1e1e2c1t2e1m2e1s2e1u2e1v1e1u2e1t2e1y2c1u2e102c1s3e1r2e1q2c1x2e1u1c1q2e1r2g1u2c1u3f1r2c1u2e1l2e1q1c1s2e1v2e152e1s2e1i2c1s1g1w2c1u1f1w2e1s2e1z2e1v2c1j2e1u3f132c1t2g1x2c1s2g152e1r1e1v2e1u1e152e1u2e1y2c1t2e1m2c1s1g1y2e1r1c1w2e1v2e1t2e1s2g1p2c1u2e1v2c1s1g162e1q3e1r2e1u2c162e1t2e1j2c1s3f1y2c1s2f102e1s1e1v2e1v1e102e1t2g1u2c1s2e1j2c1s2e1h2e1r1d1l2e1u1c1w2e1u2e1a2c1s2e1x2c1t2e1l2e1s2e1c2e1w1e102e1t3f1u2c1s2f1j2c1s2f1y2e1s1d1l2e1v2e1c2e1t2f122c1t2g122c1t2e1z2e1q2c1v2e1v1c1w2e1u1g1x2c1s2g1v2c1r1e1l2e1r2d102e1v2e102e1t3e1w2c1u2e102c1t2e1s2e1r2c1k2e1w2c1h2e1u2g1y2c1t2e1t2c1u3g102e1s2c1w2e1v1d1w2e1u1e1u2c1t3g1j2c1t2g1h2e1r2e1h2e1v1e1z2e1t3g1a2c1u2e1s2c1s1g1u2e1r1e1u2e1w1c1r2e1t3f1g2c1t3e1r2c1t2e1y2e1s2e1g2e1v1c1i2e1s2g1x2c1t1e1e2c1s1g1l2e1r2c1f2e1w2e1o2e1s1g1f2c1u1g1h2c1s3g1s2e1r2e1x2e1v1c142e1u2f1p2c1s2g182c1t2f1v2e1q3c1f2e1w2c102e1s2e1x2c1u2g102c1s1e1w2e1r2d1k2e1u3c1y2e1r1g1f2c1t2g1m2c1t2e1s2e1q1e1s2e1v2d1r2e1u1g1y2c1u3f1m2c1r1g1s2e1r1c1r2e1w2c1o2e1t1g1j2c1s2e1h2c1u2g1y2e1s2e1z2e1w2e1h2e1u1e1k2c1s2g1h2c1u2e1s2e1r2e1v2e1u2c1b2e1t3g162c1u2e1l2c1t2g1h2e1q1c1h2e1u1c1t2e1s3e1t2c1s2g1v2c1s2e1h2e1s3c1l2e1v1d1s2e1t2g1s2c1u3e1c2c1t2e1h2e1q2e1u2e1v2c1c2e1u3g1y2c1u1e1k2c1t2e1v2e1p2c1k2e1u1e1w2e1t2e1t2c1t3e1x2c1t1f1x2e1s2c1h2e1u2e1w2e1u2e1p2c1u2g1v2c1u2e102e1q2e142e1u2e1w2e1u2f1i2c1r1g1z2c1u2g1u2e1q1c1v2e1v2e1k2e1u2e1d2c1u2e102c1t2g1f2e1q2c1m2e1t2c1p2e1u3e1p2c1r2g1s2c1s1g1h2e1p2e1t2e1v1e1t2e1u2g1q2c1s1e182c1t2e1s2e1q3c172e1w3c102e1u2e1s2c1t2g112c1s1g1h2e1r1e1t2e1w2e1s2e1s1e162c1s2g1v2c1u3e1z2e1q2e1s2e1u2e1w2e1s2e1j2c1u3f1t2c1u3g1h2e1s2e1u2e1w2c1z2e1t3e1p2c1u2g1v2c1t2g1g2e1q1e1i2e1v3c1w2e1u2g1h2c1s2e1s2c1u2f142e1s2d142e1u2e1h2e1u2f1p2c1s2g1v2c1u2f1c2e1q1e1i2e1u2e1v2e1s2e122c1t1e1i2c1u1g1h2e1s1e1h2e1w3c1v2e1t1e1f2c1u2e1r2c1s1e1h2e1q1e1l2e1w1e1y2e1t1e1j2c1u2e1z2c1s1e142e1s2e102e1v2c1t2e1u2e1y2c1u3g1w2c1t3g1t2e1s1d1u2e1v2c1s2e1s2g1p2c1u1g172c1u2g1s2e1q2c1r2e1v1e1z2e1t1e132c1t3e1u2c1t2g102e1q2e1e2e1v2c162e1u3f1j2c1t1f1x2c1t2e1s2e1s2c1e2e1v2d1d2e1t1f1u2c1t2e1j2c1s1f1m2e1p2e1t2e1u1c1p2e1s2e1v2c1u2g112c1r1g102e1s2d1s2e1w3c1c2e1u3e1v2c1u2e1r2c1t1e1m2e1r2c152e1v2e1t2e1t2f1x2c1t1e1l2c1s3e1l2e1r2c152e1w1c102e1u2g1q2c1u2f1v2c1u3g172e1s3e1l2e1w3c1a2e1u1g1q2c1u2e172c1u2e1z2e1s2e102e1v2e1r2e1s2g1x2c1u3g102c1t2f152e1s2c102e1u1c102e1s1e1w2c1s3e1z2c1t2g1h2e1q2c1y2e1u3c1t2e1t2g1x2c1t3e1y2c1t2e1y2e1s3e142e1w2d142e1u2f1j2c1s3g1r2c1t2g1s2e1s2e1w2e1v2c1w2e1s3e1w2c1u3g1d2c1t1f182e1r2d162e1w3e1i2e1t1e122c1t3e1v2c1s1g142e1q1c1s2e1w1c1u2e1u2e1h2c1s2g1z2c1u2e152e1q2d1l2e1u2e1s2e1s2f1s2c1s3e1z2c1u1e102e1r2c152e1v3e162e1t2f1r2c1s1e1h2c1u1g102e1r2c1t2e1t1c1i2e1t2e1g2c1s2e102c1s2g1z2e1s3e1x2e1w2e1t2e1u3f1r2c1u2e1y2c1t1f1z2e1p2d1v2e1v2c1z2e1u1g132c1t2g1r2c1u1e142e1q2c1z2e1v2e1v2e1u2g1q2c1u1g1h2c1u2e1z2e1s1e142e1w2e1j2e1u2g1k2c1u3e1u2c1u2g152e1s2e1z2e1t1c1f2e1s1f1y2c1s2e1r2c1t2f1s2e1r2c102e1w2c102e1u1g1r2c1u3e1m2c1s2g1w2e1s2e102e1w2e1u2e1u2e1q2c1u2f1m2c1u3g1x2e1r2e162e1u1d1z2e1t2e1v2c1u2e1y2c1r1e1s2e1q2d1y2e1w2e1k2e1u2g1p2c1u2e1y2c1u1g1l2e1r2c1s2e1w2c1o2e1t2g1t2c1u2g1k2c1u1g1z2e1r2e142e1w2e152e1s2e132c1s1e102c1u2g142e1q1c1s2e1w2c102e1s3e1r2c1s3f1v2c1t2e1w2e1r2c142e1v2c1f2e1t2g1v2c1t1g1j2c1u2g1f2e1r1e1q2e1v2e1s2e1u1f1v2c1u2f102c1t2e1h2e1q3c1r2e1w2c1r2e1u1g1x2c1u1e1a2c1u1e1e2e1s1e1m2e1w1e1r2e1t2g1j2c1u1g1v2c1u2g1v2e1s2c1y2e1w2e1o2e1s1f163c182e1u2d1k2e1r2g1t2c1u2e1j2c1u2f1t2e1q2c1l2e1u2c1x2e1u1g1u2c1s2g172c1u1e1t2e1s2e1v2e1w2e1s2e1s1e1h2c1u1g1u2c1s3e1t2e1s1e1s2e1v2c1h2e1t1e1r2c1u2f1t2c1u2g1j2e1q2c1t2e1w1c1y2e1s2e1b2c1u1e1y2c1t2e182e1r3e1f2e1w1c1x2e1s1g1i2c1u2e1v2c1t1e102e1s3d1x2e1u2c1t2e1t2g1y2c1u2e1y2c1s1g1m2e1q2e1x2e1u2c1x2e1u2e1w2c1u1e162c1t2e1d2e1r1e1t2e1u1e1u2e1t2e1q2c1s2g172c1u2g1v2e1s2c1i2e1w2c1v2e1u2g1t2c1s2e1z2c1r1e1t2e1q1c1q2e1w1c1j2e1s2e1r2c1s2e102c1u2e1w2e1s3c1f2e1u3c1h2e1t3e1r2c1s2g182c1u2e1r2e1q2e162e1v3e182e1u1e1t2c1s2e1t2c1s1e1f2e1s3e102e1v2c1z2e1s2g1r2c1u2f1g2c1s2e1y2e1r1e102e1v2d102e1s2e122c1u2e102c1u1g1j2e1s2e1q2e1w1d1e2e1u1f142c1u2f1j2c1t1e1m2e1r3c1t2e1w3c1x2e1s2e1y2c1t2e112c1u2f1g2e1s3e1y2e1w2e1h2e1s2e1f2c1u2g1t2c1u3e1u2e1s2e1r2e1u2e1f2e1u1e172c1s2g172c1u1g1y2e1r2e152e1u2c1f2e1t2g1w2c1u1f1q2c1t2e162e1q2c1j2e1v2e102e1t2g1o2c1u2e1j2c1u2g1t2e1r1e1q2e1v2d1f2e1t2e1k2c1t2f1u2c1s2g1j2e1r1e1y2e1v2c1y2e1u1e1a2c1u2g1v2c1s1g1s2e1s2e1u2e1u1e1j2e1s2e1d2c1u2g1u2c1t1f1f2e1q2c1f2e1u2e172e1t2g1r2c1u2e1j2c1s1e1m2e1s2e1i2e1u2d1u2e1t2e1h2c1t2e1m2c1s2e1m2e1s2d1t2e1w1c1y2e1u1g1c2c1s1e122c1t2g1y2e1q2c1t2e1w2d1q2e1u1g1w2c1u2e122c1s2g1g2e1r3c1t2e1u2e1b2e1u1g1u2c1s2g1v2c1s1e1s2e1r1c1u2e1v2e1t2e1u2g1i2c1t3g1q2c1s2g1c2e1r2e1s2e1w2c1t2e1s1f1s2c1s2f172c1u2e1f2e1q3e1m2e1w2c1t2e1u2e1d2c1s2f182c1s1e1x2e1s1c1t2e1u1c1p2e1u2g1r2c1u1g122c1s2e1r2e1s2e1t2e1v1c1t2e1u1g1v2c1u2e1w2c1s1e182e1q2e1j2e1w2e1t2e1t2e1w2c1u1e112c1s2e102e1s3e1h2e1u2e1j2e1u2f1r2c1s2e1w2c1t3e1u2e1s2e1t2e1u1e162e1u2e1k2c1u1e1m2c1t3e1u2e1r2e1h2e1u2e1w2e1t1e1h2c1t1e1j2c1t1g1d2e1q3e1j2e1w2e1y2e1s2e1h2c1u2e1u2c1s2e1f2e1s3c1f2e1w2e1r2e1t2e1r2c1u1e1j2c1u1e1f2e1q2e1x2e1v3c102e1u2g1w2c1t3e172c1t2e1h2e1q2e1e2e1v2c1r2e1t2g1h2c1u1e1j2c1s2g1x2e1r1c1m2e1w1e1t2e1u2g1c2c1s1g1k2c1t3e1u2e1s3c1q2e1u2e1t2e1t2g1r2c1t2g1j2c1t1g1i2e1q3e1u2e1u1c1x2e1u2g1q2c1s3f1e2c1u1e1i2e1q2e1j2e1v2c102e1t1e1d2c1t1g102c1s2g1g2e1r1e1f2e1u2c1g2e1u1e1r2c1s2g1c2c1u2e1g2e1s2e1t2e1w3d1a2e1s1e1t2c1u2e1q2c1t2g1q2e1s3c1j2e1w2e1u2e1u2g1d2c1u2g102c1s2e1t2e1q2e1w2e1v3e1f2e1s3g1d2c1s1e1r2c1u2e1t2e1r2e1v2e1u2c1t2e1t2e1b2c1u2g1t2c1u1e1j2e1s3c1v2e1w1e1t2e1u1e1i2c1u2g122c1u2g1y2e1q3c1u2e1v3d152e1t2g1v2c1s2e1v2c1t1e1u2e1r2c1g2e1u3c1x2e1r2g122c1u3f1q2c1t2e1v2e1r2c1f2e1v3e1v2e1t3e1s2c1u3e172c1u2g1v2e1r2e1j2e1w2c102e1u2g1y2c1u2g1v2c1u2e1q2e1s3c1x2e1u2e1y2e1u2g1d2c1s2g1u2c1s3e1f2e1s2c1y2e1v2e1s2e1u1e1f2c1s2g1m2c1u1e1x2e1r3c102e1w1e1k2e1u1g1r2c1t1e122c1t2g102e1r2c1f2e1t1c1x2e1t2e1u2c1t2g1q2c1s2e1x2e1r2e1q2e1w1e102e1u3g1d2c1u2e1j2c1u2f142e1q3e1t2e1u2e1p2e1t2e1o2c1u3g112c1t1f1m2e1r2c1t2e1u2d1j2e1s2f1h2c1t3g1v2c1u2g1h2e1r1c1s2e1w2c152e1s1e1u2c1u1g1s2c1t2e1j2e1q3d1j2e1v2e1r2e1t2g1k2c1u2e1r2c1s2f1r2e1r2e102e1u1c1t2e1t1g1t2c1t2g1m2c1t2e102e1s2e182e1v2c1j2e1u2e1r2c1t3e1w2c1u2e1j2e1s2e102e1v1c1c2e1t2e1r2c1t2e1u2c1t2f1r2e1s3c102e1v2c1r2e1s2g1w2c1s2g1x2c1u3g1y2e1q2c1u2e1w2e1f2e1s2g1q2c1u2e1q2c1s2g1i2e1r2e1i2e1w2c1h2e1u2g1p2c1t2g122c1s2g1s2e1r3e1m2e1t1c142e1u1g1t2c1u2e1v2c1s2g1q2e1s2c102e1w2e1u2e1s1g1s2c1s2g1z2c1u2e1r2e1r1c1u2e1u2c1v2e1u3e1w2c1t2g1s2c1t2g1u2e1r2e1y2e1u2c1i2e1u1g1j2c1s2g122c1t1g1r2e1r2d1k2e1v2c1k2e1s2g1p2c1t2g122c1t2e1t2e1r2c1t2e1v2c1q2e1t2g1v2c1u3g1i2c1r2g1x2e1r2e1t2e1u1e1g2e1u2g1r2c1t2e1r2c1t2g1r2e1s1e1d2e1w1e1q2e1s2e1t2c1r2e122c1s1g1f2e1s2c1w2e1v2d1c2e1s2g1u2c1s2g1v2c1u1f182e1p2e1s2e1u1e1v2e1u2g1f2c1t2e1j2c1t2e1s2e1s2c1l2e1v1e1t2e1t2e1h2c1s2g1s2c1t2e1t2e1s2d1s2e1v2e182e1u2g1o2c1t2g112c1u2e1t2e1r3d1t2e1u1c1u2e1u1g1k2c1t2e1v2c1t2e1y2e1s2e1r2e1w1d1u2e1s1f1o2c1u2g1i2c1u3g1g2e1s2e1d2e1w2c1q2e1u1e1k2c1t2g1y2c1u2e1a2e1q2c1t2e122c1t2e1w2e1q2c1m2e1u2c1t2e1t2f1x2c1u2e1j2c1u1g1s2e1r3d1s2e1v2c1v2e1t2e1h2c1t2g1j2c1u2g1v2e1r1c1g2e1u2e1u2e1u2e1q2c1t2e1j2c1s2e1u2e1q3e1x2e1u2c1x2e1u2e1y2c1u1g1w2c1t3f1m2e1r2d1d2e1w3c162e1t2g1q2c1u1e1u2c1u2g162e1s3c1w2e1t3c1t2e1t3e1y2c1u2g172c1u1e1w2e1r2e1r2e1v2e1f2e1u2f1d2c1u2e1w2c1t2e172e1q2c1t2e1u1c1j2e1u2g1j2c1u2g1u2c1u2e1h2e1s2c1t2e1u2c1t2e1t3e1t2c1u2e1t2c1s2g1s2e1s2c1v2e1w2d102e1u2f1t2c1u2e1c2c1t1g1y2e1s1c1w2e1v1e1h2e1s2e1k2c1s2e1l2c1s3e152e1r2e1t2e1v2d1t2e1s3g1x2c1s2f1w2c1u3g1l2e1q2c1m2e1u3c1v2e1u2g1f2c1s2g1u2c1s2g1a2e1r2c102e1v2e1q2e1u1e1e2c1s1g1y2c1s2g1a2e1s3e1k2e1v1d1w2e1s2e1u2c1u3e1u2c1t2e1t2e1r1d1i2e1v2e1e2e1s2e1q2c1u2e1r2c1r2g1x2e1r2c1y2e1w1c1f2e1s1e152c1u2e1j2c1u1g162e1q1c1q2e1w2c1y2e1s2e1y2c1u2e172c1t2f1h2e1s3c1d2e1w2e1h2e1s1e1f2c1u1g172c1s1g1w2e1s3c1t2e1v1e1b2e1t2g1q2c1u2e1x2c1u3e1z2e1r2d1t2e1u2c1t2e1u2g1t2c1t2e1h2c1t3g1g2e1r3d1u2e1w1e1w2e1u1g1s2c1t1e1t2c1u2g102e1q1e1j2e1v1c1t2e1u2g1k2c1t1g1c2c1s2g1l2e1q3c1g2e1u1c1s2e1t2g1j2c1t2g112c1s3g1a2e1r2c102e1u3c1t2e1s3g1y2c1s2f1u2c1s1g1y2e1r3c1s2e1v2e1p2e1t2e1s2c1s1e1t2c1u2g1l2e1r2e1y2e1u2c1f2e1t2g1w2c1t2e1l2c1r1e1q2e1s3d1x2e1u2c1t2e1t1e1q2c1s1g1u2c1s3f1y2e1r1e1w2e1v2c1h2e1s1e1j2c1s1e1w2c1t1g1h2e1s2e1g2e1w3c1j2e1t1e1q2c1u2g1r2c1u2g1w2e1r3d1u2e1w1e1p2e1u2g1f2c1s1e1u2c1t2g1v2e1q2e1j2e1v2c1j2e1u2e1f2c1u1g1j2c1s2e1h2e1q1c1v2e1w2d1t2e1s2e1y2c1u1g1u2c1u2e1z2e1s2e1h2e1v2e1z2e1t2e1y2c1u2e1x2c1u2e102e1s2c1m2e1t2e1t2e1t2g1x2c1u2g1w2c1t2e1v2e1s2e1m2e1v2e1a2e1u1g1x2c1t2g1v2c1r2g1r2e1q2c1z2e1w2e1a2e1u1e1i2c1s2g1q2c1s1g1t2e1s2c1s2e1w2c1j2e1t1e1w2c1u1e122c1s1e102e1r2e1s2e1v2e1t2e1u2g1o2c1u2g1u2c1u1e1i2e1r1c1e2e1w2e1r2e1u2g1r2c1s2e1i2c1s2g1h2e1r2c142e1u2e1t2e1t2e1u2c1u2g112c1t1e1i2e1s3d1r2e1w2e1r2e1s2e1e2c1s3g1y2c1s1e1z2e1s2e1s2e1u3d1a2e1u1e1q2c1s2g1v2c1t1e1z2e1q1c1x2e1t1c1x2e1s3f1k2c1t2e1u2c1u2e1t2e1q2c1e2e1w1c1u2e1t1e1y2c1u2g122c1r2g1t2e1r1e1r2e1w2e1q2e1s1e162c1t2e1u2c1s3e172e1r2c1s2e1w1c1z2e1u2e1w2c1r1e1t2c1u1g152e1r2c1f2e1w2e1t2e1s1f1t2c1u2e122c1t1g1v2e1r2e1m2e1v2e1f2e1u1e1w2c1u2g1j2c1u2g1h2e1s2c1j2e1w1d1x2e1t1f1t2c1s1e1y2c1t2e1z2e1r2d1a2e1u2e1q2e1t1e1j2c1s1e1y2c1u3g1t2e1r3c1j2e1t1e1z2e1u1g1q2c1u3g192c1r2e1y2e1p2e1j2e1v2e1j2e1t2e1c2c1t1g1l2c1t1e1d2e1r2d1u2e1v2c1g2e1r2e1c2c1t2f1z2c1u2e102e1r2d1f2e1w2c1z2e1s2g1r2c1s2e1j2c1s2e1y2e1s3e1j2e1v2c1p2e1t2e1p2c1t2g1l2c1u1g1l2e1s3e1w2e1v2e1u2e1u2g1i2c1u1f192c1u3e1a2e1q3e1s2e1v1c1f2e1t2e1j2c1s2g1x2c1u1e1w2e1r1c1q2e1u1c1c2e1s2e1w2c1t2g1g2c1t2g1z2e1r2e1z2e1w2d1j2e1s2g1p2c1t2g1u2c1u2g1w2e1r2e1h2e1w2e1f2e1t2e1j2c1s2e1z2c1u2e172e1q2d1j2e1v2e1f2e1t2e1w2c1t3g1w2c1t2g1r2e1s2e1y2e1u3d1r2e1s2e1w2c1s3e102c1s1g1j2e1r3e1z2e1v1d1h2e1u3g1y2c1u1g122c1u2f1z2e1r3c162e1v1c1u2e1u1f1x2c1u2e1x2c1t2g1s2e1s2c1q2e1u2e1t2e1s2e1t2c1u2g1t2c1s1e1l2e1s3e1f2e1w3c1y2e1s2g1q2c1s2g1j2c1s1g1f2e1s2d1f2e1w2e1x2e1s3g1y2c1t2e1u2c1s3e1s2e1q2e1f2e1v2e1w2e1u2e1e2c1u3e1e2c1t2g1g2e1s2c1u2e1v2d1w2e1u1g1q2c1u1g162c1u2g1a2e1s1c182e1v1e1j2e1u2e1u2c1s1e1l2c1u1f102e1s2c1j2e1w2d1r2e1s1f1q2c1u2e1v2c1s2g1t2e1s2c1h2e1v3e152e1u2g1r2c1t2e1w2c1r2g1m2e1p2e1k2e1u1e1t2e1u1g1q2c1u2g1q2c1s2g1m2e1q2e1s2e1w2c182e1u3e1v2c1s2e1y2c1t1e1y2e1s3c1a2e1u1c1p2e1r2e132c1s2e1s2c1t2e1w2e1r1c1r2e1w2e1q2e1u2e132c1s3g1u2c1s2f1a2e1s3c1a2e1u1c1u2e1s2e1p2c1t2g1u2c1r2e1s2e1q2c1l2e1w1e1j2e1u1e1v2c1u1e122c1s2e1i2e1r2e1z2e1w1e1y2e1u2e1w2c1t2e1c2c1s2g1x2e1s2c1w2e1u3e1f2e1t2g1j2c1u2e182c1s3e1j2e1s2e1f2e1w2c1x2e1t2g1x2c1s1f102c1u2e1u2e1s2e1x2e1v2c1j2e1s1g1t2c1s1e172c1u2g102e1s2c142e1v2e1j2e1t2e1x2c1u2e1h2c1t2e1t2e1q2c1s2e1w1c162e1s2g1g2c1s2g102c1s2e1k2e1r3d102e1u2d1g2e1t2f1v1c172e1a2c1t3e1f341c2k2g1l1s2j1s1v1v2u1t141','0ac16m3o1t3q221a271s393v2z1b3o0z101m252z3o193v2c1i193v1z1i1a2z173s3w1z3z141z133v392o1720241s3s2t202n1z3u242c133v392o1720341z2z1m233c1g2c29361w2v3s1z101m260w1z1029213v2z29361w2v3s1z101m2c162t2z2n1z2038231q25332c142z2v232c162s271z1z38231q25333c142z261w1a2s271w2s27162s271s3s271o2c1z3u261z1z3u261z3u243s3m3o0z1z2z393w121m252c2o1z1x21121z101m253c2o2m35203o1z2z2z29213v2026143o0z1c1c2t2c292o122s1z101d2z1o1z2z3823353u253u253r1336211z1z38371z2z141h1z1c1m2c162t2z2p2c29213v2z2o1g27312c293w121m121e2c1d2d1c1c1h1c122e1k1c1a2e1k1c1a3e181e151e1i1c1i1d1f2c1s1d1r2c1r2e1r2c1s2c1w2c1s2e1c2c1s1c1z2c1s3c1r2c1s2c122c1s2e1p2c1u1c1i2c1s3c1h2c1u2d1z2c1q3c1x2c1t1d1u2c1s1d1s2c1q2c1u2c1t3e1v2c1s2c1t2c1u2e192c1u1d1w2c1r2e1q2c1s2d1y2c1r2e1j2c1t1c1u2c1t2c1q2c1q2c1y2c1s3c192c1s2e1y2c1s3c172c1t3e1r2c1q2d172c1s3d1x2c1q3d152c1s3d1b2c1s2d172c1q3d1a2c1s1d192c1r3e142c1s3d182c1s3d1t2c1q2d172c1t3e1c2c1q3d162c1s3d142c1s3d172c1s3d1a2c1s3d182c1q3d1f2c1s1d192c1s3d1b2c1q3d172c1s3d1t2c1q2d172c1s3d162c1s3d152c1r3c1i2c1s2d172c1q3d172c1s3d172c1u2c1s2c1q2c1e1c1f1c1p1e1a1c1i2d1d3c1b2c141c101d123d1s3d1c1e1u1d1u2d1h2d181d121b1c3e1c3d1k1c1b3c1c3d1j3e111d1j1c1i1d1h3d1g2c161c1d2d161e1s1e1j3c1d1c1e3e141d1h3e193e1d3d1q1e1p3c1c1c1c3d1d3d1d3d1c3d1c3d1c1d192d1c3d1e3d1b1e1s3c1d1c121e1s2e1f3e1r3b1d3d1d1c1c1c181c1c2e192c1a1e1b3d1g2c1c2c1d1e1i1c1d3c1g1d1g2c1h1d1r2c1s1d1j3c1d3e161c1b3e1i1d1f1c1g2c1s2c1y2c1u2e102c1t2e1i2c1r1e142c1u1e1z2c1s3e1w2c1u2e142c1r1c1t2c1q2e1s2c1s1e1s2c1s2c1b2c1u2e1u2c1t1e1s2c1r2c102c1u2c102c1q2e1y2c1u2c1w2c1t2c1q2c1s2e172c1s2c1z2c1r2e1v2c1t2c1w2c1u1c1v2c1r2e142c1u2c1r2c1q2e1o2c1t2e1y2c1t2c1u2c1r2e1f2c1t2c1s2c1q3c1w2c1s2e182c1s1c1i2c1q2c1o2c1t2c1x2c1r3c1i2c1u2e1p2c1u3c1t2c1q3c1r2c1s2e1v2c1r2c122c1t3e102c1t2e132c1r2e1q2c1u1e1v2c1p2e1y2c1s2e1u2c1s2e1y2c1r2d1f2c1t2e102c1r2c1u2c1t2e1o2c1s2c1x2c1p1c1h2c1t2c1y2c1s3d1h2c1s3d1f2c1s1e1t2c1s2c1i2c1u2e172c1q2e1f2c1s2c1c2c1t3e1y2c1s3e1s2c1t2d102c1s2e1w2c1u2c102c1t3e162c1s2e102c1u3c1q2c1q2c1f2c1s2e1s2c1t2c1u2c1s2e1h2c1t3d1f2c1r3d1r2c1t2c1s2c1t2e1a2c1s1c1v2c1s1c1z2c1s2c1d2c1u2e102c1t1c1r2c1s3e102c1u2c1t2c1s3c1w2c1s2c1u2c1u2e122c1p2c102c1u3e182c1r2c1w2c1s1e1d2c1t2e1g2c1s3e1q2c1t2c1w2c1q2c1w2c1t3c102c1s2e1q2c1r1e1h2c1u2c1u2c1q2e1h2c1u2c1s2c1t2c1q2c1s2e1h2c1u2c1h2c1q2e1s2c1s2c1h2c1t2e1x2c1r3c1h2c1u2e1d2c1q1c1k2c1u2c1p2c1t1e1y2c1q2e1s2c1t2d1k2c1s2e1g2c1t3c102c1u3c1e2c1q2e1r2c1t2d1y2c1r2e1x2c1t2c102c1s1e1y2c1q3c152c1t3c1p2c1r2e1i2c1u3c1q2c1s1e182c1r1e1g2c1u2e1h2c1q2d1w2c1t2c1p2c1r1e1s2c1q1c1w2c1u1c1z2c1r2e1o2c1u2c152c1r3e1u2c1s2c1s2c1s1c152c1s3c1w2c1u2d1p2c1t1d1i2c1s1e142c1t1c1c2c1r2e1i2c1u1e1v2c1u2e1p2c1q2e1a2c1u1e1o2c1r2d1g2c1t2c1z2c1t2c1f2c1s3c1j2c1s3d1w2c1s3c1r2c1u1e1h2c1t1c1f2c1r2e102c1s2c1w2c1q3d1o2c1t2e1o2c1t3c1w2c1r2c1o2c1u1c1z2c1r3c1v2c1s2d1p2c1t2d1j2c1r1c142c1s1d1e2c1q3d1v2c1u3c1a2c1s2c1v2c1q2e1v2c1s1c1q2c1s3c1v2c1u2d102c1s3e1t2c1r2c1t2c1u2e102c1p2e1d2c1t2c1t2c1u2e1j2c1r2d1t2c1u2e1s2c1s2c1v2c1u2d102c1t3e162c1r3e1o2c1t1c1x2c1s2e1t2c1t2e1s2c1u1c1q2c1s2e1h2c1t3d1w2c1s3c1o2c1s2c1s2c1u1d1s2c1q2e162c1s2e1s2c1s2e1j2c1t2e192c1u1c1j2c1r2e1k2c1s1e1r2c1s2e1f2c1u2c1s2c1u2e1s2c1q2e1s2c1t2e1q2c1r2e1v2c1t1e1h2c1s2c1g2c1r1e1s2c1u2e1z2c1s2e1d2c1s1e1h2c1u1e1f2c1r2e1s2c1t3e1v2c1s1e1x2c1t2c1s2c1s3c152c1s2c1o2c1t1c1a2c1p2e1h2c1s2e1h2c1t1e1f2c1r2e1t2c1u2d1u2c1q1c1v2c1u2e1u2c1s1e1s2c1r3c1o2c1u2c1v2c1s2e1d2c1s3c102c1t1e1p2c1r2e1t2c1t2c1s2c1q2e1i2c1s2e1o2c1t2c1r2c1s1c1v2c1s3c1z2c1s2e1u2c1s2d162c1u2c1t2c1r2c1f2c1s1c1v2c1r2e1u2c1u2d1f2c1u2e1v2c1s2e142c1t1c1s2c1s3e1r2c1t2c1r2c1t1c1u2c1s2c152c1t2c152c1s2c1u2c1s2e162c1r2e1h2c1p1e102c1t1d102c1s1c1s2c1t1c1e2c1s1c1o2c1q1d1r2c1r2e1h2c1s2c1d2c1t2d1q2c1s1c1f2c1q3c1o2c1t2e102c1p1c1w2c1s1c1y2c1u2e1h2c1s2c1x2c1s1e1x2c1s2e1d2c1u3c152c1t2c162c1s1e1h2c1t2c182c1r2e1y2c1u2e1v2c1t2c1x2c1s1c1x2c1s2c1o2c1s2d122c1t2c102c1t2e1v2c1r2e1b2c1s2e1x2c1r1d162c1t2c1r2c1u2e1p2c1q2e1z2c1u3c1j2c1r1e142c1s2c1s2c1u1c1y2c1s3e102c1u1e102c1q3d1p2c1s2c1y2c1r3c1w2c1q2e1j2c1t3e142c1r2d1r2c1s1e1h2c1u2d142c1q3e1v2c1s3e1r2c1r1d1o2c1u3e1z2c1t1d1p2c1r2c1z2c1u2c1h2c1s2d122c1r2c1e2c1r2e1f2c1s1c102c1u2c1j2c1r2d1h2c1t2c1x2c1t2c1q2c1p2e1w2c1u3c1c2c1s2c1k2c1s1e1w2c1t2c1h2c1q2e1v2c1u2e1w2c1s3d1d2c1s3e1r2c1r2e1r2c1r2e1w2c1r3e152c1s1e1k2c1t1e1v2c1t1c1p2c1r1e1v2c1s2e1g2c1r3c1s2c1u1e152c1t2e1p2c1q2c1s2c1s2c1x2c1q2c1w2c1s2d1u2c1u3e1t2c1r2c152c1t2e1r2c1q2c1k2c1t2d1t2c1t2c1q2c1s3e1s2c1u2c1o2c1q2e1p2c1s2c152c1s2d1r2c1s1e1w2c1s2c1x2c1q1c1y2c1t2e152c1u1e1v2c1s2e1z2c1s2e1z2c1r2e1p2c1u2e1s2c1r2e1y2c1r2e1j2c1t2c1u2c1q2d1w2c1s1e102c1u2c1r2c1q1c1w2c1t2e1y2c1r3e1s2c1s1e1p2c1r1c1q2c1q2c1i2c1u2c1s2c1q2c1p2c1t2d1s2c1u2c1r2c1r2d102c1u3e1s2c1r1e1v2c1t2c1v2c1u2c1g2c1r2e152c1s2e1q2c1r2d162c1s2c1q2c1u1e1y2c1r2e1p2c1t2e102c1s1e1r2c1r2e1c2c1t2e1s2c1s2d1t2c1s1c1w2c1q3e1r2c1t2c152c1u3c1y2c1s2c1q2c1s1d1o2c1q2c1o2c1u2e1y2c1s2c1u2c1s2e1j2c1u3e1h2c1s2c1h2c1t2d1y2c1s2e1c2c1s2e102c1u1e1h2c1r2e1w2c1t2e1h2c1t3d1t2c1s2e1u2c1s3e1z2c1s3c1p2c1t2e1r2c1t2e1s2c1r1c162c1u1d171c142c1q2c1t2c1s1c1f2c1s2e1i2c1t3e1j2c1u2e1r2c1q2e1j2c1t1e1f2c1s1c1y2c1s2e1d2c1s2e1d2c1q2e1k2c1u2c1r2c1r1c132c1u3d1x2c1s2c1r2c1r2e1q2c1t2c102c1s3c1k2c1u1e1k2c1u3e1r2c1q2e102c1s2c1i2c1q3d132c1s2c1j2c1s2c1s2c1r2d1t2c1u2e1v2c1q1c1c2c1s2e1w2c1u2e1b2c1p2d1q2c1s3e1w2c1q2c122c1s1c1y2c1u2e1f2c1p1c1g2c1s1c1y2c1r3c1q2c1t2e102c1u1c1r2c1q2c1k2c1s2c1v2c1s3c1x2c1u2e1u2c1u2c1w2c1s2e1s2c1u2c1k2c1q2e1s2c1s2c1j2c1t1c1i2c1r2e1z2c1t2c1t2c1q2c1j2c1t2e1f2c1u2c1w2c1r2c142c1s2e1t2c1s2c1r2c1s3c1u2c1t3d1p2c1q2e1b2c1t2d1a2c1q1c1v2c1u2e1h2c1u2e1k2c1s3c162c1u1c1q2c1q2e1s2c1u1c1f2c1t2c142c1r2c1z2c1u2e1u2c1q2c1y2c1t2c1t2c1t2e1h2c1s2c1x2c1s3e1z2c1q2c1w2c1u2e162c1r3e1y2c1s1e1y2c1t2e152c1q2c1f2c1t2e1y2c1t1c1p2c1q1c1v2c1t2e1j2c1r1e1v2c1u2e1p2c1u3e1y2c1q1d1q2c1u3e1x2c1q1e1q2c1r1c1j2c1t2d1w2c1r2e1y2c1t3c1w2c1s2c1y2c1t2d1f2c1u3c1r2c1s2e1f2c1u1e1y2c1r1e1q2c1u2e1r2c1s2e1r2c1s2c1s2c1u3e1i2c1s2e1i2c1t2c1j2c1t2e1c2c1r2e1z2c1t2e1q2c1r3c1y2c1s2e1x2c1u2e1w2c1r1e1p2c1u2e1q2c1s2e1p2c1t2c1t2c1u2e1o2c1s3c1w2c1s2d1v2c1q2e142c1s1e1u2c1s1c1b2c1s2c1v2c1t2e1v2c1s1d122c1u2c1x2c1r3c1k2c1q1c1j2c1u2c1q2c1r2e1y2c1t2c1q2c1u2e122c1q2e1f2c1s1e152c1q2c1y2c1s2e162c1t3c1w2c1q3c1t2c1s2e1q2c1r2e1f2c1r1c1t2c1t1e1g2c1r1e1q2c1t1c1t2c1s2d1t2c1u1c1k2c1s1c1f2c1s2e1y2c1s2c1z2c1s2e1o2c1t2c1u2c1u2e1h2c1r2c1t2c1s2e102c1s2c1y2c1u2d1t2c1s2c1h2c1r2c1f2c1u1e1k2c1r2c122c1u1e1f2c1u2e1g2c1r2c1h2c1u3e1x2c1q1c1f2c1u3e1f2c1s2c1h2c1s2c1k2c1t2e102c1s2e1p2c1u2c1w2c1s1e1k2c1s2e1t2c1u1e1f2c1s1c1x2c1t2c1j2c1t2c1t2c1s2c142c1u2c1t2c1s1c1q2c1t2c1j2c1t1c162c1p2e1j2c1t2d102c1q2e1q2c1t1e162c1t2c1q2c1r2c1u2c1t2e1o2c1r2c1u2c1s3e1s2c1u2c1h2c1q1e1f2c1t2c102c1r1e1p2c1u2e1p2c1u3c1h2c1q1c1t2c1t1e1r2c1q2c1t2c1t3c1t2c1u2c1v2c1q2e1t2c1t2c102c1s2e1p2c1u2c1j2c1s1c1r2c1s1e1z2c1t2c1q2c1q3c152c1u2c1j2c1t2c1t2c1r2c1r2c1t2c1r2c1r2c1r2c1t2c1t2c1s1e1c2c1p1c1r2c1u2e1y2c1r3c132c1s2e1j2c1t2c1v2c1s2d1q2c1t2c1y2c1q2c1y2c1t1c1t2c1t2c1c2c1s2d1r2c1s2c1e2c1s1e1x2c1t1c1t2c1r2e1r2c1r2e1k2c1s2c1h2c1q2c1q2c1u2c1u2c1t1e1o2c1s2c1u2c1t1e1j2c1s2c1f2c1t2c142c1s2c1h2c1r3c1p2c1u2c1x2c1s2c1o2c1t2e1k2c1t2c1r2c1r1c1i2c1t2e1y2c1q3d1k2c1u1e1j2c1s2c1q2c1r2c1p2c1u2c1t2c1q1c1j2c1s2e1u2c1s2e1w2c1s3e1x2c1s2e1t2c1s2d1j2c1s2e1f2c1u2c1d2c1r3e1v2c1t1e1r2c1r1d1y2c1u1e1u2c1r1e1k2c1s3e1f2c1s2c1q2c1s3e1x2c1u3c1q2c1u1c1r2c1s3c1p2c1t2e1v2c1s3c1r2c1s2c1w2c1u2c1u2c1s2d1s2c1s2e162c1q3e1w2c1u3e1u2c1s3e132c1r2e1f2c1u2c1p2c1s2e1t2c1t2c1w2c1u2d1u2c1s2c1v2c1s1c1p2c1r2c1q2c1t1c1h2c1u2c1w2c1q1c1t2c1u2c1q2c1r2c1x2c1t2e1f2c1s2c1u2c1q2c1r2c1u2e1x2c1r2c1s2c1t1c1j2c1u2d1r2c1r2c1q2c1u2e1t2c1r2c1p2c1u2c1h2c1u3e1d2c1q1e1t2c1u2e102c1r2c1j2c1s2c1v2c1u3c132c1q2d1j2c1t2e1f2c1r2c1w2c1t3e1z2c1u2e1d2c1r2c1j2c1r2e1f2c1s3e1q2c1s1c1u2c1s2e1r2c1q2e1q2c1r2c1t2c1q2c1t2c1u2c1q2c1u2c1v2c1q2e1w2c1t2c1p2c1q3c1y2c1u2c1q2c1s2c1i2c1s2e1w2c1t2d102c1r3e122c1u1d1z2c1s2e1v2c1s2c1x2c1u1c1r2c1r2e1x2c1r2e1t2c1s2e1d2c1q2e1r2c1u1c1g2c1r3c1t2c1u2c102c1t2c1o2c1r2c1a2c1u2e1j2c1q2e1x2c1s2e142c1t3c182c1r2e1p2c1s1d1j2c1q2c1q2c1t1e1s2c1t2c1u2c1s2c1p2c1u2c1r2c1s1d1x2c1u2c1p2c1s2d1r2c1s3c1q2c1r2c1y2c1q2c1u2c1t2e1z2c1t2c1p2c1s2d1y2c1u2e1s2c1s1e122c1u3c1s2c1u1c1w2c1q1c1u2c1s2c102c1q2d1o2c1t2d1j2c1u3c1b2c1q2c1s2c1u2c1c2c1r2e1q2c1r3d1y2c1s3e1j2c1q2c1r2c1u2e1f2c1s2c1v2c1s1c1j2c1u3c1i2c1q2d1f2c1t1c1f2c1p2e122c1s2c1j2c1t2e1d2c1r1c1r2c1u1c1z2c1p2e1y2c1s1c1o2c1s2c1u2c1s2c1p2c1u2d1z2c1s1c162c1u2c1s2c1t2c1e2c1r1c1z2c1u2e1z2c1s2e1u2c1u1e1h2c1u2e1d2c1r2e1q2c1s2c1k2c1r2e1y2c1u1e1s2c1t2c1o2c1r2c1i2c1s1e1p2c1p2d1q2c1u2c1t2c1u1c1r2c1r2c1t2c1u2c1s2c1p2c1w2c1s1c1r2c1r3e1j2c1q2c1u2c1s2c102c1s2c1f2c1u3d1o2c1s3c1d3c1h2c1u2c1x2c1u3e1d2c1s3c1t2c1s1c1z2c1r1e1y2c1u2c1v2c1u2d1h2c1r2c1e2c1t2c1j2c1q2c1q2c1t3c1y2c1r3c1r2c1r3c1y2c1u2e152c1s1c1y2c1u2e172c1t2e1v2c1q2c1g2c1s1c102c1r3c1q2c1t2c1f2c1t1e1r2c1q2c1z2c1t2e1j2c1r2e1x2c1t2c1j2c1t2c1d2c1s2c1x2c1s2e1q2c1s2c1j2c1u2c1s2c1r2e1h2c1q1c102c1u2c1s2c1s2c1v2c1t2c1s2c1t2c132c1q1c1u2c1t2e1w2c1s2e1i2c1s2c1x2c1t2e1i2c1p2c1v2c1s2c102c1s1c1u2c1t3c1a2c1s1c1u2c1s2c1v2c1s1e1i2c1q1c1q2c1s3c152c1t2c1h2c1r2e1t2c1s2c1q2c1q1c1q2c1t2d102c1t2e1o2c1r2d102c1t2c142c1s2d1j2c1u1e1t2c1s3c1d2c1s3c1x2c1s1c1s2c1s2c1j2c1s3e1r2c1s2d1f2c1q2d1w2c1u1d1o2c1s2e1q2c1s3e1x2c1t2e1e2c1s1c102c1t2c1c2c1r2c1t2c1u2c1o2c1s2c162c1r1d1w2c1u2e1c2c1s2e1h2c1s1c1h2c1u1e1y2c1q2e1u2c1u3c1v2c1r1d1u2c1u2d1r2c1s2d1q2c1s2d1p2c1u2c1w2c1q2c1o2c1u2c1s2c1t2c1v2c1q1c1z2c1s2c1j2c1s2e1p2c1u3c1w2c1u1e1p2c1q2d1c2c1s2c1s2c1q1e1t2c1u2e102c1t2e1e2c1q2c1o2c1u1d1w2c1r2e1v2c1u2e1x2c1u1e1q2c1r2e1s2c1t2c1s2c1r3e1w2c1u2e1w2c1t2c1k2c1s3c1f2c1s2c1v2c1s1c1y2c1s2e1s2c1t3d1q2c1s3c1q2c1t2e1k2c1r3c1q2c1s2c1j2c1u2e1q2c1r2c1g2c1u1d1s2c1s2d1q2c1s2c1h2c1t2e1v2c1q2e1a2c1t1e142c1q2c1x2c1u1d1s2c1t3d1d2c1s3e1q2c1t1e1s2c1s1c122c1s3c1p2c1u1d1w2c1q2d1q2c1s3e152c1p3e1u2c1u2c1p2c1u1d1q2c1s2e1h2c1t1c1z2c1s2e1f2c1u2e1y2c1u1c1r2c1p2e1u2c1t1c1y2c1s2e1b2c1u1c172c1u2c1t2c1r2d1v2c1s2c1b2c1r2c1u2c1s3d152c1t3c1r2c1s2c1t2c1t2e1z2c1s2c1x2c1u2c1t2c1t3c1w2c1s1c1j2c1u2d102c1s2d1i2c1s2e1o2c1t2c1x2c1q3c1z2c1u2c1s2c1s2c1i2c1u2c1e2c1s1e1k2c1s3c1q2c1u1d1h2c1s2d1v2c1u2c1a2c1s2c1t2c1s1e1z2c1s2e1o2c1s2d1t2c1s2e1z2c1t2c1r2c1q1c1x2c1s2e1o2c1r2e1j2c1u3c1t2c1s2e1w2c1s2e1w2c1s2e152c1r2e1q2c1t1c1s2c1s1e1o2c1r1c1t2c1u1e1w2c1r2c1t2c1t2c102c1r2e1p2c1q3c1u2c1u1c1w2c1s2e1s2c1s1e1d2c1t1c1w2c1q1e1b2c1s1e182c1q2c1y2c1u2e1y2c1r2e1p2c1s1c1u2c1u2e1u2c1q1e1b2c1r1c1t2c1u3c1w2c1r1c102c1s2e1o2c1s2d1s2c1s2c1i2c1u2e1s2c1s2e1s2c1u1e1v2c1s3c1h2c1s2e1h2c1t2c122c1q2e1e2c1t2c1v2c1s2c1q2c1t2e1z2c1s2e122c1q2e1t2c1u2e1q2c1r2e172c1u2c1o2c1t2c1q2c1s2c1t2c1s1c142c1p2c1s2c1t3c1g2c1t3c1x2c1q2c1x2c1u1e1k2c1q1c1y2c1t2c1y2c1s1c1e2c1s2c1u2c1t1c1o2c1r2e182c1u2e1o2c1t2e1u2c1r1c1z2c1u2c1h2c1s3e1r2c1u1e1v2c1t2e1r2c1s2c1u2c1u2c1z2c1s2c1q2c1u3c1j2c1s3c1v2c1s2d1t2c1u2c152c1r2c1u2c1t2e1o2c1t3e1p2c1s3e1h2c1t1e1r2c1s3d1f2c1s2c1h2c1r1e1d2c1s2c1c2c1t3e1z2c1r3e1r2c1s2e1u2c1u1e1x2c1s2c1j2c1t2c1w2c1p2e1q2c1t3c1y2c1t2c1d2c1s2c1g2c1s1d1c2c1q1c1a2c1u2c102c1u3c1s2c1q3e1f2c1u3e102c1q1c1t2c1t3e162c1s2d1u2c1s2c1p2c1s1c152c1q2e1t2c1u2d152c1u3c1f2c1r2e1w2c1u2e1s2c1r1e1x2c1u2e142c1s3e1w2c1q3e1p2c1t2d1s2c1s3e1x2c1t1d1r2c1t2c1r2c1s2c1q2c1u2d1t2c1r2d1y2c1u2c1o2c1t2e1d2c1s1c1j2c1s3e1h2c1q2e132c1u2c1x2c1u1e1q2c1s1e142c1s3c1y2c1q1e1q2c1u2c1s2c1u2d1v2c1q3c1y2c1u1e102c1r2e1s2c1u1e152c1t2d182c1s1d1u2c1u1e1g2c1s2e1q2c1t2c1v2c1t2e1q2c1s2e1q2c1s1e1t2c1r2c1y2c1u3d102c1t1c1h2c1r2e1s2c1u3d1o2c1s2c1u2c1r2e1h2c1s3e1k2c1r2e1z2c1s3e1z2c1s2c1g2c1s1e1z2c1t2e1r2c1r3c1o2c1u2c1g2c1q2e1r2c1t3c1z2c1r3c1y2c1s2c1d2c1s2e1t2c1r2e1r2c1u2c1y2c1s2c132c1q2e1f2c1t2c152c1s2c132c1u3e1w2c1u1c1q2c1s2c1j2c1s1c152c1s3c1f2c1u3c1k2c1s3e1s2c1p2e1z2c1t2c1s2c1q2e122c1r2e1k2c1s1c1d2c1q1e1y2c1t2e152c1r2e1r2c1t2c1s2c1t1c1o2c1r2d1r2c1s2e1t2c1r2e1f2c1u2e1s2c1s2e1p2c1q2c1r2c1u2e1k2c1s2e1j2c1t2e1s2c1t2e1y2c1s3c1w2c1t2e1t2c1s3e1d2c1u3c1w2c1s2c1j2c1q2e1x2c1u3e1w2c1s1c1q2c1u3c1o2c1t2d1v2c1s2e1x2c1u2c152c1s2c1s2c1u3e1s2c1u2c1j2c1s2c1r2c1u2d1o2c1q2e1j2c1s2e1w2c1u3c1x2c1q1e1t2c1u2e1s2c1s2c1j2c1s2e1x2c1t1e1h2c1r3e1t2c1u1e1s2c1r2c1d2c1t2e102c1t1d1y2c1r2e1o2c1u2d1v2c1q2e1d2c1s1c1s2c1t3c1k2c1s1e1j2c1u1e1o2c1r2c1q2c1u2c1p2c1s2d142c1r2c1t2c1u1c1b2c1s2c1b2c1t2c1u2c1t1c1t2c1s1e1j2c1s1c1d2c1s1c1y2c1u2d1y3d1x121s2i3e193d1q1c171c131e103c141e1i3d151e1e2e1i1c1x3e1i3e132c1t3e1t2c1u2c1v2c1s2e192c1s1d1y2c1t2e1o2c1s2d1w2c1t2e1o2c1r1c1u2c1r2c1s2c1s2c1w2c1s3c172c1u2e102c1q3c172c1r3e1z2c1s2c1u2c1u1c1j2c1t2c152c1q1c1o2c1q3e1f2c1u2c1c2c1s3e1e2c1u1d1x2c1r2e1j2c1s2e1t2c1u3e1x2c1s2c1a2c1u1c1x2c1s2c1h2c1q1d182c1u3d182c1s3d172c1s3d1a2c1q3d192c1s3d1o2c1s3d172c1t3c1b2c1s1d182c1s3d152c1q3d172c1t3d1b2c1s1d162c1u3e102c1q3d182c1q3d192c1s3d162c1s3c152c1s3d172c1q3c1d2c1q3d172c1s3d1j2c1s3d172c1u3d1c2c1q3d172c1q3d1j2c1s2d162c1u3d1c2c1s3d172c1q3d1b2c1q2c1z2c1s2c1i1c1h3c1d2d1e1c1h3b1d3d1c3c192c143c103b1b2e181d171e1c1e1g3d1e3c1c3d1d2e1k3c1o1c1g1d1h1e1a1c1h3c1b2d1i3d183d1d3c1a1d1g3d121d1h1c101e1w2d1j1d161c121b1b1e1e3d1p1c193c1c3e1h3e1e3d1e3e1c3d1e3c1d3d1c1d1k3d1i3d1w1e122c1e1c1b1c1b1e1h1d1k3c1y3e1c2d112c1a3d122d1c3c1g1c1g3c1c1c1q2e1p1c1c2e193d143e1b2e1i1d1k1d1f3c121e121c1a1d1r1e193c1e1c1x2c1u2c1z2c1q2d1s2c1p2c102c1s1d1c2c1s1c1i2c1u1e102c1q1c1y2c1q2d1o2c1t2e1j2c1s1c1c2c1t2c1p2c1r1c1r2c1s2d1r2c1s2e1y2c1u3d1w2c1t1e102c1s2e1j2c1q2c1s2c1s1c1q2c1r2d1q2c1u1c1s2c1s2e1k2c1s2d1x2c1u2c1i2c1u2c1p2c1t1c1p2c1s2c1j2c1p2e102c1s1c1u2c1u2e152c1u3c102c1s1c1t2c1r2e152c1u2c1u2c1t2c1x2c1s2e1o2c1s1e1j2c1s2c1s2c1s2e1i2c1u1c1y2c1s2c1f2c1q1c1d2c1s2c1r2c1s2c1o2c1t1e1w2c1u1d1j2c1q2d1t2c1r2e1z2c1s3e1t2c1s2c1u2c1u3c1x2c1s1c1p2c1s2c1o2c1s2d122c1s3c1y2c1u3e1h2c1q3d1q2c1s1e1j2c1t2d1g2c1u2c122c1s1c162c1r2d1q2c1s2e1u2c1u1c1t2c1u3c1x2c1s2c1f2c1q2c1v2c1r2e1i2c1u1c1x2c1u2e1a2c1t2c1v2c1s2c1j2c1q2c1a2c1u1d1j2c1s3e1k2c1t3e1a2c1r2c102c1s2d1s2c1u2d1a2c1s2c1y2c1u2c1w2c1s2e1x2c1s2c102c1u2e1u2c1s2e1c2c1r2d1s2c1r2c102c1s2e102c1t2e152c1s2c1f2c1t2e102c1r1c1r2c1q2c1x2c1t2d122c1t2e132c1t3c1z2c1q2c1t2c1r2d1w2c1s1c162c1u3c1y2c1s1e182c1r2e1q2c1r3c1w2c1s1c1q2c1r2c1i2c1s1c102c1s2c152c1q2e1p2c1t2e1j2c1t2e1q2c1t2d1u2c1s2c1i2c1s2e1s2c1r1c1x2c1s3e1a2c1t2e1x2c1r2d1k2c1s3c152c1t1e1g2c1t3c1k2c1u1e102c1r2d142c1r2d1o2c1s2c1u2c1u2c1q2c1t2e1g2c1s2c1q2c1s1c1h2c1u1e1o2c1u1e1x2c1s3e1u2c1s2e1k2c1r1d1u2c1u3c1o2c1t2e1u2c1s1c1e2c1q2e1s2c1r2e1s2c1u2c1f2c1t3d1p2c1s2c1w2c1q3e1u2c1r3e1w2c1t1e1q2c1s2e1x2c1s2c142c1p1e1u2c1r1e1t2c1t1c1i2c1r2e1w2c1s3e1c2c1r2c162c1s3e1r2c1u2c1t2c1u3c1j2c1t3c142c1s2c1i2c1q2e1y2c1s1c1i2c1u2e1r2c1u3c1s2c1q1e1v2c1r2c1t2c1t2c122c1u2c1w2c1t2c142c1s3e1i2c1r3c1v2c1u2c1x2c1s3c1q2c1t3e1w2c1r2c1u2c1s2c102c1u1e1q2c1u2e1x2c1s2e142c1r3d1u2c1s2e1s2c1u2c1d2c1s1c1t2c1t1e1h2c1r2c1h2c1q1c1g2c1u3e1d2c1s1c1j2c1s2c1y2c1q3e1f2c1s2c142c1s2d1f2c1t3e1f2c1t1e1s2c1r1e1v2c1s2e1s2c1s1c1p2c1u3c1j2c1u3c1j2c1r2d1r2c1s3c1i2c1u2e1u2c1u2e1p2c1t1e1v2c1q1e1t2c1r2e1g2c1s1e1g2c1u1e122c1t1c1z2c1s2d1r2c1r2c1y2c1u2e1p2c1t1e1t2c1s2e1t2c1q2e1t2c1r2d1s2c1s2e1d2c1s1c1q2c1u1e1h2c1q2e1t2c1p2e1v2c1r1e1p2c1s1e1s2c1t1c142c1s2c1j2c1r2e1v2c1s2e1k2c1u3c1s2c1t2c1s2c1q1e1f2c1s1e1h2c1t2e1q2c1t3c1c2c1r2e102c1q2c1c2c1s1c1c2c1s2c1e2c1u2e1p2c1t2e1h2c1q2e1j2c1s2d152c1s2e122c1t3c1u2c1u2e1j2c1r2c1f2c1r2c1a2c1t2e1j2c1u2c1j2c1t1e1s2c1r3e1t2c1r3c102c1u2e1q2c1u2c1x2c1t1d102c1s3c1t2c1q2d1c2c1t1c1y2c1s2e1x2c1u2e1s2c1r2c102c1q2e1s2c1t2e1s2c1t2e1i2c1u3e1o2c1s2c1f2c1r2e1u2c1s2e1g2c1t3e1x2c1u2e162c1q2c1t2c1r2e1w2c1s3e1f2c1s2c1p2c1s2d1z2c1r3e1a2c1s2c102c1u2e1k2c1t2c1r2c1s2e1s2c1s2e1p2c1r1c1z2c1t2d132c1s1c132c1s1d1u2c1q2e1y2c1p2e1x2c1t1e152c1u3e1y2c1u1e1h2c1r1e1v2c1q2e142c1t2e132c1u3c1y2c1u3c1y2c1r2d1s2c1r1c1r2c1s2e1q2c1t2c1f2c1s3c102c1s2e102c1s1d152c1t1d1g2c1u2e1y2c1t2e1r2c1r2c1j2c1r2c1u2c1s1d1v2c1s1c1i2c1r3e1c2c1r2e1j2c1q3c1z2c1t2e1f2c1u1e132c1u3e142c1s1e152c1r3e1z2c1r2e1u2c1t1e132c1s3c142c1s2d1w2c1q3c152c1t2e1w2c1s2c1f2c1t3e1z2c1r2c1q2c1r2e172c1u2d1s2c1s2c1x2c1t3e172c1s2e1p2c1r2d1s2c1r2c132c1s2e1p2c1t3d102c1s1e142c1s2c1o2c1u1e1y2c1s2e1q2c1t3c1t2c1s1c1v2c1s1e1s2c1u1e142c1s1c1y2c1u1c1g2c1s2e1f2c1r3c1p2c1r1c1x2c1t1e1g2c1s2d1r2c1p2e1r2c1r1e1s2c1u3c132c1t2e1p2c1t2e1y2c1s3c1v2c1r1e1x2c1t2e1i2c1t1e1q2c1r2c102c1s3e1a2c1r2d1t2c1u2c1u2c1t3c1q2c1u2e142c1r2e1z2c1r3e1t2c1t2d1i2c1u3e1y2c1u2c1r2c1q2d1u2c1s2e152c1r1c1p2c1t1c1k2c1t2e1r2c1s2c1j2c1p2c1s2c1t2e1u2c1s2d1j2c1u3d1u2c1s1e102c1r2e1x2c1t2e1y2c1s2e1t2c1u1e1o2c1s1e1i2c1r2c102c1t2e1i2c1s2e1x2c1t2e142c1r3e1y2c1r2e1x2c1u3d1s2c1r2e1y2c1t2c1y2c1r2c1f2c1s2d1u2c1s1e132c1t2e1w2c1s3e1z2c1s2e1z2c1r1e1u2c1t2d1q2c1u1d1d2c1t1e1x2c1r2c1a2c1r1d152c1u3c122c1u2e1r2c1u2e152c1q2e1q2c1q2d1p2c1t2e1x2c1u3e1f2c1u2d1o2c1r1e1j2c1r3c1s2c1t1c132c1s2e1u2c1u2e1x2c1s3c1q2c1r1c162c1u1d1q2c1u2d1q2c1t2c102c1q2c1d2c1q3e1h2c1t2c1y2c1s2e1s2c1s2c1o2c1q1c1j2c1q2c162c1t2e132c1s3c1a1c1t2c1s2c1o2c1u2c1r2c1s2e1f2c1q2d162c1q2c1r2c1u1d1p2c1s1c1y2c1s2c1h2c1s2c1s2c1s1c1x2c1r2e1g2c1t2e1t2c1u2d1p2c1r3c1s2c1q2e1c2c1s2c1r2c1s2c1g2c1s2e1j2c1s1e1o2c1s2c1t2c1t2e1r2c1u2c1r2c1u3e1t2c1s2c1r2c1r2c1q2c1u3c1u2c1r1e1v2c1u2e1s2c1q1c1o2c1s1e1q2c1s3c1r2c1u1c1x2c1t2e1q2c1r2c152c1s2c1p2c1u2e162c1u2c1s2c1s2e1c2c1s1c1u2c1r3d1k2c1t2c1k2c1s2e1r2c1s2c1u2c1s1e1y2c1q2e1t2c1s1c1o2c1t2c1v2c1s2c1t2c1s2c1h2c1q2e1k2c1s2c1k2c1t2e1p2c1u2c1a2c1r1c1o2c1q2c1s2c1s2e182c1s1c1h2c1t3c1g2c1q2c152c1r3c1y2c1s1e1p2c1t3d122c1u2e1u2c1s1c1p2c1p2e1v2c1t2e1y2c1t2c1u2c1u1c1w2c1r2e162c1s2d1g2c1t2c1j2c1t1e1v2c1t2e1q2c1s2d1e2c1q2c1f2c1u2c1h2c1u1e1d2c1s2e1w2c1q1d1i2c1s1c1i2c1s2c1q2c1r2c1r2c1u2d152c1q1c1w2c1s2e1y2c1u3e1t2c1t2e1f2c1s1c1f2c1s1e152c1q1e1u2c1u3c1r2c1t1d1s2c1u2d102c1r2c1v2c1s3c1x2c1s2c1y2c1t2c1v2c1u2d1r2c1q3e1v2c1r2e1a2c1s1c1s2c1u2e1v2c1s1c1j2c1q1c102c1r1c1j2c1u2e1h2c1r1e1c2c1u2e1b2c1q2c1a2c1r2e1w2c1u2e1w2c1t1e1t2c1t2c1i2c1q2e1v2c1r1c1s2c1t2c1i2c1r1e1f2c1s2c1t2c1q2e1u2c1p1e1r2c1t2d1u2c1t3d1i2c1u1e1g2c1s1e1k2c1r2c1j2c1u2c142c1t1c1w2c1u3c1s2c1q2e1t2c1s2c1h2c1u2e1i2c1t2e1y2c1t1c1t2c1s2c1w2c1r2e1t2c1u2c1v2c1s1c1y2c1u2c1y2c1s1c1c2c1q2c102c1t2e1t2c1u2e1q2c1t1e1x2c1s2e1w2c1q2d1u2c1u1e1g2c1t2c1v2c1r3c1x2c1s2e1v2c1s2e1j2c1t1c1q2c1t2e1r2c1s1c1r2c1r2c102c1r1c1v2c1s3e172c1t1c1k2c1t2e182c1s3e1h2c1s2d1t2c1t2e1u2c1u1c1r2c1s2c1f2c1q1c1y2c1q1c1f2c1s2c1s2c1s1d122c1t2e1t2c1r1e1u2c1s2c1o2c1s2c1h2c1s1d1w2c1s2e1t2c1p2e1i2c1r1c1z2c1t2e1p2c1u2c1h2c1t2e1r2c1r2e1p2c1r2c102c1t2c1r2c1t2c1x2c1u2e1x2c1r2e1p2c1s2c1w2c1t2e1s2c1t3c1h2c1u1e1i2c1q1c1g2c1q3e1u2c1s3e1w2c1s2e1s2c1t2e1y2c1q1c1v2c1r2e1t2c1s2e1h2c1s2e1r2c1u2e1f2c1r1e1h2c1r2e1r2c1u2d1q2c1s1c1v2c1u2e1s2c1q2e1r2c1q2c1v2c1t1e1h2c1s2e1r2c1s1e1f2c1r2e1t2c1s2d1s2c1t1c1x2c1u2c1h2c1t2e1t2c1q2e1p2c1s2c1s2c1t2e1v2c1u2c1h2c1u2c1j2c1q2c1t2c1s2c1e2c1u3c1k2c1s2e1r2c1u2d142c1s2c1h2c1q2e1e2c1t3e1p2c1t2c1p2c1t2c1r2c1r2c1v2c1q2e1q2c1u3c1v2c1s2e1o2c1u1c1e2c1s2e1z2c1s1c1x2c1u2e122c1t2c1p2c1s2e1x2c1r2c1u2c1q1e1y2c1s2e1k2c1t1c1r2c1t2c1j2c1r2c1t2c1s2c1a2c1t2e1i2c1t2e1q2c1s2c1d2c1s1e182c1q2c1q2c1u2c1r2c1s1e1v2c1u3c1h2c1q1c1x2c1s3c1f2c1u2c1y2c1s2e1w2c1u3e1t2c1r1e1w2c1r1c1v2c1s2d1e2c1s1e1h2c1t3d152c1p1e1r2c1q2d1x2c1t1c1a2c1s1c1j2c1t3e1x2c1s2e162c1s1c1o2c1s1d1k2c1s2e1q2c1u1c1p2c1s2c1w2c1r2e1i2c1s2e1t2c1u2e1y2c1t2c1r2c1s2c1o2c1s2c1y2c1t3c162c1t1c1s2c1t2e1y2c1r1d1t2c1r2e1j2c1s2e1h2c1u2c1s2c1t1e1j2c1s2e162c1s3c1z2c1t2c1t2c1u2c1y2c1u2c1u2c1r2e1v2c1s3e1x2c1t2e1w2c1s2e1v2c1s2c1w2c1q1e182c1r2e1j2c1s3c142c1t1c1h2c1t2c1y2c1q2e1y2c1s3e1z2c1u2d1x2c1u2d1h2c1s3e1p2c1r2e1s2c1s2e1u2c1t2e1w2c1t1e1u2c1t2c1z2c1q2e1r2c1q2e1x2c1u3e1f2c1t1e142c1s2c1t2c1s1e102c1r2e1w2c1t2c1x2c1u2d1u2c1u1c1y2c1s2c1z2c1s1e1i2c1u1c1r2c1r2e1h2c1u3c1x2c1p2c142c1q2d1c2c1t1e1c2c1s2e1r2c1s3e1j2c1s2c152c1r3c1h2c1t1e1w2c1s3c1g2c1u1e1s2c1r3d162c1q1e1t2c1u2e1q2c1s2c1d2c1r1e1r2c1r1e102c1q1d1e2c1u1e1k2c1t2d1b2c1u2c1u2c1s2e1h2c1r2c1f2c1t3e1k2c1t1e1w2c1u2c1q2c1r1c1f2c1s2e1t2c1u2e1e2c1s3e1r2c1u3c102c1q1c152c1q2c1t2c1u2c1y2c1t2e1h2c1u3e1r2c1r2c152c1r3e1u2c1s2e1w2c1t2d1q2c1t2e1c2c1r2c1u2c1r3c102c1t3e1u2c1r2c1o2c1t1e1w2c1q2e1o2c1q2c1w2c1u2c1o2c1u2e1r2c1u3c1j2c1s3e1t2c1q2e1q2c1u2e1g2c1s2e1u2c1s1e1y2c1r3c1j2c1s2e1x2c1t2e1d2c1s2e1p2c1u2c1x2c1s2e152c1s2e1x2c1t3e1u2c1s2c1f2c1u2c1v2c1r2c1x2c1s1e1s2c1u2c1u2c1u2c1s2c1t1e1s2c1r2c102c1q2e1y2c1u2c1q2c1t3c142c1u2e1z2c1p2e1u2c1q3c1t2c1u2e1k2c1u2c1w2c1t1c1t2c1s1c152c1r2c1q2c1t2c1s2c1s3c1r2c1s1c1x2c1q2c102c1q2e1t2c1u3c1i2c1r1c1r2c1u3d1o2c1p2e1q2c1s3e162c1u2e1d2c1u2e1v2c1u2c1f2c1s2e1s2c1q1e1y2c1t3c1q2c1s2e1o2c1u2e1t2c1q3e102c1q2c1y2e1v2c1s2e1h2c1s2e102c1u3c1r2c1t2c1h2c1s1c1w2c1s2c142c1s3c152c1s2c1y2c1s2e1o2c1u2e162c1r2c1o2c1r2e1w2c1s2c1v2c1s1e1r2c1t2e1z2c1s1c1s2c1q1e1z2c1u2e162c1u3c1s2c1s2e1b2c1q2c1p2c1q2c1v2c1s2d1v2c1s1e1r2c1s1c1y2c1r2e102c1q2c1r2c1t2e1r2c1t1c1e2c1s2e1w2c1s2c1s2c1q1c1o2c1u2e132c1t2e1v2c1u3e1s2c1s2e172c1q2e1z2c1t2e1s2c1s2c1g2c1u1d1h2c1r2e1c2c1r1e1j2c1t2e1w2c1u2e1r2c1u2c102c1r2c102c1r2c1v2c1t2c1k2c1t2e1d2c1u2c1w2c1r2c1w2c1r2d1s2c1t1e1y2c1u2e1y2c1u2c1s2c1q3e1z2c1r1c182c1s3e1i2c1t3c1p2c1u3d1o2c1s1d1b2c1s2c1w2c1s2d1e2c1t2c1s2c1s2c102c1q1e1w2c1s3c1s2c1t3c1r2c1t3e1i2c1u1c102c1s2c102c1s1d1h2c1u2e1g2c1t3e1v2c1u2e1s2c1r2e102c1r2c1k2c1t3c1o2c1u2c1r2c1u2e102c1s2c1s2c1s1e172c1u2d1h2c1t2e1t2c1s3c1r2c1r3e102c1r3c1x2c1u3e1d2c1s2e1w2c1u2d1o2c1s2c1o2c1r2c182c1s2c1o2c1u3d1i2c1r2c1x2c1r2c102c1s1c1h2c1s3c1w2c1t3c1o2c1t1e1o2c1q1c1u2c1q2c1h2c1u3d1y2c1s3c1k2c1s1c142c1r1e1v2c1r2e1o2c1t2c1c2c1t2e1q2c1t1e1r2c1s1c102c1q2c1p2c1r2e1u2c1s2d1h2c1u2c1t2c1r1e102c1r3c1s2c1s2c1r2c1t2e1c2c1t3e142c1q2c1v2c1q2c172c1u2e1t2c1t3e1r2c1s3c1w2c1r2d1p2c1s1c1v2c1t1e1u2c1u1c1x2c1s2e1v2c1s3c1r2c1r3c1o2c1r1e1p2c1s1c1d2c1t2c1s2c1s2e1x2c1r3c102c1s3c1r2c1u1e1q2c1t1e1s2c1s2e1z2c1r3e1x2c1t1e1v2c1r2e122c1t1e1f2c1r1d1v2c1p2e1j2c1s2e1e2c1u2d1r2c1t1c1o2c1s2e1z2c1q3e1p2c1u3c1w2c1u2c1s2c1u2d1t2c1s3d102c1q2c1s2c1t2c1h2c1t1c1x2c1s2c1t2c1r2c1a2c1r2c1y2c1s2d122c1s3c1r2c1t3c1z2c1q2c1o2c1s2e162c1t2d1u2c1u2c1p2c1u2c1h2c1r2e1u2c1s1e142c1u2c1f2c1t3c1q2c1s3c1c2c1s2c1w2c1r2c1h2c1t1e1q2c1u2c1d2c1u3c1h2c1s1d1s2c1q3e1a2c1r2e1p2c1u2c1d2c1s1c1g2c1r2c1f2c1s2c1f2c1t2d1d2c1u2e1q2c1u1c1r2c1r2c1p2c1s1c1q2c1u2e1h2c1u1e1s2c1s2c1o2c1s2e1r2c1r1c1q2c1t2c1w2c1s2c1w2c1t1c1v2c1r2c1g2c1s2c1t2c1s2c1c2c1u2e1y2c1u2c102c1p1e1r2c1r1c102c1s2c1w2c1t1c1r2c1t2c1g2c1s2c1r2c1q2e1s2c1u2d122c1u2c1d2c1u3c1h2c1s2c1s2c1q2d1g2c1s2c1k2c1r2e1d2c1t2e1z2c1r1e1h2c1q3c1i2c1t1e1o2c1u2e1r2c1u2e1z2c1s1c1i2c1s2e1w2c1u2e1q2c1u1e1r2c1s1e1s2c1s2e1g2c1q2c1o2c1t2d1h2c1r2e1v2c1r2e1g2c1r2e1s2c1r2e1u2c1t2c1x2c1s2c1b2c1s2c1w2c1s2c1x2c1r3d1h2c1t2d1f2c1t2d1r2c1t1c1o2c1r1c1j2c1r1e142c1t2c1k2c1r3e1k2c1s1d1r2c1q1c1v2c1s2e1v2c1s2e162c1u3c1r2c1u2e1t2c1q2e1s2c1s2c1s2c1u3c1d2c1t2e1h2c1t2e102c1s1e152c1r1d1x2c1r2c1t2c1u1c1j2c1s3d1r2c1r2c1e2c1q2c1s2c1s2d1v2c1u1c1w2c1t1d102c1s1e1h2c1r2c102c1t3c1r2c1t2d1w2c1u1e1t2c1q2c102c1r3c1o2c1u2d1q2c1u3c1x2c1u2c1v2c1r2e1r2c1q2e1r2c1u1e132c1u1e1r2c1u2e1t2c1r1c1k2c1q3e1c2c1u2d1h2c1t2c1r2c1u1e1o2c1q3c1z2c1s2e1s2c1s2e182c1u2c1w2c1t2c1t2c1r2c1z2c1s2c142c1t1e1y2c1s3c1x2c1u1d1y2c1q3e152c1r2e1o2c1t3c1h2c1s3e1h2c1t3e1t2c1s2e1j2c1r1c1u2c1u3c132c1s2d1u2c1u1e1q2c1s2c1o2c1s1c102c1s1c1u2c1s3c1v2c1t2e1h2c1q2c1y2c1q3c1t2c1t2e1v2c1s1c1w2c1s1c102c1q1c1s2c1r3e1z2c1t3e1g2c1u1e1s2c1s1c1u2c1s2c1z2c1r1e1s2c1t2c1y2c1t2e1u2c1t2d1u2c1s3e102c1s3e1s2c1t2e142c1s3e1w2c1u2e102c1s1e1r2c1q2e1i2c1u1e1y2c1s1c132c1u2e1s2c1q1e1t2c1r1c1t2c1s2e1r2c1s2e1k2c1u1c1x2c1p2c152c1r2e1u2c1s2e1o2c1u2e1x2c1s1e142c1p2d1e2c1r2c102c1t2e1u2c1u2e1q2c1s2c1v2c1p1c102c1r2e1s2c1u3c1s2c1u2e1t2c1u2e1w2c1q2e1s2c1s1e1i2c1t1e1r2c1s2e1h2c1u2c102c1s1e1i2c1s2c102c1u1e1y2c1t2e1k2c1t2e142c1r2c152c1s2c152c1s3e1x2c1u2e1v2c1t2c102c1s1c1w2c1s2c152c1u2d1i2c1u2e1x2c1s1d1h2c1s2c1w2c1s2c1k2c1u2c1s2c1s2e1k2c1t1d1t2c1s2c1t2c1r2e1t2c1u2e1p2c1s2e1r2c1t2d1r2c1r2e1x2c1r3c1t2c1s2c1o2c1t2d1y2c1u2c1x2c1r1d1s2c1r3c1z2c1t3d1d2c1u3e1h2c1u1e1r2c1r1d102c1r2e182c1t2e1r2c1s2c1q2c1u2c172c1s2e1t2c1q1c1o2c1t1e1q2c1s2c1q2c1s2e1f2c1r2c1u2c1q3c1r2c1s2c1j2c1s3c1w2c1t1e1f2c1r2c1w2c1q2c1o2c1s2c1c2c1r2c1c2c1t2d1o2c1r2d1r2c1r3d1b2c1s2e1r2c1t2c1j2c1u2e1h2c1r2c1a2c1s2e1o2c1u2d1r2c1u2e1r2c1f2d1u2c1x3c193c1f171t2r2d1e3e1c1c1g3c1k1e1h1d1k1c1d3c1e1d1e1d1e2c1h1e1b2c132c1s1c1j2c1t2c152c1q1c1j2c1q3e1f2c1u1c1c2c1q3e1e2c1u1d1x2c1r2e1h2c1s2e1t2c1u3e1x2c1q2c1a2c1u1c1x2c1s2c1f2c1q1c1u2c1s2c1u2c1r2c1y2c1u2c1z2c1r2d1s2c1q1c152c1t2e1w2c1s2c132c1t3e1u2c1s1c1i2c1s1c1z2c1u1c1v2c1q2d1u2c1t2c1t2c1q2d152c1r3c1z2c1s3d162c1q3c1c2c1s3d192c1s3e1b2c1q3d182c1s3d1b2c1q2d152c1t3d1z2c1q3d152c1q3c1k2c1s3d152c1q3d142c1s1d192c1q3d132c1q3d182c1s3d1t2c1q2d172c1s3e1g2c1q2d172c1q3d1b2c1s3d152c1q3c1o2c1s3d192c1s3d1r2c1q3d182c1u3e1w2c1q3d152c1s3d192c1q3d152c1q2c1u2c1s2e1d1c103e173d1q1c1p3d1p3b1b3d1d3c1b2c1p3c1w2d1i3e1d1c1c1e1p3c1b1c163e111e1h2c1b1d1i1e1d1c1e2c1s1e1c3e1d1c1h3c1b2d1b3d1j3d163c102c171d1c1e1g3d1e2c1d3d1q1d1k3c1o1c1g1e1f1e1a2d1k3d1k1e1i3e1i3e1d3d1c3e1j3e1f3e121c1d2e1f3d1s3c1b1c1d1c1g2d121d143e1d1d191e1f3b1s2d1s1d1d3c1b2e121d1o1e1a1e1g3c1h1c1d2e1c3c1x3c102c171d1q2d1b3d1w1e1q1e1d3c1p2c1u2c1z2c1r3c182c1r3e1x2c1s3d1k2c1r2c1h2c1t1c182c1r2d1s2c1r3c102c1s2c1q2c1s2e1s2c1r2e1j2c1q2c1k2c1s3c1v2c1t1c1y2c1r3c1j2c1s1c1w2c1s1c1u2c1r2e1t2c1u2d1t2c1q3c1t2c1s2c1w2c1q1c132c1s3c1u2c1u2d1v2c1s3e1f2c1t2e1k2c1r2c1v2c1r2c1s2c1t2e1d2c1q1c1q2c1s2c1w2c1r2d132c1s2e1y2c1u2e1j2c1q2c1w2c1t1e102c1s1e1u2c1s2c1k2c1u1e1t2c1s2c1y2c1u2d1f2c1q2c1i2c1s2d1p2c1t3e1x2c1q1c122c1s3c1p2c1r3c1o2c1s1c1k2c1u1e1f2c1r2c1w2c1r2c1o2c1r2e1k2c1s2c1f2c1t3e1s2c1r2c1s2c1s2e1w2c1q3e1j2c1q2c142c1s3e1o2c1r2d1s2c1s2e152c1r3d1x2c1s1c1d2c1u2e1j2c1q2c1u2c1t2c1w2c1s2c1y2c1s1d1f2c1u2c1j2c1r1e1x2c1u2e1z2c1r2c1y2c1r2c1t2c1t3e1k2c1s1e162c1t1c1r2c1r2c1q2c1s3d1g2c1u3c1x2c1q2c1s2c1t2e1u2c1s1c1y2c1s3c1u2c1u1c1j2c1q1c1d2c1t3c1o2c1q2c1i2c1q2d1s2c1r2c1q2c1s2d152c1s1c1w2c1r2e1y2c1s3e1v2c1u3e1s2c1s2c1p2c1s2c1o2c1s2c142c1s3c1t2c1t2e1f2c1s2c1g2c1t1e152c1q1c1q2c1q2e1w2c1t2e1d2c1r2e1a2c1u2c1s2c1s2e1j2c1s1c1j2c1s1e1f2c1q1e1c2c1u3e1c2c1r2e1y2c1r2c1t2c1t2e1g2c1s2e1s2c1t1e1h2c1r3c1i2c1s2e1v2c1u1e1q2c1q2c1i2c1u2c1h2c1q3c152c1r3c1t2c1u2d1h2c1q2e1t2c1s1e1q2c1r2e1y2c1q2d152c1r1e1q2c1s1e1t2c1r1c1v2c1s1e1i2c1r3c1t2c1s2c132c1r1c1h2c1u2e1u2c1q1d1p2c1q2c1f2c1s2e1u2c1r3d1j2c1u2c102c1s1e1h2c1s2e1h2c1u1d1r2c1s1d1h2c1u2e1o2c1r1c1p2c1s2e1x2c1s2d1t2c1r1e1j2c1u2e1u2c1s2c1y2c1q2e1r2c1u2e1y2c1r2c122c1t2c1z2c1r2e1v2c1r1e1j2c1t2c1f2c1r1c122c1s2e1o2c1s2e1p2c1r2c162c1u2e1h2c1q2c1q2c1s2c142c1s1e1u2c1q2e1t2c1t2d1y2c1r2e162c1t1c1i2c1r2d1u2c1s2c1x2c1t1c1i2c1s1e1t2c1s1c102c1s3c1j2c1s1c1t2c1u2e1q2c1s2c1x2c1s2e1u2c1r2c1t2c1s2e1p2c1s2e1q2c1s2c1v2c1u2c1h2c1s2c1t2c1r2d1j2c1u3e1y2c1r2c1q2c1s1c1o2c1r2e1r2c1r2e1t2c1t2e1y2c1r2c122c1u2e1z2c1r3e1i2c1r2c1q2c1s2d1e2c1q2c1p2c1r2e1h2c1q1d1x2c1q2e172c1s1e1a2c1s2e1x2c1s2e1t2c1r3e1i2c1q2c1e2c1s2c1p2c1p2e1f2c1t1c1v2c1q1e122c1r3e1t2c1t1e1q2c1s2c1y2c1s2e102c1s1e122c1r1e1z2c1u2c1r2c1q2c1c2c1u2c1p2c1p2e1t2c1q2d1i2c1s1e162c1r2d1s2c1s2e1t2c1q2e1t2c1p2e1t2c1r1e1p2c1q2c1x2c1t2c1s2c1q2c1x2c1q2c1i2c1t2e1p2c1s2c1p2c1t1e1h2c1q2c1f2c1s3e1i2c1t2c132c1p2e1c2c1s1e1v2c1s2e1j2c1q2c1j2c1t1c1h2c1s2c1f2c1t1c1o2c1r1d1j2c1s2c1y2c1t1e1p2c1q2c1v2c1u3c152c1s2e182c1r3c1d2c1u3d1s2c1r1e1y2c1t1e1f2c1q2e1s2c1r2c1y2c1r2d1j2c1s2d1j2c1u1c1a2c1r2d1p2c1q2e1p2c1s2c1x2c1q2c142c1s1c1d2c1p2e1v2c1q2e1u2c1s1e1q2c1p2e1j2c1u3d1z2c1q2e1i2c1r2e1p2c1t2e1h2c1r3c1s2c1u2c1w2c1q1c1k2c1s2e1y2c1t3c132c1s2c132c1u3d1s2c1r2d1j2c1r2d1y2c1t1e1y2c1q2d1y2c1s1c1h2c1q1c132c1q1c1y2c1t1c1i2c1s2e1w2c1s2d1w2c1s3c182c1q2c102c1s1d122c1r2c1j2c1t2d1t2c1s2e1y2c1s3e1t2c1u3c1v2c1s1e1x2c1t1d152c1s2c1p2c1s2c1q2c1s3c1d2c1r2c1f2c1t2e102c1r2c1q2c1q2c1w2c1s1e122c1r2d1u2c1t1e102c1r2e1y2c1p2d142c1s1c1v2c1r2e1o2c1s2e152c1r3c1v2c1r2e1t2c1s1c1y2c1s3e132c1r1d162c1s2e1f2c1r2e1t2c1t3c182c1r2e1c2c1r1e102c1s2c1j2c1s3e1h2c1t2c1f2c1r1d1y2c1s3e1z2c1q1c1w2c1s3e1p2c1s1c1v2c1q1c1p2c1s2e102c1s2c1f2c1s1c1y2c1u1c172c1q2d1s2c1t2e1i2c1s1c1j2c1q2e1t2c1u3c1f2c1q2e1x2c1s3c1t2c1r1d1p2c1s2e102c1u2e1r2c1r1c132c1t1c1t2c1r2c1k2c1q2c1p2c1s2d1w2c1s1e1e2c1u2e1r2c1s2e1i2c1s3e1z2c1r2e1u2c1q2e1y2c1r1c1f2c1r2d1s2c1q1e1f2c1u3c1u2c1s2c1s2c1t2c102c1r3d1s2c1q2c1s2c1t2c1j2c1s2c1i2c1t2e1q2c1r2c1r2c1s3c1u2c1t2e1r2c1p3c1j2c1s3c1a2c1p2c1r2c1r2e1r2c1u2c1x2c1r2c1u2c1t1c1t2c1p2e122c1q2c1s2c1t1e1g2c1r1e1q2c1u1c1z2c1q1c1h2c1r2e1w2c1t3c1v2c1r1c1q2c1t2c1o2c1q2c1j2c1s3e1u2c1s2d1x2c1s1e1s2c1u2d1y2c1r2e1j2c1s2c1q2c1t3e1u2c1s3c1y2c1s1c1h2c1r2d1r2c1q3c1f2c1s2c1u2c1s2c122c1u1e102c1r2d1u2c1q3c1t2c1s2e1t2c1s2e1u2c1r3e1j2c1q1c1p2c1q2c1d2c1t2e1v2c1s1e1h2c1r1e1o2c1q2c1v2c1r3e102c1s3c1r2c1p3e1g2c1r2c1j2c1p2e1k2c1s2c1d2c1u2c1j2c1q1c1t2c1s2c1h2c1r2c1y2c1s2c1t2c1t1d1t2c1s2d1i2d142c1u2c1r2c1r2e1o2c1s2e1q2c1s3e1v2c1q2e1u2c1t3e1q2c1s2e1k2c1u2c1u2c1q2e1d2c1s2e1w2c1u2e1v2c1s2e1i2c1t3d1j2c1r2c132c1q1e1f2c1u2e1w2c1r3c1d2c1t1e1y2c1s1e1s2c1s2c1p2c1s1c1f2c1p2e1v2c1s2d1h2c1r2e1x2c1q2c102c1u2c1h2c1r2c1i2c1s2e1q2c1r2c1h2c1s1e152c1t2e1t2c1r2c1x2c1s1d1t2c1q2c1g2c1q2e1o2c1s1e1u2c1q3c1w2c1s1c1d2c1r2c1r2c1q3e1h2c1s2e1h2c1r1c1q2c1t2c1q2c1s1c1x2c1q1c1r2c1t2c1s2c1r2e1t2c1t2c1o2c1q2e1d2c1s2e1j2c1t2c1h2c1r2c1x2c1u2e1t2c1r2e1o2c1r2c102c1u1d122c1r2e122c1t2c1s2c1s2c1p2c1q2c1o2c1u1e162c1q3d1d2c1u2c1u2c1s2e1f2c1r2e182c1s1d1w2c1q2e1r2c1t2c1u2c1s1e1s2c1r3d1f2c1t2c1r2c1r2c1r2c1t2c1y2c1s3c1i2c1s2e1r2c1s2c1d2c1r1c1h2c1s1c1u2c1s3d1b2c1r2c102c1t2c162c1r3d1o2c1s3e1y2c1s2c1w2c1r1e102c1s1c1s2c1s2e1w2c1u2c1t2c1s1e132c1s1c1o2c1t2e1t2c1q3c1k2c1t3c1t2c1r2e1h2c1q2c1w2c1t2c1o2c1q2c1t2c1t3c1f2c1s1e1v2c1s1e1s2c1t2e1q2c1s1c1r2c1u2c1y2c1r2e1w2c1s2e1f2c1u2e1w2c1q2e1o2c1s1e1q2c1s2e1u2c1q2d1f2c1u1c1q2c1r2e1d2c1t2c1t2c1s2c1d2c1r2c1v2c1s3e1g2c1s2e1w2c1t2e1v2c1s1c1h2c1r1e1s2c1u3c1r2c1q3c1y2c1u1d1t2c1s1c1d2c1r3e1o2c1s2c1v2c1q2c1s2c1u2d1t2c1r1c1v2c1p2e1v2c1u1e1f2c1s2e1k2c1u2c1e2c1q2e1w2c1q2d1r2c1u2e1r2c1r3d1k2c1s2c1u2c1r2d1s2c1r2c172c1s2c1r2c1q2e1i2c1t2e1s2c1s1c1f2c1r3e1j2c1r1e1y2c1q2e1s2c1u2c142c1r1e1y2c1r1e1p2c1t2c1p2c1q2c1h2c1u2e1z2c1r2c1t2c1q2e102c1u2c1s2c1s2c1r2c1s1c1t2c1s1e1d2c1s3e1h2c1t1e1g2c1s3e1t2c1u2d1k2c1r2e1x2c1s2e1s2c1u2e1b2c1r3c1i2c1t1e1q2c1s2e1b2c1s2e1v2c1u2e1q2c1r3c1s2c1u2e1e2c1s1c1y2c1s2e102c1s1c1q2c1r2e1r2c1s1c1o2c1q1e142c1q2c1r2c1u2d1h2c1r2c1v2c1s2c1h2c1q1e142c1r2d1v2c1s2e1w2c1s2c1h2c1r1e1k2c1r2d1h2c1s2c102c1s2c1o2c1s2e1w2c1s1c1s2c1s2c1o2c1q1e1a2c1u1e1x2c1q1c1v2c1u1e1f2c1s1e1d2c1r2e1s2c1t3c1a2c1p2e1w2c1s1c1c2c1r1e1s2c1s2c1v2c1u1e1r2c1q1c1v2c1u1e1f2c1r1e1r2c1r3c1b2c1u2c1i2c1p3e1r2c1s1d1i2c1q1e142c1s2c102c1u2c1r2c1p3c1u2c1r2c1q2c1r2c1h2c1q2d152c1t2e1f2c1s1c1r2c1t3d102c1p2e1k2c1s1c1r2c1t1e1v2c1s2c1h2c1u2c1j2c1q2c1p2c1r1e1g2c1u2e1w2c1r1e1b2c1u2c1t2c1q2e1q2c1s2c1v2c1r1e122c1s2e1j2c1t1c1p2c1r2c1q2c1s1e152c1u2c1w2c1r2e1r2c1s2e1w2c1q2d1x2c1s2e1z2c1t1e122c1q1c132c1u2e1j2c1s1e1y2c1s2e1r2c1t2e1v2c1s2c1w2c1s2e1t2c1s2e1k2c1s2c102c1u2e1d2c1r2e1k2c1r1e1y2c1s2c1o2c1r3c102c1t3c1d2c1s1e1p2c1t3e1r2c1s2e1h2c1s3d1z2c1t2c1c2c1r2e1w2c1s2c142c1q1c1r2c1s2e1w2c1s3e1a2c1p1e1d2c1u2c102c1s2e1o2c1r1e1t2c1s1e1y2c1q2c1q2c1t2e1x2c1q2c1t2c1s2c1c2c1t2c1u2c1r2d1o2c1u1c1x2c1r3c132c1s1d1t2c1t1e1u2c1s3e1g2c1s1c1y2c1q1c1b2c1q2c102c1s2c1k2c1r2e1d2c1s2e1i2c1r1e1t2c1s2c1r2c1t2c1d2c1r2e1r2c1t2c1u2c1s2e1w2c1r2c1s2c1s2e1d2c1r3c132c1t2c1w2c1r2e1q2c1s1e102c1r3e1y2c1r3e1o2c1t1e102c1r1e1d2c1s1e1s2c1s1c1w2c1r1c1x2c1u2e142c1r2c1y2c1r1d1i2c1u2e1w2c1r2e1k2c1t2c1j2c1r1c1q2c1s1e142c1u2e1p2c1s3e1o2c1t2e1t2c1r2c1q2c1s2e1q2c1u2e1f2c1s1c1i2c1u2c1r2c1r2e1r2c1q3c1u2c1u2c1w2c1r1e1r2c1t1c102c1s2e1w2c1s2e1v2c1s2c1f2c1p2c1r2c1t2d1t2c1q3c1p2c1s2c142c1s2c1r2c1s2e1o2c1u2c1q2c1p1c122c1q3e1s2c1r1e1v2c1p3e1o2c1u2c1v2c1s1c1s2c1q2e1w2c1r1d1o2c1q2e1x2c1u2c1u2c1r2d1o2c1s2d152c1t1e1j2c1q1e1i2c1u2e1t2c1s2c1p2c1s2c1q2c1t2e1y2c1r2e1c2c1s2c1s2c1r2e1y2c1q1e1e2c1t1e1o2c1r3c162c1s2c1w2c1q2c1t2c1q2e1p2c1s2c1w2c1q3c1k2c1s1d1p2c1s2c1k2c1q2c1o2c1t2c1y2c1p2c1v2c1s2e1t2c1q2e1o2c1r1e1o2c1r1c1y2c1r2e1p2c1t1c102c1q2c1v2c1s1e1x2c1t2e1h2c1q2e1u2c1u2c1q2c1r1e1q2c1r2e1j2c1s1e1k2c1s2e1v2c1t2d1p2c1r2e1b2c1r1e1s2c1u2c1w2c1r2c1w2c1u2c1p2c1r2e1h2c1s1c1z2c1u3e1k2c1q2c1p2c1u1d1y2c1r2e1t2c1q2e1s2c1s2c1d2c1r2c1q2c1s2c1s2c1s2e1t2c1q2e1v2c1t3e1q2c1r3e1t2c1u2c1t2c1s2c1x2c1s1e1c2c1u2e1f2c1r2e1c2c1s3c1y2c1r1e1w2c1p2e1s2c1t1e1i2c1s2c1h2c1u2c1t2c1p2e1d2c1s2e1t2c1u3c1o2c1r2c1h2c1t2e1p2c1s2e1p2c1q1c1t1e1v2c1s1c1u2c1s2e1z2c1t2c1r2c1r2c1x2c1u2c1t2c1q2c1j2c1q2e102c1s2e1v2c1s2e1s2c1t2e1t2c1r2c1t2c1q2e1j2c1t3c1w2c1s2d1s2c1u1c1q2c1r2d1q2c1r2c162c1s2e1w2c1q3c1w2c1s1c1d2c1s2e132c1r2c1x2c1u3c132c1r2e1t2c1u2c1j2c1s2e1s2c1q2e152c1t1c142c1r2e162c1u1e1t2c1s2c1f2c1s2e1x2c1u1c1q2c1q1c1v2c1t1c1t2c1q1c1q2c1q2d1s2c1u1c1i2c1r2c1w2c1u3e1u2c1r1c1q2c1q1e1v2c1s2c1x2c1q1c182c1s2c1t2c1r2d1x2c1r2c1w2c1t2c1u2c1r2e1r2c1s2e1p2c1s2d1h2c1q3e1h2c1s1c1f2c1r2e1w2c1t2e1q2c1s1c122c1r2e1s2c1t1c1t2c1s2d152c1t3e1p2c1q3c182c1q3e1v2c1s3c162c1r2e1y2c1t2e1x2c1s1e1y2c1s2e1w2c1s2c1y2c1s1e1d2c1u2e1j2c1s2c1x2c1q3e142c1s2c1f2c1r2d1r2c1s1c142c1q2e1t2c1s2d1e2c1s2c1q2c1r2d1q2c1u1e1y2c1r2e1q2c1s2c1x2c1u3c1f2c1q2c1d2c1t2c1y2c1q2c1j2c1s2c1h2c1u2e1y2c1r2c1p2c1u3e1y2c1s2c1r2c1s2c102c1s2c1p2c1s3e1f2c1t2e1j2c1q2c1j2c1q2c172c1u2d1g2c1s3c1w2c1s1c1y2c1r2c182c1r2e1r2c1t3e1y2c1r2c1w2c1t2c1y2c1q1c132c1r2e102c1t2e1j2c1q1c1h2c1s1c1j2c1s2c1q2c1s3e1k2c1t1e1f2c1s3c1u2c1t2c1j2c1s1e1q2c1r2c142c1u2e1i2c1p2e1y2c1t1c1s2c1r2e1c2c1q2c1w2c1t1e162c1q2c122c1u2e1s2c1q3e1i2c1q2c1c2c1u2d1t2c1s2d1p2c1u2c1g2c1q2e1x2c1q2e1s2c1u2e1p2c1s2e1q2c1r2d1u2c1r2e1d2c1q2c152c1t2e1v2c1r2d1k2c1s1c1f2c1q2e162c1q1c1h2c1s1e1r2c1q2c1d2c1t2e1k2c1s3c1d2c1r2c1v2c1t1c1a2c1q3c1d2c1u2e1w2c1r1d1u2c1s1c182c1t2c1j2c1s2d1p2c1t3c1h2c1q3d1u2c1r2c1s2c1s2c1x2c1s3c1x2c1u2c1j2c1q2c1w2c1s2c1k2c1u3e1x2c1s2c1x2c1t2e1f2c1s2e1w2c1s1c1v2c1t3c1y2c1q2c1s2c1s2e1u2c1s1e1q2c1s2e1z2c1u2e1x2c1p2e1t2c1u2c1z2c1s2d1u2c1q2c1r2c1u1c1q2c1p3e1k2c1s2c1z2c1p3c1y2c1s2c1y2c1t2c1q2c1p3e1k2c1u2e1p2c1r2e1f2c1r3c1w2c1u3c1q2c1q2d1k2c1u2c1j2c1s2c1i2c1r2e1p2c1u2c1y2c1s1c1p2c1u2c1x2c1p1c1j2c1p2e1j2c1t2c1r2c1r2c1p2c1t2c1t2c1q2e1q2c1s2c1z2c1s2e1q2c1s2d1w2c1s2c1t2c1r1c1j2c1p2e102c1t2c1r2c1r2c1r2c1s2e102c1r2e1h2c1s1c1v2c1t3c132c1p3e1k2c1s2c1t2c1q2e1h2c1r3c1j2c1t2e1k2c1q2c122c1s2e1r2c1q1e1t2c1r2d1s2c1s2e1d2c1q1c1h2c1s2c1w2c1s2c1q2c1q2d1g2c1s2e1p2c1p2e1d2c1s1d1x2c1q2e172c1q2e1r2c1s3c1j2c1r2d1p2c1u2c1h2c1s2e1d2c1r1c1x2c1t2c1r2c1s2e1k2c1u2c1w2c1q2c1k2c1s3e1y2c1t3c1p2c1q3e1d2c1s2d1p2c1s2e1q2c1q1c1z2c1t2c1j2c1q2e1k2c1u3c1j2c1r2c1p2c1r2e1x2c1u2c1w2c1q3c1d2c1t1e1f2c1r2e122c1r2c152c1u2e1d2c1r2d1b2c1u1c162c1s2e1q2c1r3e1z2c1t2e1y2c1s2e1s2c1s3e1f2c1q2e1b2c1q2e1o2c1u3e1x2c1r2c1p2c1t3e1x2c1s1c1w2c1s2c1u2c1s2e1y2c1s3c1v2c1u1e1z2c1r2c1q2c1q2e102c1u3e1u2c1r2d1w2c1t2d1w2c1q1c1d2c1s1c152c1u2e1q2c1r2c1y2c1u2c1f2c1q2d122c1s1c142c1u3e1f2c1s2d1r2c1s1c1y2c1s2d1c2c1r2e1i2c1t1c1j2c1s2e1v2c1t2c1p2c1s2d1y2c1s2c1o2c1t2e1o2c1q2e1y2c1t3c1v2c1r2e1q2c1q1e1o2c1s3e1r2c1s1e1v2c1u2c1r2c1s2e1y2c1r2e1r2c1s2e1x2c1s3e1w2c1t2d102c1s2c1y2c1s2c1p2c1t3d142c1q2c1u2c1s1c162c1r2e1j2c1q2c182c1t1c1j2c1s2c162c1u2c1k2c1r2d1r2c1s1d102c1s2c1c2c1p1e1e2c1u2e1v2c1s2c1r2c1r1c1w2c1u2e1s2c1s1e1r2c1u3c1v2c1q2c1j2c1q1e152c1s1c122c1q2e1y2c1u2c1y2c1s2e1k2c1s1e1s2c1u2c1u2c1r3c122c1s2e1w2c1s1c122c1q2e1s2c1s1e1r2c1q2e1r2c1u2e102c1r2c1q2c1p2c1s2c1t2e1r2c1r1c1d2c1s1c1f2c1q3c1s2c1q2d1h2c1s1e1d2c1q2d1o2c1s2d1i2c1r2c1e2c1s1c1w2c1u2e1q2c1p2d1k2c1t1e1t2c1r2e1x2c1q2c1z2c1r1c1a2c1r2c1s2c1t2d1s2c1s1e1r2c1r2e1w2c1r2c1i2c1s2d1h2c1u1c1x2c1q2e1s2c1s2e1u2c1u2c1x2c1q2e132c1s2e1y2c1s2e1c2c1r2e142c1t3c1h2c1r2e1x2c1u3e1o2c1s2e1q2c1r2c1h2c1t2c1r2c1s1e1y2c1u3e102c1q2c1q2c1s2e142c1u2c1c2c1q2c1w2c1t3e1v2c1s2e1p2c1r2c1t2c1u3c1d2c1s3d1j2c1t2c1f2c1r3e1x2c1p2e1t2c1r3c1c2c1p1e1s2c1u2e1z2c1s3c1x2c1r1c1v2c1s1c132c1s2c1o2c1u2e1o2c1s1c122c1s2e1y2c1s1e1t2c1s2c1w2c1t1e1j2c1r2c1v2c1r2c1r2c1t3e1x2c1r2c1j2c1u1e1i2c1s2e1q2c1s2e1t2c1u2e1t2c1s2e1v2c1t3e1q2c1s3e1r2c1s3d1r2c1t1c1g2c1r2d1p2c1t1e1v2c1r2c1u2c1r2c102c1u3e1y2c1r2e1r2c1f3c1v2c1v2c172c10121p1r1f1i1s1h1f1d2t1b121m','06a222933333w331w371g25202o193x3c1b3o00111m252z3o2o252c2o2m2y23381e23211g2c29361c2v3s1z3z1o360w1z3z3b213v2z39381a2v3s1z311m2z162t312n1z2038251q25333c162z2v233c1y3s271z1z3a231q25333e142z261w121z141z133x392o172z361s3s2t2z3p1z3u243c153v392o172134101z1m251z3u261z3w261z3u26113u2o2z39233v2c29213x29213v2520393v2c1z112233143o02302c293w141m2c1b3o013z2k221z311m2z1z1z3u271z2z1d3b3v2c181w12302v3u2s353c101z1c1o1z133v27231t302o12252520332c1826332z1d1g182c143z281w1z101z323s271z101o3s350z3z243314331g1v3d1o1e1k1f1f1c1o3d1j2e1q3d1f3g183e1i2e1i1c1h2d1e3e1s3d1i2c1t3c1z2c1u2g1y2c1r2c1y2c1s3d1k2e1s2c162c1s3c1r2c1u2e1q2c1r1c1g2c1u2c142e1u2c1x2c1s2c1b2c1u2g1e2c1r3e1j2c1s2c1u2e1s1e122c1u2e1r2c1s2e1z2c1s2c1g2c1u3c1t2e1u2e1u2c1t3c1t2c1u2g1g2c1r2c1x2c1u2d1y2e1u2c162c1s2e1x2c1u2g1b2c1q1d162c1u3e1v2e1s2d172c1s3d192c1s1f182c1q3d1z2c1s3d192e1s3c1g2c1s2d172c1u3f142c1q2d172c1t3d1o2e1s2d172c1u3d142c1s3f192c1s3c1c2c1s2d172e1u3d1b2c1s3d172c1t3f1c2c1q1d172c1s3e1b2e1s2d152c1t3d1z2c1s3f162c1s3e1a2c1s2d182e1u3e1t2c1s3d172c1s3g192c1q3d1u2c1s2c1u2e1f1c1f3d1g1e1g3e1u1g141e1q2e1d1c1i1d121g143d1e2c1g1c1s2e1q3g1c3c1h3c1f2d1b1d1j2f183e101c191d1c1e1g3f1g2c1d3d1s3e1k1c1o1e1i1e1f1d1c1c1h1c1b1f1k3e163d1f3c1a1d1g3g141d1f1c121c1a1c1a1e1a1c183d1m1e1s2d1b1f1b1d1k3d1f1d1g1e1d1g1p3c102c141e101c1c3f1c3e1i1d1t2e1s2c1d1f1a3e1q1c1s3c1g3d1e3g141d1g1e1s1d1g1c1u1g1h3d1a1c1f1e1k1c123g1c3d1e1e1u3c1s2c1s2e1o2c1q3c1u2c1t1c1f2e1s1c1i2c1s3c182c1t1e1z2c1s2e1f2c1u3e1s2e1s2e1k2c1u2c1o2c1r2e1r2c1r2e1d2c1s1c1s2e1s2c1u2c1t3d1s2c1s1e1w2c1s1e1t2c1t3c1x2e1t2d1x2c1s2c1w2c1t2g1p2c1q1e1m2c1r2e1v2e1s1c1q2c1u3c1w2c1u2g1u2c1p3e1y2c1t1c1t2e1u2d1p2c1s2e102c1u3f1y2c1q2e1i2c1t2e1o2e1u2e1x2c1u2e1c2c1t3f1o2c1s2e102c1t2d152e1u1e1t2c1u2c1s2c1u1g1c2c1r3e1s2c1u1c1s2e1t2c1i2c1t3c1z2c1s1e1w2c1s2c1r2c1s1e1z2e1t2c1q2c1t2c1u2c1u2g1o2c1r1e1z2c1t2c1h2e1u2c1v2c1u2c102c1t2f162c1s1c1l2c1u2c1s2e1u2e1o2c1t2c1o2c1t3e1z2c1q3e102c1t1c142e1s1d1s2c1r2c1s2c1t2e1v2c1q3e182c1u3e1p2e1t2c182c1s2c1w2c1u2g1s2c1r2c1r2c1t1e1s2e1u1c142c1u3c142c1u3e1s2c1r3c1q2c1t3e1k2e1s2c1d2c1u3e1u2c1u2e1r2c1q3c1j2c1u3c162e1u2c1t2c1t1c102c1t1g1v2c1r3c1t2c1u3c1z2e1s2c132c1t3c1z2c1u3f1i2c1s3c1y2c1u2c102e1u2c1u2c1u2e1z2c1u2e102c1s2e1u2c1s2e1d2e1s3c1p2c1t2c1y2c1s1g1v2c1q2c1t2c1s1e1x2e1s1c1y2c1s1e1p2c1t2g1p2c1r1d1t2c1t1d172e1u2d1s2c1t3e1h2c1s2g1z2c1r2d1f2c1s1e1r2e1r2e1w2c1u2e1s2c1u2g152c1r1c102c1s3c1w2e1t1e1q2c1t1e1r2c1s1g1w2c1q1c1j2c1t2e182e1t2e132c1s3e1w2c1u1e152c1s3c1h2c1u2e1h2e1t2c1p2c1s3e1z2c1t1f1u2c1r2e1j2c1s3c1i2e1u2c1j2c1t2c1p2c1u2e1t2c1s2e152c1u2d1w2e1u3e1j2c1u1c102c1t3e1s2c1r1e1i2c1t2c1h2e1t2c1e2c1u2c1v2c1t2e1j2c1s1e1z2c1s2c1u2e1t1e1h2c1t2e1y2c1u2g1v2c1r2e1q2c1s1e1b2e1u2c162c1u1d152c1t2e1h2c1q1d1d2c1t2d1p2e1t2c1s2c1u3c142c1t1g1x2c1s2c102c1s2c1z2e1u3e1f2c1s2c172c1u2e1z2c1q3e1y2c1t2c1j2e1t2d1f2c1u1e102c1s2f142c1s2e1y2c1t3c1r2e1t2c1j2c1s2e1c2c1t2e1p2c1s3c102c1t2c1o2e1t1c1r2c1u2e1o2c1u2g1r2c1q3c1v2c1t1e1v2e1t1c1r2c1s3e1v2c1t1e1v2c1s2e162c1t2c152e1u1e1j2c1r2c1u2c1t2g1w2c1r2c1f2c1t2e1p2e1u2c162c1t2c102c1t2g1t2c1q2e1j2c1t1c1z2e1s1c1x2c1r2c1z2c1s2g1v2c1s2c1j2c1t2e1v2e1s2e1j2c1u2d1u2c1s2f1r2c1q2e1t2c1s1c1z2e1r1c1x2c1s3e1v2c1u1g1g2c1s3e1y2c1t1e1g2e1t1c1r2c1u2c1z2c1t3g1k2c1s1d1g2c1u1d1r2e1s2e142c1u3e1h2c1u1f1z2c1q2e172c1s1e1s2e1u2c1j2c1t1e1z2c1t3f1t2c1s3e1f2c1u3e1u2e1u2c1x2c1t3c1j2c1u1e1v2c1r3e1i2c1u1d1c2e1t1e1t2c1u3e1r2c1t2e142c1s2c1j2c1t1c1z2e1s2e1v2c1t3c1y2c1t2g1p2c1s2d1t2c1u2e1h2e1u1e122c1t2e1y2c1t2e1y2c1r2c1x2c1u2d1u2e1t2c1h2c1s3c1w2c1s1g1r2c1r2d1s2c1s3c1x2e1u2d1j2c1u2c152c1s2g1s2c1r2e1j2c1t2e1r2e1s1c1q2c1u3d1v2c1s2g1r2c1r1c1r2c1u2c1d2e1t2e1j2c1s3c1j2c1s3g1b2c1q3e1j2c1r3e1d2e1t3e1r2c1u3e1r2c1s2f1x2c1r3c1h2c1u1e142e1u2c1u2c1t2e1h2c1t2g1h2c1r1e1s2c1u3c1s2e1u2c1k2c1u3c1r2c1u2f102c1r3c1y2c1t2e1h2e1u1c1w2c1t3e1w2c1s3g1u2c1s2c1v2c1t2c1k2e1t2c1p2c1u1c1w2c1u3f1y2c1q2e1t2c1u1c1x2e1t2c1u2c1r2e1h2c1r2g1o2c1r2d1w2c1u2e1z2e1t1c132c1t2d1h2c1u1e1z2c1s3e1g2c1u2c1a2e1t2c1k2c1t3d162c1s2e1y2c1q1c162c1t2e1o2e1s2c162c1t1c1o2c1t2e1k2c1r2e1s2c1u2c102e1r3e132c1t3e1h2c1t1g152c1r1e1f2c1u2e1s2e1t2e1s2c1t3e1u2c1u1e1v2c1q3c1t2c1u3c1h2e1s2c1x2c1r2e1v2c1s2g1o2c1r1c1y2c1s2c1x2e1u2e132c1u3e1v2c1t1e1f2c1r2c1z2c1t3e1y2e1u1c1q2c1u3c102c1t2g152c1s2e1r2c1r2e1s2e1s1d152c1t3d1h2c1t2g1h2c1s1e1f2c1r3e1h2e1t2c1w2c1s2d1c2c1s2e1h2c1q2c1t2c1u2e1r2e1t1c1s2c1u3c1u2c1t3e1y2c1r3e152c1u3e1o2e1u2c1t2c1r1c1q2c1t1e1z2c1r3d1y2c1u2e102e1u2c1u2c1u2c1z2c1s2e1q2c1r2c1s2c1t2c1j2e1u2c1x2c1t2e1j2c1s2f1t2c1s2c1m2c1t2e1x2e1u2d1w2c1u3e1u2c1t2g1x2c1s3c1v2c1t2e1u2e1r2e1w2c1u2c1w2c1s3e1k2c1r2e1t2c1s1c1e2e1t2d1r2c1t3c152c1t3g1k2c1p2c1i2c1t2e1w2e1u3c1y2c1t2c1w2c1t2g1w2c1p3e1y2c1s3c1o2e1t1e132c1t2c1k2c1s3e1t2c1s2c1u2c1u2e1s2e1u2d1s2c1t2e1u2c1u1g1q2c1s2c1f2c1t2c1u2e1s2e1y2c1t2e1j2c1u2g1w2c1q2c1w2c1t2c1w2e1r2d1j2c1u3c142c1t3g1s2c1s2e182c1u2c1u2e1s2e1j2c1u1c1x2c1s1g1v2c1s1c1w2c1s2d1o2e1s1c132c1t3c1x2c1u3f1u2c1q3c1w2c1u2e1o2e1s2e1j2c1t2e1s2c1r2e1p2c1p3e102c1u2e1s2e1t1c1b2c1t2e162c1u1g1x2c1r2e1t2c1t3c1h2e1t1e1h2c1f3c1t2c1t2e1t3e1f2c1t2e1q2c1s2e182c1s3e1v2c1u2e1t2e1u2e1i2c1u1e1h2c1s1g1r2c1r3c1y2c1r1e1x2e1s2e1o2c1t2c1j2c1u1g102c1r2e1x2c1t2c1t2e1s2c1y2c1t2e1a2c1t3e1j2c1s2e152c1t2d1q2e1u2c1w2c1u2d1a2c1u2e1y2c1r3c1y2c1s1e1p2e1t2e1s2c1u2e1i2c1t2g1v2c1s3d1r2c1t3c1t2e1s2e1a2c1u1c1s2c1t2e1h2c1r1c1v2c1t1e1k2e1t2c1i2c1r3c142c1t2e1z2c1q2c1m2c1s2c1t2e1t1c1o2c1t3c182c1t1g1o2c1r1c1w2c1u2c1v2e1u2e1o2c1s1d1u2c1u3e1v2c1p3e1h2c1u2e1p2e1u2e1u2c1u2c1t2c1s3g1r2c1p2e1z2c1s2c1w2e1t2d1t2c1s2d1t2c1t1e102c1s3d1e2c1s1e1t2e1s1e1s2c1u2c1j2c1s2e1w2c1s2c1s2c1u1e152e1t2c1i2c1u1c1y2c1u3e1k2c1r2e1s2c1s1d1y2e1u3e1s2c1u3e1u2c1t2g1w2c1r1c1x2c1t1e1p2e1t3e142c1u3c1r2c1u3e1s2c1q2c142c1t2e1j2e1s2c1s2c1t3c1q2c1s2e1v2c1r3c1h2c1u2e1j2e1r2c1r2c1u3d1k2c1r2g1v2c1r2c102c1u1c1f2e1s1e132c1u3c1f2c1u1e1i2c1q2c1u2c1s2c1t2e1u2d132c1s1c1u2c1u3g1r2c1s3c102c1s3e1w2e1u2c1k2c1s1c1k2c1s2g1t2c1s2e1s2c1s1c1p2e1t3c132c1t3c1x2c1u3e1t2c1r2e1s2c1t1d1s2e1u2e1s2c1u2e102c1s1g1t2c1q1c1v2c1u1e1j2e1t1e1w2c1u3c1t2c1u1e1y2c1r3c1z2c1t2c102e1u1d1r2c1u1c1z2c1t2f1h2c1r3c1l2c1u1c1x2e1u3e1p2c1u2c1j2c1t3g1t2c1s3c102c1r3e1j2e1u2c1q2c1u1e1t2c1r3e1u2c1s2e1u2c1s3c1w2e1r3c1j2c1u1e1y2c1u2f1w2c1r2e1a2c1t2c152e1r1c1o2c1t1d1t2c1t2e1f2c1r2c1f2c1t2d1k2e1u2e1d2c1r1c1x2c1s1e1j2c1s2e1k2c1u1c1t2e1t2c1o2c1t3c1r2c1u3f1y2c1q3e1r2c1u1e1u2e1u2e1r2c1u2e1t2c1u3g1x2c1s2e1s2c1u2e1p2e1u2c1g2c1s2e1v2c1s1e1i2c1s2c1u2c1s1c1r2e1s2d122c1t2d1g2c1s2g152c1s3e1s2c1u1d1r2e1t1e1t2c1t2c1v2c1s3g1p2c1q2c1k2c1u1c1x2e1u2c1d2c1u3c1f2c1t2e1w2c1s3c1v2c1u1c1t2e1u1e1y2c1t2d1i2c1r2e1y2c1s3c1l2c1u1c1x2e1u1d1q2c1s2e1w2c1u2e1k2c1r2e1z2c1u2c1q2e1u1e1r2c1u2e1y2c1t2g102c1q3e1r2c1s2c1i2e1t1e1v2c1u2e1j2c1u2e1z2c1s2c142c1s2e1f2e1u2d1k2c1s2e1t2c1u2f142c1r2c1v2c1u1c1p2e1t2e1v2c1u2d1q2c1u2e1z2c1q2e1h2c1u2e1f2e1u1d1v2c1s2e172c1s1g1t2c1s3c1v2c1u2c1t2e1s1c1v2c1u2e1x2c1u2e1x2c1r1e1i2c1t2c1i2e1r2e1w2c1s2c1c2c1t3g1x2c1r2e1x2c1t1e1y2e1s2e1r2c1t2e1t2c1t2g1f2c1r1e1s2c1s2e1t2e1t2d1o2c1s2c1j2c1u1g1i2c1p2c1y2c1s1e1x2e1r3e1s2c1t2d1y2c1s2g1z2c1q1e1m2c1s2c1y2e1u1d1e2c1u1e1t2c1s2g1y2c1s2c1v2c1u2e102e1s1e1r2c1t1c1u2c1u2g1v2c1r3c1w2c1s2c1f2e1u2d1t2c1t2e1a2c1t1e1k2c1s3e1r2c1s2e1z2e1t1e1w2c1u3e1i2c1u2g1x2c1r1c1z2c1s2c182e1t3e1p2c1s2c1w2c1s2g1v2c1s3e1r2c1s2d142e1s2e1f2c1s1e1j2c1s3e1h2c1q2e1l2c1u2c1c2e1s1c1p2c1u2e102c1u2g102c1s1e1h2c1t1c182e1u2c1w2c1u2c102c1s2g1r2c1q3c1w2c1s2c1w2e1t1e1v2c1s2e152c1t2g102c1q3d172c1r2c1y2e1u1e1o2c1t2c1x2c1u2e1u2c1q2d1w2c1t2c1t2e1s1c1f2c1t1d1u2c1t2e1j2c1q1e1s2c1u3e1f2e1u2c1w2c1u2c1y2c1t2e1q2c1q2c1y2c1s1e1z2e1t2c1s2c1t1c1p2c1s2e1f2c1r3e1z2c1r2d1u2e1t1e1y2c1s3c1z2c1u1e1w2c1q3e152c1t2e1j2e1u3e1y2c1u3e1x2c1u2e1r2c1s2e102c1t2e1p2e1s2e1v2c1u3e1y2c1t1e102c1s3c1t2c1u3e1x2e1u2c1t2c1s1e102c1t2g1h2c1r3e1t2c1u1e1u2e1s2c1t2c1s1c1p2c1s2g1x2c1r2e1x2c1u2c1w2e1t2c1r2c1t2c152c1t2e1q2c1r3e1r2c1t1c1t2e1r2c1p2c1t3c102c1t2e1j2c1q3c1u2c1t2e1x2e1t2c1f2c1u1c1p2c1s1e1y2c1p1d1t2c1u2d1p2e1u2e1h2c1t1c102c1r2e1t2c1r1e1t2c1t1e1r2e1u2e1r2c1u1e1w2c1t1e1x2c1r1c152c1u2c1y2e1u2c1e2c1s1c1p2c1u2g1k2c1r1e1t2c1t2e1z2e1t1e1r2c1r1e1g2c1t2e1u2c1r2c1t2c1u2e182e1t2e1r2c1s2e1x2c1t2g1x2c1p1c1s2c1t1e1q2e1s2e1x2c1u2c1d2c1t1g102c1r1e1f2c1u3c1h2e1s2e1v2c1u2e1z2c1u2e1s2c1r2e152c1s2e1x2e1s2e1y2c1u1e1r2c1s1g102c1r1e102c1u1c1y2e1u1e1x2c1r2e1y2c1s2g1h2c1r2e142c1s2e1q2e1r1e1f2c1u3d1q2c1u3g1x2c1s1c1v2c1u2d1f2e1s3e1h2c1u2c1p2c1t1g1j2c1q3c1y2c1t1c1q2e1u1e1t2c1s1c1j2c1t2e1t2c1q2c1s2c1s2c1f2e1r1e1q2c1u2d1s2c1t2e1j2c1q2c1s2c1t3e1w2e1u2c1s2c1s1c1t2c1u2g1f2c1q2c1s2c1s3e1r2e1u2c1f2c1s2e1u2c1u2e1p2c1s2e1l2c1u1e1w2e1s3e1w2c1u3c1u2c1t2f1f2c1s1e162c1t1e1y2e1u2e1r2c1t3c1q2c1s1g142c1r3c172c182c1s2e1r2c1r2e152c1t2e152e1t2c1h2c1t3c1f2c1s2g1w2c1r1c1w2c1u3c1s2e1r2c1v2c1t3c1y2c1s2e152c1r1c162c1t2e1a2e1u1e1r2c1u2c1f2c1t2e1y2c1s2e1x2c1u1e1p2e1t2c1i2c1s3c142c1t1f1v2c1q3e1h2c1s3e1v2e1r2e1y2c1s1c1t2c1t2e1w2c1r2e1v2c1u2c1o2e1t2e1s2c1s3c1x2c1s1g1s2c1r2d1w2c1s2c1h2e1s2c1q2c1s3e1q2c1s2f1r2c1q2c1x2c1u2c1h2e1u2e1t2c1t2c1u2c1u1e1v2c1q3e1v2c1t2e1s2e1t2c1v2c1s2d1h2c1t2g142c1r1e1e2c1t2e1s2e1u3c1e2c1t3c1j2c1u2g102c1r2e1z2c1u2c1q2e1u2e1w2c1u2e1h2c1u3e1v2c1q2e1w2c1t1e1s2e1s3c1v2c1t2d1z2c1s3f1b2c1r2d1c2c1t2c1c2e1t2c1d2c1u2e1y2c1t1e102c1s1c1r2c1t2e1s2e1t1d1e2c1u3e1y2c1u1g102c1r1e1r2c1u1e1h2e1t3c1r2c1u2d1u2c1s2e1s2c1q3e1u2c1t3c1h2e1u1c1w2c1s3e1p2c1u3g1j2c1r2e1l2c1s2c1o2e1s2c132c1u2e1f2c1u2f1s2c1s2c1q2c1t2c1w2e1s2c1w2c1t3c1y2c1s2g1s2c1q3e1v2c1t2e1f2e1t2e1w2c1u2c1t2c1u1g172c1s1c1l2c1t2e1x2e1t1c1p2c1s2d1j2c1t2g1o2c1q2c1w2c1u3c1o2e1t2e1d2c1u2c1y2c1t2e1u2c1q2d1l2c1t3c1o2e1u1c1w2c1t1d152c1u2e1p2c1s1e1s2c1t1e102e1t2c1r2c1u1e1h2c1t1e1y2c1s2c1e2c1s2e152e1t2d1r2c1u2e1c2c1t2e1z2c1s1c1v2c1t2c1t2e1u2c1h2c1s1e1v2c1t3e1v2c1s2d1v2c1s2c1r2e1t1e1d2c1t2e1r2c1s2f1k2c1s2c102c1t1c102e1s2c1i2c1u2c1j2c1t2e102c1q2e1i2c1t3c1s2e1s2e1a2c1u2e152c1u1f1w2c1r3c1l2c1u1e1o2e1s2c1e2c1u2e1t2c1t2g1p2c1r1e1j2c1t2c1s2e1s2e1i2c1t2e1y2c1u1g1j2c1s2c1u2c1u3c1o2e1u1e1x2c1s1c1w2c1u2e102c1r1c1a2c1s2e1u2e1t2c1x2c1u3c1w2c1u1g1s2c1r2d152c1u2c1f2e1u3e1p2c1u2c1s2c1s1e1z2c1s2e1v2c1s1e102e1u1c1v2c1u3d1u2c1u2e1o2c1s2e1l2c1u2d152e1t2c1h2c1s1c1x2c1u1g1s2c1s2e1q2c1r2e1h2e1s1e1v2c1t2d1t2c1s1e1v2c1q1e1w2c1t2e1j2e1u1e1v2c1t3e1v2c1u1g102c1s1c1u2c1t3e1p2e1r2e1u2c1u3d1q2c1t2e1h2c1r3c1h2c1s1c1h2e1t1c1h2c1s1c1r2c1u1f1z2c1s2c1s2c1s3c152e1t1c1d2c1t2e1w2c1s2g1i2c1r1e1h2c1s3c1i2e1t1e1h2c1t2c1y2c1s2e1z2c1s2c1s2c1t3c1h2e1t1e1u2c1s2e1g2c1t2e1k2c1p2e102c1s2c1b2e1t3e1v2c1t2c1t2c1s1e1o2c1p2e1s2c1r2e1s2e1t2e1e2c1s3c162c1s2g1v2c1s3c1z2c1s2d1s2e1s2e1s2c1u2c1y2c1r1g1r2c1r1c1z2c1s1c1z2e1r1c1v2c1s3e1t2c1u2e1o2c1r2e1v2c1s3c1o2e1u2e1f2c1u3c1y2c1r2g142c1q1d102c1r2e1q2e1r1e1d2c1u3c1k2c1t2f1u2c1r1e1j2c1s1c1p2e1s1d1k2c1u2c1o2c1s1g1w2c1q1c1s2c1u2c1h2e1u3d1o2c1s3c182c1t2g1h2c1q2d1s2c1t3e1w2e1t1c1s2c1u3c1q2c1t2e102c1s1e142c1u2e1t2e1s2c1r2c1s2e1s2c1u1g1s2c1r2c162c1t1e152e1r2c1h2c1u2c1c2c1u2g1z2c1q2d1j2c1u3e1r2e1s2d122c1t3c142c1u3f1o2c1q3e1k2c1u3c1s2e1u2c1w2c1t1e1z2c1u2f102c1s3c1t2c1s2e1w2e1u2e1h2c1t2d1j2c1t1g1v2c1s2e1b2c1u1c142e1t1e142c1u1c1f2c1t3g102c1r3c1z2c1u2d1s2e1u2e1h2c1t3c1t2c1u1g1o2c1s2e102c1t3e1r2e1t2d1q2c1t3d1f2c1u1g1z2c1s1e102c1t1e152e1t3c1o2c1u1e102c1t1g1h2c1s1e1s2c1u1e1v2e1t2e1u2c1t2c1z2c1s2g1r2c1q2e1z2c1u3e1j2e1t1e142c1s3c1t2c1u1e1s2c1r1e1h2c1s1c1k2e1r3e182c1t2e1j2c1s2e1z2c1r2e1s2c1u1e152e1u3e1i2c1s1d1v2c1s1e1k2c1q3c1t2c1r2e1h2e1u2e1h2c1u3c1r2c1u2e1r2c1q2d1w2c1u3c1s2e1t2e1g2c1u2c1t2c1u1e102c1r3e1j2c1u1e1w2e1t2c162c1t1d1y2c1u1g1o2c1r1e142c1t3e1r2e1t1d1b2c1t1c1o2c1s2e1g2c1r3c1y2c1s2c102e1s2e1p2c1s3d1u2c1u2g102c1r2e1c2c1t2c1t2e1s3c1r2c1u1e1t2c1u1g1x2c1s2c1w2c1s2c1s2e1s2e1r2c1t3c1p2c1u2g102c1q3c1k2c1u3c1s2e1t3c1d2c1u3c102c1t2g102c1s2e142c1s2c1z2e1r1e1w2c1u2c1z2c1u2g1r2c1r2e1j2c1t2e1k2e1t1c1u2c1s2c1u2c1t2e1r2c1r2c1l2c1t2c1t2e1t2c1o2c1u2d1x2c1u2g1o2c1r2e1v2c1u2c1o2e1u2c1y2c1r2e1v2c1t2g1o2c1q2e1s2c1u2e142e1s2e1p2c1u3c102c1u1g102c1s3e1s2c1u2d1o2e1u2e162c1t2e1c2c1r1f152c1s3c1y2c1u2e1t2e1t2e1y2c1t2e1z2c1u2e142c1s2e1u2c1s2c1z2e1t1e1q2c1t3c1z2c1t2e1y2c1r2c142c1t2c1k2e1u2e1r2c1u1c1z2c1t2e1r2c1s2e1m2c1u2e102e1u2c1d2c1s2e1t2c1u3g1s2c1r3e1l2c1u1c1s2e1t2c1y2c1t2c1y2c1s2e1h2c1s2e152c1s3d1i2e1t2e1i2c1r2e1q2c1r2g1v2c1r2c1v2c1u2c1r2e1r2e1d2c1s1c1o2c1s1e1s2c1r2e1e2c1t3e1j2e1u3d1j2c1s3d1k2c1t2f1u2d122d1h122q223c161c1k3e1e2g1c3d142c1i3d1a1e1e1f1q1e1j1c123e1c1c1p3g142c1u2e1r2c1s2c1x2e1u2c1g2c1u3c1t2c1s3g1w2c1t3c1t2c1u2e1e2e1t2c1x2c1u2d1y2c1s2e182c1s2e1x2c1u2e192e1s1d162c1s2c1z2c1q1g1g2c1u1c1u2c1t2c1i2e1u2c162c1s2e1p2c1q1f192c1u2e1m2c1u2e1v2e1s2e1y2c1s3d102c1q3e1w2c1s1d1k2c1r2e1t2e1t3e1g2c1s1d192c1s3g182c1s3d192c1t3e142e1s3d172c1u3d1c2c1q2f172c1u3e1g2c1s3d172e1u3d1d2c1s3d182c1s3g1b2c1s3d172c1s3d152e1s2d172c1u3c1a2c1q3f182c1s3d1a2c1s3d162e1s3d1a2c1s1d172c1r3f1b2c1s3d192c1s3d132e1s2d172c1u3e1w2c1q1f172c1s3d1e2c1s1d152e1s3c1z2c1s2c1w2c1i1e123d1o1e1k1d141e101g141e1s2e1f3d141e1y3g1i1d1d3c1d1d161e1d1f1b1d1q3d1f3e1g3d1e1e1d1c1c1c1f1e1p3c1d1e183d131e1h2c1b2d1i1f1c1c1g2c1s1e1j3e1b1e1j3c1c2d1b3d1j1d161e122c192d1b1d1b2d192f1b3c181c1d3d183d133e1i1d1s3d1f1e1c1e1d1e1c3c1b1c191d1r1e1q1g123c1u1d143d1c3d151g1h1d1s2d1j2e1p1c183g181d1p3e1d1c1h1c1d1e1g2c1c1e1h2c1i2e1d3f1f2c1v2c1w2c1u2c1p2e1t2c1s2c1t2e1f2c1r2e1h2c1t2c1e2c1t2c1h2e1t1c1u2c1u1e1r2c1r1e1k2c1t2c1x2c1t2c1h2e1r1c1s2c1u2d1u2c1s3e102c1r3c1m2c1t2e1w2e1s2c1v2c1t2e1f2c1r3e1s2c1s2e1d2c1s1c1v2e1t1c1v2c1s1c1p2c1r2e1w2c1s2c1j2c1s2e1q2e1s1e1z2c1s3c1k2c1s3e1x2c1t1c102c1t3c1j2e1u1e1v2c1s1c1u2c1s1g1v2c1t2c1w2c1s3e1f2e1s1e1s2c1s3c1t2c1q1f1j2c1r2e1z2c1t2c1d2e1s2c1s2c1u3c1q2c1q2g1f2c1u2d1i2c1u2c1q2e1t2d1o2c1u2c142c1r3f1o2c1t3c102c1u2e1f2e1s1c1z2c1t2c1y2c1r3e102c1u2e1a2c1s3c1a2e1t2d1i2c1u2c1y2c1s1f1q2c1u2e1l2c1s2c1u2e1s1c1q2c1s2c1i2c1r3e1a2c1t3c1s2c1u2e1x2e1t1e1r2c1u1e1f2c1r3e1v2c1u2d1w2c1s2c1q2e1s2e1u2c1u2d1g2c1s2e182c1t3c142c1u2e1u2e1s2c1r2c1u1e1u2c1s2f1v2c1s2d1u2c1u2c1p2e1u2c1w2c1s3c1o2c1s2e1s2c1t2c1z2c1s1c1x2e1t2e1o2c1s2c1u2c1r3e1s2c1s2c1x2c1t3c1f2e1u2e1o2c1s2e1o2c1r2g1u2c1u1c102c1u3c1u2e1u1c1o2c1s1c1f2c1r3e102c1t2c1h2c1t2e1v2e1u2e102c1u1e1f2c1r2e1z2c1t2d1j2c1t2e1u2e1t3c1q2c1t3c1w2c1r3g1p2c1t1e1y2c1u2e1y2e1t3c1o2c1s1e1k2c1q1g142c1u2c1q2c1r2d1y2e1t2e102c1t2e1j2c1q2g1a2c1t1e1i2c1u2e1x2e1s2e1p2c1s1c1x2c1q2f1v2c1s2e1s2c1s2d1s2e1s2c1f2c1u1e1h2c1s2e1i2c1r1c162c1t3c1t2e1t1c1b2c1s2e102c1r2e1v2c1s2e1k2c1t2e1v2e1s1c1q2c1u3c1t2c1q2g102c1u3c1w2c1s3e1c2e1r1e152c1s2e1f2c1q3g1w2c1t2e1s2c1t2e1j2e1t1c1f2c1u2c1d2c1r1g1o2c1t1e142c1u2e1x2e1u1c102c1t1c1u2c1s3f152c1t3d102c1s3e1p2e1u3e1w2c1u3e1i2c1r2g1u2c1t3c1c2c1s1c1f2e1t2e1u2c1u2e1t2c1r2e1u2c1t2c1u2c1t3d122e1u1e162c1s2c1u2c1q3f172c1t1c182c1t3e1y2e1s1c1v2c1t2e1f2c1s2e1w2c1t2c1z2c1u2c162e1t2c1r2c1u2e1z2c1r2e1j2c1s1c1g2c1u1e1u2e1u2c1h2c1u1d142c1r2e1j2c1u2e1s2c1t2c132e1s1c1p2c1t2c1p2c1s2g102c1u2e1m2c1u1c1j2e1t2e1w2c1u1e1i2c1s2g152c1t2c102c1s2e1y2e1u1e142c1r2e1q2c1p3g1s2c1t2e1i2c1s2d1i2e1r2e1v2c1s1d1i2c1r2e1h2c1u3c1h2c1t3c1y2e1u1e1s2c1r2e1q2c1r2g1i2c1s1d1s2c1u2c1p2e1t2c1z2c1s1e1q2c1r2e1j2c1s2e1g2c1u2e1p2e1u3e1r2c1u3c1j2c1q1e1g2c1t1e1h2c1r3e1u2e1u1e1z2c1u1e1t2c1r3e102c1s2e1t2c1t3e1i2e1u1d1i2c1u1d1p2c1q3g162c1s3e1z2c1r3e1p2e1s1d1h2c1s3e1x2c1r1e1z2c1u2d1r2c1t2e1t2e1t2e1t2c1u2e1p2c1s1e102c1t2e1r2c1s2e1q2e1t3e1v2c1s1e1u2c1q1e1z2c1t1e1h2c1t3c142e1s2d102c1t3c1w2c1r2e1v2c1r2c1k2c1t1c122e1u3c1o2c1t3c1f2c1r3g1t2c1u3e1q2c1t1d1s2e1t1e1t2c1t2e1v2c1s3e1x2c1u3d102c1u2c1o2e1t2c1s2c1t2d1r2c1r1f172c1t2e1s2c1s1c1s2e1r2c1u2c1u1d142c1q1g1q2c1r2c1w2c1t3e132e1s2e1v2c1u2c1x2c1r2g1s2c1t1c1y2c1t1c1q2e1s1c1h2c1r2e1x2c1s3f1j2c1u2c1l2c1u3e1x2e1t2e1z2c1u2d1f2c1s2g102c1t1c1k2c1t2e1k2e1t2e1z2c1u2d1t2c1s2e102c1u2e1a2c1s3c1y2e1t1d1h2c1t2e1o2c1r2f1s2c1u1e172c1u2d1q2e1t3c1i2c1u1c1j2c1q2g1s2c1u3c1r2c1t2c1w2e1u2d1z2c1u2c1f2c1r2e1k2c1t3c152c1t2c1u2e1t2e102c1t2c1q2c1q3g1h2c1t3c172c1u3c1j2e1s1c162c1t2d1r2c1q2f1h2c1u2e142c1t2e1o2e1s1e172c1u1c1w2c1s2e1x2c1s1c162c1t2e1u2e1t2d1r2c1r2d1w2c1q2g1u2c1t2d1c2c1t2e1u2e1u2d1u2c1u3c1q2c1r2e1t2c1u1e102c1u3c1k2e1t2d1z2c1u1e1k2c1r3e1o2c1t3c1a2c1u2c1j2e1s2c1h2c1u1d1j2c1q3f1j2c1u3c1f2c1u2e1p2e1r2c102c1u1c1f2c1q2g1i2c1t3e1y2c1r2c1q2e1s2c1h2c1u2c102c1s3g1v2c1t3e1v2c1u2c122e1t1c1h2c1u1c1v2c1s3e1h2c1s2d1s2c1t2e132e1s3d1u2c1t1c1t2c1s3e102c1u3c1r2c1t2e1x2e1r2c162c1u2d1r2c1r2g102c1s1e1v2c1t3c1q2e1u2d1o2c1s1c1i2c1q3g1h2c1r2c1s2c1u2e1q2e1u2c1o2c1u2c1q2c1s2e1w2c1u2e1c2c1s2e1f2e1u1c1y2c1t2c1s2c1r3e1r2c1s2c1k2c1u2e1g2e1s2c1s2c1u2d1u2c1q2e1z2c1s2c1s2c1r2c122e1t1e1u2c1u3c152c1r2g1p2c1t3e1t2c1t2c1y2e1s2e1s2c1u1e1j2c1r3g1o2c1s1c152c1u1e1x2e1u2c1e2c1u2d1t2c1r2f1k2c1u2d1m2c1r2c1q2e1u2d1k2c1u2e182c1p3e1s2c1t2c1s2c1s1c1s2e1u2c1w2c1s2d1y2c1r2g152c1t3c1t2c1t2e1j2e1t2e102c1u3e1f2c1s2e1q2c1t2c1w2c1t3c182e1t2e1h2c1u1e1h2c1r2g1r2c1t1c1s2c1t2d1q2e1u2e172c1u2e1r2c1p2e1p2c1t2e1v2c1s1c1k2e1u1c1q2c1t2c1y2c1r2g162c1f2d1t2d1v2c1q1g1t2c1s2c1t2c1s3e1r2e1u1e1q2c1s1e1h2c1q1e1h2c1t2c1y2c1s1d1r2e1t2c1j2c1t2c1p2c1s1e1u2c1r3e1y2c1u1e132e1s2c1u2c1u3c1o2c1s2g1w2c1u2c1u2c1s3e1d2e1s1e1t2c1s3e1p2c1r2e1t2c1s3e1a2c1s2c1r2e1t2d1y2c1u2e152c1r1e1h2c1s2e1x2c1u1e1i2e1t3c1j2c1t2c172c1q1g1d2c1t3c1t2c1s2c1y2e1u2e1t2c1s1c1s2c1q3e1y2c1u2c1y2c1s2d1d2e1u2e102c1t2c1x2c1q2e1r2c1t3c1w2c1s2d1h2e1u2c1u2c1u2e1h2c1s2e1u2c1u3c1q2c1s2c1s2e1t1c1w2c1t2e1p2c1q2g1y2c1t3c1y2c1s1c1h2e1t1c1t2c1t2e1s2c1q3g1f2c1t3c102c1s2d1y2e1s3e172c1s1d1d2c1r2f162c1t2c1w2c1u2e1h2e1t2e1q2c1t1c1x2c1r2e1v2c1t3c1j2c1u2e1y2e1t2c1y2c1t3c1w2c1q2e1h2c1s2d1w2c1s1c1s2e1u2e1q2c1s2e1x2c1r2g1g2c1u3d1x2c1u2e1h2e1u2e1h2c1t1c1r2c1r3e1q2c1s3c1v2c1t2c1d2e1s2e1u2c1s2c102c1q3g1p2c1u3e1h2c1t2e1h2e1s2c1j2c1s2c172c1s2g1f2c1u2d1t2c1u2d1w2e1t2c182c1t2d1s2c1q3g1y2c1u3c1y2c1t2e1a2e1s2d1r2c1s2e1k2c1s2e1p2c1t2e1i2c1t1e1h2e1s2c1j2c1s2e1z2c1q2g1d2c1t2e1q2c1t3c1w2e1u1e1t2c1u3c1s2c1s1e1j2c1r2d1y2c1t1e1q2e1s2c1d2c1u1c1s2c1r2g1f2c1u3e1q2c1t2e1p2e1t2e1f2c1s2e1s2c1r3f142c1u3c1g2c1s3e1h2e1u2e1z2c1t3e1v2c1q2e1k2c1u2e162c1u2e1p2e1s2e1t2c1u2c1y2c1r2e1u2c1s1d1j2c1t2c1w2e1t1c1r2c1u2c1o2c1r2g1j2c1u1c1y2c1t3c1h2e1s1e1w2c1s2e1z2c1r2g1t2c1u3c1d2c1t2c1u2e1s2c1t2c1s3c1h2c1s1e1x2c1u3e142c1u2e1r2e1u1d1u2c1t2c1f2c1s3g1y2c1s2c1h2c1s3d1s2e1u1e1k2c1u1e102c1q1e1j2c1s2e1t2c1s1d122e1u2c1s2c1s1e1w2c1s3g1f2c1u1c1z2c1t2c1d2e1u2c1f2c1t2e1u2c1r3g1j2c1u3c1x2c1s2c1h2e1s1d1w2c1t3e1u2c1q1e1k2c1t2c1t2c1t2c1x2e1t2c1f2c1s2e1p2c1s3g1p2c1s3c1z2c1s2c1r2e1t2c1u2c1u2e1z2c1s1f1y2c1s3e1t2c1u2e1r2e1t2c1y2c1t2e1t2c1p3e162c1u2e1f2c1u2e1g2e1s1e102c1u2e102c1s1e1s2c1t2e1y2c1u1e1k2e1s1e1r2c1u2e1r2c1s2e1t2c1r1c1r2c1u2e1d2e1u2e1s2c1u2c1z2c1r3e1h2c1u1c1t2c1t3d1y2e1u2e1y2c1u2e1h2c1s2e1t2c1r3e1j2c1u2e1q2e1u2c1x2c1t1e1h2c1p3g1u2c1u2e1x2c1u1e1r2e1t2c1z2c1u2e1z2c1q3g1u2c1u1e1u2c1t2e1q2e1s1e1q2c1t2c102c1r2e1t2c1s2c1x2c1s1d1o2e1s1e1t2c1u1e142c1q1e1x2c1u2e1x2c1t2c1v2e1t1e1t2c1s1e142c1r3g1t2c1t3c1d2c1s2d1r2e1s2e1c2c1u2e1p2c1q1f1u2c1s3c1x2c1u1e1q2e1t2e1i2c1u2e1u2c1s3e1f2c1t1e1v2c1u1c1v2e1t2c1y2c1u1c1w2c1r2g1x2c1u2e1y2c1u2e1h2e1t2c1y2c1u2c1u2c1q3e1j2c1t1e1a2c1s3e1f2e1u1e102c1t1c1t2c1r1g1x2c1u2e102c1t2c1h2e1s2c1i2c1u2c1q2c1r1f1j2c1r3c1f2c1s1e1d2e1r2c1u2c1t3e1e2c1q2e1c2c1t1d152c1t2e1r2e1s2c1h2c1r2d1d2c1q2e1v2c1u2c1m2c1t2d1s2e1s1c1u2c1r2e1s2c1s3e1r2c1t3c1t2c1t2e1w2e1u2e1y2c1u3c142c1s2e1j2c1s2e1t2c1t1c1d2e1s3e1t2c1u2c1t2c1r1e1u2c1u3e1k2c1t2e1w2e1s3c1a2c1u2c1y2c1s3g1t2c1t3c1y2c1u2c1u2e1t1c102c1u1e1s2c1q3e1x2c1u2c1x2c1t2e1d2e1t2c1u2c1u1e102c1r3e1h2c1t2e1z2c1t3e1y2e1r1d142c1s3c1x2c1r2g1o2c1s2e102c1t3c1t2e1t2e1t2c1s1e1p2c1q2g1f2c1u2e1t2c1s2e1q2e1u1e1x2c1u1c152c1r1f1f2c1u1c1x2c1u3e1d2e1u2e1p2c1u2e1v2c1q2g1p2c1u2e1f2c1t1e1r2e1s1e1f2c1t2c1k2c1s3g1y2c1u2c102c1t1e1q2e1r1c1x2c1u2d1h2c1q3g1s2c1t3e102c1u2c1s2e1t1e102c1s2c1h2c1q2g1a2c1t2e1i2c1u2c1b2e1u2e1j2c1t2c1v2c1s3e1y2c1t2c1j2c1t2c1k2e1s3c1f2c1r3c1g2c1s1g1y2c1s3c1r2c1s2e1w2e1u2e1y2c1u2e102c1s1g1j2c1t1e1r2c1t2c1g2e1s2c1r2c1s2e1o2c1s2f1a2c1u2c102c1t2e1g2e1u1e1z2c1t2c1u2c1r1e1w2c1u1c182c1s2c1q2e1u2e1a2c1u2c1y2c1r2e1w2c1t1c1y2c1u1e1p2e1u2c102c1u2c152c1r1g1t2c1t2e1k2c1u2c1v2e1r2e1w2c1t2e1v2c1r2g1v2c1r2c1a2c1u2c162e1t2e1r2c1t1e1t2c1r2g1s2c1s2c1k2c1u1e122e1r2c1o2c1s2e1u2c1q1g1r2c1t2e1v2c1u1e1r2e1s1c1x2c1t1e142c1r1g1y2c1u3c1q2c1u1c1r2e1s2e1j2c1u3c1v2c1r1g1x2c1s3c1j2c1u2e1x2e1t2d1v2c1t2c1w2c1q2e1a2c1u2e1v2c1u2e1q2e1s2c102c1t2e1v2c1q1g1t2c1t3e1j2c1t3e1d2e1s2c1t2c1s2c1q2c1s2f102c1u2e1m2c1t2c1o2e1s2e1x2c1s2c102c1r2e1i2c1r2e142c1t3c1w2e1t2c102c1t1c1u2c1r2e1y2c1s2e1y2c1u3e1v2e1s1e1f2c1s1e102c1s2g1w2c1s2e1t2c1t2c122e1s2d1v1c1r2c1s2c1x2e1u2c1r2c1s1e102c1s3e1z2c1u2c1f2c1t1e1r2e1u2e1a2c1u2c1s2c1r2e1y2c1u2e1s2c1s2e1q2e1u2c1v2c1s1e1y2c1r2e1h2c1s2e1u2c1t2e1h2e1t1c1k2c1s1c1s2c1q3e102c1u2c1y2c1u3c1u2e1t2e1q2c1u1e1y2c1s1f1j2c1u2e1m2c1s2e1w2e1s2d1s2c1t2c1v2c1q2g1j2c1t3c1w2c1u2d1s2e1u3c1k2c1t2c1y2c1s2g1x2c1u1e102c1t3c1t2e1t2d1z2c1s2c1w2c1r2g1s2c1u2e1k2c1u2c1y2e1s1e1j2c1s1e1s2c1s2g1w2c1s3c1u2c1u2e1w2e1s1e1y2c1s1c1w2c1q2e1r2c1s3c1y2c1u2d1q2e1s1c1u2c1s2c1f2c1q2g1u2c1s1e1t2c1t2e162e1s2d1j2c1t1c162c1q2g102c1t3c1c2c1u3c1k2e1u3e1y2c1s2e1s2c1s2e1w2c1u2e1x2c1u2e1h2e1u2d152c1s2c162c1s3g142c1s2e1j2c1u2c1o2e1u1d1g2c1u1e1y2c1q2e102c1s3c1r2c1t2c1u2e1u1c1y2c1s3e162c1s2g1o2c1u2e1q2c1s1e1r2e1s1c1h2c1u2c1o2c1r2g1z2c1t1d152c1u3e182e1u2d142c1t2e152c1r3e1z2c1s2c1t2c1t2d1s2e1u1e1z2c1s1e1v2c1s2g102c1t2e1q2c1u2d1t2e1u2c1h2c1s2c142c1s2g102c1u3c1d2c1t1c1k2e1t2c1s2c1u2c102c1q1e172c1u3c1g2c1u2e1i2e1u3e1s2c1s2c1s2c1q2e1x2c1t3c1m2c1u2c1f2e1u1c1r2c1t2e1v2c1q2e1z2c1r2e1t2c1t3d1d2e1s2e152c1s1e1t2c1r3e1s2c1u1e102c1t2c1y2e1s2d1s2c1u2c1t2c1s3g162c1u1c1a2c1t2e1x2e1s3c1h2c1u2c1i2c1r2g1h2c1t2c1w2c1s3e182e1t2e1a2c1s2c1h2c1s2g1k2c1t2c1v2c1u2e1q2e1t2e1a2c1t2c172c1q1g1f2c1s1c1m2c1u3c1r2e1s2c142c1r1c1g2c1r2g1s2c1s2e1d2c1s2c1h2e1t1e1z2c1t2e1p2c1s1g1v2c1t1e1i2c1r2e1r2e1u2c102c1t2c142c1s2g1z2c1u2e1t2c1s2c172e1u2c1y2c1t1e1x2c1s3g1j2c1t3e1z2c1u2e1r2e1t3e1v2c1u2c1s2c1s2g142c1s3c152c1u2e1o2e1s1c1z2c1u2e1z2c1s3e1z2c1u3c1t2c1s2c1u2e1u2c1h2c1u3e1t2c1q3e162c1t2c142c1t1c1s2e1s1c1t2c1t1e1h2c1s1f1s2c1s3c182c1r2e1e2e1u1e102c1u1c1z2c1r1f1s2c1s1e1f2c1u1e1x2e1r2e1o2c1u2c1o2c1q2g1s2c1t3c1f2c1t3c1v2e1t2c1h2c1t2c1z2c1q3e1h2c1u2e1z2c1s3c1p2e1s2e1j2c1u2e1s2c1r3g1s2c1t2e1f2c1t2e1o2e1s1e1v2c1t2d1s2c1q2e1o2c1t2c1v2c1u2c1g2e1s2e1j2c1u2e1s2c1r2g1h2c1t2e1q2c1t2c1w2e1t2c1s2c1s2c1z2c1q1f1s2c1s3e182c1r2e1r2e1t2c1q2c1t2c1q2c1p2e1s2c1t3e1t2c1u1e1c2e1u2e102c1t3e1g2c1r2e1t2c1s2c1t2c1u1c1h2e1r2e1s2c1r2e1s2c1r2g1i2c1s2d1i2c1r3e1r2e1s1d1s2c1u2e1v2c1s1e1z2c1s3c1y2c1t2e1r2e1t3d1w2c1u2e1z2c1r2e1o2c1u2c1x2c1t3c1w2e1u2c102c1u2e1y2c1r3g1u2c1s3c1d2c1t2e1h2e1t2e1j2c1s2e1x2c1q3e102c1u3c1m2c1s2c1j2e1u3c1s2c1u1d1u2c1s2g102c1s3e1x2c1t3c1v2e1u2c1z2c1t2e142c1r2e1y2c1t1e1u2c1t2d1d2e1u2c1i2c1t1e1s2c1r2g1j2c1r3e1e2c1t1e1u2e1s3e1t2c1r2c1w2c1r3g1e2c1s3e1j2c1s3c1f2e1r2c1o2c1s2e102c1r3e1u2c1s1c1f2c1r3e1v2e1t2c102c1u2e1s2c1s1g152c1u3e1z2c1u2e1t2e1t1e1s2c1t2c1f2c1q2e1e2c1t3e1u2c1t1d1e2e1t2d162c1t3c1w2c1r1g1v2c1u2e1k2c1u2c182e1u2c1z2c1u1e1o2c1q3g1s2c1u3c1q2c1u1e1p2e1r2c1q2c1u2c1h2c1s2g142c1t2e1l2c1s1e132e1u1c1y2c1u1e102c1s1g142c1u3e142c1t2c1y2e1t1d1i2c1u2e102c1r2g1r2c1t3c1j2c1t3c1s2e1r2e1f2c1t2c1h2c1r2g102c1t2c1q2c1s2c1u2e1s1e142c1u2c1w2c1r2g1j2c1s3c1d2c1t2c1d2e1s2c182c1t2d1c2c1s2e1g2c1s2c1f2c1t2c1y2e1t3e1k2c1u2e1o2c1q1g1q2c1t3c1x2c1u2e1a2e1t1e102c1u1e1p2c1r2e142c1t3e1s2c1u1e1d2e1u2e1o2c1s1e1i2c1r3e1c2c1s3c1s2c1u2c1d2e1t2e1g2c1s2e1v2c1q2e1v2c1t3e1g2c1u2d1r2e1t2e1x2c1t2c1u2c1s3e1r2c1t1e1i2c1t2d1v2e1u2d1z2c1t2d1r2c1r1g1x2c1t3c1x2c1u2e1k2e1t2c1y2c1u2e102c1q2g1x2c1u2e1r2c1t2e1v2e1r1c1f2c1t2e1e2c1q2f1z2c1t2c1t2c1u1c1b2e1s1e1v2c1t1e1h2c1s2e1o2c1u2e1t2c1r2e1t2e1s2e1s2c1u3c152c1p3f1r2c1u3c1q2c1u2c1k2e1t2c1q2c1t2d1x2c1r2g1o2c1r2d1m2c1t2e1o2e1r2c1s2c1u1c1z2c1r1g1t2c1t2d1f2c1t2c1y2e1s1d1z2c1t3d1o2c1s2e1o2c1t2e1w2c1u3c1w2e1u2e152c1s2e1t2c1r2g1w2c1s2c1z2c1r2c1h2e1r1e102c1t2c102c1q1e1c2c1u2c1m2c1t2d1d2e1s2c1y2c1u2c1p2c1s2g1o2c1t2e1s2c1t2d1r2e1t1e1j2c1u1e1f2c1r2e1s2c1t2c1y2c1u2c1q2e1t1c142c1u2c1s2c1q3g172c1t3c1j2c1t2d1s2e1s1c1t2c1u3d1q2c1q2g1q2c1u2c1y2c1u1e1u2e1u2e142c1t2c1s2c1s2f1v2c1s2e1w2c1u2c1x2e1s1e1z2c1s1c1s2c1q3g1y2c1s3c1s3d1z3d163e183c121g1r1p1e1a1c1k2e121e1e3g1h1d1c3e141d1g1e1j1g1t2c1g1e1w2c1p1e1g2e1u1c1s2c1t3c1i2c1u2e162c1q2e1m2c1q1d192e1u2e1k2c1u2e1v2c1s2g1y2c1q3d102c1q2c1w2e1s1d1i2c1r2e1t2c1t3g1g2c1q2c1u2c1q1d1r2e1t2e1r2c1s3c1u2c1s2g1e2c1s1c1z2c1q3c1r2e1u2c122c1s2e1k2c1u1e1k2c1s3c1h2c1s2d1z2e1s3c1x2c1t1d1s2c1s1f172c1r3c162c1q1d182e1u3d162c1s1d152c1s3e1b2c1q3d172c1s3e1t2e1s1d172c1s3d1c2c1s3f172c1q3e162c1q1d192e1s3d1e2c1s3d152c1u3f142c1q2d192c1q3d1z2e1s3d172c1s3e1u2c1s3f192c1r3d1e2c1q3d172e1s3c1c2c1s3d162c1t3f192c1q1d172c1r3c192e1s3d152c1s3d172c1s2e1u2c1q2c1w1c1d1c123e161c1i3e1b1c121c121f141e1q2c1b1c1o1c183e1c1c1e3e141e1f3e191f1c3d1q1e1m3c1b1c1c3f1s2e1k1c1b3c1b3d1c3e1p1e1d1e1c3e1d1c1s1f1c3c1b1d161e1q1d1b1f1j3d1d3e1g3d1e2c1c1e1q3d1a3d1j3d163d142e1a1c1d3d1f3d163e1c3f1p3c101d141c1c1c1d3f1s3d1g1e1f1e1k1e1d1e143c1q3d1m3c161c1t3e1c3e1e1e1i3d151e1e3e1o1c1d1c1f2c1q1d1c3f1p1e1d3c1k1e1k3c121e1r2e1q2c1t2e122c1r2e102c1r1e172c1q3e1y2e1t2d1j2c1t2c1x2c1u2g182c1r2e1r2c1r2e1x2e1u2e1y2c1t3c1y2c1s2g152c1p3c1j2c1q3c142e1t2e1i2c1s1c1j2c1t2e1x2c1r2c1s2c1r2c152e1r1c1y2c1u3e1j2c1t2g1c2c1s3c1v2c1r2e102e1t2c1q2c1u1c1u2c1u1e1s2c1s2e1x2c1r2e1f2e1t2c1u2c1s3c1x2c1u2g1p2c1r2e1y2c1q2c1t2e1t2d1d2c1u2e1d2c1u1e1w2c1r2d1j2c1s3c1t2e1t1c1x2c1t2d1t2c1t2e1w2c1q2c102c1s1e1d2e1u3c162c1t2c132c1u3e1f2c1q2c1f2c1r3c1v2e1t2c1x2c1r1e1u2c1u2e1z2c1s2e142c1r2c1u2e1u2c1q2c1s2d142c1t3g1q2c1r2e162c1q3e1r2e1t1e1x2c1t2c172c1s3e1f2c1q2d1z2c1r3c1w2e1s2c1y2c1s1c1q2c1u1f1g2c1s1e1s2c1s2d1c2e1s3c1r2c1t2c1w2c1u1e1y2c1r3e142c1q3d1g2e1t2d1i2c1t1e1x2c1t2g172c1s1e182c1q3e1t2e1t3c1v2c1u3e1f2c1r2g102c1s2d1l2c1s2c1j2e1t2c162c1s2c1y2c1t1e1r2c1r3c1s2c1q3d1v2e1t2c1f2c1s3e1u2c1s2e102c1q1c162c1q1c1q2e1u2c1y2c1s2c1y2c1u3e152c1s2e1s2c1s2e1u2e1u2c1i2c1s1c1f2c1u1g1z2c1r1c1w2c1r2c1w2e1t3e1t2c1t2e1w2c1t2g1f2c1r2d1h2c1s2c1i2e1u1e122c1u2c1q2c1s2g1s2c1r1e1v2c1q1c1p2e1u2e1k2c1t3d132c1t1e1s2c1r1c1h2c1s2e1w2e1u1e1q2c1u1c122c1t2g182c1r2d1z2c1r3d1v2e1t2c1j2c1s3d1t2c1u2g1s2c1s1e1l2c1p3e1f2e1t2c1d2c1t3c1d2c1u2g152c1p1e1t2c1q2e1f2e1s1e1x2c1u1e1k2c1u2f1o2c1s2c1s2c1s2e152e1s2c1y2c1s1c1d2c1u2g1r2c1s2e1l2c1s2e1g2e1u1c1q2c1t1e1k2c1u2e1p2c1q2c1s2c1q1e1h2e1t1c1p2c1u1c1y2c1t2g1o2c1s2d1t2c1s3d1y2e1s3d1u2c1u1e1w2c1r1g1i2c1s1e1w2c1r2c1h2e1t2d1x2c1u2c1q2c1u1e1t2c1q1c1z2c1s2e1x2e1s2d1y2c1u3c1f2c1s1e1s2c1s2e1t2c1s3e1z2e1t2c1c2c1t1d1s2c1u2e1z2c1r1e1h2c1q2e1f2e1s2d1h2c1t2e132c1t2e1k2c1p1e1u2c1r2c1t2e1u2e1p2c1s2e1u2c1s3e1r2c1s3c1q2c1r2c1t2e1u1c1q2c1u2c1p2c1t2f1u2c1r2d172c1q1e1q2e1u1c1i2c1u3c1q2c1u1g1o2c1s1e1x2c1q2d1y2e1s2c1t2c1t2c122c1t1g1u2c1r2c1q2c1r2c1o2e1r2c1q2c1u3c1g2c1u2g1s2c1s3c1i2c1p3e1p2e1s2c1q2c1t3e122c1t1e1t2c1r2c1q2c1p2c1q2e1u3c1h2c1s2e1f2c1t2e162c1q2e1g2c1r2c1t2e1t1c1p2c1s2e1f2c1t1g1h2c1r2e1t2c1s2d1q2e1s2e1w2c1t2c1y2c1t1f1p2c1q1c1l2c1r2e1t2e1s1c1q2c1u2e1p2c1u3g1r2c1s3c1l2c1q1c1t2e1t2e1r2c1s2c1t2c1t3g1u2c1q1d1r2c1s2c1q2e1u3e1f2c1u1d1q2c1r1g1a2c1s1c1q2c1s2c1x2e1u1c1k2c1t2e1q2c1s1g1u2c1r1e1l2c1s2d1x2e1u1c1j2c1t2c1g2c1s3e1v2c1q3c1f2c1s2e1y2e1t2c132c1t2e1y2c1u2g1c2c1r2c102c1q2e1d2e1s2d1j2c1s3c1q2c1u2g1s2c1r2e1r2c1q2c1p2e1s3c1j2c1t2e1u2c1t3g1o2c1s3e1q2c1r3e1r2e1s1e1j2c1t2e1v2c1t2g1r2c1s3e1h2c1q1e1y2e1t2e142c1t1c1r2c1u1g1x2c1r2d1r2c1q2c102e1t2e1r2c1s3e1f2c1s3e1s2c1p2e142c1r3e1t2e1u2e132c1u2c1p2c1s1e1t2c1s3e1h2c1p2c1r2e1t2c1f2c1t1c1h2c1t1e1j2c1r3e1l2c1s3e1y2e1u2c1x2c1s2c122c1s3g1y2c1r1c1l2c1s3c1z2e1u2e1y2c1s3e1r2c1u2e1c2c1s3c172c1q2d1j2e1t2e1f2c1t3c1w2c1t3g1y2c1q3d172c1s3e1u2e1s2d1q2c1u2c1q2c1t1f1z2c1r2e1l2c1r2d1q2e1s2e1f2c1u2e1p2c1u2e1o2c1s3c1d2c1r3d1p2e1u1e1s2c1t2d132c1s2g1s2c1r2e1l2c1s2c102e1u2c1j2c1u1c1v2c1u3g1s2c1q3e142c1s1c1y2e1t3c1f2c1t2e1q2c1t3e1a2c1s2c1w2c1q2d1j2e1s1c132c1t2e1i2c1u3e102c1r1c1j2c1q2c1f2e1t2c1w2c1u2d1x2c1t3e1j2c1s3c1h2c1q3d1v2e1u2e1u2c1u1e1g2c1t3g1v2c1p2e102c1q1c1q2e1s1d122c1r3e1g2c1s2e1o2c1q2e1u2c1r2c1j2e1t2c1j2c1t2c1y2c1u2f1o2c1r2e1r2c1q2c1j2e1u3e1s2c1t2c1p2c1u3e1a2c1q2c1x2c1q2c1x2e1u2c1j2c1s1e1r2c1t2e1h2c1p3e152c1q1c1t2e1u1e1y2c1u2e132c1u3g1r2c1q2c1s2c1s1c1y2e1s2c1p2c1s2c1u2c1t2e102c1s3c1t2c1r3c1a2e1u2c122c1t1e1q2c1t2e1o2c1r3e1s2c1s2e1r2e1t2d1f2c1t1e1r2c1u2g1z2c1s3c1k2c1r2c1j2e1u2c1j2c1t2c1e2c1r2e1s2c1s2e142c1q1d1j2e1u2e1y2c1u2e1x2c1t1e152c1q2c1r2c1q2c1k2e1u2c1p2c1u1e1r2c1u2g1s2c1s3c162c1q3c1a2e1u3e1h2c1u3c1y2c1u3e142c1s2c1y2c1s3e1s2e1s2d1j2c1r2c1q2c1u2f152c1p3c1q2c1s1e1o2e1t2c122c1s1c1j2c1t1e1z2c1s2e1w2c1s2d1j2e1s2c1h2c1t3c1t2c1t1e102c1r2e162c1r2e162e1u2c1u2c1s3e1t2c1u1e1s2c1q1c1z2c1s2d1k2e1u1d1x2c1u2c1q2c1t2g1x2c1s2e1e2c1s2e1y2e1u3c1s3c1z2c1r1e1x2e1u2e1o2c1r1d122c1t2e1t2c1s1c152c1s2e1v2e1s2e1w2c1u3c1w2c1t2e1t2c1q2c1t2c1r2e1p2e1u1e132c1u2c1t2c1t2e1h2c1s2c1z2c1q1c102e1u2d1b2c1u2e1b2c1u1f1u2c1r2e1i2c1r2c1x2e1u1d1r2c1u2c1r2c1u3e1x2c1s1e1s2c1s2c1t2e1t1e1o2c1u2c1v2c1s3g1f2c1q2e1x2c1r2d1v2e1t2c1h2c1u2e1u2c1u1e1u2c1r2e1l2c1s2e102e1u2d1i2c1u3c1u2c1t1g152c1r2c1x2c1s2e1k2e1t2d1w2c1u3e1d2c1s2e1i2c1s1c1u2c1s2e1t2e1u2c1y2c1t2c1s2c1t2g1p2c1q2e1w2c1s1c1o2e1u2c1w2c1u3c1r2c1s2e1z2c1r1c1j2c1s1c1y2e1s2e1p2c1t3c1r2c1t2f1u2c1q3c1g2c1q3c162e1u2e1o2c1t2c1y2c1s1e1t2c1s3d1k2c1s2e1s2e1t2c1p2c1t1e1g2c1t2g142c1s3c1t2c1s3c1s2e1t3c1r2c1t3c162c1u1e1y2c1s2e1y2c1s1d1h2e1t3c1h2c1t1c122c1r1f1t2c1s2e1z2c1q2c102e1u2e142c1t3c1w2c1s1g1b2c1r2e1g2c1s1c1s2e1s1e1r2c1s2c1d2c1u2e1j2c1r2e1x2c1r1d172e1u3e182c1t3e1r2c1t2e1w2c1q3e1y2c1s1d1v2e1s2c122c1s2c1b2c1t3e1f2c1r1c1v2c1s3e1h2e1s2e1y2c1s1e1t2c1t2e1y2c1s2e1t2c1s1d1p2e1t1c1i2c1t2c1q2c1t1g1s2c1s2c1d2c1s2c1s2e1t3c1y2c1u2e1p2c1t2e1z2c1s2e102c1s1c1o2e1s1c1r2c1s2c1d2c1t1e1j2c1s1c162c1q3c172e1u2c1f2c1s1e1d2c1s1g102c1s1c1r2c1r2c1z2e1s1e1r2c1u1c1f2c1u1e1x2c1q2e1h2c1p2c1o2e1t3c1y2c1r3c1x2c1s2e1q2c1r2c1t2c1q2e102e1u2c1s2c1s3c1v2c1u1f1y2c1q2d1q2c1s1e1s2e1s2c1o2c1u2e1h2c1s2g182c1q2e1i2c1s2e1u2e1t1c1r2c1s2e1b2c1u3g1h2c1r2c1z2c1s2e1o2e1t2c1r2c1u3c1r2c1u1g1y2c1s1c1q2c1s2e1x2e1t1e1f2c1t3c1i2c1s2g152c1s2e1g2c1s2e102e1u2c1v2c1s3e1w2c1s2e1z2c1q2e1s2c1r2d162e1s2e1d2c1u2d1r2c1t3e1y2c1r1e1y2c1s2c182e1s2c1o2c1t3e1d2c1u3g1u2c1s1c1h2c1q1e1t2e1t2e1f2c1u2c1h2c1t2e1y2c1q2e1x2c1r3c1w2e1u1e1r2c1u1c1h2c1t2g1t2c1q1c1t2c1q2c1z2e1s1c1g2c1t1e1q2c1u1e1p2c1s1e1t2c1r2e1s2e1t1c1i2c1t2c1q2c1u1g1f2c1r1e1f2c1p2c1g2e1t2e1g2c1u1c1e2c1u1f1p2c1q2e142c1q3e1z2e1r2e1k2c1s3d1b2c1s1e1t2c1s1e1f2c1p2c1g2e1u1e1e2c1u1c1k2c1s2g142c1q1e1w2c1r2c102e1u1d1i2c1s1e1h2c1t2e1x2c1q2e1q2c1r2c102e1s2c1w2c1t1c1r2c1t1g1t2c1s2e1s2c1q2c1i2e1s2d122c1t3c1w2c1t1e1j2c1s1c1j2c1q3e1w2e1u1e1s2c1t3e1q2c1s1g1b2c1s1c1y2c1q1e1d2e1t2e1r2c1t3e1r2c1u1e1t2c1q2c1k2c1s3c1t2e1u2c1g2c1u2c1t2c1s2g1f2c1q1c1q2c1q2e1y2e1s1c1u2c1t3c1u2c1t2e1y2c1r2c1h2c1r1e1i2e1u1c1u2c1r2c1h2c1t2e1v2c1s2e1v2c1s2c1o2e1u1d1t2c1u2e1r2c1t1g1y2c1s2c1v2c1s2c1o2e1u1e1i2c1t3c1r2c1t2e102c1s2d1f2c1r3e1j2e1s2c122c1u2c1r2c1t2g142c1r1d1s2c1r2e1z2e1u3e1p2c1s2e1h2c1s2g1s2c1s3d142c1q2e1h2e1u2c1w2c1t3c1q2c1u2g1j2c1p1d1j2c1s3c1o2e1t2c1v2c1u2e1r2c1u2e1t2c1s2c1y2c1r2c1u2e1t1d1h2c1u2c162c1t1f1f2c1p2c1m2c1r2e102e1u1c1f2c1t1c1g2c1u2e1w2c1r3c1w2c1r1e1x2e1u2c1v2c1u3e1i2c1u3e1p2c1r1e1r2c1s2c1o2e1u2c1u2c1s2e1r2c1u2e1q2c1s2c1x2c1q3c102e1t1e1w2c1t1e1o2c1t3e1k2c1p2c1f2c1r2c152e1s2c1d2c1u3c1d2c1u1f1j2c1r2e1h2c1r1c1h2e1s1c1v2c1u2e1p2c1u1e1j2c1q2e1t2c1s3c1r2e1t2c1u2c1u2c1k2c1s1g1f2c1q1c1x2c1r2c152e1u1c1u2c1t2e1t2c1u2g1r2c1s3c1u2c1s2c1k2e1t2e1y2c1s1c1r2c1u3e142c1s3c1q2c1s1c1h2e1u2d1f2c1u2e1x2c1u1g1s2c1s3e1t2c1r1e1v2e1t2c1r2c1s2e1a2c1s2e1q2c1r3c1q2c1p2e1u2e1r2e1p2c1t2c1f2c1r2g142c1q2e1g2c1s1e162e1u2c1u2c1t2e1h2c1u1g1x2c1s1e1j2c1q1c1s2e1u2c1w2c1u3c1u2c1u2f1r2c1s1c1m2c1s3e1h2e1t2e1q2c1s2e1v2c1s2e1x2c1q3c1v2c1s2c1o2e1s2e1r2c1u2c1r2c1t2g1j2c1s2d1f2c1q2c142e1u2c1o2c1s2c1y2c1r2g1s2c1s2e1q2c1q1c102e1s1e1g2c1u3c1p2c1s2g1z2c1s1e1v2c1q1c1o2e1u2c1w2c1t3c1o2c1u2f1j2c1r2c1f2c1q2c1t2e1t2e1h2c1s1c1y2c1t2e1i2c1p2c1q2c1p1c1t2e1u2c1w2c1t2e1h2c1t2f1t2c1p1e1f2c1q2e1u2e1r2e1v2c1t3c1u2c1s1e1j2c1q2e1x2c1s1e1t2e1u2e1r2c1t2e1y2c1t3e1j2c1r2e102c1s2c1w2e1u1e1h2c1r1e1r2c1u2e1s2c1r1e1q2c1s2e1r2e1t1c1x2c1t2e1s2c1u2e1x2c1q2c102c1s3c102e1r2e1t2c1s3e1r2c1u2e1f2c1q2c1w2c1q2e1v2e1t1c122c1s2e1d2c1s2g1q2c1r2c1m2c1p2c1r2e1s2c1w2c1u1e1r2c1s1f1t2c1r1c102c1s2c1s2e1t1e1r2c1s2d1r2c1u3f1f2d1k2c1s3e1i2c1u2f1p2c1r1d1v2c1s2e1v2e1s2e1t2c1s1c1r2c1u2e1w2c1s2c1s2c1s2c1o2e1t1c1r2c1t1d1r2c1u2f1q2c1s1d102c1s2e1o2e1s2e1b2c1s1c1y2c1u2e1t2c1r2e1q2c1s2e102e1u2d1k2c1u2c1x2c1s1g1x2c1q1c142c1q3c1p2e1r2e1v2c1t2c1q2c1u3e1t2c1q2e1h2c1q2c1s2e1s2c1j2c1u3c1r2c1s2e1y2c1r2e1l2c1r1c1k2e1s1e1i2c1t2e1d2c1t3e1t2c1q2e1d2c1r1c1w2e1s1c132c1u2c1g2c1u1e1h2c1s2e1r2c1r2c1k2e1s2e1y2c1s2d1q2c1u2g1t2c1s2e1t2c1q3e1r2e1u2e1s2c1u3c1u2c1t2e152c1s2e1f2c1r1c1r2e1u1e1q2c1t1c1f2c1s3e1t2c1s2e1h2c1r2c1v2e1s2c142c1t2e1b2c1t1f102c1s1d152c1r2e1u2e1u1c1y2c1u2c1d2c1u3g1u2c1s3e1w2c1s2e1h2e1t1c1v2c1t2c1w2c1u3g162c1s1e1r2c1r2e1o2e1s2c1h2c1s2e1r2c1u2e1u2c1s1e1w2c1s1c1x2e1u2e1j2c1t2e1t2c1u2g1p2c1s2e152c1q1d1s2e1u3e1x2c1s1c1r2c1u3g1s2c1s2c1r2c1q2c1o2e1u2c142c1u3c1r2c1t1e1y2c1r1e1y2c1r1c152e1s1e1q2c1u3d1u2c1u2g1u2c1s2c1t2c1r1e102e1u2e1d2c1t2e1x2c1s2e1y2c1r2e142c1r2e1z2e1t2c1v2c1u1c1g2c1s1g1t2c1q2e1s2c1r2c1h2e1t2d1k2c1r2e1r2c1t3e102c1s1c1h2c1r2c162e1t1e1u2c1t3c1h2c1s1f1s2c1q1d1w2c1r2e1p2e1u1d1i2c1u3c1s2c1s3e1u2c1s3c1k2c1q2e1p2e1t2c1x2c1t2c162c1t2e1w2c1s2e1s2c1q2e1v2e1s2e1r2c1u2e1q2c1t1e1w2c1s2c1t2c1s1e1z2e1u2e1y2c1t1c1p2c1s2g1w2c1q2c1z2c1r2d1p2e1u2d1j2c1u2c1r2c1t2g1j2c1r2e1h2c1q1e1s2e1u1c1q2c1t2e162c1s1g1r2c1r1c1g2c1s1e1c2e1t2c1t2c1t2e1d2c1u2e1g2c1r2e1u2c1r2c1v2e1s1c192c1u2c142c1t2f1w2c1q1c1y2c1s1c102e1u1c1x2c1t1c1q2c1t1f1u2c1q2e162c1r2c1z2e1u2c1x2c1u2c1r2c1t2e1j2c1r1c142c1q2c1t2e1s2c1y2c1u2e1h2c1u3g1p2c1q1d1v2c1s2e1x2e1s2c1t2c1u2e1r2c1u2g1z2c1q1e1l2c1p3c102e1u2c1w2c1t2c182c1u2e1q2c1r2e1t2c1p3c102e1u1c1p2c1u2c1v2c1u2e102c1s2e1a2c1r1c1o2e1s2e1x2c1s3e1w2c1t3g1x2c1r2e1s2c1r2e1f2e1s2c1v2c1t2c1d2c1t1g1x2c1s1d1z2c1s2e1z2e1u2c1x2c1t1e1r2c1s1g1z2c1r3e1v2c1r2e1p2e1t2c1p2c1t3c1i2c1t1g1x2c1s2e1z2c1s2c1z2e1t1e1t2c1u2e1q2c1s2e1g2c1q2e162c1r3c102e1u2c1s2c1t2e1v2c1s2g142c1q2e1s2c1s2e1q2e1s1d1q2c1u2c1k2c1t2e1x2c1q1e1s2c1r2c1j2e1u2c1q2c1t3e1r2c1t2e1o2c1r2c1q2c1p2c1s2e1u3c1g2c1u2e1o2c1u3e1t2c1s2e142c1r2e1t2e1u2c1r2c1s2d1p2c1u3e1j2c1r1e1v2c1s2e1w2e1t2e1v2c1t3c1v2c1t2g192c1s1e152c1q1e172e1u2e1q2c1u1c1r2c1s1e1f2c1s1e1y2c1q2e1o2e1u2d132c1u2e1v2c1s2e1p2c1q3c1s2c1s2c102e1t1e1d2c1s2c1p2c1t2f1y2c1q1c1z2c1q2e1r2e1s2c1d2c1u3e1r2c1s2f142c1r1d1w2c1q1e1u2e1u1d142c1s1c1q2c1s1g1v2c1r2e162c1r1d1u2e1t1d152c1t2e1f2c1t3g1x2c1r1e1z2c1r2c1a2e1u2c1i2c1u1c1w2c1u2g1t2c1r1c152c1q2e1w2e1s2e1v2c1s1c1d2c1s1f1d2c1r2d1s2c1r2d1s2e1t1e1r2c1s3c1r2c1u3e1f2c1s2e1a2c1q1e1x2e1t1c1h2c1u2e1w2c1u2e1r2c1q2e1h2c1r1c1w2e1s2e1y2c1u1c1p2c1t2e1u2c1r2d1r2c1s1e1u2e1t2c132c1s2e1r2c1u2g1j2c1q1c102c1s1c1b2e1u1c1r2c1r2e1r2c1u3e1v2c1s1e1z2c1r1d152e1u2e1p2c1t2e1q2c1t2g1y2c1q2e102c1s2d1z2e1t2e1f2c1t3c1s2c1u1g1y2c1r2d1j2c1s1e1v2e1t2c1y2c1s3e1w2c1s2g1f2c1r3e1r2c1s2e1h2e1t2e1s2c1t2e1y2c1s2e1c2c1r2c1w2c1s2e1j2e1u2c122c1r2c1o2c1u1g1f2c1q1c1k2c1s2d1s2e1s2c1q2c1s1e1p2c1s1f1f2c1s1e1s2c1q2d102e1s2e1p2c1t2e1f2c1u2e1y2c1r1c1g2c1q2e1t2e1s1c1q2c1s3c1r2c1s1f1p2c1r2e1t2c1r2c1h2e1s2e1f2c1s3c122c1u3e1y2c1s3e1l2c1q1c1r2e1t2e1x2c1r1c1r2c1r3g1c2c1r1c1s2c1r2e1o2e1t2c1j2c1u2c1o2c1u2f1r2c1p1c1l2c1s3c1s2e1s2c1w2c1u2e1i2c1u1g1v2c1q1e1s2c1s2c1t2e1u2c1j2c1r2e1s2c1u1g1y2c1s2e1q2c1r3e1q2e1u2c1y2c1u2e1t2c1u2e1x2c1p3e142c1q2c1p2e1u3c132c1s2e1t2c1t2e1y2c1s2d1x2c1q2e1h2e1t3c1a2c1u2c1w2c1u3e1r2c1p3e1t2c1s2d1s2e1u2e122c1u2d1p2c1u2e1t2c1r1e102c1q1c1c2e1t2c1y2c1u3d172c1t1e1x2c1s2c172c1r2c1h2e1s2c1q2c1u3c122c1u2f1d2c1s2e1j2c1s1c1v2e1s1c1y2c1r3e1k2c1s1g1t2c1s1c1l2c1q2e1v2e1t2c1j2c1t3c1x2c1u2g1u2c1q2c102c1r1c1v2e1t2c1d2c1t3e1q2c1u3f1t2c1q3e1y2c1s1e1y2e1s2e132c1u1c162c1t2e172c1s2e1k2c1s3e1y2e1u1e1j2c1t3c1w2c1s1g1t2c1s3e152c1s1e1o2e1s2c133c1y3c1t2d1r1e171c1k1d1i2e1e2d2i2q2b2h14','11b99d324857c3e836e24f72fafe00f6'));
//]]>
jQuery(document).ready(function($) {$(&#39;#megamenuid&#39;).megaBloggerMenu({ postsNumber : 4, noThumbnail : &#39;https://2.bp.blogspot.com/-Z7jG9iO9OTg/Vazz6YJnFQI/AAAAAAAALVs/wlSvXPgdDAo/s1600/no_image_available.png&#39; 
}); });
</script>

<b:if cond='data:view.isHomepage'>
<script type='text/javascript'>
//<![CDATA[
(function($) {"use strict";
$.fn.sliderResponsive = function(settings) {
var set = $.extend( {slidePause: 4000, fadeSpeed: 800, autoPlay: "on", showArrows: "off", hideDots: "off"}, settings ); 
var $slider = $(this); var size = $slider.find("> div").length; var position = 0; var sliderIntervalID;
$slider.append("<ul></ul>"); $slider.find("> div").each(function(){$slider.find("> ul").append('<li></li>');});
$slider.find("div:first-of-type").addClass("show");
$slider.find("li:first-of-type").addClass("showli")
$slider.find("> div").not(".show").fadeOut();
if (set.autoPlay === "on") { startSlider();}
if (set.showArrows === "on") {$slider.addClass('showArrows'); }
if (set.hideDots === "on") {$slider.addClass('hideDots'); }
function startSlider() {sliderIntervalID = setInterval(function() {nextSlide();}, set.slidePause);}
$slider.mouseover(function() {if (set.autoPlay === "on") {clearInterval(sliderIntervalID);} });
$slider.mouseout(function() { if (set.autoPlay === "on") {startSlider(); } });
$slider.find("> .right").click(nextSlide)
$slider.find("> .left").click(prevSlide);
function nextSlide() {position = $slider.find(".show").index() + 1;
if (position > size - 1) position = 0; changeCarousel(position);}
function prevSlide() {position = $slider.find(".show").index() - 1;
if (position < 0) position = size - 1; changeCarousel(position);}
$slider.find(" > ul > li").click(function() {position = $(this).index(); changeCarousel($(this).index()); });
function changeCarousel() {$slider.find(".show").removeClass("show").fadeOut();
$slider .find("> div") .eq(position) .fadeIn(set.fadeSpeed) .addClass("show");
$slider.find("> ul").find(".showli").removeClass("showli");
$slider.find("> ul > li").eq(position).addClass("showli"); }
return $slider;};
})(jQuery);
$(document).ready(function() { $("#slider1").sliderResponsive({// Using default everything // slidePause: 5000, // fadeSpeed: 800,  // autoPlay: "on", // showArrows: "off", // hideDots: "off", // titleBarTop: "off" 
}); }); 
//]]>
</script>
</b:if>

<b:defaultmarkups>
  <b:defaultmarkup type='Common'>
    <b:includable id='widget-title'>
      <b:if cond='data:defaultTitle or data:title'>
        <div class='widget-title'>
          <h3 class='title'>
            <data:title/>
          </h3>
        </div>
      </b:if>
    </b:includable>    
  </b:defaultmarkup>
  <b:defaultmarkup type='AdSense,Blog'>
   <b:includable id='defaultAdUnit'>
          <!-- Clear out style (need non-empty string) -->
          <b:with value='&quot;/* Done in css. */&quot;' var='style'>
            <b:include name='super.defaultAdUnit'/>
          </b:with>
   </b:includable>
  </b:defaultmarkup>
  <b:defaultmarkup type='PopularPosts'>
    <b:includable id='main' var='this'>
      <b:include name='widget-title'/>
      <div class='widget-content'>
        <b:loop values='data:posts' var='post'>
          <b:include data='post' name='postContent'/>
        </b:loop>
      </div>
    </b:includable>
    <b:includable id='postContent' var='post'>
      <div class='post'>
        <div class='post-content'>
          <a class='post-image-link' expr:href='data:post.url'>
            <b:if cond='data:post.featuredImage'>
              <img class='post-thumb' expr:alt='data:post.title' expr:src='data:post.featuredImage resizeImage 680'/>
              <b:else/>
              <img class='post-thumb' expr:alt='data:post.title' src='https://4.bp.blogspot.com/-O3EpVMWcoKw/WxY6-6I4--I/AAAAAAAAB2s/KzC0FqUQtkMdw7VzT6oOR_8vbZO6EJc-ACK4BGAYYCw/w680/nth.png'/>
            </b:if>
          </a>
          <div class='post-info'>
            <h2 class='post-title'>
              <a expr:href='data:post.url'><data:post.title/></a>
            </h2>
            <div class='title-secondary'>
              <span class='post-date published' expr:datetime='data:post.date.iso8601'><data:post.date/></span>
            </div>
          </div>
        </div>
      </div>
    </b:includable>
  </b:defaultmarkup>
  <b:defaultmarkup type='Header'>
    <b:includable id='main' var='this'>
      <div class='header-widget'>
        <b:include cond='data:imagePlacement in {&quot;REPLACE&quot;, &quot;BEFORE_DESCRIPTION&quot;}' name='image'/>
        <b:include cond='data:imagePlacement == &quot;BEHIND&quot;' name='title'/>
      </div>
    </b:includable>
    <b:includable id='image'>
      <a class='header-image-wrapper' expr:href='data:blog.homepageUrl'>
        <img expr:alt='data:blog.title.escaped' expr:data-height='data:height' expr:data-width='data:width' expr:src='data:image'/>
      </a>
    </b:includable>
  </b:defaultmarkup>
  <b:defaultmarkup type='FeaturedPost'>
    <b:includable id='main' var='this'>
      <b:include name='widget-title'/>
      <div class='widget-content'>
        <b:loop values='data:posts' var='post'>
          <b:include data='post' name='postContent'/>
        </b:loop>
      </div>
    </b:includable>
    <b:includable id='postContent' var='post'>
      <div class='post'>
        <div class='post-content'>
          <a class='post-image-link' expr:href='data:post.url'>
            <b:if cond='data:post.featuredImage'>
              <img class='post-thumb' expr:alt='data:post.title' expr:src='data:post.featuredImage resizeImage 680'/>
              <b:else/>
              <img class='post-thumb' expr:alt='data:post.title' src='https://4.bp.blogspot.com/-O3EpVMWcoKw/WxY6-6I4--I/AAAAAAAAB2s/KzC0FqUQtkMdw7VzT6oOR_8vbZO6EJc-ACK4BGAYYCw/w680/nth.png'/>
            </b:if>
            <span class='post-tag'><data:post.labels.last.name/></span>
          </a>
          <div class='post-info'>
            <h2 class='post-title'>
              <a expr:href='data:post.url'><data:post.title/></a>
            </h2>
            <div class='title-secondary'>
              <span class='post-date published' expr:datetime='data:post.date.iso8601'><data:post.date/></span>
            </div>
          </div>
        </div>
      </div>
    </b:includable>
  </b:defaultmarkup>
  <b:defaultmarkup type='Label'>
    <b:includable id='main' var='this'>
      <b:include name='widget-title'/>
      <b:include name='content'/>
    </b:includable>
    <b:includable id='content'>
      <div class='widget-content'>
        <b:class expr:name='data:this.display + &quot;-label&quot;'/>
        <b:include cond='data:this.display == &quot;list&quot;' name='list'/>
        <b:include cond='data:this.display == &quot;cloud&quot;' name='list'/>
      </div>
    </b:includable>
    <b:includable id='list'>
      <ul>
        <b:loop values='data:labels' var='label'>
          <li>
            <a class='label-name' expr:href='data:label.url'>
              <data:label.name/>
              <b:if cond='data:this.showFreqNumbers'>
                <span class='label-count'><data:label.count/></span>
              </b:if>
            </a>
          </li>
        </b:loop>
      </ul>
    </b:includable>
  </b:defaultmarkup>
  <b:defaultmarkup type='FollowByEmail'>
    <b:includable id='main' var='this'>
      <b:include name='content'/>
    </b:includable>
    <b:includable id='content'>
      <div class='widget-content'>
        <b:if cond='data:defaultTitle or data:title'>
          <h3 class='title'>
            <data:title/>
          </h3>
        </b:if>
        <span class='before-text'><data:skin.vars.followByEmail/></span>
        <div class='follow-by-email-inner'>
          <form action='https://feedburner.google.com/fb/a/mailverify' expr:onsubmit='&quot;window.open(\&quot;https://feedburner.google.com/fb/a/mailverify?uri=&quot; + data:feedPath + &quot;\&quot;, \&quot;popupwindow\&quot;, \&quot;scrollbars=yes,width=550,height=520\&quot;); return true&quot;' method='post' target='popupwindow'>
            <input autocomplete='off' class='follow-by-email-address' expr:placeholder='data:messages.emailAddress' name='email' type='email'/>
            <input class='follow-by-email-submit' expr:value='data:messages.subscribe' type='submit'/>
            <input expr:value='data:feedPath' name='uri' type='hidden'/>
            <input name='loc' type='hidden' value='en_US'/>
          </form>
        </div>
      </div>
    </b:includable>
  </b:defaultmarkup>
  <b:defaultmarkup type='BlogArchive'>
    <b:includable id='main' var='this'>
      <b:include name='widget-title'/>
      <b:include name='content'/>
    </b:includable>
    <b:includable id='content'>
      <div class='widget-content'>
        <div id='ArchiveList'>
          <div expr:id='data:widget.instanceId + &quot;_ArchiveList&quot;'>
            <b:include cond='data:this.style in {&quot;FLAT&quot;, &quot;MENU&quot;, &quot;HIERARCHY&quot;}' name='flat'/>
          </div>
        </div>
      </div>
    </b:includable>
    <b:includable id='flat'>
      <ul class='flat'>
        <b:loop values='data:data' var='i'>
          <li class='archivedate'>
            <a expr:href='data:i.url'>
              <data:i.name/><span class='post-count'><data:i.post-count/></span>
            </a>
          </li>
        </b:loop>
      </ul>
    </b:includable>
  </b:defaultmarkup>
</b:defaultmarkups>
 
    <b:if cond='data:blog.adsenseClientId and !data:widgets.AdSense.empty'>
      <script async='async' src='//pagead2.googlesyndication.com/pagead/js/adsbygoogle.js'/>
    </b:if>

    <script async='async' src='//www.gstatic.com/external_hosted/clipboardjs/clipboard.min.js'/>

</head>
<body expr:class='data:blog.pageType'>

<div id='fb-root'/>
<script async='async' crossorigin='anonymous' defer='defer' src='https://connect.facebook.net/en_US/sdk.js#xfbml=1&amp;version=v5.0'/>

  <b:class cond='data:view.isHomepage' name='home'/>
  <b:class cond='data:view.isPage' name='item'/>
  <b:class cond='data:view.isArchive' name='index'/>
  <b:class cond='data:view.isError' name='error404'/>

<!-- Theme Options -->
  <div class='theme-options' style='display:none'>
    <b:section class='jet-panel' id='jet-panel' maxwidgets='1' name='Theme Options' showaddelement='no'>
      <b:widget id='LinkList69' locked='true' title='Payment Options' type='LinkList' version='2' visible='true'>
        <b:widget-settings>
          <b:widget-setting name='sorting'>NONE</b:widget-setting>
          <b:widget-setting name='text-1'>paymentOption</b:widget-setting>
          <b:widget-setting name='link-1'>PayPal</b:widget-setting>
          <b:widget-setting name='text-0'>Online Souq Store</b:widget-setting>
          <b:widget-setting name='link-2'>USD</b:widget-setting>
          <b:widget-setting name='link-0'>youremail@hotmail.com</b:widget-setting>
          <b:widget-setting name='text-2'>currencyOption</b:widget-setting>
        </b:widget-settings>
        <b:includable id='main'>
          <b:include name='content'/>
        </b:includable>
        <b:includable id='content'>
          &lt;script type=&#39;text/javascript&#39;&gt;
          //&lt;![CDATA[
          <b:loop values='data:links' var='link'>
            <b:if cond='data:link.name == &quot;paymentOption&quot;'>
              var paymentOption = &quot;<data:link.target/>&quot;;
            </b:if>
            <b:if cond='data:link.name == &quot;paypalMail&quot;'>
              var paypalMail = &quot;<data:link.target/>&quot;;
            </b:if>
            <b:if cond='data:link.name == &quot;currencyOption&quot;'>
              var currencyOption = &quot;<data:link.target/>&quot;;
            </b:if>
          </b:loop>
          //]]&gt;
          &lt;/script&gt;
        </b:includable>
      </b:widget>
    </b:section>
  </div>

  <div class='ct-wrapper'>

     <b:with value='data:widgets.AdSense any (w =&gt; w.sectionId == &quot;ads&quot;)' var='hasVerticalAds'>

          <b:class cond='data:hasVerticalAds' name='vertical-ads'/>

<div class='tred'>

<div class='contained'>
  
  
<div class='slogy'>

<!-- Social Profile Icons -->

Welcome to Souq Ecommerce Store !
  
</div>

<ul class='cates'>

<!-- Customize Top Menu Here -->

<li class='bhider'><a href=''><i class='fa fa-map-marker'/> Store Location</a></li>   

<li class='hider'><a href=''><i class='fa fa-headphones'/> Help Center</a></li>   

<li><a href=''><i class='fa fa-mobile'/> Download App</a></li>   

</ul>

</div>

</div>
<div class='clear'/>
       
<header class='header-wrapper' role='banner'>

<div class='contained'>

<div class='topper'>

   <b:section class='header-logo' id='header' name='Header' showaddelement='false'>
     <b:widget id='Header1' locked='true' title='Souq Store (Header)' type='Header' version='2' visible='true'>
       <b:widget-settings>
         <b:widget-setting name='displayUrl'>http://2.bp.blogspot.com/-h2balztxoeQ/XqCKw8ggy0I/AAAAAAAABcw/_XdiPWOPxMg19Qagad0nNiLPLB1Xg--GgCK4BGAYYCw/s1600/logo-souqstore.png</b:widget-setting>
         <b:widget-setting name='displayHeight'>47</b:widget-setting>
         <b:widget-setting name='sectionWidth'>368</b:widget-setting>
         <b:widget-setting name='useImage'>true</b:widget-setting>
         <b:widget-setting name='shrinkToFit'>false</b:widget-setting>
         <b:widget-setting name='imagePlacement'>REPLACE</b:widget-setting>
         <b:widget-setting name='displayWidth'>208</b:widget-setting>
       </b:widget-settings>
       <b:includable id='main' var='this'>
    <div class='header-widget'>
      <b:include cond='data:imagePlacement in {&quot;REPLACE&quot;, &quot;BEFORE_DESCRIPTION&quot;}' name='image'/>
      <b:include cond='data:imagePlacement not in {&quot;REPLACE&quot;, &quot;BEFORE_DESCRIPTION&quot;}' name='title'/>
      <b:include cond='data:imagePlacement != &quot;REPLACE&quot;' name='description'/>
    </div>
    <b:include cond='data:imagePlacement == &quot;BEHIND&quot;' name='behindImageStyle'/>
  </b:includable>
       <b:includable id='behindImageStyle'>
    <b:if cond='data:sourceUrl'>
      <b:include cond='data:this.image' data='{                    image: data:this.image,                    selector: &quot;.header-widget&quot;                  }' name='responsiveImageStyle'/>
      <style type='text/css'>
        .header-widget {
          background-position: <data:blog.locale.languageAlignment/>;
          background-repeat: no-repeat;
        }
      </style>
    </b:if>
  </b:includable>
       <b:includable id='description'>
          <!-- Don't show description on the item page -->
          <b:include cond='not data:view.isSingleItem' name='super.description'/>
        </b:includable>
       <b:includable id='image'>
      <a class='header-image-wrapper' expr:href='data:blog.homepageUrl'>
        <img expr:alt='data:blog.title.escaped' expr:data-height='data:height' expr:data-width='data:width' expr:src='data:image'/>
      </a>
          <!-- If we are replacing the title, force it to render anyway, and it'll be hidden in CSS. -->
        </b:includable>
       <b:includable id='title'>

<b:if cond='data:blog.pageType != &quot;item&quot;'>
<b:if cond='data:blog.pageType != &quot;static_page&quot;'>
    <h1>
      <b:tag expr:href='data:blog.homepageUrl' expr:title='data:blog.title' itemprop='url' name='a' rel='bookmark'>
        <span itemprop='headline'><data:title/></span>
      </b:tag>
    </h1>
<b:else/>
    <h2>
      <b:tag expr:href='data:blog.homepageUrl' expr:title='data:blog.title' itemprop='url' name='a' rel='bookmark'>
        <span itemprop='headline'><data:title/></span>
      </b:tag>
    </h2>
</b:if>
<b:else/>
    <h2>
      <b:tag expr:href='data:blog.homepageUrl' expr:title='data:blog.title' itemprop='url' name='a' rel='bookmark'>
        <span itemprop='headline'><data:title/></span>
      </b:tag>
    </h2>
</b:if>

        </b:includable>
     </b:widget>
   </b:section>

<li class='tabmid search'>
<b:section id='search_top' name='Search (Top)' showaddelement='false'>
  <b:widget id='BlogSearch1' locked='true' title='Search This Blog' type='BlogSearch' version='2' visible='true'>
    <b:includable id='main'>
<b:include name='content'/>
</b:includable>
    <b:includable id='content'>
<div class='widget-content' role='search'>
<b:include name='searchForm'/>
</div>
</b:includable>
    <b:includable id='searchForm'>
<form expr:action='data:blog.searchUrl'>
<b:attr cond='not data:view.isPreview' name='target' value='_top'/>
<b:include name='urlParamsAsFormInput'/>
<div class='search-input'>
<input aria-label='Search for Products' autocomplete='off' expr:value='data:view.isSearch ? data:view.search.query.escaped : &quot;&quot;' name='q' placeholder='Search for Products'/>
</div>
<b:include name='searchSubmit'/>
</form>
</b:includable>
    <b:includable id='searchSubmit'>
<b:if cond='data:widget.sectionId == &quot;search_top&quot;'>
<label class='search-submit-container'>
<button title='search' type='submit'>Search</button>
</label>
<b:else/>
<b:include name='super.searchSubmit'/>
</b:if>
</b:includable>
  </b:widget>
</b:section>
</li>

<ul class='menu-page'>

<!-- Top menu links -->

<li class='view-art'><a href='/p/cart.html'>View cart</a></li>

          <li class='my-cart'>
            <a class='cart-details'><i class='fa fa-shopping-cart'/>
              <span class='simpleCart_quantity'>0</span>
            </a>
            <div class='cart-description'>
              <div class='simpleCart_items'/>
              <div class='cart-buttons-wrap'>
                <div class='cart-amount'><span class='cart-subtotal'>SUBTOTAL :</span><span class='simpleCart_total'/></div>
                <div class='cart-buttons'>
                  <a class='simpleCart_empty' href='javascript:;'><span>Empty cart</span></a><a class='simpleCart_checkout' href='/p/checkout.html'><span><i class='fa fa-credit-card'/> Checkout</span></a>
                </div>
              </div>
            </div>
          </li>

</ul>
</div><!-- topper -->

</div><!--Div Contained-->

            </header>
      <div class='clear'/>

<div class='menu-bg'>
<div class='contained'>

  <a class='menu-btn' href='#menu'> <div class='hamburger'><div/></div> Menu</a>
		
<nav class='menu' id='menu'>
<ul class='megamenu' id='megamenuid'>

<li><a expr:href='data:blog.homepageUrl'>Home</a></li>

<li class='with-ul'><a href='#'>Fashion</a>
<ul>
<li><a href='https://souqstore-bloggertheme9.blogspot.com/search/label/Men'>Men</a></li>
<li><a href='https://souqstore-bloggertheme9.blogspot.com/search/label/Women'>Women</a></li>
<li><a href='https://souqstore-bloggertheme9.blogspot.com/search/label/Gadgets'>Gadgets</a></li>
<li><a href='https://souqstore-bloggertheme9.blogspot.com/search/label/Furniture'>Furniture</a></li>
</ul>
</li>

<li><a href='https://souqstore-bloggertheme9.blogspot.com/2020/04/lamp-et-dolorum-fuga-extra-harum-nat.html'>Post right</a></li>

<li><a href='https://souqstore-bloggertheme9.blogspot.com/2020/04/illo-inventore-veritatis-et-salvia.html'>Full Width</a></li>

<li><a href='https://souqstore-bloggertheme9.blogspot.com/p/documentation.html'>DOCUMENT</a></li>

<li><a href='#'>Contact</a></li>

</ul>
</nav>

</div>
</div>
<div class='clear'/>

<b:if cond='data:view.isHomepage'>
<!-- slider -->
<div class='contained'>

<div class='slider' id='slider1'>

<div><a href='/'><img src='https://4.bp.blogspot.com/-5MORAWuKZRw/XqryORmehyI/AAAAAAAAACw/UUYNV-J7eGg3910DmKh4qtwSEFHmqThvgCLcBGAsYHQ/s1600/slider1.jpg'/></a></div>

<div><a href='/'><img src='https://3.bp.blogspot.com/-567MuwbssoA/XqryPNo3TRI/AAAAAAAAAC0/3pXHOX0YXsQrOGzF83U3NylLfQhiVz59ACLcBGAsYHQ/s1600/slider2.jpg'/></a></div>

<div><a href='/'><img src='https://2.bp.blogspot.com/-hs0B0U8DN6c/XqryPjYtsRI/AAAAAAAAAC4/5S-fmUGrOLkfIODMEQf-YPnk7ONxkcWBwCLcBGAsYHQ/s1600/slider3.jpg'/></a></div>

<div><a href='/'><img src='https://2.bp.blogspot.com/-hDA_sao7SCA/XqryRGSxL2I/AAAAAAAAADA/vNVFali1LxELrwmSqTqqQOCqzol2s7WuACLcBGAsYHQ/s1600/slider5.jpg'/></a></div>

<div><a href='/'><img src='https://3.bp.blogspot.com/--4VmFDfN74M/XqryQceFnZI/AAAAAAAAAC8/uLGPLBPbEdE0Zw9LyNWz0j4pfIaznC1MgCLcBGAsYHQ/s1600/slider4.jpg'/></a></div>

    <!-- The Arrows -->
<i class='arrows left' style=''><svg viewBox='0 0 100 100'><path d='M 10,50 L 60,100 L 70,90 L 30,50  L 70,10 L 60,0 Z'/></svg></i>
<i class='arrows right' style=''><svg viewBox='0 0 100 100'><path d='M 10,50 L 60,100 L 70,90 L 30,50  L 70,10 L 60,0 Z' transform='translate(100, 100) rotate(180) '/></svg></i>
</div>
<div class='clear'/> 


<div class='dab'>
<div class='bow'>
<b:section class='banner3' id='Ad-1' maxwidgets='1' name='Ad left (side)' showaddelement='yes'>
  <b:widget id='Image3' locked='false' title='Ad banner 1' type='Image' visible='true'>
    <b:widget-settings>
      <b:widget-setting name='displayUrl'>https://1.bp.blogspot.com/-upFxPuToXrA/Xo3Lx9w16kI/AAAAAAAABT8/nXg7c-HSy14ZAN6lNjZoZ7nWzahRXpeTgCLcBGAsYHQ/s1600/ad1.png</b:widget-setting>
      <b:widget-setting name='displayHeight'>190</b:widget-setting>
      <b:widget-setting name='sectionWidth'>170</b:widget-setting>
      <b:widget-setting name='shrinkToFit'>false</b:widget-setting>
      <b:widget-setting name='displayWidth'>365</b:widget-setting>
      <b:widget-setting name='link'>/</b:widget-setting>
      <b:widget-setting name='caption'>banner</b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <b:include name='widget-title'/>
  <b:include name='content'/>
</b:includable>
    <b:includable id='content'>
  <div class='widget-content'>
    <b:tag cond='data:link' expr:href='data:link' name='a'>
      <img expr:alt='data:title' expr:height='data:height' expr:id='data:widget.instanceId + &quot;_img&quot;' expr:src='data:sourceUrl' expr:width='data:width'>
        <b:attr cond='data:sourceSet' expr:value='data:sourceSet' name='srcset'/>
      </img>
    </b:tag>
    <br/>
    <b:if cond='data:caption'>
      <span class='caption'><data:caption/></span>
    </b:if>
  </div>
</b:includable>
  </b:widget>
</b:section>
<b:section class='banner3' id='Ad-2' maxwidgets='1' name='Ad bottom' showaddelement='yes'>
  <b:widget id='Image4' locked='false' title='Ad banner 2' type='Image' visible='true'>
    <b:widget-settings>
      <b:widget-setting name='displayUrl'>https://3.bp.blogspot.com/-EsdQ1NSYGso/Xo3MIzXnV-I/AAAAAAAABUE/2Aad4q4FVNU8OF1bYNmaYViWfI1g1kqtwCLcBGAsYHQ/s1600/ad2.png</b:widget-setting>
      <b:widget-setting name='displayHeight'>190</b:widget-setting>
      <b:widget-setting name='sectionWidth'>171</b:widget-setting>
      <b:widget-setting name='shrinkToFit'>false</b:widget-setting>
      <b:widget-setting name='displayWidth'>365</b:widget-setting>
      <b:widget-setting name='link'>/</b:widget-setting>
      <b:widget-setting name='caption'>banner 2</b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <b:include name='widget-title'/>
  <b:include name='content'/>
</b:includable>
    <b:includable id='content'>
  <div class='widget-content'>
    <b:tag cond='data:link' expr:href='data:link' name='a'>
      <img expr:alt='data:title' expr:height='data:height' expr:id='data:widget.instanceId + &quot;_img&quot;' expr:src='data:sourceUrl' expr:width='data:width'>
        <b:attr cond='data:sourceSet' expr:value='data:sourceSet' name='srcset'/>
      </img>
    </b:tag>
    <br/>
    <b:if cond='data:caption'>
      <span class='caption'><data:caption/></span>
    </b:if>
  </div>
</b:includable>
  </b:widget>
</b:section>

<b:section class='banner3' id='Ad-3' maxwidgets='1' name='Ad right (side)' showaddelement='yes'>
  <b:widget id='Image5' locked='false' title='Ad banner 2' type='Image' visible='true'>
    <b:widget-settings>
      <b:widget-setting name='displayUrl'>https://1.bp.blogspot.com/-Np3ktpYomxs/Xo3MJVGt1XI/AAAAAAAABUI/LQOe4gaoxDQ0rq0-EwF9Hua2ZC87DTyMwCLcBGAsYHQ/s1600/ad3.png</b:widget-setting>
      <b:widget-setting name='displayHeight'>190</b:widget-setting>
      <b:widget-setting name='sectionWidth'>170</b:widget-setting>
      <b:widget-setting name='shrinkToFit'>false</b:widget-setting>
      <b:widget-setting name='displayWidth'>365</b:widget-setting>
      <b:widget-setting name='link'>/</b:widget-setting>
      <b:widget-setting name='caption'>banner 2</b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <b:include name='widget-title'/>
  <b:include name='content'/>
</b:includable>
    <b:includable id='content'>
  <div class='widget-content'>
    <b:tag cond='data:link' expr:href='data:link' name='a'>
      <img expr:alt='data:title' expr:height='data:height' expr:id='data:widget.instanceId + &quot;_img&quot;' expr:src='data:sourceUrl' expr:width='data:width'>
        <b:attr cond='data:sourceSet' expr:value='data:sourceSet' name='srcset'/>
      </img>
    </b:tag>
    <br/>
    <b:if cond='data:caption'>
      <span class='caption'><data:caption/></span>
    </b:if>
  </div>
</b:includable>
  </b:widget>
</b:section>
</div><!-- dab -->
</div><!-- bow -->
<div class='clear'/> 

<section class='gap'>
<div class='contained'>
<div class='bow'>

<div class='fourthing'>
<i aria-hidden='true' class='fa fa-rocket'/>
<div class='ico-fourth'>
<h5>Free Delivery</h5>
<p>We will ship free if your order exceeds $150.</p>
</div>
</div>

<div class='fourthing'>
<i aria-hidden='true' class='fa fa-handshake-o'/>
  <div class='ico-fourth'>
<h5>Money Back</h5>
<p>If goods have problem we&#39;ll return your good.</p>
</div>
</div>

<div class='fourthing'>
  <i aria-hidden='true' class='fa fa-credit-card'/>
<div class='ico-fourth'>
<h5>Secure Payment</h5>
<p>Hassle free 100% secure payment through pay.</p>
</div>
</div>

<div class='fourthing'>
  <i aria-hidden='true' class='fa fa-comments'/>
<div class='ico-fourth'>
<h5>24/7 Support</h5>
  <p>Our dedicated support is available 24/7.</p>
</div>
</div>

</div>
</div><!-- contained -->
</section><div class='clear'/> 

  </div><!-- contained -->
<div class='clear'/>
</b:if>

      <div class='clear'/>

<div class='contained'>

<b:section class='crossy' id='Main-Ad' maxwidgets='1' showaddelement='yes'/>

  <div class='outer-wrapper'>

      <div class='main-wrapper top'>
              <main class='main-container' id='main' role='main' tabindex='-1'>

                <b:if cond='data:view.isMultipleItems'>
                  <h2 class='main-heading'><data:messages.posts/></h2>
                </b:if>

        <b:section class='main' id='page_body' maxwidgets='1' name='Page Body' showaddelement='yes'>
          <b:widget id='Blog1' locked='true' title='Blog Posts' type='Blog' version='2' visible='true'>
            <b:widget-settings>
              <b:widget-setting name='commentLabel'>Comments</b:widget-setting>
              <b:widget-setting name='showShareButtons'>true</b:widget-setting>
              <b:widget-setting name='authorLabel'>by</b:widget-setting>
              <b:widget-setting name='disableGooglePlusShare'>true</b:widget-setting>
              <b:widget-setting name='style.unittype'>TextAndImage</b:widget-setting>
              <b:widget-setting name='timestampLabel'/>
              <b:widget-setting name='reactionsLabel'>Reactions</b:widget-setting>
              <b:widget-setting name='showAuthorProfile'>true</b:widget-setting>
              <b:widget-setting name='style.layout'>1x1</b:widget-setting>
              <b:widget-setting name='showLocation'>false</b:widget-setting>
              <b:widget-setting name='showTimestamp'>true</b:widget-setting>
              <b:widget-setting name='postsPerAd'>1</b:widget-setting>
              <b:widget-setting name='style.bordercolor'>#ffffff</b:widget-setting>
              <b:widget-setting name='backlinksLabel'>Related Products</b:widget-setting>
              <b:widget-setting name='showDateHeader'>false</b:widget-setting>
              <b:widget-setting name='style.textcolor'>#000000</b:widget-setting>
              <b:widget-setting name='showCommentLink'>true</b:widget-setting>
              <b:widget-setting name='style.urlcolor'>#7d4998</b:widget-setting>
              <b:widget-setting name='showAuthor'>true</b:widget-setting>
              <b:widget-setting name='style.linkcolor'>#7d4998</b:widget-setting>
              <b:widget-setting name='style.bgcolor'>#ffffff</b:widget-setting>
              <b:widget-setting name='showLabels'>true</b:widget-setting>
              <b:widget-setting name='postLabelsLabel'>Tags</b:widget-setting>
              <b:widget-setting name='showBacklinks'>true</b:widget-setting>
              <b:widget-setting name='showInlineAds'>false</b:widget-setting>
              <b:widget-setting name='showReactions'>true</b:widget-setting>
            </b:widget-settings>
            <b:includable id='main' var='this'> 

              <b:include name='FilterMessage'/>

              <div class='blog-posts hfeed container'>
                <b:class cond='data:view.isMultipleItems' name='index-post-wrap'/>
                <b:class cond='data:view.isSingleItem' name='item-item-post'/>
                <b:tag class='grid-view' cond='data:view.isMultipleItems' name='div'>
                  <b:loop index='i' values='data:posts' var='post'>
                    <b:include data='post' name='postCommentsAndAd'/>
                  </b:loop>
                </b:tag>
              </div>
              <b:include cond='data:view.isMultipleItems' name='NextPrev'/>
              <b:include name='feedLinks'/>
              <script type='text/javascript'>
                var messages = { 
                  showMore: &quot;<data:messages.showMore/>&quot;
                }
              </script>
            </b:includable>
            <b:includable id='Delate' var='post'>
              <!-- Related Posts -->
                <div id='related-wrap'>
                  <!--<div class='title-wrap'>
                    <h3><data:allBylineItems.backlinks.label/></h3>
                  </div>-->
                  <div class='related-ready bow'>
                    <b:if cond='data:post.labels'>
                      <div class='related-tag' expr:data-label='data:post.labels.first.name'/>
                      <b:else/>
                      <div class='related-tag' data-label='random'/>
                    </b:if>
                  </div> 
                </div>   
            </b:includable>
            <b:includable id='FilterMessage'>

       <b:if cond='data:view.search.query'>
       <div class='post-filter-message'>
       <b:if cond='data:posts.empty'>
       <span class='result'/><data:view.search.resultsMessageHtml/>
       <a class='show-more' expr:href='data:blog.homepageUrl'><data:messages.showAll/></a>
       <b:else/>
       <span class='result'><data:view.search.resultsMessageHtml/></span>
       <a class='show-more' expr:href='data:blog.homepageUrl'><data:messages.showAll/></a>
       </b:if>
       </div>
       </b:if>

       <b:if cond='data:view.search.label'>
       <div class='post-filter-message'>
       <b:if cond='data:posts.empty'>
       <span class='result'><data:view.search.resultsMessageHtml/></span>
       <a class='show-more' expr:href='data:blog.homepageUrl'><data:messages.showAll/></a>
       <b:else/>
       <span class='result'><data:view.search.resultsMessageHtml/></span>
       <a class='show-more' expr:href='data:blog.homepageUrl'><data:messages.showAll/></a>
       </b:if>
       </div>
       </b:if>
       
       <b:if cond='data:view.isArchive'>
       <div class='post-filter-message'>
       <b:if cond='data:posts.empty'>
       <span class='result'><data:view.archive.rangeMessage/></span>
       <a class='show-more' expr:href='data:blog.homepageUrl'><data:messages.showAll/></a>
       <b:else/>
       <span class='result'><data:view.archive.rangeMessage/></span>
       <a class='show-more' expr:href='data:blog.homepageUrl'><data:messages.showAll/></a>
       </b:if>
       </div>
       </b:if>

       <b:if cond='data:view.isError'>
       <div class='error-home'>
       <h3>Page Not Found</h3>
       <h4>The requested page does not exist. We will try to automatically redirect you in 12 seconds.</h4>
       <p>Please go to the <data:blog.title/> home page by clicking the button below.</p>
       <a class='error' expr:href='data:blog.homepageUrl'><data:blog.title/> Home</a>
       </div>
       </b:if>

       <b:if cond='data:view.isMultipleItems and data:posts.empty'>
       <div class='nothing'><data:messages.noResultsFound/></div>
       </b:if>
    
        
    </b:includable>
            <b:includable id='NextPrev'>
              <!-- Post Pagination Index -->
              <div class='blog-pager container' id='blog-pager'>
                <b:include cond='data:newerPageUrl' name='previousPageLink'/>
                <b:include cond='data:olderPageUrl' name='nextPageLink'/>
                <b:include cond='data:view.url != data:blog.homepageUrl' name='homePageLink'/>
              </div>
            </b:includable>
            <b:includable id='PostArticle' var='post'>
              <!-- Item Post Content -->
              <b:include data='post' name='postMeta'/>
              <b:include data='post' name='postHeader'/>
              <b:include data='post' name='postBody'/>
              <b:include cond='data:view.isPost' data='post' name='postFooter'/>
            </b:includable>
            <b:includable id='PostTime' var='post'>
              <b:if cond='data:allBylineItems.timestamp'>
                <span class='post-date published' expr:datetime='data:post.date.iso8601'><data:post.date/></span>
              </b:if>
            </b:includable>
            <b:includable id='aboutPostAuthor'>

        <div class='about-author'>
        <b:if cond='data:post.author.authorPhoto.image'>
        <img class='author-avatar' expr:alt='data:post.author.name' expr:src='data:post.author.authorPhoto.image resizeImage 100'/>               <b:else/>
        <img class='author-avatar' expr:alt='data:post.author.name' src='https://1.bp.blogspot.com/-bcG0duKLi0U/XH5uKJyOs3I/AAAAAAAAA8c/939x6jQXytcaLhV8Q0oJsqMW3BVNirZrgCLcBGAs/s100/admin-logo.jpg'/>
        </b:if>
        <h5>
        <span><data:messages.postedBy/></span>
        <a expr:alt='data:post.author.name' expr:href='data:post.author.profileUrl' target='_blank'> <data:post.author.name/></a>
        </h5>
        <span class='author-description'><data:post.author.aboutMe/></span>
        </div>

            </b:includable>
            <b:includable id='addComments'>
              <a expr:href='data:post.commentsUrl' expr:onclick='data:post.commentsUrlOnclick'>
                <b:message name='messages.postAComment'/>
              </a>
            </b:includable>
            <b:includable id='backLinks' var='post'>
              <b:comment>Disabled</b:comment>         
            </b:includable>
            <b:includable id='blogThisShare'>
  <b:with value='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=270,width=475\&quot;); return false;&quot;' var='onclick'>
    <b:include name='platformShare'/>
  </b:with>
</b:includable>
            <b:includable id='breadcrumb' var='post'>
      <b:if cond='data:blog.homepageUrl != data:blog.url'>
      <b:if cond='data:blog.pageType == &quot;static_page&quot;'>
      <div class='breadcrumbs'><span class='breadlabel'><data:blog.pageName/></span></div>
      <b:else/>
      <b:if cond='data:blog.pageType == &quot;item&quot;'>
      <!-- breadcrumb for the post page -->
      <b:loop values='data:posts' var='post'>
      <b:if cond='data:post.labels'>
      <div class='breadcrumbs' xmlns:v='http://rdf.data-vocabulary.org/#'>
      
<b:loop values='data:post.labels' var='label'>
      <span class='breadlabel' typeof='v:Breadcrumb'><a expr:href='data:label.url + &quot;?&amp;amp;max-results=7&quot;' property='v:title' rel='v:url'><data:label.name/></a> </span>
      </b:loop>
      </div>
      <b:else/>
      <div class='breadcrumbs'><span class='breadhome'><a expr:href='data:blog.homepageUrl' rel='tag'>Home</a> </span><span class='breadlabel'>Unlabelled</span> <span class='breadlabel'><data:post.title/></span></div>
      </b:if>
      </b:loop>
      <b:else/>
      <b:if cond='data:blog.pageType == &quot;archive&quot;'>
      <!-- breadcrumb for the label archive page and search pages.. -->
      <div class='breadcrumbs'>
        <span class='breadhome'><a expr:href='data:blog.homepageUrl'>Home </a> </span><span>Archives for <data:blog.pageName/></span>
      </div>
      <b:else/>
      <b:if cond='data:blog.pageType == &quot;index&quot;'>
      <div class='breadcrumbs'>
      <b:if cond='data:blog.pageName == &quot;&quot;'>
        <span class='breadhome'><a expr:href='data:blog.homepageUrl'>Home</a> </span><span class='breadlabel'>All posts </span>
      <b:else/>
        <span class='breadhome'> <a expr:href='data:blog.homepageUrl'>Home</a> </span><span class='breadlabel'>Posts filed under <data:blog.pageName/></span>
      </b:if>
      </div>
      </b:if>
      </b:if>
      </b:if>
      </b:if>
      </b:if>
            </b:includable>
            <b:includable id='bylineByName' var='byline'>
  <b:switch var='data:byline.name'>
  <b:case value='share'/>
    <b:include cond='data:post.shareUrl' name='postShareButtons'/>
  <b:case value='comments'/>
    <b:include cond='data:post.allowComments' name='postCommentsLink'/>
  <b:case value='location'/>
    <b:include cond='data:post.location' name='postLocation'/>
  <b:case value='timestamp'/>
    <b:include cond='not data:view.isPage' name='postTimestamp'/>
  <b:case value='author'/>
    <b:include name='postAuthor'/>
  <b:case value='labels'/>
    <b:include cond='data:post.labels' name='postLabels'/>
  <b:case value='icons'/>
    <b:include cond='data:post.emailPostUrl' name='emailPostIcon'/>
  <b:case value='reactions'/>
    <b:include cond='data:post.reactionsUrl' name='postReactions'/>
  </b:switch>
</b:includable>
            <b:includable id='bylineRegion' var='regionItems'>
  <b:loop values='data:regionItems' var='byline'>
    <b:include data='byline' name='bylineByName'/>
  </b:loop>
</b:includable>
            <b:includable id='commentAuthorAvatar'>
              <div class='avatar-image-container'>
                <img class='author-avatar' expr:src='data:comment.authorAvatarSrc' height='45' width='45'/>
              </div>
            </b:includable>
            <b:includable id='commentDeleteIcon' var='comment'>
              <span expr:class='&quot;item-control &quot; + data:comment.adminClass'>
                <b:if cond='data:showCmtPopup'>
                  <div class='goog-toggle-button'>
                    <div class='goog-inline-block comment-action-icon'/>
                  </div>
                  <b:else/>
                  <a class='comment-delete' expr:href='data:comment.deleteUrl' expr:title='data:messages.deleteComment'>
                    <img src='https://resources.blogblog.com/img/icon_delete13.gif'/>
                  </a>
                </b:if>
              </span>
            </b:includable>
            <b:includable id='commentForm' var='post'>
              <div class='comment-form'>
                <a name='comment-form'/>
                <b:if cond='data:this.messages.blogComment != &quot;&quot;'>
                  <p><data:this.messages.blogComment/></p>
                </b:if>
                <b:include data='post' name='commentFormIframeSrc'/>
                <iframe allowtransparency='allowtransparency' class='blogger-iframe-colorize blogger-comment-from-post' expr:height='data:cmtIframeInitialHeight ?: &quot;90px&quot;' frameborder='0' id='comment-editor' name='comment-editor' src='' width='100%'/>
                <data:post.cmtfpIframe/>
                <script type='text/javascript'>
                  BLOG_CMT_createIframe(&#39;<data:post.appRpcRelayPath/>&#39;);
                </script>
              </div>
            </b:includable>
            <b:includable id='commentFormIframeSrc' var='post'>
              <a expr:href='data:post.commentFormIframeSrc + &quot;&amp;skin=contempo&quot;' id='comment-editor-src'/>
            </b:includable>
            <b:includable id='commentItem' var='comment'>
              <div class='comment' expr:id='&quot;c&quot; + data:comment.id'>
                <b:include cond='data:blog.enabledCommentProfileImages' name='commentAuthorAvatar'/>

                <div class='comment-block'>
                  <div class='comment-author'>
                    <b:if cond='data:comment.authorUrl'>
                      <b:message name='messages.authorSaidWithLink'>
                        <b:param expr:value='data:comment.author' name='authorName'/>
                        <b:param expr:value='data:comment.authorUrl' name='authorUrl'/>
                      </b:message>
                      <b:else/>
                      <b:message name='messages.authorSaid'>
                        <b:param expr:value='data:comment.author' name='authorName'/>
                      </b:message>
                    </b:if>
                  </div>
                  <div expr:class='&quot;comment-body&quot; + (data:comment.isDeleted ? &quot; deleted&quot; : &quot;&quot;)'>
                    <data:comment.body/>
                  </div>
                  <div class='comment-footer'>
                    <span class='comment-timestamp'>
                      <a expr:href='data:comment.url' title='comment permalink'>
                        <data:comment.timestamp/>
                      </a>
                      <b:include data='comment' name='commentDeleteIcon'/>
                    </span>
                  </div>
                </div>
              </div>
            </b:includable>
            <b:includable id='commentList' var='comments'>
              <div id='comments-block'>
                <b:loop values='data:comments' var='comment'>
                  <b:include data='comment' name='commentItem'/>
                </b:loop>
              </div>
            </b:includable>
            <b:includable id='commentPicker' var='post'>
              <b:if cond='data:post.commentSource == 1'>
                <b:include data='post' name='iframeComments'/>
                <b:elseif cond='data:post.showThreadedComments'/>
                <b:include data='post' name='threadedComments'/>
                <b:else/>
                <b:include data='post' name='comments'/>
              </b:if>
            </b:includable>
            <b:includable id='comments' var='post'>
              <section expr:class='&quot;comments&quot; + (data:post.embedCommentForm ? &quot; embed&quot; : &quot;&quot;)' expr:data-num-comments='data:post.numberOfComments' id='comments'>
                <a name='comments'/>
                <b:if cond='data:post.allowComments'>

                  <b:include name='commentsTitle'/>

                  <div expr:id='data:widget.instanceId + &quot;_comments-block-wrapper&quot;'>
                    <b:include cond='data:post.comments' data='post.comments' name='commentList'/>
                  </div>

                  <b:if cond='data:post.commentPagingRequired'>
                    <div class='paging-control-container'>
                      <b:if cond='data:post.hasOlderLinks'>
                        <a expr:class='data:post.oldLinkClass' expr:href='data:post.oldestLinkUrl'>
                          <data:messages.oldest/>
                        </a>
                        <a expr:class='data:post.oldLinkClass' expr:href='data:post.olderLinkUrl'>
                          <data:messages.older/>
                        </a>
                      </b:if>

                      <span class='comment-range-text'>
                        <data:post.commentRangeText/>
                      </span>

                      <b:if cond='data:post.hasNewerLinks'>
                        <a expr:class='data:post.newLinkClass' expr:href='data:post.newerLinkUrl'>
                          <data:messages.newer/>
                        </a>
                        <a expr:class='data:post.newLinkClass' expr:href='data:post.newestLinkUrl'>
                          <data:messages.newest/>
                        </a>
                      </b:if>
                    </div>
                  </b:if>

                  <div class='footer99'>
                    <b:if cond='data:post.embedCommentForm'>
                      <b:if cond='data:post.allowNewComments'>
                        <b:include data='post' name='commentForm'/>
                        <b:else/>
                        <data:post.noNewCommentsText/>
                      </b:if>
                      <b:else/>
                      <b:if cond='data:post.allowComments'>
                        <b:include data='post' name='addComments'/>
                      </b:if>
                    </b:if>
                  </div>
                </b:if>
                <b:if cond='data:showCmtPopup'>
                  <div id='comment-popup'>
                    <iframe allowtransparency='allowtransparency' frameborder='0' id='comment-actions' name='comment-actions' scrolling='no'>
                    </iframe>
                  </div>
                </b:if> 
              </section>
            </b:includable>
            <b:includable id='commentsLink'>
  <a class='comment-link' expr:href='data:post.commentsUrl' expr:onclick='data:post.commentsUrlOnclick'>
    <b:if cond='data:post.numberOfComments &gt; 0'>
      <b:message name='messages.numberOfComments'>
        <b:param expr:value='data:post.numberOfComments' name='numComments'/>
      </b:message>
    <b:else/>
      <data:messages.postAComment/>
    </b:if>
  </a>
</b:includable>
            <b:includable id='commentsLinkIframe'>
  <span class='cmt_count_iframe_holder' expr:data-count='data:post.numberOfComments' expr:data-onclick='data:post.commentsUrlOnclick' expr:data-post-url='data:post.url' expr:data-url='data:post.url.canonical.http'>
  </span>
</b:includable>
            <b:includable id='commentsTitle'>
              <!-- Post Commments Title -->
              <h5><data:post.numberOfComments/> Reviews</h5>

              <h6>Your rating</h6>

<fieldset class='rating'>
    <input id='star5' name='rating' type='radio' value='5'/><label class='full' for='star5' title='Awesome - 5 stars'/>
      <input id='star4' name='rating' type='radio' value='4'/><label class='full' for='star4' title='Pretty good - 4 stars'/>
    <input id='star3' name='rating' type='radio' value='3'/><label class='full' for='star3' title='Meh - 3 stars'/>
    <input id='star2' name='rating' type='radio' value='2'/><label class='full' for='star2' title='Kinda bad - 2 stars'/>
    <input id='star1' name='rating' type='radio' value='1'/><label class='full' for='star1' title='Sucks big time - 1 star'/>
</fieldset>

            </b:includable>
            <b:includable id='defaultAdUnit'>
          <!-- Clear out style (need non-empty string) -->
          <b:with value='&quot;/* Done in css. */&quot;' var='style'>
            <b:include name='super.defaultAdUnit'/>
          </b:with>
   </b:includable>
            <b:includable id='emailPostIcon'>
  <span class='byline post-icons'>
    <!-- email post links -->
    <span class='item-action'>
      <a expr:href='data:post.emailPostUrl' expr:title='data:messages.emailPost'>
        <b:include data='{ iconClass: &quot;touch-icon sharing-icon&quot; }' name='emailIcon'/>
      </a>
    </span>
  </span>
</b:includable>
            <b:includable id='facebookShare'>
  <b:with value='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=430,width=640\&quot;); return false;&quot;' var='onclick'>
    <b:include name='platformShare'/>
  </b:with>
</b:includable>
            <b:includable id='feedLinks'>
              <b:comment>Disabled</b:comment> 
            </b:includable>
            <b:includable id='feedLinksBody' var='links'>
              <b:comment>Disabled</b:comment> 
            </b:includable>
            <b:includable id='footerBylines' var='post'>
              <!-- Post tags category label here -->
              <!-- <b:include data='post' name='postLabels'/> -->
            </b:includable>
            <b:includable id='googlePlusShare'>
  <div class='goog-inline-block google-plus-share-container'>
    <g:plusone annotation='inline' expr:href='data:originalUrl.canonical.http' size='medium' source='blogger:blog:plusone'/>
  </div>
</b:includable>
            <b:includable id='headerByline' var='post'>
              <!-- Post Header Meta -->
                <!-- <div class='title-secondary'>

                </div>-->

<b:if cond='data:view.isSingleItem'>

<!-- Show Ads Below Post Title -->

</b:if>

            </b:includable>
            <b:includable id='homePageLink'>
              <b:comment>Disabled</b:comment> 
            </b:includable>
            <b:includable id='iframeComments' var='post'>
              <b:if cond='data:post.allowIframeComments'>
                <script expr:src='data:post.iframeCommentSrc' type='text/javascript'/>
                <div class='cmt_iframe_holder' expr:data-href='data:post.url.canonical' expr:data-viewtype='data:post.viewType'/>
                <b:if cond='!data:post.embedCommentForm'>
                  <b:include data='post' name='commentsLink'/>
                </b:if>
              </b:if>
            </b:includable>
            <b:includable id='indexPost' var='post'>
              <!-- Index Post Content -->
              <div class='index-product-inner'>
                <b:include data='post' name='postFeaturedImage'/>
                <div class='product-info'>
                  <b:include data='post' name='postHeader'/>
<div class='product_item_price item_price'>

  <span class='product_price meta-price'/>

 <a class='item_add' href='javascript:;' title='Add to cart'>
 <span class='add_product'>
 <i class='fa fa-cart-plus'/>Add to Cart</span>
 <span class='product_added'>
 <i class='fa fa-check'/>Product Added</span>
 </a>
 </div>
                  
</div>
              </div>
            </b:includable>
            <b:includable id='inlineAd' var='post'>
              <b:comment>Disabled</b:comment> 
            </b:includable>
            <b:includable id='itemPost' var='post'>
              <!-- Item Post Content -->
              <b:include data='post' name='postMeta'/>
              <b:if cond='data:view.isPost'>
                <div class='product-header'>
                  <div class='col-left'>
                    <div class='post-image-wrap item_image'>
                      <b:if cond='data:post.featuredImage'> 
                        <img class='post-thumb item_thumb' expr:alt='data:post.title' expr:src='data:post.featuredImage resizeImage 680'/>
                        <b:else/>
                        <img class='post-thumb item_thumb' expr:alt='data:post.title' src='https://4.bp.blogspot.com/-O3EpVMWcoKw/WxY6-6I4--I/AAAAAAAAB2s/KzC0FqUQtkMdw7VzT6oOR_8vbZO6EJc-ACK4BGAYYCw/w680/nth.png'/>
                      </b:if>
                      <span class='product_off'/>
                    </div>
                  </div>
<div class='col-right'>

<b:include cond='data:view.isPost' data='post' name='breadcrumb'/>

<h1 class='post-title item_name'><data:post.title/>
</h1>

<div class='product_item_price item_price'><div class='tier-price product_price meta-price'/></div>

<div class='reviews'>
<i class='fa fa-star checked'/>
<i class='fa fa-star checked'/>
<i class='fa fa-star checked'/>
<i class='fa fa-star'/>
<i class='fa fa-star'/>
(<data:post.numberOfComments/> customer review)
</div>

                    <div class='product-buy-buttons'>
                      <a class='item_add' href='javascript:;'><span class='add_product'>Add to Cart</span><span class='product_added'><i class='fa fa-check'/> Item added</span></a>
                      <a class='cart-payment' href='/p/checkout.html'><i class='fa fa-credit-card'/>Checkout</a>
                    </div>
                    <b:include data='post' name='postLabels'/>
                    <b:include data='post' name='postShareButtons'/>
                  </div>
                </div>
              </b:if>
              <b:if cond='data:view.isPage'>
                <h1 class='post-title'>
                  <data:post.title/>
                </h1>
              </b:if>
              <b:include data='post' name='postBody'/>
              <b:include cond='data:view.isPost' data='post' name='postFooter'/>
            </b:includable>
            <b:includable id='linkShare'>
  <b:with value='&quot;window.prompt(\&quot;Copy to clipboard: Ctrl+C, Enter\&quot;, \&quot;&quot; + data:originalUrl + &quot;\&quot;); return false;&quot;' var='onclick'>
    <b:include name='platformShare'/>
  </b:with>
</b:includable>
            <b:includable id='nextPageLink'>
              <a class='blog-pager-older-link' expr:href='data:olderPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-older-link&quot;' expr:title='data:messages.olderPosts'>
                <data:messages.olderPosts/>
              </a>
            </b:includable>
            <b:includable id='otherSharingButton'>
  <span class='sharing-platform-button sharing-element-other' expr:aria-label='data:messages.shareToOtherApps.escaped' expr:data-url='data:originalUrl' expr:title='data:messages.shareToOtherApps.escaped' role='menuitem' tabindex='-1'>
    <b:with value='{key: &quot;sharingOther&quot;}' var='platform'>
      <b:include name='sharingPlatformIcon'/>
    </b:with>
    <span class='platform-sharing-text'><data:messages.shareOtherApps.escaped/></span>
  </span>
</b:includable>
            <b:includable id='platformShare'>
  <a expr:class='&quot;goog-inline-block sharing-&quot; + data:platform.key' expr:data-url='data:originalUrl' expr:href='data:shareUrl + &quot;&amp;target=&quot; + data:platform.target' expr:onclick='data:onclick ? data:onclick : &quot;&quot;' expr:title='data:platform.shareMessage' target='_blank'>
    <span class='share-button-link-text'>
      <data:platform.shareMessage/>
    </span>
  </a>
</b:includable>
            <b:includable id='post' var='post'>
              <!-- Post Index -->
              <b:if cond='data:view.isMultipleItems'>
                <b:include data='post' name='indexPost'/>
              </b:if>
              <!-- Post Item -->
              <b:if cond='data:view.isSingleItem'>
                <b:include data='post' name='itemPost'/>
              </b:if>
            </b:includable>
            <b:includable id='postAuthor' var='post'>
              <!-- Post Author -->
              <b:if cond='data:allBylineItems.author'>
                <span class='post-author'><b:if cond='data:post.author.authorPhoto.image'><img class='post-author-avatar' expr:alt='data:post.author.name' expr:src='resizeImage(data:post.author.authorPhoto.image, 50)'/></b:if><a expr:href='data:post.author.profileUrl' expr:title='data:post.author.name' target='_blank'><data:post.author.name/></a></span>
              </b:if>
            </b:includable>
            <b:includable id='postBody' var='post'> 
              <!-- Post Body Entry Content-->
              <div class='post-body post-content'>
                <data:post.body/>
              </div>
            </b:includable>
            <b:includable id='postBodySnippet' var='post'>
              <b:include data='post' name='postBody'/>
            </b:includable>
            <b:includable id='postCommentsAndAd' var='post'>
              <!-- Post, Comments and Ads -->
              <!-- Post Content Index and Item -->
              <div class='blog-post hentry simpleCart_shelfItem'>
         <!-- ecommerce changes -->
                <b:class cond='data:view.isMultipleItems' name='index-post post-shop-info'/>
                <b:class cond='data:view.isSingleItem' name='item-post'/>
                <b:class cond='data:view.isPost' name='product-post'/>
                <b:attr cond='data:view.isMultipleItems' expr:value='data:post.id' name='data-id'/>

                <b:include data='post' name='post'/>
              </div>
              <!-- Comments -->
              <b:if cond='data:view.isSingleItem'>
                <div class='blog-post-comments'>
    <!-- old comments form here -->     
                </div>
              </b:if>
            </b:includable>
            <b:includable id='postCommentsLink'>
              <b:if cond='data:view.isMultipleItems'>
                <span class='byline post-comment-link container'>
                  <b:include cond='data:post.commentSource != 1' name='commentsLink'/>
                  <b:include cond='data:post.commentSource == 1' name='commentsLinkIframe'/>
                </span>
              </b:if>
            </b:includable>
            <b:includable id='postFeaturedImage' var='post'>
              <!-- Post Featured Image on Index -->
              <div class='post-image-wrap item_image'>
                <a class='post-image-link' expr:href='data:post.url'>
                  <b:if cond='data:post.featuredImage'> 
                    <img class='post-thumb item_thumb' expr:alt='data:post.title' expr:src='data:post.featuredImage resizeImage 680'/>
                    <b:else/>
                    <img class='post-thumb item_thumb' expr:alt='data:post.title' src='https://4.bp.blogspot.com/-O3EpVMWcoKw/WxY6-6I4--I/AAAAAAAAB2s/KzC0FqUQtkMdw7VzT6oOR_8vbZO6EJc-ACK4BGAYYCw/w680/nth.png'/>
                  </b:if>
                </a>
                <span class='product_off'/>
              </div>
            </b:includable>
            <b:includable id='postFooter' var='post'>
              
              <div class='post-footer'>
                <!-- Item added below posts -->
                <b:include data='post' name='footerBylines'/>
                <b:include cond='data:allBylineItems.icons' data='post' name='postNavigation'/>

<div class='js-tabs'>

<div class='tabs'>
<a class='tab active' href='#starks-panel' id='starks-tab'>Related Products</a>
<a class='tab' href='#lannisters-panel' id='lannisters-tab'><data:post.numberOfComments/> Reviews</a>
</div>

<div class='panels'>
<ul class='panel active' id='starks-panel'>
<b:include cond='data:allBylineItems.backlinks' data='post' name='Delate'/>
        </ul>
        <ul class='panel' id='lannisters-panel'>
            
<b:include data='post' name='commentPicker'/>
        </ul>
    </div>

</div>

              </div>

            </b:includable>
            <b:includable id='postFooterAuthorProfile' var='post'>
              <b:comment>Disabled</b:comment>   
            </b:includable>
            <b:includable id='postHeader' var='post'>
              <b:include cond='data:view.isPost' data='post' name='tagspost'/>
              <b:include data='post' name='postTitle'/>
              <b:include cond='!data:view.isPage' data='post' name='headerByline'/>
            </b:includable>
            <b:includable id='postJumpLink' var='post'>
              <b:comment>Disabled</b:comment>
            </b:includable>
            <b:includable id='postLabels' var='post'>
              <b:if cond='data:allBylineItems.labels'>
                <b:if cond='data:post.labels'>
                  <div class='post-labels'>
                    <span>Category : </span>
                    <div class='label-head Label'>
                      <b:loop values='data:post.labels' var='label'>
                        <a class='label-link' expr:href='data:label.url' rel='tag'><data:label.name/></a>
                      </b:loop>
                    </div>
                  </div>
                </b:if>
              </b:if>
            </b:includable>
            <b:includable id='postLocation'>
  <span class='byline post-location'>
    <data:byline.label/>
    <a expr:href='data:post.location.mapsUrl' target='_blank'><data:post.location.name/></a>
  </span>
</b:includable>
            <b:includable id='postMeta' var='post'>
              <b:include data='post' name='postMetadataJSON'/>
            </b:includable>
            <b:includable id='postMetadataJSONImage'>
  &quot;image&quot;: {
    &quot;@type&quot;: &quot;ImageObject&quot;,
    <b:if cond='data:post.featuredImage.isResizable'>
    &quot;url&quot;: &quot;<b:eval expr='resizeImage(data:post.featuredImage, 1200, &quot;1200:630&quot;)'/>&quot;,
    &quot;height&quot;: 630,
    &quot;width&quot;: 1200
    <b:else/>
    &quot;url&quot;: &quot;https://lh3.googleusercontent.com/ULB6iBuCeTVvSjjjU1A-O8e9ZpVba6uvyhtiWRti_rBAs9yMYOFBujxriJRZ-A=w1200&quot;,
    &quot;height&quot;: 348,
    &quot;width&quot;: 1200
    </b:if>
  },
</b:includable>
            <b:includable id='postMetadataJSONPublisher'>
 &quot;publisher&quot;: {
    &quot;@type&quot;: &quot;Organization&quot;,
    &quot;name&quot;: &quot;Blogger&quot;,
    &quot;logo&quot;: {
      &quot;@type&quot;: &quot;ImageObject&quot;,
      &quot;url&quot;: &quot;https://lh3.googleusercontent.com/ULB6iBuCeTVvSjjjU1A-O8e9ZpVba6uvyhtiWRti_rBAs9yMYOFBujxriJRZ-A=h60&quot;,
      &quot;width&quot;: 206,
      &quot;height&quot;: 60
    }
  },
</b:includable>
            <b:includable id='postNavigation' var='post'>

<!-- Greden nextprev -->

            </b:includable>
            <b:includable id='postPagination'>
  <div class='blog-pager container' id='blog-pager'>
    <b:include cond='data:newerPageUrl' name='previousPageLink'/>
    <b:include cond='data:olderPageUrl' name='nextPageLink'/>
    <b:include cond='data:view.url != data:blog.homepageUrl' name='homePageLink'/>
  </div>
</b:includable>
            <b:includable id='postReactions'>
  <span class='byline reactions'>
    <span class='reactions-label'>
      <data:byline.label/>
    </span>
    <iframe allowtransparency='true' class='reactions-iframe' expr:src='data:post.reactionsUrl' frameborder='0' name='reactions' scrolling='no'/>
  </span>
</b:includable>
            <b:includable id='postShareButtons' var='post'>
              <!-- Post ShareButtons -->
              <b:if cond='data:allBylineItems.share'>

<div class='feet-icons'>

<span>Share :</span> 
<a class='face-ico' expr:href='&quot;https://www.facebook.com/sharer.php?u=&quot; + data:post.url' onclick='window.open(this.href, &apos;windowName&apos;, &apos;width=550, height=650, left=24, top=24, scrollbars, resizable&apos;); return false;' rel='nofollow'><i class='fa fa-facebook'/> Share</a>

<a class='twi-ico' expr:href='&quot;https://twitter.com/share?url=&quot; + data:post.url + &quot;&amp;text=&quot; + data:post.title' onclick='window.open(this.href, &apos;windowName&apos;, &apos;width=550, height=450, left=24, top=24, scrollbars, resizable&apos;); return false;' rel='nofollow'><i class='fa fa-twitter'/> Tweet</a>

<a class='pint-ico' expr:href='&quot;https://www.pinterest.com/pin/create/button/?url=&quot; + data:post.url + &quot;&amp;media=&quot; + data:post.featuredImage + &quot;&amp;description=&quot; + data:post.title' onclick='window.open(this.href, &apos;windowName&apos;, &apos;width=735, height=750, left=24, top=24, scrollbars, resizable&apos;); return false;' rel='nofollow'><i class='fa fa-pinterest'/> Share</a>


<a class='link-ico' expr:href='&quot;https://www.linkedin.com/shareArticle?url=&quot; + data:post.url' onclick='window.open(this.href, &apos;windowName&apos;, &apos;width=950, height=650, left=24, top=24, scrollbars, resizable&apos;); return false;' rel='nofollow'><i class='fa fa-linkedin'/> Share</a>


<b:if cond='data:blog.isMobileRequest'>                
<a class='bitz-ico' expr:href='&quot;https://api.whatsapp.com/send?text=&quot; + data:post.title + &quot; | &quot; + data:post.url' rel='nofollow' target='_blank'><i class='fa fa-whatsapp'/> Share</a>
<b:else/>
<a class='bitz-ico' expr:href='&quot;https://web.whatsapp.com/send?text=&quot; + data:post.title + &quot; | &quot; + data:post.url' onclick='window.open(this.href, &apos;windowName&apos;, &apos;width=900, height=550, left=24, top=24, scrollbars, resizable&apos;); return false;' rel='nofollow'><i class='fa fa-whatsapp'/> Share</a>
</b:if>


</div>

              </b:if>
            </b:includable>
            <b:includable id='postTimestamp'>
  <span class='byline post-timestamp'>
    <data:byline.label/>
    <b:if cond='data:post.url'>
      <meta expr:content='data:post.url.canonical'/>
      <a class='timestamp-link' expr:href='data:post.url' rel='bookmark' title='permanent link'>
        <time class='published' expr:datetime='data:post.date.iso8601' expr:title='data:post.date.iso8601'>
          <data:post.date/>
        </time>
      </a>
    </b:if>
  </span>
</b:includable>
            <b:includable id='postTitle' var='post'>
              <!-- Post Title Index and Item -->
              <b:if cond='data:view.isMultipleItems'>
                <h2 class='post-title item_name'>
                  <a expr:href='data:post.url'><data:post.title/></a>
                </h2>
              </b:if>
            </b:includable>
            <b:includable id='postdesc' var='post'>
              <p class='post-snippet'><b:eval expr='data:post.snippets.short snippet { length: 116 }'/></p>
            </b:includable>
            <b:includable id='previousPageLink'>
              <a class='blog-pager-newer-link' expr:href='data:newerPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-newer-link&quot;' expr:title='data:messages.newerPosts'>
                <data:messages.newerPosts/>
              </a>
            </b:includable>
            <b:includable id='sharingButton'>
  <span expr:aria-label='data:platform.shareMessage' expr:class='&quot;sharing-platform-button sharing-element-&quot; + data:platform.key' expr:data-href='data:shareUrl + &quot;&amp;target=&quot; + data:platform.target' expr:data-url='data:originalUrl' expr:title='data:platform.shareMessage' role='menuitem' tabindex='-1'>
    <b:include name='sharingPlatformIcon'/>
    <span class='platform-sharing-text'><data:platform.name/></span>
  </span>
</b:includable>
            <b:includable id='sharingButtonContent'>
  <div class='flat-icon-button ripple'>
    <b:include name='shareIcon'/>
  </div>
</b:includable>
            <b:includable id='sharingButtons'>
  <div class='sharing' expr:aria-owns='&quot;sharing-popup-&quot; + data:sharingId' expr:data-title='data:shareTitle'>
    <button class='sharing-button touch-icon-button' expr:aria-controls='&quot;sharing-popup-&quot; + data:sharingId' expr:aria-label='data:messages.share.escaped' expr:id='&quot;sharing-button-&quot; + data:sharingId' role='button'>
      <b:include name='sharingButtonContent'/>
    </button>
    <b:include name='sharingButtonsMenu'/>
  </div>
</b:includable>
            <b:includable id='sharingButtonsMenu'>
  <div class='share-buttons-container'>
    <ul aria-hidden='true' class='share-buttons hidden' expr:aria-label='data:messages.share.escaped' expr:id='&quot;sharing-popup-&quot; + data:sharingId' role='menu'>
      <b:loop values='(data:platforms ?: data:blog.sharing.platforms) filter (p =&gt; p.key not in {&quot;blogThis&quot;})' var='platform'>
        <li>
          <b:include name='sharingButton'/>
        </li>
      </b:loop>
      <li aria-hidden='true' class='hidden'>
        <b:include name='otherSharingButton'/>
      </li>
    </ul>
  </div>
</b:includable>
            <b:includable id='sharingPlatformIcon'>
  <b:include data='{ iconClass: (&quot;touch-icon sharing-&quot; + data:platform.key) }' expr:name='data:platform.key + &quot;Icon&quot;'/>
</b:includable>
            <b:includable id='tagspost' var='post'>
              <!-- Post Label/Category -->
              <b:if cond='data:view.isMultipleItems and data:post.labels'>

              </b:if>
            </b:includable>
            <b:includable id='threadedCommentForm' var='post'>
              <div class='comment-form'>
                <a name='comment-form'/>
                <b:if cond='data:this.messages.blogComment != &quot;&quot;'>
                  <p><data:this.messages.blogComment/></p>
                </b:if>
                <b:include data='post' name='commentFormIframeSrc'/>
                <iframe allowtransparency='allowtransparency' class='blogger-iframe-colorize blogger-comment-from-post' expr:height='data:cmtIframeInitialHeight ?: &quot;90px&quot;' frameborder='0' id='comment-editor' name='comment-editor' src='' width='100%'/>
                <data:post.cmtfpIframe/>
                <script type='text/javascript'>
                  BLOG_CMT_createIframe(&#39;<data:post.appRpcRelayPath/>&#39;);
                </script>
              </div>
            </b:includable>
            <b:includable id='threadedCommentJs' var='post'>
              <script async='async' expr:src='data:post.commentSrc' type='text/javascript'/>
              <b:template-script inline='true' name='threaded_comments'/>
              <script type='text/javascript'>
                blogger.widgets.blog.initThreadedComments(
                  <data:post.commentJso/>,
                  <data:post.commentMsgs/>,
                  <data:post.commentConfig/>);
              </script>
            </b:includable>
            <b:includable id='threadedComments' var='post'>
              <section class='comments threaded' expr:data-embed='data:post.embedCommentForm' expr:data-num-comments='data:post.numberOfComments' id='comments'>

<div class='my-comments'>
                <a name='comments'/>

                <b:include name='commentsTitle'/>

                <div class='comments-content'>
                  <b:if cond='data:post.embedCommentForm'>
                    <b:include data='post' name='threadedCommentJs'/>
                  </b:if>
                  <div id='comment-holder'>
                    <data:post.commentHtml/>
                  </div>
                </div>

                <p class='comment-footer'>
                  <b:if cond='data:post.allowNewComments'>
                    <b:include data='post' name='threadedCommentForm'/>
                    <b:else/>
                    <data:post.noNewCommentsText/>
                  </b:if>
                </p>

                <b:if cond='data:showCmtPopup'>
                  <div id='comment-popup'>
                    <iframe allowtransparency='allowtransparency' frameborder='0' id='comment-actions' name='comment-actions' scrolling='no'>
                    </iframe>
                  </div>
                </b:if>
                </div><!-- my comments -->
              </section>
            </b:includable>
          </b:widget>
        </b:section> 

        </main>
      </div>


              <div class='sidebar-container1 sidebar-wrapper top' role='complementary'>

                  <b:section class='sidebar' id='sidebar_feed' name='Sidebar' preferred='yes'/>
                  <b:section id='sidebar_item' name='Sidebar (Item Page)'>
                    <b:widget id='Image6' locked='false' title='' type='Image' visible='true'>
                      <b:widget-settings>
                        <b:widget-setting name='displayUrl'>http://1.bp.blogspot.com/-QVKawAupKa4/XpCrGBsaznI/AAAAAAAABbI/ohQ6SxuD2cIiWltcStTLmlKECeHerYTbgCK4BGAYYCw/s1600/sidebar-260x600%2Bad.png</b:widget-setting>
                        <b:widget-setting name='displayHeight'>600</b:widget-setting>
                        <b:widget-setting name='sectionWidth'>245</b:widget-setting>
                        <b:widget-setting name='shrinkToFit'>false</b:widget-setting>
                        <b:widget-setting name='displayWidth'>260</b:widget-setting>
                        <b:widget-setting name='link'>/</b:widget-setting>
                        <b:widget-setting name='caption'/>
                      </b:widget-settings>
                      <b:includable id='main'>
  <b:include name='widget-title'/>
  <b:include name='content'/>
</b:includable>
                      <b:includable id='content'>
  <div class='widget-content'>
    <b:tag cond='data:link' expr:href='data:link' name='a'>
      <img expr:alt='data:title' expr:height='data:height' expr:id='data:widget.instanceId + &quot;_img&quot;' expr:src='data:sourceUrl' expr:width='data:width'>
        <b:attr cond='data:sourceSet' expr:value='data:sourceSet' name='srcset'/>
      </img>
    </b:tag>
    <br/>
    <b:if cond='data:caption'>
      <span class='caption'><data:caption/></span>
    </b:if>
  </div>
</b:includable>
                    </b:widget>
                    <b:widget id='PopularPosts1' locked='false' title='Popular Posts' type='PopularPosts' version='2' visible='true'>
                      <b:widget-settings>
                        <b:widget-setting name='numItemsToShow'>3</b:widget-setting>
                        <b:widget-setting name='showThumbnails'>true</b:widget-setting>
                        <b:widget-setting name='showSnippets'>true</b:widget-setting>
                        <b:widget-setting name='timeRange'>LAST_MONTH</b:widget-setting>
                      </b:widget-settings>
                      <b:includable id='main' var='this'>
      <b:include name='widget-title'/>
      <div class='widget-content'>
        <b:loop values='data:posts' var='post'>
          <b:include data='post' name='postContent'/>
        </b:loop>
      </div>
    </b:includable>
                      <b:includable id='blogThisShare'>
  <b:with value='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=270,width=475\&quot;); return false;&quot;' var='onclick'>
    <b:include name='platformShare'/>
  </b:with>
</b:includable>
                      <b:includable id='bylineByName' var='byline'>
  <b:switch var='data:byline.name'>
  <b:case value='share'/>
    <b:include cond='data:post.shareUrl' name='postShareButtons'/>
  <b:case value='comments'/>
    <b:include cond='data:post.allowComments' name='postCommentsLink'/>
  <b:case value='location'/>
    <b:include cond='data:post.location' name='postLocation'/>
  <b:case value='timestamp'/>
    <b:include cond='not data:view.isPage' name='postTimestamp'/>
  <b:case value='author'/>
    <b:include name='postAuthor'/>
  <b:case value='labels'/>
    <b:include cond='data:post.labels' name='postLabels'/>
  <b:case value='icons'/>
    <b:include cond='data:post.emailPostUrl' name='emailPostIcon'/>
  <b:case value='reactions'/>
    <b:include cond='data:post.reactionsUrl' name='postReactions'/>
  </b:switch>
</b:includable>
                      <b:includable id='bylineRegion' var='regionItems'>
  <b:loop values='data:regionItems' var='byline'>
    <b:include data='byline' name='bylineByName'/>
  </b:loop>
</b:includable>
                      <b:includable id='commentsLink'>
  <a class='comment-link' expr:href='data:post.commentsUrl' expr:onclick='data:post.commentsUrlOnclick'>
    <b:if cond='data:post.numberOfComments &gt; 0'>
      <b:message name='messages.numberOfComments'>
        <b:param expr:value='data:post.numberOfComments' name='numComments'/>
      </b:message>
    <b:else/>
      <data:messages.postAComment/>
    </b:if>
  </a>
</b:includable>
                      <b:includable id='commentsLinkIframe'>
  <span class='cmt_count_iframe_holder' expr:data-count='data:post.numberOfComments' expr:data-onclick='data:post.commentsUrlOnclick' expr:data-post-url='data:post.url' expr:data-url='data:post.url.canonical.http'>
  </span>
</b:includable>
                      <b:includable id='emailPostIcon'>
  <span class='byline post-icons'>
    <!-- email post links -->
    <span class='item-action'>
      <a expr:href='data:post.emailPostUrl' expr:title='data:messages.emailPost'>
        <b:include data='{ iconClass: &quot;touch-icon sharing-icon&quot; }' name='emailIcon'/>
      </a>
    </span>
  </span>
</b:includable>
                      <b:includable id='facebookShare'>
  <b:with value='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=430,width=640\&quot;); return false;&quot;' var='onclick'>
    <b:include name='platformShare'/>
  </b:with>
</b:includable>
                      <b:includable id='footerBylines'>
  <b:if cond='data:widgets.Blog.first.footerBylines'>
    <b:loop index='i' values='data:widgets.Blog.first.footerBylines' var='region'>
      <b:if cond='not data:region.items.empty'>
        <div expr:class='&quot;post-footer-line post-footer-line-&quot; + (data:i + 1)'>
          <b:with value='&quot;footer-&quot; + (data:i + 1)' var='regionName'>
            <b:include data='region.items' name='bylineRegion'/>
          </b:with>
        </div>
      </b:if>
    </b:loop>
  </b:if>
</b:includable>
                      <b:includable id='googlePlusShare'>
  <div class='goog-inline-block google-plus-share-container'>
    <g:plusone annotation='inline' expr:href='data:originalUrl.canonical.http' size='medium' source='blogger:blog:plusone'/>
  </div>
</b:includable>
                      <b:includable id='headerByline'>
  <b:if cond='data:widgets.Blog.first.headerByline'>
    <div class='post-header'>
      <div class='post-header-line-1'>
        <b:with value='&quot;header-1&quot;' var='regionName'>
          <b:include data='data:widgets.Blog.first.headerByline.items' name='bylineRegion'/>
        </b:with>
      </div>
    </div>
  </b:if>
</b:includable>
                      <b:includable id='linkShare'>
  <b:with value='&quot;window.prompt(\&quot;Copy to clipboard: Ctrl+C, Enter\&quot;, \&quot;&quot; + data:originalUrl + &quot;\&quot;); return false;&quot;' var='onclick'>
    <b:include name='platformShare'/>
  </b:with>
</b:includable>
                      <b:includable id='otherSharingButton'>
  <span class='sharing-platform-button sharing-element-other' expr:aria-label='data:messages.shareToOtherApps.escaped' expr:data-url='data:originalUrl' expr:title='data:messages.shareToOtherApps.escaped' role='menuitem' tabindex='-1'>
    <b:with value='{key: &quot;sharingOther&quot;}' var='platform'>
      <b:include name='sharingPlatformIcon'/>
    </b:with>
    <span class='platform-sharing-text'><data:messages.shareOtherApps.escaped/></span>
  </span>
</b:includable>
                      <b:includable id='platformShare'>
  <a expr:class='&quot;goog-inline-block sharing-&quot; + data:platform.key' expr:data-url='data:originalUrl' expr:href='data:shareUrl + &quot;&amp;target=&quot; + data:platform.target' expr:onclick='data:onclick ? data:onclick : &quot;&quot;' expr:title='data:platform.shareMessage' target='_blank'>
    <span class='share-button-link-text'>
      <data:platform.shareMessage/>
    </span>
  </a>
</b:includable>
                      <b:includable id='postAuthor'>
  <span class='byline post-author vcard'>
    <span class='post-author-label'>
      <data:byline.label/>
    </span>
    <span class='fn'>
      <b:if cond='data:post.author.profileUrl'>
        <meta expr:content='data:post.author.profileUrl'/>
        <a class='g-profile' expr:href='data:post.author.profileUrl' rel='author' title='author profile'>
          <span><data:post.author.name/></span>
        </a>
      <b:else/>
        <span><data:post.author.name/></span>
      </b:if>
    </span>
  </span>
</b:includable>
                      <b:includable id='postCommentsLink'>
  <span class='byline post-comment-link container'>
    <b:include cond='data:post.commentSource != 1' name='commentsLink'/>
    <b:include cond='data:post.commentSource == 1' name='commentsLinkIframe'/>
  </span>
</b:includable>
                      <b:includable id='postContent' var='post'>
      <div class='post post-shop-info' expr:data-id='data:post.id'>
        <div class='post-content'>
          <a class='post-image-link' expr:href='data:post.url'>
            <b:if cond='data:post.featuredImage'>
              <img class='post-thumb' expr:alt='data:post.title' expr:src='data:post.featuredImage resizeImage 680'/>
              <b:else/>
              <img class='post-thumb' expr:alt='data:post.title' src='https://4.bp.blogspot.com/-O3EpVMWcoKw/WxY6-6I4--I/AAAAAAAAB2s/KzC0FqUQtkMdw7VzT6oOR_8vbZO6EJc-ACK4BGAYYCw/w680/nth.png'/>
            </b:if>
          </a>
          <div class='product-info'>
            <h2 class='post-title'>
              <a expr:href='data:post.url'><data:post.title/></a>
            </h2>
            <span class='meta-price'/>
          </div>
        </div>
      </div>
    </b:includable>
                      <b:includable id='postJumpLink' var='post'>
  <div class='jump-link flat-button'>
    <a expr:href='data:post.url fragment &quot;more&quot;' expr:title='data:post.title'>
      <b:eval expr='data:blog.jumpLinkMessage'/>
    </a>
  </div>
</b:includable>
                      <b:includable id='postLabels'>
  <span class='byline post-labels'>
    <span class='byline-label'><data:byline.label/></span>
    <b:loop index='i' values='data:post.labels' var='label'>
      <a expr:href='data:label.url' rel='tag'>
        <data:label.name/>
      </a>
    </b:loop>
  </span>
</b:includable>
                      <b:includable id='postLocation'>
  <span class='byline post-location'>
    <data:byline.label/>
    <a expr:href='data:post.location.mapsUrl' target='_blank'><data:post.location.name/></a>
  </span>
</b:includable>
                      <b:includable id='postReactions'>
  <span class='byline reactions'>
    <span class='reactions-label'>
      <data:byline.label/>
    </span>
    <iframe allowtransparency='true' class='reactions-iframe' expr:src='data:post.reactionsUrl' frameborder='0' name='reactions' scrolling='no'/>
  </span>
</b:includable>
                      <b:includable id='postShareButtons'>
  <div class='byline post-share-buttons goog-inline-block'>
    <b:with value='data:sharingId ?: ((data:widget.instanceId ?: &quot;sharing&quot;) + &quot;-&quot; + (data:regionName ?: &quot;byline&quot;) + &quot;-&quot; + data:post.id)' var='sharingId'>
      <!-- Note: 'sharingButtons' includable is from the default Sharing widget markup. -->
      <b:include data='{                                                sharingId: data:sharingId,                                                originalUrl: data:post.url,                                                platforms: data:this.sharing.platforms,                                                shareUrl: data:post.shareUrl,                                                shareTitle: data:post.title,                                              }' name='sharingButtons'/>
    </b:with>
  </div>
</b:includable>
                      <b:includable id='postTimestamp'>
  <span class='byline post-timestamp'>
    <data:byline.label/>
    <b:if cond='data:post.url'>
      <meta expr:content='data:post.url.canonical'/>
      <a class='timestamp-link' expr:href='data:post.url' rel='bookmark' title='permanent link'>
        <time class='published' expr:datetime='data:post.date.iso8601' expr:title='data:post.date.iso8601'>
          <data:post.date/>
        </time>
      </a>
    </b:if>
  </span>
</b:includable>
                      <b:includable id='sharingButton'>
  <span expr:aria-label='data:platform.shareMessage' expr:class='&quot;sharing-platform-button sharing-element-&quot; + data:platform.key' expr:data-href='data:shareUrl + &quot;&amp;target=&quot; + data:platform.target' expr:data-url='data:originalUrl' expr:title='data:platform.shareMessage' role='menuitem' tabindex='-1'>
    <b:include name='sharingPlatformIcon'/>
    <span class='platform-sharing-text'><data:platform.name/></span>
  </span>
</b:includable>
                      <b:includable id='sharingButtonContent'>
  <div class='flat-icon-button ripple'>
    <b:include name='shareIcon'/>
  </div>
</b:includable>
                      <b:includable id='sharingButtons'>
  <div class='sharing' expr:aria-owns='&quot;sharing-popup-&quot; + data:sharingId' expr:data-title='data:shareTitle'>
    <button class='sharing-button touch-icon-button' expr:aria-controls='&quot;sharing-popup-&quot; + data:sharingId' expr:aria-label='data:messages.share.escaped' expr:id='&quot;sharing-button-&quot; + data:sharingId' role='button'>
      <b:include name='sharingButtonContent'/>
    </button>
    <b:include name='sharingButtonsMenu'/>
  </div>
</b:includable>
                      <b:includable id='sharingButtonsMenu'>
  <div class='share-buttons-container'>
    <ul aria-hidden='true' class='share-buttons hidden' expr:aria-label='data:messages.share.escaped' expr:id='&quot;sharing-popup-&quot; + data:sharingId' role='menu'>
      <b:loop values='(data:platforms ?: data:blog.sharing.platforms) filter (p =&gt; p.key not in {&quot;blogThis&quot;})' var='platform'>
        <li>
          <b:include name='sharingButton'/>
        </li>
      </b:loop>
      <li aria-hidden='true' class='hidden'>
        <b:include name='otherSharingButton'/>
      </li>
    </ul>
  </div>
</b:includable>
                      <b:includable id='sharingPlatformIcon'>
  <b:include data='{ iconClass: (&quot;touch-icon sharing-&quot; + data:platform.key) }' expr:name='data:platform.key + &quot;Icon&quot;'/>
</b:includable>
                      <b:includable id='snippetedPostByline'>
  <b:with value='(data:widgets first (w =&gt; w.type == &quot;Blog&quot;)).allBylineItems' var='blogBylines'>
    <div class='item-byline'>
      <b:with value='data:blogBylines first (i =&gt; i.name == &quot;author&quot;)' var='byline'>
        <b:include cond='data:byline and data:this.postDisplay.showAuthor' data='post' name='postAuthor'/>
      </b:with>
      <b:with value='data:blogBylines first (i =&gt; i.name == &quot;timestamp&quot;)' var='byline'>
        <b:include cond='data:byline and data:this.postDisplay.showDate' data='post' name='postTimestamp'/>
      </b:with>
    </div>
  </b:with>
</b:includable>
                      <b:includable id='snippetedPostContent'>
  <div class='post-content'>
    <b:include cond='data:this.postDisplay.showTitle' name='snippetedPostTitle'/>
    <b:include cond='data:this.postDisplay.showDate or data:this.postDisplay.showAuthor' name='snippetedPostByline'/>
    <b:include cond='data:this.postDisplay.showSnippet' data='post' name='postSnippet'/>
    <b:include cond='data:this.postDisplay.showFeaturedImage and data:post.featuredImage' name='snippetedPostThumbnail'/>
  </div>
</b:includable>
                      <b:includable id='snippetedPostThumbnail'>
  <div class='item-thumbnail'>
    <a expr:href='data:post.url'>
      <b:include data='{                         image: data:post.featuredImage,                         imageSizes: [72, 144],                         imageRatio: &quot;1:1&quot;,                         sourceSizes: &quot;72px&quot;                        }' name='responsiveImage'/>
    </a>
  </div>
</b:includable>
                      <b:includable id='snippetedPostTitle'>
  <b:if cond='data:post.title != &quot;&quot;'>
    <h3 class='post-title'><a expr:href='data:post.url'><data:post.title/></a></h3>
  </b:if>
</b:includable>
                      <b:includable id='snippetedPosts'>
  <div role='feed'>
    <!-- Don't render the post that we're currently already looking at. -->
    <b:loop values='data:posts filter (p =&gt; p.id != data:view.postId)' var='post'>
      <article class='post' role='article'>
        <b:include name='snippetedPostContent'/>
      </article>
    </b:loop>
  </div>
</b:includable>
                    </b:widget>
                    <b:widget id='Label1' locked='false' title='Labels' type='Label' version='2' visible='true'>
                      <b:widget-settings>
                        <b:widget-setting name='sorting'>ALPHA</b:widget-setting>
                        <b:widget-setting name='display'>LIST</b:widget-setting>
                        <b:widget-setting name='selectedLabelsList'>Decoration,Furniture,Gadgets,Men,Women</b:widget-setting>
                        <b:widget-setting name='showType'>USER_SELECTED</b:widget-setting>
                        <b:widget-setting name='showFreqNumbers'>false</b:widget-setting>
                      </b:widget-settings>
                      <b:includable id='main' var='this'>
  <b:include name='widget-title'/>
  <b:include name='content'/>
</b:includable>
                      <b:includable id='cloud'>
  <b:loop values='data:labels' var='label'>
    <span class='label-size'>
      <b:class expr:name='&quot;label-size-&quot; + data:label.cssSize'/>
      <a class='label-name' expr:href='data:label.url'>
        <data:label.name/>
        <b:if cond='data:this.showFreqNumbers'>
          <span class='label-count'><data:label.count/></span>
        </b:if>
      </a>
    </span>
  </b:loop>
</b:includable>
                      <b:includable id='content'>
  <div class='widget-content'>
    <b:class expr:name='data:this.display + &quot;-label-widget-content&quot;'/>
    <b:include cond='data:this.display == &quot;list&quot;' name='list'/>
    <b:include cond='data:this.display == &quot;cloud&quot;' name='cloud'/>
  </div>
</b:includable>
                      <b:includable id='list'>
  <ul>
    <b:loop values='data:labels' var='label'>
      <li>
        <a class='label-name' expr:href='data:label.url'>
          <data:label.name/>
          <b:if cond='data:this.showFreqNumbers'>
            <span class='label-count'><data:label.count/></span>
          </b:if>
        </a>
      </li>
    </b:loop>
  </ul>
</b:includable>
                    </b:widget>
                    <b:widget id='ContactForm1' locked='false' title='Contact Form' type='ContactForm' version='2' visible='true'>
                      <b:includable id='main'>
    <b:include name='content'/>
</b:includable>
                      <b:includable id='content'>

</b:includable>
                    </b:widget>
                  </b:section>
              </div>   <!-- close sidebar-container -->
    
    </div><!-- outer-wrapper -->

</div><!--Div Contained-->

 <div class='clear'/>

      </b:with>

<div class='clear'/> 

<div class='contained'>

<b:if cond='data:view.isHomepage'>

<div class='gap'>
<div class='bow'>
<b:section class='banner2' id='Adder1' maxwidgets='1' name='Ad banner (left)' showaddelement='yes'>
  <b:widget id='Image1' locked='false' title='Ad banner 1' type='Image' visible='true'>
    <b:widget-settings>
      <b:widget-setting name='displayUrl'>http://4.bp.blogspot.com/-27YXjTRi4ug/Xo9n96N33PI/AAAAAAAABaw/C1hik36SUEUGKL4ohp-azMjURuCDFGM-gCK4BGAYYCw/s1600/adder-1.png</b:widget-setting>
      <b:widget-setting name='displayHeight'>253</b:widget-setting>
      <b:widget-setting name='sectionWidth'>752</b:widget-setting>
      <b:widget-setting name='shrinkToFit'>false</b:widget-setting>
      <b:widget-setting name='displayWidth'>570</b:widget-setting>
      <b:widget-setting name='link'>/</b:widget-setting>
      <b:widget-setting name='caption'>banner</b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <b:include name='widget-title'/>
  <b:include name='content'/>
</b:includable>
    <b:includable id='content'>
  <div class='widget-content'>
    <b:tag cond='data:link' expr:href='data:link' name='a'>
      <img expr:alt='data:title' expr:height='data:height' expr:id='data:widget.instanceId + &quot;_img&quot;' expr:src='data:sourceUrl' expr:width='data:width'>
        <b:attr cond='data:sourceSet' expr:value='data:sourceSet' name='srcset'/>
      </img>
    </b:tag>
    <br/>
    <b:if cond='data:caption'>
      <span class='caption'><data:caption/></span>
    </b:if>
  </div>
</b:includable>
  </b:widget>
</b:section>
<b:section class='banner2' id='Adder2' maxwidgets='1' name='Ad banner (right)' showaddelement='yes'>
  <b:widget id='Image2' locked='false' title='Ad banner 2' type='Image' version='2' visible='true'>
    <b:widget-settings>
      <b:widget-setting name='displayUrl'>http://3.bp.blogspot.com/-fONWRjqKdzE/Xo9oBBH9TZI/AAAAAAAABa4/NHtiKoZryK0cmUbOgPJrgPQswQVPL-98wCK4BGAYYCw/s1600/adder-2.png</b:widget-setting>
      <b:widget-setting name='displayHeight'>253</b:widget-setting>
      <b:widget-setting name='sectionWidth'>752</b:widget-setting>
      <b:widget-setting name='shrinkToFit'>false</b:widget-setting>
      <b:widget-setting name='displayWidth'>570</b:widget-setting>
      <b:widget-setting name='link'>/</b:widget-setting>
      <b:widget-setting name='caption'>banner 2</b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <b:include name='widget-title'/>
  <b:include name='content'/>
</b:includable>
    <b:includable id='content'>
  <div class='widget-content'>
    <b:tag cond='data:link' expr:href='data:link' name='a'>
      <img expr:alt='data:title' expr:height='data:height' expr:id='data:widget.instanceId + &quot;_img&quot;' expr:src='data:sourceUrl' expr:width='data:width'>
      <b:attr cond='data:sourceSet' expr:value='data:sourceSet' name='srcset'/>
      </img>
    </b:tag>
    <br/>
    <b:if cond='data:caption'>
      <span class='caption'><data:caption/></span>
    </b:if>
  </div>
</b:includable>
  </b:widget>
</b:section>
</div>
</div><!-- bow -->
<div class='clear'/> 

<div class='gap'>
  <b:section class='producting' id='prodct' maxwidgets='1' name='Products by category' showaddelement='yes'>
    <b:widget id='HTML34' locked='false' title='Handmade Furniture' type='HTML' version='2' visible='true'>
      <b:widget-settings>
        <b:widget-setting name='content'>6/Furniture/post-list</b:widget-setting>
      </b:widget-settings>
      <b:includable id='main'>
        <em><b:include name='widget-title'/></em>
        <div class='clear'/>
<div class='bow'>
   <div class='widget-content'>
 <data:content/>
   </div>
</div>
   </b:includable>
    </b:widget>
  </b:section>
</div>

<div class='gap'>
  <b:section class='producting' id='prodct2' maxwidgets='1' name='Products by category 2' showaddelement='yes'>
    <b:widget id='HTML36' locked='false' title='Hot Gadgets' type='HTML' version='2' visible='true'>
      <b:widget-settings>
        <b:widget-setting name='content'>6/Gadgets/post-list</b:widget-setting>
      </b:widget-settings>
      <b:includable id='main'>
        <em><b:include name='widget-title'/></em>
<div class='clear'/>
<div class='bow'>
   <div class='widget-content'>
 <data:content/>
   </div>
</div>
   </b:includable>
    </b:widget>
  </b:section>
</div>
</b:if>
</div><div class='clear'/> 

 <div id='footer'>

<div class='contained'>
<div class='footer-wrapper'>

<b:section class='footer' id='footer1' preferred='yes'>
  <b:widget id='HTML1' locked='false' title='Souq Store' type='HTML' version='2' visible='true'>
    <b:widget-settings>
      <b:widget-setting name='content'>Short description of your blog can be added here. Mashable rassure vous nous les avons regroup en un autre buffet ressource pratique bien approvisione pour.</b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
<div class='logo-footer'>
  <b:include name='widget-title'/>
</div>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
  </b:widget>
</b:section>
<b:section class='footer' id='footer2' preferred='yes'>
  <b:widget id='HTML2' locked='false' title='Services' type='HTML' visible='true'>
    <b:widget-settings>
      <b:widget-setting name='content'>&lt;ul&gt;
&lt;li&gt;&lt;a href=&#39;/&#39;&gt;FAQ&#39;s&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a href=&#39;/&#39;&gt;Privacy Policy&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a href=&#39;/&#39;&gt;Terms &amp; Conditions&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a href=&#39;/p/contact.html&#39;&gt;Contact Us&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;</b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <b:include name='widget-title'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
  </b:widget>
</b:section>
<b:section class='footer' id='footer3' preferred='yes'>
  <b:widget id='HTML3' locked='false' title='Quick links' type='HTML' visible='true'>
    <b:widget-settings>
      <b:widget-setting name='content'>&lt;ul&gt;
&lt;li&gt;&lt;a href=&#39;/&#39;&gt;Terms of Use&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a href=&#39;/&#39;&gt;Privacy Policy&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a href=&#39;/&#39;&gt;Track Order&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a href=&#39;/&#39;&gt;Contact Us&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;</b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <b:include name='widget-title'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
  </b:widget>
</b:section>
<b:section class='footer' id='footer4' preferred='yes'>
  <b:widget id='HTML9' locked='false' title='Cutomer Care' type='HTML' visible='true'>
    <b:widget-settings>
      <b:widget-setting name='content'>&lt;ul&gt;
&lt;li&gt;&lt;a href=&#39;/&#39;&gt;Warranty Policy&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a href=&#39;/&#39;&gt;Return &amp; Exchange&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a href=&#39;/&#39;&gt;FAQ&#39;s&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a href=&#39;/&#39;&gt;Contact Us&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;</b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <b:include name='widget-title'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
  </b:widget>
</b:section>
<b:section class='footer' id='footer5' preferred='yes'>
  <b:widget id='HTML4' locked='false' title='Follow Us' type='HTML' visible='true'>
    <b:widget-settings>
      <b:widget-setting name='content'>&lt;div class=&#39;socal&#39;&gt;

&lt;!-- Social Profile Icons --&gt;

&lt;a class=&#39;fb-ic&#39; href=&#39;YOUR-FACEBOOK-URL&#39; title=&#39;Like us&#39;&gt;&lt;i class=&#39;fa fa-facebook&#39;/&gt;&lt;/i&gt;&lt;/a&gt;
&lt;a class=&#39;tw-ic&#39; href=&#39;YOUR-TWITTER-URL&#39; title=&#39;Follow us&#39;&gt;&lt;i class=&#39;fa fa-twitter&#39;/&gt;&lt;/i&gt;&lt;/a&gt;
&lt;a class=&#39;ig-ic&#39; href=&#39;YOUR-INSTAGRAM-URL&#39; title=&#39;Follow on Instagram&#39;&gt;&lt;i class=&#39;fa fa-instagram&#39;/&gt;&lt;/i&gt;&lt;/a&gt;
&lt;a class=&#39;yt-ic&#39; href=&#39;YOUR-YOUTUBE-URL&#39; title=&#39;Subscribe on youtube&#39;&gt;&lt;i class=&#39;fa fa-youtube&#39;/&gt;&lt;/i&gt;&lt;/a&gt;
&lt;a class=&#39;rs-ic&#39; href=&#39;YOUR-RSS-URL&#39; title=&#39;Rss feeds&#39;&gt;&lt;i class=&#39;fa fa-envelope&#39;/&gt;&lt;/i&gt;&lt;/a&gt;

&lt;/div&gt;

&lt;div class=&#39;apploads&#39;&gt;
&lt;a href=&#39;/&#39;&gt;
&lt;i aria-hidden=&#39;true&#39; class=&#39;fa fa-apple&#39;/&gt; iOS
&lt;/i&gt;&lt;/a&gt;

&lt;a href=&#39;/&#39;&gt;
&lt;i aria-hidden=&#39;true&#39; class=&#39;fa fa-android&#39;/&gt; Android
&lt;/i&gt;&lt;/a&gt;
&lt;/div&gt;</b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <b:include name='widget-title'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
  </b:widget>
</b:section>
      
</div><!-- footer wrapper -->

</div><!--Div Contained-->

</div><!-- footer -->

<div class='clear'/> 

<div class='contained'>

<div class='dlab'>
  <b:section class='med-lab' id='medlab' maxwidgets='1' name='Category labels' showaddelement='yes'>
    <b:widget id='Label3' locked='false' title='Clothing &amp;amp; Apparel:' type='Label' visible='true'>
      <b:widget-settings>
        <b:widget-setting name='sorting'>ALPHA</b:widget-setting>
        <b:widget-setting name='display'>LIST</b:widget-setting>
        <b:widget-setting name='selectedLabelsList'>Chair,Decoration,Dolce,Furniture,Gadgets,Games,Lamps,Leather,Makeup,Men,Sadidas</b:widget-setting>
        <b:widget-setting name='showType'>USER_SELECTED</b:widget-setting>
        <b:widget-setting name='showFreqNumbers'>false</b:widget-setting>
      </b:widget-settings>
      <b:includable id='main' var='this'>
      <b:include name='widget-title'/>
      <b:include name='content'/>
    </b:includable>
      <b:includable id='cloud'>
  <b:loop values='data:labels' var='label'>
    <span class='label-size'>
      <b:class expr:name='&quot;label-size-&quot; + data:label.cssSize'/>
      <a class='label-name' expr:href='data:label.url'>
        <data:label.name/>
        <b:if cond='data:this.showFreqNumbers'>
          <span class='label-count'><data:label.count/></span>
        </b:if>
      </a>
    </span>
  </b:loop>
</b:includable>
      <b:includable id='content'>
      <div class='widget-content'>
        <b:class expr:name='data:this.display + &quot;-label&quot;'/>
        <b:include cond='data:this.display == &quot;list&quot;' name='list'/>
        <b:include cond='data:this.display == &quot;cloud&quot;' name='list'/>
      </div>
    </b:includable>
      <b:includable id='list'>
      <ul>
        <b:loop values='data:labels' var='label'>
          <li>
            <a class='label-name' expr:href='data:label.url'>
              <data:label.name/>
              <b:if cond='data:this.showFreqNumbers'>
                <span class='label-count'><data:label.count/></span>
              </b:if>
            </a>
          </li>
        </b:loop>
      </ul>
    </b:includable>
    </b:widget>
  </b:section>
  <b:section class='med-lab' id='medlab2' maxwidgets='1' name='Category labels2' showaddelement='yes'>
    <b:widget id='Label4' locked='false' title='Jewelry &amp;amp; Watches:' type='Label' visible='true'>
      <b:widget-settings>
        <b:widget-setting name='sorting'>ALPHA</b:widget-setting>
        <b:widget-setting name='display'>LIST</b:widget-setting>
        <b:widget-setting name='selectedLabelsList'>Gadgets,Games,Lamps,Leather,Makeup,Men,Sadidas,Speaker,Tablet,Wireless,Women</b:widget-setting>
        <b:widget-setting name='showType'>USER_SELECTED</b:widget-setting>
        <b:widget-setting name='showFreqNumbers'>false</b:widget-setting>
      </b:widget-settings>
      <b:includable id='main' var='this'>
      <b:include name='widget-title'/>
      <b:include name='content'/>
    </b:includable>
      <b:includable id='cloud'>
  <b:loop values='data:labels' var='label'>
    <span class='label-size'>
      <b:class expr:name='&quot;label-size-&quot; + data:label.cssSize'/>
      <a class='label-name' expr:href='data:label.url'>
        <data:label.name/>
        <b:if cond='data:this.showFreqNumbers'>
          <span class='label-count'><data:label.count/></span>
        </b:if>
      </a>
    </span>
  </b:loop>
</b:includable>
      <b:includable id='content'>
      <div class='widget-content'>
        <b:class expr:name='data:this.display + &quot;-label&quot;'/>
        <b:include cond='data:this.display == &quot;list&quot;' name='list'/>
        <b:include cond='data:this.display == &quot;cloud&quot;' name='list'/>
      </div>
    </b:includable>
      <b:includable id='list'>
      <ul>
        <b:loop values='data:labels' var='label'>
          <li>
            <a class='label-name' expr:href='data:label.url'>
              <data:label.name/>
              <b:if cond='data:this.showFreqNumbers'>
                <span class='label-count'><data:label.count/></span>
              </b:if>
            </a>
          </li>
        </b:loop>
      </ul>
    </b:includable>
    </b:widget>
  </b:section>
  <b:section class='med-lab' id='medlab3' maxwidgets='1' name='Category labels3' showaddelement='yes'>
    <b:widget id='Label45' locked='false' title='Health &amp;amp; Beauty:' type='Label' visible='true'>
      <b:widget-settings>
        <b:widget-setting name='sorting'>ALPHA</b:widget-setting>
        <b:widget-setting name='display'>LIST</b:widget-setting>
        <b:widget-setting name='selectedLabelsList'>Dolce,Furniture,Gadgets,Games,Lamps,Leather,Makeup,Men,Sadidas,Speaker,Tablet</b:widget-setting>
        <b:widget-setting name='showType'>USER_SELECTED</b:widget-setting>
        <b:widget-setting name='showFreqNumbers'>false</b:widget-setting>
      </b:widget-settings>
      <b:includable id='main' var='this'>
      <b:include name='widget-title'/>
      <b:include name='content'/>
    </b:includable>
      <b:includable id='cloud'>
  <b:loop values='data:labels' var='label'>
    <span class='label-size'>
      <b:class expr:name='&quot;label-size-&quot; + data:label.cssSize'/>
      <a class='label-name' expr:href='data:label.url'>
        <data:label.name/>
        <b:if cond='data:this.showFreqNumbers'>
          <span class='label-count'><data:label.count/></span>
        </b:if>
      </a>
    </span>
  </b:loop>
</b:includable>
      <b:includable id='content'>
      <div class='widget-content'>
        <b:class expr:name='data:this.display + &quot;-label&quot;'/>
        <b:include cond='data:this.display == &quot;list&quot;' name='list'/>
        <b:include cond='data:this.display == &quot;cloud&quot;' name='list'/>
      </div>
    </b:includable>
      <b:includable id='list'>
      <ul>
        <b:loop values='data:labels' var='label'>
          <li>
            <a class='label-name' expr:href='data:label.url'>
              <data:label.name/>
              <b:if cond='data:this.showFreqNumbers'>
                <span class='label-count'><data:label.count/></span>
              </b:if>
            </a>
          </li>
        </b:loop>
      </ul>
    </b:includable>
    </b:widget>
  </b:section>
</div>

</div><!-- contained -->

<div class='contained'>

<div class='footer-credits'>

<a expr:href='data:blog.homepageUrl'><data:blog.title/></a> &#169; 2020 Designed by <a href='http://www.bloggertheme9.com/' id='credit'>Bloggertheme9</a> | <a href='https://www.freebloggertemplates.org/' target='_blank' title='Distributed by FreeBloggerTemplates.org'>Free Blogger Templates</a>.

  <img class='img-payments' src='https://4.bp.blogspot.com/-WfFEmIE9az4/Xq1vjrpAY2I/AAAAAAAABc8/Cvaxl0T5znIOgjzTxsghE4p-D5vfW-gwgCLcBGAsYHQ/s1600/payments.png'/>

</div><!-- footer-credits -->

</div><!-- contained -->


    <b:template-script async='true' name='vegeclub' version='1.0.0'/>
    <b:include data='blog' name='google-analytics'/>

</div><!-- ct-wrapper -->

<!-- Main Scripts -->
<script type='text/javascript'>
//<![CDATA[
/*! jquery-simplecart | License MIT */

var _0x71d9=["\x73\x74\x72\x69\x6E\x67","\x75\x6E\x64\x65\x66\x69\x6E\x65\x64","\x66\x75\x6E\x63\x74\x69\x6F\x6E","\x6F\x62\x6A\x65\x63\x74","\x6E\x6F\x64\x65\x54\x79\x70\x65","\x6E\x6F\x64\x65\x4E\x61\x6D\x65","","\x61\x74\x74\x72","\x65\x78\x74\x65\x6E\x64","\x69\x73\x52\x65\x61\x64\x79","\x6C\x65\x66\x74","\x64\x6F\x53\x63\x72\x6F\x6C\x6C","\x64\x6F\x63\x75\x6D\x65\x6E\x74\x45\x6C\x65\x6D\x65\x6E\x74","\x69\x6E\x69\x74","\x24\x24","\x2A","\x73\x69\x6D\x70\x6C\x65\x43\x61\x72\x74","\x6C\x6F\x63\x61\x6C\x53\x74\x6F\x72\x61\x67\x65","\x63\x6F\x6E\x73\x6F\x6C\x65","\x70\x75\x73\x68","\x6D\x73\x67\x73","\x55\x53\x44","\x26\x23\x33\x36\x3B","\x55\x53\x20\x44\x6F\x6C\x6C\x61\x72","\x41\x55\x44","\x41\x75\x73\x74\x72\x61\x6C\x69\x61\x6E\x20\x44\x6F\x6C\x6C\x61\x72","\x42\x52\x4C","\x52\x26\x23\x33\x36\x3B","\x42\x72\x61\x7A\x69\x6C\x69\x61\x6E\x20\x52\x65\x61\x6C","\x43\x41\x44","\x43\x61\x6E\x61\x64\x69\x61\x6E\x20\x44\x6F\x6C\x6C\x61\x72","\x43\x5A\x4B","\x26\x6E\x62\x73\x70\x3B\x26\x23\x37\x35\x3B\x26\x23\x32\x36\x39\x3B","\x43\x7A\x65\x63\x68\x20\x4B\x6F\x72\x75\x6E\x61","\x44\x4B\x4B","\x44\x4B\x4B\x26\x6E\x62\x73\x70\x3B","\x44\x61\x6E\x69\x73\x68\x20\x4B\x72\x6F\x6E\x65","\x45\x55\x52","\x26\x65\x75\x72\x6F\x3B","\x45\x75\x72\x6F","\x48\x4B\x44","\x48\x6F\x6E\x67\x20\x4B\x6F\x6E\x67\x20\x44\x6F\x6C\x6C\x61\x72","\x48\x55\x46","\x26\x23\x37\x30\x3B\x26\x23\x31\x31\x36\x3B","\x48\x75\x6E\x67\x61\x72\x69\x61\x6E\x20\x46\x6F\x72\x69\x6E\x74","\x49\x4C\x53","\x26\x23\x38\x33\x36\x32\x3B","\x49\x73\x72\x61\x65\x6C\x69\x20\x4E\x65\x77\x20\x53\x68\x65\x71\x65\x6C","\x4A\x50\x59","\x26\x79\x65\x6E\x3B","\x4A\x61\x70\x61\x6E\x65\x73\x65\x20\x59\x65\x6E","\x4D\x58\x4E","\x4D\x65\x78\x69\x63\x61\x6E\x20\x50\x65\x73\x6F","\x4E\x4F\x4B","\x4E\x4F\x4B\x26\x6E\x62\x73\x70\x3B","\x4E\x6F\x72\x77\x65\x67\x69\x61\x6E\x20\x4B\x72\x6F\x6E\x65","\x4E\x5A\x44","\x4E\x65\x77\x20\x5A\x65\x61\x6C\x61\x6E\x64\x20\x44\x6F\x6C\x6C\x61\x72","\x50\x4C\x4E","\x50\x4C\x4E\x26\x6E\x62\x73\x70\x3B","\x50\x6F\x6C\x69\x73\x68\x20\x5A\x6C\x6F\x74\x79","\x47\x42\x50","\x26\x70\x6F\x75\x6E\x64\x3B","\x50\x6F\x75\x6E\x64\x20\x53\x74\x65\x72\x6C\x69\x6E\x67","\x53\x47\x44","\x53\x69\x6E\x67\x61\x70\x6F\x72\x65\x20\x44\x6F\x6C\x6C\x61\x72","\x53\x45\x4B","\x53\x45\x4B\x26\x6E\x62\x73\x70\x3B","\x53\x77\x65\x64\x69\x73\x68\x20\x4B\x72\x6F\x6E\x61","\x43\x48\x46","\x43\x48\x46\x26\x6E\x62\x73\x70\x3B","\x53\x77\x69\x73\x73\x20\x46\x72\x61\x6E\x63","\x54\x48\x42","\x26\x23\x33\x36\x34\x37\x3B","\x54\x68\x61\x69\x20\x42\x61\x68\x74","\x42\x54\x43","\x20\x42\x54\x43","\x42\x69\x74\x63\x6F\x69\x6E","\x50\x61\x79\x50\x61\x6C","\x79\x6F\x75\x40\x79\x6F\x75\x72\x73\x2E\x63\x6F\x6D","\x65\x6E\x67\x6C\x69\x73\x68\x2D\x75\x73","\x64\x69\x76","\x6E\x61\x6D\x65","\x4E\x61\x6D\x65","\x70\x72\x69\x63\x65","\x50\x72\x69\x63\x65","\x63\x75\x72\x72\x65\x6E\x63\x79","\x64\x65\x63\x72\x65\x6D\x65\x6E\x74","\x71\x75\x61\x6E\x74\x69\x74\x79","\x51\x74\x79","\x69\x6E\x63\x72\x65\x6D\x65\x6E\x74","\x74\x6F\x74\x61\x6C","\x53\x75\x62\x54\x6F\x74\x61\x6C","\x72\x65\x6D\x6F\x76\x65","\x52\x65\x6D\x6F\x76\x65","\x74\x68\x75\x6D\x62","\x72\x65\x61\x64\x79","\x63\x61\x6C\x6C","\x68\x61\x73\x4F\x77\x6E\x50\x72\x6F\x70\x65\x72\x74\x79","\x70\x72\x6F\x74\x6F\x74\x79\x70\x65","\x62\x65\x66\x6F\x72\x65\x41\x64\x64","\x74\x72\x69\x67\x67\x65\x72","\x68\x61\x73","\x69\x64","\x75\x70\x64\x61\x74\x65","\x61\x66\x74\x65\x72\x41\x64\x64","\x6D\x61\x74\x63\x68","\x3C\x3D","\x72\x65\x70\x6C\x61\x63\x65","\x67\x65\x74","\x3C","\x3E\x3D","\x3E","\x65\x61\x63\x68","\x66\x69\x6E\x64","\x65\x71\x75\x61\x6C\x73","\x74\x61\x78","\x73\x68\x69\x70\x70\x69\x6E\x67","\x73\x61\x76\x65","\x6C\x6F\x61\x64","\x63\x72\x65\x61\x74\x65\x45\x6C\x65\x6D\x65\x6E\x74","\x2E","\x73\x70\x6C\x69\x74","\x73\x68\x69\x66\x74","\x45\x4C\x45\x4D\x45\x4E\x54","\x62\x65\x66\x6F\x72\x65\x53\x61\x76\x65","\x66\x69\x65\x6C\x64\x73","\x6F\x70\x74\x69\x6F\x6E\x73","\x5F\x69\x74\x65\x6D\x73","\x73\x74\x72\x69\x6E\x67\x69\x66\x79","\x73\x65\x74\x49\x74\x65\x6D","\x61\x66\x74\x65\x72\x53\x61\x76\x65","\x67\x65\x74\x49\x74\x65\x6D","\x70\x61\x72\x73\x65","\x61\x64\x64","\x45\x72\x72\x6F\x72\x20\x4C\x6F\x61\x64\x69\x6E\x67\x20\x64\x61\x74\x61\x3A\x20","\x65\x72\x72\x6F\x72","\x62\x69\x6E\x64","\x6D\x65\x73\x73\x61\x67\x65","\x73\x69\x6D\x70\x6C\x65\x43\x61\x72\x74\x28\x6A\x73\x29\x20\x45\x72\x72\x6F\x72\x3A\x20","\x6C\x6F\x67","\x74\x61\x78\x53\x68\x69\x70\x70\x69\x6E\x67","\x74\x61\x78\x52\x61\x74\x65","\x73\x68\x69\x70\x70\x69\x6E\x67\x51\x75\x61\x6E\x74\x69\x74\x79\x52\x61\x74\x65","\x73\x68\x69\x70\x70\x69\x6E\x67\x54\x6F\x74\x61\x6C\x52\x61\x74\x65","\x73\x68\x69\x70\x70\x69\x6E\x67\x46\x6C\x61\x74\x52\x61\x74\x65","\x73\x68\x69\x70\x70\x69\x6E\x67\x43\x75\x73\x74\x6F\x6D","\x74\x6F\x43\x75\x72\x72\x65\x6E\x63\x79","\x3C\x61\x20\x68\x72\x65\x66\x3D\x27","\x27\x3E","\x74\x65\x78\x74","\x3C\x2F\x61\x3E","\x3C\x61\x20\x68\x72\x65\x66\x3D\x27\x6A\x61\x76\x61\x73\x63\x72\x69\x70\x74\x3A\x3B\x27\x20\x63\x6C\x61\x73\x73\x3D\x27","\x5F\x64\x65\x63\x72\x65\x6D\x65\x6E\x74\x27\x3E","\x2D","\x5F\x69\x6E\x63\x72\x65\x6D\x65\x6E\x74\x27\x3E","\x2B","\x3C\x69\x6D\x67\x20\x73\x72\x63\x3D\x27","\x27\x2F\x3E","\x3C\x69\x6E\x70\x75\x74\x20\x74\x79\x70\x65\x3D\x27\x74\x65\x78\x74\x27\x20\x76\x61\x6C\x75\x65\x3D\x27","\x27\x20\x63\x6C\x61\x73\x73\x3D\x27","\x5F\x69\x6E\x70\x75\x74\x27\x2F\x3E","\x5F\x72\x65\x6D\x6F\x76\x65\x27\x3E","\x58","\x74\x6F\x4C\x6F\x77\x65\x72\x43\x61\x73\x65","\x63\x61\x72\x74\x53\x74\x79\x6C\x65","\x74\x61\x62\x6C\x65","\x74\x72","\x74\x68","\x74\x64","\x68\x65\x61\x64\x65\x72\x52\x6F\x77","\x61\x64\x64\x43\x6C\x61\x73\x73","\x61\x70\x70\x65\x6E\x64","\x20","\x68\x74\x6D\x6C","\x6C\x65\x6E\x67\x74\x68","\x63\x61\x72\x74\x43\x6F\x6C\x75\x6D\x6E\x73","\x69\x74\x65\x6D\x2D","\x76\x69\x65\x77","\x6C\x61\x62\x65\x6C","\x63\x65\x6C\x6C","\x63\x6C\x61\x73\x73\x4E\x61\x6D\x65","\x63\x72\x65\x61\x74\x65\x43\x61\x72\x74\x52\x6F\x77","\x63\x61\x72\x74\x49\x74\x65\x6D\x5F","\x69\x74\x65\x6D\x52\x6F\x77\x20\x72\x6F\x77\x2D","\x65\x76\x65\x6E","\x6F\x64\x64","\x49\x74\x65\x6D","\x64\x65\x63\x69\x6D\x61\x6C","\x64\x65\x6C\x69\x6D\x69\x74\x65\x72","\x53\x43\x49\x2D","\x73\x65\x74","\x72\x65\x73\x65\x72\x76\x65\x64\x46\x69\x65\x6C\x64\x73","\x5F","\x62\x65\x66\x6F\x72\x65\x52\x65\x6D\x6F\x76\x65","\x71\x75\x61\x6E\x74\x69\x74\x79\x20\x69\x64\x20\x69\x74\x65\x6D\x5F\x6E\x75\x6D\x62\x65\x72\x20\x70\x72\x69\x63\x65\x20\x6E\x61\x6D\x65\x20\x73\x68\x69\x70\x70\x69\x6E\x67\x20\x74\x61\x78\x20\x74\x61\x78\x52\x61\x74\x65","\x73\x79\x6D\x62\x6F\x6C","\x63\x75\x73\x74\x6F\x6D","\x74\x79\x70\x65","\x63\x68\x65\x63\x6B\x6F\x75\x74","\x66\x6E","\x64\x61\x74\x61","\x61\x63\x74\x69\x6F\x6E","\x6D\x65\x74\x68\x6F\x64","\x62\x65\x66\x6F\x72\x65\x43\x68\x65\x63\x6B\x6F\x75\x74","\x67\x65\x6E\x65\x72\x61\x74\x65\x41\x6E\x64\x53\x65\x6E\x64\x46\x6F\x72\x6D","\x4E\x6F\x20\x56\x61\x6C\x69\x64\x20\x43\x68\x65\x63\x6B\x6F\x75\x74\x20\x4D\x65\x74\x68\x6F\x64\x20\x53\x70\x65\x63\x69\x66\x69\x65\x64","\x66\x6F\x72\x6D","\x73\x74\x79\x6C\x65","\x64\x69\x73\x70\x6C\x61\x79\x3A\x6E\x6F\x6E\x65\x3B","\x76\x61\x6C","\x68\x69\x64\x64\x65\x6E","\x69\x6E\x70\x75\x74","\x62\x6F\x64\x79","\x73\x75\x62\x6D\x69\x74","\x65\x6C","\x65\x6D\x61\x69\x6C","\x4E\x6F\x20\x65\x6D\x61\x69\x6C\x20\x70\x72\x6F\x76\x69\x64\x65\x64\x20\x66\x6F\x72\x20\x50\x61\x79\x50\x61\x6C\x20\x63\x68\x65\x63\x6B\x6F\x75\x74","\x5F\x63\x61\x72\x74","\x31","\x63\x6F\x64\x65","\x47\x45\x54","\x30","\x32","\x74\x6F\x46\x69\x78\x65\x64","\x75\x74\x66\x2D\x38","\x73\x61\x6E\x64\x62\x6F\x78","\x68\x74\x74\x70\x73\x3A\x2F\x2F\x77\x77\x77\x2E\x73\x61\x6E\x64\x62\x6F\x78\x2E\x70\x61\x79\x70\x61\x6C\x2E\x63\x6F\x6D\x2F\x63\x67\x69\x2D\x62\x69\x6E\x2F\x77\x65\x62\x73\x63\x72","\x68\x74\x74\x70\x73\x3A\x2F\x2F\x77\x77\x77\x2E\x70\x61\x79\x70\x61\x6C\x2E\x63\x6F\x6D\x2F\x63\x67\x69\x2D\x62\x69\x6E\x2F\x77\x65\x62\x73\x63\x72","\x50\x4F\x53\x54","\x73\x75\x63\x63\x65\x73\x73","\x72\x65\x74\x75\x72\x6E","\x63\x61\x6E\x63\x65\x6C","\x63\x61\x6E\x63\x65\x6C\x5F\x72\x65\x74\x75\x72\x6E","\x6E\x6F\x74\x69\x66\x79","\x6E\x6F\x74\x69\x66\x79\x5F\x75\x72\x6C","\x69\x74\x65\x6D\x5F\x6E\x61\x6D\x65\x5F","\x71\x75\x61\x6E\x74\x69\x74\x79\x5F","\x61\x6D\x6F\x75\x6E\x74\x5F","\x69\x74\x65\x6D\x5F\x6E\x75\x6D\x62\x65\x72\x5F","\x69\x74\x65\x6D\x5F\x6E\x75\x6D\x62\x65\x72","\x65\x78\x63\x6C\x75\x64\x65\x46\x72\x6F\x6D\x43\x68\x65\x63\x6B\x6F\x75\x74","\x6F\x6E","\x6F\x73","\x6F\x70\x74\x69\x6F\x6E\x5F\x69\x6E\x64\x65\x78\x5F","\x6D\x69\x6E","\x6D\x65\x72\x63\x68\x61\x6E\x74\x49\x44","\x4E\x6F\x20\x6D\x65\x72\x63\x68\x61\x6E\x74\x20\x69\x64\x20\x70\x72\x6F\x76\x69\x64\x65\x64\x20\x66\x6F\x72\x20\x47\x6F\x6F\x67\x6C\x65\x43\x68\x65\x63\x6B\x6F\x75\x74","\x47\x6F\x6F\x67\x6C\x65\x20\x43\x68\x65\x63\x6B\x6F\x75\x74\x20\x6F\x6E\x6C\x79\x20\x61\x63\x63\x65\x70\x74\x73\x20\x55\x53\x44\x20\x61\x6E\x64\x20\x47\x42\x50","\x53\x68\x69\x70\x70\x69\x6E\x67","\x68\x74\x74\x70\x73\x3A\x2F\x2F\x63\x68\x65\x63\x6B\x6F\x75\x74\x2E\x67\x6F\x6F\x67\x6C\x65\x2E\x63\x6F\x6D\x2F\x61\x70\x69\x2F\x63\x68\x65\x63\x6B\x6F\x75\x74\x2F\x76\x32\x2F\x63\x68\x65\x63\x6B\x6F\x75\x74\x46\x6F\x72\x6D\x2F\x4D\x65\x72\x63\x68\x61\x6E\x74\x2F","\x69\x74\x65\x6D\x5F\x71\x75\x61\x6E\x74\x69\x74\x79\x5F","\x69\x74\x65\x6D\x5F\x70\x72\x69\x63\x65\x5F","\x69\x74\x65\x6D\x5F\x63\x75\x72\x72\x65\x6E\x63\x79\x5F\x20","\x69\x74\x65\x6D\x5F\x74\x61\x78\x5F\x72\x61\x74\x65","\x3A\x20","\x69\x74\x65\x6D\x5F\x64\x65\x73\x63\x72\x69\x70\x74\x69\x6F\x6E\x5F","\x2C\x20","\x6A\x6F\x69\x6E","\x6D\x65\x72\x63\x68\x61\x6E\x74\x5F\x73\x69\x67\x6E\x61\x74\x75\x72\x65","\x4E\x6F\x20\x6D\x65\x72\x63\x68\x61\x6E\x74\x20\x73\x69\x67\x6E\x61\x74\x75\x72\x65\x20\x70\x72\x6F\x76\x69\x64\x65\x64\x20\x66\x6F\x72\x20\x41\x6D\x61\x7A\x6F\x6E\x20\x50\x61\x79\x6D\x65\x6E\x74\x73","\x6D\x65\x72\x63\x68\x61\x6E\x74\x5F\x69\x64","\x4E\x6F\x20\x6D\x65\x72\x63\x68\x61\x6E\x74\x20\x69\x64\x20\x70\x72\x6F\x76\x69\x64\x65\x64\x20\x66\x6F\x72\x20\x41\x6D\x61\x7A\x6F\x6E\x20\x50\x61\x79\x6D\x65\x6E\x74\x73","\x61\x77\x73\x5F\x61\x63\x63\x65\x73\x73\x5F\x6B\x65\x79\x5F\x69\x64","\x4E\x6F\x20\x41\x57\x53\x20\x61\x63\x63\x65\x73\x73\x20\x6B\x65\x79\x20\x69\x64\x20\x70\x72\x6F\x76\x69\x64\x65\x64\x20\x66\x6F\x72\x20\x41\x6D\x61\x7A\x6F\x6E\x20\x50\x61\x79\x6D\x65\x6E\x74\x73","\x77\x65\x69\x67\x68\x74\x5F\x75\x6E\x69\x74","\x6C\x62","\x68\x74\x74\x70\x73\x3A\x2F\x2F\x70\x61\x79\x6D\x65\x6E\x74\x73","\x2D\x73\x61\x6E\x64\x62\x6F\x78","\x2E\x61\x6D\x61\x7A\x6F\x6E\x2E\x63\x6F\x6D\x2F\x63\x68\x65\x63\x6B\x6F\x75\x74\x2F","\x69\x74\x65\x6D\x5F\x74\x69\x74\x6C\x65\x5F","\x69\x74\x65\x6D\x5F\x73\x6B\x75\x5F\x20","\x73\x6B\x75","\x69\x74\x65\x6D\x5F\x6D\x65\x72\x63\x68\x61\x6E\x74\x5F\x69\x64\x5F","\x77\x65\x69\x67\x68\x74","\x69\x74\x65\x6D\x5F\x77\x65\x69\x67\x68\x74\x5F","\x73\x68\x69\x70\x70\x69\x6E\x67\x5F\x6D\x65\x74\x68\x6F\x64\x5F\x70\x72\x69\x63\x65\x5F\x70\x65\x72\x5F\x75\x6E\x69\x74\x5F\x72\x61\x74\x65\x5F","\x75\x72\x6C","\x55\x52\x4C\x20\x72\x65\x71\x75\x69\x72\x65\x64\x20\x66\x6F\x72\x20\x53\x65\x6E\x64\x46\x6F\x72\x6D\x20\x43\x68\x65\x63\x6B\x6F\x75\x74","\x69\x74\x65\x6D\x5F\x6F\x70\x74\x69\x6F\x6E\x73\x5F","\x65\x78\x74\x72\x61\x5F\x64\x61\x74\x61","\x65\x78\x74\x65\x6E\x64\x43\x68\x65\x63\x6B\x6F\x75\x74","\x5F\x65\x76\x65\x6E\x74\x73","\x61\x70\x70\x6C\x79","\x24","\x2C","\x61\x63\x63\x75\x72\x61\x63\x79","\x72\x65\x76\x65\x72\x73\x65","\x63\x68\x75\x6E\x6B","\x61\x66\x74\x65\x72","\x2E\x7B\x31\x2C","\x7D","\x67","\x73\x65\x74\x4F\x75\x74\x6C\x65\x74","\x73\x65\x6C\x65\x63\x74\x6F\x72","\x65\x76\x65\x6E\x74","\x63\x61\x6C\x6C\x62\x61\x63\x6B","\x73\x65\x74\x49\x6E\x70\x75\x74","\x6C\x69\x76\x65","\x63\x72\x65\x61\x74\x65","\x76\x61\x6C\x75\x65","\x64\x69\x73\x70\x6F\x73\x65","\x72\x65\x6D\x6F\x76\x65\x43\x6C\x61\x73\x73","\x61\x64\x6F\x70\x74","\x63\x6C\x69\x63\x6B","\x61\x64\x64\x45\x76\x65\x6E\x74","\x66\x69\x72\x65\x45\x76\x65\x6E\x74","\x3A\x72\x65\x6C\x61\x79\x28","\x29","\x67\x65\x74\x50\x61\x72\x65\x6E\x74","\x67\x65\x74\x45\x6C\x65\x6D\x65\x6E\x74\x73","\x74\x61\x67\x4E\x61\x6D\x65","\x69\x6E\x6E\x65\x72\x48\x54\x4D\x4C","\x72\x65\x61\x64\x41\x74\x74\x72\x69\x62\x75\x74\x65","\x77\x72\x69\x74\x65\x41\x74\x74\x72\x69\x62\x75\x74\x65","\x61\x70\x70\x65\x6E\x64\x43\x68\x69\x6C\x64","\x61\x64\x64\x43\x6C\x61\x73\x73\x4E\x61\x6D\x65","\x72\x65\x6D\x6F\x76\x65\x43\x6C\x61\x73\x73\x4E\x61\x6D\x65","\x6F\x62\x73\x65\x72\x76\x65","\x66\x69\x72\x65","\x66\x69\x6E\x64\x45\x6C\x65\x6D\x65\x6E\x74","\x75\x70","\x67\x65\x74\x45\x6C\x65\x6D\x65\x6E\x74\x73\x42\x79\x53\x65\x6C\x65\x63\x74\x6F\x72","\x64\x65\x73\x63\x65\x6E\x64\x61\x6E\x74\x73","\x70\x61\x73\x73\x74\x68\x72\x6F\x75\x67\x68","\x64\x65\x6C\x65\x67\x61\x74\x65","\x70\x61\x72\x65\x6E\x74","\x63\x6C\x6F\x73\x65\x73\x74","\x73\x65\x74\x75\x70\x56\x69\x65\x77\x54\x6F\x6F\x6C","\x77\x72\x69\x74\x65\x43\x61\x72\x74","\x67\x72\x61\x6E\x64\x54\x6F\x74\x61\x6C","\x62\x69\x6E\x64\x4F\x75\x74\x6C\x65\x74\x73","\x65\x6D\x70\x74\x79","\x2E\x69\x74\x65\x6D\x52\x6F\x77","\x63\x68\x61\x6E\x67\x65","\x63\x6C\x61\x73\x73","\x73\x68\x65\x6C\x66\x49\x74\x65\x6D\x20\x2E\x69\x74\x65\x6D\x5F\x61\x64\x64","\x74\x65\x78\x74\x61\x72\x65\x61","\x63\x68\x65\x63\x6B\x62\x6F\x78","\x72\x61\x64\x69\x6F","\x63\x68\x65\x63\x6B\x65\x64","\x6E\x75\x6D\x62\x65\x72","\x73\x65\x6C\x65\x63\x74","\x73\x72\x63","\x69\x6D\x67","\x74\x61\x67","\x5F\x73\x68\x65\x6C\x66\x49\x74\x65\x6D","\x62\x69\x6E\x64\x49\x6E\x70\x75\x74\x73","\x61\x64\x64\x45\x76\x65\x6E\x74\x4C\x69\x73\x74\x65\x6E\x65\x72","\x44\x4F\x4D\x43\x6F\x6E\x74\x65\x6E\x74\x4C\x6F\x61\x64\x65\x64","\x72\x65\x6D\x6F\x76\x65\x45\x76\x65\x6E\x74\x4C\x69\x73\x74\x65\x6E\x65\x72","\x61\x74\x74\x61\x63\x68\x45\x76\x65\x6E\x74","\x63\x6F\x6D\x70\x6C\x65\x74\x65","\x72\x65\x61\x64\x79\x53\x74\x61\x74\x65","\x6F\x6E\x72\x65\x61\x64\x79\x73\x74\x61\x74\x65\x63\x68\x61\x6E\x67\x65","\x64\x65\x74\x61\x63\x68\x45\x76\x65\x6E\x74","\x6F\x6E\x6C\x6F\x61\x64","\x66\x72\x61\x6D\x65\x45\x6C\x65\x6D\x65\x6E\x74","\x6C\x61\x73\x74\x49\x6E\x64\x65\x78","\x74\x65\x73\x74","\x22","\x5C\x75","\x73\x6C\x69\x63\x65","\x30\x30\x30\x30","\x63\x68\x61\x72\x43\x6F\x64\x65\x41\x74","\x74\x6F\x4A\x53\x4F\x4E","\x6E\x75\x6C\x6C","\x62\x6F\x6F\x6C\x65\x61\x6E","\x5B\x6F\x62\x6A\x65\x63\x74\x20\x41\x72\x72\x61\x79\x5D","\x74\x6F\x53\x74\x72\x69\x6E\x67","\x5B\x5D","\x5B\x0A","\x2C\x0A","\x0A","\x5D","\x5B","\x3A","\x7B\x7D","\x7B\x0A","\x7B","\x67\x65\x74\x55\x54\x43\x46\x75\x6C\x6C\x59\x65\x61\x72","\x67\x65\x74\x55\x54\x43\x4D\x6F\x6E\x74\x68","\x67\x65\x74\x55\x54\x43\x44\x61\x74\x65","\x54","\x67\x65\x74\x55\x54\x43\x48\x6F\x75\x72\x73","\x67\x65\x74\x55\x54\x43\x4D\x69\x6E\x75\x74\x65\x73","\x67\x65\x74\x55\x54\x43\x53\x65\x63\x6F\x6E\x64\x73","\x5A","\x5C\x62","\x5C\x74","\x5C\x6E","\x5C\x66","\x5C\x72","\x5C\x22","\x5C\x5C","\x4A\x53\x4F\x4E\x2E\x73\x74\x72\x69\x6E\x67\x69\x66\x79","\x40","\x28","\x4A\x53\x4F\x4E\x2E\x70\x61\x72\x73\x65","\x67\x6C\x6F\x62\x61\x6C\x53\x74\x6F\x72\x61\x67\x65","\x64\x69\x73\x70\x6C\x61\x79","\x6E\x6F\x6E\x65","\x68\x65\x61\x64","\x67\x65\x74\x45\x6C\x65\x6D\x65\x6E\x74\x73\x42\x79\x54\x61\x67\x4E\x61\x6D\x65","\x61\x64\x64\x42\x65\x68\x61\x76\x69\x6F\x72","\x23\x64\x65\x66\x61\x75\x6C\x74\x23\x75\x73\x65\x72\x64\x61\x74\x61","\x67\x65\x74\x41\x74\x74\x72\x69\x62\x75\x74\x65","\x73\x65\x74\x41\x74\x74\x72\x69\x62\x75\x74\x65","\x72\x65\x6D\x6F\x76\x65\x41\x74\x74\x72\x69\x62\x75\x74\x65","\x61\x74\x74\x72\x69\x62\x75\x74\x65\x73","\x58\x4D\x4C\x44\x6F\x63\x75\x6D\x65\x6E\x74","\x69\x6D\x61\x67\x65","\x3C\x69\x20\x63\x6C\x61\x73\x73\x3D\x27\x66\x61\x20\x66\x61\x2D\x6D\x69\x6E\x75\x73\x27\x3E\x3C\x2F\x69\x3E","\x3C\x69\x20\x63\x6C\x61\x73\x73\x3D\x27\x66\x61\x20\x66\x61\x2D\x70\x6C\x75\x73\x27\x3E\x3C\x2F\x69\x3E","\x3C\x69\x20\x63\x6C\x61\x73\x73\x3D\x27\x66\x61\x20\x66\x61\x2D\x74\x72\x61\x73\x68\x27\x3E\x3C\x2F\x69\x3E","\x70\x72\x65\x76\x65\x6E\x74\x44\x65\x66\x61\x75\x6C\x74","\x61\x63\x74\x69\x76\x65","\x2E\x74\x61\x62\x2C\x20\x2E\x70\x61\x6E\x65\x6C","\x23","\x70\x61\x6E\x65\x6C","\x66\x6F\x63\x75\x73","\x2E\x74\x61\x62"];(function(_0x49fcx1,_0x49fcx2){var _0x49fcx3=_0x71d9[0],_0x49fcx4=function(_0x49fcx5,_0x49fcx2){return  typeof _0x49fcx5=== _0x49fcx2},_0x49fcx5=function(_0x49fcx5){return _0x49fcx4(_0x49fcx5,_0x71d9[1])},_0x49fcx6=function(_0x49fcx5){return _0x49fcx4(_0x49fcx5,_0x71d9[2])},_0x49fcx7=function(_0x49fcx5){return _0x71d9[3]===  typeof HTMLElement?_0x49fcx5 instanceof  HTMLElement:_0x71d9[3]===  typeof _0x49fcx5&& 1=== _0x49fcx5[_0x71d9[4]]&& _0x71d9[0]===  typeof _0x49fcx5[_0x71d9[5]]},_0x49fcx8=function(_0x49fcx9){function _0x49fcxa(_0x49fcxb){return _0x49fcx16[_0x71d9[8]]({attr:_0x71d9[6],label:_0x71d9[6],view:_0x71d9[7],text:_0x71d9[6],className:_0x71d9[6],hide:!1},_0x49fcxb|| {})}function _0x49fcxc(){if(!_0x49fcx16[_0x71d9[9]]){try{_0x49fcx2[_0x71d9[12]][_0x71d9[11]](_0x71d9[10])}catch(a){setTimeout(_0x49fcxc,1);return};_0x49fcx16[_0x71d9[13]]()}}var _0x49fcxd={MooTools:_0x71d9[14],Prototype:_0x71d9[14],jQuery:_0x71d9[15]},_0x49fcxe=0,_0x49fcxf={},_0x49fcx10=_0x49fcx9|| _0x71d9[16],_0x49fcx11={};_0x49fcx9= {};_0x49fcx9= {};var _0x49fcx12=_0x49fcx1[_0x71d9[17]],_0x49fcx13=_0x49fcx1[_0x71d9[18]]|| {msgs:[],log:function(_0x49fcxb){_0x49fcx13[_0x71d9[20]][_0x71d9[19]](_0x49fcxb)}},_0x49fcx14={USD:{code:_0x71d9[21],symbol:_0x71d9[22],name:_0x71d9[23]},AUD:{code:_0x71d9[24],symbol:_0x71d9[22],name:_0x71d9[25]},BRL:{code:_0x71d9[26],symbol:_0x71d9[27],name:_0x71d9[28]},CAD:{code:_0x71d9[29],symbol:_0x71d9[22],name:_0x71d9[30]},CZK:{code:_0x71d9[31],symbol:_0x71d9[32],name:_0x71d9[33],after:!0},DKK:{code:_0x71d9[34],symbol:_0x71d9[35],name:_0x71d9[36]},EUR:{code:_0x71d9[37],symbol:_0x71d9[38],name:_0x71d9[39]},HKD:{code:_0x71d9[40],symbol:_0x71d9[22],name:_0x71d9[41]},HUF:{code:_0x71d9[42],symbol:_0x71d9[43],name:_0x71d9[44]},ILS:{code:_0x71d9[45],symbol:_0x71d9[46],name:_0x71d9[47]},JPY:{code:_0x71d9[48],symbol:_0x71d9[49],name:_0x71d9[50],accuracy:0},MXN:{code:_0x71d9[51],symbol:_0x71d9[22],name:_0x71d9[52]},NOK:{code:_0x71d9[53],symbol:_0x71d9[54],name:_0x71d9[55]},NZD:{code:_0x71d9[56],symbol:_0x71d9[22],name:_0x71d9[57]},PLN:{code:_0x71d9[58],symbol:_0x71d9[59],name:_0x71d9[60]},GBP:{code:_0x71d9[61],symbol:_0x71d9[62],name:_0x71d9[63]},SGD:{code:_0x71d9[64],symbol:_0x71d9[22],name:_0x71d9[65]},SEK:{code:_0x71d9[66],symbol:_0x71d9[67],name:_0x71d9[68]},CHF:{code:_0x71d9[69],symbol:_0x71d9[70],name:_0x71d9[71]},THB:{code:_0x71d9[72],symbol:_0x71d9[73],name:_0x71d9[74]},BTC:{code:_0x71d9[75],symbol:_0x71d9[76],name:_0x71d9[77],accuracy:4,after:!0}},_0x49fcx15={checkout:{type:_0x71d9[78],email:_0x71d9[79]},currency:_0x71d9[21],language:_0x71d9[80],cartStyle:_0x71d9[81],cartColumns:[{attr:_0x71d9[82],label:_0x71d9[83]},{attr:_0x71d9[84],label:_0x71d9[85],view:_0x71d9[86]},{view:_0x71d9[87],label:!1},{attr:_0x71d9[88],label:_0x71d9[89]},{view:_0x71d9[90],label:!1},{attr:_0x71d9[91],label:_0x71d9[92],view:_0x71d9[86]},{view:_0x71d9[93],text:_0x71d9[94],label:!1}],excludeFromCheckout:[_0x71d9[95]],shippingFlatRate:0,shippingQuantityRate:0,shippingTotalRate:0,shippingCustom:null,taxRate:0,taxShipping:!1,data:{}},_0x49fcx16=function(_0x49fcxb){if(_0x49fcx6(_0x49fcxb)){return _0x49fcx16[_0x71d9[96]](_0x49fcxb)};if(_0x49fcx4(_0x49fcxb,_0x71d9[3])){return _0x49fcx16[_0x71d9[8]](_0x49fcx15,_0x49fcxb)}},_0x49fcx17,_0x49fcx18;_0x49fcx16[_0x71d9[8]]= function(_0x49fcxb,_0x49fcx19){var _0x49fcx1a;_0x49fcx5(_0x49fcx19)&& (_0x49fcx19= _0x49fcxb,_0x49fcxb= _0x49fcx16);for(_0x49fcx1a in _0x49fcx19){Object[_0x71d9[99]][_0x71d9[98]][_0x71d9[97]](_0x49fcx19,_0x49fcx1a)&& (_0x49fcxb[_0x49fcx1a]= _0x49fcx19[_0x49fcx1a])};return _0x49fcxb};_0x49fcx16[_0x71d9[8]]({copy:function(_0x49fcxb){_0x49fcxb= _0x49fcx8(_0x49fcxb);_0x49fcxb[_0x71d9[13]]();return _0x49fcxb}});_0x49fcx16[_0x71d9[8]]({isReady:!1,add:function(_0x49fcxb,_0x49fcx19){var _0x49fcx1a= new _0x49fcx16.Item(_0x49fcxb|| {}),_0x49fcx1b=!0,_0x49fcx1c=!0=== _0x49fcx19?_0x49fcx19:!1;if(!_0x49fcx1c&& (_0x49fcx1b= _0x49fcx16[_0x71d9[101]](_0x71d9[100],[_0x49fcx1a]),!1=== _0x49fcx1b)){return !1};(_0x49fcx1b= _0x49fcx16[_0x71d9[102]](_0x49fcx1a))?(_0x49fcx1b[_0x71d9[90]](_0x49fcx1a[_0x71d9[88]]()),_0x49fcx1a= _0x49fcx1b):_0x49fcxf[_0x49fcx1a[_0x71d9[103]]()]= _0x49fcx1a;_0x49fcx16[_0x71d9[104]]();_0x49fcx1c|| _0x49fcx16[_0x71d9[101]](_0x71d9[105],[_0x49fcx1a,_0x49fcx5(_0x49fcx1b)]);return _0x49fcx1a},each:function(_0x49fcxb,_0x49fcx19){var _0x49fcx1a,_0x49fcx1b=0,_0x49fcx1c,_0x49fcx5,_0x49fcx1d;if(_0x49fcx6(_0x49fcxb)){_0x49fcx5= _0x49fcxb,_0x49fcx1d= _0x49fcxf}else {if(_0x49fcx6(_0x49fcx19)){_0x49fcx5= _0x49fcx19,_0x49fcx1d= _0x49fcxb}else {return}};for(_0x49fcx1a in _0x49fcx1d){if(Object[_0x71d9[99]][_0x71d9[98]][_0x71d9[97]](_0x49fcx1d,_0x49fcx1a)){_0x49fcx1c= _0x49fcx5[_0x71d9[97]](_0x49fcx16,_0x49fcx1d[_0x49fcx1a],_0x49fcx1b,_0x49fcx1a);if(!1=== _0x49fcx1c){break};_0x49fcx1b+= 1}}},find:function(_0x49fcxb){var _0x49fcx19=[];if(_0x49fcx4(_0x49fcxf[_0x49fcxb],_0x71d9[3])){return _0x49fcxf[_0x49fcxb]};if(_0x49fcx4(_0x49fcxb,_0x71d9[3])){return _0x49fcx16[_0x71d9[113]](function(_0x49fcx1a){var _0x49fcx1b=!0;_0x49fcx16[_0x71d9[113]](_0x49fcxb,function(_0x49fcxb,_0x49fcx16,_0x49fcx19){_0x49fcx4(_0x49fcxb,_0x49fcx3)?_0x49fcxb[_0x71d9[106]](/<=.*/)?(_0x49fcxb= parseFloat(_0x49fcxb[_0x71d9[108]](_0x71d9[107],_0x71d9[6])),_0x49fcx1a[_0x71d9[109]](_0x49fcx19)&& parseFloat(_0x49fcx1a[_0x71d9[109]](_0x49fcx19))<= _0x49fcxb|| (_0x49fcx1b=  !1)):_0x49fcxb[_0x71d9[106]](/</)?(_0x49fcxb= parseFloat(_0x49fcxb[_0x71d9[108]](_0x71d9[110],_0x71d9[6])),_0x49fcx1a[_0x71d9[109]](_0x49fcx19)&& parseFloat(_0x49fcx1a[_0x71d9[109]](_0x49fcx19))< _0x49fcxb|| (_0x49fcx1b=  !1)):_0x49fcxb[_0x71d9[106]](/>=/)?(_0x49fcxb= parseFloat(_0x49fcxb[_0x71d9[108]](_0x71d9[111],_0x71d9[6])),_0x49fcx1a[_0x71d9[109]](_0x49fcx19)&& parseFloat(_0x49fcx1a[_0x71d9[109]](_0x49fcx19))>= _0x49fcxb|| (_0x49fcx1b=  !1)):_0x49fcxb[_0x71d9[106]](/>/)?(_0x49fcxb= parseFloat(_0x49fcxb[_0x71d9[108]](_0x71d9[112],_0x71d9[6])),_0x49fcx1a[_0x71d9[109]](_0x49fcx19)&& parseFloat(_0x49fcx1a[_0x71d9[109]](_0x49fcx19))> _0x49fcxb|| (_0x49fcx1b=  !1)):_0x49fcx1a[_0x71d9[109]](_0x49fcx19)&& _0x49fcx1a[_0x71d9[109]](_0x49fcx19)=== _0x49fcxb|| (_0x49fcx1b=  !1):_0x49fcx1a[_0x71d9[109]](_0x49fcx19)&& _0x49fcx1a[_0x71d9[109]](_0x49fcx19)=== _0x49fcxb|| (_0x49fcx1b=  !1);return _0x49fcx1b});_0x49fcx1b&& _0x49fcx19[_0x71d9[19]](_0x49fcx1a)}),_0x49fcx19};_0x49fcx5(_0x49fcxb)&& _0x49fcx16[_0x71d9[113]](function(_0x49fcxb){_0x49fcx19[_0x71d9[19]](_0x49fcxb)});return _0x49fcx19},items:function(){return this[_0x71d9[114]]()},has:function(_0x49fcxb){var _0x49fcx19=!1;_0x49fcx16[_0x71d9[113]](function(_0x49fcx16){_0x49fcx16[_0x71d9[115]](_0x49fcxb)&& (_0x49fcx19= _0x49fcx16)});return _0x49fcx19},empty:function(){var _0x49fcxb={};_0x49fcx16[_0x71d9[113]](function(_0x49fcx16){!1=== _0x49fcx16[_0x71d9[93]](!0) && (_0x49fcxb[_0x49fcx16[_0x71d9[103]]()]= _0x49fcx16)});_0x49fcxf= _0x49fcxb;_0x49fcx16[_0x71d9[104]]()},quantity:function(){var _0x49fcxb=0;_0x49fcx16[_0x71d9[113]](function(_0x49fcx16){_0x49fcxb+= _0x49fcx16[_0x71d9[88]]()});return _0x49fcxb},total:function(){var _0x49fcxb=0;_0x49fcx16[_0x71d9[113]](function(_0x49fcx16){_0x49fcxb+= _0x49fcx16[_0x71d9[91]]()});return _0x49fcxb},grandTotal:function(){return _0x49fcx16[_0x71d9[91]]()+ _0x49fcx16[_0x71d9[116]]()+ _0x49fcx16[_0x71d9[117]]()},update:function(){_0x49fcx16[_0x71d9[118]]();_0x49fcx16[_0x71d9[101]](_0x71d9[104])},init:function(){_0x49fcx16[_0x71d9[119]]();_0x49fcx16[_0x71d9[104]]();_0x49fcx16[_0x71d9[96]]()},$:function(_0x49fcxb){return  new _0x49fcx16.ELEMENT(_0x49fcxb)},$create:function(_0x49fcxb){return _0x49fcx16.$(_0x49fcx2[_0x71d9[120]](_0x49fcxb))},setupViewTool:function(){var _0x49fcxb,_0x49fcx19=_0x49fcx1,_0x49fcx1a;for(_0x49fcx1a in _0x49fcxd){if(Object[_0x71d9[99]][_0x71d9[98]][_0x71d9[97]](_0x49fcxd,_0x49fcx1a)&& _0x49fcx1[_0x49fcx1a]&& (_0x49fcxb= _0x49fcxd[_0x49fcx1a][_0x71d9[108]](_0x71d9[15],_0x49fcx1a)[_0x71d9[122]](_0x71d9[121]),(_0x49fcxb= _0x49fcxb[_0x71d9[123]]())&& (_0x49fcx19= _0x49fcx19[_0x49fcxb]),_0x71d9[2]===  typeof _0x49fcx19)){_0x49fcx17= _0x49fcx19;_0x49fcx16[_0x71d9[8]](_0x49fcx16[_0x71d9[124]]._,_0x49fcx11[_0x49fcx1a]);break}}},ids:function(){var _0x49fcxb=[];_0x49fcx16[_0x71d9[113]](function(_0x49fcx16){_0x49fcxb[_0x71d9[19]](_0x49fcx16[_0x71d9[103]]())});return _0x49fcxb},save:function(){_0x49fcx16[_0x71d9[101]](_0x71d9[125]);var _0x49fcxb={};_0x49fcx16[_0x71d9[113]](function(_0x49fcx19){_0x49fcxb[_0x49fcx19[_0x71d9[103]]()]= _0x49fcx16[_0x71d9[8]](_0x49fcx19[_0x71d9[126]](),_0x49fcx19[_0x71d9[127]]())});_0x49fcx12[_0x71d9[130]](_0x49fcx10+ _0x71d9[128],JSON[_0x71d9[129]](_0x49fcxb));_0x49fcx16[_0x71d9[101]](_0x71d9[131])},load:function(){_0x49fcxf= {};var _0x49fcxb=_0x49fcx12[_0x71d9[132]](_0x49fcx10+ _0x71d9[128]);if(_0x49fcxb){try{_0x49fcx16[_0x71d9[113]](JSON[_0x71d9[133]](_0x49fcxb),function(_0x49fcxb){_0x49fcx16[_0x71d9[134]](_0x49fcxb,!0)})}catch(d){_0x49fcx16[_0x71d9[136]](_0x71d9[135]+ d)};_0x49fcx16[_0x71d9[101]](_0x71d9[119])}},ready:function(_0x49fcxb){_0x49fcx6(_0x49fcxb)?_0x49fcx16[_0x71d9[9]]?_0x49fcxb[_0x71d9[97]](_0x49fcx16):_0x49fcx16[_0x71d9[137]](_0x71d9[96],_0x49fcxb):_0x49fcx5(_0x49fcxb)&&  !_0x49fcx16[_0x71d9[9]]&& (_0x49fcx16[_0x71d9[101]](_0x71d9[96]),_0x49fcx16[_0x71d9[9]]=  !0)},error:function(_0x49fcxb){var _0x49fcx19=_0x71d9[6];_0x49fcx4(_0x49fcxb,_0x49fcx3)?_0x49fcx19= _0x49fcxb:_0x49fcx4(_0x49fcxb,_0x71d9[3])&& _0x49fcx4(_0x49fcxb[_0x71d9[138]],_0x49fcx3)&& (_0x49fcx19= _0x49fcxb[_0x71d9[138]]);try{_0x49fcx13[_0x71d9[140]](_0x71d9[139]+ _0x49fcx19)}catch(c){};_0x49fcx16[_0x71d9[101]](_0x71d9[136],_0x49fcxb)}});_0x49fcx16[_0x71d9[8]]({tax:function(){var _0x49fcxb=_0x49fcx15[_0x71d9[141]]?_0x49fcx16[_0x71d9[91]]()+ _0x49fcx16[_0x71d9[117]]():_0x49fcx16[_0x71d9[91]](),_0x49fcx19=_0x49fcx16[_0x71d9[142]]()* _0x49fcxb;_0x49fcx16[_0x71d9[113]](function(_0x49fcxb){_0x49fcxb[_0x71d9[109]](_0x71d9[116])?_0x49fcx19+= _0x49fcxb[_0x71d9[109]](_0x71d9[116]):_0x49fcxb[_0x71d9[109]](_0x71d9[142])&& (_0x49fcx19+= _0x49fcxb[_0x71d9[109]](_0x71d9[142])* _0x49fcxb[_0x71d9[91]]())});return parseFloat(_0x49fcx19)},taxRate:function(){return _0x49fcx15[_0x71d9[142]]|| 0},shipping:function(_0x49fcxb){if(_0x49fcx6(_0x49fcxb)){_0x49fcx16({shippingCustom:_0x49fcxb})}else {var _0x49fcx19=_0x49fcx15[_0x71d9[143]]* _0x49fcx16[_0x71d9[88]]()+ _0x49fcx15[_0x71d9[144]]* _0x49fcx16[_0x71d9[91]]()+ _0x49fcx15[_0x71d9[145]];_0x49fcx6(_0x49fcx15[_0x71d9[146]])&& (_0x49fcx19+= _0x49fcx15[_0x71d9[146]][_0x71d9[97]](_0x49fcx16));_0x49fcx16[_0x71d9[113]](function(_0x49fcxb){_0x49fcx19+= parseFloat(_0x49fcxb[_0x71d9[109]](_0x71d9[117])|| 0)});return parseFloat(_0x49fcx19)}}});_0x49fcx18= {attr:function(_0x49fcxb,_0x49fcx16){return _0x49fcxb[_0x71d9[109]](_0x49fcx16[_0x71d9[7]])|| _0x71d9[6]},currency:function(_0x49fcxb,_0x49fcx19){return _0x49fcx16[_0x71d9[147]](_0x49fcxb[_0x71d9[109]](_0x49fcx19[_0x71d9[7]])|| 0)},link:function(_0x49fcxb,_0x49fcx16){return _0x71d9[148]+ _0x49fcxb[_0x71d9[109]](_0x49fcx16[_0x71d9[7]])+ _0x71d9[149]+ _0x49fcx16[_0x71d9[150]]+ _0x71d9[151]},decrement:function(_0x49fcxb,_0x49fcx16){return _0x71d9[152]+ _0x49fcx10+ _0x71d9[153]+ (_0x49fcx16[_0x71d9[150]]|| _0x71d9[154])+ _0x71d9[151]},increment:function(_0x49fcxb,_0x49fcx16){return _0x71d9[152]+ _0x49fcx10+ _0x71d9[155]+ (_0x49fcx16[_0x71d9[150]]|| _0x71d9[156])+ _0x71d9[151]},image:function(_0x49fcxb,_0x49fcx16){return _0x71d9[157]+ _0x49fcxb[_0x71d9[109]](_0x49fcx16[_0x71d9[7]])+ _0x71d9[158]},input:function(_0x49fcxb,_0x49fcx16){return _0x71d9[159]+ _0x49fcxb[_0x71d9[109]](_0x49fcx16[_0x71d9[7]])+ _0x71d9[160]+ _0x49fcx10+ _0x71d9[161]},remove:function(_0x49fcxb,_0x49fcx16){return _0x71d9[152]+ _0x49fcx10+ _0x71d9[162]+ (_0x49fcx16[_0x71d9[150]]|| _0x71d9[163])+ _0x71d9[151]}};_0x49fcx16[_0x71d9[8]]({writeCart:function(_0x49fcxb){var _0x49fcx19=_0x49fcx15[_0x71d9[165]][_0x71d9[164]](),_0x49fcx1a=_0x71d9[166]=== _0x49fcx19,_0x49fcx1b=_0x49fcx1a?_0x71d9[167]:_0x71d9[81],_0x49fcx1c=_0x49fcx1a?_0x71d9[168]:_0x71d9[81],_0x49fcx5=_0x49fcx1a?_0x71d9[169]:_0x71d9[81],_0x49fcx1d=_0x49fcx16.$create(_0x49fcx19),_0x49fcx19=_0x49fcx16.$create(_0x49fcx1b)[_0x71d9[171]](_0x71d9[170]),_0x49fcx2,_0x49fcx6;_0x49fcx16.$(_0x49fcxb)[_0x71d9[174]](_0x71d9[173])[_0x71d9[172]](_0x49fcx1d);_0x49fcx1d[_0x71d9[172]](_0x49fcx19);_0x49fcx1a= 0;for(_0x49fcx6= _0x49fcx15[_0x71d9[176]][_0x71d9[175]];_0x49fcx1a< _0x49fcx6;_0x49fcx1a+= 1){_0x49fcx2= _0x49fcxa(_0x49fcx15[_0x71d9[176]][_0x49fcx1a]),_0x49fcxb= _0x71d9[177]+ (_0x49fcx2[_0x71d9[7]]|| _0x49fcx2[_0x71d9[178]]|| _0x49fcx2[_0x71d9[179]]|| _0x49fcx2[_0x71d9[150]]|| _0x71d9[180])+ _0x71d9[173]+ _0x49fcx2[_0x71d9[181]],_0x49fcx2= _0x49fcx2[_0x71d9[179]]|| _0x71d9[6],_0x49fcx19[_0x71d9[172]](_0x49fcx16.$create(_0x49fcx1c)[_0x71d9[171]](_0x49fcxb)[_0x71d9[174]](_0x49fcx2))};_0x49fcx16[_0x71d9[113]](function(_0x49fcxb,_0x49fcx19){_0x49fcx16[_0x71d9[182]](_0x49fcxb,_0x49fcx19,_0x49fcx1b,_0x49fcx5,_0x49fcx1d)});return _0x49fcx1d},createCartRow:function(_0x49fcxb,_0x49fcx19,_0x49fcx1a,_0x49fcx1b,_0x49fcx1c){_0x49fcx19= _0x49fcx16.$create(_0x49fcx1a)[_0x71d9[171]](_0x71d9[184]+ _0x49fcx19+ _0x71d9[173]+ (_0x49fcx19% 2?_0x71d9[185]:_0x71d9[186]))[_0x71d9[7]](_0x71d9[103],_0x71d9[183]+ _0x49fcxb[_0x71d9[103]]());var _0x49fcx5,_0x49fcx2,_0x49fcx13;_0x49fcx1c[_0x71d9[172]](_0x49fcx19);_0x49fcx1c= 0;for(_0x49fcx1a= _0x49fcx15[_0x71d9[176]][_0x71d9[175]];_0x49fcx1c< _0x49fcx1a;_0x49fcx1c+= 1){_0x49fcx5= _0x49fcxa(_0x49fcx15[_0x71d9[176]][_0x49fcx1c]),_0x49fcx2= _0x71d9[177]+ (_0x49fcx5[_0x71d9[7]]|| (_0x49fcx4(_0x49fcx5[_0x71d9[178]],_0x49fcx3)?_0x49fcx5[_0x71d9[178]]:_0x49fcx5[_0x71d9[179]]|| _0x49fcx5[_0x71d9[150]]|| _0x71d9[180]))+ _0x71d9[173]+ _0x49fcx5[_0x71d9[181]],_0x49fcx13= _0x49fcxb,_0x49fcx13= (_0x49fcx6(_0x49fcx5[_0x71d9[178]])?_0x49fcx5[_0x71d9[178]]:_0x49fcx4(_0x49fcx5[_0x71d9[178]],_0x49fcx3)&& _0x49fcx6(_0x49fcx18[_0x49fcx5[_0x71d9[178]]])?_0x49fcx18[_0x49fcx5[_0x71d9[178]]]:_0x49fcx18[_0x71d9[7]])[_0x71d9[97]](_0x49fcx16,_0x49fcx13,_0x49fcx5),_0x49fcx2= _0x49fcx16.$create(_0x49fcx1b)[_0x71d9[171]](_0x49fcx2)[_0x71d9[174]](_0x49fcx13),_0x49fcx19[_0x71d9[172]](_0x49fcx2)};return _0x49fcx19}});_0x49fcx16[_0x71d9[187]]= function(_0x49fcxb){function _0x49fcx19(){_0x49fcx4(_0x49fcx1a[_0x71d9[84]],_0x49fcx3)&& (_0x49fcx1a[_0x71d9[84]]= parseFloat(_0x49fcx1a[_0x71d9[84]][_0x71d9[108]](_0x49fcx16[_0x71d9[86]]()[_0x71d9[188]],_0x71d9[121])[_0x71d9[108]](/[^0-9\.]+/ig,_0x71d9[6])));isNaN(_0x49fcx1a[_0x71d9[84]])&& (_0x49fcx1a[_0x71d9[84]]= 0);0> _0x49fcx1a[_0x71d9[84]]&& (_0x49fcx1a[_0x71d9[84]]= 0);_0x49fcx4(_0x49fcx1a[_0x71d9[88]],_0x49fcx3)&& (_0x49fcx1a[_0x71d9[88]]= parseInt(_0x49fcx1a[_0x71d9[88]][_0x71d9[108]](_0x49fcx16[_0x71d9[86]]()[_0x71d9[189]],_0x71d9[6]),10));isNaN(_0x49fcx1a[_0x71d9[88]])&& (_0x49fcx1a[_0x71d9[88]]= 1);0>= _0x49fcx1a[_0x71d9[88]]&& _0x49fcx1b[_0x71d9[93]]()}var _0x49fcx1a={},_0x49fcx1b=this;_0x49fcx4(_0x49fcxb,_0x71d9[3])&& _0x49fcx16[_0x71d9[8]](_0x49fcx1a,_0x49fcxb);_0x49fcxe+= 1;for(_0x49fcx1a[_0x71d9[103]]= _0x49fcx1a[_0x71d9[103]]|| _0x71d9[190]+ _0x49fcxe;!_0x49fcx5(_0x49fcxf[_0x49fcx1a[_0x71d9[103]]]);){_0x49fcxe+= 1,_0x49fcx1a[_0x71d9[103]]= _0x71d9[190]+ _0x49fcxe};_0x49fcx1b[_0x71d9[109]]= function(_0x49fcxb,_0x49fcx16){var _0x49fcx19=!_0x49fcx16;return _0x49fcx5(_0x49fcxb)?_0x49fcxb:_0x49fcx6(_0x49fcx1a[_0x49fcxb])?_0x49fcx1a[_0x49fcxb][_0x71d9[97]](_0x49fcx1b):_0x49fcx5(_0x49fcx1a[_0x49fcxb])?_0x49fcx6(_0x49fcx1b[_0x49fcxb])&& _0x49fcx19?_0x49fcx1b[_0x49fcxb][_0x71d9[97]](_0x49fcx1b):!_0x49fcx5(_0x49fcx1b[_0x49fcxb])&& _0x49fcx19?_0x49fcx1b[_0x49fcxb]:_0x49fcx1a[_0x49fcxb]:_0x49fcx1a[_0x49fcxb]};_0x49fcx1b[_0x71d9[191]]= function(_0x49fcxb,_0x49fcx16){_0x49fcx5(_0x49fcxb)|| (_0x49fcx1a[_0x49fcxb[_0x71d9[164]]()]= _0x49fcx16,_0x71d9[84]!== _0x49fcxb[_0x71d9[164]]()&& _0x71d9[88]!== _0x49fcxb[_0x71d9[164]]()|| _0x49fcx19());return _0x49fcx1b};_0x49fcx1b[_0x71d9[115]]= function(_0x49fcxb){for(var _0x49fcx16 in _0x49fcx1a){if(Object[_0x71d9[99]][_0x71d9[98]][_0x71d9[97]](_0x49fcx1a,_0x49fcx16)&& _0x71d9[88]!== _0x49fcx16&& _0x71d9[103]!== _0x49fcx16&& _0x49fcxb[_0x71d9[109]](_0x49fcx16)!== _0x49fcx1a[_0x49fcx16]){return !1}};return !0};_0x49fcx1b[_0x71d9[127]]= function(){var _0x49fcxb={};_0x49fcx16[_0x71d9[113]](_0x49fcx1a,function(_0x49fcx19,_0x49fcx1a,_0x49fcx5){var _0x49fcx2=!0;_0x49fcx16[_0x71d9[113]](_0x49fcx1b[_0x71d9[192]](),function(_0x49fcxb){_0x49fcxb=== _0x49fcx5&& (_0x49fcx2=  !1);return _0x49fcx2});_0x49fcx2&& (_0x49fcxb[_0x49fcx5]= _0x49fcx1b[_0x71d9[109]](_0x49fcx5))});return _0x49fcxb};_0x49fcx19()};_0x49fcx16[_0x71d9[187]][_0x71d9[193]]= _0x49fcx16[_0x71d9[187]][_0x71d9[99]]= {increment:function(_0x49fcxb){_0x49fcxb= parseInt(_0x49fcxb|| 1,10);this[_0x71d9[88]](this[_0x71d9[88]]()+ _0x49fcxb);return 1> this[_0x71d9[88]]()?(this[_0x71d9[93]](),null):this},decrement:function(_0x49fcxb){return this[_0x71d9[90]](-parseInt(_0x49fcxb|| 1,10))},remove:function(_0x49fcxb){if(!1=== _0x49fcx16[_0x71d9[101]](_0x71d9[194],[_0x49fcxf[this[_0x71d9[103]]()]])){return !1};delete _0x49fcxf[this[_0x71d9[103]]()];_0x49fcxb|| _0x49fcx16[_0x71d9[104]]();return null},reservedFields:function(){return _0x71d9[195][_0x71d9[122]](_0x71d9[173])},fields:function(){var _0x49fcxb={},_0x49fcx19=this;_0x49fcx16[_0x71d9[113]](_0x49fcx19[_0x71d9[192]](),function(_0x49fcx16){_0x49fcx19[_0x71d9[109]](_0x49fcx16)&& (_0x49fcxb[_0x49fcx16]= _0x49fcx19[_0x71d9[109]](_0x49fcx16))});return _0x49fcxb},quantity:function(_0x49fcxb){return _0x49fcx5(_0x49fcxb)?parseInt(this[_0x71d9[109]](_0x71d9[88],!0)|| 1,10):this[_0x71d9[191]](_0x71d9[88],_0x49fcxb)},price:function(_0x49fcxb){return _0x49fcx5(_0x49fcxb)?parseFloat(this[_0x71d9[109]](_0x71d9[84],!0).toString()[_0x71d9[108]](_0x49fcx16[_0x71d9[86]]()[_0x71d9[196]],_0x71d9[6])[_0x71d9[108]](_0x49fcx16[_0x71d9[86]]()[_0x71d9[189]],_0x71d9[6])|| 1):this[_0x71d9[191]](_0x71d9[84],parseFloat(_0x49fcxb.toString()[_0x71d9[108]](_0x49fcx16[_0x71d9[86]]()[_0x71d9[196]],_0x71d9[6])[_0x71d9[108]](_0x49fcx16[_0x71d9[86]]()[_0x71d9[189]],_0x71d9[6])))},id:function(){return this[_0x71d9[109]](_0x71d9[103],!1)},total:function(){return this[_0x71d9[88]]()* this[_0x71d9[84]]()}};_0x49fcx16[_0x71d9[8]]({checkout:function(){if(_0x71d9[197]=== _0x49fcx15[_0x71d9[199]][_0x71d9[198]][_0x71d9[164]]()&& _0x49fcx6(_0x49fcx15[_0x71d9[199]][_0x71d9[200]])){_0x49fcx15[_0x71d9[199]][_0x71d9[200]][_0x71d9[97]](_0x49fcx16,_0x49fcx15[_0x71d9[199]])}else {if(_0x49fcx6(_0x49fcx16[_0x71d9[199]][_0x49fcx15[_0x71d9[199]][_0x71d9[198]]])){var _0x49fcxb=_0x49fcx16[_0x71d9[199]][_0x49fcx15[_0x71d9[199]][_0x71d9[198]]][_0x71d9[97]](_0x49fcx16,_0x49fcx15[_0x71d9[199]]);_0x49fcxb[_0x71d9[201]]&& _0x49fcxb[_0x71d9[202]]&& _0x49fcxb[_0x71d9[203]]&& !1!== _0x49fcx16[_0x71d9[101]](_0x71d9[204],[_0x49fcxb[_0x71d9[201]]])&& _0x49fcx16[_0x71d9[205]](_0x49fcxb)}else {_0x49fcx16[_0x71d9[136]](_0x71d9[206])}}},extendCheckout:function(_0x49fcxb){return _0x49fcx16[_0x71d9[8]](_0x49fcx16[_0x71d9[199]],_0x49fcxb)},generateAndSendForm:function(_0x49fcxb){var _0x49fcx19=_0x49fcx16.$create(_0x71d9[207]);_0x49fcx19[_0x71d9[7]](_0x71d9[208],_0x71d9[209]);_0x49fcx19[_0x71d9[7]](_0x71d9[202],_0x49fcxb[_0x71d9[202]]);_0x49fcx19[_0x71d9[7]](_0x71d9[203],_0x49fcxb[_0x71d9[203]]);_0x49fcx16[_0x71d9[113]](_0x49fcxb[_0x71d9[201]],function(_0x49fcxb,_0x49fcx1b,_0x49fcx5){_0x49fcx19[_0x71d9[172]](_0x49fcx16.$create(_0x71d9[212])[_0x71d9[7]](_0x71d9[198],_0x71d9[211])[_0x71d9[7]](_0x71d9[82],_0x49fcx5)[_0x71d9[210]](_0x49fcxb))});_0x49fcx16.$(_0x71d9[213])[_0x71d9[172]](_0x49fcx19);_0x49fcx19[_0x71d9[215]][_0x71d9[214]]();_0x49fcx19[_0x71d9[93]]()}});_0x49fcx16[_0x71d9[281]]({PayPal:function(_0x49fcxb){if(!_0x49fcxb[_0x71d9[216]]){return _0x49fcx16[_0x71d9[136]](_0x71d9[217])};var _0x49fcx19={cmd:_0x71d9[218],upload:_0x71d9[219],currency_code:_0x49fcx16[_0x71d9[86]]()[_0x71d9[220]],business:_0x49fcxb[_0x71d9[216]],rm:_0x71d9[221]=== _0x49fcxb[_0x71d9[203]]?_0x71d9[222]:_0x71d9[223],tax_cart:(1* _0x49fcx16[_0x71d9[116]]())[_0x71d9[224]](2),handling_cart:(1* _0x49fcx16[_0x71d9[117]]())[_0x71d9[224]](2),charset:_0x71d9[225]},_0x49fcx1a=_0x49fcxb[_0x71d9[226]]?_0x71d9[227]:_0x71d9[228],_0x49fcx1b=_0x71d9[221]=== _0x49fcxb[_0x71d9[203]]?_0x71d9[221]:_0x71d9[229];_0x49fcxb[_0x71d9[230]]&& (_0x49fcx19[_0x71d9[231]]= _0x49fcxb[_0x71d9[230]]);_0x49fcxb[_0x71d9[232]]&& (_0x49fcx19[_0x71d9[233]]= _0x49fcxb[_0x71d9[232]]);_0x49fcxb[_0x71d9[234]]&& (_0x49fcx19[_0x71d9[235]]= _0x49fcxb[_0x71d9[234]]);_0x49fcx16[_0x71d9[113]](function(_0x49fcxb,_0x49fcx1a){var _0x49fcx1b=_0x49fcx1a+ 1,_0x49fcx5=_0x49fcxb[_0x71d9[127]](),_0x49fcx2=0,_0x49fcx6;_0x49fcx19[_0x71d9[236]+ _0x49fcx1b]= _0x49fcxb[_0x71d9[109]](_0x71d9[82]);_0x49fcx19[_0x71d9[237]+ _0x49fcx1b]= _0x49fcxb[_0x71d9[88]]();_0x49fcx19[_0x71d9[238]+ _0x49fcx1b]= (1* _0x49fcxb[_0x71d9[84]]())[_0x71d9[224]](2);_0x49fcx19[_0x71d9[239]+ _0x49fcx1b]= _0x49fcxb[_0x71d9[109]](_0x71d9[240])|| _0x49fcx1b;_0x49fcx16[_0x71d9[113]](_0x49fcx5,function(_0x49fcxb,_0x49fcx1a,_0x49fcx5){10> _0x49fcx1a&& (_0x49fcx6=  !0,_0x49fcx16[_0x71d9[113]](_0x49fcx15[_0x71d9[241]],function(_0x49fcxb){_0x49fcxb=== _0x49fcx5&& (_0x49fcx6=  !1)}),_0x49fcx6&& (_0x49fcx2+= 1,_0x49fcx19[_0x71d9[242]+ _0x49fcx1a+ _0x71d9[193]+ _0x49fcx1b]= _0x49fcx5,_0x49fcx19[_0x71d9[243]+ _0x49fcx1a+ _0x71d9[193]+ _0x49fcx1b]= _0x49fcxb))});_0x49fcx19[_0x71d9[244]+ _0x49fcx1a]= Math[_0x71d9[245]](10,_0x49fcx2)});return {action:_0x49fcx1a,method:_0x49fcx1b,data:_0x49fcx19}},GoogleCheckout:function(_0x49fcxb){if(!_0x49fcxb[_0x71d9[246]]){return _0x49fcx16[_0x71d9[136]](_0x71d9[247])};if(_0x71d9[21]!== _0x49fcx16[_0x71d9[86]]()[_0x71d9[220]]&& _0x71d9[61]!== _0x49fcx16[_0x71d9[86]]()[_0x71d9[220]]){return _0x49fcx16[_0x71d9[136]](_0x71d9[248])};var _0x49fcx19={ship_method_name_1:_0x71d9[249],ship_method_price_1:_0x49fcx16[_0x71d9[117]](),ship_method_currency_1:_0x49fcx16[_0x71d9[86]]()[_0x71d9[220]],_charset_:_0x71d9[6]},_0x49fcx1a=_0x71d9[250]+ _0x49fcxb[_0x71d9[246]];_0x49fcxb= _0x71d9[221]=== _0x49fcxb[_0x71d9[203]]?_0x71d9[221]:_0x71d9[229];_0x49fcx16[_0x71d9[113]](function(_0x49fcxb,_0x49fcx1a){var _0x49fcx5=_0x49fcx1a+ 1,_0x49fcx2=[],_0x49fcx6;_0x49fcx19[_0x71d9[236]+ _0x49fcx5]= _0x49fcxb[_0x71d9[109]](_0x71d9[82]);_0x49fcx19[_0x71d9[251]+ _0x49fcx5]= _0x49fcxb[_0x71d9[88]]();_0x49fcx19[_0x71d9[252]+ _0x49fcx5]= _0x49fcxb[_0x71d9[84]]();_0x49fcx19[_0x71d9[253]+ _0x49fcx5]= _0x49fcx16[_0x71d9[86]]()[_0x71d9[220]];_0x49fcx19[_0x71d9[254]+ _0x49fcx5]= _0x49fcxb[_0x71d9[109]](_0x71d9[142])|| _0x49fcx16[_0x71d9[142]]();_0x49fcx16[_0x71d9[113]](_0x49fcxb[_0x71d9[127]](),function(_0x49fcxb,_0x49fcx19,_0x49fcx1a){_0x49fcx6=  !0;_0x49fcx16[_0x71d9[113]](_0x49fcx15[_0x71d9[241]],function(_0x49fcxb){_0x49fcxb=== _0x49fcx1a&& (_0x49fcx6=  !1)});_0x49fcx6&& _0x49fcx2[_0x71d9[19]](_0x49fcx1a+ _0x71d9[255]+ _0x49fcxb)});_0x49fcx19[_0x71d9[256]+ _0x49fcx5]= _0x49fcx2[_0x71d9[258]](_0x71d9[257])});return {action:_0x49fcx1a,method:_0x49fcxb,data:_0x49fcx19}},AmazonPayments:function(_0x49fcxb){if(!_0x49fcxb[_0x71d9[259]]){return _0x49fcx16[_0x71d9[136]](_0x71d9[260])};if(!_0x49fcxb[_0x71d9[261]]){return _0x49fcx16[_0x71d9[136]](_0x71d9[262])};if(!_0x49fcxb[_0x71d9[263]]){return _0x49fcx16[_0x71d9[136]](_0x71d9[264])};var _0x49fcx19={aws_access_key_id:_0x49fcxb[_0x71d9[263]],merchant_signature:_0x49fcxb[_0x71d9[259]],currency_code:_0x49fcx16[_0x71d9[86]]()[_0x71d9[220]],tax_rate:_0x49fcx16[_0x71d9[142]](),weight_unit:_0x49fcxb[_0x71d9[265]]|| _0x71d9[266]},_0x49fcx1a=_0x71d9[267]+ (_0x49fcxb[_0x71d9[226]]?_0x71d9[268]:_0x71d9[6])+ _0x71d9[269]+ _0x49fcxb[_0x71d9[261]],_0x49fcx1b=_0x71d9[221]=== _0x49fcxb[_0x71d9[203]]?_0x71d9[221]:_0x71d9[229];_0x49fcx16[_0x71d9[113]](function(_0x49fcx1a,_0x49fcx1b){var _0x49fcx5=_0x49fcx1b+ 1,_0x49fcx2=[];_0x49fcx19[_0x71d9[270]+ _0x49fcx5]= _0x49fcx1a[_0x71d9[109]](_0x71d9[82]);_0x49fcx19[_0x71d9[251]+ _0x49fcx5]= _0x49fcx1a[_0x71d9[88]]();_0x49fcx19[_0x71d9[252]+ _0x49fcx5]= _0x49fcx1a[_0x71d9[84]]();_0x49fcx19[_0x71d9[271]+ _0x49fcx5]= _0x49fcx1a[_0x71d9[109]](_0x71d9[272])|| _0x49fcx1a[_0x71d9[103]]();_0x49fcx19[_0x71d9[273]+ _0x49fcx5]= _0x49fcxb[_0x71d9[261]];_0x49fcx1a[_0x71d9[109]](_0x71d9[274])&& (_0x49fcx19[_0x71d9[275]+ _0x49fcx5]= _0x49fcx1a[_0x71d9[109]](_0x71d9[274]));_0x49fcx15[_0x71d9[143]]&& (_0x49fcx19[_0x71d9[276]+ _0x49fcx5]= _0x49fcx15[_0x71d9[143]]);_0x49fcx16[_0x71d9[113]](_0x49fcx1a[_0x71d9[127]](),function(_0x49fcxb,_0x49fcx19,_0x49fcx1a){var _0x49fcx1b=!0;_0x49fcx16[_0x71d9[113]](_0x49fcx15[_0x71d9[241]],function(_0x49fcxb){_0x49fcxb=== _0x49fcx1a&& (_0x49fcx1b=  !1)});_0x49fcx1b&& _0x71d9[274]!== _0x49fcx1a&& _0x71d9[116]!== _0x49fcx1a&& _0x49fcx2[_0x71d9[19]](_0x49fcx1a+ _0x71d9[255]+ _0x49fcxb)});_0x49fcx19[_0x71d9[256]+ _0x49fcx5]= _0x49fcx2[_0x71d9[258]](_0x71d9[257])});return {action:_0x49fcx1a,method:_0x49fcx1b,data:_0x49fcx19}},SendForm:function(_0x49fcxb){if(!_0x49fcxb[_0x71d9[277]]){return _0x49fcx16[_0x71d9[136]](_0x71d9[278])};var _0x49fcx19={currency:_0x49fcx16[_0x71d9[86]]()[_0x71d9[220]],shipping:_0x49fcx16[_0x71d9[117]](),tax:_0x49fcx16[_0x71d9[116]](),taxRate:_0x49fcx16[_0x71d9[142]](),itemCount:_0x49fcx16[_0x71d9[114]]({})[_0x71d9[175]]},_0x49fcx1a=_0x49fcxb[_0x71d9[277]],_0x49fcx1b=_0x71d9[221]=== _0x49fcxb[_0x71d9[203]]?_0x71d9[221]:_0x71d9[229];_0x49fcx16[_0x71d9[113]](function(_0x49fcxb,_0x49fcx1a){var _0x49fcx1b=_0x49fcx1a+ 1,_0x49fcx5=[],_0x49fcx2;_0x49fcx19[_0x71d9[236]+ _0x49fcx1b]= _0x49fcxb[_0x71d9[109]](_0x71d9[82]);_0x49fcx19[_0x71d9[251]+ _0x49fcx1b]= _0x49fcxb[_0x71d9[88]]();_0x49fcx19[_0x71d9[252]+ _0x49fcx1b]= _0x49fcxb[_0x71d9[84]]();_0x49fcx16[_0x71d9[113]](_0x49fcxb[_0x71d9[127]](),function(_0x49fcxb,_0x49fcx19,_0x49fcx1a){_0x49fcx2=  !0;_0x49fcx16[_0x71d9[113]](_0x49fcx15[_0x71d9[241]],function(_0x49fcxb){_0x49fcxb=== _0x49fcx1a&& (_0x49fcx2=  !1)});_0x49fcx2&& _0x49fcx5[_0x71d9[19]](_0x49fcx1a+ _0x71d9[255]+ _0x49fcxb)});_0x49fcx19[_0x71d9[279]+ _0x49fcx1b]= _0x49fcx5[_0x71d9[258]](_0x71d9[257])});_0x49fcxb[_0x71d9[230]]&& (_0x49fcx19[_0x71d9[231]]= _0x49fcxb[_0x71d9[230]]);_0x49fcxb[_0x71d9[232]]&& (_0x49fcx19[_0x71d9[233]]= _0x49fcxb[_0x71d9[232]]);_0x49fcxb[_0x71d9[280]]&& (_0x49fcx19= _0x49fcx16[_0x71d9[8]](_0x49fcx19,_0x49fcxb[_0x71d9[280]]));return {action:_0x49fcx1a,method:_0x49fcx1b,data:_0x49fcx19}}});_0x49fcx9= {bind:function(_0x49fcxb,_0x49fcx19){if(!_0x49fcx6(_0x49fcx19)){return this};this[_0x71d9[282]]|| (this[_0x71d9[282]]= {});var _0x49fcx1a=_0x49fcxb[_0x71d9[122]](/ +/);_0x49fcx16[_0x71d9[113]](_0x49fcx1a,function(_0x49fcxb){!0=== this[_0x71d9[282]][_0x49fcxb]?_0x49fcx19[_0x71d9[283]](this):_0x49fcx5(this[_0x71d9[282]][_0x49fcxb])?this[_0x71d9[282]][_0x49fcxb]= [_0x49fcx19]:this[_0x71d9[282]][_0x49fcxb][_0x71d9[19]](_0x49fcx19)});return this},trigger:function(_0x49fcxb,_0x49fcx16){var _0x49fcx1a=!0,_0x49fcx1b,_0x49fcx2;this[_0x71d9[282]]|| (this[_0x71d9[282]]= {});if(!_0x49fcx5(this[_0x71d9[282]][_0x49fcxb])&& _0x49fcx6(this[_0x71d9[282]][_0x49fcxb][0])){for(_0x49fcx1b= 0,_0x49fcx2= this[_0x71d9[282]][_0x49fcxb][_0x71d9[175]];_0x49fcx1b< _0x49fcx2;_0x49fcx1b+= 1){_0x49fcx1a= this[_0x71d9[282]][_0x49fcxb][_0x49fcx1b][_0x71d9[283]](this,_0x49fcx16|| [])}};return !1=== _0x49fcx1a?!1:!0}};_0x49fcx9[_0x71d9[242]]= _0x49fcx9[_0x71d9[137]];_0x49fcx16[_0x71d9[8]](_0x49fcx9);_0x49fcx16[_0x71d9[8]](_0x49fcx16[_0x71d9[187]]._,_0x49fcx9);_0x49fcx9= {beforeAdd:null,afterAdd:null,load:null,beforeSave:null,afterSave:null,update:null,ready:null,checkoutSuccess:null,checkoutFail:null,beforeCheckout:null,beforeRemove:null};_0x49fcx16(_0x49fcx9);_0x49fcx16[_0x71d9[113]](_0x49fcx9,function(_0x49fcxb,_0x49fcx19,_0x49fcx1a){_0x49fcx16[_0x71d9[137]](_0x49fcx1a,function(){_0x49fcx6(_0x49fcx15[_0x49fcx1a])&& _0x49fcx15[_0x49fcx1a][_0x71d9[283]](this,arguments)})});_0x49fcx16[_0x71d9[8]]({toCurrency:function(_0x49fcxb,_0x49fcx19){var _0x49fcx1a=parseFloat(_0x49fcxb),_0x49fcx1b=_0x49fcx19|| {},_0x49fcx1b=_0x49fcx16[_0x71d9[8]](_0x49fcx16[_0x71d9[8]]({symbol:_0x71d9[284],decimal:_0x71d9[121],delimiter:_0x71d9[285],accuracy:2,after:!1},_0x49fcx16[_0x71d9[86]]()),_0x49fcx1b),_0x49fcx5=_0x49fcx1a[_0x71d9[224]](_0x49fcx1b[_0x71d9[286]])[_0x71d9[122]](_0x71d9[121]),_0x49fcx1a=_0x49fcx5[1],_0x49fcx5=_0x49fcx5[0],_0x49fcx5=_0x49fcx16[_0x71d9[288]](_0x49fcx5[_0x71d9[287]](),3)[_0x71d9[258]](_0x49fcx1b[_0x71d9[189]][_0x71d9[287]]())[_0x71d9[287]]();return (_0x49fcx1b[_0x71d9[289]]?_0x71d9[6]:_0x49fcx1b[_0x71d9[196]])+ _0x49fcx5+ (_0x49fcx1a?_0x49fcx1b[_0x71d9[188]]+ _0x49fcx1a:_0x71d9[6])+ (_0x49fcx1b[_0x71d9[289]]?_0x49fcx1b[_0x71d9[196]]:_0x71d9[6])},chunk:function(_0x49fcxb,_0x49fcx16){_0x71d9[1]===  typeof _0x49fcx16&& (_0x49fcx16= 2);return _0x49fcxb[_0x71d9[106]](RegExp(_0x71d9[290]+ _0x49fcx16+ _0x71d9[291],_0x71d9[292]))|| []}});String[_0x71d9[99]][_0x71d9[287]]= function(){return this[_0x71d9[122]](_0x71d9[6])[_0x71d9[287]]()[_0x71d9[258]](_0x71d9[6])};_0x49fcx16[_0x71d9[8]]({currency:function(_0x49fcxb){if(_0x49fcx4(_0x49fcxb,_0x49fcx3)&&  !_0x49fcx5(_0x49fcx14[_0x49fcxb])){_0x49fcx15[_0x71d9[86]]= _0x49fcxb}else {if(_0x49fcx4(_0x49fcxb,_0x71d9[3])){_0x49fcx14[_0x49fcxb[_0x71d9[220]]]= _0x49fcxb,_0x49fcx15[_0x71d9[86]]= _0x49fcxb[_0x71d9[220]]}else {return _0x49fcx14[_0x49fcx15[_0x71d9[86]]]}}}});_0x49fcx16[_0x71d9[8]]({bindOutlets:function(_0x49fcxb){_0x49fcx16[_0x71d9[113]](_0x49fcxb,function(_0x49fcxb,_0x49fcx1a,_0x49fcx5){_0x49fcx16[_0x71d9[137]](_0x71d9[104],function(){_0x49fcx16[_0x71d9[293]](_0x71d9[121]+ _0x49fcx10+ _0x71d9[193]+ _0x49fcx5,_0x49fcxb)})})},setOutlet:function(_0x49fcxb,_0x49fcx19){var _0x49fcx1a=_0x49fcx19[_0x71d9[97]](_0x49fcx16,_0x49fcxb);_0x49fcx4(_0x49fcx1a,_0x71d9[3])&& _0x49fcx1a[_0x71d9[215]]?_0x49fcx16.$(_0x49fcxb)[_0x71d9[174]](_0x71d9[173])[_0x71d9[172]](_0x49fcx1a):_0x49fcx5(_0x49fcx1a)|| _0x49fcx16.$(_0x49fcxb)[_0x71d9[174]](_0x49fcx1a)},bindInputs:function(_0x49fcxb){_0x49fcx16[_0x71d9[113]](_0x49fcxb,function(_0x49fcxb){_0x49fcx16[_0x71d9[297]](_0x71d9[121]+ _0x49fcx10+ _0x71d9[193]+ _0x49fcxb[_0x71d9[294]],_0x49fcxb[_0x71d9[295]],_0x49fcxb[_0x71d9[296]])})},setInput:function(_0x49fcxb,_0x49fcx19,_0x49fcx1a){_0x49fcx16.$(_0x49fcxb)[_0x71d9[298]](_0x49fcx19,_0x49fcx1a)}});_0x49fcx16[_0x71d9[124]]= function(_0x49fcxb){this[_0x71d9[299]](_0x49fcxb);this[_0x71d9[294]]= _0x49fcxb|| null};_0x49fcx16[_0x71d9[8]](_0x49fcx11,{MooTools:{text:function(_0x49fcxb){return this[_0x71d9[7]](_0x71d9[150],_0x49fcxb)},html:function(_0x49fcxb){return this[_0x71d9[7]](_0x71d9[174],_0x49fcxb)},val:function(_0x49fcxb){return this[_0x71d9[7]](_0x71d9[300],_0x49fcxb)},attr:function(_0x49fcxb,_0x49fcx16){if(_0x49fcx5(_0x49fcx16)){return this[_0x71d9[215]][0]&& this[_0x71d9[215]][0][_0x71d9[109]](_0x49fcxb)};this[_0x71d9[215]][_0x71d9[191]](_0x49fcxb,_0x49fcx16);return this},remove:function(){this[_0x71d9[215]][_0x71d9[301]]();return null},addClass:function(_0x49fcxb){this[_0x71d9[215]][_0x71d9[171]](_0x49fcxb);return this},removeClass:function(_0x49fcxb){this[_0x71d9[215]][_0x71d9[302]](_0x49fcxb);return this},append:function(_0x49fcxb){this[_0x71d9[215]][_0x71d9[303]](_0x49fcxb[_0x71d9[215]]);return this},each:function(_0x49fcxb){_0x49fcx6(_0x49fcxb)&& _0x49fcx16[_0x71d9[113]](this[_0x71d9[215]],function(_0x49fcx16,_0x49fcx1a,_0x49fcx5){_0x49fcxb[_0x71d9[97]](_0x49fcx1a,_0x49fcx1a,_0x49fcx16,_0x49fcx5)});return this},click:function(_0x49fcxb){_0x49fcx6(_0x49fcxb)?this[_0x71d9[113]](function(_0x49fcx16){_0x49fcx16[_0x71d9[305]](_0x71d9[304],function(_0x49fcx1a){_0x49fcxb[_0x71d9[97]](_0x49fcx16,_0x49fcx1a)})}):_0x49fcx5(_0x49fcxb)&& this[_0x71d9[215]][_0x71d9[306]](_0x71d9[304]);return this},live:function(_0x49fcxb,_0x49fcx19){var _0x49fcx1a=this[_0x71d9[294]];_0x49fcx6(_0x49fcx19)&& _0x49fcx16.$(_0x71d9[213])[_0x71d9[215]][_0x71d9[305]](_0x49fcxb+ _0x71d9[307]+ _0x49fcx1a+ _0x71d9[308],function(_0x49fcxb,_0x49fcx16){_0x49fcx19[_0x71d9[97]](_0x49fcx16,_0x49fcxb)})},match:function(_0x49fcxb){return this[_0x71d9[215]][_0x71d9[106]](_0x49fcxb)},parent:function(){return _0x49fcx16.$(this[_0x71d9[215]][_0x71d9[309]]())},find:function(_0x49fcxb){return _0x49fcx16.$(this[_0x71d9[215]][_0x71d9[310]](_0x49fcxb))},closest:function(_0x49fcxb){return _0x49fcx16.$(this[_0x71d9[215]][_0x71d9[309]](_0x49fcxb))},descendants:function(){return this[_0x71d9[114]](_0x71d9[15])},tag:function(){return this[_0x71d9[215]][0][_0x71d9[311]]},submit:function(){this[_0x71d9[215]][0][_0x71d9[214]]();return this},create:function(_0x49fcxb){this[_0x71d9[215]]= _0x49fcx17(_0x49fcxb)}},Prototype:{text:function(_0x49fcxb){if(_0x49fcx5(_0x49fcxb)){return this[_0x71d9[215]][0][_0x71d9[312]]};this[_0x71d9[113]](function(_0x49fcx16,_0x49fcx1a){$(_0x49fcx1a)[_0x71d9[104]](_0x49fcxb)});return this},html:function(_0x49fcxb){return this[_0x71d9[150]](_0x49fcxb)},val:function(_0x49fcxb){return this[_0x71d9[7]](_0x71d9[300],_0x49fcxb)},attr:function(_0x49fcxb,_0x49fcx16){if(_0x49fcx5(_0x49fcx16)){return this[_0x71d9[215]][0][_0x71d9[313]](_0x49fcxb)};this[_0x71d9[113]](function(_0x49fcx1a,_0x49fcx5){$(_0x49fcx5)[_0x71d9[314]](_0x49fcxb,_0x49fcx16)});return this},append:function(_0x49fcxb){this[_0x71d9[113]](function(_0x49fcx16,_0x49fcx1a){_0x49fcxb[_0x71d9[215]]?_0x49fcxb[_0x71d9[113]](function(_0x49fcxb,_0x49fcx16){$(_0x49fcx1a)[_0x71d9[315]](_0x49fcx16)}):_0x49fcx7(_0x49fcxb)&& $(_0x49fcx1a)[_0x71d9[315]](_0x49fcxb)});return this},remove:function(){this[_0x71d9[113]](function(_0x49fcxb,_0x49fcx16){$(_0x49fcx16)[_0x71d9[93]]()});return this},addClass:function(_0x49fcxb){this[_0x71d9[113]](function(_0x49fcx16,_0x49fcx1a){$(_0x49fcx1a)[_0x71d9[316]](_0x49fcxb)});return this},removeClass:function(_0x49fcxb){this[_0x71d9[113]](function(_0x49fcx16,_0x49fcx1a){$(_0x49fcx1a)[_0x71d9[317]](_0x49fcxb)});return this},each:function(_0x49fcxb){_0x49fcx6(_0x49fcxb)&& _0x49fcx16[_0x71d9[113]](this[_0x71d9[215]],function(_0x49fcx16,_0x49fcx1a,_0x49fcx5){_0x49fcxb[_0x71d9[97]](_0x49fcx1a,_0x49fcx1a,_0x49fcx16,_0x49fcx5)});return this},click:function(_0x49fcxb){_0x49fcx6(_0x49fcxb)?this[_0x71d9[113]](function(_0x49fcx16,_0x49fcx1a){$(_0x49fcx1a)[_0x71d9[318]](_0x71d9[304],function(_0x49fcx16){_0x49fcxb[_0x71d9[97]](_0x49fcx1a,_0x49fcx16)})}):_0x49fcx5(_0x49fcxb)&& this[_0x71d9[113]](function(_0x49fcxb,_0x49fcx16){$(_0x49fcx16)[_0x71d9[319]](_0x71d9[304])});return this},live:function(_0x49fcxb,_0x49fcx16){if(_0x49fcx6(_0x49fcx16)){var _0x49fcx1a=this[_0x71d9[294]];_0x49fcx2[_0x71d9[318]](_0x49fcxb,function(_0x49fcxb,_0x49fcx5){_0x49fcx5=== _0x49fcx17(_0x49fcxb)[_0x71d9[320]](_0x49fcx1a)&& _0x49fcx16[_0x71d9[97]](_0x49fcx5,_0x49fcxb)})}},parent:function(){return _0x49fcx16.$(this[_0x71d9[215]][_0x71d9[321]]())},find:function(_0x49fcxb){return _0x49fcx16.$(this[_0x71d9[215]][_0x71d9[322]](_0x49fcxb))},closest:function(_0x49fcxb){return _0x49fcx16.$(this[_0x71d9[215]][_0x71d9[321]](_0x49fcxb))},descendants:function(){return _0x49fcx16.$(this[_0x71d9[215]][_0x71d9[323]]())},tag:function(){return this[_0x71d9[215]][_0x71d9[311]]},submit:function(){this[_0x71d9[215]][0][_0x71d9[214]]()},create:function(_0x49fcxb){_0x49fcx4(_0x49fcxb,_0x49fcx3)?this[_0x71d9[215]]= _0x49fcx17(_0x49fcxb):_0x49fcx7(_0x49fcxb)&& (this[_0x71d9[215]]= [_0x49fcxb])}},jQuery:{passthrough:function(_0x49fcxb,_0x49fcx16){if(_0x49fcx5(_0x49fcx16)){return this[_0x71d9[215]][_0x49fcxb]()};this[_0x71d9[215]][_0x49fcxb](_0x49fcx16);return this},text:function(_0x49fcxb){return this[_0x71d9[324]](_0x71d9[150],_0x49fcxb)},html:function(_0x49fcxb){return this[_0x71d9[324]](_0x71d9[174],_0x49fcxb)},val:function(_0x49fcxb){return this[_0x71d9[324]](_0x71d9[210],_0x49fcxb)},append:function(_0x49fcxb){this[_0x71d9[215]][_0x71d9[172]](_0x49fcxb[_0x71d9[215]]|| _0x49fcxb);return this},attr:function(_0x49fcxb,_0x49fcx16){if(_0x49fcx5(_0x49fcx16)){return this[_0x71d9[215]][_0x71d9[7]](_0x49fcxb)};this[_0x71d9[215]][_0x71d9[7]](_0x49fcxb,_0x49fcx16);return this},remove:function(){this[_0x71d9[215]][_0x71d9[93]]();return this},addClass:function(_0x49fcxb){this[_0x71d9[215]][_0x71d9[171]](_0x49fcxb);return this},removeClass:function(_0x49fcxb){this[_0x71d9[215]][_0x71d9[302]](_0x49fcxb);return this},each:function(_0x49fcxb){return this[_0x71d9[324]](_0x71d9[113],_0x49fcxb)},click:function(_0x49fcxb){return this[_0x71d9[324]](_0x71d9[304],_0x49fcxb)},live:function(_0x49fcxb,_0x49fcx16){_0x49fcx17(_0x49fcx2)[_0x71d9[325]](this[_0x71d9[294]],_0x49fcxb,_0x49fcx16);return this},parent:function(){return _0x49fcx16.$(this[_0x71d9[215]][_0x71d9[326]]())},find:function(_0x49fcxb){return _0x49fcx16.$(this[_0x71d9[215]][_0x71d9[114]](_0x49fcxb))},closest:function(_0x49fcxb){return _0x49fcx16.$(this[_0x71d9[215]][_0x71d9[327]](_0x49fcxb))},tag:function(){return this[_0x71d9[215]][0][_0x71d9[311]]},descendants:function(){return _0x49fcx16.$(this[_0x71d9[215]][_0x71d9[114]](_0x71d9[15]))},submit:function(){return this[_0x71d9[215]][_0x71d9[214]]()},create:function(_0x49fcxb){this[_0x71d9[215]]= _0x49fcx17(_0x49fcxb)}}});_0x49fcx16[_0x71d9[124]][_0x71d9[193]]= _0x49fcx16[_0x71d9[124]][_0x71d9[99]];_0x49fcx16[_0x71d9[96]](_0x49fcx16[_0x71d9[328]]);_0x49fcx16[_0x71d9[96]](function(){_0x49fcx16[_0x71d9[331]]({total:function(){return _0x49fcx16[_0x71d9[147]](_0x49fcx16[_0x71d9[91]]())},quantity:function(){return _0x49fcx16[_0x71d9[88]]()},items:function(_0x49fcxb){_0x49fcx16[_0x71d9[329]](_0x49fcxb)},tax:function(){return _0x49fcx16[_0x71d9[147]](_0x49fcx16[_0x71d9[116]]())},taxRate:function(){return _0x49fcx16[_0x71d9[142]]()[_0x71d9[224]]()},shipping:function(){return _0x49fcx16[_0x71d9[147]](_0x49fcx16[_0x71d9[117]]())},grandTotal:function(){return _0x49fcx16[_0x71d9[147]](_0x49fcx16[_0x71d9[330]]())}});_0x49fcx16[_0x71d9[347]]([{selector:_0x71d9[199],event:_0x71d9[304],callback:function(){_0x49fcx16[_0x71d9[199]]()}},{selector:_0x71d9[332],event:_0x71d9[304],callback:function(){_0x49fcx16[_0x71d9[332]]()}},{selector:_0x71d9[90],event:_0x71d9[304],callback:function(){_0x49fcx16[_0x71d9[114]](_0x49fcx16.$(this)[_0x71d9[327]](_0x71d9[333])[_0x71d9[7]](_0x71d9[103])[_0x71d9[122]](_0x71d9[193])[1])[_0x71d9[90]]();_0x49fcx16[_0x71d9[104]]()}},{selector:_0x71d9[87],event:_0x71d9[304],callback:function(){_0x49fcx16[_0x71d9[114]](_0x49fcx16.$(this)[_0x71d9[327]](_0x71d9[333])[_0x71d9[7]](_0x71d9[103])[_0x71d9[122]](_0x71d9[193])[1])[_0x71d9[87]]();_0x49fcx16[_0x71d9[104]]()}},{selector:_0x71d9[93],event:_0x71d9[304],callback:function(){_0x49fcx16[_0x71d9[114]](_0x49fcx16.$(this)[_0x71d9[327]](_0x71d9[333])[_0x71d9[7]](_0x71d9[103])[_0x71d9[122]](_0x71d9[193])[1])[_0x71d9[93]]()}},{selector:_0x71d9[212],event:_0x71d9[334],callback:function(){var _0x49fcxb=_0x49fcx16.$(this),_0x49fcx19=_0x49fcxb[_0x71d9[326]](),_0x49fcx1a=_0x49fcx19[_0x71d9[7]](_0x71d9[335])[_0x71d9[122]](_0x71d9[173]);_0x49fcx16[_0x71d9[113]](_0x49fcx1a,function(_0x49fcx1a){_0x49fcx1a[_0x71d9[106]](/item-.+/i)&& (_0x49fcx1a= _0x49fcx1a[_0x71d9[122]](_0x71d9[154])[1],_0x49fcx16[_0x71d9[114]](_0x49fcx19[_0x71d9[327]](_0x71d9[333])[_0x71d9[7]](_0x71d9[103])[_0x71d9[122]](_0x71d9[193])[1])[_0x71d9[191]](_0x49fcx1a,_0x49fcxb[_0x71d9[210]]()),_0x49fcx16[_0x71d9[104]]())})}},{selector:_0x71d9[336],event:_0x71d9[304],callback:function(){var _0x49fcxb={};_0x49fcx16.$(this)[_0x71d9[327]](_0x71d9[121]+ _0x49fcx10+ _0x71d9[346])[_0x71d9[323]]()[_0x71d9[113]](function(_0x49fcx19,_0x49fcx1a){var _0x49fcx5=_0x49fcx16.$(_0x49fcx1a);_0x49fcx5[_0x71d9[7]](_0x71d9[335])&& _0x49fcx5[_0x71d9[7]](_0x71d9[335])[_0x71d9[106]](/item_.+/)&&  !_0x49fcx5[_0x71d9[7]](_0x71d9[335])[_0x71d9[106]](/item_add/)&& _0x49fcx16[_0x71d9[113]](_0x49fcx5[_0x71d9[7]](_0x71d9[335])[_0x71d9[122]](_0x71d9[173]),function(_0x49fcx16){var _0x49fcx1a,_0x49fcx19;if(_0x49fcx16[_0x71d9[106]](/item_.+/)){_0x49fcx16= _0x49fcx16[_0x71d9[122]](_0x71d9[193])[1];_0x49fcx1a= _0x71d9[6];switch(_0x49fcx5[_0x71d9[345]]()[_0x71d9[164]]()){case _0x71d9[212]:;case _0x71d9[337]:;case _0x71d9[342]:_0x49fcx19= _0x49fcx5[_0x71d9[7]](_0x71d9[198]);if(!_0x49fcx19|| (_0x71d9[338]=== _0x49fcx19[_0x71d9[164]]()|| _0x71d9[339]=== _0x49fcx19[_0x71d9[164]]())&& _0x49fcx5[_0x71d9[7]](_0x71d9[340]) || _0x71d9[150]=== _0x49fcx19[_0x71d9[164]]() || _0x71d9[341]=== _0x49fcx19[_0x71d9[164]]()){_0x49fcx1a= _0x49fcx5[_0x71d9[210]]()};break;case _0x71d9[344]:_0x49fcx1a= _0x49fcx5[_0x71d9[7]](_0x71d9[343]);break;default:_0x49fcx1a= _0x49fcx5[_0x71d9[150]]()};null!== _0x49fcx1a&& _0x71d9[6]!== _0x49fcx1a&& (_0x49fcxb[_0x49fcx16[_0x71d9[164]]()]= _0x49fcxb[_0x49fcx16[_0x71d9[164]]()]?_0x49fcxb[_0x49fcx16[_0x71d9[164]]()]+ _0x71d9[257]+ _0x49fcx1a:_0x49fcx1a)}})});_0x49fcx16[_0x71d9[134]](_0x49fcxb)}}])});_0x49fcx2[_0x71d9[348]]?_0x49fcx1[_0x71d9[349]]= function(){_0x49fcx2[_0x71d9[350]](_0x71d9[349],DOMContentLoaded,!1);_0x49fcx16[_0x71d9[13]]()}:_0x49fcx2[_0x71d9[351]]&& (_0x49fcx1[_0x71d9[349]]= function(){_0x71d9[352]=== _0x49fcx2[_0x71d9[353]]&& (_0x49fcx2[_0x71d9[355]](_0x71d9[354],DOMContentLoaded),_0x49fcx16[_0x71d9[13]]())});(function(){if(_0x71d9[352]=== _0x49fcx2[_0x71d9[353]]){return setTimeout(_0x49fcx16[_0x71d9[13]],1)};if(_0x49fcx2[_0x71d9[348]]){_0x49fcx2[_0x71d9[348]](_0x71d9[349],DOMContentLoaded,!1),_0x49fcx1[_0x71d9[348]](_0x71d9[119],_0x49fcx16[_0x71d9[13]],!1)}else {if(_0x49fcx2[_0x71d9[351]]){_0x49fcx2[_0x71d9[351]](_0x71d9[354],DOMContentLoaded);_0x49fcx1[_0x71d9[351]](_0x71d9[356],_0x49fcx16[_0x71d9[13]]);var _0x49fcxb=!1;try{_0x49fcxb= null=== _0x49fcx1[_0x71d9[357]]}catch(d){};_0x49fcx2[_0x71d9[12]][_0x71d9[11]]&& _0x49fcxb&& _0x49fcxc()}}})();return _0x49fcx16};_0x49fcx1[_0x71d9[16]]= _0x49fcx8()})(window,document);var JSON;JSON|| (JSON= {});(function(){function _0x49fcx1(_0x49fcx5){return 10> _0x49fcx5?_0x71d9[222]+ _0x49fcx5:_0x49fcx5}function _0x49fcx2(_0x49fcx2){_0x49fcx5[_0x71d9[358]]= 0;return _0x49fcx5[_0x71d9[359]](_0x49fcx2)?_0x71d9[360]+ _0x49fcx2[_0x71d9[108]](_0x49fcx5,function(_0x49fcx5){var _0x49fcx2=_0x49fcx8[_0x49fcx5];return _0x71d9[0]===  typeof _0x49fcx2?_0x49fcx2:_0x71d9[361]+ (_0x71d9[363]+ _0x49fcx5[_0x71d9[364]](0).toString(16))[_0x71d9[362]](-4)})+ _0x71d9[360]:_0x71d9[360]+ _0x49fcx2+ _0x71d9[360]}function _0x49fcx3(_0x49fcx5,_0x49fcx4){var _0x49fcxd,_0x49fcxe,_0x49fcxf,_0x49fcx1,_0x49fcx11=_0x49fcx6,_0x49fcx12,_0x49fcx13=_0x49fcx4[_0x49fcx5];_0x49fcx13&& _0x71d9[3]===  typeof _0x49fcx13&& _0x71d9[2]===  typeof _0x49fcx13[_0x71d9[365]]&& (_0x49fcx13= _0x49fcx13[_0x71d9[365]](_0x49fcx5));_0x71d9[2]===  typeof _0x49fcx9&& (_0x49fcx13= _0x49fcx9[_0x71d9[97]](_0x49fcx4,_0x49fcx5,_0x49fcx13));switch( typeof _0x49fcx13){case _0x71d9[0]:return _0x49fcx2(_0x49fcx13);case _0x71d9[341]:return isFinite(_0x49fcx13)?String(_0x49fcx13):_0x71d9[366];case _0x71d9[367]:;case _0x71d9[366]:return String(_0x49fcx13);case _0x71d9[3]:if(!_0x49fcx13){return _0x71d9[366]};_0x49fcx6+= _0x49fcx7;_0x49fcx12= [];if(_0x71d9[368]=== Object[_0x71d9[99]][_0x71d9[369]][_0x71d9[283]](_0x49fcx13)){_0x49fcx1= _0x49fcx13[_0x71d9[175]];for(_0x49fcxd= 0;_0x49fcxd< _0x49fcx1;_0x49fcxd+= 1){_0x49fcx12[_0x49fcxd]= _0x49fcx3(_0x49fcxd,_0x49fcx13)|| _0x71d9[366]};_0x49fcxf= 0=== _0x49fcx12[_0x71d9[175]]?_0x71d9[370]:_0x49fcx6?_0x71d9[371]+ _0x49fcx6+ _0x49fcx12[_0x71d9[258]](_0x71d9[372]+ _0x49fcx6)+ _0x71d9[373]+ _0x49fcx11+ _0x71d9[374]:_0x71d9[375]+ _0x49fcx12[_0x71d9[258]](_0x71d9[285])+ _0x71d9[374];_0x49fcx6= _0x49fcx11;return _0x49fcxf};if(_0x49fcx9&& _0x71d9[3]===  typeof _0x49fcx9){for(_0x49fcx1= _0x49fcx9[_0x71d9[175]],_0x49fcxd= 0;_0x49fcxd< _0x49fcx1;_0x49fcxd+= 1){_0x71d9[0]===  typeof _0x49fcx9[_0x49fcxd]&& (_0x49fcxe= _0x49fcx9[_0x49fcxd],(_0x49fcxf= _0x49fcx3(_0x49fcxe,_0x49fcx13))&& _0x49fcx12[_0x71d9[19]](_0x49fcx2(_0x49fcxe)+ (_0x49fcx6?_0x71d9[255]:_0x71d9[376])+ _0x49fcxf))}}else {for(_0x49fcxe in _0x49fcx13){Object[_0x71d9[99]][_0x71d9[98]][_0x71d9[97]](_0x49fcx13,_0x49fcxe)&& (_0x49fcxf= _0x49fcx3(_0x49fcxe,_0x49fcx13))&& _0x49fcx12[_0x71d9[19]](_0x49fcx2(_0x49fcxe)+ (_0x49fcx6?_0x71d9[255]:_0x71d9[376])+ _0x49fcxf)}};_0x49fcxf= 0=== _0x49fcx12[_0x71d9[175]]?_0x71d9[377]:_0x49fcx6?_0x71d9[378]+ _0x49fcx6+ _0x49fcx12[_0x71d9[258]](_0x71d9[372]+ _0x49fcx6)+ _0x71d9[373]+ _0x49fcx11+ _0x71d9[291]:_0x71d9[379]+ _0x49fcx12[_0x71d9[258]](_0x71d9[285])+ _0x71d9[291];_0x49fcx6= _0x49fcx11;return _0x49fcxf}}_0x71d9[2]!==  typeof Date[_0x71d9[99]][_0x71d9[365]]&& (Date[_0x71d9[99]][_0x71d9[365]]= function(){return isFinite(this.valueOf())?this[_0x71d9[380]]()+ _0x71d9[154]+ _0x49fcx1(this[_0x71d9[381]]()+ 1)+ _0x71d9[154]+ _0x49fcx1(this[_0x71d9[382]]())+ _0x71d9[383]+ _0x49fcx1(this[_0x71d9[384]]())+ _0x71d9[376]+ _0x49fcx1(this[_0x71d9[385]]())+ _0x71d9[376]+ _0x49fcx1(this[_0x71d9[386]]())+ _0x71d9[387]:null},String[_0x71d9[99]][_0x71d9[365]]= Number[_0x71d9[99]][_0x71d9[365]]= Boolean[_0x71d9[99]][_0x71d9[365]]= function(){return this.valueOf()});var _0x49fcx4=/[\u0000\u00ad\u0600-\u0604\u070f\u17b4\u17b5\u200c-\u200f\u2028-\u202f\u2060-\u206f\ufeff\ufff0-\uffff]/g,_0x49fcx5=/[\\\"\x00-\x1f\x7f-\x9f\u00ad\u0600-\u0604\u070f\u17b4\u17b5\u200c-\u200f\u2028-\u202f\u2060-\u206f\ufeff\ufff0-\uffff]/g,_0x49fcx6,_0x49fcx7,_0x49fcx8={"\x08":_0x71d9[388],"\x09":_0x71d9[389],"\x0A":_0x71d9[390],"\x0C":_0x71d9[391],"\x0D":_0x71d9[392],'\x22':_0x71d9[393],"\x5C":_0x71d9[394]},_0x49fcx9;_0x71d9[2]!==  typeof JSON[_0x71d9[129]]&& (JSON[_0x71d9[129]]= function(_0x49fcx5,_0x49fcx2,_0x49fcx4){var _0x49fcxe;_0x49fcx7= _0x49fcx6= _0x71d9[6];if(_0x71d9[341]===  typeof _0x49fcx4){for(_0x49fcxe= 0;_0x49fcxe< _0x49fcx4;_0x49fcxe+= 1){_0x49fcx7+= _0x71d9[173]}}else {_0x71d9[0]===  typeof _0x49fcx4&& (_0x49fcx7= _0x49fcx4)};if((_0x49fcx9= _0x49fcx2)&& _0x71d9[2]!==  typeof _0x49fcx2&& (_0x71d9[3]!==  typeof _0x49fcx2|| _0x71d9[341]!==  typeof _0x49fcx2[_0x71d9[175]])){throw Error(_0x71d9[395])};return _0x49fcx3(_0x71d9[6],{"":_0x49fcx5})});_0x71d9[2]!==  typeof JSON[_0x71d9[133]]&& (JSON[_0x71d9[133]]= function(_0x49fcx5,_0x49fcx2){function _0x49fcx6(_0x49fcx5,_0x49fcx4){var _0x49fcxe,_0x49fcx1,_0x49fcx13=_0x49fcx5[_0x49fcx4];if(_0x49fcx13&& _0x71d9[3]===  typeof _0x49fcx13){for(_0x49fcxe in _0x49fcx13){Object[_0x71d9[99]][_0x71d9[98]][_0x71d9[97]](_0x49fcx13,_0x49fcxe)&& (_0x49fcx1= _0x49fcx6(_0x49fcx13,_0x49fcxe),void(0)!== _0x49fcx1?_0x49fcx13[_0x49fcxe]= _0x49fcx1: delete _0x49fcx13[_0x49fcxe])}};return _0x49fcx2[_0x71d9[97]](_0x49fcx5,_0x49fcx4,_0x49fcx13)}var _0x49fcxe;_0x49fcx5= String(_0x49fcx5);_0x49fcx4[_0x71d9[358]]= 0;_0x49fcx4[_0x71d9[359]](_0x49fcx5)&& (_0x49fcx5= _0x49fcx5[_0x71d9[108]](_0x49fcx4,function(_0x49fcx5){return _0x71d9[361]+ (_0x71d9[363]+ _0x49fcx5[_0x71d9[364]](0).toString(16))[_0x71d9[362]](-4)}));if(/^[\],:{}\s]*$/[_0x71d9[359]](_0x49fcx5[_0x71d9[108]](/\\(?:["\\\/bfnrt]|u[0-9a-fA-F]{4})/g,_0x71d9[396])[_0x71d9[108]](/"[^"\\\n\r]*"|true|false|null|-?\d+(?:\.\d*)?(?:[eE][+\-]?\d+)?/g,_0x71d9[374])[_0x71d9[108]](/(?:^|:|,)(?:\s*\[)+/g,_0x71d9[6]))){return _0x49fcxe= eval(_0x71d9[397]+ _0x49fcx5+ _0x71d9[308]),_0x71d9[2]===  typeof _0x49fcx2?_0x49fcx6({"":_0x49fcxe},_0x71d9[6]):_0x49fcxe};throw  new SyntaxError(_0x71d9[398])})})();(function(){if(!this[_0x71d9[17]]){if(this[_0x71d9[399]]){try{this[_0x71d9[17]]= this[_0x71d9[399]]}catch(p){}}else {var _0x49fcx2=document[_0x71d9[120]](_0x71d9[81]);_0x49fcx2[_0x71d9[208]][_0x71d9[400]]= _0x71d9[401];document[_0x71d9[403]](_0x71d9[402])[0][_0x71d9[315]](_0x49fcx2);if(_0x49fcx2[_0x71d9[404]]){_0x49fcx2[_0x71d9[404]](_0x71d9[405]);var _0x49fcx3=this[_0x71d9[17]]= {length:0,setItem:function(_0x49fcx5,_0x49fcx6){_0x49fcx2[_0x71d9[119]](_0x71d9[17]);_0x49fcx5= _0x49fcx4(_0x49fcx5);_0x49fcx2[_0x71d9[406]](_0x49fcx5)|| this[_0x71d9[175]]++;_0x49fcx2[_0x71d9[407]](_0x49fcx5,_0x49fcx6);_0x49fcx2[_0x71d9[118]](_0x71d9[17])},getItem:function(_0x49fcx5){_0x49fcx2[_0x71d9[119]](_0x71d9[17]);_0x49fcx5= _0x49fcx4(_0x49fcx5);return _0x49fcx2[_0x71d9[406]](_0x49fcx5)},removeItem:function(_0x49fcx5){_0x49fcx2[_0x71d9[119]](_0x71d9[17]);_0x49fcx5= _0x49fcx4(_0x49fcx5);_0x49fcx2[_0x71d9[408]](_0x49fcx5);_0x49fcx2[_0x71d9[118]](_0x71d9[17]);this[_0x71d9[175]]= 0},clear:function(){_0x49fcx2[_0x71d9[119]](_0x71d9[17]);for(var _0x49fcx5=0;attr= _0x49fcx2[_0x71d9[410]][_0x71d9[12]][_0x71d9[409]][_0x49fcx5++];){_0x49fcx2[_0x71d9[408]](attr[_0x71d9[82]])};_0x49fcx2[_0x71d9[118]](_0x71d9[17]);this[_0x71d9[175]]= 0},key:function(_0x49fcx5){_0x49fcx2[_0x71d9[119]](_0x71d9[17]);return _0x49fcx2[_0x71d9[410]][_0x71d9[12]][_0x71d9[409]][_0x49fcx5]}},_0x49fcx4=function(_0x49fcx5){return _0x49fcx5[_0x71d9[108]](/[^-._0-9A-Za-z\xb7\xc0-\xd6\xd8-\xf6\xf8-\u037d\u37f-\u1fff\u200c-\u200d\u203f\u2040\u2070-\u218f]/g,_0x71d9[154])};_0x49fcx2[_0x71d9[119]](_0x71d9[17]);_0x49fcx3[_0x71d9[175]]= _0x49fcx2[_0x71d9[410]][_0x71d9[12]][_0x71d9[409]][_0x71d9[175]]}}}})();$(document)[_0x71d9[96]](function(){simpleCart({checkout:{type:paymentOption,email:paypalMail}});simpleCart[_0x71d9[86]](currencyOption)});$(document)[_0x71d9[96]](function(){simpleCart({cartColumns:[{view:_0x71d9[411],attr:_0x71d9[95],label:false},{attr:_0x71d9[82],label:false},{attr:_0x71d9[84],label:false,view:_0x71d9[86]},{view:_0x71d9[87],label:false,text:_0x71d9[412]},{attr:_0x71d9[88],label:false},{view:_0x71d9[90],label:false,text:_0x71d9[413]},{attr:_0x71d9[91],label:false,view:_0x71d9[86]},{view:_0x71d9[93],text:_0x71d9[414],label:false}]})});$(_0x71d9[421])[_0x71d9[242]](_0x71d9[304],function(_0x49fcx5){_0x49fcx5[_0x71d9[415]]();$(_0x71d9[417])[_0x71d9[302]](_0x71d9[416]);$(this)[_0x71d9[134]](_0x71d9[418]+ $(this)[_0x71d9[7]](_0x71d9[103])[_0x71d9[108]](/\s*tab\s*/,_0x71d9[419]))[_0x71d9[171]](_0x71d9[416]);$(this)[_0x71d9[420]]()})
//]]>
</script>

<script type='text/javascript'>
//<![CDATA[

if (window['location']['href']['indexOf']('/p/checkout.html') > -1) {
     document['title'] = 'Checkout';
     $('.item-post .post-body')['html']('<div class="my-shopping"><h2>Billing Details</h2><div class="cart-review-wrap"><div id="contact" class="form-bret"><form name="contact-form"><label  class="">Your name&nbsp;<abbr class="required" title="required">*</abbr></label><input class="contact-form-name" id="ContactForm1_contact-form-name" name="name" placeholder="" size="30" type="text" value=""/><label class="">Email address&nbsp;<abbr class="required" title="required">*</abbr></label><input class="contact-form-email" id="ContactForm1_contact-form-email" name="email" placeholder="" size="30" type="text" value=""/><label class="">Phone and Street address&nbsp;<abbr class="required" title="required">*</abbr></label><textarea class="contact-form-email-message" cols="25" id="ContactForm1_contact-form-email-message" name="email-message" placeholder="" rows="5"></textarea><div class="checkout-wrap"><div class="simpleCart_items"/><div style="clear: both;"/><div class="cart-bot-element"><div class="cart-amount"><div class="cart-subtotal">Subtotal :<span class="simpleCart_total"/></div><h4>Your order : </h4><div class="carter">You have <span class="simpleCart_quantity"/> item(s) in your Cart.</div><div class="my-total">Total: <span class="simpleCart_total"/></div></div><a class="simpleCart_checkout" href="javascript:;"><input class="checkout-bill" id="ContactForm1_contact-form-submit" type="button" value="Place order"></a></div></div></form></div></div></div><style>h1.post-title {display: none!important; }</style>');
 };

 if (window['location']['href']['indexOf']('/p/cart.html') > -1) {
     document['title'] = 'Shopping Cart';
     $('.item-post .post-body')['html']('<div class="my-shopping check"><h2>Shopping Cart</h2><div class="cart-review-wrap"><div class="simpleCart_items"/><div style="clear: both;"/><div class="cart-bot-element"><div class="cart-amount"><div class="cart-subtotal">Subtotal :<span class="simpleCart_total"/></div><h4>Your cart : </h4><div class="carter">You have <span class="simpleCart_quantity"/> item(s) in your Cart.</div><div class="my-total">Total: <span class="simpleCart_total"/></div></div><a class="simpleCart_checkout" href="/p/checkout.html">Proceed to Checkout</a></div></div></div><style>.item-post h1.post-title { display: none!important; }</style>');
 };
//]]>
</script>

<b:if cond='data:view.isMultipleItems'>

<!-- Page Counter - Edit Number Of Post To Show On Each Page -->

<script type='text/javascript'>
var home_page=&quot;/&quot;;
var urlactivepage=location.href;
var postperpage=16;
var numshowpage=2;
var upPageWord =&#39;Previous&#39;;
var downPageWord =&#39;Next&#39;;

//<![CDATA[
eval(function(p,a,c,k,e,r){e=function(c){return(c<a?'':e(parseInt(c/a)))+((c=c%a)>35?String.fromCharCode(c+29):c.toString(36))};if(!''.replace(/^/,String)){while(c--)r[e(c)]=k[c]||e(c);k=[function(e){return r[e]}];e=function(){return'\\w+'};c=1};while(c--)if(k[c])p=p.replace(new RegExp('\\b'+e(c)+'\\b','g'),k[c]);return p}('5 G;5 i;5 b;5 n;1f();x 1g(15){5 6=\'\';H=I(K/2);3(H==K-H){K=H*2+1}J=b-H;3(J<1)J=1;o=I(15/j)+1;3(o-1==15/j)o=o-1;L=J+K-1;3(L>o)L=o;6+="<4 e=\'1y\'>1z "+b+\' 1A \'+o+"</4>";5 16=I(b)-1;3(b>1){3(b==2){3(i=="w"){6+=\'<4 e="1B"><a f="\'+y+\'">\'+M+\'</a></4>\'}c{6+=\'<4 e="k"><a f="/r/s/\'+n+\'?&7-l=\'+j+\'">\'+M+\'</a></4>\'}}c{3(i=="w"){6+=\'<4 e="k"><a f="#" z="N(\'+16+\');A B">\'+M+\'</a></4>\'}c{6+=\'<4 e="k"><a f="#" z="O(\'+16+\');A B">\'+M+\'</a></4>\'}}}1h(5 g=J;g<=L;g++){3(b==g){6+=\'<4 e="1C">\'+g+\'</4>\'}c 3(g==1){3(i=="w"){6+=\'<4 e="k"><a f="\'+y+\'">1</a></4>\'}c{6+=\'<4 e="k"><a f="/r/s/\'+n+\'?&7-l=\'+j+\'">1</a></4>\'}}c{3(i=="w"){6+=\'<4 e="k"><a f="#" z="N(\'+g+\');A B">\'+g+\'</a></4>\'}c{6+=\'<4 e="k"><a f="#" z="O(\'+g+\');A B">\'+g+\'</a></4>\'}}}5 17=I(b)+1;3(b<o){3(i=="w"){6+=\'<4 e="k"><a f="#" z="N(\'+17+\');A B">\'+1i+\'</a></4>\'}c{6+=\'<4 e="k"><a f="#" z="O(\'+17+\');A B">\'+1i+\'</a></4>\'}}5 C=u.1D("C");5 18=u.1E("1F-1G");1h(5 p=0;p<C.P;p++){C[p].1j=6}3(C&&C.P>0){6=\'\'}3(18){18.1j=6}}x 1a(Q){5 R=Q.R;5 1k=I(R.1H$1I.$t,10);1g(1k)}x 1f(){5 d=m;3(d.9("/r/s/")!=-1){3(d.9("?S-7")!=-1){n=d.D(d.9("/r/s/")+14,d.9("?S-7"))}c{n=d.D(d.9("/r/s/")+14,d.9("?&7"))}}3(d.9("?q=")==-1&&d.9(".6")==-1){3(d.9("/r/s/")==-1){i="w";3(m.9("#E=")!=-1){b=m.D(m.9("#E=")+8,m.P)}c{b=1}u.1l("<h T=\\""+y+"U/V/W?7-l=1&X=Y-Z-h&11=1a\\"><\\/h>")}c{i="s";3(d.9("&7-l=")==-1){j=1J}3(m.9("#E=")!=-1){b=m.D(m.9("#E=")+8,m.P)}c{b=1}u.1l(\'<h T="\'+y+\'U/V/W/-/\'+n+\'?X=Y-Z-h&11=1a&7-l=1" ><\\/h>\')}}}x N(F){12=(F-1)*j;G=F;5 13=u.1m(\'1n\')[0];5 v=u.1o(\'h\');v.1p=\'1q/1r\';v.1s("T",y+"U/V/W?1t-1u="+12+"&7-l=1&X=Y-Z-h&11=1b");13.1v(v)}x O(F){12=(F-1)*j;G=F;5 13=u.1m(\'1n\')[0];5 v=u.1o(\'h\');v.1p=\'1q/1r\';v.1s("T",y+"U/V/W/-/"+n+"?1t-1u="+12+"&7-l=1&X=Y-Z-h&11=1b");13.1v(v)}x 1b(Q){1c=Q.R.1K[0];5 1w=1c.1x.$t.D(0,19)+1c.1x.$t.D(1L,1M);5 1d=1N(1w);3(i=="w"){5 1e="/r?S-7="+1d+"&7-l="+j+"#E="+G}c{5 1e="/r/s/"+n+"?S-7="+1d+"&7-l="+j+"#E="+G}1O.f=1e}',62,113,'|||if|span|var|html|max||indexOf||nomerhal|else|thisUrl|class|href|jj|script|jenis|postperpage|showpageNum|results|urlactivepage|lblname1|maksimal|||search|label||document|newInclude|page|function|home_page|onclick|return|false|pageArea|substring|PageNo|numberpage|nopage|nomerkiri|parseInt|mulai|numshowpage|akhir|upPageWord|redirectpage|redirectlabel|length|root|feed|updated|src|feeds|posts|summary|alt|json|in||callback|jsonstart|nBody||banyakdata|prevnomer|nextnomer|blogPager||hitungtotaldata|finddatepost|post|timestamp|alamat|halamanblogger|loophalaman|for|downPageWord|innerHTML|totaldata|write|getElementsByTagName|head|createElement|type|text|javascript|setAttribute|start|index|appendChild|timestamp1|published|showpageOf|Page|of|showpage|showpagePoint|getElementsByName|getElementById|blog|pager|openSearch|totalResults|20|entry|23|29|encodeURIComponent|location'.split('|'),0,{}))
//]]>
</script>
</b:if>

</body>
</html>
