# 🎬 Sistem de Recomandare Filme

## Problema

Sistemul nostru are scopul de a recomanda filme.

## Dataset

Pentru acest proiect, am utilizat un set de date despre filme de pe Kaggle, cunoscut sub numele de TMDB 5000 Movie Dataset.

Puteți găsi setul de date original aici: https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata.

## Ce am facut

1. Am început prin a explora datele, folosind 6 grafice pentru a înțelege mai bine informațiile disponibile.

2. Am curățat textul, transformând toate caracterele în litere mici și eliminând caracterele speciale.

3. Am antrenat două modele diferite: unul folosind tehnologia TF-IDF și celălalt folosind Sentence Transformers.

4. Am comparat performanțele celor două modele pentru a vedea care este mai eficient.

5. Am decis să creez un model final care combină avantajele ambelor modele.

6. Am salvat modelele pentru a putea fi utilizate ulterior.

## Rezultate

| Model | Scor mediu | Viteza | Înțelege sinonime |

|-------|-----------|--------|-------------------|

| TF-IDF | în jur de 0.15 | Rapid | Nu |

| Sentence Transformers | în jur de 0.45 | Mai lent | Da |

**Modelul final:** Am combinat Sentence Transformers cu TF-IDF, folosind o pondere de 70% pentru partea semantică și 30% pentru TF-IDF.

## Cum să rulați

Pentru a rula proiectul, vă recomandăm să urmați pașii de mai jos:

```bash

pip install -r requirements.txt

# Deschideți notebook.ipynb în Google Colab

```

## Ce am învățat

A fost foarte interesant să văd diferența dintre un model clasic de recomandare, cum ar fi TF-IDF, și unul bazat pe inteligență artificială.
