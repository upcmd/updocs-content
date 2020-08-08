---
title: "c0122_vvvvv"
date: 2020-08-09T01:36:17+88:00
draft: false
weight: 11224

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0122
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
    loading [Task]:  ./tests/functests/c0122
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001c1240)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "student": {
        "sex": "male",
        "name": "tom"
      }
    }
    
    (core.Cache) (len=1) {
     (string) (len=7) "student": (map[string]interface {}) (len=2) {
      (string) (len=4) "name": (string) (len=3) "tom",
      (string) (len=3) "sex": (string) (len=4) "male"
     }
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "student": {
        "name": "tom",
        "sex": "male"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "student": {
        "name": "tom",
        "sex": "male"
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "student": {
        "name": "tom",
        "sex": "male"
      }
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
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
    None
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "student": {
        "name": "tom",
        "sex": "male"
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "student": {
        "name": "tom",
        "sex": "male"
      }
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "tom",
        "sex": "male"
      }
    })
    
    hello tom
    ~SubStep1: [print:  ]
    hello tom
    -Step3: [: add support if the element does not exist, then if condition should be false by default ]
    {
      Name: "",
      Do: {
        {
          "name": "assert",
          "desc": "this cmd will not evaluated as it will not reach here\nthe below evaluate will cause issue, as age does not exist\nalways map to a dvar first\n",
          "cmd": "{{eq .student.age \"None\"}}"
        },
        {
          "name": "print",
          "cmd": "{{.student.age}}"
        },
        {
          "name": "print",
          "cmd": "you will not see this message\n"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "student_age",
          Value: ".student.age",
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
      Desc: "add support if the element does not exist, then if condition should be false by default",
      Reg: "",
      Flags: <nil>,
      If: "{{eq .student_age \"None\"}}",
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
      "student": {
        "sex": "male",
        "name": "tom"
      }
    })
    
    [local] dvar expanded result:
    {
      "student_age": ".student.age"
    }
    
    
    scope[local] merged: {
      "student": {
        "sex": "male",
        "name": "tom"
      },
      "student_age": ".student.age"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "sex": "male",
        "name": "tom"
      },
      "student_age": ".student.age"
    })
    
    condition failed, skip executing step 
    
    
```

##### Logs with different verbose level
* [c0122 log - verbose level v](../../logs/c0122_v)
* [c0122 log - verbose level vv](../../logs/c0122_vv)
* [c0122 log - verbose level vvv](../../logs/c0122_vvv)
* [c0122 log - verbose level vvvv](../../logs/c0122_vvvv)
* [c0122 log - verbose level vvvvv](../../logs/c0122_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0122)
