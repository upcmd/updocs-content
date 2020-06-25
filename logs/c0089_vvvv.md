---
title: "c0089_vvvv"
date: 2020-06-25T01:55:52+66:00
draft: false
weight: 10893

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0089
                 Verbose -> vvvv
              ModuleName -> naughty_shockley2
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0089
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [naughty_shockley2] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "dynadir": "./tests/functests"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "dynadir": "./tests/functests"
    }
    
    loading [flow ref]:  ./tests/functests/c0089-task-main.yml
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"task step 1\"",
        "echo \"task step 2\""
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
      "dynadir": "./tests/functests"
    })
    
    naughty_shockley2: overall final exec vars:
    
    (*core.Cache)({
      "dynadir": "./tests/functests"
    })
    
    cmd( 1):
    echo "task step 1"
    
     \_ echo "task step 1"
    task step 1
     .. ok
    cmd( 2):
    echo "task step 2"
    
     \_ echo "task step 2"
    task step 2
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0089 log - verbose level v](../../logs/c0089_v)
* [c0089 log - verbose level vv](../../logs/c0089_vv)
* [c0089 log - verbose level vvv](../../logs/c0089_vvv)
* [c0089 log - verbose level vvvv](../../logs/c0089_vvvv)
* [c0089 log - verbose level vvvvv](../../logs/c0089_vvvvv)

##### References
* [Related Chapter](../../organization/c0089)
