---
title: "c0003_vvvv"
date: 2020-06-25T01:55:36+66:00
draft: false
weight: 10033

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0003
                 Verbose -> vvvv
              ModuleName -> evil_ardinghelli2
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0003
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [evil_ardinghelli2] instance id: [dev]
    merged[ dev ] runtime vars:
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
      Do: "echo \"hello\"\necho \"world\"\n",
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
    
    evil_ardinghelli2: overall final exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo "hello"
    echo "world"
    
    
     \_ echo "hello"
    echo "world"
    
    hello
    world
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0003 log - verbose level v](../../logs/c0003_v)
* [c0003 log - verbose level vv](../../logs/c0003_vv)
* [c0003 log - verbose level vvv](../../logs/c0003_vvv)
* [c0003 log - verbose level vvvv](../../logs/c0003_vvvv)
* [c0003 log - verbose level vvvvv](../../logs/c0003_vvvvv)

##### References
* [Related Chapter](../../quick-start/c0003)
