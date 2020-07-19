---
title: "c0004_vvvvv"
date: 2020-07-20T02:01:29+77:00
draft: false
weight: 10044

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0004
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0004
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001c0ee0)(<nil>)
    
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
    Task1: [task ==> task: this is task1 ]
    Executing task stack layer: 1
    
    -Step1: [: do step1 in shell func ]
    {
      Name: "",
      Do: {
        "echo \"hello\"\necho \"world\"\n",
        "echo \"how are you\""
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
    echo "world"
    
    
    cmd=>:
    echo "hello"
    echo "world"
    <=
    hello
    world
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=26) "echo \"hello\"\necho \"world\"\n",
     Code: (int) 0,
     Output: (string) (len=11) "hello\nworld",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "how are you"
    
    cmd=>:
    echo "how are you"<=
    how are you
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"how are you\"",
     Code: (int) 0,
     Output: (string) (len=11) "how are you",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0004 log - verbose level v](../../logs/c0004_v)
* [c0004 log - verbose level vv](../../logs/c0004_vv)
* [c0004 log - verbose level vvv](../../logs/c0004_vvv)
* [c0004 log - verbose level vvvv](../../logs/c0004_vvvv)
* [c0004 log - verbose level vvvvv](../../logs/c0004_vvvvv)

##### References
* [Related Chapter](../../quick-start/c0004)
