# DEEP - DoneDone Evolution and Enhancement Process

> Inspired by [Kotlin/KEEP](https://github.com/Kotlin/KEEP)

던던은 [Hype Driven Development](https://blog.daftcode.pl/hype-driven-development-3469fc2e9b22)(+ 오버 엔지니어링)를 피하기 위해 각자 개발할 범위를 미리 정리하고 적당한 범위인지 검토받는 과정을 진행합니다. 이 과정을 DEEP 이라고 지칭합니다.

## Current DEEPs

DEEP 은 4가지 유형으로 나뉩니다.

1. 프로덕트
2. 자동화
3. 라이브러리

각각 유형마다 `product`, `automation`, `library` 폴더에 DEEP 문서를 저장합니다. 프로덕트 유형은 [writing-cosmos](https://github.com/TodayDoneDone/writing-cosmos), [ui-waffle](https://github.com/TodayDoneDone/ui-waffle), [donedone-android](https://github.com/TodayDoneDone/donedone-android) 에 해당합니다.

DEEP 는 다음과 같은 양식으로 작성돼야 합니다.

```
# title

작성자:
유형: 
마일스톤: 
마지막 수정일:

### 요약

### 필요한 이유 (프로덕트 유형은 생략 가능)

### 목표

### 비 목표 (non-goal)

### 계획

### 논의 사항
```

DEEP 문서는 개별 브런치에 작성하고 논의를 마친 후에 메인 브런치로 합쳐야 합니다. 논의는 GitHub Discussion 으로 진행합니다. 메인 브런치로 합치는 과정은 PR 로 진행되며 맞춤법 교정과 불필요한 단어 제거 등, 한글을 다듬는 과정을 거친 후 진행됩니다.

## 참고 자료

### 영문

- [Hype Driven Development](https://blog.daftcode.pl/hype-driven-development-3469fc2e9b22)
- [A practical guide to writing technical specs](https://stackoverflow.blog/2020/04/06/a-practical-guide-to-writing-technical-specs/)
- [How to Write Awesome Tech Specs](https://eng.lyft.com/awesome-tech-specs-86eea8e45bb9)

### 한글

- [Hype Driven Development - 설레발 주도 개발](https://lazygyu.net/blog/hype_driven_development)
- [뱅크샐러드의 특별한 스펙, '테크 스펙'](https://blog.banksalad.com/tech/we-work-by-tech-spec/)
