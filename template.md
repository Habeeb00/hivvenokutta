**CONTENTS**

**ACKNOWLEDGEMENT**

**ABSTRACT**

**LIST OFFIGURES**

**LIST OFABBREVIATIONS**

**1 INTRODUCTION**

**i**

**ii**

**v**

**vi**

**1**

**1.1 Problem Statement . . . . . . . . . . . . . . . . . . . . . . . . . . . 2**

**1.2 Objective . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 2**

**1.3 Purpose and Need . . . . . . . . . . . . . . . . . . . . . . . . . . . . 3**

**1.4 Organization of Report . . . . . . . . . . . . . . . . . . . . . . . . . 5**

**2 LITERATUREREVIEW**

**2.1 HandGesture Recognition Based on Deep Learning . . . . . . . . .**

**2.2 HandSign and Gesture Recognition System . . . . . . . . . . . . . .**

**7**

**7**

**9**

**2.3 Face Recognition Using Deep Learning . . . . . . . . . . . . . . . . 12**

**2.4 Face Recognition And Identification Using Deep Learning . . . . . . 15**

**2.5 Deep Learning Based Speaker Recognition System with CNN and**

**LSTMTechniques . . . . . . . . . . . . . . . . . . . . . . . . . . . 17**

**2.6 Machine Learning Based Voice Authentication and Identification. . . 21**

**2.7 ASurvey OnUnimodal, Multimodal Biometrics And Its Fusion Tech**

**niques . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 22**

**2.8 AComprehensiveOverviewonBiometricAuthentication Systems Us**

**ing Artificial Intelligence Techniques . . . . . . . . . . . . . . . . . . 24**

**2.9 Multimodal Biometric Systems– Study To Improve Accuracy And**

**Performance . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 25**

**2.10 Information Fusion in Biometrics . . . . . . . . . . . . . . . . . . . . 28**

**2.11 ANovelMultimodalBiometricAuthentication System Using Machine**

**Learning and Blockchain . . . . . . . . . . . . . . . . . . . . . . . . 31**

**iii**

**2.12 Face-Voice Based Multimodal Biometric Authentication System via**

**FaceNet and GMM . . . . . . . . . . . . . . . . . . . . . . . . . . . 32**

**2.13 Dynamic Audio-Visual Biometric Fusion for Person Recognition . . . 35**

**2.14 A Multimodal User Authentication System Using Faces and Gestures**

**2.15 A Multimodal Biometric System Using Fingerprint, Face, and Speech**

**3 METHODOLOGY**

**39**

**42**

**44**

**3.1 Technical Approach and Design Rationale . . . . . . . . . . . . . . . 44**

**3.2 Overall System Framework . . . . . . . . . . . . . . . . . . . . . . . 45**

**3.3 Multimodal Enrollment Strategy . . . . . . . . . . . . . . . . . . . . 46**

**3.4**

**Face Recognition Methodology . . . . . . . . . . . . . . . . . . . . 48**

**3.5 Voice Recognition Methodology . . . . . . . . . . . . . . . . . . . . 49**

**3.6 Gesture Recognition Methodology . . . . . . . . . . . . . . . . . . . 50**

**3.7 Parallel Multimodal Verification Strategy . . . . . . . . . . . . . . . 50**

**3.8 Adaptive Preset-Based Score-Level Fusion . . . . . . . . . . . . . . . 52**

**4 IMPLEMENTATION**

**53**

**4.1 Development Environment and System Setup . . . . . . . . . . . . . 53**

**4.2 Face Recognition Module Implementation . . . . . . . . . . . . . . . 54**

**4.3 Voice Recognition Module Implementation . . . . . . . . . . . . . . 55**

**4.4 Gesture Recognition Module Implementation . . . . . . . . . . . . . 55**

**4.5 Multimodal Enrollment and Verification Engines . . . . . . . . . . . 56**

**4.5.1**

**4.5.2**

**Sequential Enrollment Engine . . . . . . . . . . . . . . . . . 56**

**Parallel Verification Engine . . . . . . . . . . . . . . . . . . 57**

**4.6 Adaptive Fusion and Decision Logic Implementation . . . . . . . . . 58**

**5 CONCLUSIONANDFUTURESCOPE**

**59**

**5.1 Conclusion . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 59**

**5.2 Future Improvements and Enhancements . . . . . . . . . . . . . . . . 59**

**REFERENCES**

**60**

**LIST OFFIGURES**

**2.1 Block diagram of hand gesture recognition using deep learning . . . .**

**7**

**2.2 Framework of Hand Sign and Gesture Recognition System . . . . . . 10**

**2.3 Face Recognition Process using deep learning . . . . . . . . . . . . . 13**

**2.4 Face Recognition Chart Using Deep Learning . . . . . . . . . . . . . 16**

**2.5 General architecture of biometric system . . . . . . . . . . . . . . . . 23**

**2.6 Multimodal biometric system using face and fingerprint . . . . . . . . 26**

**2.7 Biomodal biometric system showing three levels of fusion . . . . . . 29**

**2.8 Voice recognition process . . . . . . . . . . . . . . . . . . . . . . . . 32**

**2.9 Face recognition process . . . . . . . . . . . . . . . . . . . . . . . . 33**

**2.10 Overall process of the multimodal biometric system . . . . . . . . . . 40**

**2.11 Process of the face representation module . . . . . . . . . . . . . . . 41**

**3.1 System Architecture . . . . . . . . . . . . . . . . . . . . . . . . . . . 45**

**4.1 Enrollment Pipeline . . . . . . . . . . . . . . . . . . . . . . . . . . . 56**

**4.2 Verification Pipeline . . . . . . . . . . . . . . . . . . . . . . . . . . . 57**

**v**

**LIST OFABBREVIATIONS**

**CNN Convolutional Neural Network**

**RNN RecurrentNeural Network**

**LSTM LongShort-Term Memory Network**

**MFCC Mel-Frequency Cepstral Coefficient**

**GMM GaussianMixture Model**

**PCA Principal Component Analysis**

**SVM SupportVector Machine**

**EER**

**FAR**

**Equal Error Rate**

**False Accept Rate**

**FRR FalseReject Rate**

**SNR Signal-to-Noise Ratio**

**HOG HistogramofOriented Gradients**

**vi**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**CHAPTER1**

**INTRODUCTION**

**In the modern digital era, secure and reliable authentication has become a critical**

**necessity. With the rapid increase in digital services, online transactions, and smart**

**devices, protecting user identity has become more challenging than ever before. Tra**

**ditional methods of authentication, such as passwords, PINs, and security tokens, are**

**no longer sufficient due to their vulnerability to theft, guessing, and phishing attacks.**

**Reports of large-scale data breaches highlight how easily compromised credentials can**

**lead to identity theft and financial loss.**

**To address these concerns, biometric authentication has gained popularity because it**

**uses unique human traits like fingerprints, facial patterns, or voice signatures. Bio**

**metrics offer stronger security since they are inherently tied to an individual, unlike**

**passwords that can be shared or stolen. However, most existing systems rely on a**

**single biometric modality. While effective in certain scenarios, these systems are not**

**foolproof: for example, face recognition struggles under poor lighting or when masks**

**are worn, and fingerprint systems fail if the finger is dirty, wet, or injured. Furthermore,**

**touch-based systems raise hygiene concerns, especially in shared environments such**

**as hospitals or public kiosks.**

**In light of these challenges, multimodal biometric authentication has emerged as a**

**promising solution. Instead of relying on a single trait, it combines multiple inde**

**pendent biometric signals, improving robustness, security, and user inclusivity. By**

**leveraging modern artificial intelligence and machine learning, multimodal systems**

**can intelligently fuse evidence from different sources to make authentication decisions**

**that are both more reliable and resistant to spoofing attacks.**

**This project, titled SilentAuth: A Multimodal Biometric Authentication System, fo**

**cuses on developing a secure, touchless, and inclusive authentication solution that**

**integrates face recognition, gesture recognition, and sound-based authentication. The**

**aim is to overcome the limitations of passwords and single-biometric systems, while**

**also addressing modern concerns of hygiene, accessibility, and security.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**1**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**1.1 Problem Statement**

**The major challenge in modern authentication lies in the fact that existing systems are**

**either insecure, inconvenient, or fail to be sufficiently inclusive. Traditional password**

**based authentication is increasingly unreliable because passwords can be guessed,**

**reused across platforms, or stolen through phishing attacks and large-scale data breaches.**

**Users themselves often compromise security by selecting weak passwords or sharing**

**them, which further weakens the system. While biometric authentication was intro**

**duced to overcome these issues, single-biometric systems such as facial recognition,**

**f**

**ingerprint scanning, or voice authentication cannot guarantee reliability under all**

**conditions. They are often prone to spoofing attacks, for example, photographs can de**

**ceive facial recognition, recorded voices can bypass voice authentication, and artificial**

**f**

**ingerprints can be used to trick scanners. Environmental factors such as poor lighting,**

**background noise, or physical injuries can also degrade their performance. Moreover,**

**touch-based systems like fingerprint or palm scanners present hygiene concerns, es**

**pecially in shared public environments such as hospitals, airports, and workplaces,**

**where frequent contact can contribute to the spread of infections. These systems also**

**present accessibility challenges, as they often fail to support users with disabilities or**

**special needs who may be unable to interact with traditional authentication methods.**

**Considering these limitations, there is a clear need for a system that ensures strong**

**security while also being hygienic, inclusive, and user-friendly. SILENT AUTH aims**

**to address this gap by designing a multimodal biometric authentication system that**

**integrates face recognition, gesture recognition, and sound-based verification into a**

**unified fusion engine, thereby enhancing security, reducing spoofing risks, and en**

**abling touchless, accessible authentication suitable for diverse real-world applications.**

**1.2 Objective**

**The primary objective of the project,SILENTAUTH is to design, develop, and evaluate**

**a Silent Multimodal Biometric Authentication System that delivers secure, touchless,**

**and inclusive authentication by integrating face, gesture, and sound modalities into a**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**2**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**unified framework. To achieve this, the project first seeks to conduct a comprehen**

**sive review of existing biometric and multimodal authentication systems in order to**

**understand their strengths, limitations, and the gaps that can be addressed through**

**a fusion-based approach. Building upon this foundation, recognition modules for**

**face, gesture, and sound will be designed using modern artificial intelligence and**

**machine learning techniques to ensure accurate and efficient identification under var**

**ied conditions. A central focus of the project is the development of a robust fusion**

**engine capable of combining the evidence from these different modalities to arrive at**

**a reliable final authentication decision, thereby enhancing both security and usability.**

**The system will then be evaluated thoroughly in terms of its performance metrics,**

**including accuracy, speed of authentication, and resistance to spoofing or adversarial**

**attempts, while testing under diverse environmental conditions such as variations in**

**lighting, background noise, or user behavior. An important objective is to ensure**

**inclusivity by supporting users with disabilities through alternative modalities that**

**can serve as fallbacks when one biometric input cannot be provided. Finally, the**

**project aims to prototype a practical proof-of-concept system that demonstrates the**

**applicability of SilentAuth in real-world scenarios, such as secure login for personal**

**devices, smart home entry systems, or access management in workplace environments,**

**thereby bridging theoretical design with practical implementation.**

**1.3 Purpose and Need**

**The purpose of the SILENTAUTH: A Multimodal Biometric Authentication System**

**project is to design, develop, and implement a secure, touchless, and inclusive authenti**

**cation mechanism that overcomes the limitations of conventional methods. In today’s**

**digital era, the reliance on traditional authentication techniques such as passwords,**

**PINs, and security tokens has become increasingly problematic. These methods are**

**often vulnerable to theft, phishing attacks, and human errors, including weak pass**

**word selection or reuse across multiple platforms. The consequences of compromised**

**credentials are severe, ranging from identity theft to financial fraud, as evidenced**

**by numerous large-scale data breaches in recent years. Furthermore, conventional**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**3**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**password-based systems often fail to provide a user-friendly experience, requiring**

**individuals to remember complex combinations of characters, which can lead to frus**

**tration, inefficiency, and security risks when passwords are written down or shared.**

**Biometric authentication has emerged as a potential solution to these challenges, as it**

**leverages unique physiological or behavioral traits, such as fingerprints, facial patterns,**

**and voice signatures. Unlike passwords, biometric identifiers are inherently tied to**

**the individual and cannot be easily shared or replicated, offering stronger security.**

**However, single-biometric systems are not entirely reliable. Facial recognition sys**

**tems, for instance, may fail under poor lighting conditions or when users wear masks.**

