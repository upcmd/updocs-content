---
title: "c0130_vvvvv"
date: 2020-07-01T15:34:39+77:00
draft: false
weight: 11304

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0130
                 Verbose -> vvvvv
              ModuleName -> agitated_elion5
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0130
    -------full vars in scopes------
    (*impl.Scopes)(0xc000185680)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [agitated_elion5] instance id: [dev]
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
    
    -Step1: [: show example the route goes to call goelse for the condition of not if condition succeeds ]
    {
      Name: "",
      Do: {
        {
          "func": "shell",
          "do": {
            "echo \"shell step1\"",
            "echo \"shell step2\""
          }
        },
        {
          "func": "cmd",
          "vars": {
            "a": "block_layer1_aaa"
          },
          "do": {
            {
              "name": "print",
              "cmd": "layer 1\nup_runtime_task_layer_number: {{.up_runtime_task_layer_number}}\na: {{.a}}\nb: {{.b}}\nc: {{.c}}\nda: {{.da}}\ndb: {{.db}}\n"
            }
          }
        },
        {
          "func": "shell",
          "do": {
            "echo \"shell step3\"",
            "echo \"shell step4\""
          }
        },
        {
          "vars": {
            "a": "local_block_layer2_aaa",
            "b": "local_block_layer2_bbb"
          },
          "dvars": {
            {
              "name": "da",
              "value": "local_da_layer2"
            },
            {
              "name": "db",
              "value": "local_db_layer2"
            }
          },
          "do": {
            {
              "func": "cmd",
              "vars": {
                "a": "block_layer2_aaa"
              },
              "do": {
                {
                  "cmd": "layer 2\nup_runtime_task_layer_number: {{.up_runtime_task_layer_number}}\na: {{.a}}\nb: {{.b}}\nc: {{.c}}\nda: {{.da}}\ndb: {{.db}}\n",
                  "name": "print"
                }
              }
            }
          },
          "func": "block",
          "desc": "test embeded 2nd layer of block"
        },
        {
          "func": "shell",
          "do": {
            "echo \"shell step5\"",
            "echo \"shell step6\""
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
      Desc: "show example the route goes to call goelse for the condition of not if condition succeeds",
      Reg: "",
      Flags: <nil>,
      If: "{{.goahead}}",
      Else: {
        {
          "func": "shell",
          "do": {
            "echo \"else step1\"",
            "echo \"else step2\""
          }
        },
        {
          "func": "cmd",
          "vars": {
            "a": "block_layer1_aaa_else"
          },
          "do": {
            {
              "name": "print",
              "cmd": "layer 1\nup_runtime_task_layer_number: {{.up_runtime_task_layer_number}}\na: {{.a}}\nb: {{.b}}\nc: {{.c}}\nda: {{.da}}\ndb: {{.db}}\n"
            }
          }
        }
      },
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
    
    [local] dvar expanded result:
    {
      "db": "local_db",
      "da": "local_da"
    }
    
    
    scope[local] merged: {
      "b": "local_bbb",
      "c": "global_ccc",
      "da": "local_da",
      "db": "local_db",
      "a": "local_aaa"
    }
    
    
    agitated_elion5: overall final exec vars:
    
    (*core.Cache)({
      "c": "global_ccc",
      "da": "local_da",
      "db": "local_db",
      "a": "local_aaa",
      "b": "local_bbb"
    })
    
    condition failed, skip executing step 
    
    
```

##### Logs with different verbose level
* [c0130 log - verbose level v](../../logs/c0130_v)
* [c0130 log - verbose level vv](../../logs/c0130_vv)
* [c0130 log - verbose level vvv](../../logs/c0130_vvv)
* [c0130 log - verbose level vvvv](../../logs/c0130_vvvv)
* [c0130 log - verbose level vvvvv](../../logs/c0130_vvvvv)

##### References
* [Related Chapter](../../block-func/c0130)
