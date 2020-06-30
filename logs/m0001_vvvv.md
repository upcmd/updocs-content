---
title: "0001_vvvv"
date: 2020-07-01T15:34:57+77:00
draft: false
weight: 100103

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/modtests/0001/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/modtests/0001
                 WorkDir -> refdir
              AbsWorkDir -> /up_project/up/tests/modtests/0001
                TaskFile -> up.yml
                 Verbose -> vvvv
              ModuleName -> condescending_feynman7
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up/tests/modtests/0001
    -exec task: Main
    loading [Task]:  ./up.yml
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [condescending_feynman7] instance id: [dev]
    merged[ dev ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
      located task-> 1 [Main]: 
    Task1: [Main ==> Main: main entry ]
    Executing task stack layer: 1
    
    -Step1: [: main job ]
    {
      Name: "",
      Do: {
        "echo \"hello world\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "main job",
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
    
    condescending_feynman7: overall final exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo "hello world"
    
     \_ echo "hello world"
    hello world
     .. ok
    . ok
    -Step2:
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
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      })
    })
    
    condescending_feynman7: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      })
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
          "cmd": "this is a internal task"
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
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    condescending_feynman7: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      })
    })
    
    ~~SubStep1: [print:  ]
    this is a internal task
    -Step3:
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
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    condescending_feynman7: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      })
    })
    
    loading [Config]:  ./upconfig.yml
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
    
      located task-> 2 [Say_world]: 
    Task2: [TODO: Main Caller Taskname ==> Say_world:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "... world"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "a": "aaa"
      },
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
      "a": "aaa",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1
    })
    
    hello-module: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1,
      "a": "aaa"
    })
    
    ~SubStep1: [print:  ]
    ... world
    
```

##### Logs with different verbose level
* [m0001 log - verbose level v](../../logs/m0001_v)
* [m0001 log - verbose level vv](../../logs/m0001_vv)
* [m0001 log - verbose level vvv](../../logs/m0001_vvv)
* [m0001 log - verbose level vvvv](../../logs/m0001_vvvv)
* [m0001 log - verbose level vvvvv](../../logs/m0001_vvvvv)

##### References
* [Related Chapter](../../module/0001)
