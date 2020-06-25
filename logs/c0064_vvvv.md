---
title: "c0064_vvvv"
date: 2020-06-25T01:55:47+66:00
draft: false
weight: 10643

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0064
                 Verbose -> vvvv
              ModuleName -> focused_lumiere2
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0064
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [focused_lumiere2] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
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
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    })
    
    focused_lumiere2: overall final exec vars:
    
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
          "desc": "print some info",
          "cmd": "hello, this is print commmand"
        },
        {
          "name": "print",
          "cmd": "hello, {{.student.school}}"
        },
        {
          "name": "print",
          "cmd": "hello, {{.student.school}}\nhello, {{.student.school}}\n"
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
    
    focused_lumiere2: overall final exec vars:
    
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
      })
    })
    
    ~SubStep1: [print: print some info ]
    hello, this is print commmand
    ~SubStep2: [print:  ]
    hello, Sydney Grammar
    ~SubStep3: [print:  ]
    hello, Sydney Grammar
    hello, Sydney Grammar
    
    
```

##### Logs with different verbose level
* [c0064 log - verbose level v](../../logs/c0064_v)
* [c0064 log - verbose level vv](../../logs/c0064_vv)
* [c0064 log - verbose level vvv](../../logs/c0064_vvv)
* [c0064 log - verbose level vvvv](../../logs/c0064_vvvv)
* [c0064 log - verbose level vvvvv](../../logs/c0064_vvvvv)

##### References
* [Related Chapter](../../cmd-func/c0064)
