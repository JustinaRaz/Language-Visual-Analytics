# Assignment 1: Extracting linguistic features using ```spaCy```

## Short description

The Python script for the assignment is designed to extract linguistic information from a corpus of multiple texts - relative frequency of nouns, verbs, adjectives, adverbs, and a total number of unique words related to person, location or organization from each text. Then, it saves the results into multiple **csv** files.

## Data and structure

*The Uppsala Student English Corpus (USE)* is used in the present assignment. The information about the data and its documentation can be found [here](https://ota.bodleian.ox.ac.uk/repository/xmlui/handle/20.500.12024/2457). Make sure to download the dataset and store it in a folder called **input**.

The overall structure of the folders should be as follows:

```
assignment-1-LANG/
├── emissions/
├── input/
│   ├── USEcorpus/
│       ├── USEcorpus/
│       │   ├── a1/
│       │   ├── .../
│       │   └── c1/
│       └── readme.md
├── out/
│   ├── a1_counts.csv
│   ├── ...
│   └── c1_counts.csv
├── src/
│   ├── assignment-1.py
│   └── functions.py
├── README.md
├── requirements.txt
└── setup.sh
```

## To reproduce

In order to run the script smoothly, the following steps should be completed:

- Open the terminal and set the working directory to the folder:

```python
cd assignment-1-LANG
```
- In the terminal, run the following command to install the required modules and set up the *virtual environment*:

```python
bash setup.sh
```
- In the terminal, activate the virtual environment by running:

```python
source ./env/bin/activate
```

- In the same terminal, run the .py script:
 
```python
python src/assignment-1.py
```
- Once the script has finished running, the output files will be stored in the folder called **out**. To deactivate the virtual environment, run the following:

```
deactivate
```

## Summary

Once the script has finished running, the main output can be located in the folder called ```out```. It will contain multiple **csv** files, one for each data folder in the ```input``` (a1, a2, ..., c1).

An example of the **csv** file:

Filename | RelFreq NOUN | RelFreq VERB | RelFreq ADJ | RelFreq ADV | Unique PER | Unique LOC | Unique ORG | 
--- | --- | --- | --- | --- | --- | --- | --- |
0100.a1.txt | 1526.39 | 1526.39 | 827.39 | 827.39 | 0 | 0 | 0 |
0101.a1.txt | 1181.7 | 1257.94 | 597.2 | 851.33 | 1 | 0 | 0 |
0102.a1.txt | 1506.68 | 1227.22 | 692.59 | 486.03 | 1 | 0 | 0 |
...

The columns represent:

-  *Filename* - text document for which the data was produced;
- *RelFreqNOUN* - the relative frequency (RF) of nouns;
- *RelFreqVERB* - the RF of verbs;
- *RelFreqADJ* - the RF of adjectives;
- *RelFreqADV* - the RF of adverbs;
- *UniquePER* - the number of unique personal names in a given text;
- *UniqueLOC* - the number of unique locations in a given text;
- *UniqueORG* - the number of unique organizations in a given text.

## Discussion

As with any programming task, there are always ways of how the code or the analysis can be improved. Here are some ways how the code/analysis could be improved:

- Use a larger English language model. This could enhance the accuracy of the results, however, it would require more time and resources to process the text.
- Provide the user with more flexibility with where the input files are located. 

## CodeCarbon tracking

Once the script has finished running, ```emissions``` folder will contain two **csv** files, representing **the total** and **task-specific** environmental impact of this code in terms of CO₂eq.

The total CO₂eq calculated for this code resulted in **0.00011** kilograms of CO₂-equivalent.

Task specific results:

- On average, calculation of **relative frequencies** has resulted in **_** kilograms of CO₂-equivalent.
- On average, calculation of **unique entities** has resulted in **_** kilograms of CO₂-equivalent.
