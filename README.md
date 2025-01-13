# Assignment2 resubmission | Collecting Data 
## MA Digital Humanities | University of Groningen

### Ungaretti war poems corpus
The corpus comprises seven of the most well-known war poems by Giuseppe Ungaretti, prominent Italian poet of the 20th century and one of the greatest representatives of the Hermetic movement, expanded with six exemplary poems from the English literary movement known as War Poetry. As for Ungaretti, the works are extracted from various collections published over a period of 15 years, all of which were integrated into “L’Allegria” (1931). The poet, who voluntarily participated in World War I, draws from personal experience and pours it into his works, which mainly reflect his torment and heartbreak, but also hope and resilience. 
The English poems belong to three renowned authors: Siegfried Sassoon, Wilfred Owen, and Isaac Rosenberg, all of whom were also active participants in the war, and offer their perspectives on the conflict shaped by personal testimony. 

This corpus is intended for Italian or comparative literature scholars and enthusiasts, as well as Digital Humanities academics and students, who wish to analyze a representative sample of Ungaretti’s war poems to yield valuable insights into his poetic expression and stylistic choices. An examination of the tokens and lemmas can, for instance, be combined with sentiment analysis to detect emotionally charged words and assess the emotional tone of each poem, enhanced by the use of minimalism. Parts-of-speech tags could, furthermore, reveal patterns in Ungaretti’s language choices, such as the predominance of personal pronouns or possessive adjectives, which suggest an intimate perspective due to his active participation in the war. 

The corpus expansion, which includes the same preprocessing steps, was added to suggest a potential type of comparative analysis. The latter may enable an investigation into the similarities and differences in the narratives of the wartime experiences lived by soldiers from different countries, interpreted through diverse styles, yet united by a shared disillusionment regarding the glorification of war. 

### Data collection process
The texts were manually extracted from distinct websites: https://www.italialibri.net/opere/poesiediguerra.html (“Veglia”, “Sono una creatura”, “San Martino del Carso”, “Soldati”) and https://lasottilelineadombra.com/2018/03/05/poesie-di-guerra-ungaretti/ (“Fratelli”, “In dormiveglia”, “Pellegrinaggio”), https://www.poetryfoundation.org/ ("August 1914", "Dulce et Decorum Est", "Break of Day in the Trenches", "Anthem for Doomed Youth"), and https://allpoetry.com/ ("Survivors", "Suicide in the Trenches"). Subsequently, the content was transferred to TextEdit and converted into plain text (.txt) file format. 

### Cleaning and preprocessing steps
The only text cleaning operations performed were string replacement (str.replace()) and whitespace stripping (str.strip()), in order to remove line break characters and excess whitespace. 
As far as preprocessing steps, tokenization, lemmatization and parts-of-speech tagging were performed using spaCy, employing the suitable language model in accordance with the processed textual data.  

### Annotations
Additional columns (“Title”, “Author”, “First Collection”, “First Publication Year”, "Second Collection", "Second Publication Year") were annexed to the initial dataset by merging it with a secondary table using spaCy. The same tool was later employed to perform named entity recognition, adding a column with named entity tags and one with the words and phrases identified as named entities (“Named_Entities”, “NE_Words”). However, the NER system often failed to accurately categorize words into their respective entities, likely due to the limitations of the small model employed. 
At the end of the code execution, the dataset was saved in a CSV format. 

### CSV file description 
The CSV file contains the following columns: 

| Variable name | Description |
| ----------------------- | ------------------------------------------------------------------------------------------ |
| Filename                | The original .txt file name                                                                |
| Title                   | The poem’s title                                                                           |
| Author                  | The author of the poem                                                                     |
| First Collection        | The collection where the poem was first published                                          |
| First Publication Year  | Year of the first (or only) collection's publication                                       |
| Second Collection       | The second published collection, gathering all of the author's war poems (if applicable)   |
| Second Publication Year | Year of the second collection's publication (if applicable)                                |
| Document                | The original, unprocessed, text                                                            |
| Text                    | The full cleaned text                                                                      |
| Tokens                  | Individual words of each poem                                                              |
| Lemmas                  | Base form of each token                                                                    |
| POS                     | Parts-of-speech tags categorizing each word                                                |
| Named_Entities          | Named entities categories                                                                  |
| NE_Words                | The words associated with named entities                                                   |
