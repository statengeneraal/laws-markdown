<meta http-equiv='Content-Type' content='text/html; charset=utf-8' />

##Regeling van 10 februari 1995, houdende Ministeriële regeling standaarduitwisselingsformaat in het kader van de Wet waardering onroerende zaken

De Staatssecretaris van Financiën,  
Gelet op [artikel 9 van het Uitvoeringsbesluit kostenverrekening en gegevensuitwisseling Wet waardering onroerende zaken](../../../../AMvB/uitvoeringsbesluit/kostenverrekening/en/gegevensuitwisseling/wet/etc/BWBR0007230/README.md);
Besluit:    

### Artikel  1  

Het in de bijlage van deze regeling geformuleerde uitwisselingsformaat vormt het standaarduitwisselingsformaat bedoeld in [artikel 9 van het Uitvoeringsbesluit kostenverrekening en gegevensuitwisseling Wet waardering onroerende zaken](../../../../AMvB/uitvoeringsbesluit/kostenverrekening/en/gegevensuitwisseling/wet/etc/BWBR0007230/README.md).  

### Artikel  2  

Het college van burgemeester en wethouders of de in [artikel 1, tweede lid, van de Wet waardering onroerende zaken ](../../../../wet/wet/waardering/onroerende/zaken/BWBR0007119/README.md)bedoelde gemeenteambtenaar levert de gegevens volgens het uitwisselingsformaat, bedoeld in artikel 1, aan afnemers door het op elektronische wijze toezenden, mits de desbetreffende afnemer zich met de gebruikte infrastructuur akkoord heeft verklaard, met dien verstande dat de levering van gegevens over feiten of omstandigheden die geen inhoudelijke wijziging betekenen van de genomen beschikking op papier kan plaatsvinden. 

### Artikel  3  

Deze regeling treedt in werking met ingang van de tweede dag na de dagtekening van de Staatscourant waarin zij wordt geplaatst en werkt terug tot en met 1 januari 1995.  

### Artikel  4  

Deze regeling wordt aangehaald als: Regeling Stuf-WOZ. 

De 
Staatssecretaris van Financiën, 
W.A. Vermeend     

### Bijlage  

####als bedoeld in artikel 1  van de Regeling Stuf-WOZ

1. Voorlooprecord

| --- | --- | --- | --- | --- |
|:---|:---|:---|:---|:---|
| positie  | lengte  | type  | nummer  | naam gegeven  |
| 1 - 2  | 2  | N  | 93.10  | Recordidentificatiecode (= 00)  |
| 3 - 6  | 4  | N  | 09.10  | Gemeentecode  |
| 7 - 46  | 40  | A  | 09.11  | Gemeentenaam  |
| 47 - 86  | 40  | A  | 91.10  | Contactpersoon  |
| 87 - 106  | 20  | A  | 91.20  | Telefoonnummer contactpersoon  |
| 107 - 110  | 4  | N  | 71.10  | Code afnemer  |
| 111 - 118  | 8  | D  | 92.10  | Aanmaakdatum  |
| 119 - 120  | 2  | N  | 92.20  | Bijgewerkt tot en met maand  |
| 121 - 128  | 8  | D  | 92.30  | Datum vorige aanlevering  |
| 129 - 129  | 1  | A  | 93.30  | Aard leveringsbestand  |
| 130 - 149  | 20  | A  | 91.30  | Softwareleverancier  |
| 150 - 151  | 2  | N  | 91.40  | Versie Stuf-WOZ  |
| 152 - 256  | 105  | A  | --- | Filler  |

2. Indien records met WOZ-objecten worden geleverd volgt hierna (anders vervolg bij 3):

| --- | --- | --- | --- | --- |
|:---|:---|:---|:---|:---|
|Stuurrecord | --- | --- | --- | --- |
| positie  | lengte  | type  | nummer  | naam gegeven  |
| 1 - 2  | 2  | N  | 93.10  | Recordidentificatiecode (= 10)  |
| 3 - 4  | 2  | N  | 93.20  | Deelbestandsidentificatie (= 20)  |
| 5 - 256  | 252  | A  | --- | Filler  |

