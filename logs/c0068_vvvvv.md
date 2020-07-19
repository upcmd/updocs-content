---
title: "c0068_vvvvv"
date: 2020-07-20T02:01:41+77:00
draft: false
weight: 10684

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0068
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0068
    -------full vars in scopes------
    (*impl.Scopes)(0xc000176f60)(<nil>)
    
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
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: do step1 in shell func ]
    {
      Name: "",
      Do: {
        "echo \"hello\"",
        "echo \"world\"|grep non-exist",
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
    echo "world"|grep non-exist
    
    cmd=>:
    echo "world"|grep non-exist<=
          exec error: -> exit status 1
    -----trace for reference-----
    
          
     .. failed(suppressed if not last step)
    (utils.ExecResult) {
     Cmd: (string) (len=27) "echo \"world\"|grep non-exist",
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
* [c0068 log - verbose level v](../../logs/c0068_v)
* [c0068 log - verbose level vv](../../logs/c0068_vv)
* [c0068 log - verbose level vvv](../../logs/c0068_vvv)
* [c0068 log - verbose level vvvv](../../logs/c0068_vvvv)
* [c0068 log - verbose level vvvvv](../../logs/c0068_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0068)
