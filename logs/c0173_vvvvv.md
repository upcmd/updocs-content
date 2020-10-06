---
title: "c0173_vvvvv"
date: 2020-10-07T00:11:31+1010:00
draft: false
weight: 11734

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0173
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0173
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001e7360)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "global_aaa": "aaa"
    })
    
    (*core.Cache)(0xc000126918)((len=1) {
     (string) (len=10) "global_aaa": (string) (len=3) "aaa"
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "global_aaa": "aaa"
    })
    
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
      Vars: {
        "local_aaa": "local_aaa"
      },
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
      Finally: {
        {
          "func": "cmd",
          "do": {
            {
              "name": "print",
              "cmd": "global aaa: {{.global_aaa}}"
            },
            {
              "name": "print",
              "cmd": "local aaa: {{.local_aaa}}"
            }
          }
        },
        {
          "func": "shell",
          "name": "close_file",
          "desc": "ensure the opened file is closed\n",
          "do": {
            "echo \"close the file .....\""
          }
        },
        {
          "func": "cmd",
          "desc": "extra steps",
          "do": {
            {
              "name": "print",
              "cmd": "extra step"
            }
          }
        }
      },
      Rescue: true
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "local_aaa": "local_aaa",
      "global_aaa": "aaa"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "local_aaa": "local_aaa",
      "global_aaa": "aaa",
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "global_aaa": "aaa",
      "up_runtime_task_layer_number": 0,
      "local_aaa": "local_aaa"
    })
    
    step 1
    ~SubStep1: [print:  ]
    step 1
    ~SubStep2: [panic:  ]
     WARN: [manual panic] - [manual trigger a panic cmd]
    Step Finally:
    (*utils.ExecResult)(<nil>)
    
    Recovered from: manual trigger a panic cmd
    -Step1:
    {
      Name: "",
      Do: {
        {
          "cmd": "global aaa: {{.global_aaa}}",
          "name": "print"
        },
        {
          "name": "print",
          "cmd": "local aaa: {{.local_aaa}}"
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
      "up_runtime_task_layer_number": 0,
      "local_aaa": "local_aaa",
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>),
      "global_aaa": "aaa"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "global_aaa": "aaa",
      "up_runtime_task_layer_number": 0,
      "local_aaa": "local_aaa",
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>)
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "global_aaa": "aaa",
      "up_runtime_task_layer_number": 0,
      "local_aaa": "local_aaa",
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>)
    })
    
    global aaa: {{.global_aaa}}
    ~SubStep1: [print:  ]
    global aaa: aaa
    local aaa: {{.local_aaa}}
    ~SubStep2: [print:  ]
    local aaa: local_aaa
    -Step2: [
    close_fileensure the opened file is closed
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
      "local_aaa": "local_aaa",
      "global_aaa": "aaa",
      "up_runtime_task_layer_number": 0,
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>)
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "local_aaa": "local_aaa",
      "global_aaa": "aaa",
      "up_runtime_task_layer_number": 0,
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>)
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>),
      "local_aaa": "local_aaa",
      "global_aaa": "aaa",
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
    (utils.ExecResult) {
     Cmd: (string) (len=27) "echo \"close the file .....\"",
     Code: (int) 0,
     Output: (string) (len=20) "close the file .....",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step3: [: extra steps ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "extra step"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "extra steps",
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
      "up_runtime_task_layer_number": 0,
      "local_aaa": "local_aaa",
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>),
      "global_aaa": "aaa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "local_aaa": "local_aaa",
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>),
      "global_aaa": "aaa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>),
      "global_aaa": "aaa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "local_aaa": "local_aaa"
    })
    
    extra step
    ~SubStep1: [print:  ]
    extra step
     WARN: [Rescued in step level, but not advised!] - [setting rescue to yes/true to continue is not recommended
    it is advised to locate root cause of the problem, fix it and re-run the task again
    it is the best practice to test the execution in your ci pipeline to eliminate problems rather than dynamically fix using rescue]
    -Step2: [: step 2 ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "step 2"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "step 2",
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
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "global_aaa": "aaa",
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "global_aaa": "aaa",
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "global_aaa": "aaa",
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      })
    })
    
    step 2
    ~SubStep1: [print:  ]
    step 2
    
```

##### Logs with different verbose level
* [c0173 log - verbose level v](../../logs/c0173_v)
* [c0173 log - verbose level vv](../../logs/c0173_vv)
* [c0173 log - verbose level vvv](../../logs/c0173_vvv)
* [c0173 log - verbose level vvvv](../../logs/c0173_vvvv)
* [c0173 log - verbose level vvvvv](../../logs/c0173_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0173)
