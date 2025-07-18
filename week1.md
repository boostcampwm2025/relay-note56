## 🧠 주제 토론

### 프롬프트를 생성해주는 AI

- 프롬프트를 생성하는 AI를 통해 캠퍼분들이 학습 과정에서 AI를 더 용이하게 사용하도록 한다.

### 피어 피드백 시간을 레코딩해서 요약해주는 AI

- 피어 피드백 시간 때 Zoom에서 나눈 이야기를 요약하여 피드백 시간에 어떤 이야기를 나눴는지 요약하면 도움이 될것 같다.

### 커밋을 할 때마다 오토 체크아웃 AI

- 새로운 커밋을 할 때마다 바뀐 내용이 본인이 만든 체크아웃 리스트에 존재할 경우 오토 체크아웃이 된다.

### 슬랙 내부에서 캠퍼들을 1대1 매칭해서 커피챗을 시키는 AI

- 캠퍼분들 사이의 네트워킹을 활발하게 하기 위해 AI를 이용하여, 캠퍼분들을 랜덤으로 1대1 매칭하여 서로 커피챗을 나눌 수 있는 창구를 마련하는 AI다.

### 미션의 학습, 설계, 구현 시간을 자동으로 분배해주는 AI

- 미션을 진행하다 보면 학습과 설계, 구현의 비중을 어떻게 나눠야 할지 어려운데, 미션을 분석하여 해당 미션에 대한 학습, 설계, 구현 시간을 분배해주면 편리할것 같다.

### 내가 원하는 질문에 대해 슬랙에서 찾아서 반환해주는 매니저

- 슬랙 채널에는 많은 메세지가 쌓여있고, 내가 할 질문을 이전에 누군가가 했고, 그에 대한 답변이 무엇인지 알려주면 편리할것 같다.

### 매일 배운 내용을 토대로 주간 요약을 해주는 AI

- 챌린지 미션을 진행하다 보면 평일 초반에 학습한 내용에 대해 잊어버리는 경우가 있는데, 매일 배운 내용을 학습시켜서 주간 요약을 해주면 리마인드되어 학습에 도움이 될것 같다.

## ✅ 중간 투표 결과

### 1차 투표

- 프롬프트를 생성해주는 AI
- 피어 피드백 시간을 레코딩해서 요약해주는 AI - 👍
- 커밋을 할 때마다 오토 체크아웃 AI - 👍👍
- 슬랙 내부에서 캠퍼들을 1대1 매칭해서 커피챗을 시키는 AI - 👍👍
- 미션의 학습, 설계, 구현 시간을 자동으로 분배해주는 AI
- 내가 원하는 질문에 대해 슬랙에서 찾아서 반환해주는 매니저 - 👍👍
- 매일 배운 내용을 토대로 주간 요약을 해주는 AI - 👍👍

### 2차 투표

**동률이 발생하여 구현하기 어려워 보이고 좀 더 하기 싫다…?로 투표를 진행했습니다.**

- 커밋을 할 때마다 오토 체크아웃 AI- 👎
- 슬랙 내부에서 캠퍼들을 1대1 매칭해서 커피챗을 시키는 AI - 👎
- 내가 원하는 질문에 대해 슬랙에서 찾아서 반환해주는 매니저 - 👎👎
- 매일 배운 내용을 토대로 주간 요약을 해주는 AI

⇒ 결국 커밋을 할 때마다 오토 체크아웃 AI, 슬랙 내부에서 캠퍼들을 1대1 매칭해서 커피챗을 시키는 AI, 매일 배운 내용을 토대로 주간 요약을 해주는 AI

**세개로 정하고 실현 가능성에 대해 조사했습니다.**

## 실현 가능성 검증

### 커밋을 할 때마다 오토 체크아웃 AI

Git에서는 모든 데이터 = 객체
<img width="443" height="280" alt="image" src="https://github.com/user-attachments/assets/58b80504-9d28-4c6b-9b63-37a0f57a6126" />

File의 SHA-1해시는 계산되어 Blob개체에 저장

**Commit**: 커밋 메타데이터 + tree 참조 + 부모 커밋 참조

ex) commit

