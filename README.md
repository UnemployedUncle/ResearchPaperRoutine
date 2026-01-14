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

## Version 3

1. Prompt Change
- Extraction of the graph, table
- Remove duplications, too much general answers
- Refresh concepts should be map with methodologies or keywords
- Related papers should be searched
- Want to know the opinion of other people
- Future work is too much disconnected

2. Add OpenRouter with BasicLLM
https://openrouter.ai/compare
https://lmarena.ai/ko/leaderboard

3. Set Agents
  - Web search
  - Chat Model

| Agent    | Model | Tool | Structured Output | Fallback |
| -------- | ----- | ---- | ----------------- | -------- |
| Meta         | gpt-4.1-mini  | - | json | openrouter |
| ImageExtraction | gpt-4o-mini | Web Search, SerpAPI | json | openrouter |
| Reading Map  | gpt-4.1-mini  | - | - | openrouter |
| Why          | gpt-4o-mini | Web Search, SerpAPI | - | openrouter |
| Methodology  | gpt-4o-mini | Web Search, SerpAPI | - | openrouter |
| Deep Dive    | gpt-4o-mini | Web Search, SerpAPI | - | openrouter |
| Results      | gpt-4.1-mini | - | - | openrouter |
| Limitation   | gpt-4.1-mini  | - | - | openrouter |
| Continuation | gpt-4o-mini | Web Search, SerpAPI | - | openrouter |
| Takeaway     | gpt-4.1-mini  | - | - | openrouter |

Version 4?
* Need researchers feedback
* Cannot give feedback loop on the prompt (n8n limitations)
* Change to code on version 4
* How about just translation with extra explanations

Not runnning!
