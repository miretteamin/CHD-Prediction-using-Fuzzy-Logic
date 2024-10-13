# Coronary Heart Disease (CHD) Detection Using Fuzzy Logic

This project uses fuzzy logic to predict the likelihood of an individual developing Coronary Heart Disease (CHD) within 10 years. The model is built using a dataset from the Framingham Heart Study and incorporates expert medical knowledge to create fuzzy logic rules that simulate human decision-making.


## Project Overview:
The project uses fuzzy logic to classify individuals at risk of CHD by analyzing various health metrics. The rules and membership functions are based on expert medical input, making the system flexible and able to handle uncertainty in patient data.

### Features:
- Fuzzy logic implementation from scratch, including fuzzification and defuzzification.
- Knowledge base containing fuzzy sets for health indicators like age, smoking habits, cholesterol levels, and blood pressure.
- Classification system that predicts CHD risk based on input data.

### Data:
The dataset used for this project was obtained from [Kaggle](https://www.kaggle.com/datasets/captainozlem/framingham-chd-preprocessed-data) and includes the following health metrics:
- Age
- Cigarettes smoked per day
- Total cholesterol level
- BMI (Body Mass Index)
- Systolic Blood Pressure
- Ten Year CHD risk (binary output)

### Fuzzy Logic:
Fuzzy logic is a mathematical approach that mimics human decision-making by handling uncertainty and reasoning with "fuzzy" values. Instead of binary true/false values, fuzzy logic uses degrees of truth (values between 0 and 1) to represent real-world conditions. It is particularly useful in this project for determining CHD risk.

### Inputs (Fuzzy Sets):
- **Age**: 
  - Child: (-1, 0, 16, 26)
  - Adult: (18, 28, 42, 50)
  - Old: (45, 50, 79, 80)
  
- **Cigarettes Per Day**: 
  - Normal: (-1, 0, 5, 12)
  - Heavy: (10, 30, 59, 60)
  
- **Total Cholesterol**: 
  - Normal: (-1, 0, 150, 200)
  - Medium: (170, 200, 240)
  - High: (235, 265, 499, 500)

- **BMI**: 
  - Normal: (0, 18, 23)
  - OverWeight: (23, 26, 30)
  - Obese: (30, 40, 59, 60)
  
- **Systolic Blood Pressure (SysBP)**:
  - Normal: (-1, 0, 120, 130)
  - Medium: (125, 135, 160)
  - High: (150, 170, 399, 400)

### Output:
The model predicts the **Ten Year CHD Risk**, which is a binary value (True or False) indicating whether a patient is at risk of developing CHD in the next 10 years.

### Rules:
The system uses 25 fuzzy logic rules based on expert medical input and existing research. These rules determine the level of CHD risk based on the input variables such as BMI, age, cholesterol levels, and smoking habits.

### Example Rules:
- **Rule 1**: If BMI is Normal and Total Cholesterol is Normal and SysBP is Normal and Cigarettes Per Day is Normal, then Ten Year CHD risk is False.
- **Rule 15**: If BMI is Obese or Age is Adult or Total Cholesterol is High or SysBP is High or Cigarettes Per Day is Heavy, then Ten Year CHD risk is True.
