---
title: "c0013_vvvvv"
date: 2020-07-20T02:01:31+77:00
draft: false
weight: 10134

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
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0013
    -------full vars in scopes------
    (*impl.Scopes)(0xc000172ec0)(<nil>)
    
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
      "studentname": "Jason",
      "a": "runtime-a",
      "e": "runtime-e",
      "k": "runtime-k"
    }
    
    (core.Cache) (len=4) {
     (string) (len=11) "studentname": (string) (len=5) "Jason",
     (string) (len=1) "a": (string) (len=9) "runtime-a",
     (string) (len=1) "e": (string) (len=9) "runtime-e",
     (string) (len=1) "k": (string) (len=9) "runtime-k"
    }
    
    [runtime global] dvar expanded result:
    {
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
        "school": "SG",
        "studentname": "Tom"
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "e": "runtime-e",
      "school": "SG",
      "k": "runtime-k",
      "studentname": "Tom",
      "a": "runtime-a"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "k": "runtime-k",
      "studentname": "Tom",
      "a": "runtime-a",
      "e": "runtime-e",
      "school": "SG"
    })
    
    cmd( 1):
    echo "hello, world"
    
    cmd=>:
    echo "hello, world"<=
    hello, world
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"hello, world\"",
     Code: (int) 0,
     Output: (string) (len=12) "hello, world",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello {{.studentname}}"
    
    cmd=>:
    echo "hello Tom"<=
    hello Tom
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=16) "echo \"hello Tom\"",
     Code: (int) 0,
     Output: (string) (len=9) "hello Tom",
     ErrMsg: (string) ""
    }
    
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
