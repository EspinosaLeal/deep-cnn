# [ARCADAHAI] Deep Convolutional Networks for Text Classification on Valohai platform 

The model is described in the Paper: [VERY DEEP CONVOLUTIONAL NETWORKS FOR TEXT CLASSIFICATION] (https://arxiv.org/abs/1606.01781)

Recommend reading list before start working with Valohai platform:

* [Git](https://git-scm.com/doc): For software version control.
* [Docker](https://docs.docker.com): For environment set-up.
* [Python argparse](https://docs.python.org/3/library/argparse.html), [Tensorflow tf.flags](https://stackoverflow.com/questions/33932901/whats-the-purpose-of-tf-app-flags-in-tensorflow): For user-friendly command-line interface. 
* [YAML](https://yaml.org): Yet Another Markup Language xD 
## Training Model on Valohai Platfrom 

1. Log in to Valohai Platform with your account 

2. Create a new **Project**. Go to **Settings** tab, choose **Repository**. Copy the Github link project to **URL** and **SAVE**. Valohai will automaticlly Fetch repository from Github to Valohai Platform. URL for this project: 

    > https://github.com/phanthaithuc/deep-cnn 

3. Go to **Execution** tab, **Create Execution**, Valohai will read the _valohai.yaml_  and give you many options for **Parameters**

4. Choose your preference paramters and start training. To train with another dataset, see **Training Dataset** below. 

5. To change **Docker image** or change running step, edit the _valohai.yaml_ file or choose another Docker image in **Image and Command** section on Valohai web interface. 

6. To commit another version of your code. **Git push** your new version to Github then click  **Fetch Repository** button on your Valohai project. 

    Valohai will fetch the new version and show another commit option base on your new version of code under **Commit**

7. To train with another dataset with Valohai. There are 2 options: 
    
    * Go to **Data** tab on your project, upload your train set and test set to Valohai storage. Go back to **Execution** tab, choose your _Data file_ under **Input** section.
    
    * If you have your dataset upload somewhere on the Internet, copy your direct link to _URL_ under **Input** section. Done 
    
    * For more datasets, see **Training Dataset** below. The datasets come from the author of the paper, it's open and free to use. 
    


## Training Model on your Local Machine

1. **Clone** or **Download** this Project from GitHub. 

2. Run this Project with default Parameters

    > python train.py 
   
3. Run this Project with your chosen Paramters: 

    > python train.py --lr learning_rate  --num_epochs number of epochs 
    
    >For example: python train --lr 0.005  --num_epochs 10 --batch_size 64
    
    Read train.py for more preference parameters 

4. To train with other datasets. 

      * Download more datasets from this [LINK](https://drive.google.com/drive/u/0/folders/0Bz8a_Dbh9Qhbfll6bVpmNUtUcFdjYmF2SEpmZUZUcVNiMUw1TWN6RDV3a0JHT3kxLVhVR2M). 
   
     * Copy new _train.csv_ and _test.csv_ to **data** folder. Start training with your new dataset. 
     
     
    

    
### Training Dataset

You can download lot of datasets that could be used for training this model from this [LINK](https://drive.google.com/drive/u/0/folders/0Bz8a_Dbh9Qhbfll6bVpmNUtUcFdjYmF2SEpmZUZUcVNiMUw1TWN6RDV3a0JHT3kxLVhVR2M). 

Dataset Overview: 

| Dataset                | Classes | Train samples | Test samples |
|------------------------|:---------:|:---------------:|:--------------:|
| AG’s News              |    4    |    120 000    |     7 600    |
| Sogou News (Chinese)           |    5    |    450 000    |    60 000    |
| DBPedia                |    14   |    560 000    |    70 000    |
| Yelp Review Polarity   |    2    |    560 000    |    38 000    |
| Yelp Review Full       |    5    |    650 000    |    50 000    |
| Yahoo! Answers         |    10   |   1 400 000   |    60 000    |
| Amazon Review Full     |    5    |   3 000 000   |    650 000   |
| Amazon Review Polarity |    2    |   3 600 000   |    400 000   |


