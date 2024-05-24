# Development of the lyrics-based deep learning algorithm for identifying alcohol-related words (LYDIA)

**Citation**: Abraham Albert Bonela, Zhen He, Dan-Anderson Luxford, Benjamin 
Riordan,
Emmanuel Kuntsche, Development of the lyrics-based deep learning algorithm for identifying alcohol-related words (LYDIA), Alcohol and Alcoholism, Volume 59, Issue 2, March 2024, agad088, https://doi.org/10.1093/alcalc/agad088

## Lyrics Dataset

This dataset has the following structure that includes essential files and 
folders required to train a classification model.

Structure:
1. Lyrics Data
2. MergedPreprocessedAnnotationData.csv
3. FilenamesAndIndices.csv
4. KeywordsFinal3.1.xlsx

**Lyrics Data**: This folder contains all the song lyrics of top-100 songs 
across the years 1959 to 2020. The song lyrics are grouped by year. Each 
year may have at least 100 songs (in some years there are fewer number of 
song lyrics) and at most slightly greater 100 (indicating ties about the 
ranks of songs). Lyrics for each song is stored in two file formats: json 
and txt. You may use the .json format files as they are updated with 
correct lyrics.

**MergedPreprocessedAnnotationData.csv**: This file contains all the 
annotations for each occurence of alcohol keywords in this above lyrics 
corpus. 

This file contains 5 columns:
1. fileIndex
2. lineIndex
3. word
4. wordLabel
5. wordContext

_fileIndex_: Represents the index of the lyrics file corresponding to the 
corpus.

_lineIndex_: Represents the line number of the lyrics file in which there is an
occurrence of alcohol keyword

_word_: Represents the alcohol keyword

_wordLabel_: Represents the annotated label (alcohol-relation) of the 
alcohol keyword for that occurrence. Each keyword corresponds to one of the 
three categories: alcohol-related, non-alcohol related, or unsure. 
    
    Label "0" represents --> non-alcohol-related
    Label "1" represents --> alcohol-related
    Label "0" represents --> unsure


_wordContext_: Represents the annotated label (alcohol-related-context) of the 
alcohol keyword for that occurrence. Each keyword corresponds to one of the 
three categories: positive, negative, or neutral.
    
    Label "0" represents --> neutral
    Label "1" represents --> positive
    Label "-1" represents --> negative

**FilenamesAndIndices.csv**: This file contains the fileIndex which 
corresponds to the song lyrics file in the corpus.

This file contains 3 columns:
1. fileIndex
2. filenames
3. year

_fileIndex_: Represents the index of the lyrics file in the corpus.

_fileName_: Represents the name of the lyrics file in the corpus.

_year_: Represents the year in which the song was released.

**KeywordsFinal3.1.xlsx**: Represents the alcohol keywords that were 
manually scraped by the annotators from various sources including academic 
research articles, and Wikipedia.

For more information please refer to the above citation or the below link to 
the [published paper](https://doi.org/10.1093/alcalc/agad088).

It would be highly appreciated if you can cite this article when you use this dataset 
for your research or commerial purposes. 