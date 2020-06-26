---
title: "c0132_vvvvv"
date: 2020-06-27T03:09:32+66:00
draft: false
weight: 11324

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
                 Verbose -> vvvvv
              ModuleName -> backstabbing_hawking1
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0132
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ed260)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [backstabbing_hawking1] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "c": "global_ccc",
      "a": "global_aaa",
      "b": "global_bbb"
    }
    
    (core.Cache) (len=3) {
     (string) (len=1) "c": (string) (len=10) "global_ccc",
     (string) (len=1) "a": (string) (len=10) "global_aaa",
     (string) (len=1) "b": (string) (len=10) "global_bbb"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "b": "global_bbb",
      "c": "global_ccc",
      "a": "global_aaa"
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
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa"
    })
    
    [local] dvar expanded result:
    {
      "da": "local_da",
      "db": "local_db"
    }
    
    
    scope[local] merged: {
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "db": "local_db",
      "da": "local_da"
    }
    
    
    backstabbing_hawking1: overall final exec vars:
    
    (*core.Cache)({
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "db": "local_db",
      "da": "local_da"
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
          "cmd": {
            "{{eq .a \"aaa\"}}"
          },
          "name": "assert"
        },
        {
          "name": "inspect",
          "cmd": {
            "exec_vars",
            "exec_base_vars"
          }
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
      "c": "global_ccc",
      "a": "block_layer2_aaa",
      "db": "local_db",
      "da": "local_da",
      "b": "local_bbb"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "block_layer2_aaa",
      "db": "local_db",
      "da": "local_da"
    }
    
    
    backstabbing_hawking1: overall final exec vars:
    
    (*core.Cache)({
      "da": "local_da",
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "block_layer2_aaa",
      "db": "local_db"
    })
    
    [{{eq .a "aaa"}} {{eq .a "block_layer2_aaa"}}]
    ~SubStep1: [assert:  ]
     1 ASSERT FAILED: [{{eq .a "aaa"}}]
     2 ASSERT OK:     [{{eq .a "block_layer2_aaa"}}]
    [{{eq .a "aaa"}}]
    ~SubStep2: [assert:  ]
     1 ASSERT FAILED: [{{eq .a "aaa"}}]
    [exec_vars exec_base_vars]
    ~SubStep3: [inspect:  ]
     1: inspect[exec_vars](*core.Cache)({
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "block_layer2_aaa",
      "db": "local_db",
      "da": "local_da"
    })
    
     2: inspect[exec_base_vars]{
      "b": "global_bbb",
      "c": "global_ccc",
      "a": "global_aaa"
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
