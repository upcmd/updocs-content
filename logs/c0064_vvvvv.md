---
title: "c0064_vvvvv"
date: 2020-09-18T01:27:30+99:00
draft: false
weight: 10644

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
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0064
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc000176fa0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
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
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "up_runtime_task_layer_number": 0
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
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "hello 1"
    
    cmd=>:
    echo "hello 1"
    -
    hello 1
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=14) "echo \"hello 1\"",
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
          "cmd": "hello, this is print commmand",
          "name": "print",
          "desc": "print some info"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello 1\"",
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
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
        Cmd: "echo \"hello 1\"",
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello 1\"",
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    hello, this is print commmand
    ~SubStep1: [print: print some info ]
    hello, this is print commmand
    hello, {{.student.school}}
    ~SubStep2: [print:  ]
    hello, Sydney Grammar
    hello, {{.student.school}}
    hello, {{.student.school}}
    
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
