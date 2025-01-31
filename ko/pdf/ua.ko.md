{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PDF/UA 파일 형식",
  "description":"PDF/UA 파일 형식과 PDF/UA 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "PDF/UA",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# PDF/UA 파일이란? #

PDF/UA는 2012년 8월에 [ISO 표준 14289-1](https://en.wikipedia.org/wiki/ISO_14289)로 게시되었으며 지금까지 보편적으로 액세스할 수 있는 PDF 문서에 대한 일련의 요구 사항에 대한 완전한 정의입니다. "보편적으로 접근할 수 있는"이라는 용어는 [PDF](/ko/pdf/) 문서에 포함된 정보가 모든 사람과 특히 장애인이 동등하고 독립적으로 접근할 수 있어야 한다는 이해를 의미합니다. PDF/UA 표준의 도입은 PDF 콘텐츠를 만들고 읽기 위한 도구와 응용 프로그램을 만드는 주요 단계로 간주될 수 있습니다.

## 파일 형식 요구 사항 ##

PDF/UA에는 이 표준의 핵심 역할을 하는 몇 가지 명확한 요구 사항이 있습니다. 기본적으로 이는 모든 PDF/UA 문서에 적절하게 태그를 지정해야 함을 의미하는 PDF 태그 지정을 기반으로 합니다. 또한 태그가 의미상 적절하고 논리적인 순서로 되어 있어야 합니다. 이렇게 하면 PDF/UA 사양으로 작성된 최종 문서가 더 안정적이고 액세스 가능합니다. 이것은 PDF 작성자가 그러한 모든 요구 사항에 대한 모든 것을 알아야 하는지에 대해 의문을 제기할 수 있습니다. 운 좋게도 PDF/UA 준수 도구가 PDF의 액세스 가능성을 추가하고 유지하는 책임을 지기 때문에 이와 같지 않습니다.

PDF/UA의 파일 형식 요구 사항은 다음과 같습니다.

* 콘텐츠는 의미 있는 콘텐츠와 장식적인 페이지 요소와 같은 인공물의 두 가지 방식 중 하나로 분류됩니다. 모든 의미 있는 콘텐츠는 태그를 지정하고 문서 내 모든 태그의 구조 트리에 통합해야 합니다. 반면에 인공물은 그대로 표시하기만 하면 됩니다.
* 의미 있는 내용은 태그로 표시되어야 하며 문서의 다른 태그와 함께 완전한 구조 트리를 생성해야 합니다.
* 의미 있는 콘텐츠는 적절한 의미 태그로 표시되어야 합니다.
* 문서 태그에 의해 생성된 구조 트리는 문서의 논리적 읽기 순서를 반영해야 합니다.
* PDF 1.7에 정의된 표준 태그만 사용할 수 있습니다. 다른 태그가 사용되는 경우 역할 할당 항목은 각각이 나타내는 표준 태그를 기록해야 합니다.
* 정보는 시각적 수단(예: 대비, 색상 또는 페이지의 위치)만으로는 전달되지 않을 수 있습니다.
* 깜박임, 깜박임 또는 깜박이는 콘텐츠는 JavaScript로 제어되는 효과로 또는 PDF에 포함된 비디오의 일부로 허용되지 않습니다.
* 문서 제목은 반드시 기재해야 하며, 창 제목에 제목(파일명이 아닌)이 나타나도록 문서를 설정해야 합니다.
* 모든 내용의 언어는 반드시 표기되어야 하며, 언어의 변경은 명시적으로 표기되어야 합니다.

## PDF/UA 준수 ##

PDF/UA 표준은 콘텐츠, 리더 및 보조 기술에 대한 사양을 정의합니다. 이 세 가지 측면은 문서의 내용을 기반으로 서로 연결되어 있습니다. 이들 각각에 대한 적합성 요구 사항은 다음과 같습니다.

## 준수 파일 ##

PDF/UA 표준을 준수하는 파일에는 [PDF 1.7 사양](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf)에 따라 유효한 기능이 포함되어야 합니다. 그러나 PDF/UA에서 특별히 금지하는 기능은 제외해야 합니다.

## 준수 독자 ##

준수하는 리더는 PDF 1.7 사양의 규칙을 준수해야 합니다. 구체적으로 다음을 지원해야 합니다.

* 접근성을 위해 지정된 모든 태그, 속성 및 키 값. 또한 디지털 서명, 주석 및 선택적 콘텐츠를 처리하고 표현할 수 있어야 합니다.
* 디지털 서명, 주석 및 선택적 콘텐츠 처리 및 표현
* 다양한 수단으로 문서 탐색

## 보조 기술 준수 ##

PDF/UA 기능을 지원하기 위해 준수하는 보조 기술이 필요합니다. 예를 들어 여기에는 콘텐츠 및 독자의 기능이 포함되며 페이지 레이블, 문서 구조 또는 개요별로 탐색할 수 있어야 합니다. 또한 사용자가 기본 탐색 확대/축소를 재정의할 수 있어야 합니다.

## 참조 ##

* [PDF/UA - 위키피디아 작성](https://en.wikipedia.org/wiki/PDF/UA)
* [PDF/UA 요약](https://pdfa.org/pdfua-in-a-nutshell/)

