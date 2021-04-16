# Terminology

Below is common terminology the lab uses when describing experiments.

## Describing an Experiment

Every experiment has the following attributes:

- **Experiment** : the type of task to be performed, defined using a paradigm, an adjustment type, a response type, and a dependent measure.
- **Condition** : dictated by the task, the method(s) used, and the stimuli type.
- **Subcondition** : a set of stable constants.
- **Trial** : marked by the user making a meaningful response/input that is purposely recorded.
    - E.g. I am trying to adjust the correlation of a specific plot to be the midpoint between a plot with a high correlation, and a plot with a lower correlation. The final correlation that I have adjusted marks the relevant trial data to be saved.
- **Action** : the actions a user can make within a trial.
    - E.g. In the above trial example, I can be taking actions to increase or decrease my correlation.

### Paradigms
According to Elliot et. al., "Paradigms are the specific visual tasks viewers complete when using a visualization." 

- **Classification**
- **Recognition**
- **Localization**
- **Detection**
- **Rapid Serial Visual Presentation (RSVP)**
- **Matching**
- **Discrimination**
- **Identification**
- **Estimation**

### Adjustment Types

- **Method of Limits**
- **Method of Adjustments**
- **Method of Constant Stimuli**
- **Adaptive Psychophysical Procedures**

### Response Types

### Dependent Measures

### Properties 
- **Balancing** : the ways in which the subconditions for a given condition are ordered.
    - Random
    - Latin-Square
- **Graph Type** : e.g. scatter plots, ring plots, strip plots, shapes 
- **Graphical Manipulation**: 
    - May be on how the points are plotted e.g. for strip plots, a y coordinate defines the horizontal translation of the "strip" and x coordinate defines the height of the "strip".
    - May be in terms of how many distributions are plotted on the same graph e.g. on the same axes, we can have TWO scatter plots with different correlations.


---
Definitions adapted from:

Pelli, D. G., & Farell, B. (2010). Psychophysical methods. In M. Bass, C. DeCusatis. J. Enoch, V. Lakshminarayanan, G. Li, C. MacDonald, V. Mahajan & E. V. Stryland (Eds.), _Handbook of Optics. Third Edition, Volume III: Visioo and Vision Optics_ (pp. 3.1-3.12). New York: McGraw-Hill. <https://denispelli.com/pubs/pelli2010methods.pdf>


## Condition Identifiers

Each condition is uniquely defined by 4 properties.

### Base Experiment

Defines the underlying procedural logic of the experiment.

- JND
- Stevens
- Estimation
- Numerosity
- Visual Search
- Ensemble Average

### Trial Structure

The trial structure represents the range or pattern of correlation values, and defines a set of constants for each subcondition. Each condition can follow these pattern of values, or use its own custom structure.

The two main types of patterns are Design or Foundational.

- **Foundational** : 17 subconditions, base correlation is in the range of `[0.0, 0.9]` in `0.1` increments.
- **Design**       : 15 subconditions, grouped into five sets with base correlation values set at `0.3, 0.6, 0.9`.
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

### Graph Types

The type of graph used in the visualization.

- **Scatter** : Scatterplots.
- **Strip** : Strip plots.
- **Ring** : Ring plots.
- **Shapes** : Shapes appearing side by side.

### Attributes

Any given condition will always have a base, trial structure, balancing and graph type. However, they will also have a set of variables that manipulate different aspects of the distribution, graphical properties of the visualization, and non-graphical properties such as having a custom instruction set. 

Here is a non-comprehensive list of properties that could be manipulated by a condition.

- Experimental attributes:
  - Distribution type.
  - Base correlation of the reference plot.
  - Whether the correlation converges from above or below.
  - Complete list of experimental attributes [here](/VCLWebFramework/manual/supported_properties.html#experimental-attributes).
- Graphical attributes: 
   - Some examples if `plot type = scatter`:
      - Point shape
      - Point color
      - Point size
   - Some examples if `plot type = strip`:
      - Line length
      - Line width
   - Complete list of graphical attributes [here](/VCLWebFramework/manual/supported_properties.html#experimental-attributes).