**Fingerprint scanners can be ineffective if the user’s finger is wet, dirty, or injured,**

**and voice-based systems are susceptible to background noise or imitation attacks.**

**Additionally, touch-based systems present hygiene concerns, particularly in public or**

**shared environments like hospitals, airports, or offices, where frequent contact can**

**contribute to the spread of infections. These limitations highlight the necessity for a**

**more robust and inclusive authentication approach.**

**SILENTAUTH addresses these challenges by employing a multimodal biometric ap**

**proach, integrating multiple independent modalities—face recognition, gesture recog**

**nition, and sound-based authentication—into a unified system. By combining multiple**

**biometric inputs, the system enhances reliability, accuracy, and security, as the weak**

**nesses of one modality can be compensated by the strengths of another. For example, if**

**environmental factors reduce the effectiveness of facial recognition, gesture or sound**

**based verification can still provide reliable authentication. This fusion-based method**

**also significantly mitigates risks from spoofing attacks, as an unauthorized individual**

**would need to replicate multiple biometric traits simultaneously to gain access.**

**Beyond security, the project emphasizes user convenience, hygiene, and accessibility.**

**The touchless design eliminates the need for physical interaction with devices, making**

**it safer and more hygienic in environments where multiple users share authentication**

**terminals. Additionally, the system is designed to support users with disabilities or**

**special needs, offering alternative modalities when one input method is unavailable.**

**This inclusive approach ensures that authentication is accessible to a wide range of**

**users without compromising security or usability.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**4**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**From a research perspective, SILENTAUTH contributes to the advancement of mul**

**timodal biometric authentication technology by exploring the fusion of multiple AI**

**driven recognition systems. It provides an experimental framework for evaluating the**

**effectiveness of integrating face, gesture, and sound modalities, offering insights into**

**optimal fusion strategies, system robustness, and performance under real-world con**

**ditions. Practically, the project demonstrates the feasibility of deploying a multimodal**

**system in applications such as secure device login, smart home entry, workplace access**

**management, and other scenarios requiring high security and touchless operation. It**

**also serves as an educational platform, enabling students and researchers to gain hands**

**on experience with AI, machine learning, computer vision, and audio processing,**

**thereby preparing them for future challenges in the field of secure digital systems.**

**In summary, the purpose and need of SILENTAUTH lie in delivering a future-ready,**

**secure, touchless, and inclusive authentication system that addresses the limitations of**

**traditional and single-biometric methods, ensures hygiene and accessibility, leverages**

**advanced AI technologies, and provides both practical and research contributions to**

**the field of digital security. By implementing a multimodal fusion-based framework,**

**the system aims to achieve superior reliability, usability, and robustness, making it a**

**comprehensive solution for modern authentication challenges.**

**1.4 Organization of Report**

**This report is systematically organized to provide a clear and comprehensive under**

**standing of the SILENTAUTH project.Chapter 2: Literature Review presents an in**

**depth review of existing research related to biometric authentication systems. It ex**

**amines two representative research papers for each biometric modality—face, gesture,**

**and audio—to establish the technical background and current advancements in uni**

**modal recognition. In addition, it reviews nine papers focusing on fusion engines,**

**multimodal biometric authentication frameworks, and machine learning-based inte**

**gration methods. This chapter identifies existing challenges and research gaps that**

**motivate the development of the proposed fusion-based authentication system.Chapter**

**3: System Design describes the overall architecture and design of the SilentAuth**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**5**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**system. It explains the functional components, data flow, and interaction between the**

**face, gesture, and audio recognition modules. Detailed system architecture and design**

**diagrams illustrate the modular structure and the operation of the fusion engine respon**

**sible for multimodal decision-making.Chapter 4: Work Plan and Schedule outlines**

**the step-by-step execution strategy for the project. It includes a structured timeline**

**representing the stages of research, development, testing, and evaluation, ensuring that**

**each module and integration phase aligns with the overall project goals.Chapter 5:**

**Conclusion and Future Scope summarizes the outcomes of the project, highlighting**

**its contributions toward improving security, hygiene, and inclusivity through touchless**

**multimodal authentication. It also discusses the project’s limitations and potential di**

**rections for future enhancement, such as incorporating additional biometric modalities**

**and adaptive learning mechanisms.This structured organization ensures a logical and**

**coherent progression—from background research to system design, implementation**

**planning, and final reflections—guiding the reader through both the conceptual and**

**practical aspects of the SILENTAUTH project.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**6**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**CHAPTER2**

**LITERATUREREVIEW**

**2.1 Hand Gesture Recognition Based on Deep Learning**

**This paper \[1] discusses the importance of hand gesture recognition in Human-Computer**

**Interaction (HCI) and the limitations of traditional systems that rely on handcrafted**

**features. Conventional systems are easily affected by environmental variations such**

**as poor lighting, occlusion of hand parts, and differences in skin tone, which lower**

**recognition accuracy. Deep learning provides a way to overcome these challenges**

**by automatically learning robust features from large amounts of data. \[1]The authors**

**emphasize that gestures are an intuitive medium for communication and interaction**

**with computers, and that recognition systems based on deep learning can be used in**

**real-time applications such as assistive technologies, smart devices, and authentication**

**systems. By focusing on the recognition of digit-based gestures (0–9), the paper high**

**lights the value of combining spatial and temporal models to achieve high precision**

**and reliability.**

**Methodology**

**Figure 2.1: Block diagram of hand gesture recognition using deep learning**

**The methodology of this paper \[1] was built around four essential steps: dataset prepa**

**ration, model design, training, and evaluation. First, the dataset was prepared using**

**MediaPipe, a framework capable of detecting and tracking twenty-one landmarks of**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**7**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**the human hand. These landmarks, which correspond to finger joints and palm posi**

**tions, were extracted for gestures representing digits from zero to nine. The dataset**

**was standardized so that every gesture was consistently represented, and augmentation**

**was performed by varying the position and orientation of the hand to make the model**

**more robust to real-world variations.**

**For model design, four deep learning approaches were tested: Convolutional Neural**

**Networks (CNNs), Recurrent Neural Networks (RNNs), a hybrid CNN and RNN**

**model, and Transformers. CNNs were used to extract spatial features such as edges**

**and contours, capturing the relative positions of fingers and the structure of the hand.**

**RNNs were employed to capture sequential changes in gestures, which is crucial for**

**recognizing dynamic movements over time. The hybrid CNN+RNN model combined**

**these strengths by using convolutional layers for spatial extraction followed by re**

**current layers for temporal modeling, thereby enabling the system to capture both**

**static and dynamic gesture features effectively. Transformers were also tested, using**

**attention mechanisms to model long-range dependencies across input sequences, but**

**these models required more data to achieve their full potential.**

**The training phase involved supervised learning with backpropagation and gradient**

**descent optimization. Regularization techniques such as dropout were used to avoid**

**overfitting, ensuring the models generalized well to unseen data. The dataset was split**

**into training and test sets, and performance was measured primarily using classification**

**accuracy. Model size and computational efficiency were also important factors in**

**determining suitability for real-time use. During evaluation, CNNs showed strong spa**

**tial recognition but struggled with temporal consistency, RNNs performed well with**

**dynamic gesture sequences while being lightweight in size, and the hybrid CNN+RNN**

**model consistently achieved the highest accuracy by leveraging both strengths. Trans**

**formers showed promise but did not surpass the hybrid model under the conditions of**

**this study.**

**Results**

**The hybrid CNN+RNN model achieved the highest performance with an accuracy**

**of 99.76 percent, while the RNN alone achieved 99.28 percent and stood out for**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**8**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**its small memory footprint of only twenty-two megabytes, making it well-suited for**

**embedded devices. CNNs also performed strongly but lacked sequential modeling,**

**and Transformers did not outperform the hybrid approach with the dataset available.**

**The main limitation was that the dataset was restricted to digits zero through nine,**

**which means generalization to more complex gestures remains untested. In addition,**

**environmental conditions such as severe occlusion or poor illumination may still pose**

**challenges.**

**Summary of Findings**

**This paper \[1] summarizes that deep learning provides a highly effective approach**

**for gesture recognition and that combining spatial and temporal modeling yields the**

**best results. For SilentAuth, this study offers three key takeaways. First, gestures**

**can be treated as a reliable behavioral biometric trait, with high recognition accuracy**

**achievable using deep learning. Second, lightweight models such as RNNs make real**

**time implementation feasible on mobile and low-power devices. Third, hybrid models**

**significantly improve recognition, making gesture-based authentication practical for**

**multimodal systems. These insights support the inclusion of gesture recognition as a**

**central component of the SilentAuth multimodal authentication framework.**

**2.2 Hand Sign and Gesture Recognition System**

**This paper \[2] presents a system designed to recognize hand signs and gestures, par**

**ticularly for Indian Sign Language, with the primary motivation of improving com**

**munication for deaf and mute communities. Many existing systems require expensive**

**hardware such as sensor gloves, while others are inflexible in real-world applications.**

**\[2]This research proposes a purely software-based system that relies only on video**

**input, making it more affordable and accessible. Beyond its intended application for**

**accessibility, the system can also be adapted to support gesture-to-text translation**

**in video conferencing, online platforms, and human-computer interaction, thereby**

**broadening its scope of use.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**9**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**Methodology**

**Thesystemwasdesignedaroundamulti-stage pipeline beginning with data acquisition**

**and ending with classification. Raw video frames were captured as input, and the hand**

**was isolated as the region of interest using the Haar Cascade classifier. By focusing**

**only on the hand, the system reduced background interference and ensured that subse**

**quent processing steps were applied to the relevant portion of the frame. Preprocessing**

**followed this step, where the region of interest was converted into grayscale, smoothed**

**with Gaussian blur, and processed with thresholding to enhance the visibility of hand**

**contours and features. These preprocessing steps were crucial in creating a cleaner**

**input for the classification models, as they reduced noise and highlighted the shape of**

**the hand.**

**Since no suitable dataset was publicly available for Indian Sign Language, the au**

**thors created their own dataset. Using OpenCV, they recorded multiple repetitions**

**of each gesture corresponding to the ISL alphabet (A–Z) and digits (0–9). This self**

**built dataset captured variability across recordings and enabled the system to train**

**on a comprehensive set of gesture samples. Data augmentation was also applied**

**by recording the same gestures under slightly different lighting and orientations to**

**improve robustness.**

**Figure 2.2: Framework of Hand Sign and Gesture Recognition System**

**For classification, the system used a two-tier approach. In the first tier, features were**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**10**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**extracted and filtered to identify clear gestures. If a gesture was consistently observed**

**in more than fifty frames, it was considered valid and passed to a Convolutional Neural**

**Network (CNN) for classification. In the second tier, ambiguous gestures were passed**

**through specialized classifiers that refined the prediction, reducing the chances of**

**misclassification.**

**The CNN was central to the classification process. It used convolutional layers to**

**extract spatial features from gesture images, with activation provided by ReLU to**

**introduce non-linearity. Max pooling layers were included to reduce computational**

**complexity by downsampling feature maps, while dropout layers were incorporated**

**to prevent overfitting. The CNN automatically learned distinctive gesture features,**

**eliminating the need for manual feature engineering. The dataset was divided into**

**training and testing subsets, and the CNN was trained with supervised learning until it**

**reached optimal performance.**

**Results**

**The proposed system achieved an impressive accuracy of 99.89 percent on the custom**

**ISL dataset, demonstrating that deep learning with CNNs is highly effective for hand**

**gesture recognition. Since the system required only a standard camera, it did not**

**depend on costly external hardware, making it accessible and scalable.**

**However, the system had limitations. It performed best under good lighting conditions**

**and with clear, stationary gestures. Recognition of dynamic gestures or gestures per**

**formed under poor illumination remains a challenge. Furthermore, since the dataset**

**was self-constructed, the generalizability to diverse populations or environments may**

**require additional validation.**

**Summary of Findings**

**This paper \[2] summarizes that CNN-based hand sign recognition systems are capable**

**of achieving near-perfect accuracy, especially when trained on custom datasets. By**

**designing a purely software-based solution, the study showed that real-time gesture**

**recognition can be practical and cost-effective. For SilentAuth, the most relevant**

**takeaways are that gesture recognition can be achieved without additional hardware,**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**11**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**making it suitable for mobile authentication, and that high recognition accuracy is**

**attainable with careful dataset design and CNN-based learning. The two-tier architec**

**ture also provides an idea for SilentAuth, where ambiguous cases in multimodal fusion**

**could be resolved with additional classification steps. This strengthens the argument**

**for gestures as a reliable behavioral biometric modality within SilentAuth.**

