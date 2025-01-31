# ZTF Summer School 2023
### Hosted hybrid by the University of Minnesota
#### July 24-28: 9 am - 12:30 pm (synchronous), group work in the afternoons (asynchronous)

Course materials for ZTF Summer School 2023

### Purpose

This course will introduce key concepts and techniques used to work with large datasets, in the context of the field of astrophysics. In the first 3 days of the course, the focus will be on the modern approaches to creating and manipulating large data sets, with the focus on time series analyses and Bayesian methods applied to astrophysics survey data. The remaining part of the course will focus on a range of machine learning techniques for processing data: classification algorithms (supervised and unsupervised learning), clustering algorithms, regression problems, recommender systems, graphic models and others. The algorithms will first be introduced in lectures, and the emphasis will then be placed on homework worked as teams in which the students will apply the algorithms (and already available packages) to astrophysical data sets to answer specific astrophysics questions. The course will assume familiarity with basic concepts in astrophysics, but it will include brief reviews as needed to demonstrate the use of modern data analysis techniques.

### Sample Syllabus

Day 1:
  * Talks: ZTF Introduction (Michael Coughlin), Searches for fast transients with ZTF (Igor Andreoni), Searches for Neutrino counterparts (Robert Stein)
  * Tutorials: Alert Stream Access, Fast transient case study

Day 2:
  * Talks: NMMA (Peter Pang), Multi-messenger Searches (Tomas Ahumada)
  * Tutorials: Bayesian inference, examples of using sncosmo / nmma
  * Outing: Bell Museum / Planetarium

Day 3:
  * Talks: BTS (Daniel Perley), BTSBot (Theophile Jegou Du Laz)
  * Tutorials: Training a BTS-like model
  * Outing: TURBO visit (Daniel Warshofsky)

Day 4:
  * Talks: Reinforcement Learning (Niharika Sravan), SCOPE (Brian Healy)
  * Tutorials: SCOPE case study

Day 5:
  * Talks: SEDM / SEDMv2 (Yashvi Sharma) 
  * Tutorials: Anomaly Detection

### How to use these materials

* Fork this repo

* The topics of each day's lectures are described in the schools' program

* Lectures are in directories named XY/ where XY/ is the number of the day

* Various help cheat sheets are included in help/. 

* You should also review in-class notebooks to make sure you understand what is happening

* The lecture notebooks have in-class exercises for you to work on

### Related Material

* UIUC Fundamentals of Data science: https://github.com/gnarayan/ast596_2023_Spring
* Caltech Astroinformatics: https://sites.astro.caltech.edu/ay119/
* GROWTH summer school: http://growth.caltech.edu/growth-school-2019.html
* AURA winter school: http://www.aura-o.aura-astronomy.org/winter_school/ - go to Past Years.
* YouTube Neural Networks: https://www.youtube.com/watch?v=aircAruvnKk
* UMN Big Data Astronomy: https://github.com/mcoughlin/ast8581_2023_Spring

### Github
If you are new to github, we recommend watching:
* https://www.youtube.com/watch?v=USjZcfj8yxE&ab_channel=ColtSteele
* https://www.youtube.com/watch?v=nhNq2kIvi9s&ab_channel=ColtSteele

### Environments
If running locally, we suggest using anaconda: https://anaconda.org/

If you are on windows, use the windows subsystem for linux:
https://docs.microsoft.com/en-us/windows/wsl/install-win10
plus the ubuntu anaconda.

After installing anaconda, you should (in a terminal):
 
* clone the repository: git clone https://github.com/mcoughlin/ztf_summer_school_2023.git
* change directories to the repository: cd ztf_summer_school_2022
* use conda to create an environment
  * on mac osx: conda env create -f environment-osx.yml
  * on linux / windows wsl: conda env create -f environment-ubuntu.yml

Activate the environment with:
* conda activate ztfsummer
(if you are running an older version of conda you may need):
* source activate ztfsummer
and can test by opening the first lecture:
* cd lectures/01
* jupyter notebook lecture01.ipynb

Either will, you will need to pip install:
* pip install git+git://github.com/colcarroll/minimc.git

Otherwise, google colaboratory will work:
https://colab.research.google.com/

Will need to create an IRSA account for data access:
https://irsa.ipac.caltech.edu/frontpage/

# ZTF useful links + QA
| Question  | Answer |
| ------------- | ------------- |
| ztfquery documentation  | https://github.com/MickaelRigault/ztfquery  |
| ZTF table content  | https://irsa.ipac.caltech.edu/onlinehelp/ztf/overview.html  |
| Alerts content  | https://zwickytransientfacility.github.io/ztf-avro-alert/schema.html |
|What is the  "Redshift Completeness Factor" program? | It's a program dedicated to determine the number of SN host galaxies with known spectroscopic redshift prior to  the SN discovery divided by the total number of SN hosts. See https://arxiv.org/abs/1910.12973 |
|What is the  "Census of the Local Unverse" program? | The Census of the Local Universe (CLU) aims to provide a galaxy catalog out to 200 Mpc that is as complete as possible. See https://arxiv.org/abs/1710.05016 |
|How is the time allocation for each filter decided? | ZTF uses a Integer Linear Programming approach, that optimizes an observing plan for an entire night by assigning targets to temporal blocks, enables strict control of the number of exposures obtained per field and minimizes filter changes. See https://arxiv.org/abs/1905.02209 |
