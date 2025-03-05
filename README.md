# Multimodal Hate Speech Detection in Dravidian languages: DravidianLangTech@NAACL 2025
This project presents a custom multimodal neural network (MMC) for Hate Speech Detection in Dravidian languages, integrating both text and audio features. Our approach enhances classification performance by combining transformer-based embeddings with a deep learning model. Additionally, we experiment with machine learning algorithms like KNN, Random Forest (RF), Naïve Bayes (NB), Logistic Regression (LR), and Support Vector Machine (SVM) for comparative evaluation.

# Text Features
For text-based feature extraction, we utilize XLM-RoBERTa-base, a transformer-based multilingual model. The text utterances are tokenized and passed through the model to generate contextual embeddings. These embeddings serve as input features for the multimodal classification network.

# Audio Features
For audio-based feature extraction, we process speech recordings using Mel-Frequency Cepstral Coefficients (MFCCs). The audio signal is first loaded using Librosa, and then 13 MFCCs are extracted per frame. To create a fixed-length feature representation, the MFCCs are averaged over the time axis: These MFCC features capture the spectral properties of speech, making them effective for distinguishing hate speech from non-hate speech.

# Multimodal Fusion & Classification
The extracted text embeddings (XLM-RoBERTa-base) and audio features (MFCCs) are concatenated to form a unified multimodal representation. This fused feature set is then fed into a custom multimodal neural network (MMC) for classification.

## The MMC architecture consists of:
1. Fully connected layers to process text embeddings
2. Fully connected layers to process audio features
3. A concatenation layer to merge both modalities

A final classification layer to predict Hate Speech categories (Gender, Political, Religious, Personal Defamation) or Non-Hate
Additionally, we compare the MMC model’s performance against traditional machine learning classifiers such as KNN, Random Forest (RF), Naïve Bayes (NB), Logistic Regression (LR), and Support Vector Machine (SVM).
This multimodal approach enhances hate speech detection by leveraging both linguistic and acoustic cues, making the model more robust in identifying hate speech across Dravidian languages.

# Rank List
### Team Name - MNLP
1. Tamil Rank list of Hate Speech detection - [Tamil Rank List.pdf](https://github.com/user-attachments/files/19090534/Tamil.Rank.List.pdf)

2. Malayalam Rank list of Hate Speech Misogyny detection - [Malayalam Rank List.pdf](https://github.com/user-attachments/files/19090532/Malayalam.Rank.List.pdf)

3. Telgu Rank list of Hate Speech Misogyny detection - [Telugu Rank List.pdf](https://github.com/user-attachments/files/19090536/Telugu.Rank.List.pdf)
   
# Research Paper
[Multimodal_Hate_Speech_Detection (1).pdf](https://github.com/user-attachments/files/18813643/Multimodal_Hate_Speech_Detection.1.pdf)
 (Under Review at NAACL 2025)
