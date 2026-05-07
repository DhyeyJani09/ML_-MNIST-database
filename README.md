# ML_-MNIST-database
Project Overview
This project explores the MNIST database of handwritten digits and implements a traditional machine learning classification model to accurately identify them.

Per the requirements, this solution strictly avoids Neural Networks and Deep Learning. Instead, it utilizes a Random Forest Classifier from the Scikit-Learn library, achieving a final Testing F1-Score of 97.02%, successfully surpassing the 95% requirement.

Prerequisites & Libraries
To run the Jupyter Notebook successfully, ensure you have Python 3 installed along with the following libraries:
numpy
pandas
matplotlib
seaborn
scikit-learn

You can install these dependencies via pip if you do not already have them:
pip install numpy pandas matplotlib seaborn scikit-learn

File Structure & Dataset Requirements
For the program to execute correctly without file path errors, the raw, uncompressed MNIST binary files must be placed in the exact same directory as the Jupyter Notebook.

Ensure your folder looks exactly like this, with no sub-folders containing the dataset:

ML_MNIST-database.ipynb (The main Jupyter Notebook)

train-images.idx3-ubyte (Training Images)

train-labels.idx1-ubyte (Training Labels)

t10k-images.idx3-ubyte (Testing Images)

t10k-labels.idx1-ubyte (Testing Labels)

(Note: Ensure the dataset files have periods before the "idx" extension, not hyphens).

How to Run the Program
Open Jupyter Notebook or Jupyter Lab in your chosen environment (e.g., VS Code).

Navigate to the directory containing the ML_MNIST-database.ipynb file and the four dataset files.

Open ML_MNIST-database.ipynb.

Run the notebook sequentially from top to bottom by selecting Kernel > Restart & Run All (or running each cell individually using Shift + Enter).

Execution Flow:

Step 1: The script will automatically load the raw binary files, skip the headers and reshape the image arrays. It will display a sample digit to confirm successful loading.

Step 2: The pixel data is normalized (scaled from a 0-255 range to a 0.0-1.0 range).

Step 3: The Random Forest Classifier initializes and trains on the 60000 training records. Note: Depending on your CPU, this step might take some time to complete.

Step 4: The model generates predictions on the 10000 testing records. It will output the final F1-Scores, a tabular classification report and display a graphical Confusion Matrix using Seaborn.

Results
As displayed in the final output cell of the notebook:

Training F1-Score: 1.0000

Testing F1-Score: 0.9702