**2.3 Face Recognition Using Deep Learning**

**Face recognition has quickly become a key technology in modern security and au**

**thentication, offering a reliable and non-intrusive way to verify identity. Unlike older**

**methods that relied on physical tokens or simple traits—often prone to loss, forgery,**

**or environmental issues—facial biometrics authenticate individuals using only visual**

**data.This paper \[3] examines the growth of face recognition powered by deep learning,**

**particularly Convolutional Neural Networks (CNNs). These networks have overcome**

**many challenges of traditional approaches by automatically learning complex patterns**

**from large image datasets. As a result, they can handle variations in lighting, pose,**

**and expression, which previously caused major difficulties. By extracting rich hierar**

**chical features directly from images, deep learning models achieve higher accuracy,**

**scalability, and robustness in real-world conditions. This paper \[3] highlights these**

**advancements and outlines a modern deep learning-based framework for face recog**

**nition, emphasizing its effectiveness and its expanding role in security, access control,**

**and everyday digital applications.**

**Methodology**

**The face recognition system in this paper \[3] starts with data preparation. All facial**

**images are resized to a standard 64×64 RGB format and divided into training and**

**testing sets. This ensures that every image the system sees has the same size and**

**format, which is important for learning effectively.The main part of the system is**

**a Convolutional Neural Network (CNN). CNNs are deep learning models that can**

**automatically learn important features from images. In this system, the CNN has two**

**convolutional layers. Each layer uses multiple filters to detect edges, textures, and**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**12**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**other important details of faces. After each convolutional layer, there is a max-pooling**

**layer that reduces the size of the feature maps. This makes the system more robust, so**

**small changes in position or slight distortions in the image don’t affect the results.Once**

**features are extracted, they are flattened (converted into a single long vector) and**

**passed through three fully connected layers. These layers act like a classifier, deciding**

**which person the face belongs to. The hidden layers use the ReLU activation function,**

**which helps the model learn complex patterns, and the final output layer uses softmax,**

**which produces probabilities for each possible identity.**

**Figure 2.3: Face Recognition Process using deep learning**

**The system is built using Keras and TensorFlow, popular tools in deep learning. Keras**

**makes it easy to build and organize the model layer by layer, while TensorFlow handles**

**the heavy computations and training. The model uses the Adam optimizer, which au**

**tomatically adjusts learning rates to train faster and more accurately. During training,**

**data is fed in batches, and the model’s weights are updated through backpropagation**

**to reduce errors. Labels are also converted into binary class matrices using NumPy**

**so that they work with the softmax output.In short, this process—from preprocessing**

**the images to extracting features, classifying faces, and optimizing training—creates**

**a complete system that can accurately recognize faces, even with large datasets or in**

**real-world conditions.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**13**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**Results**

**This study tested the custom CNN on datasets of 16, 30, and 60 people. It achieved**

**100% accuracy on the smallest dataset and maintained strong performance on larger**

**sets, with 97% and 94% accuracy for 30 and 60 people, respectively. Validation results**

**showed consistent accuracy with reasonable error margins. Compared to VGG16, the**

**custom CNN performed as well or better, especially on smaller datasets, showing it**

**can learn efficiently from limited data.**

**However, accuracy drops as dataset size increases, indicating potential challenges with**

**large populations. Small datasets also risk overfitting, and the model may struggle with**

**extreme pose, lighting, or occlusion variations. Complex models like VGG16 can be**

**computationally expensive and less effective with small datasets. Future work should**

**focus on larger datasets and advanced techniques to improve robustness and scalability**

**for real-world applications.**

**Summary of Findings**

**This paper \[3] shows that deep learning, particularly Convolutional Neural Networks**

**(CNNs), can significantly improve face recognition, achieving high accuracy even with**

**datasets of different sizes. Using automated feature extraction and classification with**

**frameworks like Keras and TensorFlow, the study demonstrates efficient training and**

**validation, highlighting the practical potential of CNN-based biometric systems for**

**security and access control.**

**For our Silent Auth project, which combines face, voice, and gesture recognition,**

**the study offers valuable lessons. A well-designed CNN can provide an efficient and**

**accurate face recognition module, even with limited data. Its modular design and use of**

**popular frameworks make integration into a multisensory system practical. Key take**

**aways—such as consistent preprocessing, proper activation functions, and optimizer**

**choices—will help us build a robust, scalable, and accurate silent authentication system**

**that leverages complementary biometric streams for improved security and usability.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**14**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**2.4 Face Recognition And Identification Using Deep Learn**

**ing**

**This paper \[4] explores the rapidly growing field of face recognition, a biometric**

**technology widely used in law enforcement, consumer authentication, and enterprise**

**tracking. It highlights how advances in affordable GPUs and large-scale face image**

**datasets have accelerated the development of deep neural networks for tasks from face**

**detection to identity recognition. The key idea is to use Convolutional Neural Networks**

**(CNNs), which automatically extract important facial features to create a compact**

**”face code.” This representation produces similar outputs for different images of the**

**same person and distinct outputs for different people, enabling accurate identification.**

**The paper \[4] also traces the history of face recognition, from holistic methods in**

**the 1990s to local-feature and learning-based methods in the 2000s, leading to the**

**dominance of deep learning techniques since 2014. Although it does not go into**

**detailed methodology, it highlights a practical pipeline combining data preprocessing,**

**feature extraction, and classification using tools like Python, OpenCV, and pretrained**

**models, efficiently handling face detection, alignment, encoding, and classification for**

**real-time recognition.**

**Methodology**

**This paper \[4] uses deeplearning, specifically Convolutional Neural Networks (CNNs),**

**to build a robust face recognition system. \[4] The process starts with dataset collection**

**and preprocessing, making sure faces are properly detected and aligned for consistent**

**input to the model. OpenCV, a popular computer vision library, is used for face**

**detection and image manipulation. The system also uses pretrained neural networks**

**to create 128-dimensional face embeddings (face codes) that capture key facial fea**

**tures. These embeddings are compact representations that allow the system to compare**

**and identify faces efficiently. Tools like dlib help detect facial landmarks accurately,**

**ensuring proper alignment of features such as eyes, nose, and mouth. Overall, the**

**methodology combines detection, alignment, feature encoding, and classification into**

**a smooth pipeline suitable for both images and videos.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**15**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**Figure 2.4: Face Recognition Chart Using Deep Learning**

**When a face is detected, it is aligned so the landmarks are consistent, which helps the**

**CNNextract features more accurately. The generated embeddings are compared with**

**stored face codes in a database to identify or verify a person. Matching is done by**

**measuring the similarity of embeddings—closer embeddings indicate a higher chance**

**of a match. The system is designed for real-time processing and remains robust against**

**variations in pose, lighting, and facial expressions, common challenges in real-world**

**biometric applications.**

**Results**

**This paper \[4] shows that the deep learning-based face recognition system can accu**

**rately detect and recognize faces in both images and real-time video. It uses CNNs to**

**extract facial features and create unique face embeddings, which are matched against**

**a database for identification. The system is efficient, processing each frame in about**

**360–390 milliseconds, making it suitable for real-time use. However, the paper does**

**not provide exact accuracy numbers or comparisons with other methods, limiting a**

**quantitative evaluation.**

**Some limitations remain, such as difficulty handling extreme pose changes, lighting**

**variations, and occlusions. The system also relies on large labeled datasets and GPU**

**resources for training, which can be a practical constraint. These gaps suggest that**

**future work could focus on more thorough evaluations, improving robustness under**

**diverse conditions, and optimizing computational efficiency for wider applicability.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**16**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**Summary of Findings**

**This paper \[4] summarizes by emphasizing the potential of deep learning techniques,**

**especially convolutional neural networks, in advancing face recognition systems to**

**perform real-time identification with efficient feature extraction and processing. While**

**the study demonstrates a practical implementation combining face detection, align**

**ment, and embedding generation, it notes existing challenges related to environmental**

**variability and the need for powerful hardware resources. The system’s modular design**

**and integration of widely-used libraries make it accessible for deployment, showcas**

**ing the feasibility and promise of deep learning in biometric applications despite the**

**absence of detailed benchmarking metrics.**

**For our Silent Auth project, which combines face, voice, and gesture recognition,**

**this study confirms that CNN-based face recognition is a strong choice for facial**

**modality. Its approach offers a reliable, efficient method for identity verification and**

**shows the value of standard tools for a flexible system. Understanding its limitations**

**also underscores the importance of multimodal biometrics to improve robustness and**

**reduce risks associated with single modalities, guiding our design and implementation**

**decisions.**

**2.5 Deep Learning Based Speaker Recognition System with**

**CNNandLSTMTechniques**

**In this work \[5], authors present a deep-learning approach to speaker identification**

**that compares convolutional neural networks (CNNs) and long short-term memory**

**networks (LSTMs) using standard audio features. The authors \[5] note that audio**

**signals are first preprocessed and transformed into perceptually motivated features**

**(MFCCs) before classification . Their goal is to determine which architecture– CNN**

**or LSTM– provides higher accuracy on the same tasks, using Mel-frequency cepstral**

**coefficients (MFCCs) as input features . (MFCCs simulate the human cochlea’s fre**

**quency analysis and are commonly used to convert time-domain speech into compact**

**spectral representations .) The study uses two benchmark speech datasets (TIMIT and**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**17**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**LibriSpeech) in both “closed-set” and “open-set” evaluation regimes. In the closed-set**

**scenario, the same speaker pool appears in training and testing, whereas in the open-set**

**scenario, training and testing are performed on disjoint speaker sets.**

**The datasets are described in detail \[5]. The TIMIT corpus consists of 630 speakers**

**(with 10 utterances per speaker, covering major U.S. dialects) . In the authors’ imple**

**mentation, 462 speakers’ data form the training pool and 168 speakers’ data form the**

**test pool. For closed-set experiments, the 462 training speakers were split 80/20 into**

**training and testing folds . For open-set experiments, the pre-defined train/test split is**

**used (training on one set of speakers and testing on a separate group) . The LibriSpeech**

**dataset (train-clean-100 subset) provides 28,539 utterances from 251 speakers . For**

**closed-set training on LibriSpeech, the full set is used with an internal 80/20 split. For**

**open-set testing, the authors follow a different partitioning (randomly selecting 12–15**

**s segments for training and 2–6 s segments for testing, yielding about 14,481 training**

**samples and 7,452 test samples after silence removal) . These datasets were chosen**

**due to their widespread use in speaker recognition and their complementary properties**

**(TIMIT is phonetically rich but small, whereas LibriSpeech is larger and cleaner) .**

**Methodology**

**In preprocessing, raw audio waveforms were resampled (using librosa at 22,050 Hz)**

**and converted to mono. Speech frames were then encoded using 40-dimensional**

**MFCCs,capturing the short-term spectrum of the signal . Specifically, librosa’s mfcc()**

**function was used to compute 40 coefficients over 173 time frames for each utterance;**

**the mean over frames was taken to produce a single 40-element feature vector per sam**

**ple . \[5] The authors chose MFCCs because they “outperform other methods” for audio**

**classification in speaker recognition (being compact and perceptually motivated) . This**

**preprocessing ensures that each audio sample is represented by a fixed-dimensional**

**feature vector reflecting the speech spectral envelope and key temporal features.**

**For the CNN architecture they build a fairly lightweight sequential network . It begins**

**with two 2D convolutional layers applied to the 20×5 (time×feature) input (the MFCC**

**vector was likely reshaped to 20×5×1 or equivalent). The first Conv2D layer has 64**

**f**

**ilters with a 5×5 kernel, stride 1 and “same” padding, followed by a ReLU nonlin**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**18**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**earity. The second Conv2D layer is similar but uses 128 filters and a 30% dropout**

**for regularization . After each convolution, a 2×2 MaxPooling2D operation is applied**

**to reduce the spatial dimension . Thus the two conv+pool stacks extract hierarchical**

**features from the MFCC inputs. The feature maps are then flattened into a vector and**

**fed into two fully connected layers of 256 and 512 units, each using ReLU activations.**

**Finally, a softmax output layer has one node per speaker class (in closed-set mode),**

**converting activations to class probabilities . In open-set evaluation, the last softmax**

**layer is removed after training: the penultimate layer’s outputs serve as an embedding**

**vector for each test utterance, which is then compared to stored speaker embeddings**

**using cosine, Euclidean or Manhattan distance to assign a speaker label . In summary,**

**the CNN model is a standard conv-stack with two conv layers (64 and 128 filters) and**

**two dense layers (256 and 512), designed to classify MFCC features into speaker IDs.**

