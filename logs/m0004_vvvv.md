---
title: "0004_vvvv"
date: 2020-06-25T01:56:26+66:00
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
              ModuleName -> silly_bardeen6
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up/tests/modtests/0004
    -exec task: Main
    loading [Task]:  ./up.yml
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [silly_bardeen6] instance id: [dev]
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
    {
      Name: "",
      Do: "internal_task",
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
    })
    
    silly_bardeen6: overall final exec vars:
    
    (*core.Cache)({
    })
    
      located task-> 2 [internal_task]: 
    =Task2: [Main ==> internal_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "this is a internal task in caller"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    silly_bardeen6: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    this is a internal task in caller
    --Step2:
    {
      Name: "",
      Do: {
        "ls -lart",
        "ls |grep up",
        "pwd",
        "ls ../..|grep modtests"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    silly_bardeen6: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    ls -lart
    
     \_ ls -lart
    total 12
    -rw-r--r--  1 root root  253 Jun 11 09:38 upconfig.yml
    -rw-r--r--  1 root root  521 Jun 11 09:38 up.yml
    drwxr-xr-x  3 root root   96 Jun 11 09:38 hello-module
    -rw-r--r--  1 root root 1019 Jun 11 09:38 doc.yml
    drwxr-xr-x  6 root root  192 Jun 11 09:38 .
    drwxr-xr-x 18 root root  576 Jun 12 00:35 ..
     .. ok
    cmd( 2):
    ls |grep up
    
     \_ ls |grep up
    up.yml
    upconfig.yml
     .. ok
    cmd( 3):
    pwd
    
     \_ pwd
    /up_project/up/tests/modtests/0004
     .. ok
    cmd( 4):
    ls ../..|grep modtests
    
     \_ ls ../..|grep modtests
    modtests
     .. ok
    . ok
    -Step2:
    {
      Name: "",
      Do: "hello-module.Say_world",
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    silly_bardeen6: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
     WARN: [config file does not exist] - [use builtin defaults]
    loading [Task]:  ./up.yml
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [hello-module] instance id: [nonamed]
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
    {
      Name: "",
      Do: {
        "ls -lart",
        "ls |grep up",
        "pwd",
        "ls ../../..|grep modtests"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2
    })
    
    hello-module: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2
    })
    
    cmd( 1):
    ls -lart
    
     \_ ls -lart
    total 4
    -rw-r--r-- 1 root root 796 Jun 11 09:38 up.yml
    drwxr-xr-x 6 root root 192 Jun 11 09:38 ..
    drwxr-xr-x 3 root root  96 Jun 11 09:38 .
     .. ok
    cmd( 2):
    ls |grep up
    
     \_ ls |grep up
    up.yml
     .. ok
    cmd( 3):
    pwd
    
     \_ pwd
    /up_project/up/tests/modtests/0004/hello-module
     .. ok
    cmd( 4):
    ls ../../..|grep modtests
    
     \_ ls ../../..|grep modtests
    modtests
     .. ok
    . ok
    -Step2: [: this should call its own internal task
     ]
    {
      Name: "",
      Do: "internal_task",
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "this should call its own internal task\n",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "modtests",
        ErrMsg: ""
      }),
      "up_runtime_tasker_layer_number": 2
    })
    
    hello-module: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
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
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "this is a internal task in module"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "modtests",
        ErrMsg: ""
      }),
      "up_runtime_tasker_layer_number": 2
    })
    
    hello-module: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "modtests",
        ErrMsg: ""
      })
    })
    
    ~~SubStep1: [print:  ]
    this is a internal task in module
    --Step2:
    {
      Name: "",
      Do: {
        "ls -lart",
        "ls |grep up",
        "pwd",
        "ls ../../..|grep modtests"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "modtests",
        ErrMsg: ""
      }),
      "up_runtime_tasker_layer_number": 2
    })
    
    hello-module: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "modtests",
        ErrMsg: ""
      }),
      "up_runtime_tasker_layer_number": 2
    })
    
    cmd( 1):
    ls -lart
    
     \_ ls -lart
    total 4
    -rw-r--r-- 1 root root 796 Jun 11 09:38 up.yml
    drwxr-xr-x 6 root root 192 Jun 11 09:38 ..
    drwxr-xr-x 3 root root  96 Jun 11 09:38 .
     .. ok
    cmd( 2):
    ls |grep up
    
     \_ ls |grep up
    up.yml
     .. ok
    cmd( 3):
    pwd
    
     \_ pwd
    /up_project/up/tests/modtests/0004/hello-module
     .. ok
    cmd( 4):
    ls ../../..|grep modtests
    
     \_ ls ../../..|grep modtests
    modtests
     .. ok
    . ok
    -Step3:
    {
      Name: "",
      Do: "internal_task",
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1
    })
    
    silly_bardeen6: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1
    })
    
      located task-> 2 [internal_task]: 
    =Task2: [Main ==> internal_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "this is a internal task in caller"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1
    })
    
    silly_bardeen6: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    this is a internal task in caller
    --Step2:
    {
      Name: "",
      Do: {
        "ls -lart",
        "ls |grep up",
        "pwd",
        "ls ../..|grep modtests"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2
    })
    
    silly_bardeen6: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2
    })
    
    cmd( 1):
    ls -lart
    
     \_ ls -lart
    total 12
    -rw-r--r--  1 root root  253 Jun 11 09:38 upconfig.yml
    -rw-r--r--  1 root root  521 Jun 11 09:38 up.yml
    drwxr-xr-x  3 root root   96 Jun 11 09:38 hello-module
    -rw-r--r--  1 root root 1019 Jun 11 09:38 doc.yml
    drwxr-xr-x  6 root root  192 Jun 11 09:38 .
    drwxr-xr-x 18 root root  576 Jun 12 00:35 ..
     .. ok
    cmd( 2):
    ls |grep up
    
     \_ ls |grep up
    up.yml
    upconfig.yml
     .. ok
    cmd( 3):
    pwd
    
     \_ pwd
    /up_project/up/tests/modtests/0004
     .. ok
    cmd( 4):
    ls ../..|grep modtests
    
     \_ ls ../..|grep modtests
    modtests
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
