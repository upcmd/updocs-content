---
title: "f0172_vvvvv"
date: 2020-08-09T01:36:30+88:00
draft: false
weight: 11724

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> f0172
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
    loading [Task]:  ./tests/functests/f0172
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001e70c0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
    }
    
    (core.Cache) {
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: step 1 ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "step 1"
        },
        {
          "name": "panic"
        },
        {
          "name": "print",
          "cmd": "extra step ......... it will never reach here"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "step 1",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: "close_file",
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
    })
    
    step 1
    ~SubStep1: [print:  ]
    step 1
    ~SubStep2: [panic:  ]
     WARN: [manual panic] - [manual trigger a panic cmd]
    Step Finally:
    (*utils.ExecResult)(<nil>)
    
    <nil>
    
    Recovered from: manual trigger a panic cmd
    finally caller vars to task (close_file)::
    (*core.Cache)({
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>)
    })
    
      located task-> 2 [close_file]: 
    =Task2: [task ==> close_file:  ]
    Executing task stack layer: 2
    
    --Step1: [close_file: ensure the opened file is closed
     ]
    {
      Name: "close_file",
      Do: {
        "echo \"close the file .....\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "ensure the opened file is closed\n",
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
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>),
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>),
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>)
    })
    
    cmd( 1):
    echo "close the file ....."
    
    cmd=>:
    echo "close the file ....."<=
    close the file .....
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=27) "echo \"close the file .....\"",
     Code: (int) 0,
     Output: (string) (len=20) "close the file .....",
     ErrMsg: (string) ""
    }
    
    . ok
     WARN: [No rescued in step level] - [please assess the panic problem and cause, fix it before re-run the task]
    Recovered from: manual trigger a panic cmd
     WARN: [No rescued in task level] - [please assess the panic problem and cause, fix it before re-run the task]
    task finally -> manual trigger a panic cmd
    -----trace for reference-----
    
```

##### Logs with different verbose level
* [f0172 log - verbose level v](../../logs/f0172_v)
* [f0172 log - verbose level vv](../../logs/f0172_vv)
* [f0172 log - verbose level vvv](../../logs/f0172_vvv)
* [f0172 log - verbose level vvvv](../../logs/f0172_vvvv)
* [f0172 log - verbose level vvvvv](../../logs/f0172_vvvvv)

##### References
* [Related Chapter](../../flow-controll/f0172)