**The LSTM-based model is constructed as a temporal sequence network. It begins with**

**two LSTM layers, each having 128 hidden units . The first LSTM layer processes**

**an input sequence of shape 20×5 (20 time steps of 5 features, per the MFCC-derived**

**input). A dropout of 0.30 is applied to the second LSTM layer to reduce overfit**

**ting. Batch normalization is applied after the first two layers to speed up training**

**convergence . After the recurrent layers, two time-distributed dense layers are used:**

**the first maps the LSTM outputs to 256 units, and the second to 512 units, both with**

**ReLUactivations . The output of the second time-distributed layer is then flattened and**

**passed to a final dense softmax classifier (as in the CNN) during closed-set training .**

**In open-set mode, just as in the CNN, the last softmax layer is popped off after training**

**to yield embedding vectors, which are matched to test samples by distance metrics .**

**Thus the LSTM model has a recurrent core (two LSTM layers) followed by two fully**

**connected time-distributed layers, culminating in classification.**

**Both models were trained with standard cross-entropy loss and the Adam optimizer**

**(the authors note these settings but do not emphasize them) . Accuracy was used as**

**the performance metric . The data were split into batches (50 batches per epoch) and**

**trained for hundreds of epochs. For example, on TIMIT the authors trained both CNN**

**and LSTM for 500 epochs in the closed-set setting, and for the open-set they reported**

**300 epochs for the CNN and 100 epochs for the LSTM . As expected, the training**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**19**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**curves showed steadily improving accuracy with more epochs. No data augmentation**

**was performed, though the authors note that augmentation could potentially boost**

**performance (it often does) in similar tasks .**

**Results**

**The key results show that the CNN model significantly outperformed the LSTM on**

**these tasks. On the TIMIT data, the CNN achieved 80.63% test accuracy in the**

**closed-set scenario and 77.51% in the open-set scenario, whereas the LSTM achieved**

**only 71.54% (closed) and 62.13% (open) . Training accuracies for both models were**

**nearly 100%, indicating that the models fit the training speakers very well. On the**

**LibriSpeech corpus (clean-100), the CNN attained 97.85% test accuracy in the closed**

**set task (with training accuracy 99.26%) . When using a modified open-set partition**

**of LibriSpeech, the CNN’s performance dropped to 64.70% (with 99.97% training**

**accuracy); under the corresponding closed-set split it achieved 84.96% . (The paper**

**does not report a corresponding LSTM accuracy on LibriSpeech, suggesting the LSTM**

**was less competitive and perhaps omitted.) In all cases, CNN’s accuracy exceeded**

**the LSTM’s by a substantial margin (often 8–15 percentage points). These results**

**demonstrate that CNN’s convolutional feature extraction is highly effective for speaker**

**identity from MFCC inputs, whereas the LSTM– while conceptually suited to sequen**

**tial data– did not reach the same performance in this setup.**

**Limitations include :**

**No Data Augmentation: Accuracy could have increased (up to ˜ 4%) if data augmenta**

**tion had been applied.**

**Open vs. Closed Sets: Models perform better on closed sets (training and testing on**

**the same dataset) than on open sets.**

**Limited Scope: Study focuses only on speaker/voice identification with relatively few**

**parameters for smaller training.**

**LSTM Performance: LSTM underperforms compared to CNN on the TIMIT dataset**

**in both open and closed sets.**

**MFCC-to-Spectrogram Conversion: MFCC transformation claims to preserve essen**

**tial audio features, which could be a limitation if some features are lost.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**20**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**Summary of Findings**

**The key takeaway from this \[5] study is that a compact CNN trained on MFCC fea**

**tures can achieve robust and accurate speaker recognition, outperforming LSTM mod**

**els while remaining computationally efficient. The approach generalizes well across**

**datasets like TIMIT and LibriSpeech, demonstrating the effectiveness of spectral feature**

**based deep learning.**

**2.6 MachineLearningBasedVoiceAuthenticationandIden**

**tification.**

**\[6] Voice authentication leverages unique vocal patterns for user identification, of**

**fering a secure and contactless biometric alternative to traditional passwords. This**

**technology analyzes features such as tone, pitch, and speech rhythm, making it well**

**suited for enhancing security in access control, finance, and healthcare systems.**

**Methodology**

**This system \[6] integrates voice biometric authentication with traditional username/password**

**verification for enhanced security. Users enroll by recording their voice samples,**

**which are then transformed into two types of features: Mel-spectrogram images and**

**Mel-scale filter bank (FBanks) coefficients.Two neural network models are trained**

**separately on these features:**

**Spectrogram Net: Processes 5-second audio segments converted into grayscale Mel**

**spectrogram images sized 227x227 pixels. The training uses a large dataset of speaker**

**voice samples to classify identities based on visualized frequency patterns.**

**FBanksNet: Processes FBanks feature matrices created from short overlapping audio**

**frames, capturing spectral properties of the voice over time. This model is trained using**

**a two-step approach—multi-class classification followed by triplet loss fine-tuning to**

**better separate genuine and impostor voice samples in feature space.**

**During authentication, spoken phrases are first verified through speech-to-text match**

**ing to prevent replay attacks, then passed through the models for voice verification.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**21**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**The system evaluates true positive and true negative rates to measure performance.**

**Results**

**Testing showed both models achieved high accuracy, with FBanksNet performing**

**best: 99.14% test accuracy and minimal loss after 20 training epochs. Challenges**

**remain: model performance depends on data size and speech quality, and small or**

**copied datasets can lower accuracy, highlighting the need for robust, diverse samples**

**to prevent spoofing.**

**Summary of Findings**

**\[6] Combining voice biometrics with classical authentication significantly boosts sys**

**tem security and user convenience. Techniques using advanced neural networks and**

**diverse audio features can serve as a strong base for SilentAuth, enabling seamless,**

**secure voice-driven authentication—especially valuable where hands-free, remote, or**

**accessibility-focused solutions are required.**

**2.7 ASurvey On Unimodal, Multimodal Biometrics And Its**

**Fusion Techniques**

**This paper \[7] reviews unimodal and multimodal biometric systems, showing that**

**combining multiple traits (like ECG, fingerprint, and face) improves accuracy, secu**

**rity, and reliability compared to single-trait systems. It discusses common challenges**

**such as noise, spoofing, and variations within the same user, and explains how fusion**

**techniques (at feature, score, or decision level) help overcome these issuesOverall, the**

**paper provides a broad overview and acts as a guide for researchers entering the field**

**of biometric authentication.**

**Methodology**

**The methodology described in this paper \[7] begins by defining biometrics as the**

**automated recognition of individuals based on their physiological or behavioral char**

**acteristics. It contrasts unimodal biometric systems, which rely on a single biometric**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**22**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**trait and face inherent shortcomings like noise sensitivity, nonuniversality, and spoof**

**vulnerabilities, with multimodal systems that integrate multiple biometric sources to**

**improve accuracy and robustness. Face recognition is highlighted as a common and**

**user-friendly modality, often paired with other traits to offset its limitations. The**

**paper \[7] specifically notes the fusion of ECG, fingerprint, and face biometrics as a**

**practical example of multimodal systems enhancing security and liveliness detection.**

**Figure 2.5: General architecture of biometric system**

**Regarding fusion methods, the paper \[7] elaborates on three primary techniques: feature**

**level fusion, which concatenates or transforms raw biometric features into a unified**

**representation; score-level fusion, where matching scores from individual modalities**

**are combined using approaches like sum rule, weighted sum, or machine learning clas**

**sifiers; and decision-level fusion, which integrates the final acceptance or rejection de**

**cisions from each modality using majority voting or other logical operations. Choosing**

**the appropriate fusion strategy is vital as it affects system complexity, computational**

**requirements, and overall recognition performance.**

**Results**

**As a survey paper, this paper \[7] consolidates findings from numerous studies, illus**

**trating that multimodal biometric systems consistently outperform unimodal ones in**

**terms of accuracy, robustness, and resistance to spoof attacks.It highlights the effective**

**ness of combining complementary biometric traits such as ECG, fingerprint, and face,**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**23**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**particularly when fusion techniques are appropriately applied at the feature, score, or**

**decision levels.The paper also points out limitations typical of survey studies, including**

**variability in datasets, evaluation metrics, and fusion strategies across reviewed works,**

**which makedirect quantitative comparison challenging. Moreover, the evolving nature**

**of biometric research means that optimal fusion methods and system designs remain**

**active areas for future exploration and refinement.**

**Summary of Findings**

**This paper \[7] summarizes that multimodal biometric systems—combining traits like**

**face, fingerprint, and ECG—are more accurate, robust, and secure than single-trait**

**systems. Using feature-, score-, or decision-level fusion helps overcome issues like**

**noise and spoofing. For our Silent Auth project, which uses face, voice, and gesture**

**recognition, the paper shows that multimodal fusion improves reliability and security.**

**Its insights on fusion strategies help us design a system that effectively combines**

**biometric features while balancing performance, usability, and robustness in real-world**

**scenarios.**

**2.8 A Comprehensive Overview on Biometric Authentica**

**tion Systems Using Artificial Intelligence Techniques**

**Biometric authentication enables identity verification based on unique biological or**

**behavioral traits, offering security without reliance on passwords or PINs. Biometric**

**systems classify traits into physiological (e.g., fingerprint, face, iris) and behavioral**

**(e.g., voice, signature, keystroke) categories. This \[8] review discusses multiple bio**

**metric modalities and their combinations with AI to improve accuracy and usability.**

**Methodology**

**This paper \[8] reviews various biometric techniques including fingerprint, facial, iris,**

**retina, voice, signature, and keystroke recognition. It explains typical design steps: ac**

**quisition, preprocessing, feature extraction, and classification using machine learning**

**algorithms like PCA, SVM, neural networks, and fuzzy models. Special attention is**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**24**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**given to hybrid approaches that combine multiple biometric features and AI techniques**

**for robust authentication.**

**Results**

**Different biometric methods offer varying merits and drawbacks. Fingerprint recog**

**nition is accurate but sensitive to skin condition; facial recognition benefits from deep**

**learning but requires substantial computation; iris and retina biometrics provide high**

**precision but require specialized sensors. Behavioral biometrics enhance continuous**

**authentication but suffer from environmental noise and variability. Challenges include**

**data quality, user convenience, computational cost, and attack resilience.**

**Summary of Findings**

**Combining multiple biometric traits with AI techniques significantly enhances authen**

**tication robustness and user experience. This comprehensive review \[8] highlights**

**the importance of multimodal fusion and intelligent classification methods for secure**

**identity verification. SilentAuth can draw from these insights to design systems that**

**balance accuracy, usability, and security, leveraging AI-driven biometrics fusion and**

**adaptive learning for continuous, seamless user authentication**

**2.9 Multimodal Biometric Systems– Study To Improve Ac**

**curacy And Performance**

**This paper \[9] surveys multimodal biometric systems, which combine multiple traits**

**to improve accuracy, reliability, and security. It explains the limits of unimodal sys**

**tems (noise, spoofing, low accuracy) and shows how combining traits like finger**

**print and face helps overcome these issues. The paper \[9] reviews different fusion**

**levels—sensor, feature, score, and decision—along with normalization methods and**

**system architectures. Overall, it highlights the design, benefits, and challenges of**

**multimodal systems for secure authentication.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**25**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**Methodology**

**This paper \[9] starts by categorizing multimodal biometric systems (MBS) based on**

**how multiple biometric data are used. Multi-algorithmic systems apply different al**

**gorithms to the same biometric sample from a single sensor, improving accuracy by**

**using multiple processing methods. Multi-instance systems use several instances of**

**the same trait, like multiple fingers for fingerprint recognition, to increase reliability.**

**Multi-sensor systems use different sensors to capture the same trait, for example,**

**combining visible light and infrared cameras for face recognition, to perform better**

**in varied environments. A key part of multimodal systems is fusion, which combines**

**information from different biometric sources to improve performance. Fusion can**

**happen at several levels: Sensor-level fusion combines raw data before processing,**

**Feature-level fusion merges feature vectors extracted from each modality, Score-level**

**fusion combines the matching scores from each modality using methods like sum,**

**weighted sum, or machinelearning classifiers, Decision-level fusion combines the final**

**decisions from each matcher, often using majority voting.**

**Figure 2.6: Multimodal biometric system using face and fingerprint**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**26**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**This paper \[9] also mentions a system combining face and fingerprint that uses score**

**level fusion to improve accuracy by leveraging the strengths of both modalities. Ad**

**vanced feature-level fusion methods, like correlation filter banks, can further opti**