| --- | --- | --- | --- | --- |
|:---|:---|:---|:---|:---|
|Gegevensrecords | --- | --- | --- | --- |
| positie  | lengte  | type  | nummer  | naam gegeven  |
| 1 - 2  | 2  | N  | 93.10  | Recordidentificatiecode  |
| 3 - 14  | 12  | N  | 01.01  | Uniek WOZ-objectnummer  |
| 15 - 54  | 40  | A  | 10.20  | Woonplaatsnaam  |
| 55 - 78  | 24  | A  | 11.10  | Straatnaam  |
| 79 - 83  | 5  | N  | 11.20  | Huisnummer  |
| 84 - 84  | 1  | A  | 11.30  | Huisletter  |
| 85 - 88  | 4  | A  | 11.40  | Huisnummertoevoeging  |
| 89 - 90  | 2  | A  | 11.50  | Aanduiding bij huisnummer  |
| 91 - 96  | 6  | A  | 11.60  | Postcode  |
| 97 - 136  | 40  | A  | 11.70  | Lokatieomschrijving  |
| 137 - 144  | 8  | N  | 12.10  | Grondoppervlakte  |
| 145 - 146  | 2  | N  | 12.20  | Gebruikscode  |
| 147 - 147  | 1  | A  | 14.10  | Code gebouwd/ongebouwd  |
| 148 - 155  | 8  | N  | 14.20  | Meegetaxeerde oppervlakte  |
| --- | --- | --- | --- | gebouwd  |
| 156 - 166  | 11  | N  | 14.30  | Aandeel waarde gebouwd  |
| 167 - 177  | 11  | N  | 15.10  | Vastgestelde waarde  |
| 178 - 185  | 8  | D  | 15.20  | Waardepeildatum  |
| 186 - 188  | 3  | N  | 15.30  | Bijzondere-waarderingscode  |
| 189 - 189  | 1  | A  | 81.10  | Mutatiecode  |
| 190 - 197  | 8  | D  | 81.20  | Ingangsdatum  |
| 198 - 205  | 8  | D  | 81.30  | Einddatum  |
| 206 - 210  | 5  | A  | --- | Filler  |
| 211 - 213  | 3  | A  | 15.40  | Aanduiding valutasoort  |
| 214 - 215  | 2  | N  | 15.50  | Code blokkeren  |
| 216 - 256  | 41  | A  | --- | Filler  |

| --- | --- | --- | --- | --- |
|:---|:---|:---|:---|:---|
|Telrecord |
| positie  | lengte  | type  | nummer  | naam gegeven  |
| 1 - 2  | 2  | N  | 93.10  | Recordidentificatiecode (= 90)  |
| 3 - 11  | 9  | N  | --- | Totaal aantal gegevensrecords  |
| --- | --- | --- | --- | deelbestand  |
| 12 - 21  | 10  | N  | --- | Totaaltelling 12.10  |
| 22 - 31  | 10  | N  | --- | Totaaltelling 14.20  |
| 32 - 44  | 13  | N  | --- | Totaaltelling 14.30  |
| 45 - 57  | 13  | N  | --- | Totaaltelling 15.10  |
| 58 - 256  | 199  | A  | --- | Filler  |

3. Indien records met subjecten worden geleverd volgt hierna (anders vervolg bij 4):

| --- | --- | --- | --- | --- |
|:---|:---|:---|:---|:---|
|Stuurrecord | --- | --- | --- | --- |
| positie  | lengte  | type  | nummer  | naam gegeven  |
| 1 - 2  | 2  | N  | 93.10  | Recordidentificatiecode (= 10)  |
| 3 - 4  | 2  | N  | 93.20  | Deelbestandsidentificatie (= 30)  |
| 5 - 256  | 252  | A  | --- | Filler  |

| --- | --- | --- | --- | --- |
|:---|:---|:---|:---|:---|
|Gegevensrecords |
| positie  | lengte  | type  | nummer  | naam gegeven  |
| 1 - 2  | 2  | N  | 93.10  | Recordidentificatiecode (= 30)  |
| 3 - 12  | 10  | N  | 01.10  | A-nummer natuurlijk persoon  |
| 13 - 21  | 9  | N  | 01.20  | BSN of een door een kamer toegekend uniek nummer als bedoeld in de [Handelsregisterwet 2007](../../../../wet/handelsregisterwet/2007/BWBR0021777/README.md)  |
| 22 - 31  | 10  | A  | 02.11  | Voorletters  |
| 32 - 41  | 10  | A  | 02.30  | Voorvoegsels  |
| 42 - 176  | 135  | A  | 02.40  | Geslachtsnaam/statutaire naam  |
| 177 - 231  | 55  | A | 02.41  | Partnernaam/bedrijfsnaam verkort  |
| 232 - 241  | 10  | A | 02.31  | Voorvoegsels behorend bij partnernaam  |
| 242 - 251  | 10  | N | 01.21  | aanvulling subjectnummer  |
| 252 - 252  | 1  | A | 04.05  | Aanduiding naamgebruik  |
| 253 - 256  | 4  | A | --- | Filler  |

