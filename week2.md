# 📘 토론 내용 정리

1. **기존 퀘스트 및 AI에 대한 고민과 검토**

AI를 어떻게 활용할 수 있을지에 대한 진지한 고민이 이루어졌다. 단순히 흥미로운 아이디어를 제시하는 데 그치지 않고, 실제 부스트캠프의 생활에 어떤 식으로 적용 가능할지, 실현 가능성과 구현 난이도 등을 함께 고려하였다.

예를 들어, 주간 요약을 자동으로 생성하는 AI는 실현 가능성과 효용성이 있어 지속할 만한 퀘스트로 판단되었으나, 슬랙에서 질문을 검색해주는 매니저 역할의 AI나 1:1 커피챗 매칭 AI의 경우, 슬랙 관리자 권한이 요구되고 기술적 난이도 역시 높아 해당 아이디어는 퀘스트 범위에서 제외하는 것이 좋겠다는 결론에 이르렀다.

2. **정확한 정보 습득의 중요성 인식**

특히 공식 문서를 해석하고 이해하는 과정에서, 번역된 문서가 갖는 한계와 오류 가능성을 인식하게 되었다. JK님의 조언을 통해 영어 원문을 직접 참고하는 습관이 필요함을 느꼈고, 이는 단순한 언어 학습 차원을 넘어 **정확한 정보 해석 능력의 기초**임을 깨닫게 되었다.

# 🎯 퀘스트 목록

## 1️⃣ 개발자에게 필요한 영어 단어 5개 추천받기

- 배경: AI가 때로는 잘못된, 부족한 정보를 주는 경우가 존재한다. 더욱 명확한 자료는 원문으로 존재하는 경우가 많다.
- 목적: 수월하게 원문을 읽기 위해 영어 능력 향상
- 달성기준: 최소 1번, 원하는 만큼만 부담 없이 수행
- 수행방법: AI에게 개발자에게 필요한 영어 단어를 5개 추천 받고 기록하기

<details>
    <summary>
        예시
    </summary>
<img width="819" height="533" alt="image" src="https://github.com/user-attachments/assets/913c6dce-f074-428a-8f09-b9bd9c3c0eb8" />
</details>

## 2️⃣ 프롬프트를 통한 학습, 설계, 구현 시간 분배하기

## 1.. 이 프롬프트를 사용하는 목적 📌

이 프롬프트의 주 목적은 **AI를 활용해 과제나 프로젝트를 효율적으로 계획하고 실행하는 데 있어요**. 구체적으로:

- **시간 관리 최적화**: 학습(개념 공부), 설계(구조 계획), 구현(실제 코딩/테스트) 단계를 분해하고, 각 단계에 적절한 시간을 배분받아 과도한 지연이나 번아웃을 방지해요. 예를 들어, 멀티스레딩 과제처럼 이론과 실습이 섞인 작업에서 학습 시간을 과소평가하면 전체 프로젝트가 늦어질 수 있죠. 이걸 AI가 추천해주면 객관적이고 유연한 계획을 세울 수 있어요. ⚖️
- **생산성 향상**: 단순히 "과제 해보자"가 아니라, 단계별 가이드와 팁(예: Pomodoro 기법)을 받아 동기부여를 유지하고, 흔한 실수(예: 설계 없이 바로 코딩)를 피할 수 있어요.
- **유연성 강조**: 어떤 과제든(프로그래밍, 학습 프로젝트 등) 적용 가능하게 만들어, 초보자부터 중급자까지 맞춤형 조언을 받을 수 있어요. 궁극적으로는 **목표 달성을 돕고, 학습 과정을 즐겁고 체계적으로 만드는 거예요**! 🚀 예를 들어, 이전 과제처럼 레이스 컨디션 구현 시, AI가 "학습 35%" 추천을 해주면 실제로 시간을 그에 맞춰 배분하며 진행할 수 있죠.

이 목적은 프로젝트 관리 원칙(예: Agile이나 bottom-up estimation)에 기반해 있어요. AI를 "개인 코치"처럼 활용하면, 혼자 고민하는 시간을 줄이고 더 나은 결과를 낼 수 있어요. 😌

## 2. 프롬프트 사용법: 단계별 가이드 🛠️

