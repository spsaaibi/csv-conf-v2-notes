# csv-conf-v2-notes

Here are my notes from [*csv,conf,v2*](http://csvconf.com/) which took place in Berlin, May 3-4 2016.


## Day 1: May 3, 2016

### 1. Richard Smith-Unna (@blahah404): Easy, massive-scale reuse of scientific outputs

- Less than 1.8% of the literature is legally reusable. 1.4M docs only!
- What can be done?
- `getpapers`: `getpapers --query nanotoxicity --pdf --outdir nano`
- `bin/getpapers.js --query nanotoxicity --minedterms --outdir nano`
- Rapidly summarise a field with a few queries!
- github codeforscience sciencefair


### 2. Richard Jones (@richard_d_jones), Cottage Labs

- Eliminate Admin.
- upload spreadsheets.
- query them easily
- We do weird shit w/ spreadsheets
- Process:
- decode the bits
- read the data to json
- make it queryable -> elasticsearch
- publish interactive interfaces: jquery on top of elasticsearch


### 3. Matthias Buus (@mafintosh) from Dat (instead of Karissa McKelvey)


- Dat project
- Founded by sloan
- 3 person team, 800 modules on npm
- built for sharing datasets
- `npm install -g dat`
- `dat link filename.csv`
- dat datcommand -> you get the data!
- git: one line per chunk, diff works well
- rabin fingerprinting: creates chunks based on the content
- `npm install rabin`
- mafintosh.github.io/hyperdrive
- p2p in the browser
- hashing makes the sharing WAY faster!
- npm install hyperdrive

### 4. KEYNOTE, Zarah Rahman (@zararah)

- Bridging tech and activism
- Responsible data program, using data ethically
- Asking questions
- The reflection stories: sometimes tech does improve people's lives
- using sensitive data, analysis, ask questions
- Program: Physicians for Human Rights
- Medicapt: Standardise collection, digitise, iterate, reality check.
- Sharing reports of violence: PII, collaboration, launch
- hrdag.org data collection on warzones
- Commonalities:
- admitting uncertainties.
- Context
- Diversity, transdisciplinarity
- Collaboration
- Questions:
- adversary do with your data?
- holistic security plan?
- what does informed consent look like for your population?
- Who thinks about the ethics of what you're doing?
- responsibledata.io


### 5. Jeni Tennison, Make CSV a first class web citizen

- discovering metadata
- linking csv in a table
- getting sorting right
- reference using hard links/references
- machine readability/ human readability
- theODI.org


### 6. Sadayuki Furuhashi (@frsyuki), Treasure Data. Fighting against chaotically separated values with Embulk

- https://github.com/frsyuki
- Treasure Data
- Fluentd (collect logs in json)
- Embulk (data collection)
- MessagePack (like json but faster/smaller)
- Embulk: Use plugins to make data loading and reading very easy
- plugin-based parallel data loader

Problem: CSV files are hard to parse

Treasure Data:SQL access to big data

But it's hard to load big data formats.

- it creates a config file that guesses timestamp format
- `embulk preview`
- `embulk run`
- load the most data, so that one can handle broken records separately

### 7.  Thomas Steiner (@tomayac), Wikipedia tools in google spreadsheets

- bit.ly/wikipedia-tools-slides
- Wikipedia/Wikidata. Structured knowledge base for wikipedia.
- Google spreadsheets is easy to extend with javascript, UrlFetchApp
- WIKISYNONYMS(en:Berlin)
- WIKITRANSLATE
- WIKIGEOCOORDINATES
- WIKIDATAFACTS (single or multi value facts)
- WIKIQUARRY (built specific querys, with ids)
- WIKICATEGORIES
- WIKIMUTUALLINKS
- WIKIINBOUNDLINKS
- WIKIOUTBOUNDLINKS
- WIKISEARCH
- bit.ly/wikipedia-tools-demo
- Usage: Ordered category panels
- tomayac/wikipedia-tools-for-google-spreadsheets
- QUERY(WIKIDATAFACTS("de: ",&A1), "SELECT Col2 WHERE Col1 = 'instance of')


### 8. Mouse Reeve (@tripofmice): Grimoires, Demonology and Databases

- Grimoires and Demons: many to many, foreign keys
- Nodes and Edges
- cool networks of grimoires and spells, directed
- grimoire.org

### 9. KEYNOTE, Sarah Gold (@sarahtgold) designing for data
- projectsbyif.com
- multidisciplinary team, understand tech/design inform one another
- problem space
- monitoring/testing
- design for data
- TC are broken
- objects are informants and will betray us
- design for minimum viable data

## Day 2: May 4, 2016


### 1. KEYNOTE, Jenny Brian (@jennybc): All my friends use spreadsheets

- spreadsheets, on github
- monads in excel!
- reactivity in excel has been there for yrs!
- data, formatting and programming logic
- stencila
- alphasheets
- pyspread
- R package TableToLongForm
- readxl,openxslx, XLConnect
- read and expose unformatted, unevaluated spreadsheet data
- you can now extract formatting out of sheets using googlesheets!
- packages: googlesheets, rexcel
- linen object: workbook, worksheet, cell
- `jailbreakr` package, to get data out of excel

### 2. Aurelie Moser (@auremoser), Maps to CSV

- Maps are extremely accesible
- CSVs are transparent
- geonames are coded at CSV
- cartodb supports CSV
- tons of great examples of usage of csvs
- awesome geocoder projects
- geocoding the future
- make their owns maps, less politics
- global forest watch
- whereonmars.co
- maps: illustrate concepts and teaching aids


### 3. Darren Barnes (@darrbarnes), ONS Databaker

- scraperwiki/databaker
- json formatting of the metadata
- the UK buro of statistics uses this to transform excel files into sane data formats

### 4. KEYNOTE, Jeremy Freeman (@thefreemanlab), Open Source Neuroscience

- janelia.org (northern virginia)
- we still don't understand much about the brain
- they use mice, put them on a VR (not visual, but tactile)
- random access  two photon mesoscope
- ethanography of labs: why is 80/20 data-munging/science
- each lab reiventing the workflow from raw data to results
- build modules; use them to build pipelines
- thunder and bolt (@jwittenbach): image and time series analysis
- neurofinder.codeneuro.org
- lightning-viz.org
- tactile coding  sofronienw
- project binder: mybinder.org
- tutorials: strata-singapore
- it's being used for data journalism
- dat-data.com -> sharing data and environments
- studying more complicated behaviors: Learning, decision making
- experiments as collections of modules
- human perception vs. what we can study in animals
- using games to understand behavior and probe brains (human experiment, hexaworld)

### 5. Basile Simon (@basilesimon), Reusability and Linked Data in Journalism BBC

- bbc news labs
- humans extract meanings from new things
- web of meanings -> linked data
- who is talking about what? By bbc. Linked data about news
- articles are the unit of journalism
- but events should be the basic units. Big or small, but easier to describe as linked data.
- news storyline model
- Elastic news project: with the same event info, one is able to dive in or zoom out to content.
- story: structured account of connected events.
- reported expertise is surfaced in content coverage.


### 6. Till Döhmen: Automatic Detection and conversion of logical table structures

- tons of data janitorial work in data science
- parse heterogeneous data sources
- Want to obtain canonical tables with tidy data
- csvs have tons of messy data
- 19982 csvs in data.gov.uk, only 1/3 are issue-free
- there's no handling for multitable per file nor complex formats
- most files are pretty small
- avoid breaks in parsing, throw computation power
- solution: multi-hypothesis parsing: add quality assessment at the end of comparing multiple table outputs.
- quality: distance from original, table shape, number of NA or NULL, coherence/consistency of values, specificity of data, unique headers
- stepwise error handling


### 7. Jure Triglav (@juretriglav): open science, open data, open source

- Collab between: stencila, substance and pubsweet.
- coko.foundation -> moore funding
- pubsweet: framework for knowledge production.
- completely open, knowledge production system.
- substance.io: web-based text editor.
- a great sci publishing blog
