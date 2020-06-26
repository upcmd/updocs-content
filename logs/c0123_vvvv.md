---
title: "c0123_vvvv"
date: 2020-06-27T03:09:31+66:00
draft: false
weight: 11233

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
                 Verbose -> vvvv
              ModuleName -> elated_morse1
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0123
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [elated_morse1] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "student": {
        "name": "tom",
        "sex": "male"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "student": {
        "name": "tom",
        "sex": "male"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n"
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
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "student": {
        "name": "tom",
        "sex": "male"
      }
    })
    
    elated_morse1: overall final exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "tom",
        "sex": "male"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n"
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
        "sex": "male",
        "name": "tom"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n"
    })
    
    elated_morse1: overall final exec vars:
    
    (*core.Cache)({
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "student": {
        "name": "tom",
        "sex": "male"
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
        "sex": "male",
        "name": "tom"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n"
    })
    
    elated_morse1: overall final exec vars:
    
    (*core.Cache)({
      "student": {
        "sex": "male",
        "name": "tom"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n"
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
      "student": {
        "name": "tom",
        "sex": "male"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n"
    })
    
    elated_morse1: overall final exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "tom",
        "sex": "male"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n"
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
      "student": {
        "name": "tom",
        "sex": "male"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n"
    })
    
    elated_morse1: overall final exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "tom",
        "sex": "male"
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
