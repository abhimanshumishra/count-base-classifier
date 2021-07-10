Machine Learning HW 2 - Abhimanshu Mishra
Email: amishr11@binghamton.edu
B Number- B00817746

Academic Honesty Statement:
I have done this assignment completely on my own. I have not copied it, nor have
I given my solution to anyone else. I understand that if I am involved in
plagiarism or cheating I will have to sign an official form that I have cheated
and that this form will be stored in my official university record. I also
understand that I will receive a grade of 0 for the involved assignment for my
first offense and that I will receive a grade of “F” for the course for any
additional offense.
-Abhimanshu Mishra

Installation instructions:
Create a virtual environment with Python 3.7.
Install the required packages using the command: pip install -r requirements.txt
I have used PorterStemmer in nltk (instead of its online version) in my preprocessing step. This step is run everytime the program is run. To facilitate this, after running the previous command, open the Python shell and run the following commands:
import nltk
nltk.download('punkt')

Usage instructions:
python run.py training_data_folder_path testing_data_folder_path yes/no <yes/no> <stopwords-file-path>
First argument is path of training data, second argument is path of test data, third argument is whether to remove stopwords or not, fourth argument (optional argument - defaults to yes) is whether to stem or not and fifth argument is the path of any stopwords file (to enable this argument, using the fourth argument is compulsory) 
Example command: python run.py train test yes

Accuracy on test set:
- No stemming & no stopword removal: 94.560
- No stemming & stopword removal: 94.560
- Stemming & no stopword removal: 93.933
- Stemming & stopword removal: 93.933
Accuracy does not improve on removal of stopwords since they are common words found everywhere and hence do not add any predictive value.

Data directory should be structured as:
- training_data_folder
	- 'ham'
	- 'spam'
- testing_data_folder
	- 'ham'
	- 'spam'
- 'stopwords.txt'

Example command sequence:
conda create --name abhimanshu_hw2 python=3.7
conda activate abhimanshu_hw2
pip install -r requirements.txt
python
import nltk
nltk.download('punkt')
exit()
python run.py train test yes yes (training data folder contains two folders named 'ham' and 'spam' and its path is 'train' - first argument - and testing data contains two folders named 'ham' and 'spam' and its path is 'test' - second argument - remove stopwords from default file - third argument - and stem using PorterStemmer - fourth argument)
