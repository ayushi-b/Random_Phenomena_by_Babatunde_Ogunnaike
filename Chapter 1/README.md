# Notes for Chapter 1

`Also contains some important points from Chapter 0.`

<br>

A process whose outcome is uncertain even if the input and other required conditions are essentially the same is called a **random phenomena** (also called a *non-deterministic* process).

**For example:** <br/>
Let us suppose we perform a chemical experiment several times to calculate the improvement in yield by using some Process A and that the experiment is performed under essentially the same conditions every time. Now, if the process results in the same value for yield each time, it will be called a deterministic process. If however, the values observed are not the same, they vary every time, it is a random process.

*Most of the processes we deal with in practical life are random in nature. Thus, we need to study random phenomena and analyze them so as to be able to make sense out of them.*

<br>

### **A Motivating Example**
____

`Note: There are two motivating examples in the book – One for continuous data (the one included in these notes) and the other one for discrete data. I left the discrete one out as the concepts are same and apply directly to it.`

We can easily solve problems related to deterministic process. Like if we want to compare which of the two Processes A or B is better (given deterministic experiment results), we can simply compare the values and say that the one with higher yield result is better. Though this does not happen in real life. The actual results look something like this:

<br>
<table><tr><td><img src = "media/table1_1.png" width=300></td></tr></table>

<br>
 
Here, sometimes Y<sub>A</sub> is greater than Y<sub>B</sub> and sometimes it is smaller. The results of the 2 processes are uncertain. We cannot simply compare these values and determine which process is better.

The intuition of a good scientist or engineer will suggest using the concept of the “arithmetic average” to represent the processes and compare based on those values.  Let us represent the average yield value for Process A by µ<sub>A</sub> and that for Process B by µ<sub>B</sub>.

µ<sub>A</sub>  =  75.52

µ<sub>B</sub>   =  72.47

Averages implies that Process A is better than Process B by 3.05%. There are a few important questions and points to consider though :
1. The variability of individual values of the data around the average value is noticeable. How confident then are we in preferring Process A over B, based on the computed averages? (For example, there are some 8 values where Y<sub>B</sub> > µ<sub>A</sub>; what should we make of this fact?)
2. Will it (or should it) matter that

    72.30 < Y<sub>A</sub> < 79.07

    67.33 < Y<sub>B</sub> < 78.41

    so that the observed data are seen to vary over a range of yield values that is 11.08 units wide for Process B as opposed to 6.77 for A? The averages give no indication of these extents of variability.
3. More fundamentally, is it always a good idea to work with averages? How reasonable is it to characterize the entire data set with the average?
4. If new sets of data are gathered, the new averages computed from them will almost surely differ from the corresponding values computed from the current set of data shown here. Observe therefore that the computed averages µ<sub>A</sub> and µ<sub>B</sub> are themselves clearly subject to random variability. How can we then be sure that using averages offers any advantages, since, like the original data, these averages are also not free from random variability?
There is a lot more to dealing with this example problem than merely using the intuitively appealing notion of averages.
 
<br>

### **Group Classification and Frequencies**
____


Instead of focusing on individual observations as presented in the tables of raw data, what if we sub-divided the observations into small groups (called “bins”) and re-organized the raw data in terms of how frequently members of each group occur?

This reclassification indicates, for instance, that for Y<sub>A</sub>, there is only one observation between 71.51 and 72.50 (the actual number is 72.30), but there are 17 observations between 74.51 and 75.50; for Y<sub>B</sub> on the other hand, 3 observations fall in the [67.51-68.50] group whereas there are 8 observations between 69.51 and 70.50. 

<br>
<table>
    <tr>
        <td>
        <img src = "media/table1_3.png" width=300>
        </td>
        <td>
        <img src = "media/fig12_8.png" width=400>
        </td>
    </tr>
    <tr>
        <td>
        <img src = "media/table1_4.png" width=300>
        </td>
        <td>
        <img src = "media/fig1_2.png" width=400>
        </td>
    </tr>
