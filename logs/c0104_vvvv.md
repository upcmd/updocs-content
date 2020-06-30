---
title: "c0104_vvvv"
date: 2020-07-01T15:34:35+77:00
draft: false
weight: 11043

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0104
                 Verbose -> vvvv
              ModuleName -> sick_curie2
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0104
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [sick_curie2] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "extra_task_name": "post_task"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "extra_task_name": "post_task"
    }
    
      located task-> 4 [task]: 
    Task4: [task ==> task: this is the task and expect the final message (hello I love this world) ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \" I love this \""
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
      "extra_task_name": "post_task"
    })
    
    sick_curie2: overall final exec vars:
    
    (*core.Cache)({
      "extra_task_name": "post_task"
    })
    
    cmd( 1):
    echo " I love this "
    
     \_ echo " I love this "
    I love this
     .. ok
    . ok
    -Step2: [: use a dynamic var to refer to a task name ]
    {
      Name: "",
      Do: {
        "{{.extra_task_name}}",
        "2ndtask"
      },
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "use a dynamic var to refer to a task name",
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
      "extra_task_name": "post_task",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "I love this",
        ErrMsg: ""
      })
    })
    
    sick_curie2: overall final exec vars:
    
    (*core.Cache)({
      "extra_task_name": "post_task",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "I love this",
        ErrMsg: ""
      })
    })
    
      located task-> 2 [post_task]: 
    =Task2: [task ==> post_task: this is post-task ]
    Executing task stack layer: 2
    
    --Step1: [: do step1 in shell func ]
    {
      Name: "",
      Do: {
        "echo \"world\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "do step1 in shell func",
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
      "extra_task_name": "post_task",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "I love this",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    sick_curie2: overall final exec vars:
    
    (*core.Cache)({
      "extra_task_name": "post_task",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "I love this",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    echo "world"
    
     \_ echo "world"
    world
     .. ok
    . ok
      located task-> 3 [2ndtask]: 
    =Task3: [task ==> 2ndtask:  ]
    Executing task stack layer: 2
    
    --Step1: [: to test multiple refs ]
    {
      Name: "",
      Do: {
        "echo \"this is 2nd task\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "to test multiple refs",
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
      "extra_task_name": "post_task",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    sick_curie2: overall final exec vars:
    
    (*core.Cache)({
      "extra_task_name": "post_task",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    echo "this is 2nd task"
    
     \_ echo "this is 2nd task"
    this is 2nd task
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0104 log - verbose level v](../../logs/c0104_v)
* [c0104 log - verbose level vv](../../logs/c0104_vv)
* [c0104 log - verbose level vvv](../../logs/c0104_vvv)
* [c0104 log - verbose level vvvv](../../logs/c0104_vvvv)
* [c0104 log - verbose level vvvvv](../../logs/c0104_vvvvv)

##### References
* [Related Chapter](../../quick-start/c0104)
