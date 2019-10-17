---
layout: contacts
# contentSize: big
contentSize: even
residences:
 - name: Pirátská strana | MORAVSKOSLEZSKÝ KRAJ
   url:
   address: |
     Ostravské pirátské centrum (OPiCe)
     Denisova 639/2
     702 00 Moravská Ostrava a Přívoz 
   spravce: jakub.dedek
   residenceImg: miscellaneous/residence.png
   mapLink: "https://goo.gl/maps/dakQGzwQKng8ER9o7"
 - name: Regionální poslanecká kancelář
   url: 
   address: |
     Denisova 639/2 (3. patro)
     702 00 Moravská Ostrava a Přívoz 
     
     <strong>Kancelář je pro Vás otevřena:</strong>
     Každé pondělí 10:00 - 12:00 <b>Lukáš Černohorský</b>
     a 12:00 - 14:00 <b>Ondřej Polanský</b>.

     Kdykoliv mimo tuto dobu je Vám k dispozici asistentka, s níž si můžete dohodnout schůzku v jiném termínu.
   spravce: zuzana.klusova
   residenceImg:
   mapLink: "https://goo.gl/maps/dakQGzwQKng8ER9o7"
contactPersons:
 - id: jakub.dedek
   position: Kontakt pro dobrovolníky
 - id: zuzana.klusova
   position: Kontakt pro novináře
---

<div class="o-section-header o-section-header--indented">
  <h1 class="t-h2-alt">Přidejte se</h1>
</div>

Zajímá vás co piráti dělají? [Naloďte se](https://nalodeni.pirati.cz/) a buďte v obraze, nebo kontaktujte našeho koordinátora (viz kontakt pro dobrovolníky).

Finanční dary můžete posílat na [zde](https://dary.pirati.cz).
Pokud chcete darovat přimo našemu kraji, poraďte se prosím s koordinátorem.

<div class="o-section-header o-section-header--indented">
  <h1 class="t-h2-alt">Poslanci</h1>
</div>

{% assign person = site.people | where_exp: "item","item.uid contains 'lukas.cernohorsky'" | first  %}
{% include people/profile-badge.html item=person imgSize='big' imgStyle='round' class='c-profile-badge--centered' %}
<br>
{% assign person = site.people | where_exp: "item","item.uid contains 'ondrej.polansky'" | first  %}
{% include people/profile-badge.html item=person imgSize='big' imgStyle='round' class='c-profile-badge--centered' %}

