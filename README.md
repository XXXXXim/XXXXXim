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

▶ **[라이브 데모](https://v-match-one.vercel.app/login)** — 로그인 화면의 데모 계정 버튼으로 바로 체험할 수 있습니다.

- FIT 점수는 규칙 기반으로 계산하고, LLM은 계산된 점수와 근거를 받아 실사 리포트 서술만 씁니다.
- 매칭 + NDA 동의 전에는 IR 원본이 열리지 않도록 권한을 나눴고, 보안 결함은 **테스트로 먼저 재현한 뒤** 고쳤습니다.
- API 키가 없어도 템플릿 폴백으로 동작해 데모가 깨지지 않습니다.

`Django REST Framework` `Vue 3` `Pinia` `OpenAI` `Anthropic`

### [SKALA 4기 학습 포트폴리오](https://github.com/XXXXXim/skala-portfolio)
과목 23개의 실습과 결과물 정리 — Java·Spring Boot, MSA, ML·DL, sLLM 파인튜닝, LangChain, Spring AI, Kubernetes(EKS), 모델 서빙(KServe·vLLM·MLflow)

---

## 기술 스택

<table>
  <tr><td align="center"><b>언어</b></td><td><img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/> <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java"/> <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript"/></td></tr>
  <tr><td align="center"><b>AI · LLM</b></td><td><img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=for-the-badge&logo=langgraph&logoColor=white" alt="LangGraph"/> <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white" alt="LangChain"/> <img src="https://img.shields.io/badge/OpenAI%20API-412991?style=for-the-badge" alt="OpenAI API"/> <img src="https://img.shields.io/badge/Claude%20API-D97757?style=for-the-badge&logo=claude&logoColor=white" alt="Claude API"/> <img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" alt="Hugging Face"/> <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" alt="PyTorch"/> <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white" alt="TensorFlow"/> <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white" alt="scikit-learn"/></td></tr>
  <tr><td align="center"><b>RAG · 검색</b></td><td><img src="https://img.shields.io/badge/FAISS-0467DF?style=for-the-badge" alt="FAISS"/> <img src="https://img.shields.io/badge/Qdrant-DC244C?style=for-the-badge&logo=qdrant&logoColor=white" alt="Qdrant"/> <img src="https://img.shields.io/badge/ChromaDB-FF6446?style=for-the-badge" alt="ChromaDB"/> <img src="https://img.shields.io/badge/BM25%20%2B%20Reranker-6E40C9?style=for-the-badge" alt="BM25 + Reranker"/> <img src="https://img.shields.io/badge/RAGAS-2D3748?style=for-the-badge" alt="RAGAS"/></td></tr>
  <tr><td align="center"><b>데이터</b></td><td><img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas"/> <img src="https://img.shields.io/badge/Polars-0075FF?style=for-the-badge&logo=polars&logoColor=white" alt="Polars"/> <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy"/> <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter"/></td></tr>
  <tr><td align="center"><b>백엔드</b></td><td><img src="https://img.shields.io/badge/Django%20REST-092E20?style=for-the-badge&logo=django&logoColor=white" alt="Django REST"/> <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI"/> <img src="https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" alt="Spring Boot"/> <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" alt="Streamlit"/> <img src="https://img.shields.io/badge/pytest-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white" alt="pytest"/></td></tr>
  <tr><td align="center"><b>프론트엔드</b></td><td><img src="https://img.shields.io/badge/Vue%203-4FC08D?style=for-the-badge&logo=vuedotjs&logoColor=white" alt="Vue 3"/> <img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white" alt="Vite"/> <img src="https://img.shields.io/badge/Pinia-FFD859?style=for-the-badge&logo=pinia&logoColor=black" alt="Pinia"/> <img src="https://img.shields.io/badge/Bootstrap-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white" alt="Bootstrap"/></td></tr>
  <tr><td align="center"><b>DB</b></td><td><img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL"/> <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL"/> <img src="https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white" alt="SQLite"/></td></tr>
  <tr><td align="center"><b>인프라 · MLOps</b></td><td><img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker"/> <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" alt="Kubernetes"/> <img src="https://img.shields.io/badge/AWS%20EKS-FF9900?style=for-the-badge" alt="AWS EKS"/> <img src="https://img.shields.io/badge/vLLM-30A2FF?style=for-the-badge&logo=vllm&logoColor=white" alt="vLLM"/> <img src="https://img.shields.io/badge/MLflow-0194E2?style=for-the-badge&logo=mlflow&logoColor=white" alt="MLflow"/> <img src="https://img.shields.io/badge/Airflow-017CEE?style=for-the-badge&logo=apacheairflow&logoColor=white" alt="Airflow"/> <img src="https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white" alt="Prometheus"/> <img src="https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white" alt="Grafana"/></td></tr>
  <tr><td align="center"><b>배포 · 도구</b></td><td><img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" alt="GitHub Actions"/> <img src="https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Vercel"/> <img src="https://img.shields.io/badge/Neon-00E599?style=for-the-badge&logo=neon&logoColor=black" alt="Neon"/> <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git"/> <img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white" alt="Postman"/></td></tr>
</table>

## 이력

- **SK AX SKALA 4기** · AI Agent·RAG·Cloud 과정 (2026)
- **SSAFY** 1학기 수료 (2026)

---

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=XXXXXim&show_icons=true&locale=kr&theme=tokyonight&hide_border=true&border_radius=12" height="165" alt="GitHub 통계"/>
<img src="https://github-readme-stats.vercel.app/api/top-langs?username=XXXXXim&layout=compact&locale=kr&theme=tokyonight&hide_border=true&border_radius=12" height="165" alt="자주 쓰는 언어"/>

<img src="https://github-readme-streak-stats.herokuapp.com/?user=XXXXXim&theme=tokyonight&hide_border=true&locale=ko" alt="연속 기록"/>

</div>
