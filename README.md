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

Delete summary
Add Reading Map, which finds the focus area
Add Why, which is the reason of reading
Add Logic, which tells the logical structure
Add Methodology, which gives detail understanding of the methods
Add Deep dive, of the forumula
Add Results, how to understand the result
Add Limitations, implementing in real world
Add Continuation, direction of future research
Add Takeaways, 3 points of the paper

| Field    | Exp.              | n8n Type           |
| -------- | ----------------- | -------------- |
| URL      | Paper Link (Primary Key) | Single line text |
| Generate | Auto Gen Button | Button |
| Reading Map | Key Question, diagram of the paper | Long text |
| Why | Why this paper exists | Long text |
| Logic | How did they prove it | Long text |
| Methodology | Big picture of the flow | Long text |
| Deep Dive | Deep dive in formula | Long text |
| Results | How can we understand the results | Long text |
| Limitation | Limitation implementing to real world | Long text |
| Continuation | Research continuation | Long text |
| Takeaway | Readers takeaway | Long text |
| Title         | Paper Title | Single line text |
| First Author  | First Author | Single line text |
| Other Authors | Other Authors | Long text |
| Year          | Published year | Single line text |
| Publisher     | Publisher | Single line text |
| Keywords      | Keywords | Single line text |
| File | Shorter version of the title | Single line text |
| Priority | Importance (A - Must see / B - Eye opening /C - Only once) | Single select |
| Insights | Key insights | Long text |


Takeaways of version 2.
- Too many workflows from the AI
- Integrate text extraction
- Remove search tool usage
- Error on primary key (encoding url) - Fixed
- Need to think of
    - How to sustain multi-turn
    - How to use differ models (Using Openrouter)

Feedback2
스킵해도되는 세션 제거.
수식을 그대로 가져와서 일일이 설명 필요. 그림은 따로 뽑아내서 그대로 넣는 개선 필요.
내용 반복되는 부분 많음.
일반론적인 내용이 많음.
관련 개념 리프레시는 키워드 기반으로 다시 수행하거나 논문내 주요 개념들 태핑헤야함.
연구자들한테 피드백 받아서 업데이트 필요.

데파 n8n 구현.
실제 사용 경험. 하나 수정하면 워크플로우 다 바꾸어야함. 귀찮음.
한번 그리고 빠르게 이터레이샨 도는게 훨씬 더 정확함. (일하는 방식의 변화)
피쳐리스트 다시 정리 후 필요한 요소만 도출. 가장 중요한 요소만 컨셉 그려냄.

개선 방안 1. 
피드백 반영 방식 중요. 프롬프트 수정.
수정한 프롬프트로 워크플로우 자체 수정.
1-1. 곧바로 프롬프트로 넣을 수는 없음
1-2. 

개선 방안 2. 
관련 논문 가져와서 풍부한 피드백 제공.
블로그 글 등 다른 사람 인사이트도 종합.

