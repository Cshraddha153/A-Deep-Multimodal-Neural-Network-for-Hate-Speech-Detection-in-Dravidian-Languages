# A Deep Multimodal Neural Network for Hate Speech Detection in Dravidian Languages
This project presents a custom multimodal neural network (MMC) for Hate Speech Detection in Dravidian languages, integrating 
both text and audio features. Our approach enhances classification performance by combining transformer-based embeddings with a 
deep learning model. Additionally, we experiment with machine learning algorithms like KNN, Random Forest (RF), Naïve Bayes (NB), 
Logistic Regression (LR), and Support Vector Machine (SVM) for comparative evaluation.

# data distribution of Tamil
![caad88616416f8a062e9066441fe261021b4d978](https://github.com/user-attachments/assets/9b3983fc-9ca1-43e7-840e-254fdf0467d1)



# data distribution of Malayalam
![b9f2be52d3b90f44f2f812bc8b6c79de97a4f80f](https://github.com/user-attachments/assets/338bac89-6297-4f69-923b-a801bc11b504)



# data distribution of Telugu
![112e3f370804b34f8e36ce89659196b5a1ff6613](https://github.com/user-attachments/assets/fd323dec-a421-4b1a-b626-68460e3855c6)



## Model Architecture
![77123cc87b50356f08a7b23dcc261119e22979d8](https://github.com/user-attachments/assets/6f6f6d97-2fe7-4e21-ba6e-629b7359cffd)


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

# Confusion Matrix for Tamil dataset
![59b69e6253047163af256dbf98093a79dcd4d48b](https://github.com/user-attachments/assets/e16659a2-d7e5-4ae3-b7f2-a17379a8e14d)


# Confusion Matrix for Malayalam dataset
![7c12d0e2cffee219625db4d1a657d3948300918d](https://github.com/user-attachments/assets/3b63807e-bb3e-4fad-b574-bc5bda190271)


# Confusion Matrix for Telugu dataset
![8cc15cd379a3fb6d261ef6df760c349ea27019a3](https://github.com/user-attachments/assets/97821759-f8d4-4288-8448-f02e8e18373d)



# Rank List
### Team Name - MNLP

1. Tamil Rank list of Hate Speech detection - [Tamil Rank List](https://github.com/user-attachments/files/19090534/Tamil.Rank.List.pdf)
2. Malayalam Rank list of Hate Speech Misogyny detection - [Malayalam Rank List](https://github.com/user-attachments/files/19090532/Malayalam.Rank.List.pdf)
3. Telgu Rank list of Hate Speech Misogyny detection - [Telugu Rank List](https://github.com/user-attachments/files/19090536/Telugu.Rank.List.pdf)
   
# Citation

@inproceedings{chauhan-kumar-2025-mnlp,
    title = "{MNLP}@{D}ravidian{L}ang{T}ech 2025: A Deep Multimodal Neural Network for Hate Speech Detection in {D}ravidian Languages",
    author = "Chauhan, Shraddha  and
      Kumar, Abhinav",
    editor = "Chakravarthi, Bharathi Raja  and
      Priyadharshini, Ruba  and
      Madasamy, Anand Kumar  and
      Thavareesan, Sajeetha  and
      Sherly, Elizabeth  and
      Rajiakodi, Saranya  and
      Palani, Balasubramanian  and
      Subramanian, Malliga  and
      Cn, Subalalitha  and
      Chinnappa, Dhivya",
    booktitle = "Proceedings of the Fifth Workshop on Speech, Vision, and Language Technologies for Dravidian Languages",
    month = may,
    year = "2025",
    address = "Acoma, The Albuquerque Convention Center, Albuquerque, New Mexico",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2025.dravidianlangtech-1.41/",
    pages = "237--242",
    ISBN = "979-8-89176-228-2",
    abstract = "Social media hate speech is a significant issue because it may incite violence, discrimination, and social unrest. Anonymity and reach of such platforms enable the rapid spread of harmful content, targeting individuals or communities based on race, gender, religion, or other attributes. The detection of hate speech is very important for the creation of safe online environments, protection of marginalized groups, and compliance with legal and ethical standards. This paper aims to analyze complex social media content using a combination of textual and audio features. The experimental results establish the effectiveness of the proposed approach, with F1-scores reaching 72{\%} for Tamil, 77{\%} for Malayalam, and 36{\%} for Telugu. Such results strongly indicate that multimodal methodologies have significant room for improvement in hate speech detection in resource-constrained languages and underscore the need to continue further research into this critical area."
}
