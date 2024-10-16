# fakenews_detector
A fake news detector model
## Ce modèle permet de détecter si un article (en anglais) est une fake news ou non.
Ce modèle a été entraîné avec le framework [scikit-learn](https://scikit-learn.org/stable/) et son modèle __LogisticRegression__

## Dataset 
La dataset utilisé est le dataset "fake-and-real-news-dataset" disponible en ligne en cliquant [ici](https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset)

## Installation
Pour utiliser le modèle, faites la commande suivante dans votre terminal : 

```
git clone https://github.com/Styyz1/fakenews_detector
```
Veillez à avoir le module ["joblib"](https://joblib.readthedocs.io/en/stable/) d'installer.

Ensuite, ouvrez le notebook nommé "detector.ipynb", exécutez la première ceullue. Dans la deuxième cellule, sur la ligne "new_article", renseignez votre nouvel article et exécutez la cellule. 

## Exemple d'utilisation

```
# Exemple d'article à prédire
new_article = ["""Donald Trump just accused millions of Americans of voter fraud, proving once again that he should be denied the presidency.Over the course of the last 24 hours, Trump has been whining about a recount effort in Wisconsin and attempts to trigger recounts in Michigan and Pennsylvania. If the recount goes against him, Hillary Clinton would become the President-Elect and Trump would be forced to go home and cry into a gold-lined pillow about how big of a loser he is.In addition to those Twitter posts about recounts, Trump just posted three more bragging that he won the popular vote even though the current vote count shows Hillary with more than a 2 million vote lead.Trump claims he won the popular vote because 3 million people voted illegally, which is a wild accusation that has zero evidence supporting it.In addition to winning the Electoral College in a landslide, I won the popular vote if you deduct the millions of people who voted illegally  Donald J. Trump (@realDonaldTrump) November 27, 2016Trump then claimed that he would have won the popular vote had he focused more on a few large states rather than smaller ones.It would have been much easier for me to win the so-called popular vote than the Electoral College in that I would only campaign in 3 or 4  Donald J. Trump (@realDonaldTrump) November 27, 2016states instead of the 15 states that I visited. I would have won even more easily and convincingly (but smaller states are forgotten)!  Donald J. Trump (@realDonaldTrump) November 27, 2016But the fact remains that Trump LOST the popular vote by a wide margin and his electoral margin could be flipped if recounts go the way many hope.Regardless, Donald Trump just disqualified himself from the presidency again by attacking the democratic process. Recounts are legal and Hillary Clinton has every right to ask for one, especially since Trump margin of victory in Wisconsin, Michigan, and Pennsylvania are so narrow. They re part of the democratic process.Furthermore, Trump just insulted 3 million Americans by claiming that their votes don t count. He has absolutely no proof that 3 million people voted illegally, and such a wild accusation proves that he is unfit to lead this country.Enough is enough. Donald Trump is a disgrace and he should be forced to step aside. He does not deserve the the title of President-Elect and he certainly does not deserve to be called President. Period"""]

# Vectoriser l'article avec le TfidfVectorizer chargé
new_article_vectorized = loaded_vectorizer.transform(new_article)

# Prédire avec le modèle chargé
prediction = loaded_model.predict(new_article_vectorized)

# Afficher le résultat
result = "Fake" if prediction == 0 else "True"
print(f"L'article est : {result}")
```

```
L'article est : Fake
```
