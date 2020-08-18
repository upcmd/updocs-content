---
title: "0004_vvvv"
date: 2020-08-18T15:16:52+88:00
draft: false
weight: 100403

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/modtests/0004/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/modtests/0004
                 WorkDir -> refdir
              AbsWorkDir -> /up_project/up/tests/modtests/0004
                TaskFile -> up.yml
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up/tests/modtests/0004
    -exec task: Main
    loading [Task]:  ./up.yml
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
      located task-> 1 [Main]: 
    Task1: [Main ==> Main: main entry ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
    })
    
      located task-> 2 [internal_task]: 
    =Task2: [Main ==> internal_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    this is a internal task in caller
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    ls -lart
    
    cmd=>:
    ls -lart
    -
    total 12
    -rw-r--r--    1 root     root           253 Jun 11 09:38 upconfig.yml
    -rw-r--r--    1 root     root           521 Jun 11 09:38 up.yml
    drwxr-xr-x    3 root     root            96 Jun 11 09:38 hello-module
    -rw-r--r--    1 root     root          1019 Jun 11 09:38 doc.yml
    drwxr-xr-x    6 root     root           192 Jun 11 09:38 .
    drwxr-xr-x   18 root     root           576 Jul 18 17:03 ..
    -
     .. ok
    cmd( 2):
    ls |grep up
    
    cmd=>:
    ls |grep up
    -
    up.yml
    upconfig.yml
    -
     .. ok
    cmd( 3):
    pwd
    
    cmd=>:
    pwd
    -
    /up_project/up/tests/modtests/0004
    -
     .. ok
    cmd( 4):
    ls ../..|grep modtests
    
    cmd=>:
    ls ../..|grep modtests
    -
    modtests
    -
     .. ok
    . ok
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
     WARN: [config file does not exist] - [use builtin defaults]
    loading [Task]:  ./up.yml
    module: [hello-module], instance id: [nonamed], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ nonamed ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
    =>call module: [hello-module] task: [Say_world]
    Executing tasker layer: 2
    
      located task-> 1 [Say_world]: 
    Task1: [TODO: Main Caller Taskname ==> Say_world:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1
    })
    
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2
    })
    
    cmd( 1):
    ls -lart
    
    cmd=>:
    ls -lart
    -
    total 4
    -rw-r--r--    1 root     root           796 Jun 11 09:38 up.yml
    drwxr-xr-x    6 root     root           192 Jun 11 09:38 ..
    drwxr-xr-x    3 root     root            96 Jun 11 09:38 .
    -
     .. ok
    cmd( 2):
    ls |grep up
    
    cmd=>:
    ls |grep up
    -
    up.yml
    -
     .. ok
    cmd( 3):
    pwd
    
    cmd=>:
    pwd
    -
    /up_project/up/tests/modtests/0004/hello-module
    -
     .. ok
    cmd( 4):
    ls ../../..|grep modtests
    
    cmd=>:
    ls ../../..|grep modtests
    -
    modtests
    -
     .. ok
    . ok
    -Step2: [: this should call its own internal task
     ]
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ls ../../..|grep modtests",
        Code: 0,
        Output: "modtests",
        ErrMsg: ""
      }),
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1
    })
    
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "ls ../../..|grep modtests",
        Code: 0,
        Output: "modtests",
        ErrMsg: ""
      }),
      "up_runtime_tasker_layer_number": 2
    })
    
      located task-> 3 [internal_task]: 
    =Task3: [TODO: Main Caller Taskname/Say_world ==> internal_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "ls ../../..|grep modtests",
        Code: 0,
        Output: "modtests",
        ErrMsg: ""
      })
    })
    
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ls ../../..|grep modtests",
        Code: 0,
        Output: "modtests",
        ErrMsg: ""
      }),
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    this is a internal task in module
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "ls ../../..|grep modtests",
        Code: 0,
        Output: "modtests",
        ErrMsg: ""
      }),
      "up_runtime_tasker_layer_number": 2
    })
    
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "ls ../../..|grep modtests",
        Code: 0,
        Output: "modtests",
        ErrMsg: ""
      }),
      "up_runtime_tasker_layer_number": 2
    })
    
    cmd( 1):
    ls -lart
    
    cmd=>:
    ls -lart
    -
    total 4
    -rw-r--r--    1 root     root           796 Jun 11 09:38 up.yml
    drwxr-xr-x    6 root     root           192 Jun 11 09:38 ..
    drwxr-xr-x    3 root     root            96 Jun 11 09:38 .
    -
     .. ok
    cmd( 2):
    ls |grep up
    
    cmd=>:
    ls |grep up
    -
    up.yml
    -
     .. ok
    cmd( 3):
    pwd
    
    cmd=>:
    pwd
    -
    /up_project/up/tests/modtests/0004/hello-module
    -
     .. ok
    cmd( 4):
    ls ../../..|grep modtests
    
    cmd=>:
    ls ../../..|grep modtests
    -
    modtests
    -
     .. ok
    . ok
    -Step3:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2
    })
    
      located task-> 2 [internal_task]: 
    =Task2: [Main ==> internal_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    this is a internal task in caller
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2
    })
    
    cmd( 1):
    ls -lart
    
    cmd=>:
    ls -lart
    -
    total 12
    -rw-r--r--    1 root     root           253 Jun 11 09:38 upconfig.yml
    -rw-r--r--    1 root     root           521 Jun 11 09:38 up.yml
    drwxr-xr-x    3 root     root            96 Jun 11 09:38 hello-module
    -rw-r--r--    1 root     root          1019 Jun 11 09:38 doc.yml
    drwxr-xr-x    6 root     root           192 Jun 11 09:38 .
    drwxr-xr-x   18 root     root           576 Jul 18 17:03 ..
    -
     .. ok
    cmd( 2):
    ls |grep up
    
    cmd=>:
    ls |grep up
    -
    up.yml
    upconfig.yml
    -
     .. ok
    cmd( 3):
    pwd
    
    cmd=>:
    pwd
    -
    /up_project/up/tests/modtests/0004
    -
     .. ok
    cmd( 4):
    ls ../..|grep modtests
    
    cmd=>:
    ls ../..|grep modtests
    -
    modtests
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [m0004 log - verbose level v](../../logs/m0004_v)
* [m0004 log - verbose level vv](../../logs/m0004_vv)
* [m0004 log - verbose level vvv](../../logs/m0004_vvv)
* [m0004 log - verbose level vvvv](../../logs/m0004_vvvv)
* [m0004 log - verbose level vvvvv](../../logs/m0004_vvvvv)

##### References
* [Related Chapter](../../module/0004)
