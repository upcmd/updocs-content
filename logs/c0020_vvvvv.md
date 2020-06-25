---
title: "c0020_vvvvv"
date: 2020-06-25T01:55:39+66:00
draft: false
weight: 10204

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
                 Verbose -> vvvvv
              ModuleName -> nostalgic_hypatia2
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0020
    -------full vars in scopes------
    (*impl.Scopes)(0xc00000e920)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [nostalgic_hypatia2] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "school": "sydney grammar"
    }
    
    (core.Cache) (len=1) {
     (string) (len=6) "school": (string) (len=14) "sydney grammar"
    }
    
    [runtime global] dvar expanded result:
    {
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
        "gender": "male",
        "studentname": "Tom",
        "school": "sydney grammar"
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
      "school": "sydney grammar",
      "gender": "male",
      "studentname": "Tom"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "school": "sydney grammar",
      "gender": "male",
      "studentname": "Tom"
    }
    
    
    nostalgic_hypatia2: overall final exec vars:
    
    (*core.Cache)({
      "school": "sydney grammar",
      "gender": "male",
      "studentname": "Tom"
    })
    
    caller's vars to task (function)::
    (*core.Cache)({
      "school": "sydney grammar",
      "gender": "male",
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
      "school": "sydney grammar",
      "gender": "male",
      "studentname": "Tom",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "school": "sydney grammar",
      "gender": "male",
      "studentname": "Tom",
      "up_runtime_task_layer_number": 1
    }
    
    
    nostalgic_hypatia2: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "school": "sydney grammar",
      "gender": "male",
      "studentname": "Tom"
    })
    
    cmd( 1):
    echo "studentname -> {{.studentname}} | gender -> {{.gender}}"
    
     \_ echo "studentname -> Tom | gender -> male"
    studentname -> Tom | gender -> male
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=35) "studentname -> Tom | gender -> male",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "school -> {{.school}}"
    
     \_ echo "school -> sydney grammar"
    school -> sydney grammar
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=24) "school -> sydney grammar",
     ErrMsg: (string) ""
    }
    
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
