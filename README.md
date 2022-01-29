# Tomato Dieses Classification

In This project use dataset from kaggle.com with 10 different image classes. and we get 94% of training Accuracy.

## Setup for Python:
1. Install Python ([Setup instructions](https://wiki.python.org/moin/BeginnersGuide))
2. Install Python packages
```
pip3 install -r training/requirements.txt
pip3 install -r api/requirements.txt
```
3. Install Tensorflow Serving ([Setup instructions](https://www.tensorflow.org/tfx/serving/setup))

## Training the Model

4. Download the data from [kaggle](https://www.kaggle.com/arjuntejaswi/plant-village).
5. Only keep folders related to Tomato.
6. Run Jupyter Notebook in Browser.

```bash
jupyter notebook
```
7.  open 'tometo project.ipynb' in Jupyter Notebook.
8.  In cell #2, update the path to dataset.
9.  Run all the Cells one by one.
10. Copy the model generated and save it with the version number in the `models` folder.

we use 80% data for train model
we use 10% data for validation
we use 10% data for test our model

## Running the API

### Using FastAPI

1. Get inside `api` folder

```bash
cd api
```

2. Run the FastAPI Server using uvicorn

```bash
uvicorn main:app --reload --host 0.0.0.0
```

3. Your API is now running at `0.0.0.0:8000`

### Using FastAPI & TF Serve

1. Get inside `api` folder

```bash
cd api
```

2. Copy the `models.config.example` as `models.config` and update the paths in file.
3. Run the TF Serve (Update config file path below)

