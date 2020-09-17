---
title: "c0126_vvvvv"
date: 2020-09-18T01:27:43+99:00
draft: false
weight: 11264

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0126
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0126
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001c13a0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "goahead": false
    }
    
    (core.Cache) (len=1) {
     (string) (len=7) "goahead": (bool) false
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "goahead": false
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "true/false value of goahead:\n{{.goahead}}\n{{not .goahead}}\n"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "goahead": false
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "goahead": false,
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    true/false value of goahead:
    {{.goahead}}
    {{not .goahead}}
    
    ~SubStep1: [print:  ]
    true/false value of goahead:
    false
    true
    
    -Step2:
    {
      Name: "",
      Do: {
        "goahead"
      },
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "{{.goahead}}",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "goahead": false,
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    condition failed, skip executing step 
    
    -Step3:
    {
      Name: "",
      Do: {
        "else"
      },
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "{{not .goahead}}",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "goahead": false
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "goahead": false,
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    caller's vars to task (else)::
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
      located task-> 3 [else]: 
    =Task3: [task ==> else:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "do something else ......."
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "goahead": false
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
    do something else .......
    ~~SubStep1: [print:  ]
    do something else .......
    
```

##### Logs with different verbose level
* [c0126 log - verbose level v](../../logs/c0126_v)
* [c0126 log - verbose level vv](../../logs/c0126_vv)
* [c0126 log - verbose level vvv](../../logs/c0126_vvv)
* [c0126 log - verbose level vvvv](../../logs/c0126_vvvv)
* [c0126 log - verbose level vvvvv](../../logs/c0126_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0126)