프롬프트는 AI(예: ChatGPT, Grok, 또는 다른 LLM)에 직접 복사해서 입력하면 돼요. 기본 구조는 이전에 제공된 대로예요 – [과제 세부 사항] 부분만 채워넣으면 돼서 초보자도 쉽죠! 아래에 사용법을 상세히 설명할게요. (전체 프롬프트를 다시 붙여놓았어요.)

## 전체 프롬프트 템플릿

`당신은 소프트웨어 개발 프로젝트의 시간 관리 전문 프로그래밍 교육자입니다. 제가 완수해야 할 프로그래밍 과제가 있는데, 학습, 설계, 구현 단계에 대한 유동적인 시간 분배 추천을 받고 싶습니다. 이는 어떤 과제 세부 사항에도 적응 가능해야 합니다.

**과제 세부 사항:** [여기에 구체적인 과제 설명을 삽입하세요. 학습 목표, 요구사항, 사전 지식 등을 포함.]

이 정보를 바탕으로:
1. 과제를 주요 단계로 분해하세요: 학습(연구 및 개념 이해), 설계(아키텍처 및 구조 계획), 구현(코딩 및 테스트).
2. 각 단계에 대한 예상 시간 분배를 총 시간의 백분율로 제공하세요 (예: 학습 30%, 설계 40%, 구현 30%). 과제 복잡도에 따라 조정하며, 중급 기술 수준을 가정. 총 시간 추정치(예: 10-20시간)를 제안하고, 프로젝트 규모에 따라 확장하는 방법을 설명하세요.
3. 유연한 시간 관리 팁을 제공하세요. 예를 들어, 포모도로 기법으로 집중 세션 관리, 시간 블로킹으로 스케줄링, 예상치 못한 지연에 대한 조정.
4. 시간 분배를 동적으로 모니터링하고 적응하는 방법(예: 주간 리뷰)을 제안하세요.

응답을 명확하고 구조화된, 어떤 과제에도 적응 가능한 방식으로 작성하세요.`

## 단계별 사용법

1. **준비 단계**: 과제 내용을 정리하세요. 예: 학습 목표, 요구사항, 사전 지식 등을 메모. (이전 과제 예시처럼 "프로세스와 스레드 차이 이해" 등을 적어요.) 이걸 **[과제 세부 사항]** 부분에 복사해서 넣어요. 📝
    - 팁: 과제가 간단하면 짧게, 복잡하면 자세히 작성. 예를 들어, "학습 목표: 멀티스레딩 구현. 요구사항: 레이스 컨디션 생성"처럼.
2. **AI에 입력**: AI 채팅창에 위 프롬프트를 통째로 복사+붙여넣기 해요. 영어 버전이 필요하면 이전 대화의 영어 템플릿을 사용하세요. (AI가 영어를 더 잘 처리할 수 있지만, 한국어로도 문제없어요!)
3. **응답 받기와 적용**: AI가 구조화된 답변을 줄 거예요. 예:
    - 단계 분해: 학습/설계/구현 설명.
    - 시간 분배: "학습 35%, 총 20시간"처럼.
    - 팁: Pomodoro 등.
    - 이를 바탕으로 실제 과제 수행! 예: "학습 7시간"을 목표로 책/온라인 자료 공부 후, 설계로 넘어가세요. ⏳
4. **커스터마이징과 반복**: 첫 응답이 맘에 안 들면, "더 자세히 설명해"나 "총 시간 10시간으로 조정해"라고 추가 쿼리. 과제가 변하면 새로 입력해 재사용하세요. 동적 모니터링처럼 주간으로 진행 상황 체크하며 조정! 🔄

1. 일상생활이나 개발을 하면서 잘못된 답을 입력받고 수정하기

## 3️⃣ "의심은 기술이다" – 근거 기반 디버깅 루틴

# 🎯 퀘스트: "의심은 기술이다" – 근거 기반 디버깅 루틴

배경

gpt를 통해 학습을 진행하면 가끔씩 `이게 맞나?`라는 의문이 들 때가 있었습니다.  따라서 이를 검증하는 과정이 필요하다고 느껴 해당 퀘스트를 만들어 보았습니다.

## 📌 목적

- AI, 블로그, 커뮤니티 등에서 얻은 정보를 **맹신하지 않고 검증하는 습관**을 기른다.
- 문제 상황에 대해 **공식 문서나 테스트를 통해 스스로 판단하는 능력**을 훈련한다.
- 실제 개발 현장에서 요구되는 **비판적 사고 + 근거 중심 커뮤니케이션** 능력을 강화한다.

