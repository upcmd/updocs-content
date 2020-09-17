---
title: "c0168_vvvvv"
date: 2020-09-18T01:27:52+99:00
draft: false
weight: 11684

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0168
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
    loading [Task]:  ./tests/functests/c0168
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc00000c440)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
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
    
    -Step1: [: loopRange func will generate a range list named myloop
    myloop will be registered as local var
    the loop will use myloop to iterate through
     ]
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
      Dvars: {
        {
          Name: "void",
          Value: "{{ loopRange 1 5 \"myloop\"}}",
          Desc: "",
          Expand: 0,
          Flags: <nil>,
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
      Desc: "loopRange func will generate a range list named myloop\nmyloop will be registered as local var\nthe loop will use myloop to iterate through\n",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: "myloop",
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
      "myloop": {
        1,
        2,
        3,
        4,
        5
      }
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "myloop": {
        1,
        2,
        3,
        4,
        5
      }
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "myloop": {
        1,
        2,
        3,
        4,
        5
      }
    })
    
    {{.loopitem}}
    ~SubStep1: [print:  ]
    1
    {{.loopitem}}
    ~SubStep1: [print:  ]
    2
    {{.loopitem}}
    ~SubStep1: [print:  ]
    3
    {{.loopitem}}
    ~SubStep1: [print:  ]
    4
    {{.loopitem}}
    ~SubStep1: [print:  ]
    5
    -Step2: [: same as above, it will register a range list named my range
    myrange list's name is then returned from the func call in loopRange, then
    the name myrange will be used to refer to that var registered already
     ]
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
      Desc: "same as above, it will register a range list named my range\nmyrange list's name is then returned from the func call in loopRange, then\nthe name myrange will be used to refer to that var registered already\n",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: "{{ loopRange 321 330 \"myrange\"}}",
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "myloop": {
        1,
        2,
        3,
        4,
        5
      },
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "myloop": {
        1,
        2,
        3,
        4,
        5
      }
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "myloop": {
        1,
        2,
        3,
        4,
        5
      },
      "up_runtime_task_layer_number": 0
    })
    
    {{.loopitem}}
    ~SubStep1: [print:  ]
    321
    {{.loopitem}}
    ~SubStep1: [print:  ]
    322
    {{.loopitem}}
    ~SubStep1: [print:  ]
    323
    {{.loopitem}}
    ~SubStep1: [print:  ]
    324
    {{.loopitem}}
    ~SubStep1: [print:  ]
    325
    {{.loopitem}}
    ~SubStep1: [print:  ]
    326
    {{.loopitem}}
    ~SubStep1: [print:  ]
    327
    {{.loopitem}}
    ~SubStep1: [print:  ]
    328
    {{.loopitem}}
    ~SubStep1: [print:  ]
    329
    {{.loopitem}}
    ~SubStep1: [print:  ]
    330
    
```

##### Logs with different verbose level
* [c0168 log - verbose level v](../../logs/c0168_v)
* [c0168 log - verbose level vv](../../logs/c0168_vv)
* [c0168 log - verbose level vvv](../../logs/c0168_vvv)
* [c0168 log - verbose level vvvv](../../logs/c0168_vvvv)
* [c0168 log - verbose level vvvvv](../../logs/c0168_vvvvv)

##### References
* [Related Chapter](../../loop/c0168)
