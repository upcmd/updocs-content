---
title: "c0132_vvvvv"
date: 2020-08-18T15:16:15+88:00
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
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0132
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc00022a6c0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "a": "global_aaa",
      "b": "global_bbb",
      "c": "global_ccc"
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
      "c": "global_ccc",
      "a": "global_aaa",
      "b": "global_bbb"
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
              "cmd": {
                "exec_vars",
                "exec_base_vars"
              },
              "name": "inspect"
            }
          }
        }
      },
      Dox: <nil>,
      Func: "block",
      Vars: {
        "b": "local_bbb",
        "a": "local_aaa"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "c": "global_ccc",
      "a": "local_aaa",
      "b": "local_bbb"
    })
    
    [local] dvar expanded result:
    {
      "db": "local_db",
      "da": "local_da"
    }
    
    
    scope[local] merged: {
      "da": "local_da",
      "db": "local_db",
      "c": "global_ccc",
      "a": "local_aaa",
      "b": "local_bbb"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "db": "local_db",
      "c": "global_ccc",
      "a": "local_aaa",
      "b": "local_bbb",
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "da": "local_da",
      "db": "local_db",
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "block_layer2_aaa"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a": "block_layer2_aaa",
      "da": "local_da",
      "db": "local_db",
      "b": "local_bbb",
      "c": "global_ccc"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "block_layer2_aaa",
      "da": "local_da",
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
     1: inspect[exec_vars]
    (*core.Cache)({
      "da": "local_da",
      "db": "local_db",
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "block_layer2_aaa"
    })
    
     2: inspect[exec_base_vars]
    {
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
