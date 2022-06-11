## What Can be Improved?

- Modularize code into functions if you haven’t so far
- Automate data input: Different dataset names should’t be hardcoded
- Model Training Process: Automate model and hyperparameter selection
- Experiment tracking: Log every iteration
- Model Registry: Not all the models should be named “lr” or “rf”
- ML Pipelines: Break down logic into multiple steps. This way you don’t have to run the modules more than once or otherwise. In other words, create a workflow.
- Turn model into a service
- Monitoring the model

## Maturity Levels

### No MLOps

- Everything is on Jupyter notebooks

### Devops but no MLOps

- Releases are automated
- Unit & integration tests
- CI/CD
- Ops metrics

- No experiment tracking
- No reproducibility
- DS separated from engineering

### Automated Training

- Training pipeline
- Experiment tracking
- Model registry
- Low friction deployment
- DS work with engineering

### Automated Deployment

- Deployment is the part of pipeline
- A/B testing
- Model monitoring

### Full MLOps Automation

- Everything is automated