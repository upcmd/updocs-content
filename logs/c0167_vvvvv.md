---
title: "c0167_vvvvv"
date: 2020-09-18T00:51:53+99:00
draft: false
weight: 11674

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0167
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
    loading [Task]:  ./tests/functests/c0167
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc000173000)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "items": {
        "item1",
        "item2",
        "item3"
      },
      "loopkey": "items"
    }
    
    (core.Cache) (len=2) {
     (string) (len=5) "items": ([]interface {}) (len=3 cap=3) {
      (string) (len=5) "item1",
      (string) (len=5) "item2",
      (string) (len=5) "item3"
     },
     (string) (len=7) "loopkey": (string) (len=5) "items"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "items": {
        "item1",
        "item2",
        "item3"
      },
      "loopkey": "items"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: demo varname to ref to a loop item from var ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.loopitem}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "demo varname to ref to a loop item from var",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: "items",
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
      "loopkey": "items",
      "items": {
        "item1",
        "item2",
        "item3"
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopkey": "items",
      "items": {
        "item1",
        "item2",
        "item3"
      },
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopkey": "items",
      "items": {
        "item1",
        "item2",
        "item3"
      },
      "up_runtime_task_layer_number": 0
    })
    
    {{.loopitem}}
    ~SubStep1: [print:  ]
    item1
    {{.loopitem}}
    ~SubStep1: [print:  ]
    item2
    {{.loopitem}}
    ~SubStep1: [print:  ]
    item3
    -Step2: [: demo use dynamic key to ref to a loop item from var ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.loopitem}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "demo use dynamic key to ref to a loop item from var",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: "{{.loopkey}}",
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "items": {
        "item1",
        "item2",
        "item3"
      },
      "loopkey": "items",
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "items": {
        "item1",
        "item2",
        "item3"
      },
      "loopkey": "items",
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "items": {
        "item1",
        "item2",
        "item3"
      },
      "loopkey": "items",
      "up_runtime_task_layer_number": 0
    })
    
    {{.loopitem}}
    ~SubStep1: [print:  ]
    item1
    {{.loopitem}}
    ~SubStep1: [print:  ]
    item2
    {{.loopitem}}
    ~SubStep1: [print:  ]
    item3
    
```

##### Logs with different verbose level
* [c0167 log - verbose level v](../../logs/c0167_v)
* [c0167 log - verbose level vv](../../logs/c0167_vv)
* [c0167 log - verbose level vvv](../../logs/c0167_vvv)
* [c0167 log - verbose level vvvv](../../logs/c0167_vvvv)
* [c0167 log - verbose level vvvvv](../../logs/c0167_vvvvv)

##### References
* [Related Chapter](../../loop/c0167)
