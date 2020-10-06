---
title: "c0174_vvvv"
date: 2020-10-06T23:46:24+1010:00
draft: false
weight: 11743

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0174
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0174
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "opening file"
    
    cmd=>:
    echo "opening file"
    -
    opening file
    
    -
     .. ok
    cmd( 2):
    echo "hello"|grep "world"
    
    cmd=>:
    echo "hello"|grep "world"
    -
    
    -
     .. failed(suppressed if it is not the last step)
    Step Finally:
    -Step1: [
    ensure the opened file is closed
    ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_shell_exec_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_shell_exec_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "close the file ....."
    
    cmd=>:
    echo "close the file ....."
    -
    close the file .....
    
    -
     .. ok
    cmd( 2):
    echo """
    exec command: {{.up_runtime_shell_exec_result.Cmd}}
    error code: {{.up_runtime_shell_exec_result.Code}}
    error message: {{.up_runtime_shell_exec_result.ErrMsg}}
    error output: {{.up_runtime_shell_exec_result.Output}}
    """
    
    
    cmd=>:
    echo """
    exec command: echo "hello"|grep "world"
    error code: 1
    error message: exit status 1
    error output: 
    """
    
    -
    
    exec command: echo hello|grep world
    error code: 1
    error message: exit status 1
    error output: 
    
    
    -
     .. ok
    . ok
    -Step2: [
    see if the exec context result: up_runtime_shell_exec_result is still availabe
    conditional do something about the error etc
    ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_shell_exec_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"\"\"\nexec command: echo \"hello\"|grep \"world\"\nerror code: 1\nerror message: exit status 1\nerror output: \n\"\"\"\n",
        Code: 0,
        Output: "exec command: echo hello|grep world\nerror code: 1\nerror message: exit status 1\nerror output:",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_shell_exec_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"\"\"\nexec command: echo \"hello\"|grep \"world\"\nerror code: 1\nerror message: exit status 1\nerror output: \n\"\"\"\n",
        Code: 0,
        Output: "exec command: echo hello|grep world\nerror code: 1\nerror message: exit status 1\nerror output:",
        ErrMsg: ""
      })
    })
    
    ~SubStep1: [print:  ]
    error message: exit status 1
    
     WARN: [ignoreError:] - [Error ignored!!!]
    -Step2: [
    this step will not be reached if the ignoreError flag is not set
    try it yourself to remove the ignoreError flag and see difference
    ]
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    })
    
    cmd( 1):
    echo "extra step ..."
    
    cmd=>:
    echo "extra step ..."
    -
    extra step ...
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0174 log - verbose level v](../../logs/c0174_v)
* [c0174 log - verbose level vv](../../logs/c0174_vv)
* [c0174 log - verbose level vvv](../../logs/c0174_vvv)
* [c0174 log - verbose level vvvv](../../logs/c0174_vvvv)
* [c0174 log - verbose level vvvvv](../../logs/c0174_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0174)
