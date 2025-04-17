# 클라우드 클럽 7기 스터디 - Google-SRE-Study

## 1. Introduction
> [!NOTE]
>
> ### 스터디 소개
>
> 안녕하세요!
> 
> 이 스터디는 Google이 만든 SRE(Site Reliability Engineering) 개념과 실무에 대해 함께 공부하는 모임입니다. Google의 SRE 책을 통해 서비스 운영 방식과 신뢰성 관리 기법을 배우고, 실제 업무에 적용할 수 있는 인사이트를 얻어갈 수 있습니다.
> 
> 매주 월요일 오후 9시에 모여 각자 읽은 내용을 공유하고 토론하며, GitHub을 통해 스터디 내용을 관리합니다.

---
<br>

### 🕑 Schedule & Members
- **기간**: 2025.03 ~ 2025.05 (8회)
- **시간**: 매주 월요일 오후 10시
- **장소**: 온라인 디스코드 미팅
- **최소 읽기 분량**: 매주 2 Chapter 이상 (추가는 자율적으로)
- **PR 제출 마감**: 스터디 1일 전 **일요일 오후 10시**까지
- **리뷰 마감**: **스터디 시작 30분 전**까지

<br>

### Who need this study?
- DevOps, SRE에 대해 들어봤지만 추상적으로만 이해하고 있는 분들
- 서비스 출시 이후 관리 방법에 대해 궁금하신 분들
- 사이트의 '신뢰성'에 관심 있는 분들
- 서비스 배포 후 안정적인 운영을 '보장'할 방법을 알고 싶은 분들
  

> [!IMPORTANT]
> 
> **이 스터디를 신청하기 전 알아두세요**
> - 책의 내용이 다소 어려울 수 있습니다.
> - 이 책은 SRE 실습보다는 Google의 SRE 철학과 방법론에 초점을 맞추고 있습니다
> - 한국어판은 구매를 권장하며, 영문판은 웹사이트에서 무료로 제공됩니다: [SRE Books](https://sre.google/books/)
> - 스터디 참여 시 불가피한 상황이 아니라면, 캠을 키는 것을 권장하고 있습니다.

---
<br>

## 2. 👽 Our Squad

<table>
  <tr>
    <td align="center"><a href="https://github.com/MinhoJJang"><img src="https://avatars.githubusercontent.com/u/84257033?v=4" width="100px;" alt=""/><br /><sub><b>
👑장민호</b></sub></a><br /></td>
    <td align="center"><a href="https://github.com/doxxx93"><img src="https://avatars.githubusercontent.com/u/51396905?v=4" width="100px;" alt=""/><br /><sub><b>
김도율</b></sub></a><br /></td>
    <td align="center"><a href="https://github.com/Hamburg-Whale"><img src="https://avatars.githubusercontent.com/u/87288460?v=4" width="100px;" alt=""/><br /><sub><b>
조승빈</b></sub></a><br /></td>
    <td align="center"><a href="https://github.com/yucori"><img src="https://avatars.githubusercontent.com/u/110710238?v=4" width="100px;" alt=""/><br /><sub><b>
장지원</b></sub></a><br /></td>
    <td align="center"><a href="https://github.com/yureutaejin"><img src="https://avatars.githubusercontent.com/u/85734054?v=4" width="100px;" alt=""/><br /><sub><b>
진윤태</b></sub></a><br /></td>
    <td align="center"><a href="https://github.com/kiku99"><img src="https://avatars.githubusercontent.com/u/66311161?v=4" width="100px;" alt=""/><br /><sub><b>
김재현</b></sub></a><br /></td>
    <td align="center"><a href="https://github.com/MarkSon-42"><img src="https://avatars.githubusercontent.com/u/84828274?v=4" width="100px;" alt=""/><br /><sub><b>
손민우</b></sub></a><br /></td>
  </tr>
</table>

<br>

## 3. ⛳ Curriculum (Season - 1)
### Season 1 : 25.03.02 ~ 25.05.05 : Site Reliability Engineering Book Study

| Week | Learning Content Title | Details of Learning Content | Completion |
| --- | --- | --- | --- |
| Week 1 | Orientation |  |  |
| Week 2 | Part 1 - Introduction | Chapter 1, Chapter 2 |  |
| Week 3 | Part 2 - Principles | Chapter 3, Chapter 4 |  |
| Week 4 | Part 2 - Principles | Chapter 5, Chapter 6 |  |
| Week 5 | Part 2 - Principles | Chapter 7, Chapter 8 |  |
| Week 6 | Part 3 - Practices | Chapter 9, Chapter 10 |  |
| Week 7 | Part 3 - Practices | Chapter 11, Chapter 12 |  |
| Week 8 | Part 3 - Practices | Chapter 13, Chapter 14 |  |

<br>

---

## 4. GitHub Collaboration Guidelines

### a. 디렉토리 구조
사이트 목차를 기반으로 디렉토리 구조를 구성합니다:
```
root/
├── README.md
├── Part-1-Introduction/
│   ├── Chapter-1/
│   │   ├── minho/
│   │   │   └── README.md
│   │   ├── doyul/
│   │   │   └── README.md
│   │   └── ...
│   ├── Chapter-2/
│   │   └── ...
├── Part-2-Principles/
│   └── ...
```

### b. 커밋 규칙
```
[GSRE-MINHO] - week1
[GSRE-DOYUL] - week2
[Fix] PR 템플릿 오류 수정
[Add] 유용한 참고 자료 추가
```

### c. 브랜치 규칙
- 브랜치명: `GSRE-{이름 대문자}/week{주차}` 
- 예시: `GSRE-YUNTAE/week1`

### d. PR(Pull Request) 규칙
- PR 제목: `[GSRE-MINHO] - week1` 형식으로 작성
- PR 내용은 자유롭게 선택하여 작성:
  - 가볍게 요약
  - 읽으며 궁금했던 점
  - 내 생각
  - 어려웠던 점
  - 레퍼런스 (추가 찾아봄)
  - 다른 사람의 의견이 궁금한 부분

### e. 그라운드 룰
- 스터디 불참 시 Slack에 사유 공유 (필요 시 스터디장에게 DM)
- 불참 시 5,000원 이하 부담 없는 선에서 기프티콘 쏘기
- 책은 구매 권장

### f. README 작성 가이드
- 각자 공부한 내용을 정리할 때 필요하면 [Templates/README-copy.md](https://github.com/cloud-club/google-sre-study/blob/main/Templates/README-copy.md)를 복사하여 사용하세요. 이 템플릿은 기본적인 형식을 제공하므로, 이를 기반으로 내용을 추가하거나 수정할 수 있습니다.

## 5. Reference
- 📚 [SRE 책 구매 링크(Yes24)](https://www.yes24.com/Product/Goods/57979286)
- 🌐 [Google SRE 무료 영문판(온라인)](https://sre.google/books/)
- 📄 [SRE 개념 소개 - IBM](https://www.ibm.com/kr-ko/topics/site-reliability-engineering)
- 🎬 [SRE 소개 영상(YouTube)](https://www.youtube.com/watch?v=uTEL8Ff1Zvk)

> [!WARNING]
> 
> **출석 규정**
> 
> 3회 이상 불참 시 7기를 수료할 수 없습니다.    
> 각 스터디 모임에 참여하지 못할 경우, 사전에 Slack으로 사유를 작성해주세요
