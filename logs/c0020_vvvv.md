---
title: "c0020_vvvv"
date: 2020-07-01T15:34:23+77:00
draft: false
weight: 10203

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0020
                 Verbose -> vvvv
              ModuleName -> cranky_franklin5
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0020
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [cranky_franklin5] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "school": "sydney grammar"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "school": "sydney grammar"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: call function with different vars ]
    {
      Name: "",
      Do: {
        "function"
      },
      Dox: <nil>,
      Func: "call",
      Vars: {
        "school": "sydney grammar",
        "gender": "male",
        "studentname": "Tom"
      },
      Dvars: <nil>,
      Desc: "call function with different vars",
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
      "gender": "male",
      "school": "sydney grammar",
      "studentname": "Tom"
    })
    
    cranky_franklin5: overall final exec vars:
    
    (*core.Cache)({
      "gender": "male",
      "school": "sydney grammar",
      "studentname": "Tom"
    })
    
      located task-> 2 [function]: 
    =Task2: [task ==> function: as a design pattern, this is a function task
    it's better to not to use any local vars, in this
    way, the vars are passed in from caller call so
    that this function could be used by multiple ref tasks
     ]
    Executing task stack layer: 2
    
    --Step1: [: show school and student info ]
    {
      Name: "",
      Do: {
        "echo \"studentname -> {{.studentname}} | gender -> {{.gender}}\"",
        "echo \"school -> {{.school}}\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "show school and student info",
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
      "up_runtime_task_layer_number": 1,
      "school": "sydney grammar",
      "studentname": "Tom",
      "gender": "male"
    })
    
    cranky_franklin5: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "school": "sydney grammar",
      "studentname": "Tom",
      "gender": "male"
    })
    
    cmd( 1):
    echo "studentname -> {{.studentname}} | gender -> {{.gender}}"
    
     \_ echo "studentname -> Tom | gender -> male"
    studentname -> Tom | gender -> male
     .. ok
    cmd( 2):
    echo "school -> {{.school}}"
    
     \_ echo "school -> sydney grammar"
    school -> sydney grammar
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0020 log - verbose level v](../../logs/c0020_v)
* [c0020 log - verbose level vv](../../logs/c0020_vv)
* [c0020 log - verbose level vvv](../../logs/c0020_vvv)
* [c0020 log - verbose level vvvv](../../logs/c0020_vvvv)
* [c0020 log - verbose level vvvvv](../../logs/c0020_vvvvv)

##### References
* [Related Chapter](../../call-func/c0020)
