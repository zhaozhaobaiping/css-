### �����ǳ��õĴ����ռ���û���κμ���������ֻ����ӵĻ��ۡ�ת����ע��������лл��

#### 1. css 2.x
- ���ֻ���
```css
/*ǿ�Ʋ�����*/
white-space:nowrap;
/*�Զ�����*/
word-wrap: break-word;
word-break: normal;
/*ǿ��Ӣ�ĵ��ʶ���*/
word-break:break-all;
```

- ���˶���
```css
text-align:justify;text-justify:inter-ideogra
```

- [ȥ��Webkit(chrome)�������input(�ı���)��textarea�Ļ�ɫ�����](http://www.cnblogs.com/niao/archive/2012/09/07/2674511.html)
```css
input,button,select,textarea{ outline:none;}
textarea{ resize:none;}
```

- [ȥ��chrome��ס������Զ������Ļ�ɫ����](http://www.tuicool.com/articles/EZ777n )

- ie6: position:fixed
```css
.fixed-top /* position fixed Top */{position:fixed;bottom:auto;top:0; }
* html .fixed-top /* IE6 position fixed Top */{position:absolute;bottom:auto;top:expression(eval(document.documentElement.scrollTop));}
*html{background-image:url(about:blank);background-attachment:fixed;}
```

- clearfix
```css
.clearfix:after{visibility:hidden;display:block;font-size:0;content:" ";clear:both;height:0;}
.clearfix{display:inline-block;}
html[xmlns] .clearfix{display:block;}
* html .clearfix{height:1%;}

.clearfix{*zoom: 1;}
.clearfix:after{clear:both;display:table;content:"��;}

.clearfix{overflow:hidden;_zoom:1;}
```
[http://www.daqianduan.com/3606.html](http://www.daqianduan.com/3606.html)

- seperate-table
```css
.tab{border-collapse:separate;border:1px solid #e0e0e0;}
.tab th,.tab td{padding:3px;font-size:12px;background:#f5f9fb;border:1px solid;border-color:#fff #deedf6 #deedf6 #fff;}
.tab th{background:#edf4f0;}
.tab tr.even td{background:#fff;}
```
```html
<table class="tab" width="100%" cellpadding="0" cellspacing="0" border="0">
    <tr>
        <th>111</th>
        <td>222</td>
    </tr>
    <tr>
        <th>111</th>
        <td>222</td>
    </tr>
</table>
```

- min-height: ��С�߶ȼ��ݴ���
```css
.minheight500{min-height:500px;height:auto !important;height:500px;overflow:visible;}
```
- ��겻������
```css
cursor:not-allowed;
```
- mac font: osxƽ̨�����Ż�
```css
font-family:"Hiragino Sans GB","Hiragino Sans GB W3",'΢���ź�';
```

- ���ֹ������ʾʡ�Ժ�
```css
.ellipsis,.ell{white-space:nowrap;overflow:hidden;text-overflow:ellipsis}
```

#### 2. css 3

- title ����
```html
&#13;
```

- �ر� x ����
```html
&#215;
```

- ͶӰ
```css
.b{box-shadow:inset 1px -1px 0 #f1f1f1;text-shadow:1px 1px 0px #630;}
filter:progid:DXImageTransform.Microsoft.gradient(enabled='true',startColorstr='#99000000',endColorstr='#99000000');background:rgba(0,0,0,.6);

background:rgba(0,0,0,0.5);filter:progid:DXImageTransform.Microsoft.gradient(GradientType=0,startColorstr='#50000000',endColorstr='#50000000')\9;
```
- [searchռλ](http://www.qianduan.net/search-box-style-custom-webkit.html)
```css
::-webkit-input-placeholder {}
::-moz-input-placeholder {}
input:focus::-webkit-input-placeholder { color: transparent; }
-webkit-appearance:none;  google�߿�ȥ��
input[type="search"]{-webkit-appearance:textfield;} // ȥ��chromeĬ����ʽ
http://i.wanz.im/2011/02/04/remove_border_from_input_type_search/
http://blog.csdn.net/do_it__/article/details/6789699
line-height: normal; /* for non-ie */
line-height: 22px\9; /* for ie */
```

- [ȫ��������ļ��ݴ�������](http://www.colorzilla.com/gradient-editor/ )
[CSS ʵ�� textArea �� placeholder ����](http://segmentfault.com/a/1190000000362621)

- ��ֹĬ���¼�
```css
pointer-events:none;
```

- [ȥ�������۽�ʱ��İ�ɫ����](http://ntesmailfetc.blog.163.com/blog/static/20628706120139184457401/)
```css
-webkit-user-modify: read-write-plaintext-only;
```

- [input:focusʱinput��������������̧�ߵ����](http://www.cnblogs.com/hongru/archive/2013/02/06/2902938.html)
```css
 :focus{-webkit-tap-highlight-color:rgba(255, 255, 255, 0);
 -webkit-user-modify:read-write-plaintext-only;}
```

- ��� gray
```css
html{
    filter: grayscale(100%);
    -webkit-filter: grayscale(100%);
    -moz-filter: grayscale(100%);
    -ms-filter: grayscale(100%);
    -o-filter: grayscale(100%);
    filter: url("data:image/svg+xml;utf8,<svg xmlns=\'http://www.w3.org/2000/svg\'><filter id=\'grayscale\'><feColorMatrix type=\'matrix\' values=\'0.3333 0.3333 0.3333 0 0 0.3333 0.3333 0.3333 0 0 0.3333 0.3333 0.3333 0 0 0 0 0 1 0\'/></filter></svg>#grayscale");
    filter:progid:DXImageTransform.Microsoft.BasicImage(grayscale=1);
    -webkit-filter: grayscale(1);
}
```
- firefox ��ֹѡ��
```css
-moz-user-focus:ignore;-moz-user-input:disabled;-moz-user-select:none;
```
- ��ͷ
```css
display:block;border:solid transparent;line-height: 0;width:0; height:0;border-top:solid #0288ce;border-width:8px 6px 0 6px;

border-style:solid; border-width:7px; border-color:transparent transparent transparent #ff7020;
position:absolute;top: 0;left: 0;border-width:20px;border-style:solid;border-color:#d1ddde transparent transparent #d1ddde;
```
ie6 bug���ԣ���border-style��Ϊdashed.

- ȡ��textarea���½ǿ��϶��ֱ�
```css
resize:none
```
- ȡ��chrome form���ľ۽��߿�
```css
input,button,select,textarea{outline:none}
textarea{resize:none}
```
- ȡ��a���ӵĻ�ɫ�߿�
```css
a{-webkit-tap-highlight-color:rgba(0,0,0,0);}
```
- ȡ��input,button�������ʱ��ɫ�߿�
```css
input{outline:none;}
```
- webkit ˮƽ����
```css
display:-webkit-box;-webkit-box-pack:center; -webkit-box-align: center;
position:absolute; top:50%;left:50%;transform:translate(-50%,-50%);
```
- ȡ��chrome ����x��ʾ
```css
input[type=search]::-webkit-search-decoration,
input[type=search]::-webkit-search-cancel-button,
input[type=search]::-webkit-search-results-button,
input[type=search]::-webkit-search-results-decoration {
    display: none;
}
```
- [chromeȡ��Ĭ�ϻ�ɫ����](http://stackoverflow.com/questions/2338102/override-browser-form-filling-and-input-highlighting-with-html-css)
```css
input:-webkit-autofill {-webkit-box-shadow: 0 0 0px 1000px white inset;}
input:-webkit-autofill,
textarea:-webkit-autofill,
select:-webkit-autofill {
    -webkit-box-shadow: 0 0 0 1000px white inset;
}
autocomplete="off"
```
- �ֻ��汾��ҳa������߿�����
```css
a:focus {outline:none;-moz-outline:none;}
```
- ����ȥ������
```css
-webkit-tap-highlight-color:rgba(255, 255, 255, 0);
-webkit-tap-highlight-color:transparent;  // i.e. Nexus5/Chrome and Kindle Fire HD 7''
```
- placeholderռλ����ɫ�Զ���
```css
input:-moz-placeholder {color: #369;}
::-webkit-input-placeholder {color:#369;}
```

- [IOS ���ø���](http://hi.barretlee.com/2014/03/31/tap-highlight-in-webview/)
```css
-webkit-tap-highlight-color:rgba(255,0,0,0.5);-webkit-tap-highlight-color:transparent; /* For some Androids */
```

- IOS iframe ���� [�����ص���Ч](http://www.cnblogs.com/flash3d/archive/2013/09/28/3343877.html)
```css
-webkit-overflow-scrolling:touch;overflow-y:scroll;
```

- [��ֹѡ���ı�](http://www.qianduan.net/introduce-user-select/)
```css
-moz-user-select:none;
-webkit-user-select:none;
-ms-user-select:none;
user-select:none;
```
- [ģ��(ë����)Ч��1](http://www.zhangxinxu.com/wordpress/2013/11/%E5%B0%8Ftip-%E4%BD%BF%E7%94%A8css%E5%B0%86%E5%9B%BE%E7%89%87%E8%BD%AC%E6%8D%A2%E6%88%90%E6%A8%A1%E7%B3%8A%E6%AF%9B%E7%8E%BB%E7%92%83%E6%95%88%E6%9E%9C/)
- [ģ��(ë����)Ч��2](http://mao.li/css3-blur-filter-pratice/)
- [ģ��(ë����)����Ч��](http://codepen.io/ariona/pen/geFIK)
```css
.blur {
    -webkit-filter: blur(10px); /* Chrome, Opera */
       -moz-filter: blur(10px);
        -ms-filter: blur(10px);
            filter: blur(10px);
}
```
```html
<img src="mm1.jpg" />
<img src="mm1.jpg" class="blur" />
```

- ��ʾ��ת����ͼƬ��[������������](https://github.com/chalecao/chale/blob/master/iscroll.js)
```css
#pullDown .pullDownIcon{display:inline-block;vertical-align:middle;width:40px;height:40px;background:url(https://github.com/chalecao/chale/blob/master/pull-icon%402x.png) 0 0 no-repeat;-webkit-background-size:40px 80px;background-size:40px 80px;-webkit-transition-property:-webkit-transform;-webkit-transition-duration:250ms}
#pullDown .pullDownIcon{-webkit-transform:rotate(0deg) translateZ(0)}
#pullDown .pullDownLabel{display:inline-block;vertical-align:middle;margin-left:5px;}
#pullDown.flip .pullDownIcon{-webkit-transform:rotate(-180deg) translateZ(0)}
#pullDown.loading .pullDownIcon{background-position:0 100%;-webkit-transform:rotate(0deg) translateZ(0);-webkit-transition-duration:0ms;-webkit-animation-name:loading;-webkit-animation-duration:2s;-webkit-animation-iteration-count:infinite;-webkit-animation-timing-function:linear}
@-webkit-keyframes loading{
    from{-webkit-transform:rotate(0deg) translateZ(0)}
    to{-webkit-transform:rotate(360deg) translateZ(0)}
}

```

```html
<div id="pullDown" class="none loading">
    <span class="pullDownIcon"></span><span class="pullDownLabel">����������...</span>
</div>
```

- �ֻ����ն����� media query[web app iphone4 iphone5 iphone6 ��Ӧʽ���� �������](http://club.zoomla.cn/PItem?id=12594)
```css
@media (device-height:480px) and (-webkit-min-device-pixel-ratio:2){/* ����iphone4/4s */
    .class{}
}
@media (device-height:568px) and (-webkit-min-device-pixel-ratio:2){/* ����iphone5 */
    .class{}
}
@media (device-height:667px) and (-webkit-min-device-pixel-ratio:2){/* ����iphone6 */
    .class{}
}
@media (device-height:736px) and (-webkit-min-device-pixel-ratio:2){/* ����iphone6 Plus */
    .class{}
}
```

- ����ƻ������������ֵ�ʶ��[Meta��ǩ�е�format-detection���Լ�����](http://blog.sina.com.cn/s/blog_51048da70101cgea.html)
```html
<meta content="telephone=no" name="format-detection">
```

- �Ƴ�HTML5 input��type="number"ʱ������С��ͷ
  - ��chrome�£�
  ```css
    input::-webkit-outer-spin-button,input::-webkit-inner-spin-button{
        -webkit-appearance: none !important;
        margin: 0;
    }
  ```
  - Firefox�£�
  ```css
    input[type="number"]{-moz-appearance:textfield;}
  ```

  - �ڶ��ַ�����
    - ��type="number"��Ϊtype="tel"��ͬ�������ּ��̣�����û�м�ͷ��

- [HTML5�ֻ����ֱ�Ӹ�һ�������绰��������](http://java-er.com/blog/html5-mobile-call-sms/)

```html
<a href="tel:15222222222">�ƶ�WEBҳ��JSһ�����������ѯ����</a>
<a href="sms:15222222222">�ƶ�WEBҳ��JSһ�����Ͷ�����ѯ����</a>
<!--�ƶ�webҳ���Զ�̽��绰����-->
<meta name="format-detection" content="telephone=no">
<meta http-equiv="x-rim-auto-match" content="none">
```

- [CSS�жϺ�������](http://www.w3cways.com/1772.html)
```css
@media screen and (orientation: portrait) {
  /*���� css*/
}
@media screen and (orientation: landscape) {
  /*���� css*/
}
```

```javascript
//�ж��ֻ�������״̬��
window.addEventListener("onorientationchange" in window ? "orientationchange" : "resize", function() {
        if (window.orientation === 180 || window.orientation === 0) {
            alert('����״̬��');
        }
        if (window.orientation === 90 || window.orientation === -90 ){
            alert('����״̬��');
        }
    }, false);
//�ƶ��˵������һ�㶼֧��window.orientation���������ͨ��������������жϳ��ֻ��Ǵ��ں�����������״̬��
```

- rem ���䣬����̫�ֻ࣬����ַ

    - [rem����Ӧ����](https://github.com/imweb/mobile/issues/3)
    - [html5�ƶ���ҳ��ֱ������ü���Ӧ�����С���õĿ���ʹ�÷�ʽ](http://www.cnblogs.com/willian/p/3573353.html)
    - [�ƶ��˸��塢�������䷽��](http://www.html-js.com/article/Mobile-terminal-H5-mobile-terminal-HD-multi-screen-adaptation-scheme%203041)
    - [ͨ��rem����+media-query:aspect-ratioʵ���ƶ���ȫ�������串��](http://xiaoyuze88.github.io/blog/2015/05/12/%E9%80%9A%E8%BF%87rem%E5%B8%83%E5%B1%80+media-query%E7%9A%84aspect-ratio%E5%AE%9E%E7%8E%B0%E7%A7%BB%E5%8A%A8%E7%AB%AF%E5%85%A8%E6%9C%BA%E5%9E%8B%E9%80%82%E9%85%8D%E8%A6%86%E7%9B%96/)
    - [web app���֮rem](http://isux.tencent.com/web-app-rem.html)
    - [�ֻ��Ա���flexible�����ʵ��](http://www.html-js.com/article/2402)
    - [�ƶ�������Ӧ����](https://github.com/amfe/lib-flexible)
    - [��ԭ�����ƶ��˸��塢�������䷽��](http://www.html-js.com/article/3041)
    - [6��html5ҳ������iphone6�ļ���](http://qietuwang.baijia.baidu.com/article/73861)
    - [�����ƶ��� rem ���ֵ�һЩ�ܽ�](http://segmentfault.com/a/1190000003690140)
    - [���������Ա���font-size˼��ǰ����Ƹ��빤����](http://www.cnblogs.com/lyzg/p/4877277.html)
    - [�ƶ�������Ӧ����](http://f2e.souche.com/blog/yi-dong-duan-zi-gua-ying-fang-an/)
    - [MobileWeb �����ܽ�](http://www.w3ctech.com/topic/979)
    - [�ƶ���web app����Ӧ����̽�����ܽ�](http://www.html-js.com/article/JavaScript-learning-notes%203234)
    - ��ʽ

        ```javascript
        var PAGE_MAX_WIDTH = 1280,
            BASE_FONT_SIZE = 50;
        (function() {
            function n() {
                e.fontSize = Math.min(window.innerWidth / PAGE_MAX_WIDTH * BASE_FONT_SIZE, BASE_FONT_SIZE) + "px"
            }
            var e = document.documentElement.style;
            window.addEventListener("load", n),
            window.addEventListener("resize", n),
            n();
        }());
        ```

- ҳ����л�ʹ����page-enter
```html
<meta http-equiv="PAGE-ENTER" content="RevealTrans(Duration=0,Transition=1)" />
```
- css����ܽ���ַ

    - [css����Ч���ܽ�](http://www.haorooms.com/post/css_common)
    - [css�Ĳ�����Ч���ܽ�](http://www.haorooms.com/post/css_notuse_common)
	- [css��������](http://www.haorooms.com/post/css_skill)
	- [����css��ѡ����](http://www.haorooms.com/post/css_selectelement)
	- [css�ı����ͼ̳�](http://www.haorooms.com/post/css_inherit_bl)
	- [css3�Ļ��ģʽ](http://www.haorooms.com/post/css3_mixblendmode)
	- [css��αԪ��before��after��content�������÷�attr](http://www.haorooms.com/post/content_attr)