# Terminology

Below is common terminology the lab uses when describing experiments.

## Describing an Experiment

Every experiment is defined using a _paradigm_, an _adjustment type_, a _response type_, and a _dependent measure_.

Experiments are further broken down into subdivisions called _conditions_. They are iterations on the same general experiment type with differences in things such as stimuli, balancing, or trial structure.

- **Condition**: Dictated by the task, the method(s) used, and the stimuli type.
- **Subcondition**: Individual experiment blocks containing a number of trials. Typically defined by a set of stable constants, demarked by independent variables.
- **Trial**: Marked by the user making a meaningful response/input that is purposely recorded.
    - E.g. I am trying to adjust the correlation of a specific plot to be the midpoint between a plot with a high correlation, and a plot with a lower correlation. The final correlation that I have adjusted marks the relevant trial data to be saved.

### Paradigms
According to Elliot et. al., "Paradigms are the specific visual tasks viewers complete when using a visualization." 

- **Classification**: Viewers identify a stimulus by categorizing it.  Viewers may classify an entire display, specific regions within a display, or objects.
- **Recognition**: Viewers indicate whether they saw a stimulus previously. A common example of this task is presenting a set of images, and then later presenting a second set of images composed of new images as well as ones from the original set.  Viewers then indicate which images in the second set is old or new.
- **Localization**: The viewer indicates the location of a stimulus.  Some examples could be: clicking where a stimulus previously was, or pressing a key to indicate which region of a screen contains an object of interest.
- **Detection**: Requires the viewer to indicate whether or not they perceive the presence of a stimulus.  Two common types of detection are visual search and change detection.
- **Rapid Serial Visual Presentation (RSVP)**: In the RSVP paradigm, viewers are shown a set of images quickly in a sequence, with at least one target image. Viewers then identify either the target image or target category (e.g. press the button when you see a positive correlation).
- **Matching**: The viewer adjusts one stimulus until it matches another. For instance, adjusting the size of a square until it has the same area as a rectangle also present on the screen.
- **Discrimination**: Viewers make comparative judgments about the magnitude of two stimuli, often side-by-side. For example: indicating which of two images has a higher total luminance.
- **Identification**: Viewers respond with the identity of the stimulus using open-ended answers.
- **Estimation**: Viewers directly estimate some value of a continuous feature in a display. Estimation paradigm experiments differ from the classification paradigm: where a viewer might classify a correlation as "low" or "steep", an estimation paradigm would require them to produce the magnitude numerically as "0.2" or "0.8".

### Adjustment Types

- **Method of Limits [MoL]**: The researcher steadily adjusts a property of a stimulus until it is seen or no longer seen by the participant.  For example, displaying white dots on a white background, and darkening them until they are perceptible.  This can be done either as ascending or descending, and it is not uncommon to see both within the same experiment.
- **Method of Adjustments [MoA]**: Similar to Method Limits, except it is the user who does the stimulus adjustments.  For instance, a user adjusting the brightness of dots until they are perceptible or imperceptible. 
- **Method of Constant Stimuli [MoCS]**: The researcher presents  viewers with random levels of a target property, and the user is asked to draw inferences.  From the previous examples, dots would be shown at various brightness levels, and the user indicates whether or not they are present or absent each trial.
- **Adaptive Psychophysical Procedures [APP]**: Researchers adjust visualizations for users based on their current performance relative to a threshold. A common APP used within the VCL Web Framework is staircasing, as seen in the JND experiment.  Users indicate which of two scatterplots is more correlated.  If the user responds correctly, the next pair of scatterplots have closer correlation values; if they respond incorrectly, the correlation values are farther apart. The adjustments continue until a steady-state criteria is met (e.g. 50% accuracy over _n_ trials).

### Response Types

- **Stimulus Level**: Users give direct reports indicating perceived values. For example, dragging a slider to indicate the average height of bars in a bar chart. Viewers can report stimulus levels verbally, by typing in a value, or visually by recreating the stimulus level.

- **2AFC**: Two-alternative forced-choice tasks give viewers two options of response after perceiving certain stimuli. For example, being shown two stimuli and asking users to indicate which one was darker. Two common choices for 2AFC are comparison and categorization.

- **NAFC**: The N-alternative forced-choice task is a scaled-up version of the 2AFC. For example, a 2AFC task might involve users indicating whether or not a chart matches a regression line 'yes' or 'no', while an NAFC might provide several charts and the user must choose one that matches.

### Dependent Measures

**Direct Dependent Measures**: A single number directly measuring how well people process visual information. Some examples:

