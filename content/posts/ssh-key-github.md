+++
title = "Specify an SSH key for git push"
+++

## USE CASE

I would like to able to push to github using a different ssh key, like `id_rsa-github` rather the default `id_rsa`.

### Solution 1
First, edit the ssh config file

``` 
Host github
	HostName 	github.com
	User		git
	IdentityFile    ~/.ssh/id_rsa-github
	IdentitiesOnly  yes
```

then 
```sh
git remote set-url origin github:xhorn-pan/xhorn-pan.github.io.git
```