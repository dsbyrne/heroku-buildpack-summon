# heroku-buildpack-summon
Buildpack to run your Heroku application with Summon

## Getting Started
First, add this buildpack to your Heroku app.
```
$ heroku buildpacks:add --app my-app https://github.com/dsbyrne/heroku-buildpack-summon.git
```

This buildpack will require a few prerequisites:
1. Your app slug contains a `secrets.yml` in the root directory. [Read more here](http://conjurinc.github.io/summon).
2. You have a Procfile which invokes Summon.  
    `web: ./summon node src/server.js`
3. The following Config Variables have been set:
    - CONJUR_ACCOUNT
    - CONJUR_APPLIANCE_URL
    - CONJUR_AUTHN_API_KEY
    - CONJUR_SSL_CERTIFICATE 

You can read more on what these variables are here:
https://developer.conjur.net/key_concepts/machine_identity.html
