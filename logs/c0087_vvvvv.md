---
title: "c0087_vvvvv"
date: 2020-06-25T01:55:52+66:00
draft: false
weight: 10874

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
                 Verbose -> vvvvv
              ModuleName -> sharp_mestorf2
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0087
    -------full vars in scopes------
    (*impl.Scopes)(0xc000226920)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [sharp_mestorf2] instance id: [dev]
    merged[ dev ] runtime vars:
    {
    }
    
    (core.Cache) {
    }
    
    [runtime global] dvar expanded result:
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
    }
    
    
    sharp_mestorf2: overall final exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo 'hello'
    
     \_ echo 'hello'
    hello
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=5) "hello",
     ErrMsg: (string) ""
    }
    
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      })
    }
    
    
    sharp_mestorf2: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      })
    })
    
    %!s(int=2000)
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      })
    }
    
    
    sharp_mestorf2: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      })
    })
    
    world
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      })
    }
    
    
    sharp_mestorf2: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      })
    })
    
    caller's vars to task (impl1)::
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "loopitem": "impl1",
      "loopindex": 0,
      "loopindex1": 1
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "loopitem": "impl1",
      "loopindex": 0,
      "loopindex1": 1
    }
    
    
    sharp_mestorf2: overall final exec vars:
    
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
    
    hello
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopitem": "impl1",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      })
    }
    
    
    sharp_mestorf2: overall final exec vars:
    
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
    
    %!s(int=1000)
    ~~SubStep1: [sleep:  ]
    sleeping 1000 milli seconds
    ..........
    caller's vars to task (impl2)::
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "loopitem": "impl2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
      located task-> 3 [impl2]: 
    =Task3: [task ==> impl2:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "cmd": "world",
          "name": "print"
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "loopitem": "impl2",
      "loopindex": 1
    }
    
    
    sharp_mestorf2: overall final exec vars:
    
    (*core.Cache)({
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "loopitem": "impl2",
      "loopindex": 1
    })
    
    world
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
