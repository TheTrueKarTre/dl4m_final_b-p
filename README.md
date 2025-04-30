# dl4m_final_b-p

1. Project Description & Motivation
Classification Method: Binary
Data Classes: Cantonese vs. Mandarin
Motivation: Contemporary globally employed music streaming platforms, such as Spotify, often struggle to distinguish between the predominant languages used in Chinese pop songs, specifically, Cantonese and Mandarin. As a preliminary attempt to resolve this issue, this project aims to build a basic deep learning model for the binary classification of the two linguistic branches in Chinese pop songs, with a particular emphasis on identifying Cantonese songs.

2. Dataset Description
Data Content & Form: Vocal stems extracted from 160 Chinese pop songs, 80 Cantonese versus 80 Mandarin. Each vocal stem is randomly cut into five .wav clips, each 30 seconds long, totaling 800 samples.
Special Note: Each pair contains two versions of the same song, the only difference being the language used by the vocalist.

3. Code Structure & Organization (Methodology)
Research Question: Which pre-trained model achieves the highest test accuracy and F1 Score in the recognition task? How do these results compare with reference values of the parameters?
General Structure: Data augmentation -> CNN / Transfer learning (insert pre-trained model here) -> Classifier head
Rationale/Reasoning: Transfer learning models used in class (inadequate performance) -> Transfer learning models used in pertinent research (excellent performance)

4. Summary of Results & Key Findings
The following is a comprehensive ranking list of the three models applied:
CNN (High accuracy, low loss, short run time)
Wav2Vec2 (Medium accuracy, medium loss, long run time)
YAMNet (Low accuracy, high loss, medium run time)
Findings:
Ceteris paribus, CNN has achieved the best overall performance among the three models applied in the language recognition task for Chinese pop vocals.
CNN outperforms pre-trained models when applied to tasks with a limited sample size, while pre-trained models become more effective when the sample size is sufficiently large.
CNN was unable to learn data features before augmentation and log-mel extraction.
The high parameter quantity of the Wav2Vec2 model makes training on a small sample size a rather strenuous task.
YAMNet, being more event-focused in nature, lacks the perceptual capabilities to identify linguistic discrepancies, making it less suitable for the task.

5. Task Distribution
Kelvin Bo: Original idea, presentation & README outlining
Sienna Peng: Methodology & work plan, data preprocessing
Common: Data collection, source searching, model testing, performance analysis
