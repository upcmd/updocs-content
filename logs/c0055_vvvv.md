---
title: "c0055_vvvv"
date: 2020-06-25T01:55:46+66:00
draft: false
weight: 10553

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0055
                 Verbose -> vvvv
              ModuleName -> stupefied_wright1
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0055
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [stupefied_wright1] instance id: [dev]
    merged[ dev ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "taska"
      },
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "false",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
    })
    
    stupefied_wright1: overall final exec vars:
    
    (*core.Cache)({
    })
    
    condition failed, skip executing step 
    
    -Step2:
    {
      Name: "",
      Do: <nil>,
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "greet",
          Value: "hello",
          Desc: "",
          Expand: 0,
          Flags: {
            "vvvv"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "true",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
    })
    
    dvar> greet:
    "hello"
    
    stupefied_wright1: overall final exec vars:
    
    (*core.Cache)({
      "greet": "hello"
    })
    
     WARN: [cmd] - [Not implemented or void for no action!]
    -Step3:
    {
      Name: "",
      Do: {
        "taska"
      },
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "true",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
    })
    
    stupefied_wright1: overall final exec vars:
    
    (*core.Cache)({
    })
    
      located task-> 2 [taska]: 
    =Task2: [task ==> taska:  ]
    Executing task stack layer: 2
    
    --Step1: [: greet var will be no value as it is a local var for cmd step ]
    {
      Name: "",
      Do: {
        "echo \"hello from taska\"",
        "echo \"{{.greet}} from taska\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "greet var will be no value as it is a local var for cmd step",
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
      "up_runtime_task_layer_number": 1
    })
    
    stupefied_wright1: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    echo "hello from taska"
    
     \_ echo "hello from taska"
    hello from taska
     .. ok
    cmd( 2):
    echo "{{.greet}} from taska"
    
     \_ echo "<no value> from taska"
    <no value> from taska
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0055 log - verbose level v](../../logs/c0055_v)
* [c0055 log - verbose level vv](../../logs/c0055_vv)
* [c0055 log - verbose level vvv](../../logs/c0055_vvv)
* [c0055 log - verbose level vvvv](../../logs/c0055_vvvv)
* [c0055 log - verbose level vvvvv](../../logs/c0055_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0055)
