# IT1244 Group Project: Bank Marketing Campaign Analysis and Prediction

**Team 21 Members**
- Aaron Lee Xuan
- Chang Chee Heng Clarence
- Mohamad ’Afif Bin Mohamad Satari
- Thaddeus Lim

## How to Run the Project

### 1. Install the required Python libraries

Make sure the following libraries are installed before running the notebook:

- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn
- imbalanced-learn

You can install them with:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn imbalanced-learn
```

### 2. Place the required files in the same folder

Ensure these files are in the same directory as:

`IT1244 Group Project Code.ipynb`

Required files:
- `dataset.csv`
- `final_model.pkl`

### 3. Comment out code cells 12 and 13 before running

#### Cell 12
This cell trains the model and takes a long time to run.

Keep it commented out unless:
- there is an error with `final_model.pkl`, or
- you want to retrain the model

#### Cell 13
This cell allows the user to input their own dataset for prediction and testing.

Keep it commented out unless you want to test on a custom dataset.

## Using Your Own Dataset

If you want to use your own dataset in Cell 13:

1. Place the input dataset in the same folder as `IT1244 Group Project Code.ipynb`
2. Make sure the dataset has the **same structure** as the original dataset:
   - same number of columns
   - same column names
   - `unknown` / `-1` values must only appear in the same columns as the original dataset

Relevant columns for `unknown` / `-1` encoding:
- `job`
- `marital`
- `education`
- `default`
- `housing`
- `loan`

3. Write the file path of the input dataset into the `filepath` variable

The code in Cell 13 will then:
- split the dataset into `X` columns and the `y` column
- replace the `X_test` and `y_test` variables from the original train/test split

## Notes

- Use `final_model.pkl` for faster execution if the trained model is already available.
- Only retrain the model when necessary, since training may take a long time.
