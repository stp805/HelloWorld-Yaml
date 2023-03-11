# HelloWorld-Yaml
using openapi (swaggerapi) make a yaml file

# using the OpenAPI Generator for templated source code initilalisation (back-end), below option uses cpp-pistache for restfull services
1. Downalod openapi-generator-cli.jar
```bash
wget https://repo1.maven.org/maven2/org/openapitools/openapi-generator-cli/6.3.0/openapi-generator-cli-6.3.0.jar -O openapi-generator-cli.jar
```
2. Create the very basic SRC Code, Business Logic, DB Integration and Database schema needs to be updated.
```bash
java -jar openapi-generator-cli.jar generate -g cpp-pistache-server -o <PATH FOR OUTPUT SRC FILE DIRECTORY> -i <PATH OF openapi .yaml file>/openapi.yaml
```
#after step 2 src code is initialise at mentioned path.. go inside the Creted Folder for installation.
## Installation
First of all, you need to download and install the libraries listed [here](#libraries-required).

Once the libraries are installed, in order to compile and run the server please follow the steps below:
```bash
mkdir build
cd build
cmake ..
make
```

Once compiled run the server:

```bash
cd build
./api-server
```

## Libraries required
- [pistache](http://pistache.io/quickstart)
- [JSON for Modern C++](https://github.com/nlohmann/json/#integration): Please download the `json.hpp` file and
put it under the model/nlohmann folder

server addr: http://127.0.01:9000

## execute the creted binary
in bash you may use below curl command 
```bash
  curl -X GET http://127.0.0.1:9000/
```
