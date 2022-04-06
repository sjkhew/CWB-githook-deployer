# CWB WebHook Deployer Script

- This is PHP webhook deployer script to auto git pull source code on server.

- This webhook script can be used in Github, Bitbucket and Gitlab.

- Use deploy.example.php as working script. **E.g. deploy.cwb2.php**

- Setup a webhook URL and Public Key at Github, Bitbucket and Gitlab.

## Configuration in deploy.example.php

```php
define("TOKEN", ""); // generate by "openssl rand -base64 32"
define("REMOTE_REPOSITORY", "git@github.com:username/reponame.git"); // edit repo remote address
define("DIR", "/var/www/html/reponame"); // repo path
define("BRANCH", "main"); // branch name
define("LOGFILE", "/var/www/html/githook/logs/".date('YmdHis')."_reponame_deploy.log"); // log path
define("GIT", "/usr/bin/git");
define("MAX_EXECUTION_TIME", 180);
define("BEFORE_PULL", "");
define("AFTER_PULL", "");
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
