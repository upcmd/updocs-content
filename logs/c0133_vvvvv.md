---
title: "c0133_vvvvv"
date: 2020-10-06T23:46:15+1010:00
draft: false
weight: 11334

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0133
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
    loading [Task]:  ./tests/functests/c0133
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001f78a0)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "b": "global_bbb",
      "c": "global_ccc",
      "goahead": false,
      "a": "global_aaa"
    })
    
    (*core.Cache)(0xc0000b6950)((len=4) {
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
      "goahead": false,
      "a": "global_aaa",
      "b": "global_bbb",
      "c": "global_ccc"
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
          "dvars": {
            {
              "name": "db",
              "value": "local_db_layer1"
            }
          },
          "do": {
            {
              "name": "print",
              "cmd": "layer 1\nup_runtime_task_layer_number: {{.up_runtime_task_layer_number}}\na: {{.a}}\nb: {{.b}}\nc: {{.c}}\nda: {{.da}}\ndb: {{.db}}\n"
            },
            {
              "name": "assert",
              "cmd": {
                "{{eq .a \"block_layer1_aaa\" }}",
                "{{eq .b \"local_bbb\" }}",
                "{{eq .c \"global_ccc\" }}",
                "{{eq .da \"local_da\" }}",
                "{{eq .db \"local_db_layer1\" }}"
              },
              "flags": {
                "failFast"
              }
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
                },
                {
                  "name": "assert",
                  "cmd": {
                    "{{eq .a \"block_layer2_aaa\" }}",
                    "{{eq .b \"local_block_layer2_bbb\" }}",
                    "{{eq .c \"global_ccc\" }}",
                    "{{eq .da \"local_da_layer2\" }}",
                    "{{eq .db \"local_db_layer2\" }}"
                  },
                  "flags": {
                    "failFast"
                  }
                }
              },
              "func": "cmd"
            }
          },
          "func": "block",
          "desc": "test embeded 2nd layer of block",
          "vars": {
            "a": "local_block_layer2_aaa",
            "b": "local_block_layer2_bbb"
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
      "a": "local_aaa",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 0,
      "c": "global_ccc",
      "goahead": false
    })
    
    [local] dvar expanded result:
    {
      "da": "local_da",
      "db": "local_db"
    }
    
    
    scope[local] merged: {
      "b": "local_bbb",
      "up_runtime_task_layer_number": 0,
      "c": "global_ccc",
      "goahead": false,
      "a": "local_aaa",
      "da": "local_da",
      "db": "local_db"
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
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"shell step1\"",
        "echo \"shell step2\""
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
      "a": "local_aaa",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "c": "global_ccc",
      "goahead": false
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "da": "local_da",
      "db": "local_db",
      "c": "global_ccc",
      "goahead": false,
      "a": "local_aaa",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "db": "local_db",
      "c": "global_ccc",
      "goahead": false,
      "a": "local_aaa",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 0,
      "da": "local_da"
    })
    
    cmd( 1):
    echo "shell step1"
    
    cmd=>:
    echo "shell step1"
    -
    shell step1
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"shell step1\"",
     Code: (int) 0,
     Output: (string) (len=11) "shell step1",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "shell step2"
    
    cmd=>:
    echo "shell step2"
    -
    shell step2
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"shell step2\"",
     Code: (int) 0,
     Output: (string) (len=11) "shell step2",
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
        },
        {
          "name": "assert",
          "cmd": {
            "{{eq .a \"block_layer1_aaa\" }}",
            "{{eq .b \"local_bbb\" }}",
            "{{eq .c \"global_ccc\" }}",
            "{{eq .da \"local_da\" }}",
            "{{eq .db \"local_db_layer1\" }}"
          },
          "flags": {
            "failFast"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "a": "block_layer1_aaa"
      },
      Dvars: {
        {
          Name: "db",
          Value: "local_db_layer1",
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
      "goahead": false,
      "a": "block_layer1_aaa",
      "b": "local_bbb",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step2\"",
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db"
    })
    
    [local] dvar expanded result:
    {
      "db": "local_db_layer1"
    }
    
    
    scope[local] merged: {
      "goahead": false,
      "a": "block_layer1_aaa",
      "b": "local_bbb",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step2\"",
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db_layer1",
      "c": "global_ccc"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step2\"",
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db_layer1",
      "c": "global_ccc",
      "goahead": false,
      "a": "block_layer1_aaa",
      "b": "local_bbb"
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
    a: block_layer1_aaa
    b: local_bbb
    c: global_ccc
    da: local_da
    db: local_db_layer1
    
    [{{eq .a "block_layer1_aaa" }} {{eq .b "local_bbb" }} {{eq .c "global_ccc" }} {{eq .da "local_da" }} {{eq .db "local_db_layer1" }}]
    ~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .a "block_layer1_aaa" }}]
     2 ASSERT OK:     [{{eq .b "local_bbb" }}]
     3 ASSERT OK:     [{{eq .c "global_ccc" }}]
     4 ASSERT OK:     [{{eq .da "local_da" }}]
     5 ASSERT OK:     [{{eq .db "local_db_layer1" }}]
    -Step3:
    {
      Name: "",
      Do: {
        "echo \"shell step3\"",
        "echo \"shell step4\""
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
      "goahead": false,
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "a": "local_aaa",
      "b": "local_bbb",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step2\"",
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "c": "global_ccc"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "goahead": false,
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "a": "local_aaa",
      "b": "local_bbb",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step2\"",
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "c": "global_ccc"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "a": "local_aaa",
      "b": "local_bbb",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step2\"",
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "c": "global_ccc"
    })
    
    cmd( 1):
    echo "shell step3"
    
    cmd=>:
    echo "shell step3"
    -
    shell step3
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"shell step3\"",
     Code: (int) 0,
     Output: (string) (len=11) "shell step3",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "shell step4"
    
    cmd=>:
    echo "shell step4"
    -
    shell step4
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"shell step4\"",
     Code: (int) 0,
     Output: (string) (len=11) "shell step4",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step4: [: test embeded 2nd layer of block ]
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
              "name": "print",
              "cmd": "layer 2\nup_runtime_task_layer_number: {{.up_runtime_task_layer_number}}\na: {{.a}}\nb: {{.b}}\nc: {{.c}}\nda: {{.da}}\ndb: {{.db}}\n"
            },
            {
              "flags": {
                "failFast"
              },
              "name": "assert",
              "cmd": {
                "{{eq .a \"block_layer2_aaa\" }}",
                "{{eq .b \"local_block_layer2_bbb\" }}",
                "{{eq .c \"global_ccc\" }}",
                "{{eq .da \"local_da_layer2\" }}",
                "{{eq .db \"local_db_layer2\" }}"
              }
            }
          }
        }
      },
      Dox: <nil>,
      Func: "block",
      Vars: {
        "a": "local_block_layer2_aaa",
        "b": "local_block_layer2_bbb"
      },
      Dvars: {
        {
          Name: "da",
          Value: "local_da_layer2",
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
          Value: "local_db_layer2",
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
      Desc: "test embeded 2nd layer of block",
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
      "a": "local_block_layer2_aaa",
      "b": "local_block_layer2_bbb",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step4\"",
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      }),
      "c": "global_ccc",
      "goahead": false
    })
    
    [local] dvar expanded result:
    {
      "da": "local_da_layer2",
      "db": "local_db_layer2"
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "da": "local_da_layer2",
      "db": "local_db_layer2",
      "a": "local_block_layer2_aaa",
      "b": "local_block_layer2_bbb",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step4\"",
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      }),
      "c": "global_ccc",
      "goahead": false
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "c": "global_ccc",
      "goahead": false,
      "up_runtime_task_layer_number": 0,
      "da": "local_da_layer2",
      "db": "local_db_layer2",
      "a": "local_block_layer2_aaa",
      "b": "local_block_layer2_bbb",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"shell step4\"",
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      })
    })
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "cmd": "layer 2\nup_runtime_task_layer_number: {{.up_runtime_task_layer_number}}\na: {{.a}}\nb: {{.b}}\nc: {{.c}}\nda: {{.da}}\ndb: {{.db}}\n",
          "name": "print"
        },
        {
          "name": "assert",
          "cmd": {
            "{{eq .a \"block_layer2_aaa\" }}",
            "{{eq .b \"local_block_layer2_bbb\" }}",
            "{{eq .c \"global_ccc\" }}",
            "{{eq .da \"local_da_layer2\" }}",
            "{{eq .db \"local_db_layer2\" }}"
          },
          "flags": {
            "failFast"
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
      "b": "local_block_layer2_bbb",
      "up_runtime_task_layer_number": 0,
      "da": "local_da_layer2",
      "db": "local_db_layer2",
      "c": "global_ccc",
      "goahead": false,
      "a": "block_layer2_aaa"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a": "block_layer2_aaa",
      "b": "local_block_layer2_bbb",
      "up_runtime_task_layer_number": 0,
      "da": "local_da_layer2",
      "db": "local_db_layer2",
      "c": "global_ccc",
      "goahead": false
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "block_layer2_aaa",
      "b": "local_block_layer2_bbb",
      "up_runtime_task_layer_number": 0,
      "da": "local_da_layer2",
      "db": "local_db_layer2",
      "c": "global_ccc",
      "goahead": false
    })
    
    layer 2
    up_runtime_task_layer_number: {{.up_runtime_task_layer_number}}
    a: {{.a}}
    b: {{.b}}
    c: {{.c}}
    da: {{.da}}
    db: {{.db}}
    
    ~SubStep1: [print:  ]
    layer 2
    up_runtime_task_layer_number: 0
    a: block_layer2_aaa
    b: local_block_layer2_bbb
    c: global_ccc
    da: local_da_layer2
    db: local_db_layer2
    
    [{{eq .a "block_layer2_aaa" }} {{eq .b "local_block_layer2_bbb" }} {{eq .c "global_ccc" }} {{eq .da "local_da_layer2" }} {{eq .db "local_db_layer2" }}]
    ~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .a "block_layer2_aaa" }}]
     2 ASSERT OK:     [{{eq .b "local_block_layer2_bbb" }}]
     3 ASSERT OK:     [{{eq .c "global_ccc" }}]
     4 ASSERT OK:     [{{eq .da "local_da_layer2" }}]
     5 ASSERT OK:     [{{eq .db "local_db_layer2" }}]
    -Step5:
    {
      Name: "",
      Do: {
        "echo \"shell step5\"",
        "echo \"shell step6\""
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
      "da": "local_da",
      "db": "local_db",
      "c": "global_ccc",
      "goahead": false,
      "a": "local_aaa",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "da": "local_da",
      "db": "local_db",
      "c": "global_ccc",
      "goahead": false,
      "a": "local_aaa",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "b": "local_bbb",
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "c": "global_ccc",
      "goahead": false,
      "a": "local_aaa"
    })
    
    cmd( 1):
    echo "shell step5"
    
    cmd=>:
    echo "shell step5"
    -
    shell step5
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"shell step5\"",
     Code: (int) 0,
     Output: (string) (len=11) "shell step5",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "shell step6"
    
    cmd=>:
    echo "shell step6"
    -
    shell step6
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"shell step6\"",
     Code: (int) 0,
     Output: (string) (len=11) "shell step6",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0133 log - verbose level v](../../logs/c0133_v)
* [c0133 log - verbose level vv](../../logs/c0133_vv)
* [c0133 log - verbose level vvv](../../logs/c0133_vvv)
* [c0133 log - verbose level vvvv](../../logs/c0133_vvvv)
* [c0133 log - verbose level vvvvv](../../logs/c0133_vvvvv)

##### References
* [Related Chapter](../../test-debug/c0133)
