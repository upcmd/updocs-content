---
title: "0014_vvvv"
date: 2020-10-07T00:12:05+1010:00
draft: false
weight: 101403

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/modtests/0014/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/modtests/0014
                 WorkDir -> refdir
              AbsWorkDir -> /up_project/up/tests/modtests/0014
                TaskFile -> up.yml
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> Main
      ModRepoUsernameRef -> GIT_USERNAME
      ModRepoPasswordRef -> GIT_PASSWORD
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up/tests/modtests/0014
    -exec task: Main
    loading [Task]:  ./up.yml
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    dvar> github_password:
    "IXXDRoOJcdNTkQU3QlU0vY+LFA6fA/qB8IueX7WDLGL+5PsAPQGfolq+uXlAAHv8"
    
    -
    IXXDRoOJcdNTkQU3QlU0vY+LFA6fA/qB8IueX7WDLGL+5PsAPQGfolq+uXlAAHv8
    dvar> GITHUB_USERNAME:
    "my_github_username"
    
    -
    my_github_username
    dvar> GITHUB_PASSWORD_ENCRYPTED:
    "IXXDRoOJcdNTkQU3QlU0vY+LFA6fA/qB8IueX7WDLGL+5PsAPQGfolq+uXlAAHv8"
    
    -
    IXXDRoOJcdNTkQU3QlU0vY+LFA6fA/qB8IueX7WDLGL+5PsAPQGfolq+uXlAAHv8
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "github_password": "IXXDRoOJcdNTkQU3QlU0vY+LFA6fA/qB8IueX7WDLGL+5PsAPQGfolq+uXlAAHv8",
      "GITHUB_USERNAME": "my_github_username",
      "envVar_GITHUB_USERNAME": "my_github_username",
      "GITHUB_PASSWORD_ENCRYPTED": "IXXDRoOJcdNTkQU3QlU0vY+LFA6fA/qB8IueX7WDLGL+5PsAPQGfolq+uXlAAHv8",
      "envVar_GITHUB_PASSWORD_ENCRYPTED": "something_secret"
    })
    
      located task-> 1 [Main]: 
    Task1: [Main ==> Main: main entry ]
    Executing task stack layer: 1
    
    -Step1: [
    note that the module dir is: hello-module, but in upconfig.yml you give the alias hello as module name
    ]
    current exec runtime vars:
    (*core.Cache)({
      "GITHUB_PASSWORD_ENCRYPTED": "IXXDRoOJcdNTkQU3QlU0vY+LFA6fA/qB8IueX7WDLGL+5PsAPQGfolq+uXlAAHv8",
      "envVar_GITHUB_PASSWORD_ENCRYPTED": "something_secret",
      "github_password": "IXXDRoOJcdNTkQU3QlU0vY+LFA6fA/qB8IueX7WDLGL+5PsAPQGfolq+uXlAAHv8",
      "GITHUB_USERNAME": "my_github_username",
      "envVar_GITHUB_USERNAME": "my_github_username",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "GITHUB_USERNAME": "my_github_username",
      "envVar_GITHUB_USERNAME": "my_github_username",
      "up_runtime_task_layer_number": 0,
      "GITHUB_PASSWORD_ENCRYPTED": "IXXDRoOJcdNTkQU3QlU0vY+LFA6fA/qB8IueX7WDLGL+5PsAPQGfolq+uXlAAHv8",
      "envVar_GITHUB_PASSWORD_ENCRYPTED": "something_secret",
      "github_password": "IXXDRoOJcdNTkQU3QlU0vY+LFA6fA/qB8IueX7WDLGL+5PsAPQGfolq+uXlAAHv8"
    })
    
     WARN: [config file does not exist] - [use builtin defaults]
    loading [Task]:  ./up.yml
    module: [hello], instance id: [nonamed], exec profile: []
     WARN: [*be aware*] - [both instance id and exec profile are not set]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ nonamed ] runtime vars:
    (*core.Cache)({
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
    })
    
    =>call module: [hello] task: [Say_world]
    Executing tasker layer: 2
    
      located task-> 2 [Say_world]: 
    Task2: [TODO: Main Caller Taskname ==> Say_world:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "envVar_GITHUB_PASSWORD_ENCRYPTED": "something_secret",
      "github_password": "IXXDRoOJcdNTkQU3QlU0vY+LFA6fA/qB8IueX7WDLGL+5PsAPQGfolq+uXlAAHv8",
      "GITHUB_USERNAME": "my_github_username",
      "envVar_GITHUB_USERNAME": "my_github_username",
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 2,
      "GITHUB_PASSWORD_ENCRYPTED": "IXXDRoOJcdNTkQU3QlU0vY+LFA6fA/qB8IueX7WDLGL+5PsAPQGfolq+uXlAAHv8"
    })
    
    hello: final context exec vars:
    
    (*core.Cache)({
      "envVar_GITHUB_PASSWORD_ENCRYPTED": "something_secret",
      "github_password": "IXXDRoOJcdNTkQU3QlU0vY+LFA6fA/qB8IueX7WDLGL+5PsAPQGfolq+uXlAAHv8",
      "GITHUB_USERNAME": "my_github_username",
      "envVar_GITHUB_USERNAME": "my_github_username",
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 2,
      "GITHUB_PASSWORD_ENCRYPTED": "IXXDRoOJcdNTkQU3QlU0vY+LFA6fA/qB8IueX7WDLGL+5PsAPQGfolq+uXlAAHv8"
    })
    
    ~SubStep1: [print:  ]
     .... world from Say_world
    
```

##### Logs with different verbose level
* [m0014 log - verbose level v](../../logs/m0014_v)
* [m0014 log - verbose level vv](../../logs/m0014_vv)
* [m0014 log - verbose level vvv](../../logs/m0014_vvv)
* [m0014 log - verbose level vvvv](../../logs/m0014_vvvv)
* [m0014 log - verbose level vvvvv](../../logs/m0014_vvvvv)

##### References
* [Related Chapter](../../module/0014)
