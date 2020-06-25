---
title: "c0123_vvvvv"
date: 2020-06-25T01:56:02+66:00
draft: false
weight: 11234

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0123
                 Verbose -> vvvvv
              ModuleName -> grave_hawking2
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0123
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001f7220)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [grave_hawking2] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "student": {
        "sex": "male",
        "name": "tom"
      }
    }
    
    (core.Cache) (len=2) {
     (string) (len=6) "ymldoc": (string) (len=33) "student:\n  name: tom\n  sex: male\n",
     (string) (len=7) "student": (map[string]interface {}) (len=2) {
      (string) (len=3) "sex": (string) (len=4) "male",
      (string) (len=4) "name": (string) (len=3) "tom"
     }
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "student": {
        "sex": "male",
        "name": "tom"
      }
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task: main entry ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.student.name}}"
        },
        {
          "name": "print",
          "cmd": "{{.student.age}}"
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
      "student": {
        "sex": "male",
        "name": "tom"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "student": {
        "sex": "male",
        "name": "tom"
      }
    }
    
    
    grave_hawking2: overall final exec vars:
    
    (*core.Cache)({
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "student": {
        "sex": "male",
        "name": "tom"
      }
    })
    
    {{.student.name}}
    ~SubStep1: [print:  ]
    tom
    {{.student.age}}
    ~SubStep2: [print:  ]
    <no value>
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "hello tom"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "{{eq .student.name \"tom\"}}",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "student": {
        "sex": "male",
        "name": "tom"
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "student": {
        "sex": "male",
        "name": "tom"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n"
    }
    
    
    grave_hawking2: overall final exec vars:
    
    (*core.Cache)({
      "student": {
        "sex": "male",
        "name": "tom"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n"
    })
    
    hello tom
    ~SubStep1: [print:  ]
    hello tom
    -Step3: [: add support if the element does not exist, then if condition should be false by default ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "you will not see this message"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "add support if the element does not exist, then if condition should be false by default",
      Reg: "",
      Flags: <nil>,
      If: "{{.student.age}}",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "student": {
        "sex": "male",
        "name": "tom"
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "student": {
        "sex": "male",
        "name": "tom"
      }
    }
    
    
    grave_hawking2: overall final exec vars:
    
    (*core.Cache)({
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "student": {
        "sex": "male",
        "name": "tom"
      }
    })
    
    condition failed, skip executing step 
    
    -Step4: [query:  ]
    {
      Name: "query",
      Do: <nil>,
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: {
        "ymlonly"
      },
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "student": {
        "sex": "male",
        "name": "tom"
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "student": {
        "sex": "male",
        "name": "tom"
      }
    }
    
    
    grave_hawking2: overall final exec vars:
    
    (*core.Cache)({
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "student": {
        "sex": "male",
        "name": "tom"
      }
    })
    
     WARN: [cmd] - [Not implemented or void for no action!]
    -Step5:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "you will not see this message"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "{{.studentage}}",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "student": {
        "sex": "male",
        "name": "tom"
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "student": {
        "sex": "male",
        "name": "tom"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n"
    }
    
    
    grave_hawking2: overall final exec vars:
    
    (*core.Cache)({
      "student": {
        "sex": "male",
        "name": "tom"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n"
    })
    
    condition failed, skip executing step 
    
    
```

##### Logs with different verbose level
* [c0123 log - verbose level v](../../logs/c0123_v)
* [c0123 log - verbose level vv](../../logs/c0123_vv)
* [c0123 log - verbose level vvv](../../logs/c0123_vvv)
* [c0123 log - verbose level vvvv](../../logs/c0123_vvvv)
* [c0123 log - verbose level vvvvv](../../logs/c0123_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0123)