**mize performance by effectively combining complementary information from different**

**traits. Another important step is normalization, which makes scores from different bio**

**metric modalities comparable before fusion. Methods include min-max normalization**

**(scales scores between minimum and maximum), z-score normalization (standardizes**

**scores using mean and standard deviation), median and MAD (reduces sensitivity**

**to outliers), and tanh estimator (reduces the effect of extreme values). Proper nor**

**malization ensures that fusion works effectively, resulting in higher overall system**

**performance.**

**Results**

**Multimodal biometric systems reviewed in the paper \[9] show improved accuracy**

**and robustness by combining traits like face and fingerprint using fusion techniques**

**at different levels. For instance, score-level fusion of face and fingerprint can boost**

**accuracy up to 98%, reducing false acceptance rates significantly. Techniques like**

**correlation filter banks enhance feature integration, while normalization methods such**

**as min-max and z-score ensure comparability of matching scores. Limitations include**

**increased system complexity and computational demands, as well as challenges in**

**selecting the best fusion and normalization methods. Data compatibility across sensors**

**and standardization of evaluation metrics also remain hurdles for practical deployment.**

**Summary of Findings**

**This paper \[9] summarizes that multimodal biometric systems, which combine traits**

**like face, fingerprint, voice, or gestures, perform better and are more accurate than**

**unimodal systems. Evaluating various normalization and fusion techniques on large**

**datasets, the study found that fusion significantly improves matching performance, and**

**doing so at the matching score level allows integration of existing biometric systems**

**without modification. Future research could explore alternative normalization and fu**

**sion methods and test larger datasets to ensure scalability for commercial deployments.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**27**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**For the SilentAuth project, which combines face, voice, and gesture recognition, key**

**takeaways are: multimodal fusion reduces false accepts, false rejects, and spoofing;**

**fusion at different levels improves overall accuracy; score normalization (often min**

**max) is important; and large-scale testing is necessary. Leveraging these insights,**

**SilentAuth can achieve better accuracy, robustness, and flexible integration.**

**2.10 Information Fusion in Biometrics**

**This paper \[10] ”Information Fusion in Biometrics” addresses the inherent limitations**

**of unimodal biometric systems, such as noisy sensor data and unacceptable error rates,**

**by proposing a multimodal biometric system that integrates information from multiple**

**sources. The core principle is that fusing multiple pieces of evidence for the same**

**identity can significantly improve reliability and overall performance.**

**Methodology**

**\[10]The authors categorize fusion strategies into three levels: feature level , where the**

**raw data from multiple sensors are combined before feature extraction . score level**

**fusion, where matching scores are combined and abstract level, where final decisions**

**are consolidated. The study primarily focuses on fusion at the confidence (score) and**

**feature levels, as they provide more discriminatory information than decision-level**

**fusion. The experimental setup involved three biometric modalities: face, fingerprint,**

**and hand geometry. For data collection, the authors used two separate user sets due to**

**the independence of the biometric indicators. Face and fingerprint data were collected**

**from ”user set I” (50 users), while hand geometry data was collected from ”user set**

**II” (also 50 users). The authors addressed this by randomly pairing users from the**

**two sets. The paper \[10] provides a brief overview of how each individual biometric**

**model works within the system. For face verification, the system uses the eigenface**

**approach, which applies Principal Component Analysis (PCA) to extract features from**

**grayscale images. Matching is then performed by computing the Euclidean distance**

**between the eigenface coefficients of the template and the detected face. For fingerprint**

**verification, the features correspond to the position and orientation of minutiae. The**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**28**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**matching process involves comparing the two-dimensional minutiae patterns extracted**

**from the user’s print with those in the template. For hand geometry verification, the**

**system computes 14 feature values, including the lengths and widths of the fingers**

**and palm. The Euclidean distance metric is used to compare feature vectors and**

**generate a matching score. A critical step before score-level fusion was normalization,**

**which mapped all scores to a common range of \[0, 100] to account for differences**

**in score distributions from the various matchers. The study evaluated three specific**

**fusion techniques at the confidence level: the sum rule, a C5.0 decision tree, and a**

**linear discriminant function. The sum rule takes the weighted average of individual**

**scores , and in this study, equal weights were assigned to each modality. A decision**

**tree is a predictive model that creates a series of rules to classify data, while a linear**

**discriminant function (LDF) finds a linear combination of features that maximizes the**

**separation between classes.**

**Figure 2.7: Biomodal biometric system showing three levels of fusion**

**Results**

**The results consistently showed that fusing information led to a significant perfor**

**mance increase over individual biometrics. The sum rule proved to be the most effec**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**29**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**tive of the three classifiers tested, achieving a False Accept Rate (FAR) of 0.03% and**

**a False Reject Rate (FRR) of 1.78%. In comparison, the linear discriminant classifier**

**had an FAR of 0.47% and an FRR of 0.00%, though this low FRR was noted as a**

**consequence of overfitting the genuine class. The C5.0 decision tree performed with**

**an FARof0.036% and anFRRof9.63%. Thepaper also notes that initial experiments**

**with fusion at the representation level showed better performance than score-level**

**fusion.**

**A key limitation of the study, particularly relevant to real-world applications, is that**

**it does not explicitly discuss a contingency plan for handling the failure of a single**

**modality during verification. The discussed fusion techniques—the sum rule, decision**

**tree, and LDF—assume that scores from all participating modalities are present for**

**fusion. While the multimodal approach inherently provides robustness to noisy data,**

**the paper does not outline a specific mechanism for dealing with the complete absence**

**of data from a particular biometric due to sensor failure or other issues.**

**Summary of Findings**

**In summary, this research \[10] emphasizes the critical role of fusion techniques in**

**enhancing multimodal biometric systems. By integrating multiple biometric indicators**

**such as face, fingerprint, and hand geometry, the study demonstrates how different**

**fusion strategies—particularly at the confidence level using methods like the sum**

**rule—can significantly improve verification performance. Moreover, the project high**

**lights effective approaches for handling biometric inputs of varying quality, showing**

**that appropriate preprocessing and adaptive weighting of modalities can mitigate the**

**impact of noisy or low-quality data. Overall, the findings underscore that careful**

**selection of fusion techniques combined with robust handling of diverse input qualities**

**is key to achieving reliable and secure biometric verification.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**30**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**2.11 A Novel Multimodal Biometric Authentication System**

**Using Machine Learning and Blockchain**

**Password and token-based authentication systems are increasingly vulnerable to com**

**promise, prompting the shift to biometric methods that utilize unique physical and**

**behavioral traits for reliable user verification. However, traditional unimodal biometric**

**methods suffer from spoofing and accuracy issues; this leads to the development of**

**multimodal systems that combine multiple traits for robust security.**

**Methodology**

**This paper \[11]introduces a multimodal authentication approach using fingerprint, face,**

**age, and gender traits. These biometrics are processed and fused through a Decision**

**Tree machine learning algorithm to calculate a user confidence score. Blockchain**

**technology is also integrated for secure and tamper-resistant storage of identity and**

**authentication data, enabling decentralized token management and increased trans**

**parency.**

**Results**

**Experiments with real users demonstrated high authentication accuracy (up to 99–100%)**

**and extremely low false acceptance rates. Fingerprint and face biometrics contribute**

**most to the overall confidence score, with age and gender adding supplemental checks.**

**Although the system is efficient and secure, its real-world usability depends on data**

**quality, and further testing is needed for larger-scale deployments and resilience to**

**complex attacks.**

**Summary of Findings**

**The proposed system shows that combining multiple biometrics and machine learn**

**ing significantly improves authentication reliability while blockchain enhances data**

**integrity.SilentAuth can leverage this foundation to build user-friendly, secure, and**

**decentralized authentication solutions with minimal user interaction, ensuring both**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**31**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**convenience and robust security. Key takeaways include the value of multimodal**

**fusion, confidence-driven access, and blockchain-based trust management for next**

**generation authentication projects**

**2.12 Face-VoiceBasedMultimodalBiometricAuthentication**

**System via FaceNet and GMM**

**This paper \[12] presents a multimodal biometric authentication system that integrates**

**face and voice recognition to address the shortcomings of unimodal systems. Uni**

**modal systems are vulnerable to spoofing, environmental noise, and intra-class vari**

**ation, which can cause errors in identity verification. \[12]The proposed multimodal**

**system combines two complementary biometric traits, face and voice, to improve**

**robustness and reduce Equal Error Rate (EER). By using FaceNet for face recogni**

**tion and Gaussian Mixture Models (GMM) for voice recognition, and by applying**

**score-level fusion to combine the outputs, the system achieves superior performance**

**compared to earlier approaches.**

**Methodology**

**This methodology is divided into three main modules: voice recognition, face recog**

**nition, and score-level fusion.**

**Figure 2.8: Voice recognition process**

**Voice recognition begins with the acquisition of audio samples, which are then pro**

**cessed into Mel Frequency Cepstral Coefficients (MFCCs). The preprocessing pipeline**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**32**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**includes pre-emphasis to strengthen high-frequency components, framing the audio**

**into short segments, applying Hamming windows to reduce spectral leakage, and using**

**Fast Fourier Transform to convert signals into the frequency domain. Mel filters are**

**applied to model human auditory perception, and a Discrete Cosine Transform is used**

**to generate MFCCs. Cepstral Mean Subtraction and Cepstral Mean Variance Nor**

**malization further reduce noise and variability. These MFCCs are input to a Gaussian**

**Mixture Model, which estimates the probability distribution of speech features. During**

**authentication, the GMM calculates likelihood scores for the input and compares them**

**against stored models to verify identity.**

**Figure 2.9: Face recognition process**

**Face recognition begins with detection using the Haar Cascade classifier to isolate the**

**region of interest. The detected face is resized and fed into the FaceNet model, which**

**produces 128-dimensional embeddings. These embeddings are vector representations**

**of faces in a Euclidean space, where the distance between embeddings reflects facial**

**similarity. The embeddings are normalized using the L2 norm and then classified with**

**a Support Vector Machine. The strength of FaceNet lies in its ability to generate highly**

**discriminative embeddings, making it resistant to variations such as lighting and minor**

**pose changes. The final step is score-level fusion. The scores from voice and face**

**recognition are converted into probabilities and combined into a single fused score.**

**Since GMM outputs can be extreme, more weight was assigned to the FaceNet output**

**to balance the fusion. The final score determines whether authentication is accepted**

**or denied. The AVSpeech dataset was used to test the system. This dataset includes**

**thousands of YouTube video clips covering different languages, lighting conditions,**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**33**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**and background noises, ensuring robustness to real-world variability. Seven users were**

**selected for testing, with one hundred samples each, to validate the proposed system.**

**Results**

**The system achieved an Equal Error Rate of 0.13 for voice recognition using GMM,**

**0.22 for face recognition using FaceNet, and a remarkably low 0.011 for the fused**

**multimodal system. This shows that multimodal fusion significantly outperforms uni**

**modal recognition, especially under noisy or variable conditions. The performance**

**also exceeded that of previous studies using similar modalities.**

**However, the system depends on both modalities being available. If the user’s voice**

**is heavily distorted by background noise or if the face image is occluded or poorly**

**lit, recognition accuracy decreases. Another limitation is that voice recognition, while**

**strong, did not surpass the very best prior work due to slight differences in speech**

**preprocessing.**

**Summary of Findings**

**This paper \[12] summarizes that multimodal authentication integrating face and voice**

**is highly effective, with score-level fusion significantly reducing error rates. For Silen**

**tAuth, this work demonstrates the critical advantage of combining multiple biometric**

**modalities to improve reliability and security. The key takeaways for SilentAuth are**

**that multimodal fusion is essential for robust authentication, score-level fusion is a**

**practical and effective strategy for combining different traits, and integrating both**

**physiological traits like face and voice with behavioral traits like gestures can further**

**strengthen authentication. This directly validates the approach of SilentAuth as a**

**multimodal system that silently integrates gesture, face, and voice recognition for**

**secure identity verification.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**34**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**2.13 DynamicAudio-VisualBiometricFusionforPersonRecog**

**nition**

**Multimodal biometric systems combine independent traits (e.g. face and voice) to im**

**prove recognition robustness. Unimodal systems often fail under common challenges:**

**for face recognition, occlusions (like masks or sunglasses) can hide key features , and**

**for voice recognition, environmental noise can corrupt the signal . The COVID-19**

**pandemic has highlighted these issues: mandatory mask-wearing obscures the lower**

**face and filters speech acoustically . By fusing face and voice, errors in one modality**

**can be compensated bythe other . Indeed, multimodal integration of evidence typically**

