# typeform-hidden-fields
Typeform stelt je in staat om snel enquetes te publiceren op je website. Nadat een enquete is aangemaakt, wordt er een unieke typeform url gegenereerd
die ge-embed kan worden.
Aan die url kunnen vrij te kiezen 'hidden fields' worden toegevoegd. Dit zijn parameters die als doel hebben extra data op te vragen van een gebruiker.

`https://www.typeform.com/to/typeform_ID?useragent=xxxxx&screen=xxxxx`

useragent en screen zijn 2 'hidden fields', waarvan de key zelf gekozen wordt, maar de value moet geprogrammeerd worden.

Dit javascript probeert de value voor 6 keys te achterhalen:
* useragent: Omgeving waarin enquete wordt ingevuld: browser of webview geintegreerd in app
* product: enquete ingevuld via m-site of www-site. Enkel relevant bij 2 aparte producten
* screen: Schermgrootte waarmee enquete is ingevuld
* urlsource: Detecteert vanwaar gebruiker kwam
* pageviews: Telt aantal pageviews tot gebruiker enquete verlaat
* timeonsite: Geeft tijd weer die gebruiker in huidige sessie op de site heeft gespendeerd.

# Hoe werkt het?
## typeform.html
1. Vul de typeform url zonder parameter in bij de variabele tf_URL
2. Geef met een boolean aan welke hidden fields worden gebruikt voor de betreffende bevraging
3. Embed de html file in je site.
## typeform_site_integration.html
Voor urlsource, pageviews en timeonsite moet het scriptje typeform_site_integration.html op iedere pagina van je website geïntegreerd worden.
