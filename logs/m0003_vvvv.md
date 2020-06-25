---
title: "0003_vvvv"
date: 2020-06-25T01:56:26+66:00
draft: false
weight: 100303

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
                 Verbose -> vvvv
              ModuleName -> thirsty_jones6
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up/tests/modtests/0003
    -exec task: Main
    loading [Task]:  ./up.yml
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [thirsty_jones6] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "a": "caller-aaa"
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "a": "caller-aaa"
    })
    
    thirsty_jones6: overall final exec vars:
    
    (*core.Cache)({
      "a": "caller-aaa"
    })
    
     WARN: [config file does not exist] - [use builtin defaults]
    loading [Task]:  ./up.yml
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [hello-module] instance id: [nonamed]
    merged[ nonamed ] runtime vars:
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
          "name": "return",
          "desc": "var b should be return to caler\n",
          "cmd": {
            "b"
          }
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "a": "caller-aaa",
      "b": "module-bbb",
      "up_runtime_tasker_layer_number": 2
    })
    
    hello-module: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 2,
      "a": "caller-aaa",
      "b": "module-bbb"
    })
    
    ~SubStep1: [print:  ]
    ... module world
    a: caller-aaa
    b: module-bbb
    
    ~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .a "caller-aaa"}}]
     2 ASSERT OK:     [{{eq .b "module-bbb"}}]
    ~SubStep3: [return: var b should be return to caler
     ]
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "a": "caller-aaa",
      "b": "module-bbb",
      "up_runtime_tasker_layer_number": 2
    })
    
    thirsty_jones6: overall final exec vars:
    
    (*core.Cache)({
      "b": "module-bbb",
      "up_runtime_tasker_layer_number": 2,
      "a": "caller-aaa"
    })
    
    ~SubStep1: [inspect:  ]
     1: inspect[exec_vars](*core.Cache)({
      "b": "module-bbb",
      "up_runtime_tasker_layer_number": 2,
      "a": "caller-aaa"
    })
    
     2: inspect[exec_base_vars]{
      "a": "caller-aaa",
      "b": "module-bbb"
    }
    
    ~SubStep2: [print:  ]
    back to main caller
    a: caller-aaa
    b: module-bbb
    
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