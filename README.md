# go-weather-app
## objective
Fetch current temperature of any city in Kelvin by hitting api provided by OpenWeather.org in the browser.
URL: localhost:8080/weather/<city>
## required files
two files required:
- .apiConfig : to store the api key
- main.go : actual application
## required packages
- io/ioutil
- encoding/json
- net/http
- strings
## types
create two custom data types using struct for storing:
- api key data stored in the .apiConfig file
- weather temp data coming from api
## funcs
4 funcs including main func.
1. a func to load the api key into a var using the ioutil pkg. ioutil.ReadFile() func helps reading the file supplied.
2. a hello func to confirm if the web server is working. just use the http.ResponseWriter to write out "hello from go"
3. a query func to actually query the api and store the temp data into a var. this func uses func1 to load the api key first. then it hits the api using http.Get method (URL as param). use json pkg to decode the response and store in a var.
4. main func which defines the routes to access hello and query func and encode the response from web server using json pkg. it also has http.ListenAndServe func which serves files on port 8080.