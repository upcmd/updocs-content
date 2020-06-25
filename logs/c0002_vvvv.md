---
title: "c0002_vvvv"
date: 2020-06-25T01:55:36+66:00
draft: false
weight: 10023

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
                 Verbose -> vvvv
              ModuleName -> modest_sinoussi7
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0002
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [modest_sinoussi7] instance id: [dev]
    merged[ dev ] runtime vars:
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
    
    modest_sinoussi7: overall final exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo "hello"
    
     \_ echo "hello"
    hello
     .. ok
    cmd( 2):
    echo "world"
    
     \_ echo "world"
    world
     .. ok
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
        "ignore_error"
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
        Code: 0,
        Output: "world",
        ErrMsg: ""
      })
    })
    
    modest_sinoussi7: overall final exec vars:
    
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
    cmd( 2):
    echo "I got exception"|grep non-exist
    
     \_ echo "I got exception"|grep non-exist
          exec error: -> exit status 1
    -----trace for reference-----
    
          
     .. failed(suppressed if not last step)
    cmd( 3):
    echo "world"
    
     \_ echo "world"
    world
     .. ok
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
