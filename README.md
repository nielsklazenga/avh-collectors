# AVH collectors

Script and output from work done to match AVH collector strings to Wikidata 
Items, following https://github.com/matdillen/STSM-wikidata-people.

### Jupyter Notebooks

- [Create AVH collectors data set](./create_avh_collectors_dataset.ipynb)

  Explanation of column headers:

  Column | Description
  -|-
  **AVH collectors** |
  label | Collector name string from AVH
  count | Number of records with this collector name string in AVH
  start_date | Year of first collection
  end_date | Year of last collection
  activity_span | Number of years between first and last collection
  **Name matching** |
  name | input name; = AVH collector name string
  matched_name | matched name; = Wikidata item label name is matched to
  distance | Nearest Neighbour distance between the name and matched name; the lower the value, the better the match
  **Wikidata** |
  item | Wikidata Item ID (URL)
  itemLabel | Wikidata Item label
  surname	| Surname; derived from item label
  initials | Initials; derived from item label
  canonical_string | Canonical name string; derived from item label, used for matching
  orcid | ORCID ([P496](https://www.wikidata.org/wiki/Property:P496))
  viaf | VIAF ID ([P214](https://www.wikidata.org/wiki/Property:P214))
  isni | ISNI ID ([P213](https://www.wikidata.org/wiki/Property:P496))	
  harv | Harvard Index of Botanists ID ([P6264](https://www.wikidata.org/wiki/Property:P6264))
  ipni | IPNI author ID ([P586](https://www.wikidata.org/wiki/Property:P586))
  abbr | botanist author abbreviation (standard form) ([P428](https://www.wikidata.org/wiki/Property:P428))
  yob	| Year of birth (derived from [P569](https://www.wikidata.org/wiki/Property:P569))
  yod	| Year of death (derived from [P496](https://www.wikidata.org/wiki/Property:P570))
  wyb	| Start year of work period (derived from [P2031](https://www.wikidata.org/wiki/Property:P2031))
  wye | End year of work period (derived from [P2032](https://www.wikidata.org/wiki/Property:P2032))

- [Create CHAH Collectors and Illustrators data set](./create_chah_collectors_dataset.ipynb)

- [Create Wikidata items data set](./create_wikidata_dataset.ipynb)

- [Match AVH collector strings to Wikidata items](./match_names_to_wikidata_items.ipynb)

### Results

- [1000 most prolific collectors in AVH](./data/avhcoll_wikidata_matches_indiv.csv)

- [Australian Collectors and Illustrators](./data/chahcoll_wikidata_matches_indiv.csv)

- [Agents with 1000 or more collections in MELISR](./data/melcoll_wikidata_matches_indiv.csv) (Collection Management System of the National Herbarium of Victoria (MEL))




