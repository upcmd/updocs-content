---
title: "c0147_vvvvv"
date: 2020-10-07T00:11:26+1010:00
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
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0147
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001bf5e0)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "b": "bbb-global",
      "c": "ccc",
      "a": "aaa"
    })
    
    (*core.Cache)(0xc00000e940)((len=3) {
     (string) (len=1) "c": (string) (len=3) "ccc",
     (string) (len=1) "a": (string) (len=3) "aaa",
     (string) (len=1) "b": (string) (len=10) "bbb-global"
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "b": "bbb-global",
      "c": "ccc",
      "a": "aaa"
    })
    
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
          "cmd": {
            "{{eq .b  \"bbb\"}}",
            "{{eq .d  \"ddd\"}}"
          },
          "name": "assert"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "b": "bbb",
      "d": "ddd"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "d": "ddd",
      "up_runtime_task_layer_number": 0,
      "b": "bbb"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "b": "bbb",
      "d": "ddd"
    })
    
    [exec_vars exec_base_vars]
    ~SubStep1: [inspect: the vars in caller after invoking module task ]
     1: inspect[exec_vars]
    (*core.Cache)({
      "b": "bbb",
      "d": "ddd",
      "up_runtime_task_layer_number": 0
    })
    
     2: inspect[exec_base_vars]
    {
      "b": "bbb-global",
      "c": "ccc",
      "a": "aaa"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "e": "first_level_eee",
      "f": "first_level_fff"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "e": "first_level_eee",
      "f": "first_level_fff"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "e": "first_level_eee",
      "f": "first_level_fff"
    })
    
    caller's vars to task (substack)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "e": "first_level_eee",
      "f": "first_level_fff"
    })
    
      located task-> 2 [substack]: 
    =Task2: [task ==> substack:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "cmd": {
            "exec_vars",
            "exec_base_vars"
          },
          "name": "inspect",
          "desc": "the vars in caller after invoking module task"
        },
        {
          "name": "assert",
          "cmd": {
            "{{eq .f  \"first_level_fff\"}}",
            "{{eq .e  \"first_level_eee\"}}",
            "{{eq .g  \"ggg\"}}"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "g": "ggg",
        "h": "hhh",
        "f": "fff"
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
      "f": "first_level_fff",
      "up_runtime_task_layer_number": 1,
      "e": "first_level_eee",
      "g": "ggg",
      "h": "hhh"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "g": "ggg",
      "h": "hhh",
      "f": "first_level_fff",
      "up_runtime_task_layer_number": 1,
      "e": "first_level_eee"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "g": "ggg",
      "h": "hhh",
      "f": "first_level_fff",
      "up_runtime_task_layer_number": 1,
      "e": "first_level_eee"
    })
    
    [exec_vars exec_base_vars]
    ~~SubStep1: [inspect: the vars in caller after invoking module task ]
     1: inspect[exec_vars]
    (*core.Cache)({
      "f": "first_level_fff",
      "up_runtime_task_layer_number": 1,
      "e": "first_level_eee",
      "g": "ggg",
      "h": "hhh"
    })
    
     2: inspect[exec_base_vars]
    {
      "up_runtime_task_layer_number": 0,
      "e": "first_level_eee",
      "f": "first_level_fff"
    }
    
    [{{eq .f  "first_level_fff"}} {{eq .e  "first_level_eee"}} {{eq .g  "ggg"}}]
    ~~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .f  "first_level_fff"}}]
     2 ASSERT OK:     [{{eq .e  "first_level_eee"}}]
     3 ASSERT OK:     [{{eq .g  "ggg"}}]
    
```

##### Logs with different verbose level
* [c0147 log - verbose level v](../../logs/c0147_v)
* [c0147 log - verbose level vv](../../logs/c0147_vv)
* [c0147 log - verbose level vvv](../../logs/c0147_vvv)
* [c0147 log - verbose level vvvv](../../logs/c0147_vvvv)
* [c0147 log - verbose level vvvvv](../../logs/c0147_vvvvv)

##### References
* [Related Chapter](../../vars/c0147)
