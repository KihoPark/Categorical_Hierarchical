# Categorical_Hierarchical
In our paper, we show that large language models represent categorical concepts as simplices and hierarchical relations as orthogonality.

We confirm our theory with Gemma-2B representations and this repo provides the code for the experiments.

## Data
[`animals.json`](data/animals.json) and [`plants.json`](data/plants.json) are sets of words generated by ChatGPT-4.

`***_gemma.json` and `***_graph.adjlist` files in [`data`](data) are the collections of words and hierarchy graph of WordNet for noun and verb, which are obtained by `get_wordnet_hypernym.ipynb`.

## Requirement
You need to install Python packages `transformers`, `networkx`, `scikit-learn`, `nltk`, `inflect`, `torch`, `numpy`, `seaborn`, `matplotlib`, `json`, and `tqdm` to run the codes. Also, some GPUs would be helpful to implement the codes efficiently.

Run `store_matrices.py` first to store the unembedding vectors, before you run other jupyter notebooks.

## Experiments
- [**`1_Animal.ipynb`**](1_Animal.ipynb): We display 2D plots in Figure 2 and 3D plots in Figure 3.
- [**`2_Noun_Test.ipynb`**](2_Noun_Test.ipynb): We validate the existence of the vector representations for each feature in WordNet noun hierarchy in Figure 4.
- [**`3_Noun_Heatmap.ipynb`**](3_Noun_Heatmap.ipynb): We confirm that the hierarchical relation in WordNet noun hierarchy is encoded as orthogonality in Figure 5. Also, we zoom in the heatmaps in Figure 8 for the subtree in Figure 7.
- [**`4_Verb_Test.ipynb`**](4_Verb_Test.ipynb): We validate the existence of the vector representations for each feature in WordNet verb hierarchy in Figure 9.
- [**`5_Verb_Heatmap.ipynb`**](5_Verb_Heatmap.ipynb): We confirm that the hierarchical relation in WordNet verb hierarchy is encoded as orthogonality in Figure 10.