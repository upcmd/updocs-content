---
title: "c0035_vvvv"
date: 2020-06-27T03:09:18+66:00
draft: false
weight: 10353

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0035
                 Verbose -> vvvv
              ModuleName -> thirsty_mclean8
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0035
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [thirsty_mclean8] instance id: [dev]
    merged[ dev ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [step1:  ]
    {
      Name: "step1",
      Do: {
        "pwd"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "b": "bbb",
        "a": "aaa"
      },
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
      "b": "bbb",
      "a": "aaa"
    })
    
    thirsty_mclean8: overall final exec vars:
    
    (*core.Cache)({
      "b": "bbb",
      "a": "aaa"
    })
    
    cmd( 1):
    pwd
    
     \_ pwd
    /up_project/up
     .. ok
    . ok
    -Step2: [step2:  ]
    {
      Name: "step2",
      Do: {
        "echo \"{{.a}}\""
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
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      })
    })
    
    thirsty_mclean8: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "{{.a}}"
    
     \_ echo "<no value>"
    <no value>
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0035 log - verbose level v](../../logs/c0035_v)
* [c0035 log - verbose level vv](../../logs/c0035_vv)
* [c0035 log - verbose level vvv](../../logs/c0035_vvv)
* [c0035 log - verbose level vvvv](../../logs/c0035_vvvv)
* [c0035 log - verbose level vvvvv](../../logs/c0035_vvvvv)

##### References
* [Related Chapter](../../vars/c0035)
