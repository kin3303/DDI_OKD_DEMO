## DDI_OKD_DEMO

Openshift 에서 nodejs app 배포를 위한 Demo Project


### Step 1 > Jenkins 설정

```
Credentials
    Add Credentials
        Kind : Username with password
        Scope : Global
        Username : dockerHub 계정명
        Password : dockerHub 패스워드
        ID : docker-hub
        Description : docker-hub
        
New Item
    ItemName : nodejs-pipe
    ItemType : Pipeline
    
Configure
    Advanced Project Options
        Pipeline
            Definition : Pipeline script from SCM
            SCM : Git
            Repository URL : https://github.com/kin3303/DDI_OKD_DEMO.git
            Branches to build : */master
            Script Path : misc/Jenkinsfile
```

### Reference

- https://www.jenkins.io/doc/book/pipeline/docker/
- https://docs.cloudbees.com/docs/admin-resources/latest/plugins/docker-workflow
