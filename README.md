# YelpSense

![codeclimate maintainability](https://api.codeclimate.com/v1/badges/605aa46b3acf4e517a81/maintainability)

You can find the project at [https://yelpsense.com](https://yelpsense.com).

## Contributors

|                                       [Spencer Adams](https://github.com/spentaur)                                       |                                       [Connor Sanderford](https://github.com/crsanderford)                                        |                                       [Bethany Richardson](http://github.com/ravenha)                                          |
| :-----------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------: |
|                      [<img src="https://avatars2.githubusercontent.com/u/2055801?s=460&u=2e8d9831dc72da5d99a127d070f7985a40fcacfb&v=4" width = "200" />](https://github.com/spentaur)                       |                      [<img src="https://yelpsense.com/images/connor.jpg" width = "200" />](https://github.com/crsanderford)                       |                      [<img src="https://avatars2.githubusercontent.com/u/51799343?s=460&u=cc7cd70771da267f60437f6551c05cb415f5d1fe&v=4" width = "200" />](https://github.com/ravenha)                       |
|                 [<img src="https://github.com/favicon.ico" width="15"> ](https://github.com/spentaur)                 |            [<img src="https://github.com/favicon.ico" width="15"> ](https://github.com/crsanderford)             |           [<img src="https://github.com/favicon.ico" width="15"> ](https://github.com/ravenha)            |
| [ <img src="https://static.licdn.com/sc/h/al2o9zrvru7aqj8e1x2rzsrca" width="15"> ](https://linkedin.com/in/spentaur) | [ <img src="https://static.licdn.com/sc/h/al2o9zrvru7aqj8e1x2rzsrca" width="15"> ](https://www.linkedin.com/in/connor-sanderford/) | [ <img src="https://static.licdn.com/sc/h/al2o9zrvru7aqj8e1x2rzsrca" width="15"> ](https://www.linkedin.com/in/ravenha) |



<!-- 🚫 5️⃣ Optional examples of using images with links for your tech stack, make sure to change these to fit your project

![MIT](https://img.shields.io/packagist/l/doctrine/orm.svg)
![Typescript](https://img.shields.io/npm/types/typescript.svg?style=flat)
[![Netlify Status](https://api.netlify.com/api/v1/badges/b5c4db1c-b10d-42c3-b157-3746edd9e81d/deploy-status)](netlify link goes in these parenthesis)
[![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg?style=flat-square)](https://github.com/prettier/prettier)

🚫 more info on using badges [here](https://github.com/badges/shields) -->

## Project Overview


1️⃣ [Trello Board](https://trello.com/b/Uwd55Hds/labs-pt9-pt-yelp)

1️⃣ [Product Canvas](https://www.notion.so/Part-Time-Yelp-Dataset-Challenge-4bddd7e5a8114139955d1223647dfc79)

<!-- 🚫 Replace lorem ipsum with a description of your project -->

YelpSense is a suite of machine learning demos based on the Yelp Open Dataset Challenge. 

<!-- 🚫  delete if front end is not applicable to your project

1️⃣ [Deployed Front End](🚫add link to deployed app here) -->

### Tech Stack

<!-- 🚫 List all of the languages, frameworks, services, etc used here. -->

This project done using python and it's most popular packages for data science and machine learning including:
- [Tensorflow](https://www.tensorflow.org)
- [PyTorch](https://pytorch.org)
- [scikit-learn](https://scikit-learn.org/stable/)
- [huggingface](https://huggingface.co)
- [ktrain](https://github.com/amaiya/ktrain)
- [simpletransformers](https://github.com/ThilinaRajapakse/simpletransformers)
- [eli5](https://eli5.readthedocs.io/en/latest/)
- [lime](https://lime-ml.readthedocs.io/en/latest/)
- [Docker](https://www.docker.com)
- [lightFM](https://making.lyst.com/lightfm/docs/index.html)

### 2️⃣ Predictions

#### Sentiment Analysis
We trained a sentiment analysis model using the transformers package and the DistilBERT pretrained model for transfer learning. We chose to make this a regression model instead of a classification model, hoping that this would allow more of the subtleties of sentiment to show in our predictions.

### 2️⃣ Explanatory Variables

-   Review Text
-   Star Rating

#### Recommendations
We trained a factorization machine model using the lightFM package, using only users' ratings of businesses and no content factors. We chose to interpret user scores as a binary classification problem, to better reflect the outcome of the recommender and to enable the use of metrics like ROC-AUC.

### 2️⃣ Explanatory Variables
-   User Identity
-   Business Identity


### Data Sources
<!-- 🚫  Add to or delete souce links as needed for your project -->


-   [Yelp Open Dataset](https://www.yelp.com/dataset)

### Python Notebooks

🚫  Add to or delete python notebook links as needed for your project

[Python Notebook 1](🚫add link to python notebook here)

[Recommender](https://github.com/Lambda-School-Labs/Yelp-ds/blob/recommender/recommender/lightfm_hyperparams.ipynb)

[Python Notebook 3](🚫add link to python notebook here)

### 3️⃣ How to connect to the web API

<!-- 🚫 List directions on how to connect to the API here -->

Make a json POST request to either https://8rq6v9dni0.execute-api.us-east-1.amazonaws.com/dev/sentiment or https://8rq6v9dni0.execute-api.us-east-1.amazonaws.com/dev/summarization with the a `text` field, and a `model_name` field (`distilbert-regression` or `default` for sentiment / `bert` or `t5` for summarization)

Example:

```
curl --request POST \
  --url https://8rq6v9dni0.execute-api.us-east-1.amazonaws.com/dev/sentiment \
  --header 'accept: application/json, text/plain, */*' \
  --header 'accept-encoding: gzip, deflate, br' \
  --header 'accept-language: en-us' \
  --header 'connection: keep-alive' \
  --header 'content-type: application/json;charset=utf-8' \
  --header 'host: 8rq6v9dni0.execute-api.us-east-1.amazonaws.com' \
  --header 'origin: https://yelpsense.com' \
  --header 'referer: https://yelpsense.com/' \
  --header 'user-agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_5) AppleWebKit/605.1.15 (KHTML, like Gecko) Version/13.1.1 Safari/605.1.15' \
  --data '{"text":"great!",
"model_name": "default"}'
```

### 3️⃣ How to connect to the data API

<!-- 🚫 List directions on how to connect to the API here -->

Per the Terms of Service of the dataset, we can not make the raw data avaiable.

## Contributing

When contributing to this repository, please first discuss the change you wish to make via issue, email, or any other method with the owners of this repository before making a change.

Please note we have a [code of conduct](./code_of_conduct.md.md). Please follow it in all your interactions with the project.

### Issue/Bug Request

 **If you are having an issue with the existing project code, please submit a bug report under the following guidelines:**
 - Check first to see if your issue has already been reported.
 - Check to see if the issue has recently been fixed by attempting to reproduce the issue using the latest master branch in the repository.
 - Create a live example of the problem.
 - Submit a detailed bug report including your environment & browser, steps to reproduce the issue, actual and expected outcomes,  where you believe the issue is originating from, and any potential solutions you have considered.

### Feature Requests

We would love to hear from you about new features which would improve this app and further the aims of our project. Please provide as much detail and information as possible to show us why you think your new feature should be implemented.

### Pull Requests

If you have developed a patch, bug fix, or new feature that would improve this app, please submit a pull request. It is best to communicate your ideas with the developers first before investing a great deal of time into a pull request to ensure that it will mesh smoothly with the project.

Remember that this project is licensed under the MIT license, and by submitting a pull request, you agree that your work will be, too.

#### Pull Request Guidelines

- Ensure any install or build dependencies are removed before the end of the layer when doing a build.
- Update the README.md with details of changes to the interface, including new plist variables, exposed ports, useful file locations and container parameters.
- Ensure that your code conforms to our existing code conventions and test coverage.
- Include the relevant issue number, if applicable.
- You may merge the Pull Request in once you have the sign-off of two other developers, or if you do not have permission to do that, you may request the second reviewer to merge it for you.

### Attribution

These contribution guidelines have been adapted from [this good-Contributing.md-template](https://gist.github.com/PurpleBooth/b24679402957c63ec426).

## Documentation

See [Backend Documentation](_link to your backend readme here_) for details on the backend of our project.

See [Front End Documentation](_link to your front end readme here_) for details on the front end of our project.

