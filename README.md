## Bitbucket Nodejs Library
 
  This is nodejs module to use the repository, deploy-keys, service hooks functionalities of bitbucket. Bitbucket's native rest API, both version 1 & 2 is used for appropriate actions.

## Install

To install the most recent release from npm, run:

    npm install bitbucket-rest


A simple example of to create a bitbucket client.

```javascript
  var bitbucket = require('bitbucket-rest');                                            a
  var client = bitbucket.connectClient({username : 'user', password : 'pass'});
  
  client.getRepoDetails({owner:'owner_name', repo_slug : 'repo_slug'}, function(res){
     callback(res);
  });
  
```


## Documentation


### Get Repository Details

To get complete detail about the repositiry.


```javascript
  client.getRepoDetails(req, callback)
```

Parameters of `req`:

  * `.owner` owner of the repository - REQUIRED.
  * `.repo_slug` slug of the repository - REQUIRED.
  

This returns following object:

```javascript
  { 
    status : 200,
    data : [object]
  }
```



### Create New Repository

To create a new repositiry.


```javascript
  client.createRepo(req, callback)
```

Parameters of `req`:

  * `.owner` owner of the repository - REQUIRED.
  * `.repo_slug` slug of the repository - REQUIRED.
  * `.name` name of the repository.
  * `.description` description for the repository.
  * `.is_private` 
  * `.forking_policy` fork policy values - 'no_public_forks', 'allow_forks', 'no_forks'
  

This returns following object:

```javascript
  { 
    status : 200,
    data : [object]
  }
```

