# Protein-Stability-Prediction

# Research Summary: Predicting Protein Thermostability

The goal of this assignment is to develop a model that predicts the ranking of protein thermostability as measured by tm i.e. the melting point, following single-point amino acid mutations and deletions. Accurate predictions of protein stability are crucial for various biotechnological and pharmaceutical applications.

Dataset Description:

    Training Set: Includes natural and engineered protein sequences with single or multiple mutations. Given Data has been derived from multiple sources of published studies such as the Meltome atlas and other public datasets.

    Test Set: Contains experimental melting temperatures for 2413 single-mutation variants of an enzyme (GenBank: KOC15878.1), provided by Novozymes A/S. Features: 1. seq_id: Unique identifier for each protein variant. 2. protein_sequence: Amino acid sequence of each variant, which determines the protein thermostability. 3. pH: Acidity level of aqueous under which stability was measured. 4. data_source: Source of the data. 5. tm: Experimental melting temperature which is our target variable. Higher tm values signify greater protein thermostability

Current State-of-the-Art Techniques:

Evolutionary Scale Modeling (ESM):

       Overview: ESM utilizes transformer-based language models trained on large-scale protein sequences to predict various properties.  

       Advantage: Captures long-range dependencies and evolutionary information from sequences.

       Limitation: High computational requirements and limited by the quality and diversity of training data.

       Source: Rives et al., "Biological structure and function emerge from scaling unsupervised learning to 250 million protein sequences," 2021 

Rosetta:

        Overview: A suite of software tools for protein modeling and analysis, including structure prediction and stability assessment.

        Advantage: Robust and extensively validated across numerous protein engineering tasks.

        Limitation: Computationally intensive and requires significant expertise to use effectively.

        Source: Leaver-Fay et al., "ROSETTA3: an object-oriented software suite for the simulation and design of macromolecules," 2011 .

Limitations of Current Techniques:

    Computational Resources: There is a High computational cost incurred by training and inference of models like ESM and Rosetta.

    Data Quality and Diversity: Model Performance is highly dependent on the quality and diversity of the training dataset, which can lead to high bias in models that do not generalize well to novel sequences.

    Interpretability: Many advanced models, especially DL-based methods, lack interpretability, making it difficult to understand the underlying mechanisms driving predictions.

    Generalization: Models trained on specific datasets may not generalize well to different types of proteins or experimental conditions, thereby limiting their utility.

Continuous advancements in model architecture, training algorithms, and data curation are of the essence to overcome above mentioned challenges and improve the reliability and utility of protein stability predictions.
