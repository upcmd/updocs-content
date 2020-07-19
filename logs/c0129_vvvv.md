---
title: "c0129_vvvv"
date: 2020-07-20T02:01:52+77:00
draft: false
weight: 11293

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0129
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0129
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [self] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "a": "global_aaa",
      "b": "global_bbb",
      "c": "global_ccc"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "c": "global_ccc",
      "a": "global_aaa",
      "b": "global_bbb"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: show example the route goes to call goelse for the condition of not if condition succeeds ]
    current exec runtime vars:
    (*core.Cache)({
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "c": "global_ccc",
      "a": "local_aaa",
      "b": "local_bbb",
      "da": "local_da",
      "db": "local_db"
    })
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "db": "local_db",
      "c": "global_ccc",
      "a": "local_aaa",
      "b": "local_bbb",
      "da": "local_da"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "c": "global_ccc",
      "a": "local_aaa",
      "b": "local_bbb",
      "da": "local_da",
      "db": "local_db"
    })
    
    cmd( 1):
    echo "shell step1"
    
    cmd=>:
    echo "shell step1"<=
    shell step1
     .. ok
    cmd( 2):
    echo "shell step2"
    
    cmd=>:
    echo "shell step2"<=
    shell step2
     .. ok
    . ok
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "b": "local_bbb",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step2\"",
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "da": "local_da",
      "db": "local_db",
      "c": "global_ccc",
      "a": "block_layer1_aaa"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "c": "global_ccc",
      "a": "block_layer1_aaa",
      "b": "local_bbb",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step2\"",
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "da": "local_da",
      "db": "local_db"
    })
    
    ~SubStep1: [print:  ]
    layer 1
    up_runtime_task_layer_number: <no value>
    a: block_layer1_aaa
    b: local_bbb
    c: global_ccc
    da: local_da
    db: local_db
    
    -Step3:
    current exec runtime vars:
    (*core.Cache)({
      "db": "local_db",
      "c": "global_ccc",
      "a": "local_aaa",
      "b": "local_bbb",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step2\"",
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "da": "local_da"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "c": "global_ccc",
      "a": "local_aaa",
      "b": "local_bbb",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step2\"",
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "da": "local_da",
      "db": "local_db"
    })
    
    cmd( 1):
    echo "shell step3"
    
    cmd=>:
    echo "shell step3"<=
    shell step3
     .. ok
    cmd( 2):
    echo "shell step4"
    
    cmd=>:
    echo "shell step4"<=
    shell step4
     .. ok
    . ok
    -Step4: [: test embeded 2nd layer of block ]
    current exec runtime vars:
    (*core.Cache)({
      "a": "local_block_layer2_aaa",
      "b": "local_block_layer2_bbb",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step4\"",
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      }),
      "da": "local_da",
      "db": "local_db",
      "c": "global_ccc"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "c": "global_ccc",
      "a": "local_block_layer2_aaa",
      "b": "local_block_layer2_bbb",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step4\"",
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      }),
      "da": "local_da_layer2",
      "db": "local_db_layer2"
    })
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "db": "local_db_layer2",
      "da": "local_da_layer2",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step4\"",
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      }),
      "c": "global_ccc",
      "a": "block_layer2_aaa",
      "b": "local_block_layer2_bbb"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step4\"",
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      }),
      "c": "global_ccc",
      "a": "block_layer2_aaa",
      "b": "local_block_layer2_bbb",
      "db": "local_db_layer2",
      "da": "local_da_layer2"
    })
    
    ~SubStep1: [print:  ]
    layer 2
    up_runtime_task_layer_number: <no value>
    a: block_layer2_aaa
    b: local_block_layer2_bbb
    c: global_ccc
    da: local_da_layer2
    db: local_db_layer2
    
    -Step5:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step4\"",
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      }),
      "db": "local_db",
      "da": "local_da",
      "c": "global_ccc",
      "a": "local_aaa",
      "b": "local_bbb"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "c": "global_ccc",
      "a": "local_aaa",
      "b": "local_bbb",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step4\"",
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      }),
      "db": "local_db",
      "da": "local_da"
    })
    
    cmd( 1):
    echo "shell step5"
    
    cmd=>:
    echo "shell step5"<=
    shell step5
     .. ok
    cmd( 2):
    echo "shell step6"
    
    cmd=>:
    echo "shell step6"<=
    shell step6
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0129 log - verbose level v](../../logs/c0129_v)
* [c0129 log - verbose level vv](../../logs/c0129_vv)
* [c0129 log - verbose level vvv](../../logs/c0129_vvv)
* [c0129 log - verbose level vvvv](../../logs/c0129_vvvv)
* [c0129 log - verbose level vvvvv](../../logs/c0129_vvvvv)

##### References
* [Related Chapter](../../block-func/c0129)
