# Modele Matematyczne w Uczeniu Maszynowym 
[PL only]  

```
Zakład Elektrotechniki Teoretycznej i Informatyki Stosowanej  
Instytut Elektrotechniki Teoretycznej i Systemów Informacyjno-Pomiarowych  
Wydział Elektryczny, Politechnika Warszawska  

Autorka: mgr inż. Aleksandra Osowska-Kurczab
```

Ćwiczenia laboratoryjne do przedmiotu Modele Matematyczne w Uczeniu Maszynowym, oferowanego studentom studiów magisterskich z kierunku Informatyki Stosowanej na Wydziale Elektrycznym, Politechniki Warszawskiej. Ćwiczenia obejmują praktyczne zagadnienia obejmujące analizę danych, tworzenie modeli uczenia maszynowego i metody ewaluacji. 

## **Konfiguracja środowiska**

1. **Jupyter notebook**

Ćwiczenie zostało napisane w środowisku jupyter notebook - jest to interaktywne środowisko, które pod wieloma względami przypomina Matlaba. Podzielone jest na komórki, które wykonywane są w stylu "skryptowym" (czyli dokładają do środowiska globalnego kolejne operacje, zmienne itp) - nie są to osobno wykonywane programy. Notebook'i są bardzo często wykorzystywane w DataScience ze względu na prostotę i szybkość prototypowania, która jest możliwa dzięki takiemu konstruktowi środowiska. Dodatkowym plusem jest łatwość dokumentacji kodu - można wstawiać komórki tekstowe i pisać kod prawie jak pamiętnik :) 

Aby zaznajomić się ze środowiskiem polecam przewodnik napisany bezpośrednio przez autorów dostępny [tutaj](https://jupyter.org/try).

2. **Google colab**

Aby nie musieć instalować środowiska Pythonowego bezpośrednio na swoim komputerze (virtual env, anaconda, miniconda) można skorzystać z narzędzia Google Colaboratory (Google Colab). Potrzebne jest jedynie konto Google. Google Colab ma bardzo wiele zalet, a wśród nich - bezpłatne zasoby obliczeniowe w postaci GPU i TPU. Nie jest to rozwiązanie produkcyjne, ale do prototypowania rozwiązań jest w zupełności wystarczające. 

Aby dowiedzieć się więcej o Google Colab najlepiej to zrobić zapoznając się z notebookami przygotowanymi przez samego Google'a:

* Co to jest Colaboratory? [PL] [link](https://colab.research.google.com/notebooks/intro.ipynb)
* Overview of Colaboratory Features [EN] [link](https://colab.research.google.com/notebooks/basic_features_overview.ipynb)

Jeżeli znajdzie się śmiałek, który tak czy siak zechce zsetupować sobie środowisko pythonowe to zapraszam do kontaktu chętnie pomogę. Dla wstydliwych wstawiam kilka linków, które mogą pomóc w pierwszych krokach:

* Środowisko wirtualne w Python [PL] [link](https://miroslawmamczur.pl/srodowisko-wirtualne-w-python/)
* Ideal Python environment setup for Data Science [EN] [link](https://towardsdatascience.com/ideal-python-environment-setup-for-data-science-cdb03a447de8)
* Installing Python for Data Analysis [EN] [link](https://www.codecademy.com/articles/install-python-data-analysis)

3. **Python** 

Myślę, że nie muszę Państwa przekonywać, że warto nauczyć się Pythona jeżeli myślicie o karierze w Data Science. Oczywiście nie jest to jedyny język obecny w środowisku (Matlab - środowisko akademickie, R - matematycy, SAS - ekonomiści, Julia, Jax, Java, Scala, SQL ...), ale z całą pewnością jest najbardziej rozpowszechniony i najczęściej pożądany wśród kandydatów na stanowiska związane z uczeniem maszynowym. Praktycznie wszystkie większe korporacje w swoich projektach korzystają właśnie z Pythona (w NLP czasami dominuje Java, ale ta tendencja powoli zanika). 

Jeżeli ktoś z Państwa jeszcze nie miał przyjemności pracować z tym językiem to zachęcam do samodzielnej nauki - materiałów w internecie można znaleźć całe mnóstwo. Na zachętę wstawiam przykładowy mikro-kursik realizowany (a jakżeby inaczej) bezpośrednio w Google Colab [kurs CS231n oferowany przez Stanford](https://colab.research.google.com/github/cs231n/cs231n.github.io/blob/master/python-colab.ipynb). Polecam go, ponieważ w sposób szybki obrazuje wszystkie najważniejsze funkcjonalności i struktury danych (warto przejść dla niego również dla powtórzenia i sprawdzenia czy zna się całe abecadło Pythona).

4. **NN frameworks**

Pisanie kodu potrzebnego do modularnej budowy modeli neuronowych czy uczenia i inferencji nie jest prostym zadaniem. Aby ułatwić prototypowanie, uczenie i wdrażanie modeli na produkcję przez lata rozwijane były biblioteki automatyzujące wiele z tych procesów i pozwalające na napisanie prostych projektów w zaledwie kilka linii kodu. Do najpopularniejszych bibliotek w Pythonie należą:
* Tensorflow (1.0 i 2.0)
* Keras (wyżej poziomowy Tensorflow)
* PyTorch

O innych bibliotekach można poczytać np. [tutaj](https://wiki.pathmind.com/comparison-frameworks-dl4j-tensorflow-pytorch).   

Podczas tego ćwiczenia wykorzystywany będzie [PyTorch](https://pytorch.org/). Jest to wyjątkowo wygodna i dobrze udokumentowana biblioteka pozwalająca na bardzo dużą dowolność w budowaniu modeli, dostosowywaniu procesu uczenia. Raz napisany kod często może być w bardzo prosty sposób dostosowany do kolejnych projektów. Najlepiej uczyć się poprzez projekty, do czego Państwa gorąco zachęcam (np. w ramach dyplomu). Kilka tutorialów prezentujących podstawowe właściwości biblioteki zostały przygotowane przez autorów PyTorcha i udostępnione na stronie głównej biblioteki w zakładce [Tutorials](https://pytorch.org/tutorials/). 