## 🧭 퀘스트 수행 절차

### 1. ❓ 의심 포착하기

다음과 같은 상황이 발생했을 때 바로 기록한다:

- AI/블로그 답변이 **말이 안 되거나 이해되지 않을 때**
- “**이게 맞나?**” 라는 직감이 들 때
- **코드 실행 결과가 예상과 다를 때**
- 동료와 의견이 **갈릴 때**

> 기록 항목 예시
> 
> - 📌 상황 요약
> - 🤔 받은 답변/정보
> - 🔍 구체적으로 의심되는 포인트

### 2. 🔬 검증 루틴 실행하기

최소 2가지 이상의 방법으로 **진위를 확인**한다:

| 검증 방법 | 설명 |
| --- | --- |
| 📘 **공식 문서 확인** | MDN, ECMAScript Spec, React Docs, Node.js Docs 등 |
| ✅ **단위 테스트 작성** | 예상 결과에 대해 테스트 구성 |
| 🧠 **소스 코드 추적** | 라이브러리 내부 구조 파악 (GitHub 등) |
| 💬 **커뮤니티 사례 탐색** | StackOverflow, GitHub issue, Reddit 등 |

### 3. 📓 회고 템플릿 기록 예시

```markdown
### ❓ 의심한 내용
예: "JS에서 setTimeout 안에 async 함수를 넣으면 즉시 실행되나요?"

### 🤖 받은 정보
ChatGPT: "setTimeout(async () => {...})는 일정 시간 뒤에 실행됩니다."

### 🔍 검증한 과정
1. MDN 공식 문서에서 setTimeout 설명 확인
2. 실제 코드 테스트: 로그 순서 분석

### ✅ 최종 결론
- async 함수는 지연 후 실행되며 내부 await 타이밍은 별도
- 타이밍 흐름을 혼동하면 오해 가능

### 🧩 인사이트
- async/await의 실행 흐름은 microtask 큐 기준으로 작동
- 단순히 ‘async = 비동기’가 아님

```

---

## 4️⃣ 매일 배운 내용을 AI를 통해 정리 받고, 주 단위로 개념들의 연결고리를 만들어 정리해보자!

이 미션은 week1에서 다른 조의 캠퍼분들이 만드셨던 미션을 계승하여 더욱 업그데이드 시켜서 만들어보았습니다! 전주에 진행했던 퀘스트의 내용은 
”매일 배운 내용을 한두 줄씩 AI에게 적고, 주간 요약을 시켜서 정리하게 해보기(주간 피드백 때 활용).”이였습니다.

해당 퀘스트의 목적은 챌린지 미션을 진행하다 보면 평일 초반에 학습한 내용에 대해 잊어버리는 경우가 있는데, 매일 배운 내용을 학습시켜서 주간 요약을 해주면 리마인드되어 학습에 도움을 받자는 아이디어에서 시작한 것이라고 생각했습니다.

하지만, AI에게 어떤 내용을 어떻게 입력하느냐에 따라 요약의 품질이 크게 달라지기에 단순히 배운 내용을 텍스트로 던져주면, AI는 핵심을 놓치거나 피상적인 요약만 해줄 가능성이 존재한다고 생각하합니다. 

따라서 AI를 조수 삼아 학습을 극대화 시키기 위해 잘 정리하여 나중에 한주를 돌아보며보기 좋게 정리해주는 템플릿을 활용해보고자 합니다!!!

```markdown
### 1. 핵심 개념 (Key Concept)
- 오늘 배운 내용 중 가장 중요하다고 생각하는 것 1~3가지

### 2. 나만의 언어로 설명하기 (Explain it to me like I'm five)
- 이 개념을 5살 아이에게 설명한다면? (Feynman Technique 활용)

### 3. 질문거리 (My Questions)
- 이 미션에서 꼭 이해해야될 부분을 질문으로 만들어줘!

### 4. 연결고리 (Connections)
- 오늘 배운 내용이 이전에 배운 어떤 것과 연결되는가?
```

