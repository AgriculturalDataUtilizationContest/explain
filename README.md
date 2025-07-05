
![image](https://github.com/user-attachments/assets/0464fe11-d88e-410f-8c8d-1ee5318d76d5)

# 🌾 Reasonable Agri-Price Detector

본 프로젝트는 **KAMIS API**를 기반으로 농산물 가격 데이터를 수집·전처리하고,  
데이터팀이 설계한 계산식을 통해 **합리적인 기준 가격**을 도출하여,  
**실제 시장 가격과의 차이**를 소비자에게 알기 쉽게 전달합니다.  
이는 **농업 공모전을 위한 데이터 기반 문제 해결 프로젝트**입니다.

---

## 📌 개요

- **목표**  
  소비자에게 농산물의 적정 가격 정보를 제공하여 가격 왜곡 인식을 개선하고,  
  데이터 기반의 농산물 유통 환경을 조성합니다.

- **활용 데이터**  
  KAMIS(농산물 유통정보시스템) API로부터 일별 농산물 가격 수집

- **핵심 로직 흐름**  
  데이터 수집 → 전처리 → 기준 가격 계산 → 실제 가격과 비교 → 가격 차이 시각화

---

## 🔧 기술 스택

- **Backend**: Python, FastAPI  
- **Data Processing**: Pandas, PyArrow  
- **API**: KAMIS 농산물유통정보 API  
- **ETL Format**: Parquet  
- **Dev Tools**: Uvicorn

---

## 🚀 실행 방법

```bash
# 1. 가상환경 설정
python -m venv .venv
source .venv/bin/activate  # (Windows는 .venv\Scripts\activate)

# 2. 패키지 설치
pip install -r requirements.txt

# 3. 데이터 수집
python utils/kamis_api.py

# 4. 전처리 및 기준 가격 계산
python postprocessing/compute_reasonable.py

# 5. API 서버 실행
uvicorn main:app --reload
```

---


| 역할          | 이름                |
| ----------- | ----------------- |
| **기획**      | 박예준, 김태희          |
| **디자인**     | 김태희               |
| **데이터 분석**  | 박예준, 박하린, 은수, 허지윤 |
| **프론트엔드**   | 김주한, 한선규          |
| **백엔드/인프라** | 김승환               |
