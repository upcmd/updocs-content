---
title: "c0066_vvvvv"
date: 2020-06-27T03:09:23+66:00
draft: false
weight: 10664

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
                 Verbose -> vvvvv
              ModuleName -> pensive_blackwell3
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0066
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ed320)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [pensive_blackwell3] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
    }
    
    (core.Cache) (len=1) {
     (string) (len=7) "student": (map[string]interface {}) (len=3) {
      (string) (len=4) "name": (string) (len=3) "Tom",
      (string) (len=6) "gender": (string) (len=4) "Male",
      (string) (len=6) "school": (string) (len=14) "Sydney Grammar"
     }
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
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
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      }
    }
    
    
    pensive_blackwell3: overall final exec vars:
    
    (*core.Cache)({
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      }
    })
    
    cmd( 1):
    echo "hello 1"
    
     \_ echo "hello 1"
    hello 1
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=7) "hello 1",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2:
    {
      Name: "",
      Do: {
        {
          "desc": "demo of print command",
          "cmd": "hello, {{.student.school}}",
          "name": "print"
        },
        {
          "name": "reg",
          "desc": "demo of reg command",
          "cmd": {
            "name": "greet",
            "value": "from local dvars, {{.school}}. registered to global runtime"
          }
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
            "name": "greetlocal",
            "value": "hello, {{.student.school}}. registered to local func only"
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
    
    [local] dvar expanded result:
    {
      "school": "Sydney Grammar"
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      }),
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "school": "Sydney Grammar"
    }
    
    
    pensive_blackwell3: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      }),
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "school": "Sydney Grammar"
    })
    
    hello, {{.student.school}}
    ~SubStep1: [print: demo of print command ]
    hello, Sydney Grammar
    map[name:greet value:from local dvars, {{.school}}. registered to global runtime]
    ~SubStep2: [reg: demo of reg command ]
    after reg the var - contextual global:
    
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
    
    after reg the var - local:
    
    (*core.Cache)({
      "school": "Sydney Grammar",
      "greet": "from local dvars, Sydney Grammar. registered to global runtime",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      }),
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    })
    
    hello, {{.greet}}
    ~SubStep3: [print: show above reg var greet and it is available immediately in current func
    unlike the reg in template, it is available in the next step func execution
     ]
    hello, from local dvars, Sydney Grammar. registered to global runtime
    map[name:greetlocal value:hello, {{.student.school}}. registered to local func only]
    ~SubStep4: [reg: demo greetlocal is registered to local var only
    it is accessible in current func, but not next one
     ]
    after reg the var - contextual global:
    
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
    
    after reg the var - local:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      }),
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "school": "Sydney Grammar",
      "greet": "from local dvars, Sydney Grammar. registered to global runtime",
      "greetlocal": "hello, Sydney Grammar. registered to local func only"
    })
    
    hello, {{.greetlocal}}
    ~SubStep5: [print: this show display a correct rendered value
     ]
    hello, hello, Sydney Grammar. registered to local func only
    -Step3: [: the greetlocal will not be availe in this func call ]
    {
      Name: "",
      Do: {
        {
          "desc": "this will show the registered global runtime var\n",
          "cmd": "hello, {{.greetlocal}}",
          "name": "print"
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
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
    }
    
    
    pensive_blackwell3: overall final exec vars:
    
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
    
    hello, {{.greetlocal}}
    ~SubStep1: [print: this will show the registered global runtime var
     ]
    hello, <no value>
    hello, {{.greet}}
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "greet": "from local dvars, Sydney Grammar. registered to global runtime",
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      })
    }
    
    
    pensive_blackwell3: overall final exec vars:
    
    (*core.Cache)({
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      }),
      "greet": "from local dvars, Sydney Grammar. registered to global runtime"
    })
    
    greet
    ~SubStep1: [dereg: demo of dereg command ]
    deregister var: greet
    after reg the var - contextual global:
    
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
    
    after reg the var - local:
    
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
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
    }
    
    
    pensive_blackwell3: overall final exec vars:
    
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
    
    cmd( 1):
    echo "hello {{.greet}}"
    
     \_ echo "hello <no value>"
    hello <no value>
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=16) "hello <no value>",
     ErrMsg: (string) ""
    }
    
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
