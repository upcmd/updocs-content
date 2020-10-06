---
title: "c0133_vvvv"
date: 2020-10-06T23:46:15+1010:00
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
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0133
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
      "c": "global_ccc",
      "goahead": false,
      "a": "global_aaa",
      "b": "global_bbb"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "c": "global_ccc",
      "goahead": false,
      "a": "global_aaa",
      "b": "global_bbb"
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
      "db": "local_db",
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "goahead": false,
      "up_runtime_task_layer_number": 0,
      "da": "local_da"
    })
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "da": "local_da",
      "db": "local_db",
      "c": "global_ccc",
      "goahead": false,
      "a": "local_aaa",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "a": "local_aaa",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "c": "global_ccc"
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
      "b": "local_bbb",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step2\"",
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "db": "local_db",
      "da": "local_da",
      "c": "global_ccc",
      "goahead": false,
      "a": "block_layer1_aaa"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "a": "block_layer1_aaa",
      "b": "local_bbb",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step2\"",
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "db": "local_db_layer1",
      "da": "local_da",
      "c": "global_ccc"
    })
    
    ~SubStep1: [print:  ]
    layer 1
    up_runtime_task_layer_number: 0
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
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step2\"",
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "c": "global_ccc",
      "goahead": false,
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "a": "local_aaa"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "a": "local_aaa",
      "b": "local_bbb",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step2\"",
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "c": "global_ccc"
    })
    
    cmd( 1):
    echo "shell step3"
    
    cmd=>:
    echo "shell step3"
    -
    shell step3
    
    -
     .. ok
    cmd( 2):
    echo "shell step4"
    
    cmd=>:
    echo "shell step4"
    -
    shell step4
    
    -
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
      "c": "global_ccc",
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "goahead": false
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "local_block_layer2_aaa",
      "b": "local_block_layer2_bbb",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step4\"",
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      }),
      "c": "global_ccc",
      "up_runtime_task_layer_number": 0,
      "da": "local_da_layer2",
      "db": "local_db_layer2",
      "goahead": false
    })
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "db": "local_db_layer2",
      "c": "global_ccc",
      "goahead": false,
      "a": "block_layer2_aaa",
      "b": "local_block_layer2_bbb",
      "up_runtime_task_layer_number": 0,
      "da": "local_da_layer2"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "da": "local_da_layer2",
      "db": "local_db_layer2",
      "c": "global_ccc",
      "goahead": false,
      "a": "block_layer2_aaa",
      "b": "local_block_layer2_bbb",
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    layer 2
    up_runtime_task_layer_number: 0
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
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "c": "global_ccc",
      "goahead": false,
      "a": "local_aaa",
      "b": "local_bbb"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "db": "local_db",
      "c": "global_ccc",
      "goahead": false,
      "a": "local_aaa",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 0,
      "da": "local_da"
    })
    
    cmd( 1):
    echo "shell step5"
    
    cmd=>:
    echo "shell step5"
    -
    shell step5
    
    -
     .. ok
    cmd( 2):
    echo "shell step6"
    
    cmd=>:
    echo "shell step6"
    -
    shell step6
    
    -
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
