---
title: "c0087_vvvv"
date: 2020-07-01T15:34:32+77:00
draft: false
weight: 10873

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0087
                 Verbose -> vvvv
              ModuleName -> sharp_payne4
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0087
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [sharp_payne4] instance id: [dev]
    merged[ dev ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task: generate logs ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo 'hello'"
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
    })
    
    sharp_payne4: overall final exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo 'hello'
    
     \_ echo 'hello'
    hello
     .. ok
    . ok
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "sleep",
          "cmd": 2000
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
        Output: "hello",
        ErrMsg: ""
      })
    })
    
    sharp_payne4: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      })
    })
    
    ~SubStep1: [sleep:  ]
    sleeping 2000 milli seconds
    ....................
    -Step3:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "world"
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
        Output: "hello",
        ErrMsg: ""
      })
    })
    
    sharp_payne4: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      })
    })
    
    ~SubStep1: [print:  ]
    world
    -Step4:
    {
      Name: "",
      Do: {
        "{{.loopitem}}"
      },
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "impl1",
        "impl2"
      },
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      })
    })
    
    sharp_payne4: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      })
    })
    
      located task-> 2 [impl1]: 
    =Task2: [task ==> impl1:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "hello"
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
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "loopitem": "impl1",
      "loopindex": 0
    })
    
    sharp_payne4: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "loopitem": "impl1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    ~~SubStep1: [print:  ]
    hello
    --Step2:
    {
      Name: "",
      Do: {
        {
          "name": "sleep",
          "cmd": 1000
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
        Output: "hello",
        ErrMsg: ""
      }),
      "loopitem": "impl1",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1
    })
    
    sharp_payne4: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "loopitem": "impl1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    ~~SubStep1: [sleep:  ]
    sleeping 1000 milli seconds
    ..........
      located task-> 3 [impl2]: 
    =Task3: [task ==> impl2:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "world"
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
        Output: "hello",
        ErrMsg: ""
      }),
      "loopitem": "impl2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    sharp_payne4: overall final exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "loopitem": "impl2"
    })
    
    ~~SubStep1: [print:  ]
    world
    
```

##### Logs with different verbose level
* [c0087 log - verbose level v](../../logs/c0087_v)
* [c0087 log - verbose level vv](../../logs/c0087_vv)
* [c0087 log - verbose level vvv](../../logs/c0087_vvv)
* [c0087 log - verbose level vvvv](../../logs/c0087_vvvv)
* [c0087 log - verbose level vvvvv](../../logs/c0087_vvvvv)

##### References
* [Related Chapter](../../cmd-func/c0087)
