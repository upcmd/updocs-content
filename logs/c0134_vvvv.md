---
title: "c0134_vvvv"
date: 2020-10-06T23:46:16+1010:00
draft: false
weight: 11343

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0134
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
    loading [Task]:  ./tests/functests/c0134
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
      "c": "global_ccc",
      "a": "global_aaa",
      "b": "global_bbb"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "c": "global_ccc",
      "a": "local_aaa",
      "up_runtime_task_layer_number": 0,
      "b": "local_bbb"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db"
    })
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "a": "local_aaa",
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "b": "local_bbb",
      "c": "global_ccc"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "da": "local_da",
      "db": "local_db",
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "in block"
    
    cmd=>:
    echo "in block"
    -
    in block
    
    -
     .. ok
    . ok
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "c": "global_ccc",
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "a": "local_aaa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"in block\"",
        Code: 0,
        Output: "in block",
        ErrMsg: ""
      }),
      "b": "local_bbb"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "c": "global_ccc",
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "a": "local_aaa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"in block\"",
        Code: 0,
        Output: "in block",
        ErrMsg: ""
      }),
      "b": "local_bbb"
    })
    
      located task-> 2 [callee_task]: 
    =Task2: [task ==> callee_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "c": "global_ccc",
      "up_runtime_task_layer_number": 1,
      "da": "local_da",
      "db": "local_db",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"in block\"",
        Code: 0,
        Output: "in block",
        ErrMsg: ""
      }),
      "b": "local_bbb",
      "a": "local_aaa"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "da": "local_da",
      "db": "callee_db",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"in block\"",
        Code: 0,
        Output: "in block",
        ErrMsg: ""
      }),
      "b": "local_bbb",
      "a": "local_aaa",
      "c": "global_ccc"
    })
    
    ~~SubStep1: [print:  ]
    layer 1
    up_runtime_task_layer_number: 1
    a: local_aaa
    b: local_bbb
    c: global_ccc
    da: local_da
    db: callee_db
    
    ~~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .a "local_aaa" }}]
     2 ASSERT OK:     [{{eq .b "local_bbb" }}]
     3 ASSERT OK:     [{{eq .c "global_ccc" }}]
     4 ASSERT OK:     [{{eq .da "local_da" }}]
     5 ASSERT OK:     [{{eq .db "callee_db" }}]
    
```

##### Logs with different verbose level
* [c0134 log - verbose level v](../../logs/c0134_v)
* [c0134 log - verbose level vv](../../logs/c0134_vv)
* [c0134 log - verbose level vvv](../../logs/c0134_vvv)
* [c0134 log - verbose level vvvv](../../logs/c0134_vvvv)
* [c0134 log - verbose level vvvvv](../../logs/c0134_vvvvv)

##### References
* [Related Chapter](../../block-func/c0134)
