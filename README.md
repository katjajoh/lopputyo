Tänne tulee tietoa lopputyön vaiheista
Tämä rivi on MAIN-versiossa
Tämä rivi on TOINEN_HAARA-versiossa

# Git-lopputyö: terminaaliversio

### 📘 Projektin idea  
Tein kurssin lopputyönä git-harjoittelurepon, jossa testasin erilaisia komentoja ja versionhallintaa.

---

### ✅ Käytetyt Git-komennot  
git clone git@github.com:katjajoh/lopputyo.git  
git add, git commit  
git branch, git checkout  
git merge (toinen_haara → main)  
git stash ja git stash pop  
git revert (virheellisesti lisätty tiedosto)  
git cherry-pick (kolmas_haara -branchista yksi commit mainiin)  
git tag v1.0.0 ja git push origin v1.0.0  
git rebase main (toinen_haara päivitettiin)  
git push, git pull  
.gitignore-tiedoston lisäys  
git pull origin main

---

### 💥 Ongelmat ja niiden ratkaisut 

**Merge-konflikti:**  
Muokkasin README.md:tä kahdessa eri haarassa. Ratkaisin konfliktin VS Codessa valitsemalla molemmat rivit (accept both changes) ja tein uuden commitin.  

**Cherry-pick ei mennyt heti läpi:**  
Etsin ensin valitsemani commitin ("Palautettu stashi ja tallennettu muutos”) tunnisteen `git log` -komennolla ja ajoin sen jälkeen komennon `git cherry-pick commit-id`.  
Cherry-pick kuitenkin epäonnistui, koska se yritti poimia commitin, joka muokkasi tiedostoa (`dokumentointi.md`). Tämä tiedosto oli kuitenkin siinä vaiheessa poistettu main-haarassa. Tämä johti *modify/delete*-konfliktiin. Tässä vaiheessa Git avasi myös editorinäkymän, mikä aiheutti hetkellisen hämmennyksen, koska se ei sulkeutunut normaalisti ja terminaalin näkymä jäi jumiin. Jouduin sulkemaan terminaalin ja avaamaan uuden ikkunan. Ratkaisin ongelman lisäkomennolla `git cherry-pick --continue --no-edit`, jolla Git palautti poistettuna olleen tiedoston (dokumentointi.md) takaisin ja lisäsi siihen commitin sisällön.

**Virheellinen commit:**  
Lisäsin tarkoituksella "vahinkotiedoston" ja peruin sen komennolla `git revert`.

**Väliaikaiset tiedostot:**  
Loin .gitignore-tiedoston ja lisäsin siihen `.log` ja `temp/`, jotta tällaiset turhat tiedostot eivät päädy GitHubiin.  

---

### 💡 Mitä opin  

- Lopputyön aikana opin käyttämään Gitin keskeisimpiä toimintoja sekä hahmottamaan, miten versiohallinta helpottaa työn seurantaa ja virheiden korjaamista. 
- Ymmärrän, miten haarat mahdollistavat eri osien kehittämisen rinnakkain ilman, että päähaara rikkoutuu tai vahingoittuu.
- Opin ratkaisemaan merge-konfliktin VS Codessa.
- Ymmärrän mergen ja cherry-pickin eron: merge yhdistää kokonaisia haaroja, kun taas cherry-pickillä voi poimia yksittäisiä committeja eri haaroista.
- Opin tekemään tagin ja viemään sen GitHubiin.
- Opin myös käyttämään rebasingia, joka auttaa pitämään historian selkeänä.
- Opin, että Stash-komento on hyödyllinen, kun haluaa tallentaa keskeneräiset muutokset ilman commitointia ja jatkaa työtä myöhemmin.
- Lisäksi opin, että virheellisiä committeja voi perua git revert -komennolla ja että .gitignore-tiedoston avulla voi rajata pois tarpeettomat tai väliaikaiset tiedostot versionhallinnasta.
- Opin myös tekemään miellyttävän näköisen README-tiedoston (jätin tiedoston alkuun rivit "Tänne tulee tietoa lopputyön vaiheista" "Tämä rivi on MAIN-versiossa" ja "Tämä rivi on TOINEN_HAARA-versiossa" läpinäkyvyyden vuoksi, mutta tiedän että ne voisi siistiä myös pois).
- Kaiken kaikkiaan sain varmuutta komentorivin käyttöön ja rohkeutta kokeilla uutta.  

---

### ✔️ Yhteenveto  

Lopputyö oli opettavainen, sillä sain käsityksen Gitin keskeisistä toiminnoista ja opin hahmottamaan, miten commitit, haarat ja yhdistämiskomennot toimivat. Projektin aikana sain myös varmuutta komentorivin käyttöön ja ongelmatilanteiden ratkaisuun.  

---

### Linkki GitHub-repositorioon
https://github.com/katjajoh/lopputyo

### Kuvia työn vaiheista  

**Merge-konfliktin ratkaisu:**  
![Merge-konflikti](https://github.com/katjajoh/lopputyo/blob/main/merge.png?raw=true)  
![Merge-konflikti 2](https://github.com/katjajoh/lopputyo/blob/main/merge2.png?raw=true)  

**Cherry-pick-komennon testaus:**  
![Cherry-pick 1](https://github.com/katjajoh/lopputyo/blob/main/image-1.png?raw=true)  
![Cherry-pick 2](https://github.com/katjajoh/lopputyo/blob/main/image-2.png?raw=true)  

---

