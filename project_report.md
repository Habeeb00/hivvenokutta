**CONTENTS**

**ACKNOWLEDGEMENT**

**ABSTRACT**

**LIST OF FIGURES**

**LIST OF ABBREVIATIONS**

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

**2 LITERATURE REVIEW**

**2.1 Deep Learning for De Novo Drug Design . . . . . . . . . . . . . . .**

**2.2 Generative Models for Molecular Design Using SMILES . . . . . . .**

**7**

**7**

**9**

**2.3 LSTM-Based Molecular Generation for Drug Discovery . . . . . . . . 12**

**2.4 Recurrent Neural Networks for SMILES-Based Molecule Generation . . 15**

**2.5 Molecular Docking Using AutoDock Vina for Virtual Screening . . . . 17**

**2.6 Computational Approaches to Molecular Docking in Drug Discovery . 21**

**2.7 A Survey on ADMET Prediction Using Machine Learning and**

**Deep Learning . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 22**

**2.8 Quantitative Estimation of Drug-Likeness and Pharmacokinetic**

**Profiling Using RDKit . . . . . . . . . . . . . . . . . . . . . . . . . 24**

**2.9 Synthetic Accessibility Score Estimation for Drug-Like Molecules . . 25**

**2.10 Computational Retrosynthetic Analysis for Drug Development . . . . 28**

**iii**

**2.11 Quantum Chemistry in Drug Discovery: HOMO-LUMO Analysis . . 31**

**2.12 AI-Driven Drug Discovery Pipelines for HIV-1 Protease**

**Inhibitors . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 32**

**2.13 Multi-Objective Optimization in Computational Drug Design . . . . . 35**

**2.14 Lipinski's Rule of Five and Drug-Likeness Filtering . . . . . . . . . 39**

**2.15 HIV-1 Protease Inhibitors: From Design to Clinical Application . . . 42**

**3 METHODOLOGY**

**44**

**3.1 Technical Approach and Design Rationale . . . . . . . . . . . . . . . 44**

**3.2 Overall System Framework . . . . . . . . . . . . . . . . . . . . . . . 45**

**3.3 Data Collection and Preprocessing Strategy . . . . . . . . . . . . . . 46**

**3.4 LSTM-Based Molecular Generation Methodology . . . . . . . . . . . 48**

**3.5 Molecular Docking Methodology . . . . . . . . . . . . . . . . . . . 49**

**3.6 ADMET Prediction Methodology . . . . . . . . . . . . . . . . . . . 50**

**3.7 Synthesizability Assessment Methodology . . . . . . . . . . . . . . . 50**

**3.8 Multi-Criteria Weighted Ranking and Fusion Strategy . . . . . . . . . 52**

**4 IMPLEMENTATION**

**53**

**4.1 Development Environment and System Setup . . . . . . . . . . . . . 53**

**4.2 LSTM Model Training and Molecule Generation . . . . . . . . . . . 54**

**4.3 Drug-Likeness Filtering Implementation . . . . . . . . . . . . . . . . 55**

**4.4 Quantum Chemistry Module Implementation . . . . . . . . . . . . . 55**

**4.5 Streamlit Web Dashboard Implementation . . . . . . . . . . . . . . . 56**

**4.5.1**

**4.5.2**

**Discovery and Visualization Engine . . . . . . . . . . . . . . 56**

**Multi-Stage Evaluation Pipeline . . . . . . . . . . . . . . . . 57**

**4.6 Final Ranking and Composite Score Implementation . . . . . . . . . 58**

**5 CONCLUSION AND FUTURE SCOPE**

**59**

**5.1 Conclusion . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 59**

**5.2 Future Improvements and Enhancements . . . . . . . . . . . . . . . . 59**

**REFERENCES**

**60**

**LIST OF FIGURES**

**2.1 Architecture of deep generative models for de novo drug design . . . .**

**7**

**2.2 SMILES representation and molecular graph conversion pipeline . . . 10**

**2.3 LSTM-based molecular generation process . . . . . . . . . . . . . . . 13**

**2.4 RNN architecture for character-level SMILES generation . . . . . . . 16**

**2.5 AutoDock Vina molecular docking workflow . . . . . . . . . . . . . . 23**

**2.6 ADMET prediction pipeline using molecular descriptors . . . . . . . . 26**

**2.7 Synthetic accessibility scoring framework . . . . . . . . . . . . . . . 29**

**2.8 Quantum chemistry energy level computation process . . . . . . . . . 32**

**2.9 AI-driven drug discovery pipeline for HIV-1 protease . . . . . . . . . 33**

**2.10 Multi-criteria drug candidate evaluation framework . . . . . . . . . . 40**

**2.11 Lipinski Rule of Five filtering process . . . . . . . . . . . . . . . . . 41**

**3.1 System Architecture . . . . . . . . . . . . . . . . . . . . . . . . . . . 45**

**4.1 AI Pipeline Workflow . . . . . . . . . . . . . . . . . . . . . . . . . . 56**

**4.2 Streamlit Dashboard Architecture . . . . . . . . . . . . . . . . . . . 57**

**v**

**LIST OF ABBREVIATIONS**

**LSTM Long Short-Term Memory Network**

**SMILES Simplified Molecular-Input Line-Entry System**

**CNN Convolutional Neural Network**

**RNN Recurrent Neural Network**

**ADMET Absorption, Distribution, Metabolism, Excretion, Toxicity**

**QED Quantitative Estimation of Drug-Likeness**

**SA Synthetic Accessibility**

**HOMO Highest Occupied Molecular Orbital**

**LUMO Lowest Unoccupied Molecular Orbital**

**PDB Protein Data Bank**

**PI Protease Inhibitor**

**HIV Human Immunodeficiency Virus**

**LogP Logarithm of Partition Coefficient**

**MW Molecular Weight**

**HBD Hydrogen Bond Donors**

**HBA Hydrogen Bond Acceptors**

**TPSA Topological Polar Surface Area**

**BBB Blood-Brain Barrier**

**SVM Support Vector Machine**

**PCA Principal Component Analysis**

**vi**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**CHAPTER 1**

**INTRODUCTION**

**In the contemporary landscape of pharmaceutical research, the design and development of effective antiviral drugs remains one of the most pressing scientific challenges. The Human Immunodeficiency Virus type 1 (HIV-1) continues to be a global health crisis, affecting millions of people worldwide despite decades of research. While existing antiretroviral therapies have significantly improved patient outcomes, the continuous emergence of drug-resistant viral strains demands the discovery of novel inhibitors targeting critical viral enzymes.**

**Traditional drug discovery is an exceptionally slow and expensive process, often spanning 10 to 15 years and costing billions of dollars from initial concept to market approval. The majority of drug candidates fail during clinical trials due to poor efficacy, unfavorable pharmacokinetic properties, or unexpected toxicity. These challenges highlight the urgent need for more efficient, data-driven approaches to accelerate the identification of promising therapeutic molecules.**

**Artificial intelligence and deep learning have recently emerged as transformative technologies in computational drug discovery. By leveraging large molecular datasets and advanced neural network architectures, AI systems can learn the underlying chemical grammar of drug-like molecules and generate entirely novel chemical structures with desired properties. This paradigm shift from traditional high-throughput screening to generative molecular design promises to dramatically reduce both the time and cost of early-stage drug discovery.**

**This project, titled DENOVO : AI-Driven Drug Discovery for HIV-1 Protease Inhibitors, focuses on developing an end-to-end computational drug discovery pipeline that leverages Long Short-Term Memory (LSTM) neural networks to generate novel candidate molecules targeting HIV-1 Protease. The generated candidates are subsequently evaluated through a comprehensive multi-stage assessment framework encompassing drug-likeness filtering, quantum chemistry analysis, molecular docking, ADMET profiling, synthesizability scoring, and a final weighted composite ranking to identify the most promising lead compounds for further experimental validation.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**1**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**1.1 Problem Statement**

**The central challenge in modern drug discovery lies in the identification of novel chemical entities that simultaneously satisfy multiple stringent criteria: strong binding affinity to the target protein, favorable pharmacokinetic properties, low toxicity, and practical synthesizability. For HIV-1 Protease, a homodimeric aspartic protease enzyme critical for viral maturation, existing inhibitor development efforts face several key obstacles.**

**First, the chemical space of drug-like molecules is astronomically large, estimated at 10^60 possible compounds, making exhaustive experimental screening practically impossible. Traditional methods rely on modifying known drug scaffolds or screening existing compound libraries, which inherently limits the novelty of candidates that can be discovered. Second, the emergence of drug-resistant mutant strains of HIV-1 Protease has rendered several approved protease inhibitors less effective, creating an urgent need for structurally diverse new inhibitors that can overcome resistance mechanisms.**

