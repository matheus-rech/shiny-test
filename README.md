Shiny app for using LLMs to create Shiny apps
=============================================


## Prequisites

This is a Shiny for Python application, so you will need Python installed on your system.

Get an Anthropic API key from [Anthropic](https://console.anthropic.com/).

You can run this Shiny application locally on your computer, or you can deploy to a hosted service like [shinyapps.io](https://www.shinyapps.io/) (Posit's managed cloud hosting service) or your own server running [Posit Connect](https://posit.co/products/enterprise/connect/) (Posit's hosting platform which you run on your own server).


## Setup and usage

Install the required packages:

```
pip install -r requirements.txt
```


Create a file `.env` that contains your Anthropic API key:

```
ANTHROPIC_API_KEY="xxxxxxxxxxxxxxxxx"
```

You can also include these optional environment variables:

* `GOOGLE_ANALYTICS_ID` - Google Analytics ID to use for tracking page views. If provided, the Google Analytics tracking code will be included in the app.

Run the app locally:

```
shiny run app.py
```

## Meta-Analysis Functionalities

This repository now includes functionalities for meta-analysis in R. The main functionalities include:

* **Data input and management**: Upload and manage datasets for meta-analysis, including reading data from various file formats like CSV, Excel, etc.
* **Data preprocessing**: Handle missing values, data transformation, and outlier detection.
* **Meta-analysis methods**: Implement various meta-analysis methods, including fixed-effect and random-effects models, subgroup analysis, and meta-regression.
* **Statistical tests and measures**: Conduct statistical tests and calculate measures such as effect sizes, confidence intervals, and heterogeneity statistics.
* **Visualization**: Visualize the results of the meta-analysis, such as forest plots, funnel plots, and other relevant charts.
* **Reporting**: Generate comprehensive reports summarizing the results of the meta-analysis, including tables, figures, and textual descriptions.
* **User interface**: An intuitive and user-friendly interface for interacting with the assistant, including input widgets, output displays, and navigation elements.
* **Documentation and help**: Detailed documentation and help resources to guide users in using the assistant effectively.

## Deploying to a server

You can deploy this app to a server for others to access.

Learn about:

- Deploying to the cloud with [shinyapps.io](https://shiny.posit.co/py/docs/deploy-cloud.html)
- Deploying to a [self-hosted server]([https://shiny.posit.co/py/docs/deploy-on-prem.html])


Once you have your server set up, you can deploy the app with:

```
# Deploy (replace `gallery` with your server's nickname)
rsconnect deploy shiny -n gallery -t assistant .
```
