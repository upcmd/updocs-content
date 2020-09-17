---
title: "0003_vvvvv"
date: 2020-09-18T01:28:26+99:00
draft: false
weight: 100304

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/modtests/0003/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/modtests/0003
                 WorkDir -> refdir
              AbsWorkDir -> /up_project/up/tests/modtests/0003
                TaskFile -> up.yml
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> Main
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up/tests/modtests/0003
    -exec task: Main
    loading [Task]:  ./up.yml
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc00022a9c0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "a": "caller-aaa"
    }
    
    (core.Cache) (len=1) {
     (string) (len=1) "a": (string) (len=10) "caller-aaa"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "a": "caller-aaa"
    }
    
      located task-> 1 [Main]: 
    Task1: [Main ==> Main: main entry ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: "hello-module.Say_world",
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
      "a": "caller-aaa",
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a": "caller-aaa",
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "a": "caller-aaa"
    })
    
    caller's vars to task (hello-module.Say_world)::
    (*core.Cache)({
      "a": "caller-aaa",
      "up_runtime_task_layer_number": 0
    })
    
     WARN: [config file does not exist] - [use builtin defaults]
    loading [Task]:  ./up.yml
    module: [hello-module], instance id: [nonamed], exec profile: []
     WARN: [*be aware*] - [both instance id and exec profile are not set]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc00022bbc0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ nonamed ] runtime vars:
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
    
    =>call module: [hello-module] task: [Say_world]
    Executing tasker layer: 2
    
      located task-> 2 [Say_world]: 
    Task2: [TODO: Main Caller Taskname ==> Say_world:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "... module world\na: {{.a}}\nb: {{.b}}\n"
        },
        {
          "name": "assert",
          "cmd": {
            "{{eq .a \"caller-aaa\"}}",
            "{{eq .b \"module-bbb\"}}"
          }
        },
        {
          "desc": "var b should be return to caler\n",
          "cmd": {
            "b"
          },
          "name": "return"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "a": "module-aaa",
        "b": "module-bbb"
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
      "a": "caller-aaa",
      "b": "module-bbb",
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a": "caller-aaa",
      "b": "module-bbb",
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 2
    }
    
    
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 2,
      "a": "caller-aaa",
      "b": "module-bbb",
      "up_runtime_task_layer_number": 0
    })
    
    ... module world
    a: {{.a}}
    b: {{.b}}
    
    ~SubStep1: [print:  ]
    ... module world
    a: caller-aaa
    b: module-bbb
    
    [{{eq .a "caller-aaa"}} {{eq .b "module-bbb"}}]
    ~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .a "caller-aaa"}}]
     2 ASSERT OK:     [{{eq .b "module-bbb"}}]
    [b]
    ~SubStep3: [return: var b should be return to caler
     ]
    contextual return vars:
    
    (*core.Cache)({
      "b": "module-bbb"
    })
    
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "inspect",
          "cmd": {
            "exec_vars",
            "exec_base_vars"
          }
        },
        {
          "name": "print",
          "cmd": "back to main caller\na: {{.a}}\nb: {{.b}}\n"
        },
        {
          "name": "assert",
          "des": "var b is returned from module\n",
          "cmd": {
            "{{eq .a \"caller-aaa\"}}",
            "{{eq .b \"module-bbb\"}}"
          }
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
      "b": "module-bbb",
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 2,
      "a": "caller-aaa"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a": "caller-aaa",
      "b": "module-bbb",
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 2,
      "a": "caller-aaa",
      "b": "module-bbb"
    })
    
    [exec_vars exec_base_vars]
    ~SubStep1: [inspect:  ]
     1: inspect[exec_vars]
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 2,
      "a": "caller-aaa",
      "b": "module-bbb",
      "up_runtime_task_layer_number": 0
    })
    
     2: inspect[exec_base_vars]
    {
      "a": "caller-aaa",
      "b": "module-bbb"
    }
    
    back to main caller
    a: {{.a}}
    b: {{.b}}
    
    ~SubStep2: [print:  ]
    back to main caller
    a: caller-aaa
    b: module-bbb
    
    [{{eq .a "caller-aaa"}} {{eq .b "module-bbb"}}]
    ~SubStep3: [assert:  ]
     1 ASSERT OK:     [{{eq .a "caller-aaa"}}]
     2 ASSERT OK:     [{{eq .b "module-bbb"}}]
    
```

##### Logs with different verbose level
* [m0003 log - verbose level v](../../logs/m0003_v)
* [m0003 log - verbose level vv](../../logs/m0003_vv)
* [m0003 log - verbose level vvv](../../logs/m0003_vvv)
* [m0003 log - verbose level vvvv](../../logs/m0003_vvvv)
* [m0003 log - verbose level vvvvv](../../logs/m0003_vvvvv)

##### References
* [Related Chapter](../../module/0003)
