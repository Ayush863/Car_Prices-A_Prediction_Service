# Car Prices-An AI enabled prediction service
![New Data1](https://user-images.githubusercontent.com/57457066/202673095-a4cca876-d47a-4f0b-93c7-884cd4006acf.png)
Using web scraped data from one of India's largest car website, Cardekho, building a prediction service with **Feature**, **Training** and **Inference pipelines** for continous prdictions on prices of used cars in India.
> A Forbes study (March 2016) finds that Data Scientists spend less than 4 percent time on model selection and refining algorithms. This project builds on that and has a data centric approach to it, rather than a conventional model centric approach.

## CI Workflow
The github workflow triggers two ipynb notebooks, Feature and Inference Pipelines. The feature pipeline works in normal mode (backfill = False), and adds a random sample from the holdout set to the feature group. The Batch Inference then runs on this sample and returns the predictions. This prediction is logged to github pages website.

## Project Layout
There are three files for experimentation and logging. First, the data cleaning notebook, then the Exploratory Data Analysis(EDA) file and finally a model selection notebook.
Then there are three pipelines: **Feature pipeline**, **Training pipeline** and **Inference pipeline**. The training pipeline is run on demand, as there is any accountable data drift. Feature and Inference pipelines are run on a schedule(as of Nov 2022, once every day).

### Acknowledgements:
This project uses the Hopsworks Feature store and github actions, I'd like to thank them for the free resources. 
A lot of my Machine and Deep Learning knowledge comes from either Andrew NG's Deeplearning.ai, Fastai's Jeremy Howard, Swayam lectures and my university professors. I'd like to thank them as well. Finally and the most important, the Serverless ML course (available for free on youtube) by Jim Dowling, CEO Hopsworks helped me a lot in completing this project.
