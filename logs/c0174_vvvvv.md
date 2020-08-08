---
title: "c0174_vvvvv"
date: 2020-08-09T01:36:27+88:00
draft: false
weight: 11744

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
    loading [Task]:  ./tests/functests/c0174
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001e7220)(<nil>)
    
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
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"opening file\"",
        "echo \"hello\"|grep \"world\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: {
        "ignoreError"
      },
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: {
        {
          "func": "shell",
          "desc": "ensure the opened file is closed\n",
          "do": {
            "echo \"close the file .....\"",
            "echo \"\"\"\nexec command: {{.up_runtime_shell_exec_result.Cmd}}\nerror code: {{.up_runtime_shell_exec_result.Code}}\nerror message: {{.up_runtime_shell_exec_result.ErrMsg}}\nerror output: {{.up_runtime_shell_exec_result.Output}}\n\"\"\"\n"
          }
        },
        {
          "desc": "see if the exec context result: up_runtime_shell_exec_result is still availabe\nconditional do something about the error etc\n",
          "do": {
            {
              "cmd": "error message: {{.up_runtime_shell_exec_result.ErrMsg}}\n",
              "name": "print"
            }
          },
          "if": "{{ne .up_runtime_shell_exec_result.Code 0}}",
          "func": "cmd"
        }
      },
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
    
    cmd( 1):
    echo "opening file"
    
    cmd=>:
    echo "opening file"<=
    opening file
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"opening file\"",
     Code: (int) 0,
     Output: (string) (len=12) "opening file",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello"|grep "world"
    
    cmd=>:
    echo "hello"|grep "world"<=
          exec wait -> exit status 1
    -----trace for reference-----
          exit status 1
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=25) "echo \"hello\"|grep \"world\"",
     Code: (int) 1,
     Output: (string) "",
     ErrMsg: (string) (len=13) "exit status 1"
    }
    
    Step Finally:
    (*utils.ExecResult)({
      Cmd: "echo \"hello\"|grep \"world\"",
      Code: 1,
      Output: "",
      ErrMsg: "exit status 1"
    })
    
    <nil>
    
    -Step1: [: ensure the opened file is closed
     ]
    {
      Name: "",
      Do: {
        "echo \"close the file .....\"",
        "echo \"\"\"\nexec command: {{.up_runtime_shell_exec_result.Cmd}}\nerror code: {{.up_runtime_shell_exec_result.Code}}\nerror message: {{.up_runtime_shell_exec_result.ErrMsg}}\nerror output: {{.up_runtime_shell_exec_result.Output}}\n\"\"\"\n"
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
      "up_runtime_shell_exec_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
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
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_shell_exec_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
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
    <=
    
    exec command: echo hello|grep world
    error code: 1
    error message: exit status 1
    error output: 
    
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=111) "echo \"\"\"\nexec command: echo \"hello\"|grep \"world\"\nerror code: 1\nerror message: exit status 1\nerror output: \n\"\"\"\n",
     Code: (int) 0,
     Output: (string) (len=92) "exec command: echo hello|grep world\nerror code: 1\nerror message: exit status 1\nerror output:",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2: [: see if the exec context result: up_runtime_shell_exec_result is still availabe
    conditional do something about the error etc
     ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "error message: {{.up_runtime_shell_exec_result.ErrMsg}}\n"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "see if the exec context result: up_runtime_shell_exec_result is still availabe\nconditional do something about the error etc\n",
      Reg: "",
      Flags: <nil>,
      If: "{{ne .up_runtime_shell_exec_result.Code 0}}",
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
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"\"\"\nexec command: echo \"hello\"|grep \"world\"\nerror code: 1\nerror message: exit status 1\nerror output: \n\"\"\"\n",
        Code: 0,
        Output: "exec command: echo hello|grep world\nerror code: 1\nerror message: exit status 1\nerror output:",
        ErrMsg: ""
      }),
      "up_runtime_shell_exec_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
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
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"\"\"\nexec command: echo \"hello\"|grep \"world\"\nerror code: 1\nerror message: exit status 1\nerror output: \n\"\"\"\n",
        Code: 0,
        Output: "exec command: echo hello|grep world\nerror code: 1\nerror message: exit status 1\nerror output:",
        ErrMsg: ""
      }),
      "up_runtime_shell_exec_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    })
    
    error message: {{.up_runtime_shell_exec_result.ErrMsg}}
    
    ~SubStep1: [print:  ]
    error message: exit status 1
    
     WARN: [HightLight:] - [Error ignored!!!]
    -Step2: [: this step will not be reached if the ignoreError flag is not set
    try it yourself to remove the ignoreError flag and see difference
     ]
    {
      Name: "",
      Do: {
        "echo \"extra step ...\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "this step will not be reached if the ignoreError flag is not set\ntry it yourself to remove the ignoreError flag and see difference\n",
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
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
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
    echo "extra step ..."<=
    extra step ...
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=21) "echo \"extra step ...\"",
     Code: (int) 0,
     Output: (string) (len=14) "extra step ...",
     ErrMsg: (string) ""
    }
    
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
