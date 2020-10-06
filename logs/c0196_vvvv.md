---
title: "c0196_vvvv"
date: 2020-10-06T23:46:28+1010:00
draft: false
weight: 11963

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0196
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0196
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
      "my_secrete_file_reg_name": "my_secret"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "my_secrete_file_reg_name": "my_secret"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "my_secrete_file_reg_name": "my_secret",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "my_secrete_file_reg_name": "my_secret",
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [tmpFile:  ]
    tmp file handler: my_secret
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "my_secret": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84431071298",
      "my_secrete_file_reg_name": "my_secret"
    })
    
    dvar> filepath:
    "/tmp/BpLnfgDsc2WD8F2qNfHK5a84431071298"
    
    -
    /tmp/BpLnfgDsc2WD8F2qNfHK5a84431071298
    self: final context exec vars:
    
    (*core.Cache)({
      "my_secret": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84431071298",
      "my_secrete_file_reg_name": "my_secret",
      "up_runtime_task_layer_number": 0,
      "filepath": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84431071298"
    })
    
    ~SubStep1: [inspect:  ]
     1: inspect[debug_vars]
    -debug vars-
    "UpRunTimeVars"
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    "RuntimeVarsAndDvarsMerged"
    (*core.Cache)({
      "my_secrete_file_reg_name": "my_secret",
      "my_secret": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84431071298"
    })
    
    "ExecbaseVars"
    (*core.Cache)({
      "my_secrete_file_reg_name": "my_secret",
      "my_secret": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84431071298"
    })
    
    "TaskVars"
    (*core.Cache)({
    })
    
    "ExecContextVars"
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "filepath": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84431071298",
      "my_secret": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84431071298",
      "my_secrete_file_reg_name": "my_secret"
    })
    
    --
    ~SubStep2: [readFile:  ]
    ~SubStep3: [print:  ]
    file content: hello, world
    
```

##### Logs with different verbose level
* [c0196 log - verbose level v](../../logs/c0196_v)
* [c0196 log - verbose level vv](../../logs/c0196_vv)
* [c0196 log - verbose level vvv](../../logs/c0196_vvv)
* [c0196 log - verbose level vvvv](../../logs/c0196_vvvv)
* [c0196 log - verbose level vvvvv](../../logs/c0196_vvvvv)

##### References
* [Related Chapter](../../cmd-func/c0196)
