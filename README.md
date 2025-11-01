Tänne tulee tietoa lopputyön vaiheista
Tämä rivi on MAIN-versiossa
Tämä rivi on TOINEN_HAARA-versiossa

# Git-lopputyö: terminaaliversio

### Projektin idea  
Tein git-harjoittelurepon, jossa testasin erilaisia komentoja ja versionhallintaa.

---

### Käytetyt Git-komennot  
git clone git@github.com:katjajoh/lopputyo.git  
git add, git commit  
git branch, git checkout  
git merge (toinen_haara → main)  
git stash ja git stash pop  
git revert (virheellisesti lisätty tiedosto)  
git cherry-pick (kolmas_haara -branchista yksi commit mainiin)  
git tag v1.0.0 ja git push origin v1.0.0  
git rebase main (päivitettiin toisen_haaran)  
git push, git pull  
.gitignore-tiedoston lisäys  

---

### Ongelmat ja niiden ratkaisut  

**Merge-konflikti:**  
Muokkasin README.md:tä kahdessa eri haarassa. Ratkaisin konfliktin VS Codessa valitsemalla molemmat rivit (accept both changes) ja tein uuden commitin.  

**Cherry-pick ei mennyt läpi heti:**  
Etsin ensin haluamani commitin ("Palautettu stashi ja tallennettu muutos”) tunnisteen git log -komennolla ja ajoin sen jälkeen komennon git cherry-pick commit-id.
Tässä vaiheessa Git avasi editorin ja pyysi viimeistelemään commitin, mikä aiheutti hetkellisen hämmennyksen, koska editori ei sulkeutunut normaalisti ja terminaalin näkymä jäi jumiin.
Suljin terminaalin ja avasin uuden. Lopulta ratkaisin tilanteen suorittamalla komennon uudelleen lisäoptiolla --no-edit, jolloin Git hyväksyi komennon ilman erillistä editoria ja commit siirtyi onnistuneesti mainiin ilman, että muut saman haaran muutokset tulivat mukana.

**Virheellinen commit:**  
Lisäsin tarkoituksella tiedoston “vahingossa” ja peruin sen komennolla git revert.  

**Väliaikaiset tiedostot:**  
Loin .gitignore-tiedoston ja lisäsin siihen `.log` ja `temp/`, jotta ne eivät mene GitHubiin.  

---

### Mitä opin  

- Lopputyön aikana opin käyttämään Gitin keskeisimpiä toimintoja sekä hahmottamaan, miten versiohallinta helpottaa työn seurantaa ja virheiden korjaamista. 
- Ymmärrän, miten haarat mahdollistavat eri osien kehittämisen rinnakkain ilman, että päähaara rikkoutuu tai vahingoittuu.
- Opin ratkaisemaan merge-konfliktin VS Codessa.
- Ymmärrän mergen ja cherry-pickin eron: merge yhdistää kokonaisia haaroja, kun taas cherry-pickillä voi poimia yksittäisiä committeja eri haaroista.
- Opin tekemään tagin ja viemään sen GitHubiin.
- Opin myös käyttämään rebasingia, joka auttaa pitämään historian selkeänä.
- Opin,että Stash-komento on hyödyllinen, kun haluaa tallentaa keskeneräiset muutokset ilman commitointia ja jatkaa työtä myöhemmin.
- Lisäksi opin, että virheellisiä committeja voi perua git revert -komennolla ja että .gitignore-tiedoston avulla voi rajata pois tarpeettomat tai väliaikaiset tiedostot versionhallinnasta.
- Kaiken kaikkiaan sain varmuutta komentorivin käyttöön ja rohkeutta kokeilla uutta.  

---

### Yhteenveto  

Lopputyö oli opettavainen, sillä sain käsityksen Gitin keskeisistä toiminnoista ja opin hahmottamaan, miten commitit, haarat ja yhdistämiskomennot toimivat.  
Projektin aikana sain myös varmuutta komentorivin käyttöön ja ongelmatilanteiden ratkaisuun.  

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

