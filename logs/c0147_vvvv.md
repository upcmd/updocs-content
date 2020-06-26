---
title: "c0147_vvvv"
date: 2020-06-27T03:09:35+66:00
draft: false
weight: 11473

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
                 Verbose -> vvvv
              ModuleName -> insane_brattain5
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0147
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [insane_brattain5] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "a": "aaa",
      "b": "bbb",
      "c": "ccc"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "a": "aaa",
      "b": "bbb",
      "c": "ccc"
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
    
    insane_brattain5: overall final exec vars:
    
    (*core.Cache)({
      "b": "bbb",
      "d": "ddd"
    })
    
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
    
    insane_brattain5: overall final exec vars:
    
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
          "cmd": {
            "exec_vars",
            "exec_base_vars"
          },
          "name": "inspect",
          "desc": "the vars in caller after invoking module task"
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "g": "ggg",
      "h": "hhh",
      "f": "first_level_fff",
      "up_runtime_task_layer_number": 1,
      "e": "first_level_eee"
    })
    
    insane_brattain5: overall final exec vars:
    
    (*core.Cache)({
      "g": "ggg",
      "h": "hhh",
      "f": "first_level_fff",
      "up_runtime_task_layer_number": 1,
      "e": "first_level_eee"
    })
    
    ~~SubStep1: [inspect: the vars in caller after invoking module task ]
     1: inspect[exec_vars](*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "e": "first_level_eee",
      "g": "ggg",
      "h": "hhh",
      "f": "first_level_fff"
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
