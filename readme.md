# jihomoravsky.pirati.cz

Naklonovaný web pirati.cz, z kterého vychází web JmK. Níže následuje obsah copypastovaný z centrální verze.
## Lokální spuštění

Instalacee na Fedora 25: `dnf install rubygem-jekyll`

Instalace ubuntu 16.04:

```
sudo apt-get install ruby-dev gcc make libghc-zlib-dev
gem install rubygems-update
gem install jekyll bundler
bundle
```

Repozitář můžeme naklonovat do jakékoliv složky (nemusí být ve `/var/www/`).

`jekyll serve`, což stránku zkompiluje, spustí a ještě je stránka přístupná skrz localhost: `http://127.0.0.1:4000`

Popřípadě můžeme spustit jen: `jekyll build`, což do složky `_site` připraví kompletní web (ten můžeme otevřít z prohlíže pomocí klavesové zkratky `ctrl+o`).

## Struktura

Samotné stránky jsou v markdownu nebo v html (složitější struktura, např. vícesloupců apod)

Kolekce jsou markdown soubory s yaml frontend v přísliušné složce, na webu jsou použity 4:

- posts (články)
- people (lidé)
- program
- teams (týmy)

Některé údaje jsou uvedeny v složce `_data`. Jsou zde ve formátu yaml nebo json.

**CSS** je ve složce `_sass` a je automaticky kompilováno a minifikován do jednoho souboru `main.css`.

**JavaScript** je ve složce `_include/js`. Knihovny jsou linkovány skrze CDN v minifikované podobě. Další JS je v spojen do jednoho scriptu bez minifikace (zatím).

Jekyll má velmi podrobnou [dokumentaci](http://jekyllrb.com/docs/home/). A při vývoji též doporučuji [cheat sheet](http://jekyll.tips/jekyll-cheat-sheet/)
