# Machine Learning Project Template

Welcome to the Machine Learning Project Template! 

Efficiently structuring your projects is crucial for clarity, maintainability, and consistency across your machine learning endeavors. This template provides you with a standardized organization that makes it easy to understand, modify, and replicate your work across multiple projects.

## Folder Stracture
```bash
├── README.md                                  # Project documentation
├── data
│   ├── feature_eng                            # Data for feature engineering
│   ├── processed                              # Processed data
│   └── raw
│       ├── source_a                          # Raw data from source A
│       │   └── data.csv                      # Sample data from source A
│       └── source_b                          # Raw data from source B
├── docs
│   ├── pdf                                   # PDF documents
│   │   └── overview.pdf                     # Example PDF document
│   └── pdfs                                  # PDFs related to the project
├── infrastructure                           
│   ├── common_resources                      # yaml or template files to create common resources via Infrastructure as Code (IaC)
│   ├── ml_resources                          # crate Machine learning resources via IaC
│   │   ├── inference.yaml                    # crate infernce components via IaC 
│   │   └── training.yaml                     # create training components via IaC
│   ├── shared-resources                      # create shared resources such as s3 buckets
│   │   └── common.yaml                       # Common configurations, secrets, etc
│   └── test_resources                        # Test resources for infrastructure
│       └── integration-tests.yaml            # create required Integration test resources
├── models
│   ├── artifacts                             # Model artifacts
│   │   └── model_a                           # Artifacts for Model A
│   │       └── model_a_v1_2023_03_15.joblib  # Model A serialized artifcat
│   └── metadata                              # Model metadata
├── notebooks
│   ├── data_assessment                       # Notebooks for data assessment
│   ├── experiments                           # Notebooks for experiments
│   ├── exploratory                           # Exploratory data analysis notebooks
│   │   └── 01-fs-EDA_exploration-work.ipynb  # Example EDA notebook
│   ├── feature_engineering                    # Notebooks for feature engineering
│   └── visualizations                        # Notebooks for data visualization
├── pipelines
│   ├── etl                                   # ETL (Extract, Transform, Load) pipelines
│   │   ├── extractions                       # Data extraction components
│   │   │   ├── source_a
│   │   │   │   └── source_a.py              # Extraction script for source A
│   │   │   └── source_b
│   │   │       └── source_b.py              # Extraction script for source B
│   │   ├── loads                            # Data loading components
│   │   └── transformations                   # Data transformation components
│   │       ├── source_a
│   │       └── source_b
│   ├── inference                             # Inference pipeline
│   │   ├── inference.py                     # Inference script
│   │   ├── model_a
│   │   │   ├── lambda_a                     # service files/Lambda functions for Model A infernece
│   │   │   └── lambda_b                     # service files/Lambda functions for Model B infernece
│   │   └── model_b
│   ├── monitoring                            # Monitoring components
│   │   └── slack                             # Slack/Email/teams monitoring integration
│   ├── orchestration                         # Pipeline orchestration such as Stepfunction, Airflow, etc
│   └── training                              # Auomtated re-training pipelines
│       └── model_build
│           ├── model_a
│           │   ├── Dockerfile               # Dockerfile for Model A
│           │   └── requirements.txt         # Python requirements for Model A
│           └── model_b
├── prototyping                               # Prototyping code  for quick dashboard or visualization apps
├── requirements.txt                          # Python dependencies for your project (or more robust tools like Pipenv,Poetry)
├── scripts                                   # Finale script to be used in Docker for Production
│   ├── data_processing.py                    # Data processing script finilized after expermiation in notebooks
│   ├── feature_engineering.py                # Feature engineering script finilized after expermiation in notebooks
│   ├── inference.py                          # Inference script
│   ├── model_evaluation.py                   # Model drift evaluation script
│   └── model_training.py                     # Model training script
└── tests
    ├── end-to-end                            # End-to-end tests
    ├── integration                           # Integration tests
    └── unit                                  # Unit tests

```

## Getting Started

1. **Clone the Repository**: Start by cloning this template repository to kickstart your project.

2. **Customize as Needed**: Tailor the structure and files to your specific project requirements.



> Note: The data folder should be used to store the actual CSV files if the size of the data files is relatively small. If your data file size is substantial, such as images, it's better to use a data versioning tool such as [dvc](https://dvc.org/) or alternatives. These versioning tools generally keep the actual files on external storage, such as AWS S3, and track the data version using meta files stored in the data folder on GitHub.


## Contribute

Feel free to contribute improvements or suggest changes to enhance this project template. Together, we can create a resource that benefits the entire machine learning community.

## License

This project is licensed under the [MIT License](LICENSE), allowing you to adapt and use it for any purposes.

