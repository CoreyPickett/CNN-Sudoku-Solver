# 🧩 Convolutional Neural Network (CNN) Sudoku Solver

Machine learning project implementing a Convolutional Neural Network (CNN) to predict missing digits in partially filled Sudoku puzzles. 
The model treats Sudoku as a multi‑class classification problem, learning to approximate valid puzzle solutions from generated training data.
Completed as an assignment for a third-year computing course "Machine Intelligence".

## 🤖 Technologies

- Python
- Jupyter Notebook
- LaTeX

## 🚀 Features

- CNN architecture designed to predict digits for empty Sudoku cells
- One‑hot encoding of puzzle grids for efficient learning
- Cross‑entropy loss for multi‑class classification
- Batch normalisation and dropout to reduce overfitting
- Training and validation accuracy tracking
- Evaluation and visual comparison of predictions

## 📋 The Process
Sudoku can be framed as a constraint satisfaction problem, but this project instead explores a machine‑learning‑based approach. A CNN was trained to predict the most likely digit (1–9) for each empty cell in a 9×9 grid.
When beginning the project, I didn’t necessarily believe this was the best way to approach the problem, more I was interested in trying something new and seeing how the model worked.

The workflow I created includes:
- Generation of large datasets of valid Sudoku puzzles for the model to train on
- One‑hot encoding each puzzle into 10 channels (empty + digits 1–9)
- Training a CNN for 30 epochs on 100,000 puzzles
- Monitoring training and validation loss/accuracy
- Evaluating the model on five unseen puzzles and one final example
- Comparing predicted solutions with correct answers

Although CNNs do not explicitly enforce Sudoku constraints, the model learned to approximate valid solutions by generalising patterns from the training data.

## 🧠 What I Learned

- Designing and training a CNN for structured grid‑based prediction
- Implementing one‑hot encoding for categorical spatial data
- Using PyTorch for model construction, batching, and optimisation
- Applying dropout and batch normalisation to mitigate overfitting
- Interpreting training/validation curves and diagnosing model behaviour

## 📊 Key Results

- Final evaluation accuracy: 75% (30/40 cells correct)
- Average accuracy across 5 evaluation puzzles: 67%
- Training loss decreased steadily, with plateauing near epoch 30
- Validation metrics improved modestly due to smaller validation set
- Model successfully predicts many digits but struggles with low‑clue (hard) puzzles
- CNN approach is viable but inferior to classical solvers

## 📈 Future Improvements

- Train on a larger and more varied dataset
- Extend the approach to other logic puzzles (KenKen, Kakuro)
- Combine CNN predictions with a constraint solver to enforce Sudoku rules (however this may defeat the point of CNN in the first place)
