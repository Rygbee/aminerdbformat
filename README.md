Aminer DB Format 
===================================

_Write before all , this is just a suggestion of our format , we also welcome any other fields_
Please do not hesitate to contact me(Yu Jing <yujing5b5d@gmail.com>) if you have any question or suggestion. 


### Publication 

Field Name       | Field Type     |  Description           | Example 
:--------------- | :------------: | :--------------------: | --------------:
title            | String         | Title                  | ArnetMiner: extraction and mining of academic social networks
abstract         | String         | Abstract               | This paper addresses several key issues ....
keywords         | String         | Keywords,splited by ';'| Social Network ; Information Extraction ; Name Disambiguation ; Topic Modeling ;Expertise Search ; Association Search
page_start       | String         | Page Start             | 990
page_end         | String         | Page End               | 998
volume           | String         | Volume                 | 
issue            | String         | Issue                  |
editor           | AuthorInPub*   | Editor List            |
author_str       | String         | Origin Author String   | Jie Tang, Jing Zhang,Limin Yao, Juanzi Li,Li Zhang, Zhong Su
venue            | VenueInPub*    | Venue Information      | 
isbn             | String         | ISBN                   |
issn             | String         | ISSN                   |
doi              | String         | DOI                    |
url              | String List    | external links         | ["http://xxx.com/doi/xxx","http://yyy.org/xxx"]
citation         | CiteInfo*      | cited by other papers  | 
reference        | CiteInfo*      | reference some other paper | 
raw_reference    | String         | reference string       | 
src              | String         | identity of data source  | ides
sid              | String         | origin id in data source | "0123467fb"
pdf              | String         | pdf data file name     | "~aminer/data/pdf/aa/bb/cc/paper.pdf"

### AuthorInPub

Field Name       | Field Type     |  Description           | Example 
:--------------- | :------------: | :--------------------: | --------------:
name             | String         | name                   | Jie Tang
alias            | String         | may some other names , splited by ';' | J. Tang ; Tang,Jie
email            | String         |                        | jietang@tsinghua.edu.cn
org              | String         | organization           | Tsinghua University
pos              | Integer        | position , start form 0 | 
sid              | String         | id in data srouce      |

### VenueInPub
Field Name       | Field Type     |  Description           | Example 
:--------------- | :------------: | :--------------------: | --------------:
name             | String         | venue name in paper    | 
type             | Integer        | definited in _Type Definition of Venue_ |
id               | String         | id in _Venue_            |        

### CiteInfo
Field Name       | Field Type     |  Description           | Example 
:--------------- | :------------: | :--------------------: | --------------:
raw              | String         | Citation Raw String    | J. Tang, J. Zhang, L. Yao, J. Li, L. Zhang,  and Z. Su,   "ArnetMiner: extraction and mining of academic social networks",  ;in Proc. KDD, 2008, pp.990-998. 
sid              | String         | cited or reference paper's id in data source  |
seq              | Integer        | Sequence , for reference only , start from 0 | 
doi              | String         | 


### Venue
Field Name       | Field Type     |  Description          | Example 
:--------------- | :------------: | :-------------------: | --------------:
if               | Float          | Impact Factor         | 1.68
name             | String         | Full Name             | Knowledge Discovery and Data Mining
short_name       | String         | Short Name            | KDD
publisher        | String         | Publisher             | ACM
alias            | String         | Alias                 |
url              | String         | Official website      | http://www.kdd.org/
type             | Integer        | Id in Type Definition | 2


### Type Definition of Venue

Venue Type       | Type Id     | Description
:--------------- | :---------: | --------:
unknown          |  0          | this is just 'unkown' , not 'other', if you know the venue's right type , you may add more type definition
journal          |  1          |
conference       |  2          |
book             |  3          | 
thesis           |  4          | master thesis , phd thesis , etc.
technical report |  5          | 
encyclopedia     |  6          |
magazine         |  7          |
newsletter       |  8          |
play             |  9          |
inproceedings    | 10          |
article          | 11          |
incollection     | 12          |
www              | 13          |