</table>

<br>

The “relative frequency” column indicates what proportion of the original 50 data points are found in each group. A plot of this reorganisation of the data, known as the **histogram**.

A key advantage of such a representation is how clearly it portrays the nature of the variability associated with each variable. For example, we easily see from Fig 12.8 that the “center of action” for the Y<sub>A</sub> data is somewhere around the group whose bar is centered around 75 (i.e. in the interval [74.51, 75.50]). Furthermore, most of the values of Y<sub>A</sub> cluster in the 4 central groups centered around 74, 75, 76 and 77. In fact, 41 out of the 50 observations, or 82%, fall into these 4 groups; groups further away from the center of action (to the left as well as to the right) contribute less to the Y<sub>A</sub> data. <br>
Similarly, Fig 1.2 shows that the “center of action” for the Y<sub>B</sub> data is located somewhere around the group in the [71.51, 72.50] interval but it is not as sharply defined as it was with Y<sub>A</sub>. Also the values of Y<sub>B</sub> are more “spread out” and do not cluster as tightly around this central group.

The histogram also provides quantitative insight. For example, we see that 38 of the 50 Y<sub>A</sub> observations (or 76%) are greater than 74.51; only 13 out of the 50 Y<sub>B</sub> observations (or 26%) fall into this category. Also, exactly 0% of Y<sub>A</sub> observations are less than or equal to 71.50 compared with 20 out of 50 observations (or a staggering 40%) of Y<sub>B</sub> observations. 

Thus, if these data sets can be considered as representative of the overall performance of each process, then it is reasonable to conclude, for example, that there is a better chance of obtaining yields greater than 74.50 with Process A than with Process B (a 76% chance compared to a 26% chance). Similarly, while it is highly unlikely that Process A will ever return yields less than 71.50, there is a not-insignificant chance (40%) that the yield obtained from Process B will be less than 71.50.
 
*A fundamental tenet of the probabilistic approach to dealing with randomly varying phenomena is an abandonment of the individual observation as the basis for theoretical characterization, in favor of an ensemble description.*
 
How can the benefits of the histogram be consolidated into a useful tool for quantitative analysis of randomly varying phenomena? The answer: by appealing to a fundamental axiom of random phenomena: that **conceptually, as more observations are made, the shape of the data histogram stabilizes, and tends to the form of the theoretical distribution that characterizes the random phenomenon in question, in the limit as the total number of observations approaches infinity.**
 
<br>

### **Certainty in Uncertainty:**
____

Even though the above example is non-deterministic in nature, we were still able to perform quantitative analysis on it. For example - We cannot say with certainty what the yield result will be if the experiment is performed one more time, but we can say that there are 94% chance of  Y<sub>A</sub> > 73.5 and only 38% chances of  Y<sub>B</sub>  > 73.5.

Conversely, there is some certainty in random - uncertain outcomes too.


The following points can be stated for a random phenomena:
1. If characterized properly, random phenomena are subject to rigorous mathematical analysis in much the same manner as deterministic phenomena.
The unpredictable irregularities of the individual observations (or, more generally, the “detail”) of random phenomena in fact co-exist with surprisingly predictable ensemble, or aggregate, behavior. This fact makes rigorous analysis possible.
2. The ensemble (or aggregate) characterization provided by ideal probability models can be used successfully to develop the theoretical basis for solving real problems where one is always limited to dealing with an incomplete collection of individual observations—never the entire aggregate.
 A key defining characteristic of random phenomena is that specific outcomes or observations cannot be predicted with absolute certainty. With probabilistic analysis, this otherwise “impossible task” of predicting the unpredictable individual observation or outcome is simply replaced by the analytical task of determining the mathematical probability of its occurrence.

There is a pattern hidden inside random data that can be approximated with statistical approaches. This forms the basis for the modern day Machine Learning methods.