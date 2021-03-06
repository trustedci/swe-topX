# Readme

#### Purpose
This purpose of the project is to determine the most frequent computer security weaknesses encountered in the wild. This is done by taking JSON file(s) containing CVEs and counting the CWEs referenced within. 

#### Interface
The JSON files commonly referred to as CVE NVD data feeds were sourced from the National Vulnerability Database (NVD). The main script in the project is `countCWE.py`. It requires at least one JSON file provided as input in order to create a CSV file containing the CWE IDs and their respective frequencies of occurrence as found within the JSON file. An optional additional input file may be provided to help label the name/title of respective CWE IDs in the output file. You may use the CWE research concepts file, `1000.csv`, as provided by Mitre, for this. Also, an optional bar chart plotting script `plotFreq.py` is included for visualization of the data file returned from `countCWE.py`.

#### File Index
* Readme.md - the file you are reading now
* report.md - a more comprehensive description of this project
* countCWE.py - counts the frequency of CWE occurrences in a given JSON dataset of CVEs
* plotFreq.py - uses the output CSV file from *countCWE.py* to plot standard frequency and relative (ratio) frequency bar graphs of CWEs
* LICENSE - the terms of use of this project

#### Requirements
* Python 3.XX
* *plotFreq.py* requires you to install matplotlib.
If you have pip installed you may install matplotlib by running `pip install matplotlib`
* While not required, the markdown (.md) file styles are best viewed in a markdown viewer

#### Usage
Run `python countCWE.py -h` or `python plotFreq.py -h` for respective usage. 


#### Additional Documentation
Use one of the following commands: `pydocs countCWE` or `pydocs plotFreq` to get an outline of function documentation of functions implemented in *countCWE.py* and *plotFreq.py* respectively. The comments displayed from using pydoc are also available in the actual python code but if you do not wish to view the entire source code then it is nice to know that the pydoc command exists.
