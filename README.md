# MultiTool: dane

Paczki stacji sieci komórkowych z innych krajów Europy dla aplikacji MultiTool (Android). To tylko dane:
gotowe pliki `KRAJ.pack.gz` i spis `index.json`, odświeżane co tydzień. Kodu tu nie ma.

Mobile network base station packs for other European countries, used by the MultiTool app. Data only, no code.

| Kraj / Country | Źródło / Source | Licencja / Licence |
|---|---|---|
| Francja / France (FR) | ANFR, „Données sur les réseaux mobiles” (data.anfr.fr); nazwy gmin / commune names: INSEE, Code officiel géographique | Licence Ouverte 2.0 (Etalab) |
| Belgia / Belgium (BE) | Flandria / Flanders: Departement Omgeving, zendantennes (conformiteitsattesten); Walonia / Wallonia: SPW, cadastre des antennes émettrices stationnaires; Bruksela / Brussels: Bruxelles Environnement, cadastre des antennes | Modellicentie Gratis Hergebruik 1.0 (Flanders); CC BY 4.0 (Wallonia); no conditions (Brussels WFS) |
| Chorwacja / Croatia (HR) | HAKOM, Geografski sustav popisa odašiljača (ekarta.hakom.hr) | Otvorena dozvola (data.gov.hr) |
| Luksemburg / Luxembourg (LU) | Géoportail, INSPIRE GSM antennas cadastre (data.public.lu) | CC0 |
| Szwajcaria / Switzerland (CH) | BAKOM/OFCOM, Standorte von Sendeanlagen für Mobilfunk (data.geo.admin.ch) | Open use, must provide the source (opendata.swiss) |

Kraje z `"kind": "ocid"` w `index.json`: Cell tower data from OpenCelliD (https://opencellid.org), licensed under
CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/). Zmiany / changes: komórki LTE złożone w stacje po numerze
eNB, położenie to średnia położeń komórek ważona liczbą pomiarów, technologie (5G, GSM, UMTS) z komórek tej samej sieci
do 500 m / LTE cells grouped into stations by eNB, position averaged weighted by samples, technologies added from
cells of the same network within 500 m. Położenie przybliżone (środek miejsc pomiarów, zwykle ok. 1 km od masztu),
to nie jest pełny wykaz / approximate positions (centre of the measurement points, usually about 1 km from the mast),
not a complete list.

Kraje z `"kind": "osm"` w `index.json`: maszty sieci komórkowych z OpenStreetMap, © OpenStreetMap contributors,
licencja ODbL 1.0 (https://www.openstreetmap.org/copyright). Tylko maszty z podaną siecią, to nie jest pełny wykaz.
Countries with `"kind": "osm"` in `index.json`: mobile masts from OpenStreetMap, © OpenStreetMap contributors,
ODbL 1.0. Only masts with a known network, not a complete list of stations.

Paczki są udostępniane na licencjach ich źródeł, z podaniem źródła i daty danych (w paczce i w aplikacji).
Dane są przetworzone: anteny tej samej sieci blisko siebie złożone w jedną stację, współrzędne przeliczone na WGS84.
Packs are provided under the licences of their sources, with source and data date in each pack and in the app.
The data is processed: antennas of the same network close together are merged into one station, coordinates are
converted to WGS84.
