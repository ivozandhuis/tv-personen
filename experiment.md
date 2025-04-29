# Derivation

Combining person observations into one person reconstruction is an interesting and elaborate activity. In this text I try to explain how I did this for the underlying project: which persons where attending the unveiling of the Coster statue in Haarlem on 16 July 1856? A list of the 420 names of these persons is published in a book and only contains the initials, family name and society of which they are member. As an example I study how I decide which person observations should be used to reconstruct a person record. The example I use is "J.F.C. Bolenius" of the Haarlem society of typographers.

First of all, this mentioning implies a lot of information:
- the person is a typographer, that is either a typecaster, typesetter, printer, bookbinder or bookseller.
- the person is male. Women were not typographers.
- the person is likely to be over 16 years old, so born before 1840.
- the person lives in the place of the society in 1856

If we combine these assumptions with the name "J.F.C. Bolenius" we are able to find out more about this person by looking for person observations in other sources.

| |po1|po2|po3|po4||reconstruction 1856|
|-|---|---|---|---|-|---|
|**sdo:name**|J.F.C. Bolenius|J.R.C. Bolenius|J.F.C. Bolenius|Johann Friderich Christoff Bolenius||Johann Friderich Christoff Bolenius|
|**sdo:givenName**||||Johann Friderich Christoff||Johann Friderich Christoff|
|**pnv:initials**|J.F.C.|J.R.C.|J.F.C.||||
|**sdo:familyName**|Bolenius|Bolenius|Bolenius|Bolenius||Bolenius|
|**sdo:gender**|_sdo:Male_|_sdo:Male_|_sdo:Male_|sdo:Male||sdo:Male|
|**sdo:hasOccupation**|_typograaf_|boekdrukker|_typograaf_|boekdrukker||boekdrukker|
|**picom:hasAge**|_>16_|21|_>16_|23||27|
|**sdo:address**|_Haarlem_|Amsterdam|_Haarlem_|Amsterdam||Haarlem|
|**sdo:memberOf**|haarlem1851|amsterdam1849|haarlem1851|||haarlem1851|
|**source**|||||||
|**sdo:name**|gedenkboek|ledenregister amsterdam|ledenregister haarlem|huwelijksakte1|||
|**sdo:dateCreated**|1856|1850|1855|1852|||
|**sdo:alternativeType**|drukwerk|ledenregistratie|ledenregistratie|burgerlijke stand||	


## On the observation

### Reliability
We are using a variety of sources to find observations and variation is big. If we were to use only civil registries, we would be able to rely and restrict the derivations on specific data. If the sources are very different, and the overlap in data is limited you have to work with what you've got.

Burgerlijke Stand is more reliable than Bevolkingsregister is more reliable than Ledenregistratie is more reliable than drukwerk.

### Rules
- Exactly one birth certificate per reconstruction.
- Exactly one tax registration per time period per administrative unit per reconstruction.
- etc. 

## On the values

### On strings
- Levenshtein distance / Winkler thing
- Incorporate length of the string? (The longer the string, the bigger the chance an error occurs, but more letters capture more information, see [Entropy](https://en.wikipedia.org/wiki/Entropy_(information_theory))).

### On terms
- For occupational title: place in the HISCO-tree
- For places: in the geographical hierarchy

### On numbers
- For age: calculate approx. date of birth

### On dates
Compare like strings

## On the combination of values
- Combining various attributes|relations
- Data triangulation

## On the uniqueness of values
tf/idf?

## On the uniqueness of the combination of values


