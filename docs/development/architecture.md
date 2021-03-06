# Architecture

## Flow Diagram

![Flow Diagram](image/flow_diagram.png)

Due to the COVID-19 pandemic, our team felt increasing urgency in implementing a version of the framework that was ready for running experiments online. We ended up deploying online with Heroku with Cloud Firestore as the database, and Prolific for the participant hub. This required major feature changes such as routing, resolution scaling, screening tasks. 

[Detailed documentation](https://docs.google.com/document/d/1221pq6_ehmMGN0F6CGLEhbQOaf9zoMEsmH3cXxXPJgs/edit?usp=sharing)


## Experiment Application Architecture

![Experiment Application Architecture](image/application_architecture.png)

Experiments are displayed on the browser (client) with a URL created by Heroku (<a href="https://vcl-web.herokuapp.com" target="_blank">https://vcl-web.herokuapp.com</a>).

## Sequence Diagram

![Sequence Diagram](image/sequence_diagram.png)