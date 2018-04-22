# Containerized Model Serving using Scikit-Learn and Docker


## Build the docker image
`$ docker build -t sklearn-docker .`

##### 4. Start a container
`$ docker run -p 15000:5000 microservice`


### You should see the following output:
```
vjain:docker vedantjain$ docker run -p 15000:5000 vedantja/model_microservice_example
 * Restarting with stat
 * Debugger is active!
 * Debugger PIN: 556-327-343
 * Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)
```
#### The application is running on port 5000. So open another terminal window and submit the following command:

<code>$ curl -H 'Content-Type:application/json' -d '{"x": -39.578, "y": -22.41,  "z": 39.21, "User": "a", "Model": "gear_2", "Device": "gear"}' localhost:5000<</code>


### You will see the following output in the new window:
```
{"prediction":"walk"}
```
