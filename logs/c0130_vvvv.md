---
title: "c0130_vvvv"
date: 2020-10-07T00:11:23+1010:00
draft: false
weight: 11303

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0130
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
    loading [Task]:  ./tests/functests/c0130
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
      "goahead": false,
      "a": "global_aaa"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "a": "global_aaa",
      "b": "global_bbb",
      "c": "global_ccc",
      "goahead": false
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: show example the route goes to call goelse for the condition of not if condition succeeds ]
    current exec runtime vars:
    (*core.Cache)({
      "c": "global_ccc",
      "goahead": false,
      "up_runtime_task_layer_number": 0,
      "a": "local_aaa",
      "b": "local_bbb"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "db": "local_db",
      "da": "local_da",
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "goahead": false
    })
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "goahead": false,
      "up_runtime_task_layer_number": 0,
      "db": "local_db",
      "da": "local_da"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "da": "local_da",
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "goahead": false,
      "up_runtime_task_layer_number": 0,
      "db": "local_db"
    })
    
    cmd( 1):
    echo "else step1"
    
    cmd=>:
    echo "else step1"
    -
    else step1
    
    -
     .. ok
    cmd( 2):
    echo "else step2"
    
    cmd=>:
    echo "else step2"
    -
    else step2
    
    -
     .. ok
    . ok
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "db": "local_db",
      "da": "local_da",
      "a": "block_layer1_aaa_else",
      "b": "local_bbb",
      "c": "global_ccc",
      "goahead": false,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"else step2\"",
        Code: 0,
        Output: "else step2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "c": "global_ccc",
      "goahead": false,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"else step2\"",
        Code: 0,
        Output: "else step2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "db": "local_db",
      "da": "local_da",
      "a": "block_layer1_aaa_else",
      "b": "local_bbb"
    })
    
    ~SubStep1: [print:  ]
    layer 1
    up_runtime_task_layer_number: 0
    a: block_layer1_aaa_else
    b: local_bbb
    c: global_ccc
    da: local_da
    db: local_db
    
    
```

##### Logs with different verbose level
* [c0130 log - verbose level v](../../logs/c0130_v)
* [c0130 log - verbose level vv](../../logs/c0130_vv)
* [c0130 log - verbose level vvv](../../logs/c0130_vvv)
* [c0130 log - verbose level vvvv](../../logs/c0130_vvvv)
* [c0130 log - verbose level vvvvv](../../logs/c0130_vvvvv)

##### References
* [Related Chapter](../../block-func/c0130)