**yields higher accuracy and reliability than any single modality . \[13]The goal is to**

**adaptively weight or select features from each modality based on quality, so that noise**

**or occlusion does not dominate the match.**

**Methodology**

**Occluded Face Recognition :**

**Numerous methods address face recognition under occlusion. \[13]Early approaches**

**segmented the face into blocks and discarded occluded parts. For example, one block**

**oriented method extracts HOG and LBP features from each block and applies sparse**

**reconstruction for identification . Other techniques focus on visible regions: attention**

**based CNNs that emphasize eye regions, or optimal cropping strategies, have shown**

**improved masked-face recognition . In one study, faces were divided into sub-images**

**and occluded blocks detected via eigenfaces; Gabor features were then extracted only**

**from unoccluded patches . Similarly, horizontal-split methods use pyramid HOG**

**features on the visible half-face , while deep Siamese networks learn a “mask dictio**

**nary” that maps occluded features to unoccluded ones . These works demonstrate that**

**ignoring or modeling occluded areas (e.g. masks, sunglasses, scarves) and extracting**

**features only from clear face regions can significantly boost recognition performance .**

**Noisy Voice Recognition :**

**Voice biometric systems suffer when background noise or low-quality recording condi**

**tions degrade the speech signal . Several studies have aimed to improve speaker recog**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**35**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**nition in noisy environments using feature engineering and noise modeling. A common**

**approach is to use Mel-Frequency Cepstral Coefficients (MFCCs)– which capture the**

**spectral envelope of speech– possibly in combination with other features. For instance,**

**a CNN-MFCC hybrid approach used deep features plus MFCCs to identify speakers**

**in noise, achieving about 87% accuracy . Another method combined standard MFCC**

**GMM models with GMMs trained on pitch-synchronous phase information, nearly**

**doubling accuracy from 32% to 62% in noise . Hybrid pipelines have also exploited**

**Gabor-filtered spectrograms and adaptive filtering: one system fused Gabor+CNN**

**features with recursive least-squares noise cancellation to improve recognition by 9%**

**over a baseline CNN . Even multi-resolution analysis (e.g. combining MFCC with**

**discrete wavelet transform features) has proven effective: fusing MFCCs with DWT**

**MFCC features and feature warping yielded high verification performance under var**

**ied noise and reverberation .**

**Proposed Algorithms: Feature Extraction and Fusion :**

**\[13]The proposed system uses face and voice at the feature fusion level, with dynamic**

**adaptation based on data quality . Face features are extracted in two ways: (1) using**

**Principal Component Analysis (PCA) to derive compact eigenface features , and (2)**

**using a bank of 2D Gabor filters to capture multiscale, multi-orientation textures .**

**Gabor features are known to perform well on faces, even under partial occlusion .**

**Voice features are standard MFCCs, encoding the spectral envelope of speech . The**

**fullfeature-level fusion simply concatenates the face and voice feature vectors into a**

**high-dimensional vector. However, to avoid dilution by bad data, two dynamic fusion**

**algorithms are introduced: Dynamic Size Fusion and Dynamic Weight Fusion.**

**Dynamic Size Fusion (Alg. 1): This algorithm adjusts the dimension of the fused**

**feature vector by removing low-quality components. Four cases are considered based**

**on probe quality:**

**Both Face \& Voice High-Quality: use the full face and voice feature vectors (standard**

**fusion).**

**Face High, Voice Noisy: keep the entire face feature vector, but reduce the voice vector**

**to its most salient features via PCA .**

**Face Occluded, Voice High: apply PCA to condense the face vector (dropping oc**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**36**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**cluded parts) and use the full voice vector .**

**Both Low-Quality: apply PCA to both face and voice vectors, selecting only the top**

**quality components .**

**In practice, an SVMdetector flags face occlusion (e.g. mask, sunglasses) and computes**

**speech SNR for the voice. If occlusion or low SNR is detected, the algorithm selects a**

**subset of features (top-k) from that modality, and it correspondingly resizes the training**

**templates . This produces a reduced-dimension fused feature that contains only high**

**quality information .**

**Dynamic Weight Fusion (Alg. 2): This algorithm uses fixed-length feature vectors, but**

**weights down the low-quality parts. Again four cases apply:**

**Both High-Quality: normalize all features and fuse normally.**

**Face Low, Voice High: occluded-face feature components are scaled by a factor be**

**tween 0 and 1 (determined empirically), reducing their influence ; voice features are**

**used normally. Face High, Voice Low: voice features are normalized and then multi**

**plied by a weight derived from the SNR (weight = SNR/20 ); face features are used**

**normally.**

**Both Low: scale occluded-face features and noisy-voice features by their respective**

**weights, while unoccluded-face features remain unchanged .**

**In effect, this down-weights all features coming from occluded regions or from noisy**

**speech , preventing them from misleading the classifier. After weighting, the face and**

**voice vectors are concatenated into a single feature vector.**

**Results**

**The authors \[13] evaluated identification and verification on AR, Extended Yale B,**

**and VOiCES datasets using face-only (PCA or Gabor), voice-only (MFCC), standard**

**feature fusion, and two dynamic fusion methods. Key findings include:**

**• Dynamic Size (Gabor+MFCC): Improved accuracy by 7% over standard fu**

**sion and outperformed unimodalbaselines (Gabor +8.4%, MFCC+43.6%). EER**

**on ARdropped from 0.077 to 0.041.**

**• Dynamic Size (PCA+MFCC): Accuracy improved 5.6% on AR and 8% on**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**37**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**Yale B; EERreductions showed excluding occluded/noisy features boosts recog**

**nition.**

**• DynamicWeight(Gabor+MFCC):Accuracyincreased 4.2%;bestYaleB+VOiCES**

**accuracy 96%, EER dropped to 0.05, AUC rose to 0.986.**

**• Dynamic Weight (PCA+MFCC): Top results with 95.7% identification accu**

**racy and EER of 0.016, significantly outperforming all baselines.**

**Limitations include:**

**Dependence on Data Quality: The performance of dynamic fusion algorithms relies**

**heavily on accurate assessment of input quality.**

**Feature-Level Fusion Challenges: Combining feature spaces can be difficult due to**

**unknown relationships between modalities, leading to dimensionality issues.**

**Weight and Size Accuracy: Proper selection of weights and sizes is crucial for optimal**

**dynamic fusion performance.**

**General Biometric Limitations: Multimodal systems remain vulnerable to real-world**

**factors such as occlusion, pose variations, illumination changes, and noise in voice**

**data.**

**Summary of Findings**

**This work \[13] demonstrates that dynamic feature-level fusion for face and voice**

**biometrics—adjusting feature vectors based on occlusion and noise—significantly im**

**proves recognition performance. The key takeaway is that quality-aware fusion, via dy**

**namicsize or weight adjustments, effectively handles low-quality inputs. The approach**

**can be extended to additional modalities, such as hand gestures, further enhancing**

**robustness when face or voice data are unreliable. Overall, adapting fusion to data**

**quality is crucial for building accurate and resilient multimodal biometric systems in**

**real-world scenarios.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**38**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**2.14 AMultimodal User Authentication System Using Faces**

**and Gestures**

**\[14]In ”A Multimodal User Authentication System Using Faces and Gestures,” Hyun**

**soek Choi and Hyeyoung Park propose a novel and cost-effective approach to user**

**authentication by fusing two heterogeneous biometric signals: a static, physical trait**

**(face) and a dynamic, behavioral trait (gesture). A key innovation of this system is that**

**both biometrics are captured using a single vision sensor, which significantly reduces**

**developmental and hardware costs compared to traditional multimodal systems that**

**require multiple sensors. The core motivation is to overcome the inherent vulner**

**abilities of unimodal systems, particularly the susceptibility of face recognition to**

**environmental factors like illumination and occlusion. By incorporating a changeable**

**behavioral signal like a gesture, the system provides a valuable countermeasure against**

**scenarios where physical information might be compromised, similar to how a user can**

**change a password.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**39**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**Methodology**

**Figure 2.10: Overall process of the multimodal biometric system**

**\[14]The system’s architecture is divided into three main components: a face repre**

**sentation module, a gesture representation module, and a decision module. During the**

**data registration phase, both face and gesture information are extracted from a video**

**and stored as feature matrices in a user database. In the subsequent authentication**

**phase, a new video is processed in the same way, and the resulting feature matrices**

**are compared against the registered data to determine authenticity. A notable technical**

**detail is that the system utilizes a common feature extraction method for both modal**

**ities, which simplifies the overall process and reduces implementation costs. For data**

**representation, the authors \[14] employed the Histogram of Oriented Gradients (HOG)**

**descriptor for both face and gesture analysis. For faces, the Viola-Jones detector first**

**locates the face, which is then resized and divided into a grid. The HOG descriptor is**

**applied to create a 16x31 feature matrix. For gestures, a frame differencing technique**

**is used to detect movement, and HOG is then applied to these different images. This**

**results in a gesture feature matrix where the number of rows (T) depends on the video**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**40**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**length. The decision module is designed to maintain the spatial locality of facial**

**features and the sequential relationship of gesture frames by directly using the feature**

**matrices rather than vectorizing them. The authors proposed a matrix correlation**

**distance measure for this purpose. To handle the varying lengths of gesture videos,**

**they incorporated the Dynamic Time Warping (DTW) algorithm to align the gesture**

**feature matrices before calculating the distance. The final authentication decision is**

**made using a likelihood ratio calculated from the face and gesture distances, assuming**

**a Gaussian distribution for the authentic and impostor data.**

**Figure 2.11: Process of the face representation module**

**Results**

**The experimental results, conducted on the ChaLearn database using only RGB sig**

**nals, demonstrate that the multimodal system is significantly superior to unimodal**

**systems. \[14]The proposed system achieved an average Equal Error Rate (EER) as low**

**as 0.64%, while the best unimodal gesture and face systems had EERs of 2.94% and**

**5.99%, respectively. The authors also showed that the proposed matrix correlation dis**

**tance measure was more effective than conventional Euclidean or Manhattan distances**

**for their system. The performance gains are attributed to the near-independence of the**

**two modalities, with an average correlation coefficient of 0.19, which is a desirable**

**property for multimodal fusion. The primary limitation noted in this paper \[14] is that**

**the proposed system’s performance is susceptible to various environmental factors,**

**such as illumination, facial expressions, pose, and occlusion, which are common chal**

**lenges for face recognition systems. The paper also suggests that more comprehensive**

**studies on feature extraction and classification are needed to prepare the system for**

**real-world applications.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**41**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**Summary of Findings**

**To summarize, this research \[14] presents a simple, effective, and cost-efficient mul**

**timodal biometric system for user authentication. The key achievement is the sys**

**tem’s ability to utilize both face and gesture information from a single vision sensor,**

**eliminating the need for expensive, multiple sensors. The methodology shows how to**

**capture and represent both types of biometric data from a video stream. It leverages**

**the fact that a single camera can acquire both physical (face) and behavioral (gesture)**

**information simultaneously. The use of gestures, which can be changed by the user,**

**provides a valuable security layer that can counter the vulnerability of fixed physical**

**information like faces. This dual-modality approach, combined with a specialized**

**distance measure, significantly improves authentication performance compared to uni**

**modal systems. The system’s design makes it particularly suitable for integration into**

**common smart devices, such as smart TVs, where a single vision sensor is readily**

**available.**

**2.15 AMultimodalBiometricSystemUsingFingerprint,Face,**

**and Speech**

**\[15]Traditional authentication based on passwords and tokens faces issues like for**

**getting, theft, or impersonation, making them insufficient for sensitive applications.**

**Biometric systems, which use physiological or behavioral traits, overcome these draw**

**backs thanks to improved reliability and discrimination power. Integrating multiple**

**biometric modalities addresses the limitations of any single trait, creating robust secu**

**rity for real-world scenarios.**

**Methodology**

**This paper \[15] presents a multimodal system combining three biometrics: fingerprint,**

**face, and speech.**

**• Fingerprints are processed using minutiae extraction and pattern matching.**

**• Face recognition employs the eigenface approach for comparing facial features.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**42**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**• Speaker verification uses hidden Markov models to analyze speech signal pat**

**terns.**

**Each module independently scores user authenticity; a final decision fuse combines**

**these scores at the decision level using statistical methods, ensuring accuracy and**

**versatility for varied conditions.**

**Results**

**Tests on asmallset of 50users(with hundredsofsampleseachforfingerprint, face, and**

**speech) demonstrated that fusing multiple biometrics substantially improves reliability**

**compared to individual methods. The system features low false acceptance and rejec**

