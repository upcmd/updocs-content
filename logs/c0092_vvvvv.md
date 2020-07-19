---
title: "c0092_vvvvv"
date: 2020-07-20T02:01:45+77:00
draft: false
weight: 10924

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0092
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0092
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001c7060)(<nil>)
    
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
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "{{.person.name}}_action"
      },
      Dox: <nil>,
      Func: "call",
      Vars: {
        "person": {
          "name": "tom",
          "age": 23
        }
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
      "person": {
        "name": "tom",
        "age": 23
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "person": {
        "name": "tom",
        "age": 23
      }
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "person": {
        "name": "tom",
        "age": 23
      }
    })
    
    caller's vars to task (tom_action)::
    (*core.Cache)({
      "person": {
        "name": "tom",
        "age": 23
      }
    })
    
      located task-> 2 [tom_action]: 
    =Task2: [task ==> tom_action:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "hello {{.person.name}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
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
      "person": {
        "name": "tom",
        "age": 23
      },
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "person": {
        "name": "tom",
        "age": 23
      },
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "person": {
        "age": 23,
        "name": "tom"
      }
    })
    
    hello {{.person.name}}
    ~~SubStep1: [print:  ]
    hello tom
    
```

##### Logs with different verbose level
* [c0092 log - verbose level v](../../logs/c0092_v)
* [c0092 log - verbose level vv](../../logs/c0092_vv)
* [c0092 log - verbose level vvv](../../logs/c0092_vvv)
* [c0092 log - verbose level vvvv](../../logs/c0092_vvvv)
* [c0092 log - verbose level vvvvv](../../logs/c0092_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0092)
