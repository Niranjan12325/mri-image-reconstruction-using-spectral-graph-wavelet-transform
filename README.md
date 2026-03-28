
#  MRI Reconstruction using Spectral Graph Wavelet Transform (SGWT)

##  Overview
This project implements an advanced MRI image reconstruction pipeline using Spectral Graph Wavelet Transform (SGWT) and Compressed Sensing techniques. It reconstructs high-quality MRI images from undersampled k-space data, improving efficiency and reducing scan time.

---

##  Features
- Load MRI k-space data from `.h5` files  
- Multiple undersampling strategies:
  - Cartesian  
  - Radial  
  - Random  
  - Variable Density  
- Graph-based signal processing using Laplacian  
- Spectral Graph Wavelet Transform (SGWT)  
- Reconstruction using pFISTA algorithm  
- Gibbs artifact removal  
- Evaluation metrics:
  - PSNR  
  - SSIM  
  - RMSE  
  - RLNE  
- Visualization of results  

---

##  Technologies Used
- Python  
- NumPy  
- SciPy  
- Scikit-learn  
- scikit-image  
- Matplotlib  
- h5py  

---

##  Project Structure
project/
│── main.py
│── data/
│ └── sample.h5
│── README.md

## ⚙️ Installation

Install required dependencies:

## bash
pip install numpy scipy scikit-learn scikit-image matplotlib h5py
 Usage

## Run the main script:

python main.py

Or modify parameters inside:

main(
    h5_file='your_file.h5',
    rate=0.5,
    mask_type='radial',
    slice_idx=7,
    iterations=200
)
##  Pipeline Workflow
 - Load Data
 - Preprocessing (Normalization + FFT/IFFT)
 - Undersampling using masks
 - Graph Laplacian construction
 - Spectral Graph Wavelet Transform
 - Reconstruction using pFISTA
 - Post-processing (artifact removal)
 - Evaluation (PSNR, SSIM, RMSE, RLNE)
 - Visualization
  
## Output
  - Ground truth image
  - Undersampled image
  - Reconstructed image
  - Sampling mask
  - Quality metrics
  - Example Metrics
  - PSNR: Higher is better
  - SSIM: Closer to 1 is better
  - RMSE: Lower is better
  - RLNE: Lower is better

## Key Algorithms
- Spectral Graph Wavelet Transform (SGWT)
- Chebyshev Polynomial Approximation
- Projected Fast Iterative Soft Thresholding Algorithm (pFISTA)

## Future Improvements
- Deep learning-based reconstruction (CNN / U-Net)
- Performance optimization
- Multi-coil enhancements
- Web or GUI interface

## Author
Niranjan E

## License
This project is for academic and research purposes.
