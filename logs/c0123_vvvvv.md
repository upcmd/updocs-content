---
title: "c0123_vvvvv"
date: 2020-09-18T00:51:43+99:00
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
    loading [Task]:  ./tests/functests/c0123
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001e72a0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "student": {
        "name": "tom",
        "sex": "male"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n"
    }
    
    (core.Cache) (len=2) {
     (string) (len=7) "student": (map[string]interface {}) (len=2) {
      (string) (len=4) "name": (string) (len=3) "tom",
      (string) (len=3) "sex": (string) (len=4) "male"
     },
     (string) (len=6) "ymldoc": (string) (len=33) "student:\n  name: tom\n  sex: male\n"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
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
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "student": {
        "name": "tom",
        "sex": "male"
      },
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "student": {
        "name": "tom",
        "sex": "male"
      },
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "student": {
        "name": "tom",
        "sex": "male"
      },
      "up_runtime_task_layer_number": 0
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
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "student": {
        "name": "tom",
        "sex": "male"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "student": {
        "name": "tom",
        "sex": "male"
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
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "student": {
        "sex": "male",
        "name": "tom"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "tom",
        "sex": "male"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "up_runtime_task_layer_number": 0
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
        "ymlOnly"
      },
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
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "student": {
        "name": "tom",
        "sex": "male"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "tom",
        "sex": "male"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "up_runtime_task_layer_number": 0
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
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "up_runtime_task_layer_number": 0,
      "student": {
        "sex": "male",
        "name": "tom"
      }
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "tom",
        "sex": "male"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "up_runtime_task_layer_number": 0
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
