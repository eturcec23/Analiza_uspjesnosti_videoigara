# Analiza uspješnosti videoigara 

Projekt iz kolegija **Programiranje za analizu podataka (PzAP)**.

**Student:** Ela Turčec

Ovaj projekt bavi se analizom industrije videoigara kroz integraciju podataka iz više izvora. Cilj je istražiti odnos između prodajnih rezultata, žanrova i procijenjenih razvojnih budžeta kako bi se izračunao povrat na investiciju (ROI).

##  Opis projekta

Projekt demonstrira cjelokupan proces inženjerstva podataka (Data Engineering) i analize:
1.  **Prikupljanje podataka:** Integracija statičkog CSV skupa podataka s dinamičkim podacima dohvaćenim putem vanjskog REST API-ja.
2.  **ETL Proces:** Čišćenje, transformacija i generiranje nedostajućih varijabli (procijenjeni budžet) pomoću Python generatora.
3.  **Pohrana:** Dizajniranje i pohrana integriranog skupa podataka u relacijsku bazu (**SQLite**).
4.  **Backend:** Izrada vlastitog **REST API**-ja (Flask) za posluživanje obrađenih podataka.
5.  **Analiza:** Vizualizacija financijske uspješnosti (ROI) pojedinih naslova i žanrova.

##  Korištene tehnologije

Projekt je implementiran u programskom jeziku **Python** koristeći sljedeće biblioteke:

* **Pandas & NumPy:** Manipulacija podacima i numerički izračuni.
* **SQLAlchemy:** ORM za interakciju sa SQLite bazom podataka.
* **Flask:** Mikro-okvir za izradu REST API sučelja.
* **Requests:** HTTP klijent za dohvat podataka s vanjskih API-ja.
* **Matplotlib & Seaborn:** Vizualizacija podataka.

##  Izvori podataka

Korišteni su međusobno heterogeni izvori podataka:
1.  **CSV:** *Video Game Sales Dataset* (Kaggle) - podaci o prodaji.
2.  **REST API:** *RAWG Video Games Database API* - dodatni meta-podaci o igrama.
3.  **Generirani podaci:** Algoritamska procjena budžeta temeljena na žanru (implementirano pomoću `numpy.random`). (Uz projekt je priložena već generirana baza podataka (`videoigre.db`). Kod je dizajniran tako da će automatski koristiti tu bazu ili kreirati novu ako ona ne postoji.)

##  Upute za pokretanje

Projekt je izrađen u obliku Jupyter (Colab) bilježnice.

### Preduvjeti
Potrebno je imati instaliran Python 3 i sljedeće biblioteke (ako pokrećete lokalno):

```bash
pip install -r requirements.txt

##  Poveznice na projekt

Svi resursi vezani uz ovaj projekt dostupni su na sljedećim poveznicama:

* **GitHub Repozitorij:** https://github.com/eturcec23/Analiza_uspjesnosti_videoigara
* **Google Colab Bilježnica:** https://colab.research.google.com/drive/1EcafDQlF9kPn_oIWcB4snIozCb7KyAev?usp=sharing

###  Napomena za pokretanje
Uz projekt je priložena već generirana baza podataka (`videoigre.db`). Kod je dizajniran tako da će automatski koristiti tu bazu za brzi pregled podataka. U slučaju da baza nije prisutna, skripta će automatski pokrenuti proces dohvaćanja i generiranja nove baze (što može potrajati nekoliko minuta zbog API ograničenja).
Također je i priložen csv.

