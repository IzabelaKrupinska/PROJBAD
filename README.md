# PROJEKT BADAWCZY
## Generowanie słownego opisu obrazu
## Bany Maciej, Krupińska Izabela
## Wstęp
Projekt badawczy opierał się na słowym opisie obrazów.
Do trenowania i testowania użyliśmy zbioru flickr8k. 
Opisy są generowane na podstawie korzystania z wyuczonego modelu.
Model składa się z dwóch części. Informacje z obrazu oraz opisu obrazu.
Kolejną częścią naszych badań było przetłumacznie podpisów zbioru na język polski z wykorzystaniem Azure. 
Następnie wytrenowaliśmy model z polskimi podpisami.

### Wykonane zadania
#### Wyodrębnienie cech obrazu
Podzieliliśmy nasz zbiór danych na treningowy o wielkości 6000 obrazów oraz testowy 1000.
Do wyodrębnienia cech z obrazu użyliśmy sieci neuronowej. Korzystaliśmy z tranfer learning z modelu InceptionV3.
Będziemy używać drugiej ostatniej warstwy, która będzie reprezentowac obraz w postaci licz, a nie jako klasyfikator.

#### Definiowanie cech tekstu
Użyliśmy funkcji Word Embedding.

#### Generator napisów
Do generowania napisów używamy funkcji Gready Search.

#### Tłumaczenie zbioru na język polski
Skorzysaliśmy z Azure i przetłumaczyliśmy flickr8k na język polski.

#### Trenowanie nowego zbioru
Zbiór w języku polskim podzieliliśmy tak samo na trenujący i testowy, wytrenowlaiśmy go również w ten sam sposób.

## Wyniki
Nasze wyniki sprawdzaliśmy za pomocą miar BOW, BLEU, CIDER.
Wyniki zostały porównane dla zbiorów trenujących i testujących zbioru danych w języku angielskim i polskim.
Szczegółowe wyniki i opisy miar zostały zawarte w plikach WYNIKI.
Poniżej otrzymany podpis dla zbioru danych w języku angielskim.

<img src="eng.PNG" width = 400> 

Poniżej otrzymany podpis dla zbioru danych w języku polskim.

<img src="pl.PNG" width = 400> 

## Źródło
https://paperswithcode.com/paper/deep-visual-semantic-alignments-for 
https://arxiv.org/abs/1412.2306
https://hub.packtpub.com/generating-automated-image-captions-using-nlp-and-computer-vision-tutorial/
https://towardsdatascience.com/image-captioning-with-keras-teaching-computers-to-describe-pictures-c88a46a311b8
https://machinelearningmastery.com/develop-a-deep-learning-caption-generation-model-in-python/
