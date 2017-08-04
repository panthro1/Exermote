# Exermote Preprocessing and Training

After collecting labeled data, a model needs to be trained!

**Preprocessing**

There were a few preprocessing steps I made. Some of them are rooted in insights I had, when I was already training models:

- merging raw recordings to one file
- reducing total number of classes from 5 to 4, by converting "set break" to "break". I don't know what I was thinking when introducing two different break classes...
- converting the first and last two time steps of every squat repetition to "break". Earlier models often counted squats, when I actually didn't do anything. This fixed it.


**Choosing a model**

I intended to write my master thesis in human activity recognition (HAR), but I didn't find a supervisor. Anyway I could use some of the insights from my <a href="https://github.com/Lausbert/Exermote/blob/master/ExermotePreprocessingAndTraining/MasterThesisProposal/master%20thesis%20proposal.pdf">thesis proposal</a>. The following table is an excerpt from this proposal.

<p align="center">
<img src="https://github.com/Lausbert/Exermote/blob/master/ExermotePreprocessingAndTraining/MasterThesisProposal/Bildschirmfoto%202017-08-04%20um%2014.55.17.png">
</p>

As you can see in the last row DeepConvLSTM Neural Networks were already tested by Francisco Javier Ordóñez and Daniel Roggen for recognizing activities of daily living. Their <a href="https://github.com/sussexwearlab/DeepConvLSTM">approach</a> and their <a href="http://www.mdpi.com/1424-8220/16/1/115/html">results</a> impressed me and so I decided to take their model and give it a try for my purpose.