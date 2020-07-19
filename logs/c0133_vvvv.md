---
title: "c0133_vvvv"
date: 2020-07-20T02:01:53+77:00
draft: false
weight: 11333

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0133
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0133
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
      "b": "global_bbb",
      "c": "global_ccc",
      "a": "global_aaa"
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
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "db": "local_db",
      "da": "local_da"
    })
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "db": "local_db",
      "da": "local_da"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "db": "local_db",
      "da": "local_da",
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa"
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
      "c": "global_ccc",
      "a": "block_layer1_aaa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step2\"",
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "da": "local_da",
      "db": "local_db"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "block_layer1_aaa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step2\"",
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "da": "local_da",
      "db": "local_db_layer1"
    })
    
    ~SubStep1: [print:  ]
    layer 1
    up_runtime_task_layer_number: <no value>
    a: block_layer1_aaa
    b: local_bbb
    c: global_ccc
    da: local_da
    db: local_db_layer1
    
    ~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .a "block_layer1_aaa" }}]
     2 ASSERT OK:     [{{eq .b "local_bbb" }}]
     3 ASSERT OK:     [{{eq .c "global_ccc" }}]
     4 ASSERT OK:     [{{eq .da "local_da" }}]
     5 ASSERT OK:     [{{eq .db "local_db_layer1" }}]
    -Step3:
    current exec runtime vars:
    (*core.Cache)({
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step2\"",
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "db": "local_db",
      "da": "local_da"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "db": "local_db",
      "da": "local_da",
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step2\"",
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      })
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
      "db": "local_db",
      "da": "local_da",
      "a": "local_block_layer2_aaa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step4\"",
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      }),
      "b": "local_block_layer2_bbb",
      "c": "global_ccc"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step4\"",
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      }),
      "b": "local_block_layer2_bbb",
      "c": "global_ccc",
      "db": "local_db_layer2",
      "da": "local_da_layer2",
      "a": "local_block_layer2_aaa"
    })
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "b": "local_block_layer2_bbb",
      "c": "global_ccc",
      "a": "block_layer2_aaa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step4\"",
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      }),
      "db": "local_db_layer2",
      "da": "local_da_layer2"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "b": "local_block_layer2_bbb",
      "c": "global_ccc",
      "a": "block_layer2_aaa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step4\"",
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      }),
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
    
    ~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .a "block_layer2_aaa" }}]
     2 ASSERT OK:     [{{eq .b "local_block_layer2_bbb" }}]
     3 ASSERT OK:     [{{eq .c "global_ccc" }}]
     4 ASSERT OK:     [{{eq .da "local_da_layer2" }}]
     5 ASSERT OK:     [{{eq .db "local_db_layer2" }}]
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
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "local_aaa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step4\"",
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      }),
      "db": "local_db",
      "da": "local_da",
      "b": "local_bbb",
      "c": "global_ccc"
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
* [c0133 log - verbose level v](../../logs/c0133_v)
* [c0133 log - verbose level vv](../../logs/c0133_vv)
* [c0133 log - verbose level vvv](../../logs/c0133_vvv)
* [c0133 log - verbose level vvvv](../../logs/c0133_vvvv)
* [c0133 log - verbose level vvvvv](../../logs/c0133_vvvvv)

##### References
* [Related Chapter](../../test-debug/c0133)
