---
title: "c0147_vvvvv"
date: 2020-07-20T02:01:55+77:00
draft: false
weight: 11474

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0147
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0147
    -------full vars in scopes------
    (*impl.Scopes)(0xc00025b3c0)(<nil>)
    
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
      "c": "ccc",
      "a": "aaa",
      "b": "bbb"
    }
    
    (core.Cache) (len=3) {
     (string) (len=1) "c": (string) (len=3) "ccc",
     (string) (len=1) "a": (string) (len=3) "aaa",
     (string) (len=1) "b": (string) (len=3) "bbb"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "c": "ccc",
      "a": "aaa",
      "b": "bbb"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task: mock up test to test module.template rendering ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "inspect",
          "desc": "the vars in caller after invoking module task",
          "cmd": {
            "exec_vars",
            "exec_base_vars"
          }
        },
        {
          "name": "assert",
          "cmd": {
            "{{eq .b  \"bbb\"}}",
            "{{eq .d  \"ddd\"}}"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "b": "bbb",
        "d": "ddd"
      },
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: {
        "pure"
      },
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
      "d": "ddd"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "b": "bbb",
      "d": "ddd"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "b": "bbb",
      "d": "ddd"
    })
    
    [exec_vars exec_base_vars]
    ~SubStep1: [inspect: the vars in caller after invoking module task ]
     1: inspect[exec_vars](*core.Cache)({
      "b": "bbb",
      "d": "ddd"
    })
    
     2: inspect[exec_base_vars]{
      "c": "ccc",
      "a": "aaa",
      "b": "bbb"
    }
    
    [{{eq .b  "bbb"}} {{eq .d  "ddd"}}]
    ~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .b  "bbb"}}]
     2 ASSERT OK:     [{{eq .d  "ddd"}}]
    -Step2:
    {
      Name: "",
      Do: "substack",
      Dox: <nil>,
      Func: "call",
      Vars: {
        "e": "first_level_eee",
        "f": "first_level_fff"
      },
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: {
        "pure"
      },
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "e": "first_level_eee",
      "f": "first_level_fff"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "e": "first_level_eee",
      "f": "first_level_fff"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "f": "first_level_fff",
      "e": "first_level_eee"
    })
    
    caller's vars to task (substack)::
    (*core.Cache)({
      "f": "first_level_fff",
      "e": "first_level_eee"
    })
    
      located task-> 2 [substack]: 
    =Task2: [task ==> substack:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "desc": "the vars in caller after invoking module task",
          "cmd": {
            "exec_vars",
            "exec_base_vars"
          },
          "name": "inspect"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "f": "fff",
        "g": "ggg",
        "h": "hhh"
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
      "f": "first_level_fff",
      "g": "ggg",
      "h": "hhh",
      "e": "first_level_eee",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "e": "first_level_eee",
      "up_runtime_task_layer_number": 1,
      "f": "first_level_fff",
      "g": "ggg",
      "h": "hhh"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "h": "hhh",
      "e": "first_level_eee",
      "up_runtime_task_layer_number": 1,
      "f": "first_level_fff",
      "g": "ggg"
    })
    
    [exec_vars exec_base_vars]
    ~~SubStep1: [inspect: the vars in caller after invoking module task ]
     1: inspect[exec_vars](*core.Cache)({
      "h": "hhh",
      "e": "first_level_eee",
      "up_runtime_task_layer_number": 1,
      "f": "first_level_fff",
      "g": "ggg"
    })
    
     2: inspect[exec_base_vars]{
      "e": "first_level_eee",
      "f": "first_level_fff"
    }
    
    
```

##### Logs with different verbose level
* [c0147 log - verbose level v](../../logs/c0147_v)
* [c0147 log - verbose level vv](../../logs/c0147_vv)
* [c0147 log - verbose level vvv](../../logs/c0147_vvv)
* [c0147 log - verbose level vvvv](../../logs/c0147_vvvv)
* [c0147 log - verbose level vvvvv](../../logs/c0147_vvvvv)

##### References
* [Related Chapter](../../vars/c0147)
