# How to use HTTP requests in python 
## GET Req 
<h3>1.install requests Library  </h3>
<p>Write the Following bash command</p>

    pip install requests

<h3>2.Test code </h3>
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
## POST Req
<h3>Test  Simple code </h3>
<p>POST request using the requests library in Python, you can use the requests.post() method. Here's an example</p>

    import requests

    def make_post_request(url, data=None, headers=None):
        try:
            # Make the POST request
            response = requests.post(url, data=data, headers=headers)

            # Check if the request was successful (status code 200)
            if response.status_code == 200:
                print("Request successful!")
                # You can access the content of the response using response.text
                print("Response content:\n", response.text)
             else:
                print(f"Request failed with status code {response.status_code}")
        except requests.exceptions.RequestException as e:
                print(f"An error occurred: {e}")
<h3>Notes : </h3>
<p>Make sure to do the following steps </p>
    # Replace 'https://www.example.com' with the URL you want to make a POST request to
    url = 'https://www.example.com'

    # Replace 'your_data' with the data you want to include in the POST request (if any)
    data = {'key1': 'value1', 'key2': 'value2'}

    # Replace 'your_headers' with any custom headers you want to include in the request (if any)
    headers = {'Content-Type': 'application/json'}

    make_post_request(url, data=data, headers=headers)
## PUT Req
<h3>Test  Simple code </h3>
<p>POST request using the `requests` library in Python, you can use the requests.put() method. Here's an example</p>

    import requests

    def make_put_request(url, data=None, headers=None):
        try:
            # Make the PUT request
            response = requests.put(url, data=data, headers=headers)

            # Check if the request was successful (status code 200)
            if response.status_code == 200:
                print("Request successful!")
                # You can access the content of the response using response.text
                print("Response content:\n", response.text)
            else:
                print(f"Request failed with status code {response.status_code}")
        except requests.exceptions.RequestException as e:
        print(f"An error occurred: {e}")

    # Replace 'https://www.example.com' with the URL you want to make a PUT request to
    url = 'https://www.example.com'

    # Replace 'your_data' with the data you want to include in the PUT request (if any)
    data = {'key1': 'value1', 'key2': 'value2'}

    # Replace 'your_headers' with any custom headers you want to include in the request (if any)
    headers = {'Content-Type': 'application/json'}

    make_put_request(url, data=data, headers=headers)
## DELETE Req
<h3>It will be the same </h3>
<p> Test the following code Using `requests.delete()` method. Here's an example</p>

    import requests

    def make_delete_request(url, headers=None):
        try:
            # Make the DELETE request
            response = requests.delete(url, headers=headers)

            # Check if the request was successful (status code 200)
            if response.status_code == 200:
                print("Request successful!")
                # You can access the content of the response using response.text
                print("Response content:\n", response.text)
            else:
                print(f"Request failed with status code {response.status_code}")
        except requests.exceptions.RequestException as e:
        print(f"An error occurred: {e}")

    # Replace 'https://www.example.com' with the URL you want to make a DELETE request to
    url = 'https://www.example.com'

    # Replace 'your_headers' with any custom headers you want to include in the request (if any)
    headers = {'Authorization': 'Bearer YOUR_ACCESS_TOKEN'}

    make_delete_request(url, headers=headers)
<p>Make sure to replace the `url`, `data`, and `headers` variables with the appropriate values for your specific use case. If you're sending JSON data in the request, you might want to use the `json` parameter instead of `data`:</p>

    response = requests.put(url, json=data, headers=headers)



