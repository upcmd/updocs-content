---
title: "c0076_vvvv"
date: 2020-06-25T01:55:50+66:00
draft: false
weight: 10763

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
                 Verbose -> vvvv
              ModuleName -> prickly_babbage8
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0076
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [prickly_babbage8] instance id: [dev]
    merged[ dev ] runtime vars:
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
    
    prickly_babbage8: overall final exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo hanks
    
     \_ echo hanks
    hanks
     .. ok
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
    
    prickly_babbage8: overall final exec vars:
    
    (*core.Cache)({
      "reg_hello": "\n",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      })
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
    
    prickly_babbage8: overall final exec vars:
    
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
    cmd( 2):
    echo "{{.hellomsg}}"
    
     \_ echo "hanks"
    hanks
     .. ok
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
      "person": {
        "age": 18,
        "name": "tom"
      }
    })
    
    dvar> local_tom:
    "my name is tom\n"
    
    prickly_babbage8: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "hellomsg": "hanks",
      "person": {
        "name": "tom",
        "age": 18
      },
      "local_tom": "my name is tom\n"
    })
    
    ~SubStep1: [reg:  ]
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
          "name": "printobj",
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
        "name": "tom",
        "age": 18
      },
      "global_tom": "my name is tom\n",
      "objname": "global_tom"
    })
    
    prickly_babbage8: overall final exec vars:
    
    (*core.Cache)({
      "objname": "global_tom",
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
    
    ~SubStep1: [print: this local_tom should be <no value> as it is in scope of last step ]
    <no value>
    ~SubStep2: [print: get the object from register global space ]
    map[age:18 name:tom]
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
