# 🎥 Gaussian Splatting Pipeline for Artists <SNOW-GS>

이 프로젝트는 COLMAP + 2D Gaussian Splatting + Houdini를 통합하여  
아티스트가 사진만으로 인터랙티브 3D 장면을 만들 수 있도록 지원하는 반자동 파이프라인입니다.

---

## 🧩 구성요소

- 📸 COLMAP (Sparse Reconstruction only)
- 🌐 2D Gaussian Splatting (hbb1 버전)
- 🧰 Houdini HDA (Run Pipeline 버튼)
- 🔧 Flask 서버를 통한 Windows ↔ Ubuntu 연결

---

## ⚙️ 설치 방법 (Ubuntu / WSL2)

```bash
git clone https://github.com/yourname/GaussianSplatting-Pipeline.git
cd GaussianSplatting-Pipeline
bash install.sh
