{
  "date" : "2021-06-09",
  "keywords" :[ "m4b", "mp3", "파일", "확장자", "형식", "m4b 파일 형식이란", "음악", "m4b 파일 형식", "M4b 대 MP3", "m4b 파일 형식 사양 "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"M4B 파일을 생성, 변환 및 열 수 있는 M4B 파일 형식 및 API에 대해 알아보세요.",
  "title" :"M4B - MPEG-4 오디오북 파일 형식",
  "linktitle" : "M4B",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## .M4B 파일이란?

확장자가 .m4b인 파일은 일반적으로 Apple Books 및 iTunes에서 사용하는 오디오북입니다. 이 형식에 사용된 오디오는 MPEG-4로 저장되고 AAC 인코딩을 사용하여 압축됩니다. M4B 파일은 M4A와 매우 유사하지만 북마크 및 장 나누기와 같은 오디오북 관련 기능을 지원합니다. M4B 파일은 DRM 지원 버전과 DRM 무료 버전 모두에서 사용할 수 있습니다. DRM 암호화 오디오북은 일반적으로 iTunes Store의 유료 오디오북입니다. 반면에 DRM free는 인터넷에서 쉽게 찾을 수 있습니다.

## M4B 파일 형식

메타데이터, 이미지, 책갈피 및 하이퍼링크가 포함된 오디오북 파일은 .m4a 확장자로 저장할 수 있지만 일반적으로 파일에 오디오북 파일 형식이 있음을 지정하기 위해 저장하는 동안 .m4b 확장자가 사용됩니다. Fairplay DRM(디지털 권한 관리)은 적용하여 M4B 파일을 보호하는 데 사용됩니다. 따라서 iTunes에서 다운로드한 파일은 인증된 장치 또는 컴퓨터에서만 재생할 수 있습니다.


## M4B 대 M4A

M4B와 [MP3](https://docs.fileformat.com/audio/mp3/)는 모두 오디오 전용 파일 형식입니다.

**M4B**: 동일한 비트 전송률로 둘 다 인코딩하는 경우 품질 측면에서 MP3와 비교할 때 승리합니다. M4B는 AAC 인코딩을 사용하여 압축된 오디오북 파일입니다. 기본적으로 "MPEG-4 오디오 레이어"와 연결되어 있으며 확장자가 .m4b인 파일은 MPEG-4 영화의 오디오 레이어이지만 추가 오디오북 관련 기능이 있습니다. 그 목표는 MP3를 추월하고 오디오 압축의 새로운 표준이 되는 것입니다. 여러 면에서 MP3에 매우 가깝지만 동일하거나 더 작은 파일 크기에서 더 나은 품질을 갖도록 개발되었습니다. M4B 형식은 Apple에서 처음 도입했습니다. 형식 유형은 Apple Lossless Encoder(ALE)로도 구현됩니다.

따라서 현재 M4B는 오디오 형식이 아직 일반적으로 재생되지 않기 때문에 MP3의 주류 성공을 얻지 못했습니다.

**Mp3**: 모든 사람에게 잘 알려진 디지털 오디오 형식입니다. 현장에서 최초의 압축 형식으로 음악 청취자들 사이에서 매우 유명해졌습니다. 주요 성공은 너무 빨라서 파일 형식이 보편적으로 재생될 수 있고 거의 모든 하드웨어 또는 소프트웨어와 호환됩니다. 일반적으로 M4A는 더 나은 음질을 제공하지만 많은 사람들이 그것이 사실이든 아니든 사운드 차이는 비교할 수 없으며 MP3 파일을 M4A 파일로 변환하는 것은 시간 낭비라고 주장합니다. 마지막으로 변환은 원래 음질을 잃게 만듭니다.

## M4B 파일 형식 사양

[M4A](/ko/audio/m4a/)와 유사하게 M4B 파일도 연속적인 청크로 구성됩니다. 각 청크는 8바이트 헤더를 가지며 다음과 같이 세분화됩니다.
- 4바이트 청크 크기(빅 엔디안, 상위 바이트 먼저)
- 4바이트 청크 유형 - 사전 정의된 서명 중 하나: "ftyp", "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "ctab", "건너뛰기", "jP2", "와이드", "로드", "imap", "matt", "chap", "kmat", "clip", "crgn", "sync", "tmcd", "PICT" ", "scpt", "ssrc".

M4A와 유사하게 M4B의 첫 번째 청크는 유형 "ftype"이고 오프셋 8에 하위 유형이 있습니다. 하위 유형에 의해 정의된 M4B는 "M4B_"여야 합니다.

알 수 없는 유형의 청크가 감지될 때까지 청크를 반복하여 M4B(MPEG-4 오디오) 파일을 구성합니다.

## 참고문헌

* [MPEG-4 14부 - 위키피디아 작성](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 오디오(M4A,M4B,M4P) 포맷 및 복구 예](https://www.file-recovery.com/m4a-signature-format.htm)
