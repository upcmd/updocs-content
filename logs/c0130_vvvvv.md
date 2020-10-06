---
title: "c0130_vvvvv"
date: 2020-10-07T00:11:23+1010:00
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
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0130
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc000210b00)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "c": "global_ccc",
      "goahead": false,
      "a": "global_aaa",
      "b": "global_bbb"
    })
    
    (*core.Cache)(0xc000212138)((len=4) {
     (string) (len=7) "goahead": (bool) false,
     (string) (len=1) "a": (string) (len=10) "global_aaa",
     (string) (len=1) "b": (string) (len=10) "global_bbb",
     (string) (len=1) "c": (string) (len=10) "global_ccc"
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "b": "global_bbb",
      "c": "global_ccc",
      "goahead": false,
      "a": "global_aaa"
    })
    
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
              "vars": {
                "a": "block_layer2_aaa"
              },
              "do": {
                {
                  "name": "print",
                  "cmd": "layer 2\nup_runtime_task_layer_number: {{.up_runtime_task_layer_number}}\na: {{.a}}\nb: {{.b}}\nc: {{.c}}\nda: {{.da}}\ndb: {{.db}}\n"
                }
              },
              "func": "cmd"
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
          "do": {
            "echo \"else step1\"",
            "echo \"else step2\""
          },
          "func": "shell"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "b": "local_bbb",
      "c": "global_ccc",
      "up_runtime_task_layer_number": 0,
      "goahead": false,
      "a": "local_aaa"
    })
    
    [local] dvar expanded result:
    {
      "da": "local_da",
      "db": "local_db"
    }
    
    
    scope[local] merged: {
      "goahead": false,
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "c": "global_ccc",
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "goahead": false,
      "a": "local_aaa",
      "b": "local_bbb"
    })
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"else step1\"",
        "echo \"else step2\""
      },
      Dox: <nil>,
      Func: "shell",
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
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "c": "global_ccc",
      "goahead": false,
      "a": "local_aaa",
      "b": "local_bbb"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "b": "local_bbb",
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "c": "global_ccc",
      "goahead": false,
      "a": "local_aaa"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "c": "global_ccc",
      "goahead": false,
      "a": "local_aaa",
      "b": "local_bbb"
    })
    
    cmd( 1):
    echo "else step1"
    
    cmd=>:
    echo "else step1"
    -
    else step1
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=17) "echo \"else step1\"",
     Code: (int) 0,
     Output: (string) (len=10) "else step1",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "else step2"
    
    cmd=>:
    echo "else step2"
    -
    else step2
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=17) "echo \"else step2\"",
     Code: (int) 0,
     Output: (string) (len=10) "else step2",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "layer 1\nup_runtime_task_layer_number: {{.up_runtime_task_layer_number}}\na: {{.a}}\nb: {{.b}}\nc: {{.c}}\nda: {{.da}}\ndb: {{.db}}\n"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "a": "block_layer1_aaa_else"
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
      "c": "global_ccc",
      "goahead": false,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"else step2\"",
        Code: 0,
        Output: "else step2",
        ErrMsg: ""
      }),
      "a": "block_layer1_aaa_else",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a": "block_layer1_aaa_else",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "c": "global_ccc",
      "goahead": false,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"else step2\"",
        Code: 0,
        Output: "else step2",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "db": "local_db",
      "c": "global_ccc",
      "goahead": false,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"else step2\"",
        Code: 0,
        Output: "else step2",
        ErrMsg: ""
      }),
      "a": "block_layer1_aaa_else",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 0,
      "da": "local_da"
    })
    
    layer 1
    up_runtime_task_layer_number: {{.up_runtime_task_layer_number}}
    a: {{.a}}
    b: {{.b}}
    c: {{.c}}
    da: {{.da}}
    db: {{.db}}
    
    ~SubStep1: [print:  ]
    layer 1
    up_runtime_task_layer_number: 0
    a: block_layer1_aaa_else
    b: local_bbb
    c: global_ccc
    da: local_da
    db: local_db
    
    
```

##### Logs with different verbose level
* [c0130 log - verbose level v](../../logs/c0130_v)
* [c0130 log - verbose level vv](../../logs/c0130_vv)
* [c0130 log - verbose level vvv](../../logs/c0130_vvv)
* [c0130 log - verbose level vvvv](../../logs/c0130_vvvv)
* [c0130 log - verbose level vvvvv](../../logs/c0130_vvvvv)

##### References
* [Related Chapter](../../block-func/c0130)