| --- | --- | --- | --- | --- |
|:---|:---|:---|:---|:---|
|Gegevensrecords (vervolg) |
| positie  | lengte  | type  | nummer  | naam gegeven  |
| 1 - 2  | 2  | N  | 93.10  | Recordidentificatiecode (= 31)  |
| 3 - 11  | 9  | N  | 01.20  | BSN of een door een kamer toegekend uniek nummer als bedoeld in de [Handelsregisterwet 2007](../../../../wet/handelsregisterwet/2007/BWBR0021777/README.md) |
| dec-35  | 24  | A  | 11.10  | Straatnaam  |
| 36 - 40  | 5  | N  | 11.20  | Huisnummer  |
| 41 - 41  | 1  | A  | 11.30  | Huisletter  |
| 42 - 45  | 4  | A  | 11.40  | Huisnummertoevoeging  |
| 46 - 47  | 2  | A  | 11.50  | Aanduiding bij huisnummer  |
| 48 - 53  | 6  | A  | 11.60  | Postcode  |
| 54 - 93  | 40  | A  | 10.20  | Woonplaatsnaam  |
| 94 - 133  | 40  | A  | 13.10  | Landnaam  |
| 134 - 134  | 1  | A  | 81.10  | Mutatiecode  |
| 135 - 142  | 8  | D  | 81.20  | Ingangsdatum  |
| 143 - 150  | 8  | D  | 81.30  | Einddatum  |
| 151 - 190  | 40  | A  | 11.70  | Lokatieomschrijving  |
| 191 - 200  | 10  | N  | 01.21  | aanvulling subjectnummer  |
| 201 - 208  | 8  | N  | 01.30  | Handelsregisternummer  |
| 209 - 226  | 18  | A  | --- | Filler  |
| 227 - 234  | 8  | D  | 03.10  | Geboortedatum natuurlijk persoon  |
| 235 - 242  | 8  | D  | 08.10  | Datum overlijden natuurlijk persoon  |
| 243 - 243  | 1  | A  | 08.11  | Status subject  |
| 244 - 248  | 5  | A  | --- | Filler  |
| 249 - 249  | 1  | A  | 10.10  | Functie adres  |
| 250 - 256  | 7  | A  | --- | Filler  |

| --- | --- | --- | --- | --- |
|:---|:---|:---|:---|:---|
|Telrecord |
| positie  | lengte  | type  | nummer  | naam gegeven  |
| 1 - 2  | 2  | N  | 93.10  | Recordidentificatiecode (= 90)  |
| 3 - 11  | 9  | N  | --- | Totaal aantal gegevensrecords  |
| --- | --- | --- | --- | deelbestand  |
| 12 20  | 9  | N  | --- | Totaal aantal gegevensrecords  |
| --- | --- | --- | --- | recordidentificatiecode = 30  |
| 21 - 29  | 9  | N  | --- | Totaal aantal gegevensrecords  |
| --- | --- | --- | --- | recordidentificatiecode = 31  |
| 30 - 256  | 227  | A  | --- | Filler  |

4. Indien records met kadastrale identificaties WOZ-objecten worden geleverd volgt hierna (anders vervolg bij 5):

| --- | --- | --- | --- | --- |
|:---|:---|:---|:---|:---|
|Stuurrecord |
| positie  | lengte  | type  | nummer  | naam gegeven  |
| 1 - 2  | 2  | N  | 93.10  | Recordidentificatiecode (= 10)  |
| 3 - 4  | 2  | N  | 93.20  | Deelbestandsidentificatie (= 40)  |
| 5 - 256  | 252  | A  | --- | Filler  |

| --- | --- | --- | --- | --- |
|:---|:---|:---|:---|:---|
|Gegevensrecord |
| positie  | lengte  | type  | nummer  | naam gegeven  |
| 1 - 2  | 2  | N  | 93.10  | Recordidentificatiecode (= 40)  |
| 3 - 14  | 12  | N  | 01.01  | Uniek WOZ-objectnummer  |
| 15 - 19  | 5  | A  | 51.10  | Kadastrale gemeentecode  |
| 20 - 21  | 2  | A  | 51.20  | Sectie  |
| 22 - 26  | 5  | N  | 51.30  | Perceelnummer  |
| 27 - 27  | 1  | A  | 51.40  | Perceel-index-letter  |
| 28 - 31  | 4  | N  | 51.50  | Perceel-index-nummer  |
| 32 - 39  | 8  | N  | 52.10  | Toegekende oppervlakte  |
| 40 - 47  | 8  | N  | 52.20  | Meegetaxeerde oppervlakte  |
| --- | --- | --- | --- | gebouwd per kadastraal object  |
| 48 - 48  | 1  | A  | 81.10  | Mutatiecode  |
| 49 - 56  | 8  | D  | 81.20  | Ingangsdatum  |
| 57 - 64  | 8  | D  | 81.30  | Einddatum  |
| 65 - 256  | 192  | A  | --- | Filler  |

