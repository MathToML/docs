# what_we_learned.md

## 이미지 여백 자동 제거 (투명 PNG 트리밍)

### 목적
오브젝트만 남기고 투명 배경 여백이 많은 PNG 이미지를 자동으로 크롭하여, 앱 등에서 보기 좋게 사용한다.

### 명령어 예시 (ImageMagick 사용)
아래 명령어를 터미널에서 실행하면, 원본 이미지의 불필요한 투명 여백이 제거된 새 파일이 생성된다.

```sh
magick 원본파일.png -trim +repage 결과파일.png
```

#### 예시
```sh
magick black.png -trim +repage black_trimmed.png
magick green.png -trim +repage green_trimmed.png
```

- 여러 파일을 한 번에 처리하려면 각 파일마다 명령어를 반복 실행해야 함.
- ImageMagick이 설치되어 있어야 한다.

## VS code reset
환경설정정보는 따로 저장되므로 아래디렉토리를 지워야 리셋된다.
```
~/Library/Application Support/Code
```
terminal에서는 빈 칸을 escape해야 하므로
```
rm -R ~/Library/Application\ Support/Code
```

---

## 이 파일을 업데이트하는 법

1. 새로운 작업이나 배운 점이 있으면, 이 파일에 마크다운 형식으로 추가한다.
2. 기존 내용 중 더 나은 방법이나 수정이 필요한 부분이 있으면, 해당 내용을 직접 수정한다.
3. 명령어, 코드, 설명 등은 복사해서 바로 쓸 수 있게 예시와 함께 작성한다.
4. 변경 후 git add/commit/push로 저장소에 반영한다.

---

## 기타

- 이 파일은 프로젝트의 지식/팁/노하우를 축적하는 용도로 사용한다.
- 불필요한 중복은 줄이고, 최신 정보로 유지한다.
- public 저장소에 저장되므로 개인정보에 관련된 것은 삭제하거나 다른 것으로 대체하고 업데이트한다.
