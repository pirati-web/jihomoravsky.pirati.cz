---
layout: post
category: CLANKY
title: Návod k administraci pirátského webu
date: 2017-11-07T08:00:00.514Z
author: Jaroslav Kupčík
permalink: /web-manual/
excerpt: >-
  Pokud je vám blízká otevřenosti a spolupráce, zajímá vás politika nebo státní správa a chcete zlepšit fungování státu, staňte se součástí Pirátského týmu.

---

Vítejte v návodu pro administraci krajského webu jihomoravského sdružení Pirátské strany

* náš projekt na [Githubu](https://github.com/): [https://github.com/pirati-web/jihomoravsky.pirati.cz](https://github.com/pirati-web/jihomoravsky.pirati.cz)
* adresa webu: [https://jihomoravsky.pirati.cz](https://jihomoravsky.pirati.cz) (master branch na GitHubu)
* náhled webu: [https://pirati-web.github.io/jihomoravsky.pirati.cz](https://pirati-web.github.io/jihomoravsky.pirati.cz/) (gh-pages branch)
* zkratka pro náhled webu: [bit.ly/piratijmk](http://bit.ly/piratijmk)
* adresa pro administraci přes CMS:  [https://pirati-web.github.io/jihomoravsky.pirati.cz/admin](https://pirati-web.github.io/jihomoravsky.pirati.cz/admin)

* články se nacházejí v adresáři `_posts`
* profily lidí se nachází v `_people`
* samostatné stránky v `_landing`
* obrázky se nacházejí v `/assets/img/...`
  * obrázky profilů v `/assets/img/people/`
  * obrázky ke článkům v `/assets/img/posts/` atp.

# Postup pro editaci v Githubu

1. Je třeba vytvořit si svůj účet v GitHubu a zažádat si o práva k zápisu
2. Přihlásit se a přejít na [https://github.com/pirati-web/jihomoravsky.pirati.cz](https://github.com/pirati-web/jihomoravsky.pirati.cz)
3. Výběr branche - defaultně je zvolena `gh-pages` - [screenshot]({{ "/assets/img/articles/admin/01-vyber-branche.png" | relative_url }}){:target="_blank"}
4. proveďte vaše změny
  * nalezení a úprava požadovaného souboru - [screenshoty]({{ "/assets/img/articles/admin/02-vyber-souboru.png" | relative_url }}){:target="_blank"}
  * nebo vytvoření nového souboru v příslušném adresáři - [screenshot]({{ "/assets/img/articles/admin/03-create-file.png" | relative_url }}){:target="_blank"}
  * nebo nahrání souboru (např. obrázku) z disku [screenshoty]({{ "/assets/img/articles/admin/04-upload.png" | relative_url }}){:target="_blank"}
5. dole popište vaše změny a potvrďte `Commit changes` - [screenshot]({{ "/assets/img/articles/admin/05-commit.png" | relative_url }}){:target="_blank"}
6. Počkejte cca 20 sekund, než GitHub zkompiluje vaše změny do statického HTML
7. Ověřte na [bit.ly/piratijmk](http://bit.ly/piratijmk){:target="_blank"}, jak se vaše změny v branchi `gh-pages` odrazily na podobě webu, v případě chyb je opravte
8. Pokud je upravený web v `gh-pages` branchi v pořádku, přepněte se do `master` branche a proveďte `merge` `gh-pages` do `mastera` - [screenshot]({{ "/assets/img/articles/admin/06-merge.png" | relative_url }}){:target="_blank"}

# Struktura článků

* Snažte se využívat kopírování a úpravy existujících stránek
* článek v sekci _posts *musí* obsahovat hlavičku:

        ---
        layout: blog
        category: CLANKY
        title: "Titulek v uvozovkách"
        date: 2017-05-26T01:00:00.000Z # datum MUSÍ být ve formátu YYYY-MM-DDT01:00:00.000Z
        author: Markéta Gregorová # jméno, které se zobrazí pod titulkem
        authorId: marketa.gregorova # ID osoby s profilem ve formátu jmeno.prijmeni (tento řádek je nepovinný)
        image: /assets/img/posts/market-u-vodotrysku-g.jpg # odkaz na obrázek ideálně s výškou 420px
        description: >-
          Autorský zákon nejen nepomáhá, ale šikanuje i všechny ostatní. Kolektivní
          správci smí vybírat poplatky a udělovat licence i jménem autorů, které
          nezastupují. Pro každou zastupovanou skupinu může existovat jen jeden správce,
          tedy je uzákoněn monopol.
        tags: kopírovací-zákon autorský-zákon kopírovací-monopol OSA Intergram # tagy jsou oddělěny mezerou
        ---

# Tipy pro pokročilé:

* Samostatné stránky se nacházejí v adresáři `landing`. Obsahují parametr `permalink` obsahující jejich přímou adresu
* Články lze upravovat rovněž přes [administrační rozhraní](https://pirati-web.github.io/jihomoravsky.pirati.cz/admin){:target="_blank"} (po přihlášení vašim GitHub účtem) vyvinuté Václavem Klecandou. Může to být pohodlnější přes to, že v něm nefunguje zobrazování obrázků a náhled WYSIWYG editoru je nepřesný.
* V těle článků lze kromě Markdownu (viz níže) využívat i rovnou HTML.
* Celý web je zkopírován z webu celostátního, jehož administrace stylů je dost šílená. Všechny úpravy stylu pro krajský web se nachází v souborech `/_sass/jmk-custom.scss` a `/_sass/jmk-custom-landing.scss`
* Úpravy webu lze navrhovat i bez příslušných práv vytvořením pull requestu - [screenshot]({{ "/assets/img/articles/admin/07-pull-request.png" | relative_url }}){:target="_blank"}

# Kramdown syntax

* Těla *.md souborů používají specifickou verzi Markdownu zvanou Kramdown.
* Oficiální dokumentace: [https://daringfireball.net/projects/markdown/syntax](https://daringfireball.net/projects/markdown/syntax){:target="_blank"}
* Pískoviště pro experimenty: [http://markdownlivepreview.com/](http://markdownlivepreview.com/){:target="_blank"}

Níže následuje nekompletní seznam prvků, které je možné v těle článků využít a jejich zápis v Markdownu.

# Hlavní nadpis

    # Hlavní nadpis

---

## Nadpis druhé úrovně

    ## Nadpis druhé úrovně

---

### Nadpis třetí úrovně

    ### Nadpis třetí úrovně

---

[Odkaz na www.pirati.cz](http://www.pirati.cz)

     [Odkaz na www.pirati.cz](http://www.pirati.cz)

---

[Odkaz na www.pirati.cz v novém okně](http://www.pirati.cz){:target="_blank"}

    [Odkaz na www.pirati.cz v novém okně](http://www.pirati.cz){:target="_blank"}

---

Odstavec s **tučným textem** a *kurzívou*.

Další odstavec.


    Odstavec s *tučným textem* a _kurzívou_.

    Další odstavec.

---

![Obrázek s kočičkou](http://lorempixel.com/660/200/cats/)

    ![Obrázek s kočičkou](http://lorempixel.com/660/200/cats/)

---

* Položka nečíslovaného seznamu
* Druhá položka nečíslovaného seznamu

  Další odstavec druhé položky
* Třetí položka nečíslovaného seznamu


        * Položka nečíslovaného seznamu
        * Druhá položka nečíslovaného seznam  

          Další odstavec druhé položky
        * Třetí položka nečíslovaného seznamu

---

1. Položka nečíslovaného seznamu
2. Druhá položka nečíslovaného seznamu

   Další odstavec druhé položky
3. Třetí položka nečíslovaného seznamu


        1. Položka nečíslovaného seznamu
        2. Druhá položka nečíslovaného seznamu

           Další odstavec druhé položky
        3. Třetí položka nečíslovaného seznamu

---

> Citace. Haxx0r ipsum dereference tunnel in printf for overflow over clock ip default afk access L0phtCrack *.* continue grep false mountain dew data hello world. It's a feature ssh spoof case Trojan horse warez try catch. Stack trace eaten by a grue big-endian d00dz private strlen.

    > Citace. Haxx0r ipsum dereference tunnel in printf for overflow over
    clock ip default afk access L0phtCrack *.* continue grep false mountain
    dew data hello world. It's a feature ssh spoof case Trojan horse warez
    try catch. Stack trace eaten by a grue big-endian d00dz private strlen.

---

| Tabulka (nefunguje v preview) | druhý sloupec | třetí sloupec |
| výdaje státu (včetně důchodců 0,52) | 1,25 | nějaké číslo |
| zisky (z toho 0,4 do zahraničí) | 0,9 | jiné číslo |
| přebytek obch. bilance | 0,4 | ještě |
| kapitalizace a nákl. financování | 1,2 | další |
| HDP | 4,75 | číslo |

    | Tabulka | druhý sloupec | třetí sloupec |
    | výdaje státu (včetně důchodců 0,52) | 1,25 | nějaké číslo |
    | zisky (z toho 0,4 do zahraničí) | 0,9 | jiné číslo |
    | přebytek obch. bilance | 0,4 | ještě |
    | kapitalizace a nákl. financování | 1,2 | další |
    | HDP | 4,75 | číslo |
