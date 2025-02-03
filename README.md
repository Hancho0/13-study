# MFC 라벨러 프로젝트

[ 이미지 불러오기 ]<br>
Tree Control에서 선택하거나 Drag and Drop 으로 끌고 오기.<br>
Tree Control 하단에 List Control 에 이미지 이름 출력.<br>
jpg 이미지 형식에 현재 창 사이즈, Picture Control에 이미지 로드<br>

1. Tree Control을 활용한 파일 구조 관리<br>
- Tree Control에서 이미지 파일 목록을 게층 구조로 표시한다.
- 사용자가 특정 이미지를 선택하면 해당 정보가 List Control에 추가된다.
- Drag and Drop 기능을 지원하여 파일을 드래그 하여 추가할 수 있다.

2. List Control을 통한 이미지 목록 관리<br>
- Tree Control에서 선택하거 Drag and Drop 된 이미지의 이름을 list Control에 표시한다.
- 사용자가 List Control에서 특정 이미지를 선택하면 해당 이미지를 Picture Control에서 로드한다.

3. Picture Control에서 이미지 표시
- 선택된 이미지를 Picture Control에 로드하여 화면에 표시한다.
- 현재 창 크기에 맞게 이미지 크기를 조절하여 출력한다.
- 이미지 흑백전환 기능 : 버튼을 누르면 현재 불러온 이미지를 흑백으로 변환하고, 다시 누르면 원래 컬러로 복원한다.

-----
**기술 개념 및 설계**

Tree Control 설계<br>
* 이미지 파일이 포함된 폴더 구조를 Tree Control에 동적으로 로드한다.
* Drag and Drop 기능을 추가하여, 사용자가 이미지를 끌고 올 수 있도록 한다.
* 파일 선택 시, 선택된 파일명을 List Control에 추가하는 이벤트 핸들러를 구현한다.

List Control 설게<br>
* 이미지 파일명을 리스트 형태로 표시한다.
* Drag and Dorp을 통해 Tree Control에서 파일이 추가되도록 처리한다.

Picture Control 설계<br>
* 선택된 이미지를 화면에 로드하여 표시한다.
* 창 크기에 맞춰 이미지를 동적으로 조절한다.
* 지원하는 이미지 포맷은 .jpg 이며, 필요시 확장이 가능하도록 설계한다.
* 이미지 흑백 전환 기능 : 사용자가 버튼을 클릭하면 이미지를 흑백 필터로 변환하고, 다시 누르면 원래 색상으로 복원하는 기능을 추가한다.

-----
**기능 흐름**

Tree Control 초기화<br>
* 사용자가 Tree Control에서 이미지가 포함된 폴더를 선택한다.
* 선택된 폴더의 이미지 파일들이 Tree Control에 게층적으로 표시된다.

Drag and Drop 기능<br>
* 사용자가 폴더에서 이미지를 Drag and Drop한다.
* Drag and Drop 시, List Control에 해당 이미지의 파일명이 추가된다.

이미지 선택 및 표시<br>
* List Control에서 특정 이미지를 클리갛면 Picture Control에서 해당 이미지가 로드된다.
* Picture Control은 현재 창 크기에 맞춰 이미지를 조정하여 표시한다.