**tion rates. Limitations include restricted sample sizes and controlled lab environments,**

**so real-world performance and scalability require further validation.**

**Summary of Findings**

**Multimodal biometric fusion yields higher verification accuracy and greater robustness**

**than single-modality systems \[15]. For projects like SilentAuth, integrating diverse**

**biometric indicators allows strong, user-friendly authentication even when one trait is**

**unavailable or compromised—key for practical, secure applications. Decision fusion,**

**modular biometrics, and adaptability are relevant takeaways.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**43**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**CHAPTER3**

**METHODOLOGY**

**3.1 Technical Approach and Design Rationale**

**The SilentAuth framework is designed as a multimodal biometric authentication sys**

**tem grounded in deep representation learning, metric-based verification, and adaptive**

**decision-level fusion. The fundamental design philosophy of the system is to move**

**away from traditional identity classification models and instead adopt an embedding**

**driven open-set verification paradigm.**

**Rather than predicting a fixed identity label during inference, SilentAuth transforms**

**each biometric input into a structured numerical representation within a learned feature**

**space. These representations, commonly referred to as embeddings, encode identity**

**specific characteristics while suppressing irrelevant variations caused by environmen**

**tal noise, pose differences, or content variability. Authentication is therefore formu**

**lated as a similarity comparison problem in a normalized embedding space.**

**A key design decision in SilentAuth is the adoption of open-set recognition. In real**

**world authentication systems, it cannot be assumed that every input belongs to a**

**previously enrolled identity. Therefore, the system performs 1-vs-N identity com**

**parison under a threshold-based acceptance rule. Authentication is granted only if the**

**similarity between a query sample and an enrolled template exceeds a predefined con**

**f**

**idence threshold. This prevents forced identity assignment and strengthens resistance**

**to impersonation attacks.**

**Another important design consideration is modality heterogeneity. Face and voice**

**recognition operate using deep metric learning–based embeddings, while gesture recog**

**nition follows a structured landmark-based classification approach. Instead of forc**

**ing uniformity across modalities, SilentAuth intentionally preserves modality-specific**

**strengths and integrates them at the decision level. This design improves modularity**

**and allows each biometric technique to operate using its most effective recognition**

**paradigm.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**44**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**The framework also incorporates preset-driven accessibility logic. Since users may**

**have varying physical abilities, SilentAuth introduces adaptive modality selection.**

**This ensures that authentication remains secure while accommodating user-specific**

**constraints. Overall, the technical approach prioritizes robustness, scalability, parallel**

**processing capability, and accessibility-aware fusion within a distributed multimodal**

**environment.**

**3.2 Overall System Framework**

**Figure 3.1: System Architecture**

**The overall framework of SilentAuth is designed as a structured multimodal authen**

**tication architecture integrating face, voice, and gesture recognition into a unified de**

**cision system. As illustrated in the system architecture diagram Figure 4.1, biometric**

**inputs are captured from the user and routed to their respective recognition modules.**

**Each modality functions as an independent processing unit, extracting identity-specific**

**representations and generating a confidence score indicating the likelihood of a match**

**with stored user profiles.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**45**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**At the core of the framework lies the Central Recognition System, which coordinates**

**identity comparison across enrolled users. During authentication, each modality per**

**forms similarity-based matching against the stored biometric templates under an open**

**set recognition approach. Instead of forcing classification into a predefined class, the**

**system evaluates whether the similarity score satisfies predefined acceptance thresh**

**olds before considering the identity valid.**

**The outputs generated by the individual modalities are forwarded to the Adaptive Fu**

**sion Engine. This component performs score-level fusion by aggregating normalized**

**confidencevalues fromtheactive modalities. The fusion mechanism assigns weights to**

**each modality and computes a combined authentication score. The weighting scheme**

**dynamically adjusts based on preset configurations, ensuring accessibility support for**

**users with motor or voice impairments.**

**Finally, the fused score is compared against a global decision threshold to determine**

**authentication success or failure. By separating modality-specific processing from cen**

**tralized decision logic, the framework ensures modularity, scalability, and robustness.**

**The architectural design enables independent modality operation while maintaining a**

**unified and secure authentication pipeline.**

**3.3 Multimodal Enrollment Strategy**

**Theenrollment strategy in SilentAuth is structured as a preset-driven multimodal regis**

**tration process designed to establish a stable and unified digital identity profile across**

**selected biometric modalities. The primary objective of the enrollment phase is to**

**create consistent identity references that can be reliably used during subsequent au**

**thentication sessions. Unlike conventional systems that treat each biometric modality**

**independently, SilentAuth integrates enrollment under a centralized identity associa**

**tion mechanism.**

**At the beginning of the enrollment process, users are required to select a preset con**

**f**

**iguration. This preset determines which biometric modalities will be active during**

**authentication. The preset-driven mechanism ensures that enrollment is aligned with**

**user capability, accessibility requirements, and contextual constraints. By defining**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**46**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**modality participation at the registration stage, the system avoids unnecessary bio**

**metric capture and maintains consistency between enrollment configuration and future**

**verification logic.**

**Oncethe preset is selected, the system generates a unique user identifier. This identifier**

**functions as the primary reference key for all modality-specific records associated with**

**the individual. Instead of storing separate and unrelated biometric entries, SilentAuth**

**maintains a structured one-to-many identity mapping. A single user identifier links**

**to multiple modality records depending on the chosen preset. This structured link**

**age guarantees cross-modal identity coherence and prevents ambiguity in multimodal**

**authentication.**

**The enrollment phase focuses on generating and storing modality-specific representa**

**tions in a structured repository. Rather than preserving raw biometric inputs, Silen**

**tAuth stores only processed identity representations. This design choice strengthens**

**privacy protection and reduces storage complexity. By limiting stored data to struc**

**tured templates or predefined associations, the system minimizes exposure to raw**

**biometric data leakage while maintaining verification efficiency.**

**The enrollment workflow also incorporates validation checks to ensure that captured**

**data satisfies predefined quality standards. These checks confirm that the acquired**

**biometric samples meet clarity, completeness, and usability criteria before being per**

**manently linked to the user identifier. Enforcing quality validation during enrollment**

**improves long-term authentication stability and reduces the probability of false rejec**

**tion during verification.**

**Additionally, the preset-driven enrollment structure supports system scalability. New**

**modalities can be integrated into the framework without disrupting existing user records,**

**as each modality operates as an independent extension linked through the central**

**identity identifier. This modular association model ensures future expandability while**

**maintaining structural integrity.**

**In general, the multimodal enrollment strategy ensures:**

**• Structured identity linkage through a unique user identifier.**

**• Modality configuration aligned with Preset.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**47**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**• Centralized but modular data association.**

**• Privacy-conscious template storage**

**• Quality-controlled identity registration**

**• Scalability for future modality integration**

**3.4 Face Recognition Methodology**

**The face recognition module in SilentAuth is implemented using deep metric learning**

**through the InsightFace framework, specifically utilizing an ArcFace-trained convo**

**lutional neural network model. The system does not perform identity classification**

**during inference; instead, it generates normalized 512-dimensional facial embeddings**

**that represent unique identity characteristics in a hyperspherical feature space.**

**ArcFace enhances discriminative learning by introducing an additive angular margin**

**penalty during training. This margin enforces greater angular separation between iden**

**tity classes in the embedding space. As a result, facial samples belonging to the same**

**individual form compact clusters, while samples from different individuals remain**

**clearly separated. This geometric separation improves resilience to pose variation,**

**illumination differences, and facial expression changes.**

**During verification, SilentAuth operates under an open-set 1-vs-N identification strat**

**egy. A live facial image is processed through the trained network to produce its**

**embedding vector. This embedding is then compared with stored identity templates**

**using cosine similarity:**

**Similarity(f, fi) = f · fi**

**∥f∥∥fi∥**

**(3.1)**

**Because embeddings are L2-normalized, cosine similarity effectively measures angu**

**lar closeness on a hypersphere. The similarity score ranges from 1 to 1, with higher**

**values indicating stronger identity correspondence. The identity associated with the**

**highest similarity score that exceeds a predefined decision threshold is selected as the**

**authentication result. If no similarity score satisfies the threshold, the system rejects**

**the authentication attempt.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**48**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**Bycombiningdeepconvolutional feature extraction, angular-margin-based embedding**

**optimization, and similarity-driven open-set verification, the face module provides a**

**scalable, high-accuracy foundation within the SilentAuth multimodal authentication**

**framework.**

**3.5 Voice Recognition Methodology**

**The voice authentication module is formulated as a deep speaker representation learn**

**ing problem. Instead of comparing raw waveforms or spectral patterns directly, Silen**

**tAuth employs high-level speaker embeddings generated using the ECAPA-TDNN**

**architecture.**

**ECAPA-TDNN extends traditional Time Delay Neural Networks by incorporating**

**channel attention mechanisms, multi-layer feature aggregation, and enhanced temporal**

**modeling. This architecture enables the network to capture long-range contextual**

**information while emphasizing frequency channels that contribute most significantly**

**to speaker discrimination. As a result, the model becomes more robust to phonetic**

**variation and environmental noise.**

**From a methodological perspective, ECAPA-TDNN functions within a deep metric**

**learning framework. It learns a nonlinear transformation that maps acoustic features**

**into a normalized embedding space where intra-speaker variability is minimized and**

**inter-speaker variability is maximized. Channel-dependent attention pooling aggre**

**gates frame-level representations into a fixed-dimensional speaker embedding, pre**

**serving identity-specific acoustic characteristics while reducing content dependency.**

**Verification is performed using cosine similarity between the query speaker embedding**

**and stored identity templates. Since embeddings lie on a normalized hypersphere,**

**angular similarity provides a stable geometric interpretation of speaker closeness. A**

**threshold-based decision mechanism regulates acceptance and rejection by balancing**

**False Acceptance Rate (FAR) and False Rejection Rate (FRR). This embedding-based**

**approach enables text-independent, real-time speaker verification suitable for multi**

**modal authentication integration.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**49**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**3.6 Gesture Recognition Methodology**

**The gesture recognition module in SilentAuth adopts a landmark-based geometric**

**representation combined with supervised classification. Instead of analyzing full**

**resolution pixel data, the system utilizes MediaPipe Hands to extract structured anatom**

**ical keypoints representing the hand skeleton. MediaPipe operates through a two-stage**

**deep learning pipeline involving palm detection followed by landmark regression.**

**The model outputs 21 three-dimensional landmark coordinates corresponding to finger**

**joints and palm structure. This structured skeletal representation significantly reduces**

**sensitivity to background noise, lighting variations, and scale differences.**

**The extracted landmark coordinates are transformed into organized feature vectors**

**describing spatial relationships and joint configurations. These feature vectors are**

**input to a Support Vector Machine (SVM) classifier. The SVM is selected due to**

**its strong margin-maximizing properties, which enhance class separability in high**

**dimensional feature space. Its ability to generalize well with limited training data**

**makes it appropriate for predefined gesture classification.**

**During verification, the predicted gesture label is compared against the user’s reg**

**istered gesture. Authentication succeeds only when the predicted class matches the**

**enrolled label. Although gesture recognition does not generate identity embeddings**

**like face and voice modules, it provides an additional active verification layer that**

**strengthens the overall multimodal authentication process.**

**3.7 Parallel Multimodal Verification Strategy**

**The verification phase of SilentAuth is structured as a parallel multimodal authentica**

**tion framework designed to ensure real-time responsiveness, computational efficiency,**

**and scalable identity validation. Unlike traditional sequential verification systems,**

**where biometric modalities are evaluated one after another, SilentAuth processes all**

**active modalities simultaneously. This parallel execution model significantly reduces**

**total authentication latency and prevents bottlenecks that could arise from modality**

**dependency.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**50**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**The decision to adopt parallel verification is rooted in performance optimization and**

**reliability considerations. In sequential systems, a delay or failure in one modality can**

**block the entire authentication pipeline. By contrast, SilentAuth treats each biometric**

**modality as an independent verification channel operating concurrently. This indepen**

**dence enhances fault tolerance and ensures that temporary performance degradation in**

**one modality does not stall the entire authentication process.**

**The verification workflow follows a distributed producer–consumer architecture. In**

**this model, biometric acquisition components act as producers, continuously capturing**

**live data streams, while inference components function as consumers that process**

**incoming data independently. Visual modalities—face and gesture—operate on real**

**time video streams, extracting relevant frames for inference. The voice modality**

**processes audio input separately, handling temporal acoustic data independently from**

**visual streams. This separation ensures true computational parallelism at both data**

