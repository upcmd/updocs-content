---
title: "c0128_vvvv"
date: 2020-10-07T00:11:22+1010:00
draft: false
weight: 11283

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0128
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
    loading [Task]:  ./tests/functests/c0128
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
      "b": "global_bbb",
      "c": "global_ccc",
      "a": "global_aaa"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "a": "global_aaa",
      "b": "global_bbb",
      "c": "global_ccc"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: show example the route goes to call goelse for the condition of not if condition succeeds ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "c": "global_ccc",
      "a": "local_aaa",
      "b": "local_bbb"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "db": "local_db",
      "c": "global_ccc",
      "a": "local_aaa",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 0,
      "da": "local_da"
    })
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "a": "local_aaa",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "c": "global_ccc"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "c": "global_ccc",
      "a": "local_aaa",
      "b": "local_bbb"
    })
    
    cmd( 1):
    echo "shell step1"
    
    cmd=>:
    echo "shell step1"
    -
    shell step1
    
    -
     .. ok
    cmd( 2):
    echo "shell step2"
    
    cmd=>:
    echo "shell step2"
    -
    shell step2
    
    -
     .. ok
    . ok
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step2\"",
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step2\"",
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db"
    })
    
    ~SubStep1: [print:  ]
    cmd print step
    up_runtime_task_layer_number: 0
    a: local_aaa
    b: local_bbb
    da: local_da
    db: local_db
    
    
```

##### Logs with different verbose level
* [c0128 log - verbose level v](../../logs/c0128_v)
* [c0128 log - verbose level vv](../../logs/c0128_vv)
* [c0128 log - verbose level vvv](../../logs/c0128_vvv)
* [c0128 log - verbose level vvvv](../../logs/c0128_vvvv)
* [c0128 log - verbose level vvvvv](../../logs/c0128_vvvvv)

##### References
* [Related Chapter](../../block-func/c0128)
