{
  "date" : "2020-08-20",
  "keywords" :[ "woff 파일", "woff 파일 형식", "woff 파일이란", "파일", "woff 예제", "woff 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WOFF - 웹 오픈 파일 형식",
  "description":"WOFF 파일은 Web Open Font Format으로 만든 개방형 글꼴 형식입니다.",
  "linktitle" : "WOFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-30"
}

## .WOFF 파일이란?

확장자가 .woff인 파일은 WOFF(Web Open Font Format)를 기반으로 하는 웹 글꼴 파일입니다. TrueType(.TTF) 또는 OpenType(.OTT) 글꼴 유형을 기반으로 하는 형식별 압축 컨테이너가 있습니다. WOFF는 데스크톱 응용 프로그램에서 사용되는 글꼴 파일과 웹 글꼴을 구분하기 위해 도입되었습니다. 또한 네트워크를 통해 서버에서 클라이언트 컴퓨터로 글꼴을 전송하는 대기 시간을 줄이기 위한 형식입니다. WOFF 파일을 TTF 및 기타 글꼴 파일 형식으로 변환할 수 있는 여러 도구를 사용할 수 있습니다.

## **WOFF 파일 형식**

WOFF 글꼴 형식은 TrueType, OpenType 및 Open 글꼴 형식과 같은 다양한 글꼴 유형에서 사용되는 테이블 기반 sfnt 구조의 글꼴 데이터 테이블을 압축합니다. 이는 이러한 글꼴 유형을 위한 컨테이너와 같으며 컨테이너에 포함될 글꼴의 메타데이터 및 개인 사용 데이터를 포함할 수 있는 공간도 있습니다. 변환기는 sfnt 파일을 WOFF 형식의 파일로 사용하고 사용자 에이전트는 웹 문서에 사용할 인코딩된 파일을 복원합니다. 복원된 글꼴 데이터는 모든 측면에서 입력 글꼴 형식과 정확히 일치합니다.

WOFF 파일 유틸리티에는 종종 글리프 하위 설정, 유효성 검사 또는 글꼴 기능 추가와 같은 추가 기능이 포함되지만 반드시 필요한 것은 아닙니다. 작성자와 사용 에이전트 모두 기본 글꼴 데이터의 유효성이 유지되도록 해야 합니다.

### WOFF 파일 구조

WOFF 파일 구조는 sfnt 글꼴의 구조와 유사합니다. 각 글꼴 데이터 테이블에 대한 길이와 오프셋이 포함된 테이블 디렉토리를 기반으로 합니다. 이 초기 정보 뒤에 모든 표가 표시됩니다. 파일에는 원본 글꼴과 동일한 글꼴 데이터베이스가 포함되어 있습니다. 테이블의 순서도 동일하지만 각각 압축될 수 있습니다. WOFF 테이블 디렉토리는 원래 테이블 디렉토리를 대체합니다.

WOFF 파일은 다음으로 구성됩니다.

* WOFFHeader - 메타데이터 및 개인 데이터 블록에 대한 오프셋과 함께 기본 글꼴 유형 및 버전이 있는 파일 헤더.
* TableDirectory - WOFF 파일 내에서 원본 크기, 압축된 크기 및 각 테이블의 위치를 나타내는 글꼴 테이블의 디렉토리입니다.
* FontTables - 대역폭 요구 사항을 줄이기 위해 압축된 입력 sfnt 글꼴의 글꼴 데이터 테이블입니다.
* ExtendedMetadata - XML 형식으로 표시되고 WOFF 파일에 저장하기 위해 압축된 확장 메타데이터의 선택적 블록입니다.
* PrivateData- 글꼴 디자이너, 파운드리 또는 공급업체가 사용할 개인 데이터의 선택적 블록입니다.

### WOFF 헤더
WOFF 헤더는 파일에 포함된 데이터의 종류를 나타내는 식별 서명으로 구성됩니다. WOFF 헤더와 해당 필드는 다음과 같습니다.

|유형|필드 이름|설명|
---|---|---|
|UInt32|서명 |0x774F4646 'wOFF' |
|UIint32| 맛 |입력 글꼴의 "sfnt 버전".|
|UIint32| length |WOFF 파일의 전체 크기입니다.|
|UInt16| numTables |글꼴 테이블의 디렉토리에 있는 항목 수.|
|UInt16| 예약됨 |예약됨; 0으로 설정합니다.|
|UIint32| totalSfntSize |sfnt 헤더, 디렉토리 및 글꼴 테이블(패딩 포함)을 포함하여 압축되지 않은 글꼴 데이터에 필요한 총 크기.|
|UInt16| majorVersion |WOFF 파일의 주 버전입니다.|
|UInt16| minorVersion |WOFF 파일의 부 버전입니다.|
|UIint32| metaOffset |WOFF 파일의 시작 부분에서 메타데이터 블록으로의 오프셋.|
|UIint32| metaLength |압축된 메타데이터 블록의 길이입니다.|
|UIint32| metaOrigLength |메타데이터 블록의 압축되지 않은 크기입니다.|
|UIint32| privOffset |WOFF 파일의 시작 부분에서 개인 데이터 블록으로 오프셋.|
|UIint32| privLength |개인 데이터 블록의 길이.|


## **참고문헌**
* [w3 WOFF 파일 형식](https://www.w3.org/TR/WOFF/)

