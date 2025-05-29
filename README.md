# 🧠 Brain Tumor Detection using YOLOv11 and SAMv2
This project was completed as part of my internship at Arch Technologies. It leverages YOLOv11 for real-time tumor detection and SAMv2 (Segment Anything Model) for accurate segmentation of brain tumors in MRI images.
## Dataset
https://universe.roboflow.com/brain-tumor-detection-wsera/tumor-detection-ko5jp/dataset/8
# 🚀 Project Steps
## Data Preparation
- MRI images collected and resized.
- Labeled images prepared for YOLOv11 training format.
- Normalization and preprocessing applied for segmentation.
## YOLOv11 Detection
- Model used to detect tumor regions in MRI scans.
- Bounding boxes drawn over detected areas.
## SAMv2 Segmentation
- Cropped regions from YOLOv11 passed to SAMv2.
- Tumor area segmented and visualized using masks.
## Evaluation
- Performance assessed using precision, recall, and intersection-over-union (IoU)./n
- Qualitative results verified via visual outputs.
## How to Run the Project
1. Clone the Repository
git clone https://github.com/SameerMeghjee/Brain-Tumor-Detection.git
cd brain-tumor-detection
2. Create a Virtual Environment
python -m venv venv
source venv/bin/activate  # For Windows: venv\Scripts\activate
3. Install Dependencies
pip install -r requirements.txt
4. Run Detection
python scripts/detect_yolo.py --source data/test_images/ --weights models/yolov11.pt
6. Run Segmentation
python scripts/segment_sam.py --input outputs/detections/ --model models/samv2.pt
## Observations
- YOLOv11 provided fast and reliable tumor localization even on small-sized lesions.
- SAMv2 performed highly accurate segmentation, capturing detailed tumor shapes.
- Combining detection + segmentation enhanced both accuracy and visual interpretability.
- This project demonstrates the power of modern deep learning in medical imaging workflows.