| --- | --- | --- | --- | --- |
|:---|:---|:---|:---|:---|
|Telrecord |
| positie  | lengte  | type  | nummer  | naam gegeven  |
| 1 - 2  | 2  | N  | 93.10  | Recordidentificatiecode (= 90)  |
| 3 - 11  | 9  | N  | --- | Totaal aantal gegevensrecords  |
| --- | --- | --- | --- | deelbestand  |
| 12 24  | 13  | N  | --- | Totaaltelling 52.10  |
| 25 - 37  | 13  | N  | --- | Totaaltelling 52.20  |
| 38 - 256  | 219  | A  | --- | Filler  |

5. Indien records met identificaties eigenaar/gebruiker worden geleverd volgt hierna (anders vervolg bij 6):

| --- | --- | --- | --- | --- |
|:---|:---|:---|:---|:---|
|Stuurrecord |
| positie  | lengte  | type  | nummer  | naam gegeven  |
| 1 - 2  | 2  | N  | 93.10  | Recordidentificatiecode (= 10)  |
| 3 - 4  | 2  | N  | 93.20  | Deelbestandsidentificatie (= 60)  |
| 5 - 256  | 252  | A  | --- | Filler  |

| --- | --- | --- | --- | --- |
|:---|:---|:---|:---|:---|
|Gegevensrecord |
| positie  | lengte  | type  | nummer  | naam gegeven  |
| 1 - 2  | 2  | N  | 93.10  | Recordidentificatiecode (= 60)  |
| 3 - 14  | 12  | N  | 01.01  | Uniek WOZ-objectnummer  |
| 15 - 24  | 10  | N  | 01.10  | A-nummer natuurlijk persoon  |
| 25 - 33  | 9  | N  | 01.20  | BSN of een door een kamer toegekend uniek nummer als bedoeld in de [Handelsregisterwet 2007](../../../../wet/handelsregisterwet/2007/BWBR0021777/README.md)  |
| 34 - 34  | 1  | A  | 41.10  | Aanduiding eigenaar/gebruiker  |
| 35 - 40  | 6  | A  | 41.20  | Zakelijk-rechtcode  |
| 41 - 42  | 2  | A  | 41.30  | s.-code  |
| 43 - 43  | 1  | A  | 81.10  | Mutatiecode  |
| 44 - 51  | 8  | D  | 81.20  | Ingangsdatum  |
| 52 - 59  | 8  | D  | 81.30  | Einddatum  |
| 60 - 69  | 10  | N  | 01.21  | aanvulling subjectnummer  |
| 70 - 256  | 187  | A  | --- | Filler  |

| --- | --- | --- | --- | --- |
|:---|:---|:---|:---|:---|
|Telrecord |
| positie  | lengte  | type  | nummer  | naam gegeven  |
| 1 - 2  | 2  | N  | 93.10  | Recordidentificatiecode (= 90)  |
| 3 - 11  | 9  | N  | --- | Totaal aantal gegevensrecords  |
| --- | --- | --- | --- | deelbestand  |
| 12 - 256  | 245  | A  | --- | Filler  |

6. Indien records met WOZ-objecten doorsneden door een waterschapsgrens worden geleverd volgt hierna (anders vervolg bij 7):

| --- | --- | --- | --- | --- |
|:---|:---|:---|:---|:---|
|Stuurrecord |
| positie  | lengte  | type  | nummer  | naam gegeven  |
| 1 - 2  | 2  | N  | 93.10  | Recordidentificatiecode (= 10)  |
| 3 - 4  | 2  | N  | 93.20  | Deelbestandsidentificatie (= 70)  |
| 5 - 256  | 252  | A  | --- | Filler  |

| --- | --- | --- | --- | --- |
|:---|:---|:---|:---|:---|
|Gegevensrecord |
| positie  | lengte  | type  | nummer  | naam gegeven  |
| 1 - 2  | 2  | N  | 93.10  | Recordidentificatiecode (= 70)  |
| 3 - 14  | 12  | N  | 01.01  | Uniek WOZ-objectnummer  |
| 15 - 25  | 11  | N  | 15.10  | Vastgestelde waarde  |
| 26 - 29  | 4  | N  | 71.10  | Code afnemer  |
| 30 - 30  | 1  | A  | 81.10  | Mutatiecode  |
| 31 - 38  | 8  | D  | 81.20  | Ingangsdatum  |
| 39 - 46  | 8  | D  | 81.30  | Einddatum  |
| 47 - 256  | 210  | A  | --- | Filler  |

