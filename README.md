## TO IMPLEMENT

Step 1: Clone the repository
```
git clone https://github.com/Akashgaur30/-Amazon-Reviews-Sentiment-Analysis-Using-NLP-and-Fuzzy-Logic.git
```

Step 2: Open the cloned repository and create a conda environment. Activate the new environment
```
conda create -n echoreviews python=3.12
```
```
conda activate echoreviews
```

Step 3: Install the requirements file
```
pip install -r requirements.txt
```

Step 4: Run the app
```
flask --app api.py run
```

Step 5: The app will run on port 5000. 
```
localhost:5000
```
### fuzzy logic used in sentiment analysis of reviews. Fuzzy logic helps in handling uncertainty and ambiguity in natural language, making it useful for sentiment classification when the sentiment is not strictly positive or negative but falls on a spectrum.

How Fuzzy Logic is Used in Sentiment Analysis

1. Fuzzy Sentiment Scores

Instead of assigning strict labels (positive, neutral, negative), fuzzy logic assigns a degree of positivity, neutrality, and negativity.

For example, a review like "The product is okay, but could be better" may get a 40% positive, 50% neutral, and 10% negative score.



2. Fuzzy Membership Functions

Words and phrases are assigned fuzzy sentiment scores based on linguistic analysis.

Example:

"Excellent" → High Positive (0.9)

"Okay" → Neutral (0.5)

"Bad" → Negative (0.8)




3. Fuzzy Inference System (FIS)

Input: Extracted features from text (e.g., words, phrases, intensity modifiers).

Rule Base: If a review contains "great" and "not", then the sentiment is "moderately positive".

Defuzzification: Converts fuzzy outputs into crisp sentiment scores or labels.




Implementation Approaches

Fuzzy Rule-Based Approach

Define rules like:

IF review contains ("good" OR "excellent") AND NOT ("but", "however"), THEN sentiment = High Positive.

IF review contains ("bad" OR "poor") AND ("not" OR "less"), THEN sentiment = Moderately Negative.



Fuzzy Neural Networks

Combine fuzzy logic with deep learning models like LSTMs, CNNs, or Transformers for better sentiment prediction.


Fuzzy Ontologies

Use predefined fuzzy sentiment lexicons (e.g., SentiWordNet with fuzzy values).


