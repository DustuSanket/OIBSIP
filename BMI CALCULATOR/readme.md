# BMI Calculator

## Description
The BMI (Body Mass Index) Calculator is a simple tool to calculate the BMI of an individual based on their weight and height. This project demonstrates the use of basic programming concepts and user interface design to create a functional health-related application.

## Features
- Input fields for weight (kg) and height (cm)
- Calculation of BMI
- Display of BMI result with corresponding health category
- User-friendly interface

## Technologies Used
- Programming Language: [Python/JavaScript/Other]
- Framework/Library: [Tkinter/React/Other]
- IDE: [VSCode/PyCharm/Other]

## Installation
1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/bmi-calculator.git
    ```
2. Navigate to the project directory:
    ```sh
    cd bmi-calculator
    ```
3. Install the necessary dependencies:
    ```sh
    pip install -r requirements.txt   # For Python projects
    npm install                       # For JavaScript projects
    ```

## Usage
1. Run the application:
    ```sh
    python app.py      # For Python projects
    npm start          # For JavaScript projects
    ```
2. Enter your weight and height into the input fields.
3. Click on the "Calculate" button to see your BMI and health category.

## Health Categories
- Underweight: BMI < 18.5
- Normal weight: 18.5 <= BMI < 24.9
- Overweight: 25 <= BMI < 29.9
- Obesity: BMI >= 30

## Example Code Snippet
```python
def calculate_bmi(weight, height):
    bmi = weight / ((height / 100) ** 2)
    return bmi
