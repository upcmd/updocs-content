---
title: "0006_vvvvv"
date: 2020-06-27T03:09:47+66:00
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
              ModuleName -> determined_mclean0
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up/tests/modtests/0006
    -exec task: Main
    loading [Task]:  ./up.yml
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ed1a0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [determined_mclean0] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb"
    }
    
    (core.Cache) (len=3) {
     (string) (len=1) "e": (string) (len=17) "caller-global-eee",
     (string) (len=1) "a": (string) (len=17) "caller-global-aaa",
     (string) (len=1) "b": (string) (len=17) "caller-global-bbb"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "e": "caller-global-eee"
    }
    
      located task-> 1 [Main]: 
    Task1: [Main ==> Main: main entry ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "cmd": {
            "exec_vars",
            "exec_base_vars"
          },
          "name": "inspect",
          "desc": "the vars in caller before invoking module task"
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
    
    
    determined_mclean0: overall final exec vars:
    
    (*core.Cache)({
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb"
    })
    
    [exec_vars exec_base_vars]
    ~SubStep1: [inspect: the vars in caller before invoking module task ]
     1: inspect[exec_vars](*core.Cache)({
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb"
    })
    
     2: inspect[exec_base_vars]{
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "e": "caller-global-eee"
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
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "e": "caller-global-eee"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb"
    }
    
    
    determined_mclean0: overall final exec vars:
    
    (*core.Cache)({
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "e": "caller-global-eee"
    })
    
    caller's vars to task (hello-module.Say_world)::
    (*core.Cache)({
      "b": "caller-global-bbb",
      "e": "caller-global-eee",
      "a": "caller-global-aaa"
    })
    
     WARN: [config file does not exist] - [use builtin defaults]
    loading [Task]:  ./up.yml
    -------full vars in scopes------
    (*impl.Scopes)(0xc000254ca0)(<nil>)
    
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
        "a": "module-local-aaa",
        "b": "module-local-bbb",
        "d": "module-local-ddd"
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
      "e": "caller-global-eee",
      "up_runtime_tasker_layer_number": 2,
      "c": "module-global-ccc",
      "b": "caller-global-bbb",
      "d": "module-local-ddd",
      "a": "caller-global-aaa"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "b": "caller-global-bbb",
      "d": "module-local-ddd",
      "a": "caller-global-aaa",
      "e": "caller-global-eee",
      "up_runtime_tasker_layer_number": 2,
      "c": "module-global-ccc"
    }
    
    
    hello-module: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 2,
      "c": "module-global-ccc",
      "b": "caller-global-bbb",
      "d": "module-local-ddd",
      "a": "caller-global-aaa",
      "e": "caller-global-eee"
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
      "b": "caller-global-bbb",
      "d": "module-local-ddd",
      "a": "caller-global-aaa",
      "e": "caller-global-eee",
      "up_runtime_tasker_layer_number": 2,
      "c": "module-global-ccc"
    })
    
     2: inspect[exec_base_vars]{
      "c": "module-global-ccc",
      "b": "caller-global-bbb",
      "e": "caller-global-eee",
      "a": "caller-global-aaa"
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
        "d": "module-local-call-ddd",
        "h": "module-local-call-hhh",
        "i": "module-local-call-iii",
        "a": "module-local-call-aaa",
        "b": "module-local-call-bbb"
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
      "d": "module-local-call-ddd",
      "h": "module-local-call-hhh",
      "i": "module-local-call-iii",
      "up_runtime_tasker_layer_number": 2,
      "e": "caller-global-eee",
      "c": "module-global-ccc",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "h": "module-local-call-hhh",
      "i": "module-local-call-iii",
      "up_runtime_tasker_layer_number": 2,
      "e": "caller-global-eee",
      "c": "module-global-ccc",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "d": "module-local-call-ddd"
    }
    
    
    hello-module: overall final exec vars:
    
    (*core.Cache)({
      "b": "caller-global-bbb",
      "d": "module-local-call-ddd",
      "h": "module-local-call-hhh",
      "i": "module-local-call-iii",
      "up_runtime_tasker_layer_number": 2,
      "e": "caller-global-eee",
      "c": "module-global-ccc",
      "a": "caller-global-aaa"
    })
    
    caller's vars to task (second_layer_internal_call)::
    (*core.Cache)({
      "e": "caller-global-eee",
      "c": "module-global-ccc",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "d": "module-local-call-ddd",
      "h": "module-local-call-hhh",
      "i": "module-local-call-iii",
      "up_runtime_tasker_layer_number": 2
    })
    
      located task-> 3 [second_layer_internal_call]: 
    =Task3: [TODO: Main Caller Taskname/Say_world ==> second_layer_internal_call:  ]
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
          "desc": "second_layer_internal_call\na: module-local-call-aaa\nb: module-local-call-bbb\nd: module-local-call-ddd\n"
        },
        {
          "cmd": {
            "{{eq .a \"caller-global-aaa\"}}",
            "{{eq .b \"caller-global-bbb\"}}",
            "{{eq .c \"module-global-ccc\"}}",
            "{{eq .d \"module-local-call-ddd\"}}",
            "{{eq .e \"caller-global-eee\"}}",
            "{{eq .i \"module-local-call-iii\"}}",
            "{{eq .h \"module-local-call-hhh\"}}",
            "{{eq .k \"module-second_layer_local-kkk\"}}"
          },
          "name": "assert"
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
        "a": "module-second_layer_local-aaa",
        "b": "module-second_layer_local-bbb",
        "d": "module-second_layer_local-ddd",
        "i": "module-second_layer_local-iii",
        "k": "module-second_layer_local-kkk"
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
      "e": "caller-global-eee",
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1,
      "d": "module-local-call-ddd",
      "i": "module-local-call-iii",
      "k": "module-second_layer_local-kkk",
      "a": "caller-global-aaa",
      "h": "module-local-call-hhh",
      "c": "module-global-ccc"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "c": "module-global-ccc",
      "up_runtime_tasker_layer_number": 2,
      "i": "module-local-call-iii",
      "k": "module-second_layer_local-kkk",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "e": "caller-global-eee",
      "h": "module-local-call-hhh",
      "up_runtime_task_layer_number": 1,
      "d": "module-local-call-ddd"
    }
    
    
    hello-module: overall final exec vars:
    
    (*core.Cache)({
      "d": "module-local-call-ddd",
      "up_runtime_task_layer_number": 1,
      "i": "module-local-call-iii",
      "k": "module-second_layer_local-kkk",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "e": "caller-global-eee",
      "h": "module-local-call-hhh",
      "c": "module-global-ccc",
      "up_runtime_tasker_layer_number": 2
    })
    
    [exec_vars exec_base_vars]
    ~~SubStep1: [inspect: second_layer_internal_call
    a: module-local-call-aaa
    b: module-local-call-bbb
    d: module-local-call-ddd
     ]
     1: inspect[exec_vars](*core.Cache)({
      "k": "module-second_layer_local-kkk",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "e": "caller-global-eee",
      "h": "module-local-call-hhh",
      "c": "module-global-ccc",
      "up_runtime_tasker_layer_number": 2,
      "i": "module-local-call-iii",
      "up_runtime_task_layer_number": 1,
      "d": "module-local-call-ddd"
    })
    
     2: inspect[exec_base_vars]{
      "b": "caller-global-bbb",
      "d": "module-local-call-ddd",
      "h": "module-local-call-hhh",
      "i": "module-local-call-iii",
      "up_runtime_tasker_layer_number": 2,
      "e": "caller-global-eee",
      "c": "module-global-ccc",
      "a": "caller-global-aaa"
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
      "a": "caller-global-aaa",
      "c": "module-global-ccc",
      "b": "caller-global-bbb",
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2,
      "e": "caller-global-eee",
      "k": "module-second_layer_local-kkk"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2,
      "e": "caller-global-eee",
      "k": "module-second_layer_local-kkk",
      "a": "caller-global-aaa",
      "c": "module-global-ccc",
      "b": "caller-global-bbb"
    }
    
    
    hello-module: overall final exec vars:
    
    (*core.Cache)({
      "e": "caller-global-eee",
      "k": "module-second_layer_local-kkk",
      "a": "caller-global-aaa",
      "c": "module-global-ccc",
      "b": "caller-global-bbb",
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2
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
          "name": "assert",
          "desc": "note the k is the result from the 2nd layer call\n",
          "cmd": {
            "{{eq .a \"caller-global-aaa\"}}",
            "{{eq .b \"caller-global-bbb\"}}",
            "{{eq .c \"module-global-ccc\"}}",
            "{{eq .e \"caller-global-eee\"}}",
            "{{eq .k \"module-second_layer_local-kkk\"}}"
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
      "b": "caller-global-bbb",
      "c": "module-global-ccc",
      "k": "module-second_layer_local-kkk",
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1,
      "b": "caller-global-bbb",
      "c": "module-global-ccc",
      "k": "module-second_layer_local-kkk",
      "e": "caller-global-eee",
      "a": "caller-global-aaa"
    }
    
    
    determined_mclean0: overall final exec vars:
    
    (*core.Cache)({
      "a": "caller-global-aaa",
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1,
      "b": "caller-global-bbb",
      "c": "module-global-ccc",
      "k": "module-second_layer_local-kkk",
      "e": "caller-global-eee"
    })
    
    [exec_vars exec_base_vars]
    ~SubStep1: [inspect: the vars in caller after invoking module task ]
     1: inspect[exec_vars](*core.Cache)({
      "c": "module-global-ccc",
      "k": "module-second_layer_local-kkk",
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1,
      "b": "caller-global-bbb"
    })
    
     2: inspect[exec_base_vars]{
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "c": "module-global-ccc",
      "k": "module-second_layer_local-kkk"
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
