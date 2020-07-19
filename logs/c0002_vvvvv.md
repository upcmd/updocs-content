---
title: "c0002_vvvvv"
date: 2020-07-20T02:01:29+77:00
draft: false
weight: 10024

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0002
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0002
    -------full vars in scopes------
    (*impl.Scopes)(0xc000204420)(<nil>)
    
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
    Task1: [task ==> task: this is task ]
    Executing task stack layer: 1
    
    -Step1: [: do step1 in shell func ]
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
      Desc: "do step1 in shell func",
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
    
    
    self: final context exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo "hello"
    
    cmd=>:
    echo "hello"<=
    hello
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"hello\"",
     Code: (int) 0,
     Output: (string) (len=5) "hello",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "world"
    
    cmd=>:
    echo "world"<=
    world
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"world\"",
     Code: (int) 0,
     Output: (string) (len=5) "world",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2: [: do step2 in shell func ]
    {
      Name: "",
      Do: {
        "echo \"hello\"",
        "echo \"I got exception\"|grep non-exist",
        "echo \"world\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "do step2 in shell func",
      Reg: "",
      Flags: {
        "ignoreError"
      },
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
        Cmd: "echo \"world\"",
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
        Cmd: "echo \"world\"",
        Code: 0,
        Output: "world",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"world\"",
        Code: 0,
        Output: "world",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "hello"
    
    cmd=>:
    echo "hello"<=
    hello
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"hello\"",
     Code: (int) 0,
     Output: (string) (len=5) "hello",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "I got exception"|grep non-exist
    
    cmd=>:
    echo "I got exception"|grep non-exist<=
          exec error: -> exit status 1
    -----trace for reference-----
    
          
     .. failed(suppressed if not last step)
    (utils.ExecResult) {
     Cmd: (string) (len=37) "echo \"I got exception\"|grep non-exist",
     Code: (int) 1,
     Output: (string) "",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "world"
    
    cmd=>:
    echo "world"<=
    world
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"world\"",
     Code: (int) 0,
     Output: (string) (len=5) "world",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0002 log - verbose level v](../../logs/c0002_v)
* [c0002 log - verbose level vv](../../logs/c0002_vv)
* [c0002 log - verbose level vvv](../../logs/c0002_vvv)
* [c0002 log - verbose level vvvv](../../logs/c0002_vvvv)
* [c0002 log - verbose level vvvvv](../../logs/c0002_vvvvv)

##### References
* [Related Chapter](../../quick-start/c0002)
