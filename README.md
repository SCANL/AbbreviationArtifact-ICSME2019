# AbbreviationArtifact-ICSME2019
Artifact for ICSME 2019.

This artifact includes two scripts. The first script, parse_abbreviation_expansions.cpp gives an example of how to parse the identifiers, abbrevivations, and expansions out of the csv files for each project. The second, GetIdentifierFileLocations.py gives an example of how to use srcML and XPath (via python) to determine every file where each identifier in the .csv artifacts occur. This is useful if you want to know, for example, where to look for abbreviation expansions while testing your own technique.

To compile parse_abbreviation_expansions.cpp:

clang++ parse_abbreviation_expansions.cpp -std=c++1y

To run:

./a.out [name of csv file]

To run GetIdentifierFileLocations.py, you'll need the wycheproof.java.xml example project file included in the repository. Follow these instructions:

1. Make sure lxml is installed: sudo apt-get install python3-lxml
2. unzip wycheproof srcml example: gzip -d wycheproof.java.xml.gz
3. python3 GetIdentifierFileLocations.py

If you're interested in modifying the scripts for your own use, you'll need to run srcML on whatever system you're interested in. Check out the srcML webpage for information on how to download/install and run srcML: https://www.srcml.org