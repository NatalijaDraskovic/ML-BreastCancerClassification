# ML-BreastCancerClassification

## Kratak opis

Invazivni duktalni karcinom (IDC) je najčešći podtip svih karcinoma dojke. Kako bi se odredio nivo agresivnosti čitavog uzorka patolozi se obično fokusiraju na regione koji sadrže IDC, pa je jedan od uobičajenih koraka da se uyorak podeli na delove i onda raygraniće tačna područja IDC unutar čitavog uyorka kako bi se odredio stepen agresivnosti, kao i tačno područje zahvaćeno IDC-om.

Originalni skup podataka sastojao se od 162 cele slike uyoraka raka dojke skeniranih pri 40x. Od toga je iydvojeno 277.524 zakrpa veličine 50 x 50 (198.739 IDC negativnih i 78.786 IDC pozitivnih). Naziv foldera predstavlja id pacijenta i u njemu se nalaze označene IDC pozitivne i IDC negativne zakrpe odvojene u poslebne foldere, sa tome da nayiv svake datoteke yakrpe ima format ID_idx5_xX_yY_classN.png, na primer 8863_idx5_x51_y1251_class0.png, gde je ID id pacijenta, X vrednost x koordinate yakrpe, Y vrednost y koordinate yakrpe i N clasa kojoj data yakrpa pripada, 0 u slučaju da nije IDC i 1 u slučaju da jeste IDC.

Ideja rada je da se obuči model koji će za dobijene zakrpe predvideti kojoj od klasa one pripadaju. Kako se radi o zakrpama, a ne čitavim uzorcima rađeno je na tome da se sam uzorak rekonstruiše nakon predviđanja kako bi se detektovala tačna lokacija IDC-a. Skup podataka nad kojim je rađeno predstavlja nešto promenjen skup podataka pomenut u prethodnom pasusu, dodato mu je još podataka, on sadrži podatke ya 279 pacijenata, ali ne sadrži originalne uyorke iz kojih su uzete zakrpe. Takođe rekonstrukcijom je utvrđeno da yakrpe ne pokrivaju kompletnu površinu uyorka već ima nedostajućih podataka.

## Programski jezici i tehnologije

Igrica je izrađena u programskom jeziku Python korišćenjem uz korišćenje sledećih biblioteka:
  * numpy
  * pandas
  * matplotlib
  * seaborn
  * skimage
  * sklearn
  * imblearn
  * keras
 
od kojih su sve osim biblioteka keras i imblearn dostupne u okviru instalacije Anaconde.

Biblioteke koje je potrebno instalirati mogu se instalirati na sledeći nacin:
  * install -c conda-forge keras
  * conda install -c conda-forge imbalanced-learn

Korišćeni skup podataka: https://www.kaggle.com/paultimothymooney/breast-histopathology-images.
Modeli koji nisu mogli biti okačeni na Github-u zbog veličine mogu se pronaći na Google Drive na linku: https://drive.google.com/drive/folders/1Su25LRT88w0UjsN1_Ls3RlGnvg1ckkeH.

## Autor
  Natalija Drašković natalija.draskovic@outlook.com, @NatalijaDraskovic