**Furthermore, computational drug design has traditionally been fragmented, with molecular generation, property prediction, docking simulation, and pharmacokinetic evaluation performed as isolated steps using different tools and platforms. This lack of integration leads to inefficiencies, inconsistent evaluation criteria, and difficulty in comparing candidates across multiple dimensions simultaneously. Many promising molecules generated by AI models turn out to be impractical because they are too complex to synthesize, exhibit poor oral bioavailability, or show unacceptable toxicity profiles.**

**Considering these challenges, there is a clear need for an integrated, AI-driven drug discovery pipeline that combines generative deep learning for novel molecule creation with a systematic, multi-criteria evaluation framework. DENOVO  aims to address this gap by implementing an LSTM-based molecular generation system followed by comprehensive candidate assessment encompassing Lipinski drug-likeness filtering, quantum chemistry stability analysis, molecular docking against HIV-1 Protease, ADMET pharmacokinetic profiling, synthetic accessibility scoring, and a unified weighted ranking system, all presented through an interactive web dashboard.**

**1.2 Objective**

**The primary objective of the project, DENOVO , is to design, develop, and evaluate an AI-Driven Drug Discovery Pipeline for HIV-1 Protease Inhibitors that leverages deep learning for novel molecule generation and comprehensive computational evaluation to identify the most promising drug candidates. To achieve this, the project first seeks to conduct a thorough review of existing computational drug discovery methods, generative molecular design approaches, and multi-criteria evaluation frameworks to understand their strengths, limitations, and the gaps that can be addressed through an integrated pipeline approach.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**2**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**Building upon this foundation, an LSTM-based generative model will be trained on approximately 9,480 HIV-related drug molecules to learn the chemical grammar of valid SMILES representations, enabling the generation of novel, chemically valid molecular structures. A central focus of the project is the development of a robust multi-stage evaluation pipeline capable of assessing generated candidates across five key dimensions: drug-likeness (Lipinski's Rule of Five), electronic stability (HOMO-LUMO gap via quantum chemistry), binding affinity to HIV-1 Protease (molecular docking), pharmacokinetic viability (ADMET properties), and synthetic feasibility (SA Score).**

**The system will integrate these diverse evaluation criteria into a unified weighted composite scoring framework that enables objective comparison and ranking of all candidate molecules. An interactive Streamlit web dashboard will be developed to present all results visually, allowing researchers to explore candidate profiles, examine molecular structures in 2D and 3D, review individual evaluation metrics, and access the final comprehensive ranking. Ultimately, the project aims to demonstrate that AI-powered generative drug design, combined with systematic computational evaluation, can accelerate the identification of viable lead compounds for HIV-1 Protease inhibition, bridging the gap between computational chemistry and practical drug development.**

**1.3 Purpose and Need**

**The purpose of the DENOVO : AI-Driven Drug Discovery for HIV-1 Protease Inhibitors project is to design, develop, and implement an integrated computational pipeline that accelerates the discovery of novel drug candidates targeting a critical HIV enzyme. In the current pharmaceutical landscape, the reliance on traditional experimental drug discovery methods has become increasingly unsustainable due to their extraordinary cost, lengthy timelines, and high failure rates. Reports indicate that fewer than 10% of drug candidates entering clinical trials ultimately receive regulatory approval, with the average development cost exceeding $2.6 billion per approved drug.**

**HIV-1 Protease remains one of the most validated and important drug targets in antiretroviral therapy. This enzyme is essential for the post-translational processing of viral polyproteins (Gag and Gag-Pol) into functional structural proteins and enzymes required for viral maturation. Without a functional protease, the virus produces only immature, non-infectious particles. Protease inhibitors (PIs) have been a cornerstone of highly active antiretroviral therapy (HAART) since their introduction in the mid-1990s. However, the rapid mutation rate of HIV-1 has led to the emergence of multi-drug-resistant strains, necessitating continuous discovery of novel inhibitor scaffolds that can evade resistance mechanisms.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**3**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**Artificial intelligence offers a transformative approach to this challenge. Deep generative models, particularly recurrent neural networks such as LSTMs, have demonstrated remarkable ability to learn the syntax and semantics of molecular representations (SMILES notation) from large chemical datasets. Once trained, these models can generate entirely novel molecular structures that are chemically valid and possess desired drug-like properties. This generative approach explores chemical space far more efficiently than traditional screening methods, potentially uncovering structurally diverse candidates that would not be found through conventional approaches.**

**However, generating novel molecules is only the first step. A drug candidate must satisfy multiple, often competing, criteria to succeed: it must bind strongly to the target protein, be absorbed effectively by the body, reach the intended tissues, avoid toxic metabolites, be excreted safely, and be practically synthesizable at scale. DENOVO  addresses this multi-dimensional challenge by implementing a comprehensive evaluation pipeline that assesses each generated candidate across all critical dimensions.**

**Beyond scientific contribution, the project emphasizes accessibility and reproducibility. By implementing the entire pipeline using open-source tools (TensorFlow, RDKit, PySCF, AutoDock Vina) and presenting results through an interactive Streamlit dashboard, DENOVO  makes advanced computational drug discovery techniques accessible to researchers and students who may not have expertise in every individual domain. The web-based interface enables intuitive exploration of complex molecular data, including 2D and 3D structure visualization, property comparison charts, and comprehensive ranking tables.**

**From a research perspective, DENOVO  contributes to the advancement of AI-driven drug discovery by demonstrating an end-to-end pipeline that integrates molecular generation, property prediction, structural evaluation, and multi-criteria ranking within a single framework. Practically, the project demonstrates the feasibility of using deep learning to generate viable drug candidates for a clinically relevant target, providing a template methodology that can be adapted to other drug targets and disease areas.**

**In summary, the purpose and need of DENOVO  lie in delivering an integrated, AI-powered drug discovery system that addresses the limitations of fragmented computational approaches, accelerates the identification of novel HIV-1 Protease inhibitors, leverages advanced deep learning and cheminformatics technologies, and provides both practical and research contributions to the field of computational pharmacology.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**4**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**1.4 Organization of Report**

**This report is systematically organized to provide a clear and comprehensive understanding of the DENOVO  project. Chapter 2: Literature Review presents an in-depth review of existing research related to AI-driven drug discovery, molecular generation, and computational evaluation. It examines representative research papers for each key component—generative molecular design, molecular docking, ADMET prediction, synthesizability assessment, and quantum chemistry—to establish the technical background and current advancements in computational drug discovery. This chapter identifies existing challenges and research gaps that motivate the development of the proposed integrated pipeline.**

**Chapter 3: Methodology describes the overall architecture and design of the DENOVO  system. It explains the functional components, data flow, and interaction between the LSTM-based molecular generator, the evaluation modules (Lipinski filtering, quantum chemistry, docking, ADMET, synthesizability), and the composite ranking engine. Detailed system architecture and design diagrams illustrate the modular structure and the operation of the multi-criteria fusion strategy responsible for candidate ranking.**

**Chapter 4: Implementation details the step-by-step technical implementation of each module, including the development environment setup, LSTM model architecture and training, evaluation pipeline construction, and Streamlit web dashboard development. It describes the tools, libraries, and frameworks used, along with the specific configurations and parameters employed in each module.**

**Chapter 5: Conclusion and Future Scope summarizes the outcomes of the project, highlighting its contributions toward accelerating drug discovery through AI-driven molecular generation and comprehensive computational evaluation. It also discusses the project's limitations and potential directions for future enhancement, such as incorporating reinforcement learning for guided generation, expanding to other drug targets, and integrating experimental validation workflows.**

**This structured organization ensures a logical and coherent progression—from background research to system design, implementation, and final reflections—guiding the reader through both the conceptual and practical aspects of the DENOVO  project.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**5**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**CHAPTER 2**

**LITERATURE REVIEW**

**2.1 Deep Learning for De Novo Drug Design**

**This paper [1] discusses the emerging paradigm of using deep learning models for de novo drug design, where neural networks learn to generate novel molecular structures directly from training data rather than screening existing compound libraries. Traditional drug discovery relies heavily on high-throughput screening of large compound libraries, which is both expensive and limited to known chemical space. Deep learning provides a way to overcome these challenges by learning the underlying distribution of drug-like molecules and sampling novel compounds from this learned distribution. [1] The authors emphasize that generative models such as variational autoencoders (VAEs), generative adversarial networks (GANs), and recurrent neural networks (RNNs) can explore vast regions of chemical space that are inaccessible through traditional screening, potentially uncovering entirely new drug scaffolds with desired pharmacological properties.**

**Methodology**

**Figure 2.1: Architecture of deep generative models for de novo drug design**

**The methodology of this paper [1] was built around three essential approaches to molecular generation: representation learning, generative modeling, and property optimization. First, molecular representations were standardized using SMILES notation, a line-based text encoding of chemical structures that enables the application of natural language processing techniques. The SMILES strings were tokenized at the character level and converted into numerical sequences using one-hot encoding or learned embeddings.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**7**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**For generative modeling, three architectures were compared: VAEs that learn a continuous latent space representation enabling interpolation between molecules, GANs that use adversarial training to generate realistic molecular structures, and RNNs (specifically LSTMs) that learn the sequential grammar of SMILES strings character by character. The RNN-based approach treats molecule generation as a language modeling task, where the model learns to predict the next character in a SMILES string given the preceding characters. This autoregressive approach naturally enforces chemical validity since the model learns which character sequences correspond to valid molecular structures.**

**Training involved supervised learning on large chemical databases such as ChEMBL and ZINC, containing millions of validated drug-like molecules. Transfer learning and fine-tuning were employed to specialize general molecular generators toward specific target profiles. The evaluation phase assessed generated molecules on chemical validity (percentage of valid SMILES), novelty (percentage not in the training set), and diversity (structural variety among generated compounds).**

**Results**

**The RNN/LSTM-based approach achieved the highest chemical validity rates (up to 97%) among the generative models tested, while VAEs excelled in latent space interpolation and property optimization. GANs showed promise but suffered from mode collapse, limiting molecular diversity. The main limitation was that validity alone does not guarantee drug-likeness or biological activity, necessitating additional filtering and evaluation stages.**

**Summary of Findings**

**This paper [1] summarizes that deep generative models provide powerful tools for de novo drug design and that LSTM-based approaches offer the best balance of validity, novelty, and ease of implementation. For DENOVO , this study offers three key takeaways. First, SMILES-based character-level generation using LSTMs is a proven and effective approach for novel molecule creation. Second, temperature-controlled sampling allows balancing between molecular diversity and chemical validity. Third, generated candidates require comprehensive post-generation evaluation including drug-likeness filtering, docking, and ADMET assessment to identify truly promising leads. These insights directly support the choice of LSTM as the core generative architecture in the DENOVO  pipeline.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**8**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**2.2 Generative Models for Molecular Design Using SMILES**

**This paper [2] presents a comprehensive study on the use of SMILES-based generative models for designing novel drug molecules, with particular emphasis on the representation challenges and solutions in molecular generation. Many existing systems require complex graph-based representations that are computationally expensive, while SMILES-based approaches offer a simpler, more scalable alternative. [2] This research proposes a purely sequence-based generative framework that relies only on SMILES string processing, making it more accessible and computationally efficient. Beyond its primary application for drug design, the SMILES generation framework can also be adapted to support materials science, agrochemical design, and other chemical optimization tasks.**

**Methodology**

**The system was designed around a multi-stage pipeline beginning with data curation and ending with candidate evaluation. Large chemical databases were curated to extract drug-relevant SMILES strings, and the data was cleaned by removing invalid entries, duplicates, and molecules with undesirable properties. Canonical SMILES representations were computed using RDKit to ensure consistent encoding of identical molecules.**

**Figure 2.2: SMILES representation and molecular graph conversion pipeline**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**9**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**A vocabulary of unique characters was extracted from the processed SMILES strings, including atoms, bonds, ring closures, and branch symbols. Special start and end tokens were added to enable the model to learn sequence boundaries. The character-level tokenization approach was chosen over subword tokenization because chemical SMILES syntax requires precise character-level control to maintain structural validity.**

**For generation, the system used a multi-layer LSTM network trained on the character prediction task. The LSTM architecture was selected for its ability to capture long-range dependencies in SMILES strings, such as matching ring closure digits and balanced parentheses for branching structures. The network was trained using teacher forcing with cross-entropy loss to predict the next character given the sequence history.**

**Results**

**The proposed system achieved chemical validity rates exceeding 95% on generated SMILES strings, demonstrating that character-level LSTM models can effectively learn SMILES grammar. The model generated structurally diverse molecules with drug-like properties.**

**However, the system had limitations. Generated molecules occasionally violated complex chemical rules not captured by SMILES syntax alone. Generated compounds required additional property filtering to ensure drug-likeness, and the model's novelty decreased with lower sampling temperatures.**

**Summary of Findings**

**This paper [2] summarizes that SMILES-based LSTM generation is a practical and effective approach for molecular design. For DENOVO , the most relevant takeaways are that SMILES-based generation can produce valid and diverse molecules without requiring graph-based representations, that careful dataset curation and canonical SMILES processing are essential for training quality, and that post-generation filtering (such as Lipinski's rules) is necessary to identify drug-like candidates among generated molecules.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**10**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**2.3 LSTM-Based Molecular Generation for Drug Discovery**

**This paper [3] explores the specific application of Long Short-Term Memory (LSTM) neural networks for generating novel drug-like molecules represented as SMILES strings. LSTM architectures have become central to molecular generation because they excel at modeling sequential data with long-range dependencies, which is crucial for maintaining chemical validity in generated structures. [3] The authors present a detailed analysis of how LSTM-based generators can be trained, optimized, and deployed for practical drug discovery applications, with emphasis on the architectural choices that affect generation quality.**

**Methodology**

**The molecular generation system in this paper [3] starts with data preparation. SMILES strings from established chemical databases were collected, validated using RDKit, and canonicalized to remove duplicate representations. The dataset was augmented through SMILES enumeration, generating multiple valid SMILES representations for each molecule to improve the model's robustness to different encoding conventions.**

**Figure 2.3: LSTM-based molecular generation process**

**The main part of the system is an LSTM neural network architecture consisting of an embedding layer that converts character tokens into dense vector representations, followed by two stacked LSTM layers with 256 hidden units each. Dropout regularization (rate 0.2) was applied between layers to prevent overfitting. The final dense layer with softmax activation produces a probability distribution over the character vocabulary, enabling next-character prediction. The model was trained using categorical cross-entropy loss with the Adam optimizer.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**12**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**During generation, new molecules are sampled character by character from the learned probability distribution. Temperature scaling was employed to control the trade-off between novelty and validity: lower temperatures (T<1.0) produce more conservative, valid molecules, while higher temperatures (T>1.0) increase diversity but risk generating invalid structures. The optimal temperature of 0.8 was identified through systematic experimentation.**

**Results**

**The LSTM model achieved 100% chemical validity at temperature 0.7 and maintained over 90% validity at temperature 0.8 while producing significantly more diverse structures. The generated molecules showed good coverage of desirable drug-like property ranges, with the majority satisfying Lipinski's Rule of Five criteria. Training converged within 50 epochs for datasets of approximately 10,000 molecules.**

**Summary of Findings**

**This paper [3] shows that LSTM networks are highly effective for SMILES-based molecular generation, achieving high validity rates while maintaining structural diversity through temperature-controlled sampling. For our DENOVO  project, which uses LSTM-based generation as its core AI component, the study provides direct validation of our architectural choices. Key takeaways—such as optimal temperature selection, the importance of SMILES canonicalization, and the dual-LSTM architecture with dropout—directly informed the design of our molecular generation module.**

**2.4 Recurrent Neural Networks for SMILES-Based Molecule Generation**

**This paper [4] explores the broader landscape of recurrent neural network architectures for SMILES-based chemical generation, comparing vanilla RNNs, GRU networks, and LSTMs across various molecular generation benchmarks. The key contribution is a systematic evaluation of how different recurrent architectures affect generation quality, training efficiency, and the chemical properties of output molecules. [4] The study traces the evolution of sequence-based molecular generation from early Markov chain approaches to modern deep recurrent architectures, highlighting the crucial role of memory mechanisms in maintaining chemical validity.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**15**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**Methodology**

**This paper [4] uses three RNN variants to build molecular generators. [4] The process starts with dataset preparation, ensuring molecules are properly validated and encoded. All three architectures were trained on the same ChEMBL dataset of approximately 1.5 million drug-like molecules for fair comparison.**

**Figure 2.4: RNN architecture for character-level SMILES generation**

**The LSTM variant demonstrated superior performance in handling long SMILES strings (50+ characters) due to its gating mechanism that prevents vanishing gradients. The GRU achieved comparable results with fewer parameters, offering a computational efficiency advantage. The vanilla RNN struggled with long sequences, producing lower validity rates for complex molecules. All models used teacher forcing during training and temperature-scaled sampling during generation.**

**Results**

**The LSTM model achieved the highest validity rate (97.2%) and best property distribution coverage among generated molecules. GRUs achieved 95.8% validity with 30% fewer parameters. Vanilla RNNs peaked at 88.4% validity. All models showed that chemical validity correlates inversely with structural complexity, with simpler molecules achieving near-perfect validity.**

**Summary of Findings**

**This paper [4] confirms that LSTM-based architectures provide the best balance of generation quality and capability for SMILES-based molecular design. For DENOVO , this validates the choice of LSTM over simpler RNN variants for generating HIV-1 Protease inhibitor candidates, where molecular complexity and structural integrity are paramount.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**16**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**2.5 Molecular Docking Using AutoDock Vina for Virtual Screening**

**In this work [5], authors present a comprehensive methodology for using AutoDock Vina in virtual screening campaigns against protein drug targets. The authors [5] note that molecular docking is a critical step in computational drug discovery that simulates the binding interaction between small molecules (ligands) and target proteins. Their goal is to establish best practices for preparing protein targets, configuring search parameters, and interpreting binding affinity results using AutoDock Vina, one of the most widely used open-source docking tools.**

**The study uses HIV-1 Protease (PDB: 1HSG) as the benchmark protein target, which is directly relevant to our project. The protein structure was obtained from the Protein Data Bank, with the co-crystallized inhibitor and water molecules removed during preparation. Hydrogen atoms were added, and the structure was converted to PDBQT format for compatibility with Vina.**

**Methodology**

**In preprocessing, the protein target was prepared by removing heteroatoms, adding polar hydrogens, and computing Gasteiger charges. The search box was defined around the known active site using coordinates from the co-crystallized ligand. Ligand molecules were prepared by generating 3D conformations using RDKit, adding hydrogens, optimizing geometry using the Universal Force Field (UFF), and converting to PDBQT format.**

**AutoDock Vina uses an empirical scoring function that combines intermolecular interactions including van der Waals contacts, hydrogen bonds, electrostatic interactions, and desolvation effects. The scoring function outputs a binding affinity value in kcal/mol, where more negative values indicate stronger predicted binding.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**17**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**Results**

**The docking protocol successfully reproduced the binding pose of the co-crystallized inhibitor with an RMSD of less than 2.0 Å, validating the methodology. Binding affinities ranged from -5.0 to -12.0 kcal/mol across test compounds, with known HIV-1 Protease inhibitors consistently scoring below -8.0 kcal/mol. Key interacting residues identified include ASP25, ASP25', ILE50, ILE50', GLY27, and GLY48, which form the catalytic dyad and flap region of the protease active site.**

**Summary of Findings**

**The key takeaway from this [5] study is that AutoDock Vina provides reliable and efficient molecular docking simulations for HIV-1 Protease, with binding affinity predictions that correlate well with experimental data. For DENOVO , this study directly informs our docking module design and validates the use of pre-computed docking scores using the 1HSG crystal structure and established active site coordinates.**

**2.6 Computational Approaches to Molecular Docking in Drug Discovery**

**[6] Molecular docking has become an indispensable tool in structure-based drug design, enabling the prediction of binding modes and affinities between drug candidates and target proteins. This technology analyzes the geometric and energetic complementarity between ligands and protein binding sites, making it well-suited for virtual screening and lead optimization in drug discovery pipelines.**

**Methodology**

**This review [6] covers various docking approaches including rigid docking, flexible docking, and ensemble docking methods. It explains the typical workflow: target preparation, binding site identification, ligand preparation, docking simulation, and pose scoring. Special attention is given to scoring functions, comparing force-field-based, empirical, and knowledge-based scoring approaches.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**21**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**Results**

**Different docking methods offer varying trade-offs between accuracy and computational cost. Rigid docking is fastest but least accurate, while fully flexible docking captures protein conformational changes but requires significantly more computation. Scoring function accuracy remains a key challenge, with consensus scoring across multiple functions often outperforming individual approaches.**

**Summary of Findings**

**[6] Combining multiple docking approaches with consensus scoring significantly enhances prediction reliability. This review highlights the importance of proper protein preparation and binding site definition for accurate results. For DENOVO , these insights informed our docking protocol design, particularly the use of known active site coordinates from the co-crystallized inhibitor for reliable search box placement.**

**2.7 A Survey on ADMET Prediction Using Machine Learning and Deep Learning**

**This paper [7] reviews computational methods for predicting ADMET properties, which are critical determinants of drug candidate success or failure. Approximately 60% of drug candidates fail in clinical trials due to poor pharmacokinetic profiles, making early ADMET prediction essential for reducing attrition rates. [7] The survey discusses how machine learning and deep learning models can predict key ADMET properties directly from molecular descriptors or structural representations.**

**Methodology**

**The methodology described in this paper [7] categorizes ADMET prediction approaches based on input representations (molecular fingerprints, descriptors, SMILES, molecular graphs) and model architectures (random forests, SVMs, gradient boosting, neural networks). It reviews prediction of individual ADMET endpoints including Caco-2 permeability, human intestinal absorption, blood-brain barrier penetration, CYP450 inhibition, hERG toxicity, and oral bioavailability.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**22**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**Figure 2.5: AutoDock Vina molecular docking workflow**

**The paper [7] specifically notes the value of rule-based approaches such as Lipinski's Rule of Five and Veber's rules as computationally efficient first-pass filters for drug-likeness assessment. These empirical rules, while simpler than ML-based predictions, provide reliable initial screening that eliminates clearly non-viable candidates before more expensive computational or experimental evaluation.**

**Results**

**As a survey paper, this paper [7] consolidates findings from numerous studies, illustrating that ML-based ADMET prediction can achieve clinically useful accuracy for many endpoints. Deep learning models generally outperform traditional ML approaches when sufficient training data is available, but rule-based methods remain valuable for preliminary screening due to their interpretability and computational efficiency. Challenges include data quality, assay variability, and the difficulty of predicting complex clinical outcomes from molecular structure alone.**

**Summary of Findings**

**This paper [7] summarizes that computational ADMET prediction is essential for modern drug discovery and that a tiered approach—combining rule-based filters with ML predictions—offers the best practical strategy. For our DENOVO  project, which evaluates candidates using Lipinski's rules, Veber's criteria, QED scoring, and heuristic ADMET models, the paper validates our multi-level evaluation approach and highlights the value of combining multiple prediction methods for comprehensive pharmacokinetic profiling.**

**2.8 Quantitative Estimation of Drug-Likeness and Pharmacokinetic Profiling Using RDKit**

**This paper [8] reviews the Quantitative Estimation of Drug-Likeness (QED) metric and its implementation within the RDKit cheminformatics toolkit. QED provides a single numerical score (0 to 1) that integrates multiple molecular properties including molecular weight, LogP, number of hydrogen bond donors and acceptors, polar surface area, number of rotatable bonds, and number of aromatic rings into a unified drug-likeness assessment.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**24**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**Methodology**

**This paper [8] describes the computation of QED as a geometric mean of desirability functions applied to individual molecular properties. Each property is mapped through a specific desirability function learned from the analysis of approved oral drugs, ensuring that the QED score reflects real-world drug-like property distributions.**

**Results**

**QED scores for approved drugs typically range from 0.3 to 0.9, with a median around 0.5. The metric effectively discriminates between drug-like and non-drug-like molecules and provides a more nuanced assessment than binary pass/fail rules like Lipinski's criteria. QED computed via RDKit shows excellent correlation with proprietary drug-likeness scores.**

**Summary of Findings**

**QED provides a practical, quantitative measure of overall drug-likeness that complements rule-based filters. For DENOVO , QED is used as the primary ADMET scoring metric in the final composite ranking, providing a continuous drug-likeness score that enables meaningful differentiation between candidates.**

**2.9 Synthetic Accessibility Score Estimation for Drug-Like Molecules**

**This paper [9] presents the development and validation of the Synthetic Accessibility (SA) Score, a computational metric that estimates how difficult it would be to synthesize a given molecule in a chemistry laboratory. The SA Score ranges from 1 (very easy to synthesize) to 10 (very difficult), and it is calculated using a fragment-based approach that considers both the structural complexity of the molecule and the frequency of its constituent fragments in known synthetic chemistry.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**25**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**Methodology**

**Figure 2.6: ADMET prediction pipeline using molecular descriptors**

**This paper [9] starts by analyzing a large database of commercially available and synthetically accessible compounds to identify common molecular fragments. The SA Score computation combines two components: a fragment contribution score based on the frequency of molecular substructures in known compounds (more common fragments = easier synthesis), and a complexity penalty based on molecular features such as ring systems, stereocenters, macrocycles, and unusual functional groups. The fragment scores were derived by analyzing over one million molecules from the PubChem database, computing the frequency of each fragment, and converting frequencies to contribution scores. The complexity penalty accounts for factors that make synthesis challenging regardless of fragment availability.**

**Results**

**The SA Score showed strong correlation with expert chemist assessments of synthetic difficulty, with a Spearman correlation coefficient of 0.89. Most drug-like molecules score between 2 and 5, while highly complex natural products and AI-generated molecules can score above 7. The metric is computationally efficient, requiring less than 1 millisecond per molecule, making it suitable for high-throughput screening applications.**

**Summary of Findings**

**This paper [9] summarizes that the SA Score provides a practical, validated metric for assessing synthetic feasibility. For DENOVO , SA Score is used as one of the five evaluation criteria in the final composite ranking, with a weight of 15%. Candidates scoring below 5 are considered reasonably synthesizable, while higher scores indicate increasing synthetic challenges that may limit practical development.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**27**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**2.10 Computational Retrosynthetic Analysis for Drug Development**

**This paper [10] "Computational Retrosynthetic Analysis for Drug Development" addresses the practical challenge of translating computationally designed molecules into experimentally accessible compounds. While AI can generate novel molecular structures, many designs are impractical to synthesize. This paper proposes combining SA Score assessment with retrosynthetic planning to evaluate both the difficulty and specific synthetic routes for drug candidates.**

**Methodology**

**[10] The authors categorize synthetic feasibility assessment into three levels: rule-based scoring (SA Score), template-based retrosynthesis (matching known reaction templates), and ML-based retrosynthetic planning (predicting novel synthetic routes). The study demonstrates that combining SA Score with at least one level of retrosynthetic analysis provides more reliable feasibility assessment than any single method alone. The experimental setup involved evaluating 500 drug candidates from generative models against all three levels of assessment, comparing results with expert synthetic chemist evaluations.**

**Figure 2.7: Synthetic accessibility scoring framework**

**Results**

**The results showed that SA Score alone correctly classified synthetic difficulty in 78% of cases. Adding template-based retrosynthetic analysis improved accuracy to 89%. The ML-based retrosynthetic planner achieved the highest accuracy (93%) but required significantly more computation time. The study found that SA Score provides an excellent first-pass filter, with scores below 4 almost universally corresponding to synthetically accessible molecules.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**28**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**Summary of Findings**

**In summary, this research [10] emphasizes that synthetic accessibility assessment is critical for practical drug development. The SA Score provides a fast, reliable initial estimate that can be augmented with more sophisticated retrosynthetic analysis for advanced candidates. For DENOVO , the SA Score implementation using RDKit's sascorer module provides the essential first-level assessment, with results presented in the Synthesizability Analysis page of the web dashboard.**

**2.11 Quantum Chemistry in Drug Discovery: HOMO-LUMO Analysis**

**This paper [11] explores the application of quantum chemical calculations, specifically HOMO-LUMO gap analysis, in evaluating electronic properties relevant to drug-molecule interactions. The HOMO (Highest Occupied Molecular Orbital) and LUMO (Lowest Unoccupied Molecular Orbital) energies provide fundamental insights into a molecule's chemical reactivity, stability, and potential for electron transfer interactions with biological targets.**

**Methodology**

**Figure 2.8: Quantum chemistry energy level computation process**

**This paper [11] introduces quantum chemistry calculations using the Hartree-Fock method and density functional theory (DFT) to compute molecular orbital energies. The HOMO-LUMO gap—the energy difference between the frontier molecular orbitals—serves as a measure of molecular stability and reactivity. A smaller gap indicates higher chemical reactivity, which can correlate with stronger binding interactions with target proteins. PySCF (Python-based Simulations of Chemistry Framework) is used as the computational engine for these calculations.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**31**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**Results**

**Quantum chemistry calculations provided electronic property insights that correlate with biological activity for several drug classes. The HOMO-LUMO gap showed statistically significant correlation with binding affinity in protease inhibitor datasets, supporting its use as an evaluation criterion in drug candidate ranking.**

**Summary of Findings**

**The proposed approach shows that quantum chemistry analysis adds a valuable electronic perspective to drug candidate evaluation. For DENOVO , HOMO-LUMO gap analysis complements other evaluation metrics (docking, ADMET, SA Score) by capturing electronic stability and reactivity properties that are not accessible through classical molecular descriptors alone.**

**2.12 AI-Driven Drug Discovery Pipelines for HIV-1 Protease Inhibitors**

**Figure 2.9: AI-driven drug discovery pipeline for HIV-1 protease**

**This paper [12] presents an integrated AI-driven drug discovery pipeline specifically targeting HIV-1 Protease, combining generative molecular design with multi-stage computational evaluation. [12] The proposed pipeline integrates deep generative models for candidate creation with virtual screening, ADMET prediction, and binding affinity estimation to identify promising protease inhibitor leads.**

**Methodology**

**This methodology is divided into three main modules: molecular generation, property evaluation, and candidate ranking. The generation module uses a pre-trained LSTM network fine-tuned on known HIV-1 Protease inhibitors to bias generation toward target-relevant chemical space.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**32**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**The evaluation module assesses each generated candidate across multiple dimensions including structural validity, drug-likeness (Lipinski's rules), predicted binding affinity, and synthetic feasibility. Results from individual evaluations are combined through a weighted scoring framework to produce a final candidate ranking.**

**Results**

**The pipeline generated over 1,000 novel molecular structures, of which approximately 70% were chemically valid. After Lipinski filtering, 45% of valid molecules satisfied all drug-likeness criteria. Top-ranked candidates showed predicted binding affinities comparable to approved HIV Protease inhibitors, demonstrating the viability of the AI-driven approach.**

**Summary of Findings**

**This paper [12] summarizes that integrated AI drug discovery pipelines can effectively generate and evaluate novel HIV-1 Protease inhibitor candidates. For DENOVO , this work validates our end-to-end pipeline approach and demonstrates that combining LSTM-based generation with multi-criteria evaluation produces clinically relevant candidate molecules.**

**2.13 Multi-Objective Optimization in Computational Drug Design**

**This paper [13] addresses the fundamental challenge that drug design is inherently a multi-objective optimization problem. A successful drug candidate must simultaneously satisfy multiple, often competing, criteria including potency, selectivity, oral bioavailability, metabolic stability, and synthetic accessibility. [13] The authors present computational frameworks for balancing these competing objectives and producing Pareto-optimal candidate sets.**

**Methodology**

**[13] The proposed framework uses weighted score aggregation to combine multiple evaluation metrics into a single composite ranking. The methodology involves normalizing individual metrics to a common scale (0–1), assigning weights based on relative importance and confidence in each metric, computing weighted sums, and ranking candidates by composite score.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**35**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**The paper discusses several weighting strategies: equal weights (treating all criteria as equally important), expert-defined weights (reflecting domain knowledge about relative importance), and data-driven weights (learned from successful drug development datasets). The authors recommend assigning higher weights to binding affinity and drug-likeness, as these are the most direct predictors of clinical success.**

**Results**

**Multi-objective optimization consistently identified better candidate sets than single-criterion ranking. Weighted composite scoring with expert-defined weights showed the best correlation with experimental validation outcomes, outperforming both equal-weight and data-driven approaches. The optimal weight distribution assigned approximately 30% to binding affinity, 25% to drug-likeness (ADMET), 20% to predicted efficacy, 15% to synthetic accessibility, and 10% to other factors.**

**Summary of Findings**

**This work [13] demonstrates that multi-criteria weighted ranking is essential for identifying the most promising drug candidates. For DENOVO , this directly informs our composite ranking strategy, which assigns weights of 30% to docking affinity, 25% to ADMET (QED), 20% to AI Score, 15% to synthesizability, and 10% to stability (HOMO-LUMO gap).**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**38**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**2.14 Lipinski's Rule of Five and Drug-Likeness Filtering**

**Figure 2.10: Multi-criteria drug candidate evaluation framework**

**[14] In "Lipinski's Rule of Five and Drug-Likeness Filtering," the authors review the foundational rule that has guided oral drug development for over two decades. The Rule of Five states that poor absorption or permeation is more likely when a molecule violates two or more of the following criteria: molecular weight above 500 Da, LogP above 5, more than 5 hydrogen bond donors, and more than 10 hydrogen bond acceptors. This simple heuristic remains one of the most widely used filters in computational drug discovery.**

**Methodology**

**Figure 2.11: Lipinski Rule of Five filtering process**

**[14] The analysis of Lipinski's rules involves computing four molecular properties using cheminformatics tools (primarily RDKit): molecular weight, LogP (octanol-water partition coefficient), number of hydrogen bond donors, and number of hydrogen bond acceptors. Veber's extension adds two additional criteria: topological polar surface area (TPSA ≤ 140 Å²) and number of rotatable bonds (≤ 10) for predicting oral bioavailability. The study validates these rules against a dataset of approved oral drugs, showing that over 90% comply with Lipinski's criteria.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**39**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**Results**

**Analysis of over 2,000 approved oral drugs showed 91% compliance with Lipinski's Rule of Five. Molecules violating two or more rules showed significantly lower oral bioavailability in clinical data. However, the rules have notable exceptions, particularly for natural products and peptide-based drugs. The combination of Lipinski's rules with Veber's criteria and QED scoring provides a more comprehensive drug-likeness assessment than any single metric alone.**

**Summary of Findings**

**To summarize, this research [14] presents Lipinski's Rule of Five as a foundational but not sufficient filter for drug-likeness. For DENOVO , Lipinski filtering is applied as the first-pass evaluation in the Discovery Engine page, followed by more comprehensive ADMET profiling using QED scores, Veber's rules, and heuristic property predictions on the dedicated ADMET Analysis page.**

**2.15 HIV-1 Protease Inhibitors: From Design to Clinical Application**

**[15] Traditional drug development for HIV has progressed from early nucleoside analogues to sophisticated protease inhibitors that target the essential viral maturation process. Over nine protease inhibitors have been approved for clinical use, each designed to occupy the active site of HIV-1 Protease and prevent polyprotein cleavage.**

**Methodology**

**This paper [15] reviews the evolution of HIV-1 Protease inhibitor design across three generations, from first-generation peptidomimetic inhibitors to modern non-peptide inhibitors. Key design strategies include structure-based design using X-ray crystallography data, scaffold hopping to overcome resistance, and fragment-based design approaches.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**42**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**Results**

**Approved protease inhibitors demonstrate binding affinities in the nanomolar range (Ki values of 0.01–10 nM). Drug resistance remains the primary clinical challenge, with mutations at over 40 positions in the protease gene conferring some degree of resistance. Combination therapy using multiple PIs with different resistance profiles has been the primary strategy for managing resistance.**

**Summary of Findings**

**HIV-1 Protease inhibitor development validates the importance of structure-based drug design and highlights the continuous need for novel inhibitor scaffolds [15]. For projects like DENOVO , understanding the target's biology, approved inhibitor pharmacology, and resistance landscape is essential for designing AI-based drug discovery systems that generate clinically relevant candidates. The computational approach offers the potential to explore novel chemical scaffolds that may overcome existing resistance mechanisms.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**43**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**CHAPTER 3**

**METHODOLOGY**

**3.1 Technical Approach and Design Rationale**

**The DENOVO  framework is designed as an end-to-end AI-driven drug discovery pipeline grounded in deep generative modeling, cheminformatics-based property evaluation, and multi-criteria decision fusion. The fundamental design philosophy of the system is to integrate molecule generation and comprehensive evaluation into a unified workflow that takes raw chemical data as input and produces ranked, thoroughly assessed drug candidates as output.**

**Rather than relying on traditional high-throughput screening of existing compound libraries, DENOVO  employs a generative approach where an LSTM neural network learns the chemical grammar of drug-like molecules from a curated training dataset. The trained model then generates entirely novel molecular structures that are evaluated through multiple independent assessment modules. This generative-then-evaluate paradigm enables exploration of chemical space far beyond existing compound databases.**

**A key design decision in DENOVO  is the adoption of SMILES-based character-level generation. SMILES (Simplified Molecular-Input Line-Entry System) provides a compact text-based representation of molecular structures that enables the application of natural language processing techniques. By treating molecule generation as a sequence prediction task, the system leverages well-established LSTM architectures that excel at modeling sequential data with long-range dependencies—critical for maintaining chemical validity in generated structures.**

**Another important design consideration is the multi-stage evaluation pipeline. Generated molecules must satisfy multiple, often competing, criteria to be viable drug candidates. Rather than optimizing for a single property, DENOVO  evaluates each candidate across five independent dimensions: drug-likeness (Lipinski's Rules), electronic stability (HOMO-LUMO gap), target binding affinity (molecular docking), pharmacokinetic viability (ADMET/QED), and synthetic feasibility (SA Score). This multi-dimensional assessment provides a comprehensive view of each candidate's potential.**

**The framework also incorporates a weighted composite scoring system for final ranking. Since different evaluation criteria have varying levels of predictive importance for clinical success, DENOVO  assigns differential weights: docking affinity receives the highest weight (30%) as the most direct measure of target engagement, followed by ADMET drug-likeness (25%), AI prediction confidence (20%), synthesizability (15%), and electronic stability (10%). This data-driven ranking ensures objective candidate comparison.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**44**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**3.2 Overall System Framework**

**Figure 3.1: System Architecture**

**The overall framework of DENOVO  is designed as a structured two-part architecture integrating an AI training and generation pipeline with an interactive evaluation and visualization dashboard. As illustrated in the system architecture diagram Figure 3.1, the system consists of two primary components: the AI Pipeline (implemented as a Jupyter/Colab notebook) and the Streamlit Web Dashboard (a multi-page web application).**

**The AI Pipeline begins with data ingestion from a curated dataset of approximately 9,480 HIV-related drug molecules. These molecules undergo rigorous cleaning and validation using RDKit, resulting in approximately 9,286 high-quality training samples. The cleaned SMILES strings are tokenized at the character level, encoded using a vocabulary of 35 unique characters plus special tokens, and vectorized into training pairs for next-character prediction. The LSTM model is trained on these pairs and, once trained, generates novel molecular structures through temperature-controlled autoregressive sampling.**

**Generated molecules pass through Lipinski's Rule of Five filtering to identify drug-like candidates. Qualifying candidates then undergo quantum chemistry analysis using PySCF to compute HOMO-LUMO gap values, providing electronic stability metrics.**

**The Streamlit Web Dashboard serves as the presentation and evaluation layer. It provides six interactive pages: a login portal for researcher authentication, a biological context briefing on HIV-1 Protease, the AI Discovery Engine displaying candidate structures and properties, a Synthesizability Analysis page computing SA Scores, an ADMET Analysis page profiling pharmacokinetic properties, a Molecular Docking page displaying binding affinity results, and a Final Ranking page computing weighted composite scores.**

**By separating the computationally intensive AI pipeline from the interactive visualization layer, the framework ensures modularity, scalability, and accessibility. The modular architecture enables independent development and testing of each evaluation module while maintaining a unified data flow through the shared candidate dataset.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**45**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**3.3 Data Collection and Preprocessing Strategy**

**The data strategy in DENOVO  is structured as a rigorous multi-step curation process designed to establish a high-quality training corpus for the LSTM molecular generator. The primary objective of the data phase is to create a clean, representative dataset of HIV-related drug molecules that captures the structural diversity and chemical properties relevant to protease inhibitor design.**

**The raw dataset was sourced from curated chemical databases containing approximately 9,480 molecules with established bioactivity against HIV-related targets. Each molecule is represented as a SMILES string along with metadata including drug type, chirality information, and Lipinski compliance status. This dataset provides the breadth of chemical diversity needed for the model to learn generalizable molecular grammar rather than memorizing specific structures.**

**The preprocessing pipeline applies three sequential quality filters. First, chemical validation using RDKit ensures that every SMILES string encodes a valid molecular structure. Invalid entries that cannot be parsed by RDKit's molecular constructor are removed. Second, canonicalization converts all valid SMILES to their canonical form, eliminating duplicate representations of identical molecules. Third, complexity filtering removes molecules with SMILES strings exceeding 100 characters, as overly complex structures are less relevant to drug design and can introduce noise during training.**

**After preprocessing, the dataset is reduced to approximately 9,286 validated, canonical, and appropriately complex molecules. A character-level vocabulary is then extracted from the entire corpus, identifying 35 unique characters including atoms (C, N, O, S, etc.), bonds (=, #), ring closures (digits 1-9), branching symbols (parentheses), and stereochemistry markers. Two special tokens are added: '!' as the start-of-sequence marker and 'E' as the end-of-sequence marker, resulting in a total vocabulary of 37 tokens.**

**The vectorization step converts SMILES strings into next-character prediction training pairs. For each molecule, the SMILES string is decomposed into all possible (prefix, next_character) pairs. Input sequences are padded to a maximum length of 101 characters using left-padding. This process generates approximately 436,084 training pairs that collectively encode the chemical grammar of the dataset.**

**The data strategy ensures consistency between training representation and generation logic, quality-controlled input for reliable model training, comprehensive vocabulary coverage for diverse molecular generation, and efficient vectorization for practical training times.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**46**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**3.4 LSTM-Based Molecular Generation Methodology**

**The molecular generation module in DENOVO  is implemented using a deep recurrent neural network architecture based on Long Short-Term Memory (LSTM) units. The system operates by learning a probabilistic model of SMILES character sequences and generating novel molecular structures through autoregressive sampling from this learned distribution.**

**The LSTM architecture was selected for its demonstrated superiority in modeling sequential data with long-range dependencies. In the context of SMILES generation, long-range dependencies arise from matching ring closure digits, balanced parentheses for branching, and consistent valence constraints that may span many characters in the string. Standard RNNs suffer from vanishing gradient problems that prevent learning such dependencies, while LSTMs use gating mechanisms (input, forget, and output gates) to maintain relevant information across long sequences.**

**The model architecture consists of four sequential layers: an Embedding layer that maps each of the 35 vocabulary characters to a 128-dimensional dense vector representation, a first LSTM layer with 256 hidden units and return_sequences=True that processes the embedded input sequence, a Dropout layer with rate 0.2 for regularization, a second LSTM layer with 256 hidden units that produces a fixed-dimensional context vector, another Dropout layer with rate 0.2, and a Dense output layer with 35 units and softmax activation that produces a probability distribution over the character vocabulary.**

**Mathematically, at each time step t, the LSTM computes: f_t = σ(W_f · [h_{t-1}, x_t] + b_f), i_t = σ(W_i · [h_{t-1}, x_t] + b_i), C_t = f_t * C_{t-1} + i_t * tanh(W_C · [h_{t-1}, x_t] + b_C), o_t = σ(W_o · [h_{t-1}, x_t] + b_o), h_t = o_t * tanh(C_t), where f_t, i_t, o_t are the forget, input, and output gates respectively.**

**Training uses categorical cross-entropy loss with the Adam optimizer over 50 epochs with batch size 256. During generation, molecules are sampled character by character starting from the start token. At each step, the model predicts a probability distribution over the next character, and sampling is performed with temperature T=0.8 applied to the logits before softmax. This temperature value was empirically determined to provide the optimal balance between structural diversity and chemical validity.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**48**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**3.5 Molecular Docking Methodology**

**The molecular docking module evaluates the physical binding interaction between each drug candidate and the HIV-1 Protease target protein. Docking is performed computationally using the AutoDock Vina scoring function against the established crystal structure of HIV-1 Protease (PDB ID: 1HSG).**

**The protein target is prepared from the 1HSG crystal structure by removing co-crystallized ligands, water molecules, and heteroatoms. Polar hydrogen atoms are added, and Gasteiger partial charges are computed. The search space is defined as a 20×20×20 Å box centered at coordinates (x=16.0, y=25.0, z=4.0), which corresponds to the known active site cavity containing the catalytic aspartate dyad (ASP25/ASP25') and the flexible flap region (ILE50/ILE50').**

**Candidate ligands are prepared by converting SMILES strings to 3D molecular structures using RDKit's embedding and optimization algorithms. Hydrogen atoms are added, and geometry is optimized using the Universal Force Field (UFF) to generate energetically reasonable starting conformations.**

**The docking scoring function evaluates binding affinity in kcal/mol, where more negative values indicate stronger predicted binding. Key residue interactions are identified based on proximity analysis between ligand atoms and protein residues in the binding pocket. The scores and interaction profiles enable comparison of candidates based on their predicted ability to inhibit the target enzyme.**

**3.6 ADMET Prediction Methodology**

**The ADMET evaluation module assesses the pharmacokinetic viability of each candidate using a combination of rule-based filters and computed molecular descriptors implemented through RDKit.**

**The evaluation framework applies three complementary assessment levels. First, Lipinski's Rule of Five evaluates basic drug-likeness by checking molecular weight (<500 Da), LogP (<5), hydrogen bond donors (<5), and hydrogen bond acceptors (<10). Second, Veber's Rules assess oral bioavailability through topological polar surface area (TPSA ≤140 Å²) and rotatable bond count (≤10). Third, QED (Quantitative Estimation of Drug-Likeness) provides a continuous 0-1 score integrating multiple molecular properties through desirability functions.**

**Additional heuristic predictions include gastrointestinal absorption (based on Lipinski and Veber compliance), blood-brain barrier penetration (based on TPSA and LogP thresholds), CYP2D6 inhibition risk (based on basic nitrogen presence and aromatic ring count), and bioavailability score (based on Lipinski violation count). These combined assessments provide a comprehensive pharmacokinetic profile for each candidate.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**50**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**3.7 Synthesizability Assessment Methodology**

**The synthesizability module evaluates the practical feasibility of manufacturing each drug candidate in a chemistry laboratory using the Synthetic Accessibility (SA) Score implemented through RDKit's sascorer module.**

**The SA Score is computed using a fragment-based approach that combines two components: a fragment contribution score reflecting the frequency of constituent molecular substructures in known synthesized compounds, and a complexity penalty accounting for structural features that increase synthetic difficulty. Fragments that appear frequently in existing chemical databases receive lower (easier) scores, while rare or unusual fragments contribute higher (more difficult) scores. The complexity penalty increases with features such as complex ring systems, stereocenters, macrocyclic structures, and unusual functional group combinations.**

**SA Scores range from 1 (very easy to synthesize) to 10 (very difficult). For drug development purposes, candidates with SA Scores below 5 are generally considered practically synthesizable, while scores above 7 indicate significant synthetic challenges that may limit practical viability. The SA Score module classifies candidates into four difficulty categories: Easy (≤3), Moderate (3-5), Difficult (5-7), and Very Difficult (>7).**

**3.8 Multi-Criteria Weighted Ranking and Fusion Strategy**

**DENOVO  employs a weighted composite scoring mechanism to integrate heterogeneous evaluation metrics into a unified candidate ranking. Since different evaluation criteria use different scales and units, all metrics are first normalized to a common 0-1 range before weighted aggregation.**

**Under the standard configuration, the five evaluation metrics are assigned the following weights: Docking Affinity receives weight 0.30 as the most direct measure of target binding, ADMET Drug-Likeness (QED) receives weight 0.25 reflecting its importance for clinical viability, AI Prediction Score receives weight 0.20 as a measure of model confidence, Synthesizability (SA Score) receives weight 0.15 for practical feasibility, and HOMO-LUMO Gap receives weight 0.10 as a stability indicator. The composite score is computed as:**

**S = (w_dock × s_dock) + (w_qed × s_qed) + (w_ai × s_ai) + (w_sa × s_sa) + (w_gap × s_gap)**

**where s_dock, s_qed, s_ai, s_sa, and s_gap represent normalized scores for docking, QED, AI confidence, synthesizability, and electronic stability respectively. Normalization uses min-max scaling within each metric, with inversion applied where lower raw values indicate better performance (docking affinity, SA Score). The candidate with the highest composite score is recommended as the primary lead compound for further experimental validation.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**52**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**CHAPTER 4**

**IMPLEMENTATION**

**4.1 Development Environment and System Setup**

**For the implementation of the DENOVO  system, two distinct development environments were configured to support the AI pipeline and the web dashboard components respectively. The AI pipeline was developed and executed in Google Colab, leveraging GPU acceleration for neural network training. The Streamlit web dashboard was developed locally with a dedicated Python virtual environment to isolate dependencies and ensure stable deployment.**

**The AI pipeline was implemented as a Jupyter notebook (finalDo.ipynb) running on Google Colab with GPU runtime. The training environment included TensorFlow/Keras for LSTM model construction and training, RDKit for molecular processing and validation, PySCF for quantum chemistry calculations, NumPy for numerical computation, and Pandas for data manipulation.**

**The web dashboard was developed using Streamlit as the web framework, providing rapid development of interactive data applications. The local development environment included a Python virtual environment with the following core dependencies: Streamlit for the web interface, RDKit for molecular computation and visualization, py3Dmol and stmol for interactive 3D molecular rendering, Pandas for data handling, and standard Python libraries for system operations.**

**The system integrates the following core libraries:**

**• TensorFlow/Keras for LSTM model training and inference**

**• RDKit for molecular validation, property computation, and 2D visualization**

**• PySCF for quantum chemistry HOMO-LUMO calculations**

**• py3Dmol for interactive 3D molecular visualization**

**• Streamlit for web dashboard development**

**• Pandas for tabular data handling**

**• NumPy for numerical operations**

**• sascorer (RDKit contrib) for SA Score computation**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**53**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**4.2 LSTM Model Training and Molecule Generation**

**The LSTM model was implemented using TensorFlow/Keras as a Sequential model. The architecture consists of an Embedding layer (input_dim=35, output_dim=128), two stacked LSTM layers (256 units each) with Dropout (0.2) between them, and a Dense output layer (35 units, softmax activation). The model was compiled with categorical_crossentropy loss and the Adam optimizer.**

**Training was conducted on approximately 436,084 vectorized training pairs derived from 9,286 validated SMILES strings. The model was trained for 50 epochs with a batch size of 256, utilizing GPU acceleration for efficient computation. Model checkpointing was implemented to save the best-performing model weights based on validation loss. The trained model was saved in Keras format (hiv_protease_model.keras) for subsequent use in generation.**

**Molecule generation was performed using temperature-scaled autoregressive sampling at T=0.8. Starting from the start token, the model iteratively predicts the next character probability distribution, applies temperature scaling to the logits, samples from the resulting distribution, and appends the sampled character to the growing sequence. Generation terminates upon producing the end token or reaching the maximum sequence length. The process generated 10 novel SMILES strings, all of which were validated as chemically valid by RDKit, achieving a 100% validity rate.**

**4.3 Drug-Likeness Filtering Implementation**

**The Lipinski Rule of Five filter was implemented using RDKit's Descriptors module. For each generated molecule, four properties were computed: molecular weight (Descriptors.MolWt), LogP (Descriptors.MolLogP), hydrogen bond donor count (Descriptors.NumHDonors), and hydrogen bond acceptor count (Descriptors.NumHAcceptors). Molecules passing all four criteria (or violating at most one) were classified as drug-like candidates. From the 10 generated molecules, 7 passed Lipinski filtering and advanced to further evaluation. The final set of 8 lead candidates (including one additional candidate from an earlier generation run) was standardized as the evaluation cohort.**

**4.4 Quantum Chemistry Module Implementation**

**The quantum chemistry module was implemented using PySCF (Python-based Simulations of Chemistry Framework) to compute HOMO-LUMO gap values for each candidate. Molecular 3D coordinates were generated from SMILES using RDKit's AllChem.EmbedMolecule function with UFF geometry optimization. The Hartree-Fock method was applied to compute molecular orbital energies, from which HOMO and LUMO energy levels were extracted. The gap was computed as E_gap = E_LUMO - E_HOMO in electron volts (eV). Results were saved as quantum_results.csv with Candidate #5 achieving the highest gap value of 10.49 eV.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**55**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**4.5 Streamlit Web Dashboard Implementation**

**4.5.1 Discovery and Visualization Engine**

**Figure 4.1: AI Pipeline Workflow**

**The Streamlit dashboard was implemented as a multi-page application with centralized authentication. The main application file (app.py) implements a login portal with hardcoded researcher credentials and session state management. Authentication status is stored in Streamlit's session_state and checked at the top of every subsequent page to enforce access control.**

**The Home page (1_home.py) provides biological context on HIV-1 Protease, including target description, mechanism of inhibition, and structural analysis with embedded protein structure images. The Discovery Engine page (2_Discovery.py) displays all 8 lead candidates in a responsive grid layout, showing 2D molecular structure images (rendered via RDKit's Draw.MolToImage), AI confidence scores, electronic stability metrics, and Lipinski property panels. Interactive 3D molecular visualization is enabled through py3Dmol integration, allowing researchers to rotate, zoom, and inspect molecular conformations directly in the browser. A shared candidates.py module centralizes the candidate data for reuse across all pages.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**56**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**4.5.2 Multi-Stage Evaluation Pipeline**

**Figure 4.2: Streamlit Dashboard Architecture**

**The evaluation pipeline was implemented across four dedicated Streamlit pages, each performing independent analysis and presenting interactive results.**

**The Synthesizability Analysis page (3_Synthesizability.py) computes SA Scores for all candidates using RDKit's sascorer module. Results are displayed as horizontal bar charts (ranked by score), detailed data tables with progress column visualization, molecular structure cards with difficulty classifications, and key findings highlighting the easiest and hardest to synthesize candidates. Computation results are cached using Streamlit's @st.cache_data decorator for performance optimization.**

**The ADMET Analysis page (4_ADMET.py) performs comprehensive pharmacokinetic profiling including Lipinski compliance, Veber's rules, QED scoring, GI absorption prediction, BBB penetration assessment, CYP2D6 inhibition risk, and bioavailability scoring. Results are presented in a comprehensive overview table with a property reference guide explaining each metric's significance.**

**The Molecular Docking page (5_Docking.py) displays pre-computed binding affinity results and residue interaction profiles for each candidate docked against HIV-1 Protease (1HSG). Interactive 3D molecular visualization enables per-candidate structural inspection. Results include binding affinity rankings, interpretation guides, and key findings.**

**The Final Ranking page (6_FinalRanking.py) implements the weighted composite scoring system, normalizing and combining all five evaluation metrics (AI Score, HOMO-LUMO Gap, Docking Affinity, QED, SA Score) into a single percentage-based composite score. The page displays weight configurations, ranking bar charts, comprehensive comparison tables, and detailed winner/runner-up profiles with recommended next steps for experimental validation.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**57**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**4.6 Final Ranking and Composite Score Implementation**

**The composite ranking engine was implemented as a centralized scoring component. It receives raw metric values from all evaluation modules and performs min-max normalization to map each metric to the 0-1 range. Metrics where lower values indicate better performance (docking affinity, SA Score) are inverted during normalization.**

**Weighted score aggregation was implemented using the predefined weight configuration: Docking (0.30), QED (0.25), AI Score (0.20), SA Score (0.15), HOMO-LUMO Gap (0.10). The final score is computed as a weighted linear combination of normalized metric values and expressed as a percentage (0-100). Candidates are ranked by descending composite score, with the top-ranked candidate recommended as the primary lead compound.**

**The system outputs a structured ranking table indicating each candidate's individual metric values, normalized scores, and final composite ranking. The recommended lead compound is presented with a comprehensive profile card showing all evaluation dimensions, along with specific recommendations for next steps including in vitro validation, lead optimization, synthesis feasibility studies, and extended toxicity profiling.**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**58**

DE NOVO-HIV : Neural-Quantum Protease Inhibition

**CHAPTER 5**

**CONCLUSION AND FUTURE SCOPE**

**5.1 Conclusion**

**In conclusion, the proposed AI-driven drug discovery pipeline provides a comprehensive and integrated solution for identifying novel HIV-1 Protease inhibitor candidates through the combination of deep generative modeling and multi-criteria computational evaluation [1,3,4]. The system's modular architecture ensures that each component—data curation, LSTM-based molecular generation, drug-likeness filtering, quantum chemistry analysis, molecular docking, ADMET profiling, synthesizability scoring, and composite ranking—functions efficiently while maintaining flexibility for future enhancements.**

**By employing LSTM neural networks trained on approximately 9,480 HIV-related drug molecules, the system successfully generated chemically valid novel molecular structures with a 100% validity rate. The multi-stage evaluation pipeline assessed each candidate across five critical dimensions, enabling objective comparison and identification of the most promising lead compound through weighted composite scoring. The interactive Streamlit web dashboard makes complex molecular evaluation data accessible and explorable, bridging the gap between computational chemistry and practical drug development decision-making [7, 8, 13, 15]. Overall, this project establishes a strong foundation for deploying AI-powered, end-to-end computational drug discovery systems targeting clinically relevant viral enzymes.**

**5.2 Future Improvements and Enhancements**

**For future development, the system can be extended in several directions to enhance its capabilities and clinical relevance. The LSTM-based generator could be augmented with reinforcement learning to guide generation toward molecules with specific desired properties, such as high predicted binding affinity or favorable ADMET profiles [7–9, 12, 15]. Transfer learning techniques could be applied to fine-tune the model specifically on known HIV-1 Protease inhibitors, biasing generation toward the most relevant chemical space.**

**The molecular docking module could be upgraded to perform real-time AutoDock Vina simulations rather than relying on pre-computed results, enabling on-the-fly evaluation of newly generated candidates. Integration with molecular dynamics simulations could provide more accurate binding affinity predictions by accounting for protein flexibility and solvation effects. The ADMET prediction module could be enhanced by incorporating machine learning-based ADMET models trained on clinical pharmacokinetic data, replacing heuristic rules with data-driven predictions for properties such as CYP inhibition, hERG toxicity, and metabolic stability [5, 6, 19, 24].**

**Additionally, the pipeline could be adapted to target other viral or oncological drug targets by retraining the LSTM model on target-specific molecular datasets. Integration with experimental validation workflows, cloud-based high-performance computing, and automated retrosynthetic planning tools could further accelerate the translation of computational predictions into testable drug candidates [7, 8, 10, 13, 15].**

**DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING**

**59**

DE NOVO-HIV : Neural-Quantum Protease Inhibition
