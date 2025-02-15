# 🏰 Concrete Strength Prediction Using Keras  

## 📌 Overview  
This project explores **neural network experimentation with Keras** to predict **concrete compressive strength** based on its **mix composition and curing age**. Through structured experimentation, we analyze how **normalization, training duration, and model complexity** impact predictive performance.

## ⚙️ Methodology  
### **A. Baseline Model**  
- Built a **feedforward neural network** with **one hidden layer (10 neurons, ReLU activation)**.  
- Used **Adam optimizer** and **Mean Squared Error (MSE) loss function**.  
- Trained for **50 epochs** on a **random 70-30 train-test split**.  
- Repeated the process **50 times** and reported **mean & standard deviation of MSE**.

### **B. Normalization**  
- Standardized features using **z-score normalization** to improve stability.  
- Re-ran the **baseline model** and compared MSE results.  

### **C. Increasing Epochs**  
- Increased training duration from **50 to 100 epochs** to observe performance gains.  
- Evaluated how extended training affects accuracy and variability.  

### **D. Increasing Hidden Layers**  
- Expanded model architecture to **three hidden layers** (each with **10 neurons, ReLU activation**).  
- Analyzed whether deeper networks improve generalization.  

## 📊 Key Findings  
| **Experiment** | **Mean MSE** | **Std Dev** | **Key Insight** |
|---------------|------------|------------|----------------------|
| **Baseline (50 epochs, 1 layer, raw data)** | 168.07 | 241.92 | High error & unstable training |
| **Normalized Data (50 epochs, 1 layer)** | 130.28 | 11.18 | Normalization improved stability |
| **Normalized Data (100 epochs, 1 layer)** | 79.09 | 15.94 | More training improved accuracy |
| **Normalized Data (50 epochs, 3 layers)** | 85.55 | 23.58 | More layers didn’t help, increased instability |

## 🚀 Conclusion  
- **Normalization significantly stabilized training** and should be applied before training.  
- **Increasing epochs improved performance** by reducing MSE, proving that the model needed more training.  
- **Adding more hidden layers didn’t enhance accuracy** and introduced instability, suggesting that a **deeper model wasn’t necessary** for this task.  

## 🔗 Dependencies  
- Python 3.x  
- TensorFlow/Keras  
- NumPy, Pandas, Scikit-learn  
- Matplotlib (for visualization)  

## 📂 How to Run  
Clone the repository and install dependencies:  
```bash
git clone https://github.com/viukpe/concrete-strength-keras.git
cd <repo-name>
pip install -r requirements.txt
```
Run the Jupyter Notebook:  
```bash
jupyter notebook
```

## 🐟 License  
This project is open-source and available under the MIT License.
