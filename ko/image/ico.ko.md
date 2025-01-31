{
  "date" : "2019-10-11",
  "keywords" :[ "ico 파일", "ico 파일 형식", "ico 파일이란", "파일", "ico 예제", "ico 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICO - 이미지 파일 형식",
  "description":"ICO 파일을 생성하고 열 수 있는 ICO 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "ICO",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## .ICO 파일이란?

ICO 확장자를 가진 파일은 [Microsoft Windows](https://www.microsoft.com/en-us/windows)에서 응용 프로그램을 나타내는 아이콘으로 사용되는 이미지 파일 형식입니다. 디스플레이 요구 사항에 맞게 다양한 크기, 색상 지원 및 해상도로 제공됩니다. Microsoft Windows의 또 다른 유사한 이미지 파일 형식은 커서 표시를 위한 [CUR](/ko/image/cur/)이며 이미지 헤더에 핫스팟을 정의합니다. MacOS에서 ICNS 파일 형식은 ICO 파일과 동일한 용도로 사용됩니다. 여러 온라인 웹 사이트 및 응용 프로그램은 이러한 파일을 만들고 [BMP](/ko/image/bmp/), [PNG](/ko/image/png/) 등과 같은 다른 이미지 형식을 아이콘 파일 형식으로 변환하는 기능을 제공합니다. ICO 파일에 대한 공식 IANA 등록 인터넷 미디어 유형은 image/vnd.microsoft.icon입니다.

## 간략한 역사 ##

아이콘은 Microsoft Windows 1.0 출시와 함께 도입되었습니다. 크기는 32x32이며 흑백이었습니다. win32가 출시되면서 최대 256x256 픽셀의 트루 컬러 아이콘 이미지 지원이 도입되었습니다. Windows XP는 32비트 컬러 아이콘 이미지에 대한 지원을 제공한 최초의 제품으로 그림자, 앤티 앨리어싱 및 유리 같은 효과와 같은 반투명 영역을 아이콘에 추가할 수 있습니다. Microsoft는 Windows XP에 대해 최대 48×48 픽셀의 아이콘 크기만 권장합니다. Windows Vista는 압축된 [PNG](/ko/image/png/) 형식에 대한 지원뿐만 아니라 Windows 탐색기에 256×256 픽셀 아이콘 보기를 추가했습니다. 더 높은 해상도와 높은 DPI 모드를 사용하는 사용자의 경우 더 큰 아이콘 형식(예: 256×256)을 사용하는 것이 좋습니다.

## ICO 파일 형식 ##

단일 ICO 파일은 다양한 크기와 색상 깊이의 하나 이상의 작은 이미지로 구성됩니다. 여러 크기의 이미지가 있는 것은 다양한 화면 해상도에서 적절한 크기 조정을 위한 것입니다. ICO/CUR 파일의 모든 값은 [little-endian](https://en.wikipedia.org/wiki/Little-endian) 바이트 순서로 표시됩니다.

ICO 파일은 아이콘 헤더, 아이콘 디렉토리,

|필드|설명
---|---|
|아이콘 헤더|ICO 파일에 대한 일반 정보를 저장합니다.
|디렉토리[1..n]|파일의 모든 이미지에 대한 일반 정보를 저장합니다.
|아이콘 #1|이전 AND/XOR DIB 형식 또는 최신 PNG 형식의 첫 번째 이미지에 대한 실제 "데이터"
|...|
|Icon #n|마지막 아이콘 이미지의 데이터

### 헤더 ###

|오프셋|크기(바이트)|목적
---|---|---|
|0|2|예약됨. 항상 0이어야 합니다.
|2|2|이미지 유형 지정: 아이콘(.ICO) 이미지의 경우 1, 커서(.CUR) 이미지의 경우 2. 다른 값은 유효하지 않습니다.
|4|2|파일의 이미지 수를 지정합니다.

### 디렉토리 ###

ICONDIR 구조로 표현되는 ICO 파일에 포함된 디렉토리는 파일의 각 이미지에 대한 ICONDIRECTORY 구조를 포함합니다. 모든 이미지 비트맵 데이터의 연속 블록이 뒤따릅니다. 이것은 아래와 같습니다.

|오프셋|크기|설명
---|---|---|
|0 (0)|1|너비, 256픽셀인 경우 0이어야 합니다.
|1 (1)|1|높이, 256픽셀인 경우 0이어야 합니다.
|2 (2)|1|색상 개수, 256개 이상의 색상인 경우 0이어야 합니다.
|3 (3)|1|예약됨, 0이어야 함
|4 (4)|2|.ICO 형식의 경우 색상 평면은 0 또는 1이어야 하며, .CUR 형식의 경우 X 핫스팟이어야 합니다.
|6 (6)|2|.ICO 형식의 경우 픽셀당 비트 수, .CUR 형식의 경우 Y 핫스팟
|8 (8)|4|바이트 단위의 비트맵 데이터 크기.
|12 (C)|4|파일의 오프셋.

## 참조 ##

* [ICO - 위키피디아 작성](https://en.wikipedia.org/wiki/ICO_(file_format))
* [IANA - vnd.microsoft.icon](http://www.iana.org/assignments/media-types/image/vnd.microsoft.icon)