1. 사용중인 AI에 채팅방을 새로 만들어 한주간 사용합니다.
2. 위의 템플릿과, 학습정리.md파일을 같이 첨부하여 “내가 첨부한 파일을 해당 스크립트를 기준으로 간단하게 정리해줘”라고 명령을 내리고 ‘질문거리’로 오늘의 공부를 리마인드 하고 마무리합니다!
3. "이번 주에 학습한 내용들의 '연결고리'를 참고해서, **개념들이 서로 어떻게 관련되어 있는지 마인드맵 형태로 설명해줘.**"라고 명령을 내려 마지막 날에 한 주간의 학습을 돌아보는 시간을 가집니다!



---
#### 퀘스트 수행인원: J152신채은, J300황지현, J301황찬우, S015박현수
## 퀘스트 선정:

#### J152신채은:
- 수행 퀘스트: 1.개발자에게 필요한 영어 단어 5개 추천받기
- 선정 이유: 
    - 자료 조사를 하고 공식 문서를 보다보면 원어로 되어있어 따로 해석을 하는 과정이 수반되는 경우가 많았다.
    - 조금씩이라도 영어단어를 알아가면 점차 원문을 읽는게 더 수월해질 것이라 생각한다. 
- 수행 계획: 
    - 피어 컴파일링 하기 전에 잠깐 ai에게 단어 추천받아 암기

#### J300황지현:
- 수행 퀘스트 : 4.매일 배운 내용을 AI를 통해 정리 받고, 주 단위로 개념들의 연결고리를 만들어 정리해보자!
- 선정 이유: 
    - 매일 지식들이 쏟아지다보니 가끔 정리가 잘 안되고,
    - 매일매일의 지식들이 어떻게 연결되는지 모르고 독립적인 개념으로 보는 경우가 있어서 이러한 문제점을 보완하기 위해
- 수행계획 : 
    - 매일매일 미션 마무리전 학습정리와 제공된 템플릿을 첨부하고 정리 요청
    - 질문거리에 답해보며 하루 공부 마무리 
    - 다음주의 마지막 미션을 완료하고 나서 지금까지 쌓인 기록을 바탕으로 개념들의 연결고리에 대해 설명 요청 
    - 결과를 기록

#### J301황찬우:
- 수행 퀘스트: 4.매일 배운 내용을 AI를 통해 정리 받고, 주 단위로 개념들의 연결고리를 만들어 정리해보자!
- 선정 이유: 
    - CS 기초가 부족한 비전공자에게 딱 맞는 릴레이 프로젝트라고 생각했고, 학습 정리에 도움이 될 것 같아서.
- 수행 계획: 
    - 매일 해당 프롬프트와 하루 미션의 학습정리.md 파일을 활용하여, 핵심개념 및 개념요약  정리.
    - AI에 채팅방 하나를 생성해 일주일 간 사용.
    - 마지막 날, 일주일 간 나온 개념들을 마인드맵 형태로 wrap up 하여 주간 학습 회고하기.
#### S015박현수:
- 수행 퀘스트: 1.개발자에게 필요한 영어 단어 5개 추천받기
- 선정 이유: 
    - 개발에 필요한 용어만 알아도 원문을 오독할 확률이 훨씬 낮아지는 것 같습니다.
- 수행 계획:
    - 매일 개발자가 알면 좋은 영어 단어 5개씩 추천 받고 기록하기


---
## 수행 결과: (2025.08.01 작성)

#### J152신채은:
- 수행 내용:
    - deprecated
뜻: 더 이상 권장하지 않음 / 폐기 예정
개발 뉘앙스:
API, 함수, 속성 등에서 “이제 사용하지 말라“는 의미로 등장
아직 동작하긴 하지만, 미래 버전에서는 없어질 수 있음
예문:
This method is deprecated and will be removed in the next release.
→ 이 메서드는 더 이상 권장되지 않으며 다음 릴리스에서 제거될 예정입니다.

    - overhead
뜻: 추가 부담, 부하, 불필요한 비용
개발 뉘앙스:
CPU/메모리/네트워크 등 성능 최적화 얘기할 때 자주 등장
“쓸데없는 추가 비용“이라는 느낌
예문:
Using reflection introduces significant overhead.
→ 리플렉션을 사용하면 성능상 큰 부담이 발생합니다.
    - robust
