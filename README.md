# more_image_clear2602  

SwinIR 기반 위성영상 이미지 고도화  

AI Super-Resolution 기술인 SwinIR을 활용하여 위성영상 이미지를 보다 더 선명하게 만들 수 있습니다. 

🌟 Key Features

SwinIR-M x4 GAN Model: 최신 Vision Transformer 기반의 SwinIR 모델을 사용하여 단순 확장이 아닌, 픽셀 단위의 디테일을 복원합니다.  

Hardware Optimization: GTX 시리즈 등 보급형 GPU에서도 안정적으로 구동되도록 메모리 캐시 정리 및 스케줄링 로직이 포함되어 있습니다.  

📊 Result (Before & After)

원본: 아스팔트 차선 및 건물 옥상 구조물 뭉개짐 발생

결과: AI가 텍스처를 복원하여 선명한 에지(Edge)와 실사급 질감 확보

🚀 Performance Benchmark

4~5년 전 출시된 GTX 노트북(GTX 1650급) 환경에서의 성능 테스트 결과입니다.

Device

Average Time per Tile

Speedup

CPU (i7-9th Gen)

23.40s

1.0x

GPU (GTX CUDA)

2.73s (Pure Compute)

8.5x


🛠️ Installation & Usage

Prerequisites

Python 3.11+

CUDA 지원 NVIDIA GPU (권장) 및 최신 드라이버

Setup

######## CUDA 12.1 버전용 PyTorch 설치  
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
pip install timm opencv-python matplotlib tqdm requests


📂 Directory Structure

.
├── models/               # SwinIR Network 정의
├── upscale01.ipynb   # 메인 코드
└── 003_realSR_..._GAN.pth # AI 모델 가중치 파일


📜 License

저는 라이선스를 따지지 않으나, SwinIR(https://github.com/JingyunLiang/SwinIR) 및 영상 이미지 데이터의 라이선스 등을 확인하시기 바랍니다. 
