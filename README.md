# Repo for hacking on composer functions and features

This branch is for testing if `mouf/nodejs-installer` will correctly install Node.js 
in `FLOW_PATH_ROOT/Data/Temporary/Binaries/RafaelKa.EmberApp/nodejs` directory.

Check this directory after running 
`composer require rafaelka/composer-study:dev-nodejs-installer` 
for existency of Node.js binaries.

As you can see here is nothing happen, except mouf/nodejs-installer package was installed.

To trigger Downloading you want to add following snippet in Flows root composer.json file:

```
    "extra": {
        "mouf": {
            "nodejs": {
                "version": "5.4.1",
                "targetDir": "Data/Temporary/Binaries/Neos.Flow/nodejs",
                "forceLocal": true
            }
        }
    }
```

Current version of `mouf/nodejs-installer` is not compatible with Flow because of [following lines](https://github.com/thecodingmachine/nodejs-installer/blob/1.0/src/NodeJsInstaller.php#L201-L202)

Nonetheless `mouf/nodejs-installer` is very nice composer plugin, which shows that you can bring anything into your PHP App.
