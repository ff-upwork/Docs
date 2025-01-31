{
  "date" : "2021-23-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MK3D 파일 형식",
  "keywords" :[ "mk3d", "matroska 비디오", "mkv 형식", "입체 3d", "스테레오 모드", "비디오", "파일", "형식" ],
  "description":"Matroska에서 만든 입체 3D 비디오용 MK3D 파일 형식과 MK3D 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "MK3D",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-23-02"
}

## .MK3D 파일이란? ##

MK3D 파일은 Matroska 비디오 형식 제품군에 속합니다. 이 파일은 실제로 Matroska 3D 형식을 사용하여 만든 **입체 3d** 동영상입니다. MKV 파일 컨테이너는 스테레오 모드 필드 값을 사용하여 입체 3D 비디오 항목의 유형을 정의합니다. StereoMode 값은 청록색과 빨간색을 분리하여 이전 스테레오 3D 비디오를 표시하는 데 사용할 수도 있습니다(AnaGlyph).

## 기술적 세부 사항 ##
3D 비디오는 다음 두 가지 방법으로 압축할 수 있습니다.

- 각 눈에 대한 별도의 트랙.
- 각 시선 추적을 단일 트랙으로 결합합니다.

MKV 파일 컨테이너는 이 두 가지를 모두 지원합니다.

내부에 3D 자료가 있는 단일 트랙 비디오의 경우 평면이 모노 또는 왼쪽 오른쪽 결합 트랙으로 조립되는지 결정하는 **StereoMode** 필드를 설정해야 합니다. 다음 StereoMode 필드 값 중 하나를 사용할 수 있습니다.

|가치 | 설명 |
|---|---|
|0| 모노|
|1| 나란히(왼쪽 눈이 먼저)|
|2| 위 아래(오른쪽 눈이 먼저)|
|3| 위아래(왼쪽 눈이 먼저)|
|4| 체크보드(오른쪽이 먼저)|
|5| 체크보드(왼쪽이 먼저)|
|6| 인터리브된 행(오른쪽이 첫 번째)|
|7| 행 인터리브(왼쪽이 첫 번째)|
|8| 열 인터리브(오른쪽이 첫 번째)|
|9| 열 인터리브(왼쪽이 첫 번째)|
|10| 애너글리프(청록색/빨간색)|
|11| 나란히(오른쪽 눈이 먼저)|
|12| 애너글리프(녹색/자홍색)|
|13| 두 눈을 하나의 블록에 묶음(왼쪽 눈이 먼저임)(필드 순차 모드)|
|14| 두 눈을 하나의 블록에 묶음(오른쪽 눈이 먼저임)(필드 순차 모드) |

다중 트랙의 경우 MKV 컨테이너는 각 트랙의 기능을 개별적으로 결정해야 합니다. **TrackCombinePlanes**가 있는 **TrackOperation**은 작업을 수행하는 데 사용됩니다.


## 참조 ##

- [Matroska 사양 노트](https://www.matroska.org/technical/notes.html)
- [스테레오 3D 비디오 및 MK3D 파일에 대한 MKV 파일 컨테이너 지원](https://3dvision-blog.com/5520-mkv-file-container-support-for-stereo-3d-video-and-the-mk3d-files/)

