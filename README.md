# Assignment2 resubmission | Collecting Data 
## MA Digital Humanities | University of Groningen

### Ungaretti war poems corpus
The corpus comprises seven of the most well-known war poems by Giuseppe Ungaretti, a prominent Italian poet of the 20th century and one of the greatest representatives of the Hermetic movement. The poems are extracted from various collections published over a period of 15 years, all of which were integrated into “L’Allegria” (1931). 
The poet, who voluntarily participated in World War I, draws from personal experience and pours it into his works, which mainly reflect his torment and heartbreak, but also hope and resilience. 

This corpus is intended for Italian literature scholars and enthusiasts, as well as Digital Humanities academics and students, who wish to analyze a representative sample of Ungaretti’s war poems to yield valuable insights into his poetic expression and stylistic choices. An examination of the tokens and lemmas can, for instance, be combined with sentiment analysis to detect emotionally charged words and assess the emotional tone of each poem, enhanced by the use of minimalism. Parts-of-speech tags could, furthermore, reveal patterns in Ungaretti’s language choices, such as the predominance of personal pronouns or possessive adjectives, which suggest an intimate perspective due to his active participation in the war. Such investigations might also enable a comparative analysis with other war poets who may have employed different approaches due to their role as observers. 

### Data collection process
The texts were manually extracted from two distinct websites, https://www.italialibri.net/opere/poesiediguerra.html (“Veglia”, “Sono una creatura”, “San Martino del Carso”, “Soldati”) and https://lasottilelineadombra.com/2018/03/05/poesie-di-guerra-ungaretti/ (“Fratelli”, “In dormiveglia”, “Pellegrinaggio”). Subsequently, the content was transferred to TextEdit and converted into plain text (.txt) file format. 

### Cleaning and preprocessing steps
The only text cleaning operations performed were string replacement (str.replace()) and whitespace stripping (str.strip()), in order to remove line break characters and excess whitespace. 
As far as preprocessing steps, tokenization, lemmatization and parts-of-speech tagging were performed using spaCy. 
