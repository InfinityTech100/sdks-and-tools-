# sdks---tools---gueidlines
# sdks-and-tools-
# How to make a HTTP Get request using python 
<h3 id="GET REQ HTTP">1.install requests Library  </h3>
<p>Write the Following bash command</p>
  pip install requests
<h3 id="GET REQ HTTP">2.Test code </h3>
<p> Here's a simple example of a Python script that makes an HTTP GET reques </p>

import requests

def make_get_request(url):
    try:
        # Make the GET request
        response = requests.get(url)

        # Check if the request was successful (status code 200)
        if response.status_code == 200:
            print("Request successful!")
            # You can access the content of the response using response.text
            print("Response content:\n", response.text)
        else:
            print(f"Request failed with status code {response.status_code}")
    except requests.exceptions.RequestException as e:
        print(f"An error occurred: {e}")
<h3 id="GET REQ HTTP">2.Test code </h3>

