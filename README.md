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

your_project/ │ ├── houdini/
│ ├── RunPipelineHDA.hda # Houdini 디지털 에셋 │ └── scripts/ │ └── gaussian_normal.py # PCA 기반 중력 추정 Python │ ├── interface/
│ └── run_pipeline_button.py # HDA 버튼 → Flask 요청 │ ├── pipeline/
│ └── run_pipeline.py # COLMAP + 2DGS 전체 실행 │ ├── server/
│ └── server.py # Flask 서버 │ ├── shared/
│ └── (WSL ↔ Windows 공유 폴더) │ ├── setup/
│ ├── install_conda_env.sh # Conda 환경 설치 │ ├── install_colmap.sh # COLMAP 소스 설치 │ ├── install_2dgs.sh # 2DGS 설치 │ └── README.md │ └── README.md # ←
