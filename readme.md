## Abstract:

Most political NLP models are tested using random splits that ignore how language changes over time. We are examining what happens when you train ideology classifiers on old political texts and test them on newer ones. Our work will use manifestos and parliamentary speeches from several countries to see how classifier performance degrades as the time gap grows. Our study will analyze political texts from party manifestos (2000-2020) and parliamentary speeches (2005-2022) across five countries. We will implement strict temporal splitting where models are trained on data before a cutoff year and tested on data from subsequent years with varying time gaps (1-8 years). We will compare three model architectures: BERT-based classifiers, RoBERTa-based classifiers, and Logistic regression baselines. Performance will be measured using accuracy, F1 score, and class-specific metrics across different temporal gaps. We expect to find substantial accuracy drops over longer periods based on preliminary analysis. The degradation will likely appear roughly linear with time, and transformer models should maintain better performance than traditional approaches but still show significant decline. Feature analysis will be performed using SHAP values to track how specific political terms shift meaning - words like ”reform” and ”security” don’t stay associated with the same ideological camps. We will examine what percentage of discriminative features remain stable versus those that show complete reversal in association. Different ideological classes will be analyzed for varying temporal patterns. This research exposes problems with how we currently evaluate political text classifiers and questions whether models trained on historical data can reliably analyze contemporary politics. The findings will push for better evaluation methods that account for language evolution in political discourse and provide methodological recommendations for more robust evaluation of political NLP systems.

## Goal

1. Political Semantic Drift Analysis

Tracks how words like "reform" and "security" shift ideological associations
Detects when terms flip from LEFT→RIGHT or RIGHT→LEFT
Measures semantic volatility across time periods

2. Proper Model Architecture

Baseline: TF-IDF + Logistic Regression (interpretable)
RoBERTa: Transformer model as specified in your paper
BERT: Optional additional transformer model
Both architectures for robustness comparison

3. Feature Analysis 

Political term extraction: Comprehensive vocabulary of political terms
Ideology weight tracking: How each term associates with LEFT/RIGHT/CENTRE over time
Direction flip detection: Identifies when terms switch ideological camps
SHAP-style interpretability: Term importance extraction from models

4. Temporal Robustness Insights

Period-based training: Models trained on specific time periods (2000-2005, 2006-2010, etc.)
Cross-period testing: See how models trained on old data perform on new data
Semantic shift quantification: Measure magnitude of term meaning changes

5. Research Output

Semantic shift detection: "reform", "security" changing associations
Volatility scores: Which terms are most unstable over time
Direction flip analysis: Terms that completely switch sides
Cross-model validation: Do BERT and RoBERTa find same patterns?
Trajectory visualization: See how terms evolve over time

🔍 Key Research Findings This Will Generate:

"Words don't stay with same ideological camps" - Quantified evidence
Transformer vs baseline comparison - Which architecture better captures drift?
Specific political terms that flip - Concrete examples for your paper
Temporal degradation patterns - How much performance drops over time
Feature stability analysis - What % of features remain stable vs flip


# Report
📊 Outputs You'll Get:

Term trajectory plots: Visual proof of semantic drift
Shift heatmaps: Which terms shift most between periods
Direction flip analysis: Terms that switch ideological sides
Research summary: Publication-ready findings
JSON data: All numerical results for statistical analysis

Please see directory political_semanatic_drift_analysis
   • Political language shows measurable semantic drift over time
   • Terms like 'reform' and 'security' change ideological associations
   • Transformer models needed for deep semantic understanding
   • Temporal evaluation crucial for political NLP model robustness

# Dataset
Data downloaded from source https://manifesto-project.wzb.eu/

# Code
```
python3 -m venv venv 
source venv/bin/activate 
pip install -r requirements.txt 
pip install ipykernel
jupyter notebook  paper.ipynb
```