- **Accuracy**: Measures how close to the true value are people's judgments. Measured in two ways: percentage correct (how often they get the answer right), and error (how close they were).
- **Response Time**: Measures how quickly a task with one stimulus is completed.
- **Precision**: The variability of participants' answers, measured as a threshold of performance, for example, the level of brightness at which a stimulus becomes visible. One of the most common of these is a just noticeable difference (JND), a threshold at which people can generally detect a difference.

**Model-Based Dependent Measures**: A model generated by factors such as (but not limited to) reaction time and accuracy.

- **Performance Slope**: Using accuracy or RT to model how these measures change as a function of the difficulty of the task. E.g. how quickly and accurately can a participant locate a target as the number of targets increases.
- **Psychometric Function**:  Models how performance changes (e.g., the number of correct or incorrect decisions) as a function of design (e.g. the luminance range of a colormap). 
- **Sensitivity & Bias Detection**:  Models performance as a function of sensitivity (change as the data or design changes) and bias (tendency to a certain response). 


### Properties 
- **Balancing**: the ways in which the subconditions for a given condition are ordered.
    - Random
    - Latin-Square
- **Graph Type**: e.g. scatter plots, ring plots, strip plots, shapes 
- **Graphical Manipulation**: 
    - May be on how the points are plotted e.g. for strip plots, a y coordinate defines the horizontal translation of the "strip" and x coordinate defines the height of the "strip".
    - May be in terms of how many distributions are plotted on the same graph e.g. on the same axes, we can have TWO scatter plots with different correlations.

---


## Condition Identifiers

Each condition is uniquely defined by 4 properties.

### Base Experiment

The experiment that the condition is an iteration of.

### Trial Structure

The trial structure represents the range or pattern of correlation values, and defines a set of constants for each subcondition. Each condition can follow these pattern of values, or use its own custom structure.

The two main types of patterns are Design or Foundational.

- **Foundational** : 17 subconditions, base correlation is in the range of `[0.0, 0.9]` in `0.1` increments.
- **Design**       : 15 subconditions, grouped into five sets of base correlation values set at `0.3, 0.6, 0.9`.
- **Estimation**
- **Custom**       : used when a condition does not follow any of the above structures.

### Balancing

How subconditions in a given condition get ordered.

- **Randomized** : Purely random.
- **Latin Square** : An _n_ &#215 _n_ array of _n_ different elements such that each element will occur exactly once in each column and once in each row.  For example, a 3 &#215 3 Latin Square would be ordered like this:

|  |  |  |
|---|---|---|
| C | A | B |
| B | C | A |
| A | B | C |

The objective of a Latin Square is to have participants with unique subcondition orderings.  Additionally, it helps control randomness in such a way that biases are reduced, e.g. subcondition _A_ is not randomly selected first at a disproportionate amount. 

### Graph Types

The type of graph used in the visualization.

- **Scatter** : Scatterplots.
- **Strip** : Strip plots.
- **Ring** : Ring plots.
- **Shapes** : Shapes appearing side by side.

### Attributes

Any given condition will always have a base, trial structure, balancing and graph type. However, they will also have a set of variables that manipulate different aspects of the distribution, graphical properties of the visualization, and non-graphical properties such as having a custom instruction set. 

Here is a non-comprehensive list of properties that could be manipulated by a condition.

- **Experimental attributes**:
    - Distribution type.
    - Base correlation of the reference plot.
    - Whether the correlation converges from above or below.
    - Complete list of experimental attributes [here](/VCLWebFramework/manual/supported_properties.html#experimental-attributes).
- **Graphical attributes**: 
     - Some examples if `plot type = scatter`:
        - Point shape
        - Point color
        - Point size
     - Some examples if `plot type = strip`:
        - Line length
        - Line width
     - Complete list of graphical attributes [here](/VCLWebFramework/manual/supported_properties.html#experimental-attributes).

---
Definitions adapted from:

Elliott, M. A., Nothelfer, C., Xiong, C., &amp; Szafir, D. A. (2021). A Design Space of Vision Science Methods for Visualization Research. _IEEE Transactions on Visualization and Computer Graphics_, 27(2), 1117–1127. <https://doi.org/10.1109/tvcg.2020.3029413> 

Pelli, D. G., & Farell, B. (2010). Psychophysical methods. In M. Bass, C. DeCusatis. J. Enoch, V. Lakshminarayanan, G. Li, C. MacDonald, V. Mahajan & E. V. Stryland (Eds.), _Handbook of Optics. Third Edition, Volume III: Visioo and Vision Optics_ (pp. 3.1-3.12). New York: McGraw-Hill. <https://denispelli.com/pubs/pelli2010methods.pdf>

---