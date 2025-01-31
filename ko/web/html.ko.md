{
  "date" : "2019-10-11",
  "keywords" :[ "html","html 파일", "html 파일 형식", "html 파일 형식", "파일", "유형", "html 파일이란" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTML 파일 형식",
  "description":"HTML 파일 형식과 HTML 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "HTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## HTML 파일이란?

HTML(Hyper Text Markup Language)은 브라우저에 표시하기 위해 생성된 웹 페이지의 확장입니다. 웹 언어로 알려진 HTML은 웹 페이지의 일부로 표시되어야 하는 새로운 정보 요구 사항의 요구 사항과 함께 발전했습니다. 최신 변형은 HTML 5로 알려져 있으며 언어 작업에 많은 유연성을 제공합니다. HTML 페이지는 호스팅되는 서버에서 수신하거나 로컬 시스템에서도 로드할 수 있습니다. 각 HTML 페이지는 양식, 텍스트, 이미지, 애니메이션, 링크 등과 같은 HTML 요소로 구성됩니다. 이러한 요소는 태그와 각 태그에 시작과 끝이 있는 여러 다른 요소로 표시됩니다. 또한 전체 레이아웃 표현을 위해 JavaScript 및 CSS(스타일 시트)와 같은 스크립팅 언어로 작성된 응용 프로그램을 포함할 수 있습니다.

## 간략한 역사 ##

HTML 사양은 처음 만들어지고 첫 역할이 나온 이후로 1996년부터 W3C(World Wide Web Consortium)에서 유지 관리되었습니다. 2000년에는 국제 표준(ISO/IEC 15445:2000)이 되기도 했습니다. 1999년에 HTML 4.01이 출판되었습니다. 2004년 WHATWG(Web Hypertext Application Technology Working Group)는 2008년 W3C와 공동 결과물이 된 HTML5 버전 작업을 시작했습니다. 2014년 10월 28일에 완료 및 표준화되었습니다.

## HTML 파일 형식 구조 ##

HTML 4 문서는 세 부분으로 구성됩니다.

1. HTML 버전 정보를 포함하는 라인
1. 선언적 헤더 섹션
1. 문서의 실제 내용을 포함하는 본문. 본문은 프레임에 본문을 포함하기 위해 BODY 요소 또는 FRAMESET 요소에 의해 구현될 수 있습니다.

각 섹션은 공백, 줄 바꿈, 탭 및 주석이 선행되거나 뒤에 올 수 있습니다. 간단한 HTML 문서의 예는 다음과 같습니다.

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
   <HEAD>
      <TITLE>Understanding HTML File Format</TITLE>
   </HEAD>
   <BODY>
      <P>Hello World!
   </BODY>
</HTML>
```

### 버전 정보 ###

코드의 첫 번째 줄, \<!DOCTYPE html> 는 doctype 선언이라고 하며 페이지가 작성된 HTML 버전을 브라우저에 알려줍니다. HTML 버전에 따라 문서에 사용 중인 DTD(문서 유형 정의)의 이름을 지정하는 다양한 doctype 선언이 있습니다. 각 DTD는 지원하는 요소가 서로 다르며 다음과 같이 다릅니다.

* HTML 4.01 Strict - [deprecated](https://www.w3.org/TR/html401/conform.html#deprecated) 또는 프레임셋 문서에 나타나지 않는 모든 요소와 속성을 포함합니다.
* HTML 4.01 Transitional - 엄격한 DTD의 모든 것과 더 이상 사용되지 않는 요소 및 속성을 포함합니다(대부분 시각적 표현과 관련됨
* HTML 4.01 프레임셋 - 과도기적인 DTD와 프레임의 모든 것을 포함합니다.

**HTML5**의 경우 버전 정보는 아래와 같습니다.

```
<!DOCTYPE html>
```

### HTML 헤더 정보 ###

HTML 문서의 헤더에는 브라우저에서 렌더링되지 않는 여러 HTML 요소가 포함될 수 있습니다. 이러한 요소는 페이지에 대한 정보를 설명하는 메타데이터이거나 CSS 스타일시트 또는 JavaScript 파일과 같은 외부 리소스에서 정보를 가져오는 데 사용되는 섹션을 포함합니다. 페이지의 헤더는 head 태그로 표현됩니다.

페이지 제목을 설정하기 위해 **title** 요소는 내에서 필요한 유일한 요소입니다.<head> 태그. 검색 엔진에서 페이지 제목을 식별하는 데 사용하는 것과 동일합니다.

### HTML 본문 정보 ###

이것은 브라우저에 의해 렌더링되는 파일의 모든 내용을 포함하는 파일의 기본 섹션입니다. HTML 본문에는 태그 형태의 다양한 빌딩 블록을 참조할 수 있는 마크업이 포함될 수 있습니다. 여기에는 텍스트, 이미지, 색상, 그래픽 등과 같은 여러 유형의 정보가 포함될 수 있습니다. 또한 오디오 및 비디오 요소는 브라우저에서 렌더링하기 위해 html 본문에 포함될 수도 있습니다. 시각적 표현을 위한 현대적인 스타일 시트 응용 프로그램이 있는 경우 배경색, 링크 색상, 텍스트 색상 등과 같은 BODY의 표시 속성이 더 이상 사용되지 않습니다. 따라서 아래와 같이 스타일시트를 사용하여 동일한 효과를 얻을 수 있습니다.

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Inline Style Sheets referencing</TITLE>
 <STYLE type#"text/css">
  BODY { background: white; color: black}
  A:link { color: red }
  A:visited { color: maroon }
  A:active { color: fuchsia }
 </STYLE>
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>
```

인라인 스타일 시트는 포함하기 쉽고 시각 효과에 대한 빠른 적용을 위해 외부 스타일 시트를 사용하면 한 번 배포하고 여러 위치에서 액세스할 수 있습니다.

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Linking to External style sheets</TITLE>
 <LINK rel#"stylesheet" type#"text/css" href#"smartstyle.css">
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>

```

### HTML 요소 ###

앞서 언급했듯이 HTML Body 내부의 내용은 Html Elements라고도 하는 태그로 표현됩니다. 각 태그는 다음과 같이 작성되는 속성의 형태로 추가 정보를 가질 수 있습니다.<tag attribute1#"value1" attribute2#"value2"> , 모든 태그에 속성을 가질 필요는 없습니다. 속성이 언급되지 않은 경우 각 경우에 기본값이 사용됩니다. 다음은 몇 가지 요소 예입니다.

#### 헤더 ####

```
<head>
  <title>The Title</title>
</head>
```

#### 제목 ####

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### 단락 ####

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```


## 참조 ##

* [HTML 문서의 글로벌 구조](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

