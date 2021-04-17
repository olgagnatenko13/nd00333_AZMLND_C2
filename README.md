## Project Overview 

This project is part of the Udacity Azure ML Nanodegree.

The purpose of this project is to configure, build, deploy and consume a cloud-based machine learning production model, both manually in AzureML Studio and automatically via a pipeline. 

The project uses the details about the clients of direct marketing campaigns of a Portuguese banking institution to determine if the clients are likely to subscribe to a bank term deposit. The dataset contains various information about the client: demographic variables, presence of loans, last contact details, outcome of the previous marketing campaign, employment and consumer information. Detailed description of the variables can be found here: https://archive.ics.uci.edu/ml/datasets/Bank+Marketing 

**Problem statement**: using the information about the client, assess whether the client will subscribe to a bank term deposit or not. The purpose of this analysis is to identify the most relevant clients for next marketing steps, and to increase bank profit by offering the term deposit product to the proper audience. 

The client will consume the model by sending client details, and receiving a response "yes" or "no" indicating that the client is either likely to subscribe to the rerm deposit or not. 

## Architectural Diagram 

![Architectural diagram](project_architecture.png)

## Future Improvements

Two important improvements to the project in the future are:
- learning on new data to avoid data drift
- consuming expert feedback to improve the model

Every model should be refined and updated in the course of time. By consuming additional training data and updating the model, we can ensure that the model provides relevant results. It would be efficient to automate this process as a pipeline.

Clients can also provide feedback on the data points they consumed and on the actual customer response. Based on this feedback, the model can be further improved and refined. 

## Project Main Steps and Screenshots

### Step 2. AutoML experiment

1. Registered datasets

![Registered datasets](screenshots/2_1_registered_datasets.png)

2. Experiment is shown as completed

![Experiment is shown as completed](screenshots/2_2_completed_experiment.png)

3. Best model 

![Best model - screen 1](screenshots/2_3_best_model_1.png)

![Best model - screen 2](screenshots/2_3_best_model_2.png)

### Step 3. Deploy the best model 

1. Select the best model for deployment

![Select the best model for deployment](screenshots/3_1_model_deployment_settings.png)

2. Deploy the model and enable authentication 

![Deploy the model and enable authentication](screenshots/3_1_model_deployment_settings.png)

3. Deploy the model using Azure Container Instance 

![Deploy the model using Azure Container Instance](screenshots/3_2_deployment_completed.png)

### Step 4. Enable Application Insights

1. "Application Insights" enabled for the endpoint

!["Application Insights" enabled for the endpoint](screenshots/4_1_application_insights_enabled.png)

2. Logs produced by running logs.py script

![Logs produced by running logs.py script](screenshots/4_2_logs_output.png)

### Step 5. Swagger documentation 

1. Swagger endpoint documentation

![Swagger endpoint documentation 1](screenshots/5_1_swagger_get.png)

![Swagger endpoint documentation 2](screenshots/5_1_swagger_get_2.png)

![Swagger endpoint documentation 3](screenshots/5_1_swagger_get_3.png)

![Swagger endpoint documentation 4](screenshots/5_1_swagger_post.png)

### Step 6. Consume model endpoints and benchmark 

1. Screenshot of endpoint.py running against the model 

![Screenshot of endpoint.py running against the model](screenshots/6_1_endpoint_py_run.png)

2. Screenshot of Apache Benchmark running against the REST API 

![Benchmark end](screenshots/6_2_benchmark_start.png)

![Benchmark start](screenshots/6_2_benchmark_end.png)

### Step 7. Create, publish and consume a pipeline

1. AzureML Pipeline section showing that the pipeline has been created

![AzureML Pipeline section showing that the pipeline has been created](screenshots/7_1_created_pipeline.png)

2. AzureML Pipelines section showing the Pipeline endpoint

![AzureML Pipelines section showing the Pipeline endpoint](screenshots/7_2_pipeline_endpoint.png)

3. The Bankmarketing dataset with the AutoML module 

![The Bankmarketing dataset with the AutoML module ](screenshots/7_3_dataset_and_automl_module.png)

4. The Published Pipeline overview 

![The Published Pipeline overview](screenshots/7_4_published_pipeline.png)

5. Jupyter Notebook with Run Details widget working 

![Jupyter Notebook with Run Details widget working](screenshots/7_5_run_details_widget.png)

![Jupyter Notebook with Run Details widget working - second run](screenshots/7_5_run_details_widget_second_run.png)

6. Scheduled run in ML Studio 

![All runs](screenshots/7_6_all_runs.png)

![Scheduled run in ML Studio](screenshots/7_6_scheduled_run.png)

## Screencast Video 
Screencast of main steps and project demo: https://youtu.be/ZWCnZ-xlyEM 
