## Example 

The example provides a dataserver for Version 2.0.0 of the Async API description. 
It implements a REST-API endpoint as well as a websocket endpoint on port 8080. 
Data from the datasource can be received in json and csv format. 
The first datastream is a sinus, the second a rectangular function. 
The timestamps are UNIX timestamps. 

### How to start the example 

To start the example make sure you have python installed on your system. 

#### Create a test environment

Open your CLI. Use either Windows or Linux. 

Type the following command into your CLI: 

```
python -m venv env 
```

#### Start the environment on Linux 

```
source env/bin/activate
``` 

#### Start the environment on Windows 

```
env\Scripts\activate 
```

#### Download packages 

Download the needed packages with 
```
pip install aiohttp websockets aiohttp_middlewares
```

#### Run the script 

Run the script with 
```
python main.py
```

If successfull you will receive the message: "Server running on port 8080 (HTTP & WebSocket)" in your CLI

### How to test the example 

To test the example you can try the following commands: 

#### GET request from the Rest API

```
curl -X GET http://localhost:8080/v1/get_devices
```

The answer should be: 

```
{
  "datastreams": [
    {"UUID": "1002345", "color": {"r": 0, "g": 0, "b": 255}},
    {"UUID": "299345", "color": {"r": 255, "g": 0, "b": 0}}
  ]
}
```

#### Connect to websocket 

Make sure wscat is installed on your system. 

Type the following in your CLI : 
```
wscat -c ws://localhost:8080/v1/subscribe_ws
```

A websocket connection should open in your CLI. 

#### Receive data from the websocket 

Type the following command into your shell. 

```
1002345 299345 100 json
```

The first two strings are the UUIDs of the datastreams. 
The third string is the sampling rate of the datastreams. 
The fourth string is the format of the datastream. 

The answer should be printed into your CLI and look something like this: 
{
  "timestamp": 1742455130.314,
  "datastreams": ["1002345", "299345"],
  "data": [
    [0.0, 1.0]
  ]
}

You can change the strings and try out which answers you get. 
Possible formats are json and csv. 






