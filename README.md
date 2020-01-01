# :package: :sparkles: Serverless Static Plugin
[![serverless](http://public.serverless.com/badges/v3.svg)](http://www.serverless.com)

## Note

Deploy functionality is in active development, it soon will be available

## 1.install the plugin

First, add Serverless Static to your project, be sure that you already have the [serverless-offline](https://github.com/dherault/serverless-offline) plugin already installed

```
$ npm install serverless-static --save-dev
```

> or, if serverless-offline is not already installed

```
$ npm install serverless-static serverless-offline --save-dev
```

## 2. add it to your serverless.yml file

Then inside your project's serverless.yml file add following entry to the plugins section: serverless-static. If there is no plugin section you will need to add it to the file.

It should look something like this:

```YAML
plugins:
  - serverless-offline
  - serverless-static
```

## 3. customize behavior (optional)

```YAML
custom:
  static:
    path: ./public # select the folder you want to serve
    port: 8000 # select a specific port
    headers:
      - Access-Control-Allow-Origin: "*"
      - Access-Control-Allow-Headers: "Content-Type,X-Requested-With"
      - Access-Control-Allow-Methods: "PUT,POST,GET,DELETE,OPTIONS"

# this will overide default behavior
# it will serve the folder ./public
# it will serve it throught localhost:8000
```

<!-- ## Todo

- [ ] support for serving multiple directories
- [ ] deploy / sync folder and bucket -->
