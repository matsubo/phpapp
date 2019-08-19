# PHP Deployer sample setting.

[Deployer](https://deployer.org) live sample app.

The master branch is deployed to the following URL.
http://phpapp.teraren.com/


## Setup

```
% git clone git@github.com:matsubo/phpapp.git
% cd phpapp
% composer install
```

## Command example

```
% time php vendor/bin/dep deploy test
✈︎ Deploying master on blog.teraren.com
✔ Executing task deploy:prepare
✔ Executing task deploy:lock
✔ Executing task deploy:release
➤ Executing task deploy:update_code
Cloning into '/home/matsu/Sites/teraren.com/phpapp/releases/2'...
Counting objects: 36, done.
Delta compression using up to 2 threads.
Compressing objects: 100% (16/16), done.
Writing objects: 100% (36/36), done.
Total 36 (delta 12), reused 36 (delta 12)
Connection to blog.teraren.com closed.
✔ Ok
✔ Executing task deploy:shared
✔ Executing task deploy:writable
✔ Executing task deploy:vendors
✔ Executing task deploy:clear_paths
✔ Executing task deploy:symlink
✔ Executing task deploy:unlock
✔ Executing task cleanup
Successfully deployed!
       15.56 real         0.65 user         0.60 sys
```


## Setup history

```
% composer init
% composer require deployer/deployer --dev
% php vendor/bin/dep init
% vim deploy.php; vim hosts.yml
```


