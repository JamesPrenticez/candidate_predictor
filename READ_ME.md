# Candidate Suitablity with Predictive Machine Learning (Python/React)

1. (Part One)[https://python.plainenglish.io/how-to-build-a-predictive-machine-learning-site-with-react-and-python-part-one-model-development-3f76d0a7d27f]
2. (Part Two)[https://python.plainenglish.io/how-to-build-a-predictive-machine-learning-site-with-react-and-python-part-two-api-development-9c1cef28f3a]
3. (Part Three)[https://python.plainenglish.io/how-to-build-a-predictive-machine-learning-site-with-react-and-python-part-three-frontend-72c063e8716e]

(Github)[https://github.com/Daltonic/predictive]

## Backend
1. Choosing and enviroment - like before the building of a house, a good enviroment will allow for our machine learning code to run.
  - Python
  - Anaconda [https://www.anaconda.com/products/distribution]
    - Spyder
  - Model [https://downgit.github.io/#/home?url=https:%2F%2Fgithub.com%2FDaltonic%2Fpredictive%2Ftree%2Fmain%2Fmodel]
- Machine learning algorithm called “RandomForestClassifier” of the sklearn library
- Pickle - library to load up our trained model from part one of this series.

2. Setting up an API endpoint
  - Python
  - Fast Api
  - Uvicorn - ASGI web server implementation  - library is used to create a server having a host and port of your preference for communicating with our API via HTTP requests and responses
  - scikit-learn
  - Thunder Clients - postman alternative
  - BaseModel class from the pydantic library is used for defining our API request parameters. This is important for ensuring that we are sending the right data types to our trained machine learning model.
  - The FastAPI - library helps us define the routes and the functions a route will run when accessed by a client. It also helps us define the responses we give for a request.
  - CORSMiddleware - helps us define the domains that will get resources from our API. This is a very important configuration in a FastAPI project.

3. Spin Server and test endpoints
    - run
      - cd backend/api
      - python main.py
    - get request
      - http://localhost:8080/
    - post request
      - http://localhost:8080/prediction
      - ``` 
          {
            "gender": 1,
            "bsc": 2.7,
            "workex": 0,
            "etest_p": 65.55,
            "msc": 4.2
          }
        ```
      - 
  



## Frontend