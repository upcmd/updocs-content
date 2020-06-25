---
title: "c0076_vvvvv"
date: 2020-06-25T01:55:50+66:00
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
              ModuleName -> nostalgic_archimedes9
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0076
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001f52a0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [nostalgic_archimedes9] instance id: [dev]
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
    }
    
    
    nostalgic_archimedes9: overall final exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo hanks
    
     \_ echo hanks
    hanks
     .. ok
    (utils.ExecResult) {
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
      "reg_hello": "\n"
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "reg_hello": "\n"
    }
    
    
    nostalgic_archimedes9: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "reg_hello": "\n"
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
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
      "hellomsg": "hanks",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      })
    }
    
    
    nostalgic_archimedes9: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "hellomsg": "hanks"
    })
    
    cmd( 1):
    echo "{{.reg_hello}}"
    
     \_ echo "<no value>"
    <no value>
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=10) "<no value>",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "{{.hellomsg}}"
    
     \_ echo "hanks"
    hanks
     .. ok
    (utils.ExecResult) {
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
          "age": 18,
          "name": "tom"
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "person": {
        "name": "tom",
        "age": 18
      },
      "hellomsg": "hanks"
    })
    
    dvar> local_tom:
    "my name is tom\n"
    
    [local] dvar expanded result:
    {
      "local_tom": "my name is tom\n"
    }
    
    
    scope[local] merged: {
      "person": {
        "name": "tom",
        "age": 18
      },
      "hellomsg": "hanks",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "local_tom": "my name is tom\n"
    }
    
    
    nostalgic_archimedes9: overall final exec vars:
    
    (*core.Cache)({
      "hellomsg": "hanks",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "local_tom": "my name is tom\n",
      "person": {
        "name": "tom",
        "age": 18
      }
    })
    
    map[name:global_tom value:{{.local_tom}}]
    ~SubStep1: [reg:  ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "hellomsg": "hanks",
      "tom": {
        "name": "tom",
        "age": 18
      },
      "global_tom": "my name is tom\n"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "person": {
        "name": "tom",
        "age": 18
      },
      "hellomsg": "hanks",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "local_tom": "my name is tom\n",
      "global_tom": "my name is tom\n"
    })
    
    -Step5: [: debug the results ]
    {
      Name: "",
      Do: {
        {
          "desc": "this local_tom should be <no value> as it is in scope of last step",
          "cmd": "{{.local_tom}}",
          "name": "print"
        },
        {
          "name": "print",
          "desc": "get the object from register global space",
          "cmd": "{{.tom}}"
        },
        {
          "desc": "dynamically reference to global_tom object registered",
          "cmd": "{{.objname}}",
          "name": "printobj"
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "hellomsg": "hanks",
      "tom": {
        "age": 18,
        "name": "tom"
      },
      "global_tom": "my name is tom\n",
      "objname": "global_tom"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "global_tom": "my name is tom\n",
      "objname": "global_tom",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "hellomsg": "hanks",
      "tom": {
        "age": 18,
        "name": "tom"
      }
    }
    
    
    nostalgic_archimedes9: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "hellomsg": "hanks",
      "tom": {
        "name": "tom",
        "age": 18
      },
      "global_tom": "my name is tom\n",
      "objname": "global_tom"
    })
    
    {{.local_tom}}
    ~SubStep1: [print: this local_tom should be <no value> as it is in scope of last step ]
    <no value>
    {{.tom}}
    ~SubStep2: [print: get the object from register global space ]
    map[age:18 name:tom]
    {{.objname}}
    ~SubStep3: [printobj: dynamically reference to global_tom object registered ]
    (string) (len=12) "{{.objname}}"
    
    object:
     global_tom: "my name is tom\n"
    
    
```

##### Logs with different verbose level
* [c0076 log - verbose level v](../../logs/c0076_v)
* [c0076 log - verbose level vv](../../logs/c0076_vv)
* [c0076 log - verbose level vvv](../../logs/c0076_vvv)
* [c0076 log - verbose level vvvv](../../logs/c0076_vvvv)
* [c0076 log - verbose level vvvvv](../../logs/c0076_vvvvv)

##### References
* [Related Chapter](../../vars/c0076)
