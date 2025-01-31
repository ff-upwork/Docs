{
  "date" : "2021-04-26",
  "keywords" :[ "m4a", "mp3", "파일", "확장자", "형식", "m4a 파일 형식이란", "음악", "m4a 파일 형식", "M4A 대 MP3", "m4a 파일 형식 사양 "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"M4A 파일을 생성, 변환 및 열 수 있는 M4A 파일 형식 및 API에 대해 알아보세요.",
  "title" :"M4A - MPEG-4 오디오 파일",
  "linktitle" : "M4A",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## .M4A 파일이란?

**M4A 파일 형식**은 손실 압축이라고 하는 AAC(Advanced Audio Coding)를 사용하여 만든 오디오 파일입니다. M4A라는 단어는 MPEG 4 오디오로 약칭됩니다. 이러한 오디오 파일의 확장자는 일반적으로 .m4a입니다. 보호되지 않은 콘텐츠의 경우 특히 그렇습니다. 오디오북, 노래 및 팟캐스트와 같은 다양한 유형의 오디오 콘텐츠를 저장할 수 있습니다. M4A는 일반적으로 오디오 전용으로 설계되지 않은 MP3보다 고급 형식으로 구현됩니다. MPEG 1 또는 2 비디오 파일의 오디오 레이어일 뿐입니다.

M4A 형식은 .m4p 확장자를 사용하는 iTunes Store를 통해 판매된 FairPlay 디지털 권한 관리에 의해 암호화됩니다. Apple iPhone은 벨소리에 MPEG-4 오디오를 사용하지만 해당 오디오 파일은 .m4r 확장자를 사용합니다.


## M4A 대 MP3

M4A와 [MP3](/audio/mp3/)는 모두 오디오 전용 파일 형식입니다.

**M4A**: 동일한 비트 전송률로 인코딩할 때 품질과 크기 면에서 MP3보다 낫습니다. .m4a 파일 확장자는 Apple에서 iTunes Music Store에서 사용하기 때문에 매우 일반적입니다. M4A는 MPEG-4 기술을 사용하여 압축된 오디오 파일입니다. 손실 압축 알고리즘. 기본적으로 "MPEG-4 오디오 레이어"와 연결되며 확장자가 .m4a인 파일은 MPEG-4 영화의 오디오 레이어입니다. MP3를 추월하고 오디오 압축의 새로운 표준이 되기 위한 것입니다. 여러 면에서 MP3에 매우 가깝지만 동일하거나 더 작은 파일 크기에서 더 나은 품질을 제공하기 위해 도입되었습니다. M4A 형식은 Apple에서 처음 도입했습니다. 형식 유형은 Apple Lossless Encoder(ALE)로도 구현됩니다.

따라서 현재 M4A는 오디오 형식이 아직 일반적으로 재생할 수 없기 때문에 MP3의 주류 성공을 얻지 못했습니다. 그것은 어떻게 든 MacOS, iPod 및 기타 Apple 제품에만 국한됩니다.

**Mp3**: 가장 유명한 디지털 오디오 형식입니다. 또한 현장에서 최초의 압축 형식 중 하나였으며 음악 애호가들 사이에서 매우 인기가 있었습니다. 주요 성공은 너무 빨라서 파일 형식이 보편적으로 그리고 거의 모든 하드웨어 또는 소프트웨어와 함께 재생될 수 있습니다. 일반적으로 M4A는 더 나은 음질을 제공하지만, 사실 여부와 상관없이 소리의 차이를 구분할 수 없고 MP3 파일을 M4A 파일로 변환하는 것은 시간낭비라고 주장하는 사람들이 많습니다. 결국 변환은 원래 음질을 잃게 만듭니다.

## M4A 파일 형식 사양

M4A 파일은 연속적인 청크로 구성됩니다. 각 청크는 8바이트 헤더를 가지며 다음과 같이 세분화됩니다.
- 4바이트 청크 크기(빅 엔디안, 상위 바이트 먼저)
- 4바이트 청크 유형 - 사전 정의된 서명 중 하나: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2", "와이드", "로드", "ctab", "imap", "matt", "kmat", "클립", "crgn", "동기화", "chap", "tmcd", "scpt ", "ssrc", "PICT".

첫 번째 청크는 유형 "ftype"이고 오프셋 8에 하위 유형이 있습니다. 하위 유형에 의해 정의된 M4A는 "M4A_"여야 하고, M4B 하위 유형의 경우 "M4B_"이어야 하고 M4P 하위 유형의 경우 반드시 "M4P_"가 됩니다.

알 수 없는 유형의 청크가 감지될 때까지 청크를 반복하여 M4A(MPEG-4 오디오) 파일을 구성합니다.

## 참조 ##

* [MPEG-4 14부 - 위키피디아 작성](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 오디오(M4A,M4B,M4P) 포맷 및 복구 예](https://www.file-recovery.com/m4a-signature-format.htm)

