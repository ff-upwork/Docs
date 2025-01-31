{
  "date" : "2021-07-13",
  "keywords" :[ "CER", "확장자", "파일", "형식", "웹", "인증서", "언어" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CER - 인증서 파일 형식",
  "description":"CER 파일을 만들고 열 수 있는 CER 파일 형식 및 API에 대해 알아보세요.",
  "linktitle" : "CER",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## .CER 파일이란? ##

확장자가 .cer인 파일은 소유자 인증서와 특정 공개 키에 대한 일부 정보를 저장하는 역할을 합니다. 이 형식의 파일은 개인 키를 저장할 수 없으며 x509라는 하나의 인증서만 저장할 수 있습니다. 특별히 보안된 인증 기관은 검색을 위한 신뢰할 수 있고 안전한 프로토콜인 HTTPS에 속하는 인증 기관입니다.
CER은 서버의 인증서입니다. 일반적으로 도메인의 인증 기관에서 수신합니다. CER은 대부분 [CRT](/ko/web/crt/)와 동일한 것으로 간주되지만 둘 다 SSL 인증서 형식은 동일하지만 파일 이름 확장자는 다릅니다.
브라우저를 열고 사용 중인 브라우저나 웹사이트의 보안을 확인하기만 하면 운영 체제에서 사용할 수 있습니다.

## 간략한 역사 ##

1995년에 Thawte는 미국 이외의 지역에서 공개 SSL(보안 소켓 링크) 인증서 문제를 해결하기 위한 최초의 인증 기관이 되었습니다. 그 후, 1995년부터 2020년까지 설립된 일련의 그러한 당국이 있습니다.

## CER 파일 형식 ##

이러한 파일은 단순히
* PKC S#7은 Base64 ASCII 인코딩으로 구성됩니다.
* 파일 확장자는 p7b 또는 p7cZ입니다.
* 바이너리 콘텐츠의 경우 인증서는 DER 또는 pkcs12/pfx입니다.
몇 가지 고유한 사양을 가진 다양한 유형의 인증서 파일이 있습니다.
* .pem, 이 형식을 연결하는 조직 usThawteificate가 인증서를 생성하는 것으로 잘 알려진 경우
* .arm은 인증을 추출하는 방법이 자체 서명을 지원하는 경우 필요하며 이를 위해 지정된 형식은 .arm입니다. base-64 ASCII 인코딩으로 표시됩니다.
* .der, 바이너리 데이터로 구성됩니다. 이는 단일 인증서에만 사용할 수 있음을 의미합니다.
* .pfx(PKC512), CA에서 발급한 인증서 또는 자체 서명된 인증서에 해당하는 개인키로 구성된다. 이 형식은 하나의 SSL 구현을 다른 구현으로 변환하는 것으로 잘 알려져 있습니다.


