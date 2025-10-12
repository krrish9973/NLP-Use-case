------------------------------------------------------
1. PROJECT OVERVIEW
------------------------------------------------------
This submission contains the complete documentation and code for a resource-constrained Image Classification system. The system implements **Transfer Learning** using the **EfficientNet-B2** architecture to classify images from a subset of the CIFAR-10 dataset. The project focused on achieving high accuracy (Final Accuracy: 87.12%) while strictly adhering to data (<100 MB) and computational time constraints (Total runtime ≈ 745 seconds).

The project successfully delivered a complete pipeline: Conception, Development, Optimization (Finalization), and comprehensive documentation.

------------------------------------------------------
2. FOLDER STRUCTURE & CONTENTS
------------------------------------------------------
The main directory, 'Final', contains the following structure:

/Final
├── Code/
│   └── Image_Classification_System.ipynb    # Main Python code notebook (Jupyter/Colab). Contains data loading, model definition, training loops, optimization (schedulers/fine-tuning), and final evaluation. Also this notebook is also available here: https://github.com/krrish9973/NLP-Use-case/blob/main/Image_Classification_System.ipynb
├── Images/
│   ├── examples/                            # Subfolder for custom image testing.
│   │   └── airplane.png                     # Example image file for single-image prediction testing.
│   └── Use case Diagram and some Screenshots # Visual aids and execution proof.
├── model/
│   └── cifar_10_Image_classification_system.pth # Final trained model weights (PyTorch state_dict file).
├── Abstract.pdf                             # The finalized, two-page project abstract.
├── Conception_phase.pdf                     # Phase 1.2.1: Initial design, rationale, and architecture planning.
├── Development_phase.pdf                    # Phase 1.2.2: Initial results (87.12% accuracy), code development, and runtime documentation.
└── Final_phase.pdf                          # (Placeholder/Report) Document summarizing the final optimization steps and overall project conclusion.

------------------------------------------------------
3. EXECUTION REQUIREMENTS
------------------------------------------------------

**A. Recommended Environment:**
* **Platform:** Google Colab Pro (The environment where the project was executed).
* **Runtime Type:** GPU (CUDA enabled).
* **Specific GPU Used:** NVIDIA A100-SXM4-40GB.
* **CUDA Version:** 12.4
* **Python:** 3.x
* **Driver Version:** 550.54.15

**B. Key Dependencies (Must be installed in the Colab/Jupyter environment):**
* `torch` (PyTorch)
* `torchvision`
* `timm` (PyTorch Image Models)
* `matplotlib`
* `numpy`
* `Pillow` (PIL)

**C. Execution Instructions:**
1.  Upload the contents of the `Final` folder to your execution environment.
2.  Open **`Code/Image_Classification_System.ipynb`**.
3.  Ensure the runtime is set to **GPU**.
4.  The notebook runs sequentially. To test custom images, modify the image path in the dedicated single-image prediction cell to point to an image within the `Images/examples/` subfolder (e.g., `'Images/examples/airplane.jpg'`).

------------------------------------------------------
4. PROJECT PERFORMANCE SUMMARY
------------------------------------------------------
* **Base Model:** EfficientNet-B2 (Pre-trained on ImageNet)
* **Dataset Used:** CIFAR-10 50% Subset (73.3 MB Train Data)
* **Final Achieved Accuracy:** 87.12%
* **Total Training Runtime:** ≈ 745 seconds (on A100 GPU)
* **Methodology:** Transfer Learning (Feature Extraction + Partial Fine-Tuning)
