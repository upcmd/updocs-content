---
title: "c0130_vvvv"
date: 2020-07-01T15:34:39+77:00
draft: false
weight: 11303

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
                 Verbose -> vvvv
              ModuleName -> modest_pasteur7
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0130
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [modest_pasteur7] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "a": "global_aaa",
      "b": "global_bbb",
      "c": "global_ccc"
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
    
    -Step1: [: show example the route goes to call goelse for the condition of not if condition succeeds ]
    {
      Name: "",
      Do: {
        {
          "do": {
            "echo \"shell step1\"",
            "echo \"shell step2\""
          },
          "func": "shell"
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
          "func": "block",
          "desc": "test embeded 2nd layer of block",
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
                  "name": "print",
                  "cmd": "layer 2\nup_runtime_task_layer_number: {{.up_runtime_task_layer_number}}\na: {{.a}}\nb: {{.b}}\nc: {{.c}}\nda: {{.da}}\ndb: {{.db}}\n"
                }
              }
            }
          }
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
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa"
    })
    
    modest_pasteur7: overall final exec vars:
    
    (*core.Cache)({
      "a": "local_aaa",
      "da": "local_da",
      "db": "local_db",
      "b": "local_bbb",
      "c": "global_ccc"
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
