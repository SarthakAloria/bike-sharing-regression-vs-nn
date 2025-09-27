
![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python&logoColor=white)![Dataset](https://img.shields.io/badge/Dataset-Seoul%20Bike%20Sharing-green)![Models](https://img.shields.io/badge/Models-Regression%20%26%20Neural%20Networks-red)

# Bike Demand Prediction: Regression vs Neural Networks

## Project Description

This project predicts bike rental demand in Seoul using the  
**[Seoul Bike Sharing Dataset (UCI Machine Learning Repository)](https://archive.ics.uci.edu/ml/datasets/Seoul+Bike+Sharing+Demand)**.  
It compares **Linear Regression** (single & multi-variable) with **Neural Networks**,  
highlighting when simple models work well and when deep learning provides advantages.  



**Key Details:**
- **Goal:** Demand forecasting for bike rentals in Seoul  
- **Dataset:** [Seoul Bike Sharing (UCI ML Repository)](https://archive.ics.uci.edu/ml/datasets/Seoul+Bike+Sharing+Demand)  
- **Focus Variable:** Temperature (baseline) + all features  
- **Methods:** Linear Regression, Multi-Regression, Neural Networks  
- **Evaluation:** Loss curves, accuracy, prediction vs actual plots  

---
## Table of Contents

- [Project Description](#project-description)
- [Features](#features)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Results](#results)
- [Visualizations](#visualizations)
- [Conclusion](#conclusion)
- [Tech Stack](#tech-stack)
- [Contributing](#contributing)
- [Authors](#authors)
- [Acknowledgement](#acknowledgement)
- [Support](#support)

---
## Features

The dataset includes the following key features used for modeling:

- **Temperature (°C)** — average temperature
- **Humidity (%)** — relative humidity
- **Wind speed (m/s)** — wind conditions
- **Visibility (10m)** — how clear the weather was
- **Dew point temperature (°C)** — atmospheric moisture indicator
- **Solar radiation (MJ/m²)** — sunlight intensity
- **Rainfall (mm)** — precipitation
- **Snowfall (cm)** — snow depth
- **Seasons** — Spring, Summer, Fall, Winter
- **Holiday** — whether the day was a holiday
- **Functioning Day** — whether the bike service was active


---
## Dataset

This project uses the **[Seoul Bike Sharing Dataset](https://archive.ics.uci.edu/ml/datasets/Seoul+Bike+Sharing+Demand)** from the UCI Machine Learning Repository.  

**Key points:**
- Contains **hourly bike rental data** along with weather and seasonal information.
- Includes features such as temperature, humidity, wind speed, visibility, dew point, solar radiation, rainfall, snowfall, seasons, holidays, and whether the bike service was active.
- **Target variable:** `Rented Bike Count` — the number of bikes rented each hour.  

The dataset is used to predict hourly bike rental demand and evaluate model performance.

---
## Methodology


The goal is to predict Seoul bike rental demand using different modeling approaches. The following methods were applied:

### 📈 Linear Regression
- Modeled the relationship between the target (`Rented Bike Count`) and a single feature (Temperature).
- Evaluated how well a simple linear model captures the demand trend.

### 🤖 Multiple Regression
- Used multiple features from the dataset (temperature, humidity, wind speed, etc.) as predictors.
- Evaluated improvements over single-variable linear regression.

### 🧠 Neural Networks
- Feedforward Neural Network applied to both single-feature and multi-feature inputs.
- Trained to minimize prediction error (MSE/MAE) with appropriate loss functions.
- Compared performance against linear models using plots and metrics (loss, accuracy).

Each method’s results were visualized and compared to assess how model complexity affects prediction quality.

---
## Results

The models were evaluated and compared using both visualizations and metrics (loss, accuracy, prediction vs actual counts).  

### Baseline: Temperature-only Linear Regression
- Predicted bike rentals using only temperature.
- Serves as a simple baseline to compare model performance.

### Linear Regression vs Neural Network Comparison
- Plotted predictions from both Linear Regression and Neural Network on the same graph.
- Evaluated how neural networks handle non-linear patterns better than linear models.

### Neural Network with All Features
- Trained on all available features from the dataset.
- Monitored training and validation loss/accuracy to check for overfitting.

### Key Observations
- Single-variable linear regression works reasonably for simple trends.
- Neural networks improve predictions, especially when multiple features are included.
- Training vs validation curves help identify overfitting and model performance.

---
## Visualizations

The following visualizations show the performance and predictions of the models:

### Linear Regression vs Neural Network
- Comparison of predicted vs actual bike rentals for single-variable and multi-variable models.  
![Linear vs NN](/model_curve_img/linear_reg_vs_nn.png)

### Linear Regression (Temperature-only)
- Baseline linear regression using only temperature as input.  
![Linear Temp Only](/model_curve_img/linear_temp_only.png)

### Neural Network Predictions (Temperature-only)
- Neural network predictions using only temperature.  
![NN Temp Only](/model_curve_img/nn_temp_only.png)

### Neural Network Predictions (All Features)
- Training and validation loss/accuracy for the neural network trained on all features.  
![NN All Features Train/Val](/model_curve_img/nn_all_val_loss.png)

### Optional: Neural Network (Temperature-only Train/Val)
- Training and validation curves for temperature-only neural network.  
![NN Temp Train/Val](/model_curve_img/nn_temp_val_loss.png)

---
## Conclusion

- **Key Takeaways:**  
  - Linear Regression works well for simple trends and provides a quick baseline.  
  - Neural Networks outperform linear models when multiple features or non-linear patterns are involved.  
  - Using all relevant features improves prediction accuracy, but care must be taken to monitor overfitting using training vs validation curves.  

- **Insights:**  
  - Single-variable models (temperature-only) are useful for quick analysis.  
  - Deep learning models (NNs) provide more flexibility and can capture complex relationships in the dataset.  
  - Visualizations help in understanding model behavior and identifying areas for improvement.

---
## Tech Stack

- **Programming Language:** Python 3.x  
- **Data Analysis & Visualization:** Pandas, NumPy, Matplotlib, Seaborn  
- **Machine Learning & Deep Learning:** Scikit-learn, TensorFlow / Keras  
- **Development Environment:** Jupyter Notebook  
- **Version Control:** Git, GitHub  
- **Dataset:** [Seoul Bike Sharing Dataset (UCI ML Repository)](https://archive.ics.uci.edu/ml/datasets/Seoul+Bike+Sharing+Demand)

---
## Contributing

Contributions are welcome! Whether it’s **improving model performance, adding new algorithms, optimizing data preprocessing, or enhancing visualizations**, you can help improve this project.

### How to Contribute

1. **Fork the repository**  
2. **Clone your fork** locally:
```bash
git clone https://github.com/SarthakAloria/bike-sharing-regression-vs-nn.git
```
3. **Create a new branch for your feature or bugfix:**
```bash
git checkout -b feature/your-feature-name
```
4. **Make your changes (e.g., add new models, improve preprocessing, add visualizations)**
5. **Commit your changes:**
```bash
git commit -m "Add: brief description of changes"
```
6. **Push your branch:**
```bash
git push origin feature/your-feature-name
```
7. **Open a Pull Request on the main repository.**

---
## Authors

- **Sarthak Aloria** – [SarthakAloria](https://github.com/SarthakAloria)


---
## Acknowledgement

- **UCI Machine Learning Repository** – for providing the [Seoul Bike Sharing Dataset](https://archive.ics.uci.edu/ml/datasets/Seoul+Bike+Sharing+Demand).  
- **Scikit-learn, TensorFlow, Keras, Pandas, NumPy, Matplotlib, Seaborn** – for the amazing tools and libraries that made analysis and modeling easy.  
- **Open-source community** – for tutorials, guidance, and code examples that helped in learning and implementing machine learning models.  

---
## Support

For any issues or feature requests, please open an issue on GitHub or contact me at sarthakaloria27@gmail.com.

---