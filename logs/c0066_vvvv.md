---
title: "c0066_vvvv"
date: 2020-06-27T03:09:23+66:00
draft: false
weight: 10663

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0066
                 Verbose -> vvvv
              ModuleName -> cocky_kirch5
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0066
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [cocky_kirch5] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"hello 1\""
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
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      }
    })
    
    cocky_kirch5: overall final exec vars:
    
    (*core.Cache)({
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    })
    
    cmd( 1):
    echo "hello 1"
    
     \_ echo "hello 1"
    hello 1
     .. ok
    . ok
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "desc": "demo of print command",
          "cmd": "hello, {{.student.school}}"
        },
        {
          "desc": "demo of reg command",
          "cmd": {
            "name": "greet",
            "value": "from local dvars, {{.school}}. registered to global runtime"
          },
          "name": "reg"
        },
        {
          "name": "print",
          "desc": "show above reg var greet and it is available immediately in current func\nunlike the reg in template, it is available in the next step func execution\n",
          "cmd": "hello, {{.greet}}"
        },
        {
          "name": "reg",
          "desc": "demo greetlocal is registered to local var only\nit is accessible in current func, but not next one\n",
          "cmd": {
            "value": "hello, {{.student.school}}. registered to local func only",
            "name": "greetlocal"
          },
          "flags": {
            "localonly"
          }
        },
        {
          "name": "print",
          "desc": "this show display a correct rendered value\n",
          "cmd": "hello, {{.greetlocal}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "school",
          Value: "{{.student.school}}",
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
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      })
    })
    
    cocky_kirch5: overall final exec vars:
    
    (*core.Cache)({
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      }),
      "school": "Sydney Grammar"
    })
    
    ~SubStep1: [print: demo of print command ]
    hello, Sydney Grammar
    ~SubStep2: [reg: demo of reg command ]
    ~SubStep3: [print: show above reg var greet and it is available immediately in current func
    unlike the reg in template, it is available in the next step func execution
     ]
    hello, from local dvars, Sydney Grammar. registered to global runtime
    ~SubStep4: [reg: demo greetlocal is registered to local var only
    it is accessible in current func, but not next one
     ]
    ~SubStep5: [print: this show display a correct rendered value
     ]
    hello, hello, Sydney Grammar. registered to local func only
    -Step3: [: the greetlocal will not be availe in this func call ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "desc": "this will show the registered global runtime var\n",
          "cmd": "hello, {{.greetlocal}}"
        },
        {
          "name": "print",
          "desc": "this will show <no value> for greetlocal, as it is not registered to global\n",
          "cmd": "hello, {{.greet}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "the greetlocal will not be availe in this func call",
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
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      }),
      "greet": "from local dvars, Sydney Grammar. registered to global runtime"
    })
    
    cocky_kirch5: overall final exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      }),
      "greet": "from local dvars, Sydney Grammar. registered to global runtime"
    })
    
    ~SubStep1: [print: this will show the registered global runtime var
     ]
    hello, <no value>
    ~SubStep2: [print: this will show <no value> for greetlocal, as it is not registered to global
     ]
    hello, from local dvars, Sydney Grammar. registered to global runtime
    -Step4:
    {
      Name: "",
      Do: {
        {
          "name": "dereg",
          "desc": "demo of dereg command",
          "cmd": "greet"
        }
      },
      Dox: <nil>,
      Func: "cmd",
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
      "greet": "from local dvars, Sydney Grammar. registered to global runtime",
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      })
    })
    
    cocky_kirch5: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      }),
      "greet": "from local dvars, Sydney Grammar. registered to global runtime",
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    })
    
    ~SubStep1: [dereg: demo of dereg command ]
    deregister var: greet
    -Step5: [: you will see that greet var is removed from global var map
    you will see <no value> here
     ]
    {
      Name: "",
      Do: {
        "echo \"hello {{.greet}}\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "you will see that greet var is removed from global var map\nyou will see <no value> here\n",
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
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      })
    })
    
    cocky_kirch5: overall final exec vars:
    
    (*core.Cache)({
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "hello {{.greet}}"
    
     \_ echo "hello <no value>"
    hello <no value>
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0066 log - verbose level v](../../logs/c0066_v)
* [c0066 log - verbose level vv](../../logs/c0066_vv)
* [c0066 log - verbose level vvv](../../logs/c0066_vvv)
* [c0066 log - verbose level vvvv](../../logs/c0066_vvvv)
* [c0066 log - verbose level vvvvv](../../logs/c0066_vvvvv)

##### References
* [Related Chapter](../../cmd-func/c0066)
