# NMT - Neural Machine Translator

## Introduction

Lets say you have gone to a place, where you don't know the language, but see a sign board, having words in that new language, you know which language that is but, don't understand or speak of it. 
<p align="center">
  <img src="https://github.com/nischaygowda105/Neural-Machine-Translator/blob/master/output.gif">
</p>   

<p align="center">
French - English Translation
</p>                           

**Google translate** comes to in handy, it scans the unknown sentence as input to give out a translated sentence of your choice of language. Impressive isn't it.

## **How is it Done ?**

![https://media.giphy.com/media/3og0IPCChsknyJA17q/giphy.gif](https://media.giphy.com/media/3og0IPCChsknyJA17q/giphy.gif)

Source - [Giphy][http://gph.is/2oJMBy3](http://gph.is/2oJMBy3) 

## Steps involved.

### Word to data translation.

1. Tranform sentences to data format inputtted to ML model. we must convert our textual data into numeric form.
2. Each word is trnsformed inot a **one hot encoding vector** which can be inputted into model.
3. Vector having 0 at evry index except for 1 at index corresponding to that word.
4. We are creating a vocabulary for each langauge, consisting of most common used words.
5. Form mini vocabulary table, then converting the words in sentences to one hot encoded forms. **Vocabulary created for both Input and Output languages** .

### Encoder Decoder

1. **Encoder** portion takes the sentences from input language and creates ***thought vector*** from this sentence.
2. ***Thought vector**  recognizes the features, meaning and context of the source sentences.*
3. ***Thought vector*** is subsequently passed to **Decoder** which outputs the translation of sentence in output language.

### Encoder

1. Each word in input sentence is fea individual to the model in number of consecutive steps.
2. At each time **t**, model updates a hiddent vector **h**, using information from word inputted to model at that time-step.
3. At first step of Encoding, since no words have yet been inputted to the Encoder at time-step t=0, the hidden state in the Encoder starts out as an empty vector at this time-step.
4. At each time step, this **hidden vector** takes the input information at that particular time step, preserving the information from previous time step.
5. Thus at final time step, meaning of the whole sentence is stored in hidden vector. This hidden at fina step is ***'thought vector'***.

### Decoder

1. The final hidden state is the initial hidden vector for the **Decoder**.
2. Now, Decoder outputs a translated output of the hidden vectors at eacj time step.
3. So, output is word prediction at that given time-step, until it output the entire sentence.

What to try it on your own.  Link to my GitHub repository. Much of the code is taken from 

Feel free to hit that claps, See you guys soon with another one.
