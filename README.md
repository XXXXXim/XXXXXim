# 심혁 · Sim Hyeok

**믿을 수 있는 AI 서비스를 만드는 개발자입니다.**
경영학을 전공했고, SSAFY를 수료한 뒤 SK AX SKALA 4기에서 AI Agent·RAG·클라우드를 배우고 있습니다.

> 제 원칙은 하나입니다. **측정하고, 한 번에 하나씩 바꾸고, 숫자로 증명한다.**
> 틀리면 안 되는 숫자는 LLM이 아니라 코드가 계산하고, LLM은 근거가 있는 말만 하게 만듭니다.

---

## 대표 프로젝트

### [Robotics Startup Investment Agent](https://github.com/XXXXXim/robotics-startup-investment-agent)
**DART 감사보고서로 비상장 로보틱스 스타트업 투자 검토 보고서를 쓰는 LangGraph Supervisor 멀티 에이전트**

- Supervisor가 "근거가 충분한가"를 판단하고, 부족한 관점만 골라 담당 에이전트에게 다시 조사시킵니다.
- 재무 계정 추출·성장률·현금 소진 기간·스코어카드 가중합은 **코드가 계산**하고, LLM은 1~5점 판정과 서술만 합니다.
- 규칙 검사 + LLM Judge 품질 평가 루프, 반복 상한을 코드로 강제해 종료를 보장합니다.
- 실제 기업 2곳(브이디컴퍼니·트위니)을 OpenDART 원문으로 실행해 보고서 PDF를 만들었습니다.

`LangGraph` `OpenAI` `ChromaDB` `OpenDART` `LangSmith` `pytest`

### [AI·반도체 정책 리포트 RAG](https://github.com/XXXXXim/vectordb-rag)
**Dense → Hybrid(BM25 + RRF) → Rerank로 검색 방식을 바꿔 가며 품질을 수치로 비교한 RAG**

- 보고서 16개(약 860쪽)를 BGE-M3로 임베딩하고 FAISS·Qdrant로 검색합니다.
- Reranker를 붙여 **Context Precision 0.72 → 0.91, 근거 청크 적중률 68% → 86%** (RAGAS 평가).
- 한국어에서는 기본값이 통하지 않았습니다. 공백 토큰화 BM25를 한글 bigram으로 바꿔 **P@5 0.65 → 0.80**.

`BGE-M3` `FAISS` `Qdrant` `BM25` `BGE-Reranker` `RAGAS`

### [V-Match](https://github.com/XXXXXim/v-match)
**VC와 스타트업을 양방향으로 연결하는 AI 투자 매칭 플랫폼** · 2인 팀

- FIT 점수는 규칙 기반으로 계산하고, LLM은 계산된 점수와 근거를 받아 실사 리포트 서술만 씁니다.
- 매칭 + NDA 동의 전에는 IR 원본이 열리지 않도록 권한을 나눴고, 보안 결함은 **테스트로 먼저 재현한 뒤** 고쳤습니다.
- API 키가 없어도 템플릿 폴백으로 동작해 데모가 깨지지 않습니다.

`Django REST Framework` `Vue 3` `Pinia` `OpenAI` `Anthropic`

### [SKALA 4기 학습 포트폴리오](https://github.com/XXXXXim/skala-portfolio)
과목 23개의 실습과 결과물 정리 — Java·Spring Boot, MSA, ML·DL, sLLM 파인튜닝, LangChain, Spring AI, Kubernetes(EKS), 모델 서빙(KServe·vLLM·MLflow)

---

## 기술 스택

<p align="left"> <a href="https://getbootstrap.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/bootstrap/bootstrap-plain-wordmark.svg" alt="bootstrap" width="40" height="40"/> </a> <a href="https://www.w3schools.com/css/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="css3" width="40" height="40"/> </a> <a href="https://www.djangoproject.com/" target="_blank" rel="noreferrer"> <img src="https://cdn.worldvectorlogo.com/logos/django.svg" alt="django" width="40" height="40"/> </a> <a href="https://www.docker.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original-wordmark.svg" alt="docker" width="40" height="40"/> </a> <a href="https://git-scm.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="40" height="40"/> </a> <a href="https://www.w3.org/html/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="html5" width="40" height="40"/> </a> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="javascript" width="40" height="40"/> </a> <a href="https://kubernetes.io" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/kubernetes/kubernetes-icon.svg" alt="kubernetes" width="40" height="40"/> </a> <a href="https://www.mysql.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" alt="mysql" width="40" height="40"/> </a> <a href="https://nodejs.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg" alt="nodejs" width="40" height="40"/> </a> <a href="https://pandas.pydata.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/2ae2a900d2f041da66e950e4d48052658d850630/icons/pandas/pandas-original.svg" alt="pandas" width="40" height="40"/> </a> <a href="https://www.postgresql.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original-wordmark.svg" alt="postgresql" width="40" height="40"/> </a> <a href="https://postman.com" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/getpostman/getpostman-icon.svg" alt="postman" width="40" height="40"/> </a> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> <a href="https://pytorch.org/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/pytorch/pytorch-icon.svg" alt="pytorch" width="40" height="40"/> </a> <a href="https://scikit-learn.org/" target="_blank" rel="noreferrer"> <img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" alt="scikit_learn" width="40" height="40"/> </a> <a href="https://seaborn.pydata.org/" target="_blank" rel="noreferrer"> <img src="https://seaborn.pydata.org/_images/logo-mark-lightbg.svg" alt="seaborn" width="40" height="40"/> </a> <a href="https://www.sqlite.org/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/sqlite/sqlite-icon.svg" alt="sqlite" width="40" height="40"/> </a> <a href="https://www.tensorflow.org" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/tensorflow/tensorflow-icon.svg" alt="tensorflow" width="40" height="40"/> </a> <a href="https://vuejs.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/vuejs/vuejs-original-wordmark.svg" alt="vuejs" width="40" height="40"/> </a> </p>

| 분야 | 사용해 본 것 |
|---|---|
| AI · LLM | LangGraph, LangChain, OpenAI·Anthropic API, RAG, RAGAS, Hugging Face, PyTorch |
| 검색 | FAISS, Qdrant, ChromaDB, BM25, Reranker |
| 백엔드 | Python, Django REST Framework, FastAPI, Java, Spring Boot, Spring AI |
| 프론트엔드 | Vue 3, Vite, Pinia |
| 데이터 | Pandas, scikit-learn, SQL (MySQL·PostgreSQL) |
| 인프라 | Docker, Kubernetes (AWS EKS), KServe, vLLM, MLflow, Airflow, GitHub Actions |

## 이력

- **SK AX SKALA 4기** · AI Agent·RAG·Cloud 과정 (2026)
- **SSAFY** 1학기 수료 (2026)

---

<p><img align="left" src="https://github-readme-stats.vercel.app/api/top-langs?username=xxxxxim&show_icons=true&locale=en&layout=compact" alt="xxxxxim" /></p>

<p>&nbsp;<img align="center" src="https://github-readme-stats.vercel.app/api?username=xxxxxim&show_icons=true&locale=en" alt="xxxxxim" /></p>

<p><img align="center" src="https://github-readme-streak-stats.herokuapp.com/?user=xxxxxim&" alt="xxxxxim" /></p>
