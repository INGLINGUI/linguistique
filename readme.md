-- Dico --

Il faut les compresser (Menu Dela -> compress)
puis les appliquer aux docs (Apply lexical ressources), on sélectionne les deux dico's sinon pas pris en compte dans les graphes.

- Days (lundi, mardi ...)
- Months (janvier, février ...)

-- Arborescence des graphes --

Final

- Hours
	- hours-numeric (12:48)
	- hours-with-letter (12h - 12h48 12 heures)
- Date (jours (lettre/chiffre) - mois - année optionnelle)
	- years 
        

V0.1 :

hours-numeric.grf

- 1:02  par contre on ne peut pas reconnaitre 1:60 et +
- 01:02 par contre on ne peut pas reconnaitre 01:60 et +
- 19:02 par contre on ne peut pas reconnaitre 19:60 et +
- 20:02 par contre on ne peut pas reconnaitre 25:05 ou 24:60

hours-with-letter.grf

- 00heure
- 00 heure
- 0 heure
- 1 heure
- 1 heure 59
- 2 heures 59 mais pas 2 heure ni 2 heures 60 (protection)
- 19 heures 59
- 24 heures 59
- 24h 59
- 24 h 59

hours

il appel hours-numeric / hours-with-letter

Years 

Reconnait les années positives de 0 à 2015

Date

mardi 01 mars
mardi 01 mars 2008
mardi 10 mars
mardi 10 mars 2008
10 mars 2008
10 mars
mardi 10 11 2008
mardi 10/11/2008
10/11/2008

protection contre 30 février / 31 septembre

Final :

Dans la première partie on reconnait :

19 à 20 h
19 à 20 heures
19 jusqu'à 20 heures
19 jusqu'à 21:30

Dans la seconde partie 

20 h à 21:30
20 heures à 21 heures
20 heures jusqu'à 21 heures 30
etc.

Troisième partie 

mercredi 4 septembre 2004 au mercredi 4 septembre 2005
mercredi 4 septembre 2004 et le jeudi 5 septembre 2004
mercredi 4/05/2004 au ...
mercredi 4 05 2004 au ...
date simple
