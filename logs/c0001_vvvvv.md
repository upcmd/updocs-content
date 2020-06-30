---
title: "c0001_vvvvv"
date: 2020-07-01T15:34:20+77:00
draft: false
weight: 10014

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0001
                 Verbose -> vvvvv
              ModuleName -> cocky_hodgkin2
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0001
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ece00)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [cocky_hodgkin2] instance id: [dev]
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
    Task1: [task ==> task: say hello world in shell ]
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
    
    
    cocky_hodgkin2: overall final exec vars:
    
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
    
```

##### Logs with different verbose level
* [c0001 log - verbose level v](../../logs/c0001_v)
* [c0001 log - verbose level vv](../../logs/c0001_vv)
* [c0001 log - verbose level vvv](../../logs/c0001_vvv)
* [c0001 log - verbose level vvvv](../../logs/c0001_vvvv)
* [c0001 log - verbose level vvvvv](../../logs/c0001_vvvvv)

##### References
* [Related Chapter](../../quick-start/c0001)
