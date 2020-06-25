---
title: "c0122_vvvv"
date: 2020-06-25T01:56:01+66:00
draft: false
weight: 11223

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
                 Verbose -> vvvv
              ModuleName -> sad_engelbart2
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0122
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [sad_engelbart2] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "student": {
        "name": "tom",
        "sex": "male"
      }
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "student": {
        "name": "tom",
        "sex": "male"
      }
    })
    
    sad_engelbart2: overall final exec vars:
    
    (*core.Cache)({
      "student": {
        "sex": "male",
        "name": "tom"
      }
    })
    
    ~SubStep1: [print:  ]
    tom
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
      "student": {
        "name": "tom",
        "sex": "male"
      }
    })
    
    sad_engelbart2: overall final exec vars:
    
    (*core.Cache)({
      "student": {
        "sex": "male",
        "name": "tom"
      }
    })
    
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
      "student": {
        "name": "tom",
        "sex": "male"
      }
    })
    
    sad_engelbart2: overall final exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "tom",
        "sex": "male"
      }
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
