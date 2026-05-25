# 🎬 Sistem de Recomandare Filme

## Problema
Vreau sa construiesc un sistem care recomanda filme pe baza unei descrieri date de utilizator, similar cu Netflix. Daca utilizatorul scrie "vreau un film de actiune in spatiu", sistemul gaseste filmele cele mai potrivite.

## Dataset
- Sursa: Dataset creat manual cu filme cunoscute (inspirat din TMDB Kaggle Dataset)
- Link Kaggle original: https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata
- Dimensiune: 50 filme
- Coloane: titlu, gen, rating, descriere, lungime_descriere

## Ce am facut
1. Am explorat datele (EDA) cu 6 grafice
2. Am curatat textul (lowercase, caractere speciale)
3. Am antrenat 2 modele: TF-IDF si Sentence Transformers
4. Am comparat modelele
5. Am creat un model final care le combina pe ambele
6. Am salvat modelele

## Rezultate

| Model | Scor mediu | Viteza | Intelege sinonime |
|-------|-----------|--------|-------------------|
| TF-IDF | ~0.15 | Rapid | Nu |
| Sentence Transformers | ~0.45 | Mai lent | Da |

**Modelul final:** Sentence Transformers + TF-IDF combinat (70% semantic + 30% tfidf)

## Cum sa rulati
```bash
pip install -r requirements.txt
# Deschideti notebook.ipynb in Google Colab
```

## Ce am invatat
A fost interesant sa vad diferenta intre un model clasic (TF-IDF) si unul bazat pe AI (Sentence Transformers). TF-IDF cauta cuvinte exacte, pe cand modelul semantic intelege sensul. De exemplu, daca caut "aventura cosmica", TF-IDF nu gaseste nimic relevant dar modelul semantic gaseste filme despre spatiu si astronauti.
