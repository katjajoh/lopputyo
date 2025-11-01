Tänne tulee tietoa lopputyön vaiheista
Tämä rivi on MAIN-versiossa
Tämä rivi on TOINEN_HAARA-versiossa

Git-lopputyö: terminaaliversio

Projektin idea:
Tein git-harjoittelurepon, jossa testasin erilaisia komentoja ja versionhallintaa.

Käytetyt komennot:
git clone git@github.com:katjajoh/lopputyo.git
git add, git commit
git branch, git checkout
git merge (toinen_haara → main)
git stash ja git stash pop
git revert (virheellisesti lisätty tiedosto)
git cherry-pick (kolmas_haara -branchista yksi commit mainiin)
git tag v1.0.0 ja git push origin v1.0.0
git rebase main (päivitin toisen_haaran)
git push, git pull
.gitignore-tiedoston lisäys

Ongelmat ja niiden ratkaisut
- Merge-konflikti: Muokkasin README.md:tä kahdessa eri haarassa. Ratkaisin konfliktin VS Codessa valitsemalla molemmat rivit (accept both changes) ja tein uuden commitin.
- Cherry-pick ei mennyt läpi heti: Etsin ensin valitsemani commitin ("Palautettu stashi ja tallennettu muutos") tunnisteen git log -komennolla ja ajoin sen jälkeen komennon git cherry-pick commit-id. Tässä kohtaa tuli vastaan ongelma, sillä ilmeisesti olin tehnyt samassa tiedostossa muutoksia myös main-haarassa, joten cherry-pick ei mennytkään läpi yhdellä komennolla, vaan Git avasi editorin ja pyysi viimeistelemään commitin. Editori aiheutti minulle hetken hämmennystä, koska se ei sulkeutunut normaalisti ja näkymä jäi jumiin. Jouduin sulkemaan terminaalin ja avaamaan uuden. Tässä vaiheessa etsin myös tietoa verkosta ja toistin komennon käyttäen lisäkomentoa --no-edit. Näin Git lopulta hyväksyi komennon eikä avannut editoria. Sain poimittua haluamani commitin, ja se siirtyi mainiin ilman että muut saman haaran muutokset tulivat mukana.
- Virheellinen commit: Lisäsin tarkoituksella tiedoston "vahingossa" ja peruin sen komennolla git revert.
- Väliaikaiset tiedostot: Loin .gitignore-tiedoston ja lisäsin siihen .log ja temp/, jotta ne eivät mene GitHubiin.

Mitä opin
- Ymmärrän nyt paremmin, miten haarat, merge ja cherry-pick eroavat toisistaan.
- Opin, että git stash ja git stash pop on kätevä tapa keskeyttää työ ja jatkaa siitä myöhemmin.
- Opin ratkaisemaan merge-konfliktin VS Codessa.
- Opin tekemään tagin ja viemään sen GitHubiin.
- Sain varmuutta komentorivin käyttöön.

Yhteenveto:
Lopputyö oli opettavainen, sillä sain käsityksen Gitin keskeisistä toiminnoista ja opin hahmottamaan, miten commitit, haarat ja yhdistämiskomennot toimivat. Projektin aikana sain myös varmuutta komentorivin käyttöön ja ongelmatilanteiden ratkaisuun.

Linkki GitHub-repositorioon
https://github.com/katjajoh/lopputyo

Kuvia työn merge- ja cherry-pick-vaiheista:

![Merge-konflikti 1](https://github.com/katjajoh/lopputyo/raw/main/merge.png)
![Merge-konflikti 2](https://github.com/katjajoh/lopputyo/raw/main/merge2.png)
![Cherry pick 1](https://github.com/katjajoh/lopputyo/raw/main/image-1.png)
![Cherry pick 2](https://github.com/katjajoh/lopputyo/raw/main/image-2.png)



