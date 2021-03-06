sa-mongo
========

[![Build Status](https://travis-ci.org/softasap/sa-mongo.svg?branch=master)](https://travis-ci.org/softasap/sa-mongo)


Role to install MongoDB 2.4 2.6 3.4 or 3.6 on ubuntu based box.


| Distribution |   MongoDB 2.6 | MongoDB 3.2 | MongoDB 3.4 | MongoDB 3.6 |
| ------------ |:-------------:|:-----------:|:-----------:|:-----------:|
| Ubuntu 14.04 | :white_check_mark: | :white_check_mark:| :white_check_mark:| :no_entry:|
| Ubuntu 16.04 | :no_entry: | :white_check_mark:| :white_check_mark:| :white_check_mark:|
| Ubuntu 18.04 | :no_entry: | :white_check_mark:| :white_check_mark:| :white_check_mark:|

- :white_check_mark: - should work fine
- :interrobang: - there were no production deploys for a while
- :no_entry: - not recommended for installation

Check for mongodb EOL for versions.  Generally, you should target latest or previous release.
Historic releases are provided for compability with old deployments that were using that role.

Check current travis tests  https://travis-ci.org/softasap/sa-mongo/builds   


Version is controlled by  mongo_version parameter.

```
mongo_version: "3.4"  #  "2.6" | "3" | "3.2" | "3.4" | "3.6"
mongo_family: "org" # "org" | "enterprise"
```


Example:

Simple

```YAML


     - {
         role: "sa-mongo",
         mongo_version: "3.4"
       }

```

Advanced:

```YAML


     - {
         role: "sa-mongo",
         mongo_version: "3.4",
         mongo_family: "enterprise"
       }

```




Usage with ansible galaxy workflow
----------------------------------

If you installed the sa-mongo role using the command


`
   ansible galaxy install softasap.sa-mongo
`

the role will be available in the folder library\softasap.mongo.
Please adjust the path accordingly.

```YAML

     - {
         role: "softasap.mongo"
       }

```


Copyright and license
---------------------

Code is dual licensed under the [BSD 3 clause] (https://opensource.org/licenses/BSD-3-Clause) and the [MIT License] (http://opensource.org/licenses/MIT). Choose the one that suits you best.

Reach us:

Subscribe for roles updates at [FB] (https://www.facebook.com/SoftAsap/)

Join gitter discussion channel at [Gitter](https://gitter.im/softasap)

Discover other roles at  http://www.softasap.com/roles/registry_generated.html

visit our blog at http://www.softasap.com/blog/archive.html
