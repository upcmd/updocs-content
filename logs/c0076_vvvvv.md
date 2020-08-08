---
title: "c0076_vvvvv"
date: 2020-08-09T01:36:10+88:00
draft: false
weight: 10764

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0076
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
    loading [Task]:  ./tests/functests/c0076
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc000173300)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
    }
    
    (core.Cache) {
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task: test the exit scenarios due to different types of validation ]
    Executing task stack layer: 1
    
    -Step1: [: step1 ]
    {
      Name: "",
      Do: {
        "echo hanks"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "step1",
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
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo hanks
    
    cmd=>:
    echo hanks<=
    hanks
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=10) "echo hanks",
     Code: (int) 0,
     Output: (string) (len=5) "hanks",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2: [: test register a variable to global vars
    the reg_hello should be <no value> since this is a template action
    you should really use dvar name void instead
     ]
    {
      Name: "",
      Do: <nil>,
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "reg_hello",
          Value: "{{.last_result.Output |reg \"hellomsg\" }}\n",
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
      Desc: "test register a variable to global vars\nthe reg_hello should be <no value> since this is a template action\nyou should really use dvar name void instead\n",
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
      "last_result": (*utils.ExecResult)({
        Cmd: "echo hanks",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
      "hellomsg": "hanks",
      "reg_hello": "hanks\n\n"
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo hanks",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "hellomsg": "hanks",
      "reg_hello": "hanks\n\n"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo hanks",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "hellomsg": "hanks",
      "reg_hello": "hanks\n\n"
    })
    
     WARN: [cmd] - [Not implemented or void for no action!]
    -Step3:
    {
      Name: "",
      Do: {
        "echo \"{{.reg_hello}}\"",
        "echo \"{{.hellomsg}}\""
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
      "last_result": (*utils.ExecResult)({
        Cmd: "echo hanks",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "hellomsg": "hanks"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo hanks",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "hellomsg": "hanks"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo hanks",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "hellomsg": "hanks"
    })
    
    cmd( 1):
    echo "{{.reg_hello}}"
    
    cmd=>:
    echo "<no value>"<=
    <no value>
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=17) "echo \"<no value>\"",
     Code: (int) 0,
     Output: (string) (len=10) "<no value>",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "{{.hellomsg}}"
    
    cmd=>:
    echo "hanks"<=
    hanks
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"hanks\"",
     Code: (int) 0,
     Output: (string) (len=5) "hanks",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step4: [: the reg_tom's value is a object, but since reg_tom is only a local, it
    will probably not very useful
     ]
    {
      Name: "",
      Do: {
        {
          "name": "reg",
          "cmd": {
            "name": "global_tom",
            "value": "{{.local_tom}}"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "person": {
          "name": "tom",
          "age": 18
        }
      },
      Dvars: {
        {
          Name: "local_tom",
          Value: "my name is tom\n{{.person |reg \"tom\" }}",
          Desc: "",
          Expand: 0,
          Flags: {
            "vvv"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
      Desc: "the reg_tom's value is a object, but since reg_tom is only a local, it\nwill probably not very useful\n",
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
      "hellomsg": "hanks",
      "person": {
        "name": "tom",
        "age": 18
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hanks\"",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      })
    })
    
    dvar> local_tom:
    "my name is tom\nage: 18\nname: tom\n"
    
    -
    my name is tom
    age: 18
    name: tom
    
    [local] dvar expanded result:
    {
      "tom": {
        "name": "tom",
        "age": 18
      },
      "local_tom": "my name is tom\nage: 18\nname: tom\n"
    }
    
    
    scope[local] merged: {
      "tom": {
        "name": "tom",
        "age": 18
      },
      "local_tom": "my name is tom\nage: 18\nname: tom\n",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hanks\"",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "hellomsg": "hanks",
      "person": {
        "age": 18,
        "name": "tom"
      }
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hanks\"",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "hellomsg": "hanks",
      "person": {
        "name": "tom",
        "age": 18
      },
      "tom": {
        "name": "tom",
        "age": 18
      },
      "local_tom": "my name is tom\nage: 18\nname: tom\n"
    })
    
    map[name:global_tom value:{{.local_tom}}]
    ~SubStep1: [reg:  ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hanks\"",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "hellomsg": "hanks",
      "tom": {
        "name": "tom",
        "age": 18
      },
      "global_tom": "my name is tom\nage: 18\nname: tom\n"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hanks\"",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "hellomsg": "hanks",
      "person": {
        "name": "tom",
        "age": 18
      },
      "tom": {
        "name": "tom",
        "age": 18
      },
      "local_tom": "my name is tom\nage: 18\nname: tom\n",
      "global_tom": "my name is tom\nage: 18\nname: tom\n"
    })
    
    -Step5: [: debug the results ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "desc": "this local_tom should be <no value> as it is in scope of last step",
          "cmd": "{{.local_tom}}"
        },
        {
          "name": "print",
          "desc": "get the object from register global space",
          "cmd": "{{.tom}}"
        },
        {
          "name": "printObj",
          "desc": "dynamically reference to global_tom object registered",
          "cmd": "{{.objname}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "objname": "global_tom"
      },
      Dvars: <nil>,
      Desc: "debug the results",
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
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hanks\"",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "hellomsg": "hanks",
      "tom": {
        "name": "tom",
        "age": 18
      },
      "global_tom": "my name is tom\nage: 18\nname: tom\n",
      "objname": "global_tom"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hanks\"",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "hellomsg": "hanks",
      "tom": {
        "name": "tom",
        "age": 18
      },
      "global_tom": "my name is tom\nage: 18\nname: tom\n",
      "objname": "global_tom"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": {
        "name": "tom",
        "age": 18
      },
      "global_tom": "my name is tom\nage: 18\nname: tom\n",
      "objname": "global_tom",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hanks\"",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "hellomsg": "hanks"
    })
    
    {{.local_tom}}
    ~SubStep1: [print: this local_tom should be <no value> as it is in scope of last step ]
    None
    {{.tom}}
    ~SubStep2: [print: get the object from register global space ]
    map[age:18 name:tom]
    {{.objname}}
    ~SubStep3: [printObj: dynamically reference to global_tom object registered ]
    (string) (len=12) "{{.objname}}"
    
    object:
     global_tom: "my name is tom\nage: 18\nname: tom\n"
    
    
```

##### Logs with different verbose level
* [c0076 log - verbose level v](../../logs/c0076_v)
* [c0076 log - verbose level vv](../../logs/c0076_vv)
* [c0076 log - verbose level vvv](../../logs/c0076_vvv)
* [c0076 log - verbose level vvvv](../../logs/c0076_vvvv)
* [c0076 log - verbose level vvvvv](../../logs/c0076_vvvvv)

##### References
* [Related Chapter](../../vars/c0076)
