# AVH collectors

Script and output from work done to match AVH collector strings to Wikidata 
Items, following https://github.com/matdillen/STSM-wikidata-people.

### Jupyter Notebooks

- [Create AVH collectors data set](./create_avh_collectors_dataset.ipynb)

- [Create CHAH Collectors and Illustrators data set](./create_chah_collectors_dataset.ipynb)

- [Create Wikidata items data set](./create_wikidata_dataset.ipynb)

- [Match AVH collector strings to Wikidata items](./match_names_to_wikidata_items.ipynb)

- [Cosine Similarity](./cosine-similarity.ipynb): tested Cosine Similarity on AVH collectors and MEL collectors. Cosine Similarity is even faster and appears to give slightly better matches.

### Results

- 1000 most prolific collectors in AVH: [Nearest Neighbour](./data/avhcoll_wikidata_matches_indiv.csv) | [Cosine Similarity](./data/avhcoll_wikidata_cossim.csv)

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
  bloodhound_id | Bloodhound Tracker ID ([P6944](https://www.wikidata.org/wiki/Property:P6944))
  enc_au_sc_id | Encyclopedia of Australian Science ID ([P4228](https://www.wikidata.org/wiki/Property:P4228))
  au_dict_bio_id | Australian Dictionary of Biography ID ([P1907](https://www.wikidata.org/wiki/Property:P1907))
  yob	| Year of birth (derived from [P569](https://www.wikidata.org/wiki/Property:P569))
  yod	| Year of death (derived from [P496](https://www.wikidata.org/wiki/Property:P570))
  wyb	| Start year of work period (derived from [P2031](https://www.wikidata.org/wiki/Property:P2031))
  wye | End year of work period (derived from [P2032](https://www.wikidata.org/wiki/Property:P2032))
  **links** |
  wikidata_link | Link to Wikidata page (HTML)
  orcid_link | Link to ORCID
  harv_link | Link to Harvard Index of Botanists
  ipni_link | Link to IPNI authors entry
  bloodhound_link | Link to Bloodhound Tracker page
  enc_au_sc_link | Link to Encyclopedia of Australian Science entry
  au_dict_bio_link | Link to Australian Dictionary of Biography entry

- Agents in MELISR (Collection Management System of the National Herbarium of Victoria (MEL)): 
  - Agents with 1000 or more collections (n=147): [Nearest Neighbour](./data/melcoll_wikidata_matches_indiv.csv) | [Cosine Similarity](./data/melcoll_wikidata_cossim.csv)

  - Agents with 500-999 collections (n=138): [Cosine Similarity](./data/melcoll_500_wikidata_cossim.csv)

  - Agents with 100-499 collections (n=821): [Cosine Similarity](./data/melcoll_100_wikidata_cossim.csv)

  - Agents with 100 or more identifications (n=107): [Cosine Similarity](./data/meldet_wikidata_cossim.csv)

- Australian Collectors and Illustrators: [Nearest Neighbour](./data/chahcoll_wikidata_matches_indiv.csv) | [Cosine Similarity](./data/chahcoll_wikidata_cossim.csv)

- Plantentuin Meise collectors (data set used in https://github.com/matdillen/STSM-wikidata-people): [Nearest Neighbour](./data/bgmcoll_wikidata_matches_indiv.csv) | [Cosine Similarity](./data/bgmcoll_wikidata_cossim.csv)




