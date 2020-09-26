# AgriTech 4.0
Internet of Things has revolutionized all the sectors, however in Agriculture there are still a plethora of problems plaguing the farmers. For instance the unavailability of proper information on real-time weather and soil conditions of his land at his disposal, and the lack of smart and integrated machinery to do automation during the times of unconventional weather and environmental situations. These vacuums in agriculture demands the digitization of the ecosystem and building a complete end to end automatized digital solution. 

We are taking the initiative to build a fully decentralized solution which allows for the farmers, 
1.	To sell their goods directly to the customers using our Blockchain Marketplace
2.	Gather information about the real-time weather and soil conditions from our single compact sensor and get notified at finger tips using our application with the help of AI and ML
3.	Intelligent Crop Maintenance systems(ICMS) which takes care of insects and pesticides, water sprinkling etc.
4.	For underground plantations, the farmer is presented with the option to perform automatic plucking of crops which will be performed by the gripper only after his consent
5.	Give personalized recommendations based on Market demand and also from the competitive landscape which boosts the likelihood of selling the crops to consumers/ businesses

An app with deep learning model to predict compatibility using soil images and also assists in minimising loss at harvest time by predicting prices.
Developed at Hack your Future 2020

## Requirements
1. Beautiful Soup
2. Tensorflow
3. Numpy
4. Pandas

## Usecase 1: Marketplace app

For setting and running the marketplace app, visit the frontend folder and follow the instructions

## Usecase 2: Price Prediction
1. First scrape crop prices data from agmarknet.gov.in using python web scraping website beautiful soup.
```
python scrap_crops.py
```
This will give output csv file for different states, crops and over different months.

2. To predict prices of crops after harvesting period, run
```
python ./scripts/hack1.py
```
This uses a random forest regressor to predict prices.


3. Train an inceptionv3 model inn tensorflow using transfer learning to classify soil type by image.
```
python ./scripts/retrain.py --imagedir <pathtoimages>
```
4. Complete pipeline output\\
Get best crop to grow from soil image taking into consideration price prediction after harvest time.
```
python ./scripts/label_image.py```