뜻: 견고한, 안정적인
개발 뉘앙스:
코드나 시스템이 예외 상황에도 잘 버티는 상태
테스트 케이스가 다양해도 쉽게 깨지지 않음
예문:
We need a more robust error handling mechanism.
→ 더 견고한 에러 처리 메커니즘이 필요합니다.
    - fallback
뜻: 대체 수단, 예비 대응책
개발 뉘앙스:
주 기능이 실패하면 실행할 차선책 로직
네트워크 끊기거나, 기능 미지원 시 대체 옵션 제공할 때
예문:
If the primary server is unavailable, the system will fallback to a backup server.
→ 메인 서버가 사용 불가 시 백업 서버로 대체됩니다.
    - legacy
뜻: 구식의, 이전 버전의
개발 뉘앙스:
오래된 코드, 구식 시스템, 유지보수는 하지만 새로운 건 쓰지 않는 상태
보통 “건드리기 싫은 코드“라는 의미로 쓰임
예문:
We are migrating from the legacy system to a modern architecture.
→ 구식 시스템에서 최신 아키텍처로 마이그레이션 중입니다.
- 느낀점:
    - 사실 개발자에게 필요한 영어단어라는 게 추상적인 개념이라 범위를 잡기 어려웠는데 그래도 ai가 범위를 정해서 알려주니 학습에 더 도움이 되었습니다.
    - 영어로 된 공식 문서를 보며 항상 제 영어의 한계를 느끼곤 하는데 시작이 반이라는 말처럼 영단어들이 익숙해지는 연습이 필요할 것 같습니다!
    - Ai는 결국 행동을 명확하고 구체적으로 지정해주거나 아니면 역할을 부여하거나 목표를 정해줄수록 답변 퀄리티가 올라간다는 생각을 했습니다.
    - 결국 그럴려면 저의 목표나 사용 이유가 명확한 상태에서 AI를 사용해야 그 효과를 제대로 볼 수 있을 것이라 생각합니다.
