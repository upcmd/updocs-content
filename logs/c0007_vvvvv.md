---
title: "c0007_vvvvv"
date: 2020-07-01T15:34:21+77:00
draft: false
weight: 10074

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0007
                 Verbose -> vvvvv
              ModuleName -> trusting_engelbart7
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0007
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001f3000)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [trusting_engelbart7] instance id: [dev]
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
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"hello\"",
        "echo \"world\""
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
    
    
    trusting_engelbart7: overall final exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo "hello"
    
     \_ echo "hello"
    hello
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=5) "hello",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "world"
    
     \_ echo "world"
    world
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=5) "world",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2:
    {
      Name: "",
      Do: {
        "echo \"hello\"",
        "echo \"world\""
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
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "world",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "world",
        ErrMsg: ""
      })
    }
    
    
    trusting_engelbart7: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "world",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "hello"
    
     \_ echo "hello"
    hello
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=5) "hello",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "world"
    
     \_ echo "world"
    world
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=5) "world",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step3:
    {
      Name: "",
      Do: {
        "echo \"hello\"",
        "echo \"world\""
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
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "world",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "world",
        ErrMsg: ""
      })
    }
    
    
    trusting_engelbart7: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "world",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "hello"
    
     \_ echo "hello"
    hello
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=5) "hello",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "world"
    
     \_ echo "world"
    world
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=5) "world",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0007 log - verbose level v](../../logs/c0007_v)
* [c0007 log - verbose level vv](../../logs/c0007_vv)
* [c0007 log - verbose level vvv](../../logs/c0007_vvv)
* [c0007 log - verbose level vvvv](../../logs/c0007_vvvv)
* [c0007 log - verbose level vvvvv](../../logs/c0007_vvvvv)

##### References
* [Related Chapter](../../quick-start/c0007)
