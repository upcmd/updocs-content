---
title: "c0157_vvvvv"
date: 2020-07-20T02:01:57+77:00
draft: false
weight: 11574

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0157
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0157
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001770c0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [self] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "person": {
        "name": "tom"
      }
    }
    
    (core.Cache) (len=1) {
     (string) (len=6) "person": (map[string]interface {}) (len=1) {
      (string) (len=4) "name": (string) (len=3) "tom"
     }
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "person": {
        "name": "tom"
      }
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: the commented if statement will cause a template rendering issue since person.school is not able to be determined
     ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "hello: {{.person.name}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "the commented if statement will cause a template rendering issue since person.school is not able to be determined\n",
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
      "person": {
        "name": "tom"
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "person": {
        "name": "tom"
      }
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "person": {
        "name": "tom"
      }
    })
    
    hello: {{.person.name}}
    ~SubStep1: [print:  ]
    hello: tom
    -Step2: [: correct way is to try to get the school value and save it to a dvar
    then it is deterministic of the school value
     ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "hello: {{.person.name}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "school",
          Value: "{{.person.school}}",
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
      Desc: "correct way is to try to get the school value and save it to a dvar\nthen it is deterministic of the school value\n",
      Reg: "",
      Flags: <nil>,
      If: "{{eq .school \"None\"}}",
      Else: {
        {
          "func": "cmd",
          "desc": "now it is safe to access school from person object",
          "do": {
            {
              "name": "print",
              "cmd": "hello: {{.person.name}} from {{.person.school}}"
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
      "person": {
        "name": "tom"
      }
    })
    
    [local] dvar expanded result:
    {
      "school": "None"
    }
    
    
    scope[local] merged: {
      "person": {
        "name": "tom"
      },
      "school": "None"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "person": {
        "name": "tom"
      },
      "school": "None"
    })
    
    hello: {{.person.name}}
    ~SubStep1: [print:  ]
    hello: tom
    
```

##### Logs with different verbose level
* [c0157 log - verbose level v](../../logs/c0157_v)
* [c0157 log - verbose level vv](../../logs/c0157_vv)
* [c0157 log - verbose level vvv](../../logs/c0157_vvv)
* [c0157 log - verbose level vvvv](../../logs/c0157_vvvv)
* [c0157 log - verbose level vvvvv](../../logs/c0157_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0157)
