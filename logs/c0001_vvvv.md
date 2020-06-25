---
title: "c0001_vvvv"
date: 2020-06-25T01:55:36+66:00
draft: false
weight: 10013

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
                 Verbose -> vvvv
              ModuleName -> prickly_mcclintock0
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0001
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [prickly_mcclintock0] instance id: [dev]
    merged[ dev ] runtime vars:
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
    
    prickly_mcclintock0: overall final exec vars:
    
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
    
```

##### Logs with different verbose level
* [c0001 log - verbose level v](../../logs/c0001_v)
* [c0001 log - verbose level vv](../../logs/c0001_vv)
* [c0001 log - verbose level vvv](../../logs/c0001_vvv)
* [c0001 log - verbose level vvvv](../../logs/c0001_vvvv)
* [c0001 log - verbose level vvvvv](../../logs/c0001_vvvvv)

##### References
* [Related Chapter](../../quick-start/c0001)
