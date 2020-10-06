---
title: "c0109_vvvvv"
date: 2020-10-06T23:46:10+1010:00
draft: false
weight: 11094

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0109
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
    loading [Task]:  ./tests/functests/c0109
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc000230ec0)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "tom": "this is tom"
    })
    
    (*core.Cache)(0xc00000e870)((len=1) {
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
          "desc": "this should print out the dvar value of jerry",
          "cmd": "{{.jerry}}"
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
      "up_runtime_task_layer_number": 0,
      "jerry": "this is jerry in task scope",
      "tom": "this is tom"
    })
    
    {{.jerry}}
    ~SubStep1: [print: this should print out the dvar value of jerry ]
    this is jerry in task scope
    -Step2:
    {
      Name: "",
      Do: {
        "subtask1"
      },
      Dox: <nil>,
      Func: "call",
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
      "jerry": "this is jerry in task scope",
      "tom": "this is tom"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "jerry": "this is jerry in task scope",
      "tom": "this is tom"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "jerry": "this is jerry in task scope",
      "tom": "this is tom"
    })
    
    caller's vars to task (subtask1)::
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0,
      "jerry": "this is jerry in task scope"
    })
    
      located task-> 2 [subtask1]: 
    =Task2: [task ==> subtask1:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "desc": "this should print out the dvar value of jerry as it is declared jerry is in taskScope",
          "cmd": "{{.jerry}}"
        },
        {
          "name": "trace",
          "cmd": "===>"
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
      "up_runtime_task_layer_number": 1,
      "jerry": "this is jerry in task scope",
      "tom": "this is tom"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "jerry": "this is jerry in task scope",
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "jerry": "this is jerry in task scope",
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
    {{.jerry}}
    ~~SubStep1: [print: this should print out the dvar value of jerry as it is declared jerry is in taskScope ]
    this is jerry in task scope
    ===>
    ~~SubStep2: [trace:  ]
    Trace:===>
    --Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "desc": "remember that the caller's vars should override callee's vars\nso jerry's value should the one from caller instead this local value\n",
          "cmd": "{{.jerry}}"
        },
        {
          "name": "trace",
          "cmd": "<==="
        },
        {
          "name": "trace",
          "cmd": "--->"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "jerry": "jerry is overriden in local scope"
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
      "jerry": "this is jerry in task scope",
      "up_runtime_task_layer_number": 1,
      "tom": "this is tom"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "this is tom",
      "jerry": "this is jerry in task scope",
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "jerry": "this is jerry in task scope",
      "up_runtime_task_layer_number": 1,
      "tom": "this is tom"
    })
    
    {{.jerry}}
    ~~SubStep1: [print: remember that the caller's vars should override callee's vars
    so jerry's value should the one from caller instead this local value
     ]
    this is jerry in task scope
    <===
    ~~SubStep2: [trace:  ]
    Trace:<===
    --->
    ~~SubStep3: [trace:  ]
    Trace:--->
    --Step3:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "desc": "this should print out the jerry defined in caller's task var scope",
          "cmd": "{{.jerry}}"
        },
        {
          "name": "trace",
          "cmd": "<---"
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
      "up_runtime_task_layer_number": 1,
      "jerry": "this is jerry in task scope"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "jerry": "this is jerry in task scope",
      "tom": "this is tom"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "jerry": "this is jerry in task scope",
      "tom": "this is tom"
    })
    
    {{.jerry}}
    ~~SubStep1: [print: this should print out the jerry defined in caller's task var scope ]
    this is jerry in task scope
    <---
    ~~SubStep2: [trace:  ]
    Trace:<---
    
```

##### Logs with different verbose level
* [c0109 log - verbose level v](../../logs/c0109_v)
* [c0109 log - verbose level vv](../../logs/c0109_vv)
* [c0109 log - verbose level vvv](../../logs/c0109_vvv)
* [c0109 log - verbose level vvvv](../../logs/c0109_vvvv)
* [c0109 log - verbose level vvvvv](../../logs/c0109_vvvvv)

##### References
* [Related Chapter](../../vars/c0109)