| --- | --- | --- | --- | --- |
|:---|:---|:---|:---|:---|
|Telrecord |
| positie  | lengte  | type  | nummer  | naam gegeven  |
| 1 - 2  | 2  | N  | 93.10  | Recordidentificatiecode (= 90)  |
| 3 - 11  | 9  | N  | --- | Totaal aantal gegevensrecords  |
| --- | --- | --- | --- | deelbestand  |
| 12 24  | 13  | N  | --- | Totaaltelling 15.10  |
| 25 - 256  | 232  | A  | --- | Filler  |

7. Indien records met statusveranderingen van beschikkingen worden geleverd volgt hierna (anders vervolg bij 8):

| --- | --- | --- | --- | --- |
|:---|:---|:---|:---|:---|
|Stuurrecord |
| positie  | lengte  | type  | nummer  | naam gegeven  |
| 1 - 2  | 2  | N  | 93.10  | Recordidentificatiecode (= 10)  |
| 3 - 4  | 2  | N  | 93.20  | Deelbestandsidentificatie (= 80)  |
| 5 - 256  | 252  | A  | --- | Filler  |

| --- | --- | --- | --- | --- |
|:---|:---|:---|:---|:---|
|Gegevensrecord |
| positie  | lengte  | type  | nummer  | naam gegeven  |
| 1 - 2  | 2  | N  | 93.10  | Recordidentificatiecode (= 80)  |
| 3 - 14  | 12  | N  | 01.01  | Uniek WOZ-objectnummer  |
| 15 - 22  | 8  | D  | 15.20  | Waardepeildatum  |
| 23 - 24  | 2  | A  | --- | Filler  |
| 25 - 26  | 2  | N  | 22.10  | Code status beschikking  |
| 27 - 27  | 1  | A  | 81.10  | Mutatiecode  |
| 28 - 35  | 8  | D  | 81.20  | Ingangsdatum  |
| 36 - 43  | 8  | D  | 81.30  | Einddatum  |
| 44 - 53  | 10  | N  | 01.10  | A-nummer natuurlijk persoon  |
| 54 - 62  | 9  | N  | 01.20  | BSN of een door een kamer toegekend uniek nummer als bedoeld in de [Handelsregisterwet 2007](../../../../wet/handelsregisterwet/2007/BWBR0021777/README.md)  |
| 63 - 72  | 10  | N  | 01.21  | aanvulling subjectnummer  |
| 73 - 80  | 8  | D  | 22.20  | Datum status  |
| 81 - 256  | 176  | A  | --- | Filler  |

| --- | --- | --- | --- | --- |
|:---|:---|:---|:---|:---|
|Telrecord |
| positie  | lengte  | type  | nummer  | naam gegeven  |
| 1 - 2  | 2  | N  | 93.10  | Recordidentificatiecode (= 90)  |
| 3 - 11  | 9  | N  | --- | Totaal aantal gegevensrecords  |
| --- | --- | --- | --- | deelbestand  |
| 12 - 256  | 245  | A  | --- | Filler  |

8. Leveringsbestand eindigt altijd met:

| --- | --- | --- | --- | --- |
|:---|:---|:---|:---|:---|
|Sluitrecord |
| positie  | lengte  | type  | nummer  | naam gegeven  |
| 1 - 2  | 2  | N  | 93.10  | Recordidentificatiecode (= 99)  |
| 3 - 11  | 9  | N  | --- | Totaal aantal records code = 10  |
| 12 20  | 9  | N  | --- | Totaal aantal records code = 20  |
| 21 - 29  | 9  | N  | --- | Totaal aantal records code = 30  |
| 30 - 38  | 9  | N  | --- | Totaal aantal records code = 31  |
| 39 - 47  | 9  | N  | --- | Totaal aantal records code = 40  |
| 48 - 56  | 9  | N  | --- | Totaal aantal records code = 60  |
| 57 - 65  | 9  | N  | --- | Totaal aantal records code = 70  |
| 66 - 74  | 9  | N  | --- | Totaal aantal records code = 80  |
| 75 - 83  | 9  | N  | --- | Totaal aantal records code = 90  |
| 84 - 256  | 173  | A  | --- | Filler  |

