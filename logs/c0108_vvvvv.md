---
title: "c0108_vvvvv"
date: 2020-10-07T00:11:18+1010:00
draft: false
weight: 11084

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0108
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0108
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0000988a0)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "tom": "this is tom"
    })
    
    (*core.Cache)(0xc0000c8128)((len=1) {
     (string) (len=3) "tom": (string) (len=11) "this is tom"
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "tom": "this is tom"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.tom}}"
        },
        {
          "name": "print",
          "cmd": "{{.jerry}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "jerry": "this is jerry"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0,
      "jerry": "this is jerry"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "jerry": "this is jerry",
      "tom": "this is tom"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0,
      "jerry": "this is jerry"
    })
    
    {{.tom}}
    ~SubStep1: [print:  ]
    this is tom
    {{.jerry}}
    ~SubStep2: [print:  ]
    this is jerry
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "desc": "jerry is in local scope so there is no value",
          "cmd": "{{.jerry}}"
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
      "tom": "this is tom"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0
    })
    
    {{.jerry}}
    ~SubStep1: [print: jerry is in local scope so there is no value ]
    None
    -Step3:
    {
      Name: "",
      Do: {
        {
          "cmd": "{{.jerry}}",
          "name": "print",
          "desc": "this should print out the dvar value of jerry"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "jerry",
          Value: "this is jerry in task scope",
          Desc: "",
          Expand: 0,
          Flags: {
            "taskScope"
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
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
      "jerry": "this is jerry in task scope"
    }
    
    
    scope[local] merged: {
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0,
      "jerry": "this is jerry in task scope"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "jerry": "this is jerry in task scope",
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0
    })
    
    {{.jerry}}
    ~SubStep1: [print: this should print out the dvar value of jerry ]
    this is jerry in task scope
    -Step4:
    {
      Name: "",
      Do: {
        {
          "desc": "this should print out the dvar value of jerry as it is declared jerry is in taskScope",
          "cmd": "{{.jerry}}",
          "name": "print"
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
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0,
      "jerry": "this is jerry in task scope"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "jerry": "this is jerry in task scope",
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "jerry": "this is jerry in task scope",
      "tom": "this is tom"
    })
    
    {{.jerry}}
    ~SubStep1: [print: this should print out the dvar value of jerry as it is declared jerry is in taskScope ]
    this is jerry in task scope
    -Step5:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "desc": "var jerry in task scope is overrided by local var jerry",
          "cmd": "{{.jerry}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "jerry": "jerry is overrided in local scope"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0,
      "jerry": "jerry is overrided in local scope"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "jerry": "jerry is overrided in local scope",
      "tom": "this is tom"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "jerry": "jerry is overrided in local scope",
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0
    })
    
    {{.jerry}}
    ~SubStep1: [print: var jerry in task scope is overrided by local var jerry ]
    jerry is overrided in local scope
    -Step6:
    {
      Name: "",
      Do: {
        {
          "desc": "this should print out the jerry defined in task var scope",
          "cmd": "{{.jerry}}",
          "name": "print"
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
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0,
      "jerry": "this is jerry in task scope"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0,
      "jerry": "this is jerry in task scope"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0,
      "jerry": "this is jerry in task scope"
    })
    
    {{.jerry}}
    ~SubStep1: [print: this should print out the jerry defined in task var scope ]
    this is jerry in task scope
    
```

##### Logs with different verbose level
* [c0108 log - verbose level v](../../logs/c0108_v)
* [c0108 log - verbose level vv](../../logs/c0108_vv)
* [c0108 log - verbose level vvv](../../logs/c0108_vvv)
* [c0108 log - verbose level vvvv](../../logs/c0108_vvvv)
* [c0108 log - verbose level vvvvv](../../logs/c0108_vvvvv)

##### References
* [Related Chapter](../../vars/c0108)
