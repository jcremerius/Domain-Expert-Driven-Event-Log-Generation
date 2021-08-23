# Domain-Expert-Driven-Event-Log-Generation

This repository contains the programmatical evaluation of the paper "Domain Expert Driven Event Log Generation". We provide a [jupyter notebook](https://jupyter-notebook.readthedocs.io/en/stable/#) in `MIMIC_analyses_processes.ipynb` that generates event logs from the [MIMIC-IV](https://mimic.mit.edu/docs/iv/) data warehouse. An overview of the tables of the MIMIC-IV data warehouse can be found in `Class_diagram_MIMIC_IV.pdf`.

To run the event log generation, [access to the MIMIC-IV data warehouse](https://mimic.mit.edu/docs/gettingstarted/) is needed.
It can then be run via the console or by using e.g. the [Anaconda navigator](https://www.anaconda.com/products/individual).
After getting access to MIMIC-IV, it is possible to download the data tables and import them in the notebook. The generated event logs can be visualized with e.g. [Disco](https://fluxicon.com/disco/) or [ProM Tools](https://www.promtools.org/doku.php).

In the paper, we proposed a feature request based, iterative event log generation. Domain experts define feature requests for the to be generated event log. Based on that, process mining experts generate the event log. This event log can then be investigated. It can either be satisfying or needs improvement. If the second is the case, new feature requests will be defined and a new event log is generated.

<img width="900" alt="image" src="https://user-images.githubusercontent.com/32839252/130455867-bae09bcd-27e6-448c-ab6e-82154f8565ab.png">

We provide an implementation of the three steps *Event Extraction*, *Event Correlation*, and *Event Abstraction*. Our jupyter notebook takes the MIMIC-IV data warehouse as input and outputs an event log. By changing and extending the implementation, feature requests can be realized.
