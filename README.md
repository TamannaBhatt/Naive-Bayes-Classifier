
# Naive Bayes Classifier from Scratch 🎯

This project demonstrates a manual implementation of the **Naive Bayes classification algorithm** using Python and Pandas on the classic **Play Tennis** dataset.

🔍 The goal is to predict whether to play tennis based on weather conditions like `outlook`, `temperature`, `humidity`, and `wind`.

---

## 📁 Dataset

The dataset used (`play_tennis.csv`) includes 14 instances with the following columns:
- `day`
- `outlook`
- `temperature`
- `humidity`
- `wind`
- `play` (Target: yes/no)

We drop the `day` column as it is irrelevant for prediction.

---

## 🧠 What I Did

- Calculated **prior probabilities**:  
  \[
  P(\text{yes}) = \frac{9}{14}, \quad P(\text{no}) = \frac{5}{14}
  \]

- Used `pd.crosstab()` to manually compute **conditional probabilities** for each feature value.

- Applied Naive Bayes formula to predict the class for a test query:  
  `{outlook=sunny, temperature=hot, humidity=high, wind=weak}`

- Compared \( P(\text{yes}|\text{features}) \) and \( P(\text{no}|\text{features}) \) to make a final prediction.

---

## 📚 Learning Outcome

✅ Understood how Naive Bayes works under the hood  
✅ Learned how to calculate priors and conditionals manually  
✅ Applied probability theory to real classification problems  
✅ Gained confidence in implementing ML logic from scratch

---

## 🚀 Future Improvements

- Extend it to use `sklearn` for comparison  
- Visualize decision boundaries (for numeric datasets)  
- Add Laplace smoothing  
- Test on new datasets (e.g., Iris, Titanic, SMS spam)

---

## 💻 Tech Stack

- Python
- Pandas
- NumPy
- Google Colab 

---

## 📸 Sample Output

Test Query: {'outlook': 'sunny', 'temperature': 'hot', 'humidity': 'high', 'wind': 'weak'}

P(Yes | features): 0.0054  
P(No | features): 0.0057

## 🧑‍🏫 Credits

> This implementation was based on a tutorial by [CampusX](https://youtu.be/DeeWsqoY4Eo?si=_gZQeJ0Wsz8qloWL).  
> I recreated the logic myself as part of my learning process.

---
Prediction: ❌ No (Don’t Play Tennis)
