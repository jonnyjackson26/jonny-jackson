---
title: Typesetting Errors in the 1830 Book of Mormon
date: 2026-08-29T09:02:00.000-06:00
weight: 0
draft: false
summary: Compiling a list of all 96+ typesetting errors or typos in the 1830
  Book of Mormon
tags:
  - church
techstack:
  - python
projectLink:
  text: GitHub
  url: https://github.com/jonnyjackson26/1830-bom-typos
cover:
  hiddenInSingle: false
---
The purpose of this project is to document every typesetting error (or typo) in the first edition (1830) of the Book of Mormon.

To do this, I begin with a digitized text of the Book of Mormon and extract every unique word it contains. I then compile every word in Noah Webster's 1828 *American Dictionary of the English Language* — the first dictionary of American English, published just two years before the Book of Mormon. Comparing the two word lists identifies every word that appears in the Book of Mormon but not in Webster's dictionary. This initial list contains far more than just typos, so I review it manually to arrive at a final list of genuine typesetting errors.

All data for this project can be found between these two GitHub repositories: https://github.com/jonnyjackson26/unique-bom-words and https://github.com/jonnyjackson26/1830-bom-typos.

## Finding the 1830 Text of the Book of Mormon
5,000 copies of the Book of Mormon were printed in 1830, using a process far more prone to human error than modern printing. Individual metal characters were set by hand, inked, and pressed onto paper; typesetters occasionally missed or misplaced a character. According to research published by BYU, as printing progressed, some errors were caught and corrected mid-run, meaning two copies of the first edition could differ from one another textually. It is possible that no two of the original 5,000 copies are textually identical.[^1] The only cleanly-formatted text I could find of the 1830 Book of Mormon was published by the BYU Office of Digital Humanities on GitHub (https://github.com/BYU-ODH/OpenScripture), so I will use this version of the text. It is unknown how many typesetting errors were corrected before this specific book was published and digitized.

[^1]: "Variations between Copies of the First Edition of the Book of Mormon," https://byustudies.byu.edu/article/variations-between-copies-of-the-first-edition-of-the-book-of-mormon


## Finding Noah Webster's 1828 Dictionary
The data came from https://github.com/DataWar/1828-dictionary, but I've published a more cleaned-up format at https://github.com/jonnyjackson26/1828-websters-dictionary. The complete list can be read in this project at [`dictionary-words.txt`](https://github.com/jonnyjackson26/1830-bom-typos/blob/main/dictionary-words.txt). Note that I chose this dictionary because it was published just two years before the publication of the Book of Mormon, and it's the first American English dictionary. Language and spelling are very subjective, so some words in this dictionary would not be deemed correct in our modern language, such as "tongue" being spelled as "tung".[^2] You will see in the compiled list below a section for words that are technically typos when the source of truth is this American English dictionary, even though the words are mostly considered correct today because it's the British English spelling. Also, there are some words that either have hyphens when they shouldn't or don't have hyphens when they should, but these are less interesting than the actual typesetting errors or typos.

[^2]: "Noah Webster and America's First Dictionary," https://www.merriam-webster.com/about-us/americas-first-dictionary


## Curating unique words
After running [`generate_unique_words.py`](https://github.com/jonnyjackson26/unique-bom-words/blob/main/scripts/generate_unique_words.py) we are left with 1,825 words that are in the Book of Mormon but not in the dictionary, as you can see in [`bom-words-not-in-dictionary.txt`](https://github.com/jonnyjackson26/1830-bom-typos/blob/main/bom-words-not-in-dictionary.txt). Most of these words are indeed words, just in other variations. For example, `denied`, `deniest`, `denieth`, and `denying` are all real words in this list, but the dictionary only has `deny`. Many of the words in this list are archaic, past or future tenses, present participles, or other forms of a verb in the dictionary, or plurals. These I mark as "Variation" in [`curated_words.csv`](https://github.com/jonnyjackson26/1830-bom-typos/blob/main/curated_words.csv). There are also words I mark as "Proper," such as names and places that are not typos but are not in the dictionary either (like `Nephi` or `Jerusalem`). Similarly, there are also words I mark as "Real," such as `liahona` or `cureloms` which are not places nor people, but real things that the Book of Mormon gives names to. All other words are marked as "Typo".



---
## Real typos / typesetting errors
- aaswer (1) - [Alma 11:21](https://bom-editions.vercel.app/en/1830/alma/11#21) should be "answer"
- adhear (1) - [Alma 60:34](https://bom-editions.vercel.app/en/1830/alma/60#34) should be "adhere"
- ancles (1) - [1 Nephi 18:15](https://bom-editions.vercel.app/en/1830/1-nephi/18#15) should be "ankles"
- angles (1) - [Helaman 10:6](https://bom-editions.vercel.app/en/1830/helaman/10#6) should be "angels"
- armss (1) - [Alma 50:26](https://bom-editions.vercel.app/en/1830/alma/50#26) should be "arms"
- arrriven (1) - [Helaman 13:24](https://bom-editions.vercel.app/en/1830/helaman/13#24) should be "arriven" (later changed to "arrived")
- atempt (1) - [Alma 55:30](https://bom-editions.vercel.app/en/1830/alma/55#30) should be "attempt"
- bablings (1) - [Alma 1:32](https://bom-editions.vercel.app/en/1830/alma/1#32) should be "babblings"
- babtized (1) - [3 Nephi 18:30](https://bom-editions.vercel.app/en/1830/3-nephi/18#30) should be "baptized"
- bacause (1) - [Helaman 7:5](https://bom-editions.vercel.app/en/1830/helaman/7#5) should be "because"
- becaus (1) - [Alma 62:1](https://bom-editions.vercel.app/en/1830/alma/62#1) should be "because"
- berak (1) - [3 Nephi 18:3](https://bom-editions.vercel.app/en/1830/3-nephi/18#3) should be "break"
- betweem (1) - [Helaman 2:1](https://bom-editions.vercel.app/en/1830/helaman/2#1) should be "between"
- carcases (1) - [Alma 16:10](https://bom-editions.vercel.app/en/1830/alma/16#10) should be "carcasses"
- changeble (1) - [Moroni 8:12](https://bom-editions.vercel.app/en/1830/moroni/8#12) should be "changeable"
- chid (1) - [1 Nephi 11:20](https://bom-editions.vercel.app/en/1830/1-nephi/11#20) should be "child"
- citties (1) - [Helaman 7:22](https://bom-editions.vercel.app/en/1830/helaman/7#22) should be "cities"
- clowd (1) - [Ether 2:4](https://bom-editions.vercel.app/en/1830/ether/2#4) should be "cloud"
- condescention(s) (3) - [1 Nephi 11:16](https://bom-editions.vercel.app/en/1830/1-nephi/11#16), [1 Nephi 11:26](https://bom-editions.vercel.app/en/1830/1-nephi/11#26), [Jacob 4:7](https://bom-editions.vercel.app/en/1830/jacob/4#7) should be "condescension"
- continnally (1) - [Alma 58:41](https://bom-editions.vercel.app/en/1830/alma/58#41) should be "continually"
- daghter (1) - [1 Nephi 16:7](https://bom-editions.vercel.app/en/1830/1-nephi/16#7) should be "daughter"
- deadnes (1) - [2 Nephi 25:27](https://bom-editions.vercel.app/en/1830/2-nephi/25#27) should be "deadness"
- deliteth (1) - [2 Nephi 4:15](https://bom-editions.vercel.app/en/1830/2-nephi/4#15) should be "delighteth"
- drunkennes (1) - [Alma 55:19](https://bom-editions.vercel.app/en/1830/alma/55#19) should be "drunkenness"
- eatheth (2) - [3 Nephi 20:8](https://bom-editions.vercel.app/en/1830/3-nephi/20#8) should be "eateth"
- eigth (1) - [Alma 53:23](https://bom-editions.vercel.app/en/1830/alma/53#23) should be "eight"
- evidencess (1) - [Helaman 5:50](https://bom-editions.vercel.app/en/1830/helaman/5#50) should be "evidences"
- feading (1) - [Enos 1:20](https://bom-editions.vercel.app/en/1830/enos/1#20) should be "feeding"
- firy (1) - [1 Nephi 15:24](https://bom-editions.vercel.app/en/1830/1-nephi/15#24) should be "fiery"
- firy-flying (1) - [1 Nephi 17:41](https://bom-editions.vercel.app/en/1830/1-nephi/17#41) should be "fiery flying"
- fraid (3) - [Alma 47:2](https://bom-editions.vercel.app/en/1830/alma/47#2), [Alma 58:24](https://bom-editions.vercel.app/en/1830/alma/58#24), + 1 more should be "afraid"
- govereor (1) - [Helaman 1:13](https://bom-editions.vercel.app/en/1830/helaman/1#13) should be "governor"
- havgn (1) - [Alma 17:18](https://bom-editions.vercel.app/en/1830/alma/17#18) should be "having"
- heen (1) - [Alma 26:9](https://bom-editions.vercel.app/en/1830/alma/26#9) should be "been"
- hehold (1) - [Alma 43:8](https://bom-editions.vercel.app/en/1830/alma/43#8) should be "behold"
- hia (1) - [Alma 22:27](https://bom-editions.vercel.app/en/1830/alma/22#27) should be "his"
- hy (1) - [Ether 9:3](https://bom-editions.vercel.app/en/1830/ether/9#3) should be "by"
- journied (7) - [1 Nephi 4:38](https://bom-editions.vercel.app/en/1830/1-nephi/4#38), [1 Nephi 5:6](https://bom-editions.vercel.app/en/1830/1-nephi/5#6), + 5 more should be "journeyed"
- khown (1) - [Alma 22:18](https://bom-editions.vercel.app/en/1830/alma/22#18) should be "known"
- lamanitas (1) - [Alma 58:6](https://bom-editions.vercel.app/en/1830/alma/58#6) should be "Lamanites"
- langauge (1) - [Mosiah 28:17](https://bom-editions.vercel.app/en/1830/mosiah/28#17) should be "language"
- mnltitude (1) - [3 Nephi 18:17](https://bom-editions.vercel.app/en/1830/3-nephi/18#17) should be "multitude"
- moulder(ing) (3) - [Alma 28:11](https://bom-editions.vercel.app/en/1830/alma/28#11), [Mormon 6:15](https://bom-editions.vercel.app/en/1830/mormon/6#15), [Mormon 6:21](https://bom-editions.vercel.app/en/1830/mormon/6#21) should be "molder"
- moulten (3) - [Ether 3:1](https://bom-editions.vercel.app/en/1830/ether/3#1), [Ether 3:3](https://bom-editions.vercel.app/en/1830/ether/3#3), + 1 more should be "molten"
- neeeds (1) - [2 Nephi 2:11](https://bom-editions.vercel.app/en/1830/2-nephi/2#11) should be "needs"
- neverthelers (1) - [3 Nephi 5:18](https://bom-editions.vercel.app/en/1830/3-nephi/5#18) should be "nevertheless"
- nevertheles (1) - [2 Nephi 2:2](https://bom-editions.vercel.app/en/1830/2-nephi/2#2) should be "nevertheless"
- numerority (1) - [Alma 56:10](https://bom-editions.vercel.app/en/1830/alma/56#10) should be "numerosity"
- numhers (1) - [Alma 58:15](https://bom-editions.vercel.app/en/1830/alma/58#15) should be "numbers"
- obout (1) - [Enos 1:19](https://bom-editions.vercel.app/en/1830/enos/1#19) should be "about"
- opon (1) - [Ether 9:20](https://bom-editions.vercel.app/en/1830/ether/9#20) should be "upon"
- peeple (1) - [Jacob 2:29](https://bom-editions.vercel.app/en/1830/jacob/2#29) should be "people"
- peopeople (1) - [Alma 8:30](https://bom-editions.vercel.app/en/1830/alma/8#30) should be "people"
- phrensied (1) - [Alma 30:16](https://bom-editions.vercel.app/en/1830/alma/30#16) should be "frenzied"
- plaees (1) - [2 Nephi 8:3](https://bom-editions.vercel.app/en/1830/2-nephi/8#3) should be "places"
- possesion (1) - [Alma 55:24](https://bom-editions.vercel.app/en/1830/alma/55#24) should be "possession"
- possessson (1) - [Alma 58:38](https://bom-editions.vercel.app/en/1830/alma/58#38) should be "possession"
- prohesy (1) - [2 Nephi 1:6](https://bom-editions.vercel.app/en/1830/2-nephi/1#6) should be "prophesy"
- prophecying(s) (2) - [Words of Mormon 1:6](https://bom-editions.vercel.app/en/1830/words-of-mormon/1#6), [Helaman 6:2](https://bom-editions.vercel.app/en/1830/helaman/6#2) should be "prophesying"
- provisons (1) - [Alma 57:8](https://bom-editions.vercel.app/en/1830/alma/57#8) should be "provisions"
- purifyer (1) - [3 Nephi 24:3](https://bom-editions.vercel.app/en/1830/3-nephi/24#3) should be "purifier"
- puteth (1) - [Mosiah 23:22](https://bom-editions.vercel.app/en/1830/mosiah/23#22) should be "putteth"
- reccive (1) - [Alma 8:24](https://bom-editions.vercel.app/en/1830/alma/8#24) should be "receive"
- recieve (4) - [Alma 16:16](https://bom-editions.vercel.app/en/1830/alma/16#16), [Alma 16:17](https://bom-editions.vercel.app/en/1830/alma/16#17), + 2 more should be "receive"
- recieved (1) - [Alma 11:20](https://bom-editions.vercel.app/en/1830/alma/11#20) should be "received"
- recieveth (1) - [Alma 11:3](https://bom-editions.vercel.app/en/1830/alma/11#3) should be "receiveth"
- recieving (1) - [Alma 22:22](https://bom-editions.vercel.app/en/1830/alma/22#22) should be "receiving"
- redemer (1) - [Helaman 5:11](https://bom-editions.vercel.app/en/1830/helaman/5#11) should be "redeemer"
- regin (1) - [Alma 28:7](https://bom-editions.vercel.app/en/1830/alma/28#7) should be "reign"
- rehearst (1) - [Alma 20:11](https://bom-editions.vercel.app/en/1830/alma/20#11) should be "rehearsed"
- rerecord (1) - [Enos 1:20](https://bom-editions.vercel.app/en/1830/enos/1#20) should be "record"
- rereward (2) - [3 Nephi 20:42](https://bom-editions.vercel.app/en/1830/3-nephi/20#42), [3 Nephi 21:29](https://bom-editions.vercel.app/en/1830/3-nephi/21#29) should be "rearward"
- rssurrection (1) - [Mosiah 15:21](https://bom-editions.vercel.app/en/1830/mosiah/15#21) should be "resurrection"
- rufused (1) - [Alma 27:3](https://bom-editions.vercel.app/en/1830/alma/27#3) should be "refused"
- rumderers (1) - [Mormon 2:10](https://bom-editions.vercel.app/en/1830/mormon/2#10) should be "murderers"
- seeond (1) - [Alma 50:24](https://bom-editions.vercel.app/en/1830/alma/50#24) should be "second"
- shew (91) - [1 Nephi 1:20](https://bom-editions.vercel.app/en/1830/1-nephi/1#20), [1 Nephi 15:17](https://bom-editions.vercel.app/en/1830/1-nephi/15#17), + 89 more should be "show"
- shewed (24) - [1 Nephi 11:31](https://bom-editions.vercel.app/en/1830/1-nephi/11#31), [1 Nephi 12:6](https://bom-editions.vercel.app/en/1830/1-nephi/12#6), + 22 more should be "showed"
- sheweth (2) - [2 Nephi 31:9](https://bom-editions.vercel.app/en/1830/2-nephi/31#9), [Jacob 4:7](https://bom-editions.vercel.app/en/1830/jacob/4#7) should be "showeth"
- shewn (26) - [1 Nephi 1:15](https://bom-editions.vercel.app/en/1830/1-nephi/1#15), [1 Nephi 1:18](https://bom-editions.vercel.app/en/1830/1-nephi/1#18), + 24 more should be "shown"
- shouldest (1) - [1 Nephi 21:6](https://bom-editions.vercel.app/en/1830/1-nephi/21#6) should be "shouldst" (technically this could also be called a variation of "should", but there are 10 "shouldst"s and only this singular "shouldest" which later got corrected to "shouldst")
- shublons (1) - [Alma 11:19](https://bom-editions.vercel.app/en/1830/alma/11#19) should be "shiblons" (a unit of currency)
- suredly (2) - [Alma 37:45](https://bom-editions.vercel.app/en/1830/alma/37#45), [Moroni 7:26](https://bom-editions.vercel.app/en/1830/moroni/7#26) should be "surely"
- swolen (1) - [1 Nephi 18:15](https://bom-editions.vercel.app/en/1830/1-nephi/18#15) should be "swollen"
- theit (1) - [Alma 24:18](https://bom-editions.vercel.app/en/1830/alma/24#18) should be "their"
- therefere (1) - [Alma 21:12](https://bom-editions.vercel.app/en/1830/alma/21#12) should be "therefore"
- therfore (2) - [Alma 17:25](https://bom-editions.vercel.app/en/1830/alma/17#25), [Mormon 1:15](https://bom-editions.vercel.app/en/1830/mormon/1#15) should be "therefore"
- thess (1) - [3 Nephi 18:12](https://bom-editions.vercel.app/en/1830/3-nephi/18#12) should be "these"
- threatnings (7) - [1 Nephi 18:17](https://bom-editions.vercel.app/en/1830/1-nephi/18#17), [Mosiah 19:3](https://bom-editions.vercel.app/en/1830/mosiah/19#3), + 5 more should be "threatenings"
- transgransgressions (1) - [Alma 9:19](https://bom-editions.vercel.app/en/1830/alma/9#19) should be "transgressions"
- treusures (1) - [Helaman 8:25](https://bom-editions.vercel.app/en/1830/helaman/8#25) should be "treasures"
- uncircumsised (1) - [Helaman 9:21](https://bom-editions.vercel.app/en/1830/helaman/9#21) should be "uncircumcised"
- understandding (1) - [2 Nephi 27:35](https://bom-editions.vercel.app/en/1830/2-nephi/27#35) should be "understanding"
- wat (1) - [3 Nephi 15:2](https://bom-editions.vercel.app/en/1830/3-nephi/15#2) should be "what"
- wherfore (1) - [Ether 13:18](https://bom-editions.vercel.app/en/1830/ether/13#18) should be "wherefore"
- whieh (1) - [Alma 59:10](https://bom-editions.vercel.app/en/1830/alma/59#10) should be "which"
- wildernsss (1) - [Ether 14:14](https://bom-editions.vercel.app/en/1830/ether/14#14) should be "wilderness"


## Unexpected technicalities
With the baseline of truth being the Webster's 1828 dictionary, these are words that are technically not proper, although today we may call these words correct.
- axe (4) - [2 Nephi 20:15](https://bom-editions.vercel.app/en/1830/2-nephi/20#15), [Enos 1:20](https://bom-editions.vercel.app/en/1830/enos/1#20), + 2 more (the Webster's 1828 dictionary spells this word "ax," but nowadays "axe" is still more common)
- cimeter(s) (11) - [Enos 1:20](https://bom-editions.vercel.app/en/1830/enos/1#20), [Mosiah 9:16](https://bom-editions.vercel.app/en/1830/mosiah/9#16), [Mosiah 10:8](https://bom-editions.vercel.app/en/1830/mosiah/10#8), + 8 more (the Webster's 1828 dictionary spells this word "cimiter", though today most people still consider "cimeter" correct)
- faggots (1) - [Mosiah 17:13](https://bom-editions.vercel.app/en/1830/mosiah/17#13) (the 1828 Webster's dictionary spells this word "fagot")
- havoc (1) - [Helaman 11:27](https://bom-editions.vercel.app/en/1830/helaman/11#27) the Webster's dictionary spells this "havock"
- miserable (6) - [2 Nephi 2:5](https://bom-editions.vercel.app/en/1830/2-nephi/2#5), [2 Nephi 2:18](https://bom-editions.vercel.app/en/1830/2-nephi/2#18), + 4 more (The Webster's dictionary spells this "miserabale," though this is not common today)



## Hyphenation
The following are words that either have a hyphen in them but shouldn't according to Webster's dictionary, or don't have a hyphen when they should according to Webster's dictionary:
- breast-plate(s) (11) - [Mosiah 8:10](https://bom-editions.vercel.app/en/1830/mosiah/8#10), [Alma 43:19](https://bom-editions.vercel.app/en/1830/alma/43#19), + 9 more
- breastwork (3) - [Mosiah 11:11](https://bom-editions.vercel.app/en/1830/mosiah/11#11), [Alma 53:4](https://bom-editions.vercel.app/en/1830/alma/53#4), + 1 more
- candlestick (1) - [3 Nephi 12:15](https://bom-editions.vercel.app/en/1830/3-nephi/12#15)
- day-time (1) - [Mosiah 18:5](https://bom-editions.vercel.app/en/1830/mosiah/18#5)
- ear-rings (1) - [2 Nephi 13:20](https://bom-editions.vercel.app/en/1830/2-nephi/13#20)
- evil-doer(s) (2) - [2 Nephi 19:17](https://bom-editions.vercel.app/en/1830/2-nephi/19#17), [2 Nephi 24:20](https://bom-editions.vercel.app/en/1830/2-nephi/24#20)
- eyewitness (2) - [3 Nephi 7:15](https://bom-editions.vercel.app/en/1830/3-nephi/7#15), [3 Nephi 7:15](https://bom-editions.vercel.app/en/1830/3-nephi/7#15)
- faint-hearted (1) - [2 Nephi 17:4](https://bom-editions.vercel.app/en/1830/2-nephi/17#4)
- head-bands (1) - [2 Nephi 13:20](https://bom-editions.vercel.app/en/1830/2-nephi/13#20)
- noon-day (1) - [1 Nephi 1:9](https://bom-editions.vercel.app/en/1830/1-nephi/1#9)
- priest-crafts (2) - [2 Nephi 10:5](https://bom-editions.vercel.app/en/1830/2-nephi/10#5), [2 Nephi 26:29](https://bom-editions.vercel.app/en/1830/2-nephi/26#29)
- seashore (24) - [1 Nephi 17:6](https://bom-editions.vercel.app/en/1830/1-nephi/17#6), [1 Nephi 17:6](https://bom-editions.vercel.app/en/1830/1-nephi/17#6), + 22 more
- selfsame (1) - [Alma 31:22](https://bom-editions.vercel.app/en/1830/alma/31#22)
- stiffnecked(ness) (21) - [1 Nephi 2:11](https://bom-editions.vercel.app/en/1830/1-nephi/2#11), [2 Nephi 25:28](https://bom-editions.vercel.app/en/1830/2-nephi/25#28) + 20 more
- storehouse (1) - [3 Nephi 24:10](https://bom-editions.vercel.app/en/1830/3-nephi/24#10)
- task-masters (2) - [Mosiah 24:9](https://bom-editions.vercel.app/en/1830/mosiah/24#9), [Mosiah 24:19](https://bom-editions.vercel.app/en/1830/mosiah/24#19)
- to-day (11) - [1 Nephi 10:18](https://bom-editions.vercel.app/en/1830/1-nephi/10#18), [2 Nephi 2:4](https://bom-editions.vercel.app/en/1830/2-nephi/2#4), + 9 more
- whirl-wind (1) - [3 Nephi 10:13](https://bom-editions.vercel.app/en/1830/3-nephi/10#13)


## British English
The following are words that are spelled correctly in British English but are not correct according to Webster's 1828 dictionary:
- armour(s) (7) - [1 Nephi 4:19](https://bom-editions.vercel.app/en/1830/1-nephi/4#19), [Mosiah 21:7](https://bom-editions.vercel.app/en/1830/mosiah/21#7), + 5 more
- baptise(d) (10) - [1 Nephi 10:9](https://bom-editions.vercel.app/en/1830/1-nephi/10#9), [1 Nephi 10:10](https://bom-editions.vercel.app/en/1830/1-nephi/10#10), + 8 more
- befal (1) - [Helaman 8:8](https://bom-editions.vercel.app/en/1830/helaman/8#8)
- centre (9) - [1 Nephi 16:2](https://bom-editions.vercel.app/en/1830/1-nephi/16#2), [Alma 31:13](https://bom-editions.vercel.app/en/1830/alma/31#13), + 7 more
- fulfil (20) - [1 Nephi 20:14](https://bom-editions.vercel.app/en/1830/1-nephi/20#14), [2 Nephi 6:12](https://bom-editions.vercel.app/en/1830/2-nephi/6#12), + 18 more
- levelled (1) - [Alma 51:18](https://bom-editions.vercel.app/en/1830/alma/51#18)
- lustre (2) - [1 Nephi 1:9](https://bom-editions.vercel.app/en/1830/1-nephi/1#9), [Mosiah 13:5](https://bom-editions.vercel.app/en/1830/mosiah/13#5)
- offence (4) - [2 Nephi 18:14](https://bom-editions.vercel.app/en/1830/2-nephi/18#14), [Alma 41:9](https://bom-editions.vercel.app/en/1830/alma/41#9), + 2 more
- realise (1) - [Mormon 3:3](https://bom-editions.vercel.app/en/1830/mormon/3#3)
- saviour (12) - [1 Nephi 10:4](https://bom-editions.vercel.app/en/1830/1-nephi/10#4), [1 Nephi 13:40](https://bom-editions.vercel.app/en/1830/1-nephi/13#40), + 10 more
- savour (1) - [3 Nephi 16:15](https://bom-editions.vercel.app/en/1830/3-nephi/16#15)
- sceptres (1) - [2 Nephi 24:5](https://bom-editions.vercel.app/en/1830/2-nephi/24#5)
- sepulchre (3) - [1 Nephi 19:10](https://bom-editions.vercel.app/en/1830/1-nephi/19#10), [Alma 19:1](https://bom-editions.vercel.app/en/1830/alma/19#1), + 1 more
- skilful (1) - [Alma 10:15](https://bom-editions.vercel.app/en/1830/alma/10#15)
- travelled (13) - [1 Nephi 2:5](https://bom-editions.vercel.app/en/1830/1-nephi/2#5), [1 Nephi 2:6](https://bom-editions.vercel.app/en/1830/1-nephi/2#6), + 11 more
- traveller (1) - [2 Nephi 1:14](https://bom-editions.vercel.app/en/1830/2-nephi/1#14)
- travelling (3) - [1 Nephi 16:33](https://bom-editions.vercel.app/en/1830/1-nephi/16#33), [Mosiah 23:35](https://bom-editions.vercel.app/en/1830/mosiah/23#35), + 1 more
- vapour (2) - [1 Nephi 19:11](https://bom-editions.vercel.app/en/1830/1-nephi/19#11), [3 Nephi 8:20](https://bom-editions.vercel.app/en/1830/3-nephi/8#20)
- wilfully (4) - [Mosiah 15:26](https://bom-editions.vercel.app/en/1830/mosiah/15#26), [3 Nephi 6:18](https://bom-editions.vercel.app/en/1830/3-nephi/6#18), + 2 more
- wilfulness (1) - [Moroni 9:23](https://bom-editions.vercel.app/en/1830/moroni/9#23)
