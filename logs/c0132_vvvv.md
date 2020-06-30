---
title: "c0132_vvvv"
date: 2020-07-01T15:34:40+77:00
draft: false
weight: 11323

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0132
                 Verbose -> vvvv
              ModuleName -> thirsty_jones8
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0132
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [thirsty_jones8] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "b": "global_bbb",
      "c": "global_ccc",
      "a": "global_aaa"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "a": "global_aaa",
      "b": "global_bbb",
      "c": "global_ccc"
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
          "vars": {
            "a": "block_layer2_aaa"
          },
          "do": {
            {
              "name": "assert",
              "cmd": {
                "{{eq .a \"aaa\"}}",
                "{{eq .a \"block_layer2_aaa\"}}"
              }
            },
            {
              "name": "assert",
              "cmd": {
                "{{eq .a \"aaa\"}}"
              }
            },
            {
              "name": "inspect",
              "cmd": {
                "exec_vars",
                "exec_base_vars"
              }
            }
          }
        }
      },
      Dox: <nil>,
      Func: "block",
      Vars: {
        "a": "local_aaa",
        "b": "local_bbb"
      },
      Dvars: {
        {
          Name: "da",
          Value: "local_da",
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
        },
        {
          Name: "db",
          Value: "local_db",
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
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc"
    })
    
    thirsty_jones8: overall final exec vars:
    
    (*core.Cache)({
      "b": "local_bbb",
      "c": "global_ccc",
      "da": "local_da",
      "db": "local_db",
      "a": "local_aaa"
    })
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "assert",
          "cmd": {
            "{{eq .a \"aaa\"}}",
            "{{eq .a \"block_layer2_aaa\"}}"
          }
        },
        {
          "name": "assert",
          "cmd": {
            "{{eq .a \"aaa\"}}"
          }
        },
        {
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
        "a": "block_layer2_aaa"
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
      "db": "local_db",
      "da": "local_da",
      "a": "block_layer2_aaa",
      "b": "local_bbb",
      "c": "global_ccc"
    })
    
    thirsty_jones8: overall final exec vars:
    
    (*core.Cache)({
      "c": "global_ccc",
      "db": "local_db",
      "da": "local_da",
      "a": "block_layer2_aaa",
      "b": "local_bbb"
    })
    
    ~SubStep1: [assert:  ]
     1 ASSERT FAILED: [{{eq .a "aaa"}}]
     2 ASSERT OK:     [{{eq .a "block_layer2_aaa"}}]
    ~SubStep2: [assert:  ]
     1 ASSERT FAILED: [{{eq .a "aaa"}}]
    ~SubStep3: [inspect:  ]
     1: inspect[exec_vars](*core.Cache)({
      "da": "local_da",
      "a": "block_layer2_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "db": "local_db"
    })
    
     2: inspect[exec_base_vars]{
      "a": "global_aaa",
      "b": "global_bbb",
      "c": "global_ccc"
    }
    
    
```

##### Logs with different verbose level
* [c0132 log - verbose level v](../../logs/c0132_v)
* [c0132 log - verbose level vv](../../logs/c0132_vv)
* [c0132 log - verbose level vvv](../../logs/c0132_vvv)
* [c0132 log - verbose level vvvv](../../logs/c0132_vvvv)
* [c0132 log - verbose level vvvvv](../../logs/c0132_vvvvv)

##### References
* [Related Chapter](../../test-debug/c0132)
