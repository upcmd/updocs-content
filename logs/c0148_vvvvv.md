---
title: "c0148_vvvvv"
date: 2020-06-27T03:09:35+66:00
draft: false
weight: 11484

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0148
                 Verbose -> vvvvv
              ModuleName -> insane_bardeen0
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0148
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ef440)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [insane_bardeen0] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "tom": "this is tom"
    }
    
    (core.Cache) (len=1) {
     (string) (len=3) "tom": (string) (len=11) "this is tom"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "tom": "this is tom"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "func": "cmd",
          "dvars": {
            {
              "name": "jerry",
              "value": "this is jerry in task scope",
              "flags": {
                "taskscope"
              }
            }
          }
        },
        {
          "do": {
            {
              "name": "print",
              "desc": "this should print out the dvar value of jerry",
              "cmd": "{{.jerry}}"
            }
          },
          "func": "cmd"
        }
      },
      Dox: <nil>,
      Func: "block",
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
      "tom": "this is tom"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "this is tom"
    }
    
    
    insane_bardeen0: overall final exec vars:
    
    (*core.Cache)({
      "tom": "this is tom"
    })
    
    -Step1:
    {
      Name: "",
      Do: <nil>,
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
            "taskscope"
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "tom": "this is tom"
    })
    
    [local] dvar expanded result:
    {
      "jerry": "this is jerry in task scope"
    }
    
    
    scope[local] merged: {
      "jerry": "this is jerry in task scope",
      "tom": "this is tom"
    }
    
    
    insane_bardeen0: overall final exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "jerry": "this is jerry in task scope"
    })
    
     WARN: [cmd] - [Not implemented or void for no action!]
    -Step2:
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
      "tom": "this is tom",
      "jerry": "this is jerry in task scope"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "this is tom",
      "jerry": "this is jerry in task scope"
    }
    
    
    insane_bardeen0: overall final exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "jerry": "this is jerry in task scope"
    })
    
    {{.jerry}}
    ~SubStep1: [print: this should print out the dvar value of jerry ]
    this is jerry in task scope
    -Step2:
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
      "tom": "this is tom",
      "jerry": "this is jerry in task scope"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "this is tom",
      "jerry": "this is jerry in task scope"
    }
    
    
    insane_bardeen0: overall final exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "jerry": "this is jerry in task scope"
    })
    
    {{.jerry}}
    ~SubStep1: [print: this should print out the dvar value of jerry ]
    this is jerry in task scope
    -Step3:
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "tom": "this is tom",
      "jerry": "this is jerry in task scope"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "this is tom",
      "jerry": "this is jerry in task scope"
    }
    
    
    insane_bardeen0: overall final exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "jerry": "this is jerry in task scope"
    })
    
    caller's vars to task (subtask1)::
    (*core.Cache)({
      "tom": "this is tom",
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
          "desc": "this should print out the dvar value of jerry as it is declared jerry is in taskscope",
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "tom": "this is tom",
      "jerry": "this is jerry in task scope",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "this is tom",
      "jerry": "this is jerry in task scope",
      "up_runtime_task_layer_number": 1
    }
    
    
    insane_bardeen0: overall final exec vars:
    
    (*core.Cache)({
      "jerry": "this is jerry in task scope",
      "up_runtime_task_layer_number": 1,
      "tom": "this is tom"
    })
    
    {{.jerry}}
    ~~SubStep1: [print: this should print out the dvar value of jerry as it is declared jerry is in taskscope ]
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
      VarsFile: ""
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
    
    
    insane_bardeen0: overall final exec vars:
    
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
    
```

##### Logs with different verbose level
* [c0148 log - verbose level v](../../logs/c0148_v)
* [c0148 log - verbose level vv](../../logs/c0148_vv)
* [c0148 log - verbose level vvv](../../logs/c0148_vvv)
* [c0148 log - verbose level vvvv](../../logs/c0148_vvvv)
* [c0148 log - verbose level vvvvv](../../logs/c0148_vvvvv)

##### References
* [Related Chapter](../../vars/c0148)
