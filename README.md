A medical imaging web application developed using Deep Learning and Computer Vision. It enables researchers or healthcare professionals to upload brain MRI scans and automatically classify the images into four distinct categories: Pituitary, Glioma, Meningioma, or No Tumor.  The web user interface is crafted with a modern, professional Light Olive Green clinical palette that is exceptionally clean and comfortable for long-term review.  ✨ FeaturesMulti-Class Classification: Detects and distinguishes between three main brain tumor types (Glioma, Meningioma, Pituitary) and healthy scan configurations (No Tumor).  Real-Time Inference: Fast model predictions powered by optimized TensorFlow backend frameworks.  Confidence Metrics: Accompanies classifications with an analytical percentage calculation indicating model certainty.  Elegant Medical UI: Uses a customized theme built on top of responsive Bootstrap 5 foundations for an intuitive UX.  📂 Project StructurePlaintextmri-tumor-detection/
│
├── models/
│   └── model.h5            # Pre-trained CNN/VGG16 deep learning model
│
├── static/
│   └── css/
│       └── style.css       # Custom light olive green clinical style sheet
│
├── templates/
│   └── index.html          # Front-end layout configured with Jinja2 syntax
│
├── app.py                  # Core Flask server application logic
├── requirements.txt        # Frozen package dependencies configuration
└── README.md               # System architectural layout documentation
🛠️ Technical Details & TrainingThe deep learning pipeline utilizes advanced image pre-processing configurations prior to model loading:  Architecture Base: Incorporates a state-of-the-art Deep Convolutional Neural Network architecture built utilizing tensorflow.keras transfer learning options (such as VGG16).  Pre-processing: Images are downsampled to a dimension profile of $128 \times 128$ pixels and normalized down to a floating scale range of $[0.0, 1.0]$ via pixel channel bit division.  Evaluation Samples: The validation loop evaluates explicit unseen test paths against core file names inside the project structure directories. Prominent examples include:  Te-gl_0015.jpg (Glioma case example evaluation)Te-meTr_0001.jpg (Meningioma case example evaluation)Te-noTr_0004.jpg (Normal control scan example evaluation)Te-piTr_0003.jpg (Pituitary case example evaluation)🚀 Installation & Local Environment Setup1. PrerequisitesPython 3.9 up to Python 3.11 environment setups.2. Setup ProcedureClone the codebase repository to your local architecture workstation and change active directories:Bashgit clone https://github.com/your-username/mri-tumor-detection.git
cd mri-tumor-detection
Initialize a local virtual environment mapping partition context to insulate dependency states:Bash# Windows
python -m venv venv
venv\Scripts\activate

# macOS / Linux
python3 -m venv venv
source venv/bin/activate
Install all necessary packages using pip:  Bashpip install -r requirements.txt
3. Launching the ServerExecute the application runner setup using the target python runtime environment wrapper:  Bashpython app.py
Open a modern standard browser web application instance pointing to the localhost address hook:Plaintexthttp://127.0.0.1:5000/
🎨 UI Aesthetics and Style GuideThe user interface avoids traditional corporate blues in favor of an organic, clinical color hierarchy tailored for medical spaces:  Background: Light olive-tinted background hue (#f4f6f4) to lower eye fatigue during continuous screen monitoring sessions.  Headings: Deep forest dark olive tone (#3b4d3b) providing authoritative contrast boundaries.  Primary Interactions: Slate medium-olive color fields (#607d60) changing shade values smoothly via ease transitions during cursor selection hover interactions.  Result Bounding Box: Solid border elements accented by dark forest green color walls (#4c644c) to visually frame positive or negative prediction outputs instantly.  🔒 Safety and Regulatory DisclaimerThis system is a software prototype built for engineering validation and educational demonstration metrics. It has not been validated by the FDA, EMA, or any local health authority. This system must not be used as a stand-alone diagnostic engine for raw clinical patient workflows or alternative critical human therapy pathways. 
