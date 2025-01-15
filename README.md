# capstone_3_hotel_booking_demand
# Hotel Booking Demand Prediction

## Overview
This project aims to predict hotel reservation cancellations to improve operational efficiency and optimize revenue. The analysis addresses class imbalance issues using XGBoost with ADASYN and focuses on minimizing false negatives and false positives to ensure smooth hotel operations.

## Repository Structure
```
CAPSTONE3Hotel_booking_demand.ipynb   # Jupyter Notebook containing the analysis and model-building process.
data_hotel_booking_demand.csv         # Dataset used for analysis and modeling.
final_model.pkl                       # Serialized file of the trained model.
README.md                             # Project documentation.
```

## Key Features
- **Exploratory Data Analysis (EDA):** Understanding the data distribution, identifying trends, and addressing missing values.
- **Preprocessing:** Includes feature engineering, encoding categorical variables, and scaling numerical features.
- **Handling Imbalanced Data:** Applied ADASYN to balance the dataset.
- **Model Selection:** XGBoost was chosen for its robustness and performance.
- **Evaluation:** Metrics like precision, recall, F1-score, and confusion matrix were used to evaluate model performance.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo-name/capstone_3_hotel_booking_demand.git
   ```
2. Navigate to the project directory:
   ```bash
   cd capstone_3_hotel_booking_demand
   ```
3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage
1. Open the Jupyter Notebook to explore the analysis and modeling process:
   ```bash
   jupyter notebook CAPSTONE3Hotel_booking_demand.ipynb
   ```
2. Load the dataset `data_hotel_booking_demand.csv` for predictions.
3. Use the pre-trained model `final_model.pkl` for making predictions:
   ```python
   import pickle
   import pandas as pd

   # Load the model
   with open('final_model.pkl', 'rb') as file:
       model = pickle.load(file)

   # Prepare your data (example format)
   data = pd.read_csv('data_hotel_booking_demand.csv')
   predictions = model.predict(data)
   print(predictions)
   ```

## Results
The final model achieved the following:
- **Precision:** 0,85%
- **Recall:** 0,75%
- **F1-Score:** 0,73%
- Reduced false positives and negatives, enabling more accurate hotel demand predictions.

## Contributing
If you'd like to contribute to the project, feel free to open a pull request or raise an issue for discussion.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