#### J300황지현:
- 수행내용
  월-화 학습정리와, 수-목 학습정리를 제공해주신 스크립트를 통해 정리하고 금요일에 동일한 채팅 안에서 학습한 CS지식끼리의 마인드맵을 그려달라고 요청하였다. 

    월-화 응답내용
    
    <aside>
    💡
    
    ---
    
    ### **1. 핵심 개념 (Key Concept)**
    
    1. **이벤트 기반 비동기 처리 구조**
        - 이벤트 루프, 이벤트 큐, 콜백 함수의 연결 구조
    2. **스레드를 활용한 병렬 처리와 스레드풀**
        - 비동기 처리를 위해 스레드와 스레드풀이 어떻게 활용되는지
    3. **Promise, async/await 문법과 개념**
        - 콜백 지옥을 해결하는 구조와 비동기 흐름을 동기처럼 다루는 방식
    
    ---
    
    ### **2. 나만의 언어로 설명하기 (Explain it to me like I’m five)**
    
    ### **🔸이벤트 루프와 큐**
    
    > 너가 장난감 가게에서 줄을 서서 하나씩 계산하는 걸 상상해보자!
    > 
    
    > 줄(큐)에 장난감들이 기다리고 있고, 점원(이벤트 루프)이 한 개씩 꺼내서 계산해줘.
    > 
    
    > 한 번에 하나씩만 처리하고, 계산이 끝나면 다음 장난감을 처리하지.
    > 
    
    > 장난감이 많으면 줄이 길어지고, 점원은 계속 줄을 보면서 “자, 다음!” 하면서 처리해줘!
    > 
    
    ### **🔸Promise**
    
    > 엄마한테 “내일 사탕 사줄 거야?” 라고 물어봤다고 해보자.
    > 
    
    > 엄마가 “응! 내일 줄게”라고 약속을 했으면, 너는 당장 사탕을 안 받고도 놀 수 있어.
    > 
    
    > 다음날 사탕이 오면 기뻐하겠지!
    > 
    
    > 근데 만약 약속을 못 지키면? 엄마가 “미안, 안 돼”라고 알려줄 거야.
    > 
    
    > 이게 바로 Promise야. 약속을 하고, 성공하면 기쁨, 실패하면 미안함을 알려주는 구조!
    > 
    
    ### **🔸스레드풀**
    
    > 넌 피자 가게 사장님이고, 알바생 4명을 두었어.
    > 
    
    > 주문이 들어오면 일하라고 시키지.
    > 
    
    > 일 끝나면 다시 대기하고, 또 주문 오면 다시 일 시켜.
    > 
    
    > 알바생은 딱 4명이니까 일단 4명까지는 한 번에 처리 가능!
    > 
    
    > 5번째 주문이 오면? 누군가 일이 끝나기 전까지 기다려야 해.
    > 
    
    ---
    
    ### **3. 질문거리 (My Questions)**
    
    1. **이벤트 루프에서 각 phase의 순서와 역할을 확실히 구분할 수 있는가?**
        - Timers / Poll / Check / Close callbacks 등의 차이점은?
    2. **스레드풀의 크기를 정할 때 고려할 요소는 무엇일까?**
        - CPU 수만 보면 되는 걸까, 아니면 작업 성격도 고려해야 할까?
    3. **Promise chaining과 async/await은 내부적으로 어떤 차이가 있는가?**
        - 둘 다 결과적으로 동일한 흐름을 만들지만 성능이나 에러 처리에 차이가 있을까?
    4. **process.nextTick과 queueMicrotask의 정확한 차이점은?**
        - 마이크로태스크보다도 우선 실행되는 구조라면 언제 써야 적절한가?
    
    ---
    
    ### **4. 연결고리 (Connections)**
    
    | **오늘 배운 개념** | **이전 학습 내용 (연결)** |
    | --- | --- |
    | 이벤트 기반 구조 | day6, day9에서 학습한 EventEmitter 구조 및 이벤트 핸들링과 연결됨 |
    | 병렬 처리와 스레드 | day9에서 학습한 멀티 스레드, 레이스 컨디션 내용과 연결됨 |
    | 콜백, Promise, async/await | day8에서 배운 함수형 프로그래밍과 모나드 구조와 연결됨 |
    | mocha 테스트 프레임워크 | 이전 미션에서 작성한 유닛 테스트 경험과 직접 연결되어 실습 가능 |
    | 화이트박스/블랙박스 테스트 | 소프트웨어 테스팅 이론과 현실 프로젝트에서의 실제 적용법과 연결됨 |
    
    ---
    
    
    </aside>
    
    수-목 응답내용
    
    <aside>
    💡
    
    ---
    
    ## **✅ 1. 핵심 개념 (Key Concept)**
    
    1. **버전관리 시스템의 필요성과 유형**
        - 로컬 / 중앙 집중형 / 분산형 구조의 개념 및 차이
    2. **Git의 내부 구조와 동작 원리**
        - .git 디렉토리 구성요소, Git Object 종류(blob, tree, commit)
    3. **Git 명령어의 동작 방식과 내부 처리 흐름**
        - add, commit, switch 등 각 명령어의 내부 처리 이해
    
    ---
    
    ## **🧒 2. 나만의 언어로 설명하기 (Explain it to me like I’m five)**
    
    ### **🖼 버전관리**
    
    “매일매일 그림을 그리고, 잘된 그림은 사진으로 찍어 앨범에 저장한다고 생각해봐! 나중에 마음에 안 들면 지난 사진을 꺼내서 다시 그리면 돼. Git은 그림 앨범을 만들어주는 똑똑한 도구야.”
    
    ### **🧱 Git Object**
    
    “블록 장난감처럼 각각의 파일 내용은 조각(blob), 폴더는 트리(tree), 그리고 사진첩은 커밋(commit)이야. Git은 이 조각들을 조립해서 시간여행을 할 수 있어!”
    
    ### **🧃 zlib + SHA-1**
    
    “Git은 그림을 사진 찍고, 그걸 압축해서 작게 만들고, 번호표(SHA-1 해시)를 붙여서 잘 보관해. 같은 그림은 한 번만 저장돼서 앨범이 절대 무거워지지 않아!”
    
    ---
    
    ## **❓ 3. 질문거리 (My Questions)**
    
    1. Git에서 커밋은 매번 전체 스냅샷을 저장하는데도 왜 효율적일까?
        
        ↪️ zlib 압축 + 중복 저장 안 함 때문이라는데, 내부 압축 알고리즘 흐름이 어떻게 작동할까?
        
    2. git add는 정확히 어떤 정보를 index에 남기는가?
        
        ↪️ blob의 해시, 경로, 권한 등인데, 실제로 커밋 전의 staging 상태를 어떻게 추적하는지 궁금
        
    3. Git은 왜 SHA-1이라는 오래된 해시 알고리즘을 여전히 사용할까?
        
        ↪️ 안정성, 속도 때문이라는데, 보안 측면에서는 문제 없을까?
        
    
    ---
    
    ## **🔗 4. 연결고리 (Connections)**
    
    | **오늘 배운 개념** | **이전 학습 내용과 연결점** |
    | --- | --- |
    | 분산형 버전관리 시스템 | Day6~9에서 공부한 협업 구조와 비동기 작업 흐름과 연결됨 |
    | Git Object 구조 | Day10에서 학습한 파일 시스템, 스냅샷, 병렬처리와의 유사성 |
    | Git 명령어 흐름 | 이전에 CLI 툴 만들며 배운 명령어 파싱과 내부 구조 연동 개념 |
    | SHA-1 + zlib | Day7의 해시함수/압축 구조(데이터 무결성과 공간 효율성) 이해의 연장 |
    
    ---
    
    </aside>
    
    마인드맵 결과
    
    <img width="1024" height="1024" alt="image" src="https://github.com/user-attachments/assets/111fa12b-73ef-46d1-b9aa-4d9a64e506fa" />

