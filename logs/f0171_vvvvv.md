---
title: "f0171_vvvvv"
date: 2020-09-18T00:52:03+99:00
draft: false
weight: 11714

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> f0171
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
    loading [Task]:  ./tests/functests/f0171
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc00000c4e0)(<nil>)
    
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
    
    -Step1: [: task fails
     ]
    {
      Name: "",
      Do: {
        "echo \"open a file .....\"",
        "echo \"reading the file\" |grep \"cause an exception\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "task fails\n",
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
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "open a file ....."
    
    cmd=>:
    echo "open a file ....."
    -
    open a file .....
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=24) "echo \"open a file .....\"",
     Code: (int) 0,
     Output: (string) (len=17) "open a file .....",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "reading the file" |grep "cause an exception"
    
    cmd=>:
    echo "reading the file" |grep "cause an exception"
    -
    
    -
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=50) "echo \"reading the file\" |grep \"cause an exception\"",
     Code: (int) 1,
     Output: (string) "",
     ErrMsg: (string) (len=13) "exit status 1"
    }
    
    Step Finally:
    (*utils.ExecResult)({
      Cmd: "echo \"reading the file\" |grep \"cause an exception\"",
      Code: 1,
      Output: "",
      ErrMsg: "exit status 1"
    })
    
    finally caller vars to task (close_file)::
    (*core.Cache)({
      "up_runtime_shell_exec_result": (*utils.ExecResult)({
        Cmd: "echo \"reading the file\" |grep \"cause an exception\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
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
      "up_runtime_task_layer_number": 1,
      "up_runtime_shell_exec_result": (*utils.ExecResult)({
        Cmd: "echo \"reading the file\" |grep \"cause an exception\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_shell_exec_result": (*utils.ExecResult)({
        Cmd: "echo \"reading the file\" |grep \"cause an exception\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_shell_exec_result": (*utils.ExecResult)({
        Cmd: "echo \"reading the file\" |grep \"cause an exception\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    echo "close the file ....."
    
    cmd=>:
    echo "close the file ....."
    -
    close the file .....
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=27) "echo \"close the file .....\"",
     Code: (int) 0,
     Output: (string) (len=20) "close the file .....",
     ErrMsg: (string) ""
    }
    
    . ok
    Recovered from:   ERROR: Failed And Not Ignored! [You may want to continue and ignore the error]
    
     WARN: [Not rescued in task level] - [please assess the panic problem and cause, fix it before re-run the task]
    task finally ->   ERROR: Failed And Not Ignored! [You may want to continue and ignore the error]
    
    -----trace for reference-----
    
```

##### Logs with different verbose level
* [f0171 log - verbose level v](../../logs/f0171_v)
* [f0171 log - verbose level vv](../../logs/f0171_vv)
* [f0171 log - verbose level vvv](../../logs/f0171_vvv)
* [f0171 log - verbose level vvvv](../../logs/f0171_vvvv)
* [f0171 log - verbose level vvvvv](../../logs/f0171_vvvvv)

##### References
* [Related Chapter](../../flow-controll/f0171)
