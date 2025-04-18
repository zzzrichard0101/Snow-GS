# 🌍 Automatic Gravity Estimation System for Gaussian Splatting

본 프로젝트는 사진 기반 3D 재구성(Gaussian Splatting) 이후,  
Mesh 기반 PCA 분석을 통해 중력 방향을 자동으로 추정하고,  
Houdini에서 바로 시뮬레이션까지 연결되는 **아티스트 친화적인 파이프라인**을 제공합니다.

---

## 🔧 Features

- 📸 **COLMAP** 기반 구조 재구성 (SfM)
- 🌌 **2D Gaussian Splatting** 학습 자동화
- 📈 **PCA 기반 중력 방향 추정**
- 🧩 **Houdini HDA** 연동 (버튼 한 번으로 전체 파이프라인 실행)
- 🌐 **Flask 서버**로 외부 Python ↔ Houdini 통신
- 📁 **Windows ↔ Ubuntu 공유 폴더 연동**

---


## 📁 Project Structure

your_project/
│

├── houdini/                            # 🎨 Houdini 디지털 에셋 및 내부 스크립트
│   ├── RunPipelineHDA.hda              # HDA 디지털 에셋
│   └── scripts/
│       └── gaussian_normal.py          # PCA 기반 중력 추정 스크립트 (HDA 내부에서 실행됨)

│
├── interface/                          # 🔌 Houdini → 외부 Flask 서버 요청용
│   └── run_pipeline_button.py          # HDA 버튼에서 Flask 서버로 HTTP 요청 보내기
│
├── pipeline/                           # 🔁 COLMAP + Gaussian Splatting 실행 로직
│   └── run_pipeline.py                 # 전체 파이프라인 (SfM → 학습 → 결과 저장)
│
├── server/                             # 🌐 Flask 서버
│   └── server.py                       # 파이프라인 요청 처리 API (POST /run 등)
│
├── shared/                             # 📂 Windows ↔ Ubuntu 공유 폴더
│   └── (예: C:/wsl-shared/)            # Gaussian 결과 저장 위치
│
├── setup/                              # ⚙️ 자동 설치 스크립트 모음
│   ├── install_conda_env.sh            # Conda 환경 생성 및 패키지 설치
│   ├── install_colmap.sh               # COLMAP 소스 빌드 및 설치
│   ├── install_2dgs.sh                 # 2D Gaussian Splatting 환경 설정
│   └── README.md                       # 설치 스크립트별 설명 문서
│
└── README.md                           # 📘 프로젝트 메인 설명 문서
