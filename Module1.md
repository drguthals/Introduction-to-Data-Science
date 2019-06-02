# Introduction to Course Tools
This module will give you a brief introduction into the tools you will need to be successful throughout and beyond this course. 

You will also get a chance to practice a few tutorials and examples of Azure Cognitive Services. 

## Verify Your Accounts
First, make sure you have verified that you have the following accounts:
1. Sign up for [GitHub](https://github.com/) to be able to ask questions.
2. Sign up for a [Microsoft Account](https://account.microsoft.com/account/Account) using a .edu email address. 
3. Go to the [Azure for Students](https://azure.microsoft.com/en-us/free/free-account-students-faq/) offer and sign up with your .edu email address. 
4. Make sure you can sign in with your Microsoft Account (MSA) on [Azure Notebooks](https://notebooks.azure.com/).
5. Make sure you can sign in with your MSA on [Azure Machine Learning Studio](https://studio.azureml.net/).

## Azure Cognitive Services Project
As an introduction to this curriculum, you will complete a 10,000 foot project using Azure Cognitive Services. 

1. Create an Azure Notebook  
Go to https://notebooks.azure.com/ and go to My Projects -> New Project and name it "IntroToDataScience".

2. Create a new Python 3 Notebook  
Click on the `+` sign and add a new Python 3 Notebook. Name your noteboo "DataScienceMod1".

3. Describe the project  
In this project, you will be thinking of an application that uses Azure Cognitive Services, and exploring the limitations of the services. Describe your project according to the application you're thinking of. 

4. Setup your Code
Add the following code to your new notebook in three different tiles:
```
# Define the Subscription key for making API calls.
secret = 'INSERT YOUR KEY HERE'
```

```
# Import required libraries for request headers and json extraction.
import http.client, urllib.request, urllib.parse, urllib.error, base64, json

# Replace the subscription_key string value with your valid subscription key.
subscription_key = secret

# Replace to match your region.
uri_base = 'westcentralus.api.cognitive.microsoft.com'

headers = {
    # Request headers.
    'Content-Type': 'application/json',
    'Ocp-Apim-Subscription-Key': subscription_key,
}

params = urllib.parse.urlencode({
    # Request parameters. All of them are optional.
    'visualFeatures': 'Description,Color,Tags',
    'language': 'en',
})
```

```
body = "{'url':'https://timeincsecure-a.akamaihd.net/rtmp_uds/293884104/201703/2681/293884104_5360456295001_5360434467001-vs.jpg?pubId=293884104&videoId=5360434467001'}"

try:
    # Execute the REST API call and get the response.
    conn = http.client.HTTPSConnection('westcentralus.api.cognitive.microsoft.com')
    conn.request("POST", "/vision/v1.0/analyze?%s" % params, body, headers)
    response = conn.getresponse()
    data = response.read()

    # 'data' contains the JSON data. The following formats the JSON data for display.
    parsed = json.loads(data.decode())
    print ("Response:")
    print (json.dumps(parsed, sort_keys=True, indent=2))
    conn.close()

except Exception as e:
    print('Error:')
    print(e)

##################################
```

5. Get your Subscription Key from the Azure Portal  
Go to the [Azure Portal](https://ms.portal.azure.com/) and click on "All Services" -> AI and Machine Learning -> Cognitive Services. Click on Create Cognitive Service and choose Computer Vision. Once it has been deployed, copy the key and paste it in the first code tile of your Azure Notebook. Ensure your HTTPS Connection is also using the correct endpoint in the second and third code tile.

6. Run Your Code  
Run each tile and ensure it is working. 

7. Experiment  
Try different images, create other cognitive services such as text analytics, and explore the [Azure docs](https://docs.microsoft.com/en-us/azure/). 

8. Write Up  
Spend 20-30 minutes writing. If you cannot describe your work to others, what is the point?
1. What was the goal of your application? (People problem)  
2. What is difficult about the goal? (Technical problem)  
3. What data did you use to explore?  
4. What gaps in data did you find?  
5. What conclusions were you able to draw?  
6. What conclusions were you not able to draw?  
7. How would you proceed?  

9. Download your file and upload it to GitHub as a Pull Request.
