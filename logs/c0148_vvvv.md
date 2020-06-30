---
title: "c0148_vvvv"
date: 2020-07-01T15:34:43+77:00
draft: false
weight: 11483

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
                 Verbose -> vvvv
              ModuleName -> elegant_noyce8
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0148
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [elegant_noyce8] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "tom": "this is tom"
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
              "flags": {
                "taskscope"
              },
              "name": "jerry",
              "value": "this is jerry in task scope"
            }
          }
        },
        {
          "func": "cmd",
          "do": {
            {
              "name": "print",
              "desc": "this should print out the dvar value of jerry",
              "cmd": "{{.jerry}}"
            }
          }
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
    
    elegant_noyce8: overall final exec vars:
    
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
    
    elegant_noyce8: overall final exec vars:
    
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
    
    elegant_noyce8: overall final exec vars:
    
    (*core.Cache)({
      "jerry": "this is jerry in task scope",
      "tom": "this is tom"
    })
    
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
    
    elegant_noyce8: overall final exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "jerry": "this is jerry in task scope"
    })
    
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
    
    elegant_noyce8: overall final exec vars:
    
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
          "cmd": "{{.jerry}}",
          "name": "print",
          "desc": "this should print out the dvar value of jerry as it is declared jerry is in taskscope"
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
    
    elegant_noyce8: overall final exec vars:
    
    (*core.Cache)({
      "jerry": "this is jerry in task scope",
      "up_runtime_task_layer_number": 1,
      "tom": "this is tom"
    })
    
    ~~SubStep1: [print: this should print out the dvar value of jerry as it is declared jerry is in taskscope ]
    this is jerry in task scope
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
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
    elegant_noyce8: overall final exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1,
      "jerry": "this is jerry in task scope"
    })
    
    ~~SubStep1: [print: remember that the caller's vars should override callee's vars
    so jerry's value should the one from caller instead this local value
     ]
    this is jerry in task scope
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
