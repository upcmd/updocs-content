---
title: "0006_vvvvv"
date: 2020-06-25T01:56:26+66:00
draft: false
weight: 100604

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/modtests/0006/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/modtests/0006
                 WorkDir -> refdir
              AbsWorkDir -> /up_project/up/tests/modtests/0006
                TaskFile -> up.yml
                 Verbose -> vvvvv
              ModuleName -> backstabbing_cray7
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up/tests/modtests/0006
    -exec task: Main
    loading [Task]:  ./up.yml
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001831a0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [backstabbing_cray7] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb"
    }
    
    (core.Cache) (len=3) {
     (string) (len=1) "a": (string) (len=17) "caller-global-aaa",
     (string) (len=1) "b": (string) (len=17) "caller-global-bbb",
     (string) (len=1) "e": (string) (len=17) "caller-global-eee"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb"
    }
    
      located task-> 1 [Main]: 
    Task1: [Main ==> Main: main entry ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "desc": "the vars in caller before invoking module task",
          "cmd": {
            "exec_vars",
            "exec_base_vars"
          },
          "name": "inspect"
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
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "e": "caller-global-eee"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "e": "caller-global-eee"
    }
    
    
    backstabbing_cray7: overall final exec vars:
    
    (*core.Cache)({
      "b": "caller-global-bbb",
      "e": "caller-global-eee",
      "a": "caller-global-aaa"
    })
    
    [exec_vars exec_base_vars]
    ~SubStep1: [inspect: the vars in caller before invoking module task ]
     1: inspect[exec_vars](*core.Cache)({
      "b": "caller-global-bbb",
      "e": "caller-global-eee",
      "a": "caller-global-aaa"
    })
    
     2: inspect[exec_base_vars]{
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb"
    }
    
    -Step2:
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
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb"
    }
    
    
    backstabbing_cray7: overall final exec vars:
    
    (*core.Cache)({
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb"
    })
    
    caller's vars to task (hello-module.Say_world)::
    (*core.Cache)({
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb"
    })
    
     WARN: [config file does not exist] - [use builtin defaults]
    loading [Task]:  ./up.yml
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001e8ca0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [hello-module] instance id: [nonamed]
    merged[ nonamed ] runtime vars:
    {
      "a": "module-global-aaa",
      "c": "module-global-ccc"
    }
    
    (core.Cache) (len=2) {
     (string) (len=1) "a": (string) (len=17) "module-global-aaa",
     (string) (len=1) "c": (string) (len=17) "module-global-ccc"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "a": "module-global-aaa",
      "c": "module-global-ccc"
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
          "name": "inspect",
          "desc": "the result would be:\na: caller-global-aaa\nb: caller-global-bbb\nc: module-global-ccc\nd: module-local-ddd\ne: caller-global-eee\n",
          "cmd": {
            "exec_vars",
            "exec_base_vars"
          }
        },
        {
          "name": "assert",
          "cmd": {
            "{{eq .a \"caller-global-aaa\"}}",
            "{{eq .b \"caller-global-bbb\"}}",
            "{{eq .c \"module-global-ccc\"}}",
            "{{eq .d \"module-local-ddd\"}}",
            "{{eq .e \"caller-global-eee\"}}"
          }
        },
        {
          "name": "return",
          "cmd": {
            "c"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "b": "module-local-bbb",
        "d": "module-local-ddd",
        "a": "module-local-aaa"
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
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "d": "module-local-ddd",
      "c": "module-global-ccc",
      "e": "caller-global-eee",
      "up_runtime_tasker_layer_number": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "d": "module-local-ddd",
      "c": "module-global-ccc",
      "e": "caller-global-eee",
      "up_runtime_tasker_layer_number": 2,
      "a": "caller-global-aaa",
      "b": "caller-global-bbb"
    }
    
    
    hello-module: overall final exec vars:
    
    (*core.Cache)({
      "d": "module-local-ddd",
      "c": "module-global-ccc",
      "e": "caller-global-eee",
      "up_runtime_tasker_layer_number": 2,
      "a": "caller-global-aaa",
      "b": "caller-global-bbb"
    })
    
    [exec_vars exec_base_vars]
    ~SubStep1: [inspect: the result would be:
    a: caller-global-aaa
    b: caller-global-bbb
    c: module-global-ccc
    d: module-local-ddd
    e: caller-global-eee
     ]
     1: inspect[exec_vars](*core.Cache)({
      "up_runtime_tasker_layer_number": 2,
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "d": "module-local-ddd",
      "c": "module-global-ccc",
      "e": "caller-global-eee"
    })
    
     2: inspect[exec_base_vars]{
      "c": "module-global-ccc",
      "a": "caller-global-aaa",
      "e": "caller-global-eee",
      "b": "caller-global-bbb"
    }
    
    [{{eq .a "caller-global-aaa"}} {{eq .b "caller-global-bbb"}} {{eq .c "module-global-ccc"}} {{eq .d "module-local-ddd"}} {{eq .e "caller-global-eee"}}]
    ~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .a "caller-global-aaa"}}]
     2 ASSERT OK:     [{{eq .b "caller-global-bbb"}}]
     3 ASSERT OK:     [{{eq .c "module-global-ccc"}}]
     4 ASSERT OK:     [{{eq .d "module-local-ddd"}}]
     5 ASSERT OK:     [{{eq .e "caller-global-eee"}}]
    [c]
    ~SubStep3: [return:  ]
    contextual return vars:
    
    (*core.Cache)({
      "c": "module-global-ccc"
    })
    
    -Step2:
    {
      Name: "",
      Do: "second_layer_internal_call",
      Dox: <nil>,
      Func: "call",
      Vars: {
        "h": "module-local-call-hhh",
        "i": "module-local-call-iii",
        "a": "module-local-call-aaa",
        "b": "module-local-call-bbb",
        "d": "module-local-call-ddd"
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
      "b": "caller-global-bbb",
      "d": "module-local-call-ddd",
      "h": "module-local-call-hhh",
      "i": "module-local-call-iii",
      "a": "caller-global-aaa",
      "up_runtime_tasker_layer_number": 2,
      "c": "module-global-ccc",
      "e": "caller-global-eee"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "e": "caller-global-eee",
      "b": "caller-global-bbb",
      "d": "module-local-call-ddd",
      "h": "module-local-call-hhh",
      "i": "module-local-call-iii",
      "a": "caller-global-aaa",
      "up_runtime_tasker_layer_number": 2,
      "c": "module-global-ccc"
    }
    
    
    hello-module: overall final exec vars:
    
    (*core.Cache)({
      "h": "module-local-call-hhh",
      "i": "module-local-call-iii",
      "a": "caller-global-aaa",
      "up_runtime_tasker_layer_number": 2,
      "c": "module-global-ccc",
      "e": "caller-global-eee",
      "b": "caller-global-bbb",
      "d": "module-local-call-ddd"
    })
    
    caller's vars to task (second_layer_internal_call)::
    (*core.Cache)({
      "d": "module-local-call-ddd",
      "h": "module-local-call-hhh",
      "i": "module-local-call-iii",
      "a": "caller-global-aaa",
      "up_runtime_tasker_layer_number": 2,
      "c": "module-global-ccc",
      "e": "caller-global-eee",
      "b": "caller-global-bbb"
    })
    
      located task-> 3 [second_layer_internal_call]: 
    =Task3: [TODO: Main Caller Taskname/Say_world ==> second_layer_internal_call:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "desc": "second_layer_internal_call\na: module-local-call-aaa\nb: module-local-call-bbb\nd: module-local-call-ddd\n",
          "cmd": {
            "exec_vars",
            "exec_base_vars"
          },
          "name": "inspect"
        },
        {
          "name": "assert",
          "cmd": {
            "{{eq .a \"caller-global-aaa\"}}",
            "{{eq .b \"caller-global-bbb\"}}",
            "{{eq .c \"module-global-ccc\"}}",
            "{{eq .d \"module-local-call-ddd\"}}",
            "{{eq .e \"caller-global-eee\"}}",
            "{{eq .i \"module-local-call-iii\"}}",
            "{{eq .h \"module-local-call-hhh\"}}",
            "{{eq .k \"module-second_layer_local-kkk\"}}"
          }
        },
        {
          "name": "return",
          "cmd": {
            "k"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "b": "module-second_layer_local-bbb",
        "d": "module-second_layer_local-ddd",
        "i": "module-second_layer_local-iii",
        "k": "module-second_layer_local-kkk",
        "a": "module-second_layer_local-aaa"
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
      "b": "caller-global-bbb",
      "k": "module-second_layer_local-kkk",
      "c": "module-global-ccc",
      "up_runtime_tasker_layer_number": 2,
      "h": "module-local-call-hhh",
      "up_runtime_task_layer_number": 1,
      "d": "module-local-call-ddd",
      "i": "module-local-call-iii",
      "a": "caller-global-aaa",
      "e": "caller-global-eee"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "b": "caller-global-bbb",
      "k": "module-second_layer_local-kkk",
      "c": "module-global-ccc",
      "i": "module-local-call-iii",
      "a": "caller-global-aaa",
      "up_runtime_tasker_layer_number": 2,
      "d": "module-local-call-ddd",
      "e": "caller-global-eee",
      "h": "module-local-call-hhh",
      "up_runtime_task_layer_number": 1
    }
    
    
    hello-module: overall final exec vars:
    
    (*core.Cache)({
      "k": "module-second_layer_local-kkk",
      "c": "module-global-ccc",
      "i": "module-local-call-iii",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "d": "module-local-call-ddd",
      "e": "caller-global-eee",
      "h": "module-local-call-hhh",
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2
    })
    
    [exec_vars exec_base_vars]
    ~~SubStep1: [inspect: second_layer_internal_call
    a: module-local-call-aaa
    b: module-local-call-bbb
    d: module-local-call-ddd
     ]
     1: inspect[exec_vars](*core.Cache)({
      "h": "module-local-call-hhh",
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2,
      "d": "module-local-call-ddd",
      "e": "caller-global-eee",
      "i": "module-local-call-iii",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "k": "module-second_layer_local-kkk",
      "c": "module-global-ccc"
    })
    
     2: inspect[exec_base_vars]{
      "i": "module-local-call-iii",
      "a": "caller-global-aaa",
      "up_runtime_tasker_layer_number": 2,
      "c": "module-global-ccc",
      "e": "caller-global-eee",
      "b": "caller-global-bbb",
      "d": "module-local-call-ddd",
      "h": "module-local-call-hhh"
    }
    
    [{{eq .a "caller-global-aaa"}} {{eq .b "caller-global-bbb"}} {{eq .c "module-global-ccc"}} {{eq .d "module-local-call-ddd"}} {{eq .e "caller-global-eee"}} {{eq .i "module-local-call-iii"}} {{eq .h "module-local-call-hhh"}} {{eq .k "module-second_layer_local-kkk"}}]
    ~~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .a "caller-global-aaa"}}]
     2 ASSERT OK:     [{{eq .b "caller-global-bbb"}}]
     3 ASSERT OK:     [{{eq .c "module-global-ccc"}}]
     4 ASSERT OK:     [{{eq .d "module-local-call-ddd"}}]
     5 ASSERT OK:     [{{eq .e "caller-global-eee"}}]
     6 ASSERT OK:     [{{eq .i "module-local-call-iii"}}]
     7 ASSERT OK:     [{{eq .h "module-local-call-hhh"}}]
     8 ASSERT OK:     [{{eq .k "module-second_layer_local-kkk"}}]
    [k]
    ~~SubStep3: [return:  ]
    contextual return vars:
    
    (*core.Cache)({
      "k": "module-second_layer_local-kkk"
    })
    
    -Step3:
    {
      Name: "",
      Do: {
        {
          "name": "return",
          "desc": "var k is return from second_layer_internal_call",
          "cmd": {
            "k"
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
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2,
      "a": "caller-global-aaa",
      "e": "caller-global-eee",
      "b": "caller-global-bbb",
      "k": "module-second_layer_local-kkk",
      "c": "module-global-ccc"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "b": "caller-global-bbb",
      "k": "module-second_layer_local-kkk",
      "c": "module-global-ccc",
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2,
      "a": "caller-global-aaa",
      "e": "caller-global-eee"
    }
    
    
    hello-module: overall final exec vars:
    
    (*core.Cache)({
      "k": "module-second_layer_local-kkk",
      "c": "module-global-ccc",
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2,
      "a": "caller-global-aaa",
      "e": "caller-global-eee",
      "b": "caller-global-bbb"
    })
    
    [k]
    ~SubStep1: [return: var k is return from second_layer_internal_call ]
    contextual return vars:
    
    (*core.Cache)({
      "c": "module-global-ccc",
      "k": "module-second_layer_local-kkk"
    })
    
    -Step3:
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
            "{{eq .a \"caller-global-aaa\"}}",
            "{{eq .b \"caller-global-bbb\"}}",
            "{{eq .c \"module-global-ccc\"}}",
            "{{eq .e \"caller-global-eee\"}}",
            "{{eq .k \"module-second_layer_local-kkk\"}}"
          },
          "name": "assert",
          "desc": "note the k is the result from the 2nd layer call\n"
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
      "up_runtime_tasker_layer_number": 2,
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "c": "module-global-ccc",
      "k": "module-second_layer_local-kkk",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "c": "module-global-ccc",
      "k": "module-second_layer_local-kkk",
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2,
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb"
    }
    
    
    backstabbing_cray7: overall final exec vars:
    
    (*core.Cache)({
      "c": "module-global-ccc",
      "k": "module-second_layer_local-kkk",
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2,
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb"
    })
    
    [exec_vars exec_base_vars]
    ~SubStep1: [inspect: the vars in caller after invoking module task ]
     1: inspect[exec_vars](*core.Cache)({
      "b": "caller-global-bbb",
      "c": "module-global-ccc",
      "k": "module-second_layer_local-kkk",
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2,
      "e": "caller-global-eee",
      "a": "caller-global-aaa"
    })
    
     2: inspect[exec_base_vars]{
      "k": "module-second_layer_local-kkk",
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "c": "module-global-ccc"
    }
    
    [{{eq .a "caller-global-aaa"}} {{eq .b "caller-global-bbb"}} {{eq .c "module-global-ccc"}} {{eq .e "caller-global-eee"}} {{eq .k "module-second_layer_local-kkk"}}]
    ~SubStep2: [assert: note the k is the result from the 2nd layer call
     ]
     1 ASSERT OK:     [{{eq .a "caller-global-aaa"}}]
     2 ASSERT OK:     [{{eq .b "caller-global-bbb"}}]
     3 ASSERT OK:     [{{eq .c "module-global-ccc"}}]
     4 ASSERT OK:     [{{eq .e "caller-global-eee"}}]
     5 ASSERT OK:     [{{eq .k "module-second_layer_local-kkk"}}]
    
```

##### Logs with different verbose level
* [m0006 log - verbose level v](../../logs/m0006_v)
* [m0006 log - verbose level vv](../../logs/m0006_vv)
* [m0006 log - verbose level vvv](../../logs/m0006_vvv)
* [m0006 log - verbose level vvvv](../../logs/m0006_vvvv)
* [m0006 log - verbose level vvvvv](../../logs/m0006_vvvvv)

##### References
* [Related Chapter](../../module/0006)