**acquisition and inference stages.**

**A key optimization in the verification process is indexed candidate filtering. When**

**gesture recognition produces a classification output, the result is immediately matched**

**against a pre-indexed user set using hash-based indexing. This allows constant-time**

**(O(1)) candidate retrieval. Instead of comparing the query sample against all enrolled**

**identities, the system narrows the candidate pool based on gesture association. This**

**significantly reduces computational complexity in large-scale identity repositories.**

**Following indexed retrieval, identity refinement is performed through set-based in**

**tersection across modalities. Candidate identity lists derived from face and voice**

**similarity evaluation are intersected with the gesture-based candidate set. This struc**

**tured reduction of the search space minimizes unnecessary similarity comparisons**

**and enhances decision efficiency. By progressively narrowing candidate identities**

**through logical set operations, the system maintains both computational scalability**

**and decision accuracy.**

**Each active modality produces a normalized confidence score reflecting the strength**

**of identity correspondence. These scores are transmitted to a central coordination**

**component responsible for asynchronous aggregation. The asynchronous collection**

**mechanism ensures that faster modalities do not wait for slower ones unnecessarily.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**51**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**Instead, score aggregation occurs once all active modality outputs are available or after**

**predefined synchronization constraints are satisfied.**

**This structured parallel verification methodology provides several advantages:**

**• Reduced authentication latency through simultaneous inference**

**• Improved scalability for large identity databases**

**• Efficient candidate space reduction using indexed filtering**

**• Fault tolerance through modality independence**

**• Asynchronous score aggregation to prevent processing delays**

**3.8 Adaptive Preset-Based Score-Level Fusion**

**SilentAuth employs a preset-driven adaptive score-level fusion mechanism to integrate**

**heterogeneous biometric evidence. Since different modalities exhibit varying reliabil**

**ity and discriminative power, authentication is modeled as a weighted aggregation of**

**normalized modality scores.**

**Under the standard configuration, face recognition is assigned weight 0.5 due to its**

**strong embedding separability and stability. Voice recognition receives weight 0.3,**

**reflecting its high discriminative power but sensitivity to environmental noise. Gesture**

**recognition contributes weight 0.2 as a supplementary authentication factor. The fused**

**score is computed as:**

**S =(wf sf) + (wv sv) + (wg sg)**

**where sf, sv, and sg represent normalized confidence scores for face, voice, and ges**

**ture respectively. Preset-based recalibration ensures accessibility support. For voice**

**impaired users, fusion weights are adjusted to 0.7 (face) and 0.3 (gesture). For motor**

**impaired users, gesture is excluded and weights are adjusted to 0.6 (face) and 0.4**

**(voice). Threshold values are also slightly modified (e.g., T = 0.55) to maintain con**

**sistent decision sensitivity when fewer modalities contribute.**

**Authentication is granted when the fused score exceeds the preset-specific threshold.**

**This adaptive weighting and threshold calibration framework ensures statistical con**

**sistency, inclusivity, and robust multimodal identity verification.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**52**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**CHAPTER4**

**IMPLEMENTATION**

**4.1 Development Environment and System Setup**

**For the implementation of the SilentAuth system, a dedicated virtual environment**

**was created to isolate dependencies and ensure stable deployment across different**

**systems.The backend services were developed using FastAPI, which enabled modu**

**lar microservice-based implementation of face, voice, and gesture processing units.**

**Uvicorn, an ASGI server, was used to handle asynchronous request–response cy**

**cles efficiently. This ensured non-blocking execution during real-time verification.For**

**inter-service communication and real-time streaming, ZeroMQ (ZMQ) was integrated**

**using a PUB-SUB (Publisher–Subscriber) model. The camera service acts as the**

**producer, while face and gesture modules function as subscribers consuming frames**

**independently.**

**The system integrates the following core libraries:**

**• InsightFace (ArcFace model) for face embeddings**

**• ONNXRuntime for efficient model inference**

**• ECAPA-TDNNmodel for speaker embedding generation**

**• Librosa / SoundDevice / PyAudio**

**• MediaPipe Hands for real-time hand landmark extraction**

**• Scikit-learn for SVM-based gesture classification**

**• NumPyfor numerical computation**

**• SQLite3 for template and preset storage 1**

**• Joblib for model persistence**

**• OpenCVfor video frame acquisition and preprocessing**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**53**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**Hardware requirements included a standard webcam and microphone to enable con**

**tactless biometric acquisition.**

**4.2 Face Recognition Module Implementation**

**The face recognition module was implemented using the InsightFace framework with**

**the pre-trained ArcFace (buffalo-l) model for feature extraction. The FaceAnalysis**

**pipeline provided by InsightFace was initialized to perform both face detection and**

**embedding generation in a unified workflow. The model was configured to run using**

**ONNX Runtime on CPU to ensure compatibility across systems without requiring**

**dedicated GPU hardware.**

**Live video frames were captured using OpenCV and streamed into the face processing**

**service. Each frame was preprocessed internally by the InsightFace detection pipeline,**

**which identified facial regions and aligned them automatically before embedding ex**

**traction. For every detected face, a 512-dimensional feature embedding was generated.**

**These embeddings were L2-normalized to ensure stable cosine similarity computation**

**during matching.**

**During enrollment, the extracted embedding vector was associated with a unique userid**

**and stored in the Biometric Template Layer (SQLite database). Only numerical em**

**beddings were persisted, and raw image data was not stored, thereby reducing storage**

**overhead and improving privacy protection.**

**During verification, a live embedding was generated from the incoming frame and**

**compared against all stored identity templates using cosine similarity. Similarity com**

**putation was implemented using NumPy vector operations for efficient numerical pro**

**cessing. The module follows an open-set 1-vs-N identification approach, where the**

**query embedding is compared against all enrolled templates. The identity correspond**

**ing to the highest similarity score exceeding the configured threshold is selected as the**

**predicted match. If no score exceeds the threshold, authentication is rejected.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**54**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**4.3 Voice Recognition Module Implementation**

**The voice authentication module was implemented using a pre-trained ECAPA-TDNN**

**speaker embedding model, integrated into the system as an independent service. Audio**

**input was captured through the system microphone using appropriate Python audio**

**handling libraries and converted into waveform format for processing.**

**The captured audio signal was passed to the ECAPA-TDNN model to generate a fixed**

**dimensional speaker embedding representing the user’s vocal characteristics. These**

**embeddings were L2-normalized to maintain geometric consistency in the similarity**

**space. During enrollment, the normalized embedding was stored in the biometric**

**template database and linked to the corresponding user identifier.**

**During verification, real-time audio input was processed to generate a query embed**

**ding using the same inference pipeline. The implementation supports text-independent**

**speaker verification, meaning users are not restricted to a predefined passphrase. This**

**improves usability and flexibility during authentication.**

**Similarity matching was performed using cosine similarity between the query embed**

**ding and stored templates. NumPy-based vector operations were used for efficient**

**computation. The highest similarity score was compared against a predefined threshold**

**to determine authentication success. The module outputs a normalized confidence**

**score, which is forwarded to the fusion engine for multimodal decision aggregation.**

**4.4 Gesture Recognition Module Implementation**

**The gesture recognition module was implemented using MediaPipe Hands for real**

**time hand landmark detection and Scikit-learn’s Support Vector Machine (SVM) clas**

**sifier for gesture classification. The module operates as a separate processing service**

**within the distributed system.**

**Live video frames were streamed from the camera service using ZeroMQ(ZMQ)PUB**

**SUB architecture. The gesture module subscribes to the latest available frame and**

**processes it independently. MediaPipe detects a single hand per frame and extracts 21**

**three-dimensional landmark coordinates, representing key joint positions of the hand.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**55**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**The extracted landmark coordinates were normalized to ensure invariance to scale and**

**position changes. These normalized coordinates were flattened into a structured feature**

**vector, which served as input to the trained SVM classifier. The SVM model was**

**trained on gesture-specific landmark datasets and persisted using Joblib for runtime**

**loading.**

**During verification, the predicted gesture label was used to retrieve candidate users**

**through a hash-based indexing mechanism. Gesture labels were mapped to user iden**

**tifiers using dictionary-based indexing, enabling constant-time (O(1)) candidate re**

**trieval. This significantly reduces the identity search space before deeper matching is**

**performed by face and voice modules.**

**Gesture recognition functions as both a behavioral biometric component and a lightweight**

**liveness indicator, strengthening the overall robustness of the multimodal authentica**

**tion process.**

**4.5 Multimodal Enrollment and Verification Engines**

**4.5.1 Sequential Enrollment Engine**

**Figure 4.1: Enrollment Pipeline**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**56**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**Figure 4.2: Verification Pipeline**

**The enrollment workflow was implemented as a sequential runner engine exposed**

**through a FastAPIendpoint. Users select a preset configuration (normal, voice-impaired,**

**or motor-impaired), which is stored in the SQLite database. Based on the selected**

**preset, modalities are executed sequentially to ensure controlled and stable biometric**

**capture. Each registration service generates its respective template and writes it to the**

**Biometric Template Layer.Sequential execution was intentionally chosen to prevent**

**concurrent capture conflicts and ensure high-quality template generation.**

**4.5.2 Parallel Verification Engine**

**The verification pipeline was implemented as a parallel execution framework coor**

**dinated by a Multimodal Parallel Executor.The camera service streams frames using**

**ZMQPUB-SUB architecture. Face and gesture modules consume the latest available**

**frame independently. The voice module processes audio input in parallel. Each modal**

**ity operates in a separate runtime context and produces a normalized confidence score.**

**Gesture-based candidate retrieval reduces the identity search space through indexed**

**lookup. Further refinement is performed using set intersection across modality out**

**puts.Results from all active modalities are asynchronously aggregated and forwarded**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**57**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**to the Adaptive Fusion Engine without blocking dependencies.**

**4.6 Adaptive Fusion and Decision Logic Implementation**

**The Adaptive Fusion Engine was implemented as a centralized decision component.**

**It receives normalized confidence scores from active modalities.Weighted score ag**

**gregation was implemented using preset-dependent weight configuration stored in the**

**database. For example:**

**• Normal preset: Face (0.5), Voice (0.3), Gesture (0.2)**

**• Voice impaired preset: Face (0.7), Gesture (0.3)**

**• Motor impaired preset: Face (0.6), Voice (0.4)**

**The final authentication score is computed as a weighted linear combination of active**

**modality scores. The decision module compares this score against a configurable**

**threshold (e.g., 0.60 or 0.55 depending on preset).The system outputs a structured**

**authentication response indicating identity and success or failure status.**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**58**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**

**CHAPTER5**

**CONCLUSIONANDFUTURESCOPE**

**5.1 Conclusion**

**In conclusion, the proposed multimodal biometric authentication system provides a**

**comprehensive and reliable solution for secure user verification by integrating face,**

**gesture, and voice modalities \[1,3,4]. The system’s modular architecture ensures that**

**each component—input acquisition, preprocessing, recognition, fusion, and decision**

**making—functions efficiently while maintaining flexibility for future enhancements.**

**By employing advanced techniques such as feature extraction, embedding generation,**

**and hybrid fusion, the system achieves high accuracy, robustness, and adaptability**

**to varying environmental conditions and user behaviors. Additionally, the design**

**incorporates considerations for accessibility, allowing users with speech or mobility**

**limitations to authenticate effectively, highlighting the system’s inclusive approach \[7,**

**8,13,15]. Overall, this project establishes a strong foundation for deploying practical,**

**scalable, and secure biometric authentication systems in real-world applications.**

**5.2 Future Improvements and Enhancements**

**For future development, the system can be extended to include additional biomet**

**ric modalities such as iris, palm vein, or gait recognition to enhance security and**

**accuracy \[7–9, 12, 15]. The fusion and decision-making mechanisms can be made**

**adaptive using machine learning models that adjust weights and thresholds based on**

**user-specific patterns and conditions. Enhanced fallback strategies can handle scenar**

**ios where one or more modalities are unavailable, ensuring seamless authentication.**

**Anti-spoofing and liveness detection can be incorporated to prevent fraudulent access**

**using photos, videos, or synthetic data \[5,6,19,24]. Integration with cloud platforms**

**and IoT ecosystems can enable scalable deployment, while further research into real**

**time monitoring, anomaly detection, and privacy-preserving techniques can make the**

**system more robust and intelligent \[7,8,10,13,15].**

**DEPARTMENTOFCOMPUTERSCIENCEANDENGINEERING**

**59**

**SILENTAUTH- MULTIMODALBIOMETRICAUTHENTICATIONSYSTEM**



