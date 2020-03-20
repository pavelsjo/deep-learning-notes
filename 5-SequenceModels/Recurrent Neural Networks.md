# NLP Basics

## Word Representation

```python
#People's name detection
#Single sentence
sentence = "Harry Potter and Hermione Granger invented a new spell"

#Vector representation, example for Tx == Ty
X = [words for words in sentence.lower().split()] #Index X[0] to X[Tx]
Y = [1, 1, 0, 1, 1, 0, 0, 0 ,0] #Index Y[0] to Y[Ty]

#NOTE: Tx and Ty could be distinct
```

For differents training examples:

- X(i)<T> ------> Tx(i) #Tx represents the Lenght of the sequence for `i` example of X
- Y(i)<T> ------> Ty(i)

## Individual words representation

```python
#In the example Andrew represents a 10.000 size vocabulary for ILUSTRATION
Vocabulary = [
    'a', #1
    'aaron', #2
    'and',
    'harry',
    'potter', #6
    'and',
    'hermione',
    'granger',
    'invented',
    'new',
    'spell',
    'zulu'] #Size 12
```

Vocabulary size references:

- `30.000` to `50.000`
- `1.000.000`

Vocabulary options:

- Make one from most commons words of the training set
- Download a online dictionary

## One Hot Representation

This notation means, make a vector with vocabulary size and place `1` in the word position and `0` for others. So, for this example using the previous sentence:

```python
#example
sentence = "Harry Potter and Hermione Granger invented a new spell"

#one hot representation
X_0 = [0,0,0,0,1,0,0,0,0,0,0,0] #related to harry position in vocabulary
X_1 = [0,0,0,0,0,1,0,0,0,0,0,0] #related to harry position in vocabulary
#etc
```
