
# TriCode-Fruits-image-classifier
A binary image classifier to accept user input as image and predict wheather it's a mango or jackfruit.

https://tricode.herokuapp.com/

![BFH Banner](https://trello-attachments.s3.amazonaws.com/542e9c6316504d5797afbfb9/542e9c6316504d5797afbfc1/39dee8d993841943b5723510ce663233/Frame_19.png)
# TriCode

In this project, I built a python application that uses a train image classifier model on a dataset, then predict the class of new images The project was devided to two parts.

##### Part 1 - Developing an Image Classifier in colab

In this first part of the project, I implemened an image classifier with data sets of JackFruit and Mango from drive to train the model.

##### Part 2 - Building the flask application

Build a pair of Python scripts that run from the command line to run the image classifier and to predict new images using the trained model.

## Team members :raising_hand:
1. Ajmal V A  [https://github.com/Ajmalva]
2. Alvin Antony  [https://github.com/A-L-V-I-N]
3. Ancy Paul  [https://github.com/smile-10]
## Team Id :key:

     BFH/recSYFS77S94PHQFg/2021

## Link to product walkthrough :tv:
![Watch the video](https://i.imgur.com/ruvUkkb.png)
(https://qrgo.page.link/wPBxC)

## Live URL :satellite:
We have deployed the current model to Heroku
You can See the webapp here: https://tricode.herokuapp.com/
## Libraries used :books:
This project requires  **Python 3.x**  and the following Python libraries installed:
-   [TensorFlow](https://www.tensorflow.org/)
-   [Numpy](https://www.numpy.org/)
-   [Pillow](https://pillow.readthedocs.io/en/stable/)
-   [keras](https://github.com/keras-team/keras)
-   [Matplotlib](https://matplotlib.org/)
# How to configure :wrench:
## How to Run

### Run with Docker

With **[Docker](https://www.docker.com)**, you can quickly build and run the entire application in minutes :whale:

```shell
# 1. First, clone the repo
$ git clone https://github.com/Ajmalva/TriCode-Fruits-image-classifier.git
$ cd keras-flask-deploy-webapp

# 2. Build Docker image
$ docker build -t keras_flask_app .

# 3. Run!
$ docker run -it --rm -p 5000:5000 TriCode-Fruits-image-classifier
```

Open http://localhost:5000 and wait till the webpage is loaded. :grin:

### Local Installation

It's easy to install and run it on your computer.

```shell
# 1. First, clone the repo
$ git clone https://github.com/Ajmalva/TriCode-Fruits-image-classifier.git
$ cd TriCode-Fruits-image-classifier

# 2. Install Python packages
$ pip install -r requirements.txt

# 3. Run!
$ python app.py
```

Open http://localhost:5000 and have fun. :smiley:

## Customization :computer:

It's also easy to customize the ui and include your own models in this app.

<details>
 <summary>Details</summary>

### Use your own model

Place your trained `.h5` file saved by `model.save()` under models directory.

### Use other pre-trained model

See [Keras applications](https://keras.io/applications/) for more available models such as DenseNet, MobilNet, NASNet, etc.

### UI Modification

Modify files in `templates` and `static` directory.

`index.html`and `style.css`  for the UI and `control.js` for all the behaviors.

</details>


## Deployment :electric_plug:

To deploy it for public use, you need to have a public **linux server**.

<details>
 <summary>Details</summary>
  
### Run the app

Run the script and hide it in background with `tmux` or `screen`.
```
$ python app.py
```

You can also use gunicorn instead of gevent
```
$ gunicorn -b 127.0.0.1:5000 app:app
```

More deployment options, check [here](https://flask.palletsprojects.com/en/1.1.x/deploying/wsgi-standalone/)

### Set up Nginx

To redirect the traffic to your local app.
Configure your Nginx `.conf` file.

```
server {
  listen  80;

  client_max_body_size 20M;

  location / {
      proxy_pass http://127.0.0.1:5000;
  }
}
```

</details>

