## Multiple bitbucket/git acocunt configuration 

You can add two Bitbucket "accounts" in your ssh config file. Bitbucket has alternative ssh host listening on port 443 (For those who has blocked almost all ports (sic!)).
```
Host bitbucketCompany
    User git
    HostName altssh.bitbucket.org
    Port 443
    IdentityFile ~/.ssh/company_id_rsa
```

```
Host bitbucketWork
    User git
    HostName bitbucket.org
    Port 22
    IdentityFile ~/.ssh/personal_id_rsa
Then update your remotes in .git/config
```
Company projects
```
[remote "origin"]
    url = ssh://bitbucketCompany/username/repo.git
Personal projects

[remote "origin"]
    url = ssh://bitbucketPersonal/username/repo.git
    
```
