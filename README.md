# Go Swagger Tools

## Swagger Editor
[Swagger Editor](https://github.com/swagger-api/swagger-editor)

To run it in local environment:
> docker pull swaggerapi/swagger-editor
>
> docker run -d -p 80:8080 swaggerapi/swagger-editor
>
> open a browser, and point to 127.0.0.1 to start using editor
>
> Change 80 to something else if there is port conflict.

**Notes**

Do not use built-in code generation tool to generate goLang code from the spec. The code generator comes with the editor is based on swagger-codegen project, which is deprecated. Use the tool specified in the [next section](#go-swagger).

## Go-Swagger
[go-swagger](https://github.com/go-swagger/go-swagger)
To run it in local environment:
> docker pull quay.io/goswagger/swagger
>
> Add the following line to ~/.bash_profile, then source ~/.bash_profile
>
> alias swagger="docker run --rm -it -e GOPATH=$GOPATH:/go -v $GOPATH:$GOPATH -w $(pwd) quay.io/goswagger/swagger" 
> swagger version

To generate server code from swagger spec:
> Use [editor](#swagger-editor) to compose an api spec in Yaml, then save as json, e.g., test1.json.
>
> cd to where json file is saved
>
> swagger generate server -f ./test1.json 



## Openapi-Generater
TODO: https://github.com/OpenAPITools/openapi-generator
