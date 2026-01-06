# ResearchPaperRoutine
Testing agentic workflow from n8n to code

---

File name: Priority_AuthorYear_ShortTitle






---
# History

## Version 1. n8n + Airtable

1.1. Build data in Airtable

| Field    | Exp.              | n8n Type           |
| -------- | ----------------- | -------------- |
| URL      | Paper Link (Primary Key) | Single line text |
| Generate | Auto Gen Button | Button |
| Summary  | Total Summary | Long text |
| Title         | Paper Title | Single line text |
| First Author  | First Author | Single line text |
| Other Authors | Other Authors | Long text |
| Year          | Published year | Single line text |
| Publisher     | Publisher | Single line text |
| Keywords      | Keywords | Single line text |
| File | Shorter version of the title | Single line text |
| Priority | Importance (A - Must see / B - Eye opening /C - Only once) | Single select |
| Insights | Key insights | Long text |

1.2. Benchmark n8n workflows

1.3. Workflow building
  - Enter the URL and click the button
  1. Start workflow with webhook
  2. LLM Generation
  3. Summary Upload

*n8n free OpenAI API credits(gpt4o-mini)
*SerpAPI - 250 Search

1.4. Feedback (RAG paper)
  - Not just summary. Need more rudder for reading the papers
  - Need more detail explanation of formulas (DPR, BART, marginalized?)
  - ChatGPT helps by giving contextual understanding (Try to explain in the manner of understanding)
  - Need more explanation for concepts (Refresh Adam, Beam search)
  - Why did the paper made those results, Structure of the what they wanted to prove.
  - Future research direction

## Version 2. 
Changed the workflow for more information and easier explanation.
Reading objective of the paper is to use information on the real world projects. It should be used for ai consultant who build the architecture of the system, transform the data and fine-tune the model.


| Field    | Exp.              | n8n Type           |
| -------- | ----------------- | -------------- |
| URL      | Paper Link (Primary Key) | Single line text |
| Generate | Auto Gen Button | Button |

| Reading Map | Key Question, diagram of the paper | Long text |
한눈에 보는 독해 지도 (Reading Map)
논문을 읽기 전에 머릿속에 그려야 할 지도
•	이 논문이 답하려는 단 하나의 핵심 질문:
•	저자들이 세운 가설(hypothesis):
•	이 논문이 주장하는 결론 한 문장:
•	논문 전체 구조에서
o	가장 중요한 섹션:
➡️ 목적:
“어디에 집중해서 읽어야 하는지”를 먼저 결정


| Why | Why this paper exists | Long text |
연구 맥락과 문제 설정 (Why this paper exists)
1.1 당시 연구 커뮤니티의 상황
•	이 논문이 나오기 직전, 주류 접근법은 무엇이었나?
•	커뮤니티가 암묵적으로 받아들이던 가정은?
•	성능은 좋았지만 찝찝했던 부분은 무엇이었나?
1.2 기존 연구의 구조적 한계
단순 나열 ❌ → 구조적 문제 정의 ⭕
•	기존 방법들이 공통적으로 갖는 구조:
•	그 구조가 만들어내는 필연적 한계:
•	저자들이 “이건 근본적으로 잘못됐다”고 본 지점:
➡️ 여기서부터 논문의 모든 선택이 설명되기 시작함


| Logic | How did they prove it | Long text |
저자들이 ‘증명하려고 한 것’의 구조
많은 논문은 사실상 논리적 증명 구조를 가짐
3.1 저자들의 논증 구조
•	Step 1: 기존 접근은 왜 실패하는가
•	Step 2: 우리가 제안하는 관점은 무엇이 다른가
•	Step 3: 그 관점이 맞다는 근거 (이론 / 실험)
•	Step 4: 그래서 어떤 결론이 나오는가
➡️ 이 구조를 이해하면 실험 결과가 갑자기 명확해짐