```swift
commit 객체 내용:
tree 4a5e6f2d...     (이 커밋의 루트 tree)
parent 8b1a9c5f...   (이전 커밋 해시)
author 홍길동 <email> 1234567890 +0900
committer 홍길동 <email> 1234567890 +0900

커밋 메시지
```

### SHA-1 해시로 변경 감지

```swift
# 파일 내용이 같으면 항상 같은 해시
echo "Hello World" | git hash-object --stdin
# 출력: 557db03de997c86a4a028e1ebd3a1ceb225be238

# 내용이 바뀌면 다른 해시
echo "Hello World!" | git hash-object --stdin
# 출력: 980a0d5f19a64b4b30a87d4206aade58726b60e3
```

### Tree 객체 비교

```swift
이전 커밋의 tree:
├── README.md (blob: abc123...)
├── src/
│   └── main.py (blob: def456...)

현재 커밋의 tree:
├── README.md (blob: abc123...)  ← 변경 없음
├── src/
│   └── main.py (blob: xyz789...)  ← 변경됨!
```

### Git diff 알고리즘 - **Myers Algorithm**

두개의 문자열 간의 최장 공통 부분 수열(LCS)를 찾는 알고리즘.

DP를 사용하여 LCS계산하고 LCS의 길이 기반으로 변경된 부분 식별

그러면 결국 git diff HEAD~1 HEAD filename.txt 하면 바뀐 내용을 찾을 수 있다.

---

### 슬랙 내부에서 캠퍼들을 1대1 매칭해서 커피챗을 시키는 AI

**개발 언어 및 프레임워크**

- 슬랙 봇을 개발하려면 일반적으로 `Node.js + Bolt` 프레임워크나 `Python`을 이용하여 개발을 진행한다.
- 모든 분야의 캠퍼분들이 모이는 특성상 어느 한쪽으로 치워쳐지는 문제가 발생할 수 있음

**AI 모델 API**

- Gemini API KEY나 Openai API를 이용하여 개발을 진행하거나, 로컬에 모델을 설치하여 개발을 진행해야한다.
- API KEY를 이용하는 경우 누군가가 비용을 지불해야한다는 문제가 생긴다.
- 로컬에 모델을 이용하는 경우 계속 백그라운드 상태에서도 실행이 되도록 배포상태가 유지되어야한다.

**데이터 저장소**

- 참가자 목록을 저장할 방법이 필요함 (이미 했던 매칭은 제외시켜야함, 유저 각각의 관심사 같은것도 저장을 해야하기 때문)
- 가장 간단한 방법은 봇을 실행하는 서버에 JSON 파일로 저장하는 것인데, 이 또한 위에서 서술한 문제(배포)가 있음

---

## 매일 배운 내용을 토대로 주간 요약을 해주는 AI

### 옵시디언

<img width="682" height="429" alt="image" src="https://github.com/user-attachments/assets/3b6a7a2f-aad7-407e-82c1-b1ccff046330" />

자유롭게 메모를 작성하고, 이를 연결하여 지식 네트워크 구축할 수 있는 강력한 도구입니다.

hint) 노트 간 링크 기능: 서로 다른 메모를 연결하여 개인 위키처럼 활용 가능

- 그래프 뷰 제공: 메모들의 관계를 시각적으로 표현

### 노션

<img width="660" height="299" alt="image" src="https://github.com/user-attachments/assets/b70434f2-c013-425a-a263-453fca5eb966" />

## 최종 아이디어 선택

<aside>
💡

**커밋을 할때마다 체크포인트를 최신화해주는 AI
매일 배운 내용을 토대로 주간 요약을 해주는 AI**

</aside>

🙏🏻 커피챗 1대1 매칭 봇 만들기는 구현의 난이도와 배포 유지에 대한 어려움 때문에 제외하였습니다.🙏🏻🙏🏻🙏🏻🙏🏻

# 🧩 개인 퀘스트 수행 내용
---
## 🧑‍💻 [J042 김서연] - "[퀘스트 주제 이름]"

### 수행 내용

---

## 🧑‍💻 [J107 박범한] - "[퀘스트 주제 이름]"

### 수행 내용

---

## 🧑‍💻 [J150 신재광] - "[퀘스트 주제 이름]"

### 수행 내용

---

## 🧑‍💻 [S020 심관혁] - "[퀘스트 주제 이름]"

### 수행 내용

---
