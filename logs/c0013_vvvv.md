---
title: "c0013_vvvv"
date: 2020-07-01T15:34:22+77:00
draft: false
weight: 10133

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0013
                 Verbose -> vvvv
              ModuleName -> sad_thompson1
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0013
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [sad_thompson1] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "e": "runtime-e",
      "k": "runtime-k",
      "studentname": "Jason",
      "a": "runtime-a"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "studentname": "Jason",
      "a": "runtime-a",
      "e": "runtime-e",
      "k": "runtime-k"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [step1: to test display env vars from shell context ]
    {
      Name: "step1",
      Do: {
        "echo \"hello, world\"",
        "echo \"hello {{.studentname}}\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "studentname": "Tom",
        "school": "SG"
      },
      Dvars: <nil>,
      Desc: "to test display env vars from shell context",
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
      "k": "runtime-k",
      "studentname": "Tom",
      "a": "runtime-a",
      "e": "runtime-e",
      "school": "SG"
    })
    
    sad_thompson1: overall final exec vars:
    
    (*core.Cache)({
      "k": "runtime-k",
      "studentname": "Tom",
      "a": "runtime-a",
      "e": "runtime-e",
      "school": "SG"
    })
    
    cmd( 1):
    echo "hello, world"
    
     \_ echo "hello, world"
    hello, world
     .. ok
    cmd( 2):
    echo "hello {{.studentname}}"
    
     \_ echo "hello Tom"
    hello Tom
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0013 log - verbose level v](../../logs/c0013_v)
* [c0013 log - verbose level vv](../../logs/c0013_vv)
* [c0013 log - verbose level vvv](../../logs/c0013_vvv)
* [c0013 log - verbose level vvvv](../../logs/c0013_vvvv)
* [c0013 log - verbose level vvvvv](../../logs/c0013_vvvvv)

##### References
* [Related Chapter](../../vars/c0013)
