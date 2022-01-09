{% capture now_unix %}{{'now' | date: '%s'}}{% endcapture %}
## Tulevat tapahtumat

### **25.11.2021**  Vuosikokous

Tervetuloa TKT-alumni ry:n vuosikokoukseen torstaina 25.11.2020 kello 18.00.
Kokouspaikkana toimii Knowit:n toimisto osoitteessa Urho Kekkosen katu 2C, 00100 Helsinki. Kokoukseen voi lisäksi osallistua etänä Zoomissa. Kutsun ja tarkemmat tiedot löydät [täältä](annual_meeting).


### **08.12.2021**  Alumni ALE @ Bruuveri, Kamppi

Tule nauttimaan oluista alumniporukalla Bruuverin kabinettiin! Hallitus kokoustaa klo 17 alkaen. Kokous loppunee 17:30-18:00 välillä, minkä jälkeen iltaa jatketaan oluiden merkeissä vapaamuotoisesti. Olet tervetullut liittymään seuraan joko kokouksen alusta lähtien tai vasta myöhemmin. Yhdistys tarjoaa pientä purtavaa oluiden kaveriksi.

## Tulevat tapahtumat
{% for event in site.events reversed %}
{% capture event_date %}{{event.date | date: '%s'}}{% endcapture %}
{% if event_date >= now_unix %}
### **{{event.date | date: "%d.%m.%Y"}}**  {{ event.title }}
{% endif %}
{% endfor %}
### Hallituksen kokous

Joka kuun toinen keskiviikko klo 17 (arkipyhän sattuessa seuraava). Koronaviruspandemian aikana kokoustamme etänä [Jitsissä](https://meet.jit.si/tkt-alumni-2021).


### TAUOLLA Kuukausittainen Alumni Ale

Alumni Ale of afterwork tapahtuma, joka järjestetään perinteisesti hallituksen kokouksen jälkeen Oluthuone Kaislassa (Vilhonkatu 4, Helsinki).

---

## Menneet tapahtumat

* 16.6.2021: Alumni Ale Online with Smartly: Video editing and rendering solution in JS
* 29.3.2021: Alumni Ale Online with Solita: Koronavilkku internals

## Menneet tapahtumat
{% for event in site.events reversed %}
{% capture event_date %}{{event.date | date: '%s'}}{% endcapture %}
{% if event_date < now_unix %}
### **{{event.date | date: "%d.%m.%Y"}}**  {{ event.title }}
{% endif %}
{% endfor %}