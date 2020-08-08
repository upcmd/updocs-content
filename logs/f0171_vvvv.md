---
title: "f0171_vvvv"
date: 2020-08-09T01:36:29+88:00
draft: false
weight: 11713

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
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/f0171
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
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
    current exec runtime vars:
    (*core.Cache)({
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo "open a file ....."
    
    cmd=>:
    echo "open a file ....."<=
    open a file .....
     .. ok
    cmd( 2):
    echo "reading the file" |grep "cause an exception"
    
    cmd=>:
    echo "reading the file" |grep "cause an exception"<=
          exec wait -> exit status 1
          exit status 1
     .. failed(suppressed if it is not the last step)
    Step Finally:
    (*utils.ExecResult)({
      Cmd: "echo \"reading the file\" |grep \"cause an exception\"",
      Code: 1,
      Output: "",
      ErrMsg: "exit status 1"
    })
    
    <nil>
    
      located task-> 2 [close_file]: 
    =Task2: [task ==> close_file:  ]
    Executing task stack layer: 2
    
    --Step1: [close_file: ensure the opened file is closed
     ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_shell_exec_result": (*utils.ExecResult)({
        Cmd: "echo \"reading the file\" |grep \"cause an exception\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "up_runtime_task_layer_number": 1
    })
    
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
    echo "close the file ....."<=
    close the file .....
     .. ok
    . ok
     WARN: [No rescued in task level] - [please assess the panic problem and cause, fix it before re-run the task]
    task finally ->   ERROR: Failed And Not Ignored! [You may want to continue and ignore the error]
    
    
```

##### Logs with different verbose level
* [f0171 log - verbose level v](../../logs/f0171_v)
* [f0171 log - verbose level vv](../../logs/f0171_vv)
* [f0171 log - verbose level vvv](../../logs/f0171_vvv)
* [f0171 log - verbose level vvvv](../../logs/f0171_vvvv)
* [f0171 log - verbose level vvvvv](../../logs/f0171_vvvvv)

##### References
* [Related Chapter](../../flow-controll/f0171)