| Methodology | Big picture of the flow | Long text |
방법론 전체 흐름 (Big Picture First)
수식 보기 전에 반드시 거쳐야 할 단계
•	입력은 무엇인가?
•	모델은 무엇을 예측하려는가?
•	중간에 어떤 추상화가 있는가?
•	출력은 무엇이며, 무엇이 달라졌는가?
📌 중요
이 단계에서 이해가 안 되면 → 수식은 절대 이해되지 않음


| Deep Dive | Deep dive in formula | Long text |
핵심 수식 Deep Dive (독해 중심)
❌ “이 수식은 loss function이다”
⭕ “이 수식이 없으면 이 논문은 성립하지 않는다”
5.1 이 수식이 등장한 이유
•	저자들이 직면한 구체적인 문제:
•	기존 수식으로는 왜 해결이 안 됐는가?
5.2 변수 하나씩 다시 읽기
“수식 = 압축된 문장”
•	각 변수는 무엇을 의미하는가
•	모델 안에서 실제로 어디에서 나오고 어디로 가는가
5.3 직관적 설명 (Understanding Mode)
•	이 수식을 한 문장으로 말하면?
•	비유로 설명하면?
•	만약 이 수식을 제거하면 어떤 일이 벌어지는가?
5.4 관련 개념 리프레시 (Context Refresher)
독자가 헷갈릴 수 있는 지점 의도적으로 보완
Examples
•	Adam Optimizer:
o	왜 SGD 대신 Adam을 썼는가?
•	Beam Search:
o	Greedy와 무엇이 다른가?
•	Marginalization:
o	왜 평균을 내는가?
o	무엇을 “모른다고 가정”하는가?
•	DPR / BART:
o	이 논문에서의 역할은 무엇인가?
o	그냥 baseline인가, 구조적 핵심인가?


| Results | How can we understand the results | Long text |
실험 결과를 “이해”하는 방식
숫자보다 이유
6.1 실험은 무엇을 검증하려 했는가
•	가설과 실험의 1:1 대응 관계:
•	각 실험이 반박하려는 반대 주장:
6.2 결과가 이렇게 나온 이유
•	어떤 구성 요소가 성능을 만들었는가?
•	단순 성능 향상인가, 구조적 개선인가?
6.3 결과 해석 시 주의점
•	저자들이 숨긴 전제:
•	특정 데이터셋에만 유리한 이유는?


| Limitation | Limitation implementing to real world | Long text |
이 논문의 한계는 어디서 오는가
한계는 실수가 아니라 선택의 결과
•	이 논문이 포기한 것:
•	이 가정이 깨지면 어떤 문제가 생기는가?
•	스케일, 도메인, 비용 측면의 제약:
Implementing to real world


| Continuation | Research continuation | Long text |
향후 연구 방향 (Research Continuation)
단순 “future work”가 아니라 연구 갈래 제시
•	이 논문이 연 문:
•	아직 열리지 않은 문:
•	후속 연구가 반드시 해결해야 할 질문들:

관련 개념·논문 연결 지도
이 논문을 연구 트리 안에 배치
•	이 논문이 기반으로 삼은 핵심 논문 2–3편
•	이 논문 이후 등장한 대표 후속 연구
•	다른 도메인에서의 유사한 접근


| Takeaway | Readers takeaway | Long text |
최종 독해 요약 (Reader’s Takeaway)
•	이 논문을 읽고 반드시 가져가야 할 생각 3가지
•	이 논문을 다시 안 읽어도 되는 이유 / 다시 읽어야 하는 이유
•	우리 연구/프로젝트에 주는 가장 현실적인 시사점



| Title         | Paper Title | Single line text |
| First Author  | First Author | Single line text |
| Other Authors | Other Authors | Long text |
| Year          | Published year | Single line text |
| Publisher     | Publisher | Single line text |
| Keywords      | Keywords | Single line text |
| File | Shorter version of the title | Single line text |

| Priority | Importance (A - Must see / B - Eye opening /C - Only once) | Single select |
| Insights | Key insights | Long text |

