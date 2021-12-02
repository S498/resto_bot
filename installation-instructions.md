# Setup and Installation
### Step 1 : Download Anaconda
Download and install Anaconda Navigator: https://docs.anaconda.com/anaconda/install/
### Step 2 : Open command prompt
- Windows: Open Anaconda Prompt in Administrator mode
- Linux user can open terminal in sudo mode

### Step 3 : Install virtual enviornment

**Create the virtual Environment**<br> 
`conda create -n resto_bot python=3.7.5`<br> 

**Activate your virtual Environment**<br> 
`conda activate resto_bot`<br> 
### Step 5 : Install Rasa
Install Rasa Framework and its dependencies by running the following commands in the virtual environment Command Prompt Shell<br>
`pip install --upgrade rasa-x --extra-index-url https://pypi.rasa.com/simple`  <br>
`pip install rasa[spacy]` <br>
`python -m spacy download en_core_web_md`  <br> 
`python -m spacy link en_core_web_md en` <br>


### Step 6 : Getting a Bing Maps Key <br>
Navigate [here](https://docs.microsoft.com/en-us/bingmaps/getting-started/bing-maps-dev-center-help/getting-a-bing-maps-key) and then click on ‘Bing Maps Key’ hyperlink. 
After we have signed up (if we do not have an account on Microsoft) and provided our basic information, we can create a key. 
After the key has been created we can view it by clicking on ‘My Account’ -> ‘My Keys’.

### Step 7 : Create Zomato API<br>
We will need an API key from Zomato, (Since it was deprecated, I'm using it from my old project), here is the link for the swagger file (https://app.swaggerhub.com/apis-docs/Vivek-Raj/zomato-api/1.0.0)

> Update both the keys in [actions.py](./actions.py) file.
