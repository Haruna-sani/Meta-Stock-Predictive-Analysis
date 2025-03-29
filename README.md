# Meta Stock Predictive Analysis  

## Overview  
This project focuses on the predictive analysis of Meta's stock prices using deep learning models. We implemented three different deep learning architectures to evaluate their performance in stock price forecasting:  

- **LSTM (Long Short-Term Memory)**
- **CNN + Bi-LSTM (Convolutional Neural Network + Bidirectional LSTM)**
- **CNN + GRU-LSTM (Convolutional Neural Network + Gated Recurrent Unit + LSTM)**  

Each model was trained using four different learning rates (0.00001, 0.0001, 0.001, 0.01) to assess their impact on predictive accuracy. The performance was measured using the **R-squared (R²) metric** to determine how well the models captured stock price movements.  

## Model Performance  

| Model | 0.00001 | 0.0001 | 0.001 | 0.01 |
|--------|---------|--------|------|------|
| **LSTM** | 0.986 | 0.993 | 0.994 | 0.993 |
| **CNN + GRU-LSTM** | 0.984 | 0.993 | 0.992 | 0.994 |
| **CNN + Bi-LSTM** | 0.983 | 0.992 | 0.992 | 0.993 |

## Comparative Analysis  

### **LSTM vs Hybrid Models (CNN+GRU-LSTM & CNN+Bi-LSTM)**  
1. **Predictive Accuracy**  
   - LSTM performed exceptionally well, achieving an **R² score of up to 0.994**, showing its ability to capture long-term dependencies.  
   - CNN+GRU-LSTM and CNN+Bi-LSTM models showed slightly **lower variance across different learning rates**, making them more stable.  

2. **Feature Extraction**  
   - The **CNN layers** in hybrid models helped in capturing local patterns in stock price trends, which improved feature extraction before feeding into recurrent layers.  
   - The **GRU component** in CNN+GRU-LSTM reduced computational complexity compared to LSTM, making it more efficient while maintaining high accuracy.  

3. **Generalization**  
   - The **LSTM model alone** showed the highest peak accuracy but also had **more sensitivity to learning rates**.  
   - The hybrid models (CNN+GRU-LSTM, CNN+Bi-LSTM) provided a **more balanced performance** across all learning rates, suggesting better generalization.  

### **Conclusion**  
- **LSTM remains a strong performer** but is highly dependent on optimal hyperparameter tuning.  
- **CNN+GRU-LSTM provides a balance between efficiency and accuracy**, making it suitable for real-time stock prediction.  
- **CNN+Bi-LSTM offers bidirectional learning advantages** but does not significantly outperform CNN+GRU-LSTM.  