- 느낀점
- 실제로 주중에 학습할때 지금까지 배웠던 내용들과의 연결고리를 생각해보려고 노력했었고 이 내용을 학습정리에 담았었는데 내가 생각한 연결고리와 A가 생성해준 연결고리가 어떻게 다른지 비교해볼 수 있었다
- 아직 한국어 이미지 생성이 완벽하지는 않지만 개념의 연결고리를 쉽게 이해하고 싶을때 쓰기에 좋은거같다
- 마인드맵보다는 스크립트를 통해 얻은 결과가 더 만족스러웠다(다른 창을 사용했음에도 불구하고 내가 지금까지 챌린지를 해오면서 사용한 기록들이 반영되어서 지식간의 연결이 더 잘 눈에 들어왔다)
- 또한 마인드맵을 그려달라고만 하면 저렇게 이미지가 아니라 그냥 글 형식으로 그려주기 때문에 이미지를 원한다면 마인드맵을 이미지 형태로 달라고 확실하게 요청해야 한다는 점을 이 퀘스트를 이어받을 분이 계시다면 고려하면 좋을듯하다
#### J301황찬우:
- 수행 내용:

    - 개념 연결 마인드맵
    ```text
    🌳 효율적인 소프트웨어 개발 및 관리
    │
    ├── 📂 1. 코드 관리 (어떻게 코드를 저장하고 변경 이력을 추적할까?)
    │   │
    │   └── 🚀 Git (버전 관리 시스템)
    │       │
    │       ├── 📄 File: Git이 관리하는 가장 기본적인 단위. 모든 코드는 파일 형태로 존재합니다.
    │       │
    │       └── 💎 Git Object (Blob, Tree, Commit): Git이 파일과 변경 이력을 저장하는 핵심 데이터 구조.
    │           │
    │           └── 🔑 Hash (SHA-1): 모든 'Git Object'를 식별하는 고유한 이름표.
    │               │
    │               └─ ✨ 연결고리: Git은 파일(File)의 내용이 조금이라도 바뀌면 완전히 새로운 해시(Hash)값을 생성하여 'Git Object'로 저장합니다. 덕분에 모든 버전의 무결성을 보장하고 빠르고 정확하게 변경 사항을 추적할 수 있습니다.
    │
    ├── 🏗️ 2. 코드 설계 (어떻게 코드를 유연하고 확장성 있게 만들까?)
    │   │
    │   └── 🧩 객체지향 설계 (OOD)
    │       │
    │       └─ ✨ 연결고리: Git으로 관리하는 코드(File)의 내용을 '객체' 단위로 잘 설계하면, 코드의 재사용성과 유지보수성이 극대화됩니다. 각 객체가 명확한 역할과 책임을 가지므로, 특정 기능의 변경이 다른 곳에 미치는 영향을 최소화할 수 있습니다.
    │
    └── ⚡ 3. 성능 최적화 (어떻게 코드를 더 빠르게 실행시킬까?)
        │
        ├── ⏸️ 비동기 (Asynchrony): "기다리지 않고 다음 일 하기"
        │   │
        │   └─ ✨ 연결고리: 객체지향 설계로 만들어진 '파일 처리 객체'가 용량이 큰 파일(File)을 읽거나 네트워크 통신을 할 때, 작업이 끝날 때까지 프로그램 전체가 멈추는 것을 막아줍니다. 요청을 보내놓고 다른 작업을 계속할 수 있어 사용자 경험이 향상됩니다.
        │
        └──  동시에! 병렬 처리 (Parallel Processing): "여러 일을 한 번에 처리하기"
            │
            └─ ✨ 연결고리: 처리할 데이터가 많거나(예: 여러 **파일** 동시에 압축), 복잡한 계산이 필요할 때, 잘 설계된 객체(OOD)들의 작업을 여러 CPU 코어에 나누어 '동시에' 실행시킵니다. 이를 통해 전체 작업 시간을 획기적으로 단축할 수 있습니다.

    총정리:
        Git과 Hash는 우리 코드(File)를 안전하고 체계적으로 보관하는 '스마트 창고' 시스템입니다.
        객체지향 설계는 그 창고에 들어갈 물건(코드)들을 규격에 맞게 잘 만들어서, 나중에 찾고 쓰기 쉽게 만드는 '설계 도면'과 같습니다.
        비동기와 병렬 처리는 잘 설계된 부품(객체)들을 활용해 작업을 더 빠르고 효율적으로 처리하는 '고성능 엔진' 기술입니다.
        
- 느낀점:
    - AI를 활용하여 학습 해시태그를 정리만 하여도 상당한 수준의 학습 루트가 만들어짐
    - 해당 루트대로 학습 계획을 짜면, CS개념 이해에 큰 도움이 됨
    - 앞으로도 개인 학습에 유용하게 활용할 예정
#### S015박현수:
- 수행 내용:
    - 1.개발자에게 필요한 영어 단어 5개 추천받기
    ```
    다음은 개발자에게 필수적인 영단어 5개입니다. 실제 문서, 커밋 메시지, 코드 리뷰, 기술 면접 등에서 매우 자주 쓰이며, 의미와 쓰임을 정확히 아는 것이 중요합니다.
    
    ⸻
    
    1. iterate
    	•	뜻: 반복하다, 순회하다
    	•	맥락: 루프, 배열, 컬렉션 처리 시
    	•	예문:
    We iterate over the array to apply the transformation.
    
    ⸻
    
    2. maintain
    	•	뜻: 유지하다, 관리하다
    	•	맥락: 코드 품질, 기술 부채
    	•	예문:
    This module is hard to maintain due to poor separation of concerns.
    
    ⸻
    
    3. optimize
    	•	뜻: 최적화하다
    	•	맥락: 성능, 메모리, 알고리즘
    	•	예문:
    We optimized the database query to reduce response time.
    
    ⸻
    
    4. rollback
    	•	뜻: (변경 사항을) 되돌리다
    	•	맥락: 배포, 트랜잭션, 에러 처리
    	•	예문:
    If the deployment fails, we should rollback to the previous version.
    
    ⸻
    
    5. merge
    	•	뜻: 병합하다
    	•	맥락: Git, 브랜치 전략
    	•	예문:
    Make sure to resolve all conflicts before merging the feature branch.
    
    ⸻
    
    필요하다면 이 단어들을 중심으로 한 기술 인터뷰 질문, 커밋 메시지 예시, 토익/IELTS 개발자 지문 단어 정리 등도 도와드릴 수 있습니다. 원하시나요?
    ```
    이렇게 하루에 5개의 영어 단어를 추천 받아서 학습했습니다!
- 느낀점:
    - 사실 이번 주에 AI가 추천해 준 단어들은 git 협업을 하거나, 개발을 해오면서 흔히 접할 수 있는 단어들이라 크게 새롭지는 않았던 것 같습니다.
    - 저는 원문 레퍼런스를 읽는 능력을 기르고 싶었는데, 그냥 개발자에게 필요한 영어 단어를 추천해 달라고 하기보다는 필요한 상황에 맞는 영어 단어를 추천해 달라고 하는 쪽이 더 효율적이라는 생각이 듭니다.
    - 추가적으로 문제를 만들어 달라고 요청해서 확인해 보면, 의미 있는 학습이 이루어질 것 같습니다!
