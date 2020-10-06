---
title: "c0187_vvvvv"
date: 2020-10-07T00:11:34+1010:00
draft: false
weight: 11874

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0187
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
    loading [Task]:  ./tests/functests/c0187
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001c1920)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc00000e950)({
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: task ]
    {
      Name: "",
      Do: {
        {
          "func": "call",
          "do": "sub_task_layer1"
        }
      },
      Dox: <nil>,
      Func: "block",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "task",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "item1",
        "item2"
      },
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
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
    
    -Step1:
    {
      Name: "",
      Do: "sub_task_layer1",
      Dox: <nil>,
      Func: "call",
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
      "loopindex": 0,
      "loopindex1": 1,
      "loopitem": "item1"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "loopindex": 0,
      "loopindex1": 1,
      "loopitem": "item1"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "loopitem": "item1",
      "up_runtime_task_layer_number": 0
    })
    
    caller's vars to task (sub_task_layer1)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "loopindex": 0,
      "loopindex1": 1,
      "loopitem": "item1"
    })
    
      located task-> 2 [sub_task_layer1]: 
    =Task2: [task ==> sub_task_layer1: sub_task_layer1 ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "in sub_task_layer1"
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
      "up_runtime_task_layer_number": 1,
      "loopindex": 0,
      "loopindex1": 1,
      "loopitem": "item1"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 0,
      "loopindex1": 1,
      "loopitem": "item1",
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 1,
      "loopitem": "item1",
      "up_runtime_task_layer_number": 1,
      "loopindex": 0
    })
    
    in sub_task_layer1
    ~~SubStep1: [print:  ]
    in sub_task_layer1
    --Step2: [: task ]
    {
      Name: "",
      Do: {
        {
          "func": "cmd",
          "desc": "processing .....",
          "do": {
            {
              "name": "print",
              "cmd": "{{.loopitem}}"
            }
          }
        },
        {
          "func": "call",
          "loop": {
            "xxx",
            "yyy"
          },
          "do": {
            "sub_task_layer2"
          }
        }
      },
      Dox: <nil>,
      Func: "block",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "task",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "aaaa",
        "bbbb"
      },
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "item1",
      "up_runtime_task_layer_number": 1,
      "loopindex": 0,
      "loopindex1": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopitem": "item1",
      "up_runtime_task_layer_number": 1,
      "loopindex": 0,
      "loopindex1": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "loopitem": "item1",
      "up_runtime_task_layer_number": 1
    })
    
    --Step1: [: processing ..... ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.loopitem}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "processing .....",
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
      "loopitem": "aaaa",
      "up_runtime_task_layer_number": 1,
      "loopindex": 0,
      "loopindex1": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 0,
      "loopindex1": 1,
      "loopitem": "aaaa",
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "aaaa",
      "up_runtime_task_layer_number": 1,
      "loopindex": 0,
      "loopindex1": 1
    })
    
    {{.loopitem}}
    ~~SubStep1: [print:  ]
    aaaa
    --Step2:
    {
      Name: "",
      Do: {
        "sub_task_layer2"
      },
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "xxx",
        "yyy"
      },
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 1,
      "loopitem": "aaaa",
      "up_runtime_task_layer_number": 1,
      "loopindex": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopitem": "aaaa",
      "up_runtime_task_layer_number": 1,
      "loopindex": 0,
      "loopindex1": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopindex": 0,
      "loopindex1": 1,
      "loopitem": "aaaa"
    })
    
    caller's vars to task (sub_task_layer2)::
    (*core.Cache)({
      "loopitem": "xxx",
      "up_runtime_task_layer_number": 1,
      "loopindex": 0,
      "loopindex1": 1
    })
    
      located task-> 3 [sub_task_layer2]: 
    ==Task3: [task/sub_task_layer1 ==> sub_task_layer2: without rescue, the execution will return a non-zero  return code in shell and also report the error
    with rescue, the program will return 0
     ]
    Executing task stack layer: 3
    
    ---Step1: [step1: step 1 ]
    {
      Name: "step1",
      Do: {
        "echo \"\"\"opening file: {{.loopitem}}\"\"\"",
        "echo \"hello\"|grep \"world\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "step 1",
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
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "xxx",
      "up_runtime_task_layer_number": 2,
      "loopindex": 0,
      "loopindex1": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 1,
      "loopitem": "xxx",
      "up_runtime_task_layer_number": 2,
      "loopindex": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "xxx",
      "up_runtime_task_layer_number": 2,
      "loopindex": 0,
      "loopindex1": 1
    })
    
    cmd( 1):
    echo """opening file: {{.loopitem}}"""
    
    cmd=>:
    echo """opening file: xxx"""
    -
    opening file: xxx
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=28) "echo \"\"\"opening file: xxx\"\"\"",
     Code: (int) 0,
     Output: (string) (len=17) "opening file: xxx",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello"|grep "world"
    
    cmd=>:
    echo "hello"|grep "world"
    -
    
    -
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=25) "echo \"hello\"|grep \"world\"",
     Code: (int) 1,
     Output: (string) "",
     ErrMsg: (string) (len=13) "exit status 1"
    }
    
     WARN: [ignoreError:] - [Error ignored!!!]
    ---Step2: [
    step2in this case, since there is no ignoreError, the exception was captured by task level finaly code block
    opened file is safely closed
    to make the flow to continue to reach step2, use ignoreError
    ]
    {
      Name: "step2",
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
      Desc: "in this case, since there is no ignoreError, the exception was captured by task level finaly code block\nopened file is safely closed\nto make the flow to continue to reach step2, use ignoreError\n",
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
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "loopitem": "xxx",
      "up_runtime_task_layer_number": 2,
      "loopindex": 0
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
      }),
      "loopitem": "xxx",
      "up_runtime_task_layer_number": 2,
      "loopindex": 0,
      "loopindex1": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "loopitem": "xxx",
      "up_runtime_task_layer_number": 2,
      "loopindex": 0
    })
    
    step 2
    ~~~SubStep1: [print:  ]
    step 2
    task Finally:
    --Step1: [
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
      "up_runtime_task_layer_number": 2,
      "loopindex": 0,
      "loopindex1": 1,
      "loopitem": "xxx"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 0,
      "loopindex1": 1,
      "loopitem": "xxx",
      "up_runtime_task_layer_number": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 1,
      "loopitem": "xxx",
      "up_runtime_task_layer_number": 2,
      "loopindex": 0
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
    caller's vars to task (sub_task_layer2)::
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "loopitem": "yyy",
      "up_runtime_task_layer_number": 1
    })
    
      located task-> 3 [sub_task_layer2]: 
    ==Task3: [task/sub_task_layer1 ==> sub_task_layer2: without rescue, the execution will return a non-zero  return code in shell and also report the error
    with rescue, the program will return 0
     ]
    Executing task stack layer: 3
    
    ---Step1: [step1: step 1 ]
    {
      Name: "step1",
      Do: {
        "echo \"\"\"opening file: {{.loopitem}}\"\"\"",
        "echo \"hello\"|grep \"world\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "step 1",
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
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "loopitem": "yyy",
      "up_runtime_task_layer_number": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 1,
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "loopitem": "yyy",
      "up_runtime_task_layer_number": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "loopindex": 1,
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "loopitem": "yyy"
    })
    
    cmd( 1):
    echo """opening file: {{.loopitem}}"""
    
    cmd=>:
    echo """opening file: yyy"""
    -
    opening file: yyy
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=28) "echo \"\"\"opening file: yyy\"\"\"",
     Code: (int) 0,
     Output: (string) (len=17) "opening file: yyy",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello"|grep "world"
    
    cmd=>:
    echo "hello"|grep "world"
    -
    
    -
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=25) "echo \"hello\"|grep \"world\"",
     Code: (int) 1,
     Output: (string) "",
     ErrMsg: (string) (len=13) "exit status 1"
    }
    
     WARN: [ignoreError:] - [Error ignored!!!]
    ---Step2: [
    step2in this case, since there is no ignoreError, the exception was captured by task level finaly code block
    opened file is safely closed
    to make the flow to continue to reach step2, use ignoreError
    ]
    {
      Name: "step2",
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
      Desc: "in this case, since there is no ignoreError, the exception was captured by task level finaly code block\nopened file is safely closed\nto make the flow to continue to reach step2, use ignoreError\n",
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
      "up_runtime_task_layer_number": 2,
      "loopindex": 1,
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "loopitem": "yyy"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 1,
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "loopitem": "yyy",
      "up_runtime_task_layer_number": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "loopitem": "yyy",
      "up_runtime_task_layer_number": 2
    })
    
    step 2
    ~~~SubStep1: [print:  ]
    step 2
    task Finally:
    --Step1: [
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
      "loopindex1": 2,
      "loopitem": "yyy",
      "up_runtime_task_layer_number": 2,
      "loopindex": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 2,
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "yyy"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "yyy",
      "up_runtime_task_layer_number": 2
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
    --Step1: [: processing ..... ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.loopitem}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "processing .....",
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
      "loopindex1": 2,
      "loopitem": "bbbb",
      "up_runtime_task_layer_number": 1,
      "loopindex": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 2,
      "loopitem": "bbbb",
      "up_runtime_task_layer_number": 1,
      "loopindex": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 2,
      "loopitem": "bbbb",
      "up_runtime_task_layer_number": 1,
      "loopindex": 1
    })
    
    {{.loopitem}}
    ~~SubStep1: [print:  ]
    bbbb
    --Step2:
    {
      Name: "",
      Do: {
        "sub_task_layer2"
      },
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "xxx",
        "yyy"
      },
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
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "bbbb"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "bbbb",
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "bbbb"
    })
    
    caller's vars to task (sub_task_layer2)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopindex": 0,
      "loopindex1": 1,
      "loopitem": "xxx"
    })
    
      located task-> 3 [sub_task_layer2]: 
    ==Task3: [task/sub_task_layer1 ==> sub_task_layer2: without rescue, the execution will return a non-zero  return code in shell and also report the error
    with rescue, the program will return 0
     ]
    Executing task stack layer: 3
    
    ---Step1: [step1: step 1 ]
    {
      Name: "step1",
      Do: {
        "echo \"\"\"opening file: {{.loopitem}}\"\"\"",
        "echo \"hello\"|grep \"world\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "step 1",
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
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "loopitem": "xxx",
      "up_runtime_task_layer_number": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 0,
      "loopindex1": 1,
      "loopitem": "xxx",
      "up_runtime_task_layer_number": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "xxx",
      "up_runtime_task_layer_number": 2,
      "loopindex": 0,
      "loopindex1": 1
    })
    
    cmd( 1):
    echo """opening file: {{.loopitem}}"""
    
    cmd=>:
    echo """opening file: xxx"""
    -
    opening file: xxx
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=28) "echo \"\"\"opening file: xxx\"\"\"",
     Code: (int) 0,
     Output: (string) (len=17) "opening file: xxx",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello"|grep "world"
    
    cmd=>:
    echo "hello"|grep "world"
    -
    
    -
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=25) "echo \"hello\"|grep \"world\"",
     Code: (int) 1,
     Output: (string) "",
     ErrMsg: (string) (len=13) "exit status 1"
    }
    
     WARN: [ignoreError:] - [Error ignored!!!]
    ---Step2: [
    step2in this case, since there is no ignoreError, the exception was captured by task level finaly code block
    opened file is safely closed
    to make the flow to continue to reach step2, use ignoreError
    ]
    {
      Name: "step2",
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
      Desc: "in this case, since there is no ignoreError, the exception was captured by task level finaly code block\nopened file is safely closed\nto make the flow to continue to reach step2, use ignoreError\n",
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
      }),
      "up_runtime_task_layer_number": 2,
      "loopindex": 0,
      "loopindex1": 1,
      "loopitem": "xxx"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 2,
      "loopindex": 0,
      "loopindex1": 1,
      "loopitem": "xxx",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 1,
      "loopitem": "xxx",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "up_runtime_task_layer_number": 2,
      "loopindex": 0
    })
    
    step 2
    ~~~SubStep1: [print:  ]
    step 2
    task Finally:
    --Step1: [
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
      "loopindex1": 1,
      "loopitem": "xxx",
      "up_runtime_task_layer_number": 2,
      "loopindex": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopitem": "xxx",
      "up_runtime_task_layer_number": 2,
      "loopindex": 0,
      "loopindex1": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "xxx",
      "up_runtime_task_layer_number": 2,
      "loopindex": 0,
      "loopindex1": 1
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
    caller's vars to task (sub_task_layer2)::
    (*core.Cache)({
      "loopitem": "yyy",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopindex": 1,
      "loopindex1": 2
    })
    
      located task-> 3 [sub_task_layer2]: 
    ==Task3: [task/sub_task_layer1 ==> sub_task_layer2: without rescue, the execution will return a non-zero  return code in shell and also report the error
    with rescue, the program will return 0
     ]
    Executing task stack layer: 3
    
    ---Step1: [step1: step 1 ]
    {
      Name: "step1",
      Do: {
        "echo \"\"\"opening file: {{.loopitem}}\"\"\"",
        "echo \"hello\"|grep \"world\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "step 1",
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
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "yyy",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 2,
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "yyy"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "yyy",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 2,
      "loopindex": 1,
      "loopindex1": 2
    })
    
    cmd( 1):
    echo """opening file: {{.loopitem}}"""
    
    cmd=>:
    echo """opening file: yyy"""
    -
    opening file: yyy
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=28) "echo \"\"\"opening file: yyy\"\"\"",
     Code: (int) 0,
     Output: (string) (len=17) "opening file: yyy",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello"|grep "world"
    
    cmd=>:
    echo "hello"|grep "world"
    -
    
    -
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=25) "echo \"hello\"|grep \"world\"",
     Code: (int) 1,
     Output: (string) "",
     ErrMsg: (string) (len=13) "exit status 1"
    }
    
     WARN: [ignoreError:] - [Error ignored!!!]
    ---Step2: [
    step2in this case, since there is no ignoreError, the exception was captured by task level finaly code block
    opened file is safely closed
    to make the flow to continue to reach step2, use ignoreError
    ]
    {
      Name: "step2",
      Do: {
        {
          "cmd": "step 2",
          "name": "print"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "in this case, since there is no ignoreError, the exception was captured by task level finaly code block\nopened file is safely closed\nto make the flow to continue to reach step2, use ignoreError\n",
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
      "loopitem": "yyy",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "up_runtime_task_layer_number": 2,
      "loopindex": 1,
      "loopindex1": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "yyy",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "up_runtime_task_layer_number": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "yyy",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "up_runtime_task_layer_number": 2,
      "loopindex": 1,
      "loopindex1": 2
    })
    
    step 2
    ~~~SubStep1: [print:  ]
    step 2
    task Finally:
    --Step1: [
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
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "yyy",
      "up_runtime_task_layer_number": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "yyy",
      "up_runtime_task_layer_number": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "yyy",
      "up_runtime_task_layer_number": 2
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
    -Step1:
    {
      Name: "",
      Do: "sub_task_layer1",
      Dox: <nil>,
      Func: "call",
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
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 0,
      "loopitem": "item2"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 0,
      "loopitem": "item2"
    })
    
    caller's vars to task (sub_task_layer1)::
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 0,
      "loopitem": "item2"
    })
    
      located task-> 2 [sub_task_layer1]: 
    =Task2: [task ==> sub_task_layer1: sub_task_layer1 ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "cmd": "in sub_task_layer1",
          "name": "print"
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
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "item2",
      "loopindex": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "item2"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "item2",
      "loopindex": 1
    })
    
    in sub_task_layer1
    ~~SubStep1: [print:  ]
    in sub_task_layer1
    --Step2: [: task ]
    {
      Name: "",
      Do: {
        {
          "func": "cmd",
          "desc": "processing .....",
          "do": {
            {
              "name": "print",
              "cmd": "{{.loopitem}}"
            }
          }
        },
        {
          "func": "call",
          "loop": {
            "xxx",
            "yyy"
          },
          "do": {
            "sub_task_layer2"
          }
        }
      },
      Dox: <nil>,
      Func: "block",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "task",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "aaaa",
        "bbbb"
      },
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
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "item2"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1
    })
    
    --Step1: [: processing ..... ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.loopitem}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "processing .....",
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
      "loopitem": "aaaa",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "loopitem": "aaaa",
      "loopindex": 0,
      "loopindex1": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "aaaa",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    {{.loopitem}}
    ~~SubStep1: [print:  ]
    aaaa
    --Step2:
    {
      Name: "",
      Do: {
        "sub_task_layer2"
      },
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "xxx",
        "yyy"
      },
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "aaaa",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopitem": "aaaa",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "aaaa",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1
    })
    
    caller's vars to task (sub_task_layer2)::
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "loopitem": "xxx"
    })
    
      located task-> 3 [sub_task_layer2]: 
    ==Task3: [task/sub_task_layer1 ==> sub_task_layer2: without rescue, the execution will return a non-zero  return code in shell and also report the error
    with rescue, the program will return 0
     ]
    Executing task stack layer: 3
    
    ---Step1: [step1: step 1 ]
    {
      Name: "step1",
      Do: {
        "echo \"\"\"opening file: {{.loopitem}}\"\"\"",
        "echo \"hello\"|grep \"world\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "step 1",
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
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2,
      "loopitem": "xxx",
      "loopindex": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopitem": "xxx",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2,
      "loopitem": "xxx"
    })
    
    cmd( 1):
    echo """opening file: {{.loopitem}}"""
    
    cmd=>:
    echo """opening file: xxx"""
    -
    opening file: xxx
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=28) "echo \"\"\"opening file: xxx\"\"\"",
     Code: (int) 0,
     Output: (string) (len=17) "opening file: xxx",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello"|grep "world"
    
    cmd=>:
    echo "hello"|grep "world"
    -
    
    -
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=25) "echo \"hello\"|grep \"world\"",
     Code: (int) 1,
     Output: (string) "",
     ErrMsg: (string) (len=13) "exit status 1"
    }
    
     WARN: [ignoreError:] - [Error ignored!!!]
    ---Step2: [
    step2in this case, since there is no ignoreError, the exception was captured by task level finaly code block
    opened file is safely closed
    to make the flow to continue to reach step2, use ignoreError
    ]
    {
      Name: "step2",
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
      Desc: "in this case, since there is no ignoreError, the exception was captured by task level finaly code block\nopened file is safely closed\nto make the flow to continue to reach step2, use ignoreError\n",
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
      }),
      "loopitem": "xxx",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "loopitem": "xxx"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "loopitem": "xxx",
      "loopindex": 0
    })
    
    step 2
    ~~~SubStep1: [print:  ]
    step 2
    task Finally:
    --Step1: [
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
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2,
      "loopitem": "xxx"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopitem": "xxx",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2,
      "loopitem": "xxx",
      "loopindex": 0
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
    caller's vars to task (sub_task_layer2)::
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "loopitem": "yyy",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1
    })
    
      located task-> 3 [sub_task_layer2]: 
    ==Task3: [task/sub_task_layer1 ==> sub_task_layer2: without rescue, the execution will return a non-zero  return code in shell and also report the error
    with rescue, the program will return 0
     ]
    Executing task stack layer: 3
    
    ---Step1: [step1: step 1 ]
    {
      Name: "step1",
      Do: {
        "echo \"\"\"opening file: {{.loopitem}}\"\"\"",
        "echo \"hello\"|grep \"world\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "step 1",
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
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "yyy",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2,
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
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "loopitem": "yyy",
      "loopindex": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "yyy",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo """opening file: {{.loopitem}}"""
    
    cmd=>:
    echo """opening file: yyy"""
    -
    opening file: yyy
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=28) "echo \"\"\"opening file: yyy\"\"\"",
     Code: (int) 0,
     Output: (string) (len=17) "opening file: yyy",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello"|grep "world"
    
    cmd=>:
    echo "hello"|grep "world"
    -
    
    -
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=25) "echo \"hello\"|grep \"world\"",
     Code: (int) 1,
     Output: (string) "",
     ErrMsg: (string) (len=13) "exit status 1"
    }
    
     WARN: [ignoreError:] - [Error ignored!!!]
    ---Step2: [
    step2in this case, since there is no ignoreError, the exception was captured by task level finaly code block
    opened file is safely closed
    to make the flow to continue to reach step2, use ignoreError
    ]
    {
      Name: "step2",
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
      Desc: "in this case, since there is no ignoreError, the exception was captured by task level finaly code block\nopened file is safely closed\nto make the flow to continue to reach step2, use ignoreError\n",
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
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "loopitem": "yyy",
      "loopindex": 1
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
      }),
      "loopitem": "yyy",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "loopitem": "yyy"
    })
    
    step 2
    ~~~SubStep1: [print:  ]
    step 2
    task Finally:
    --Step1: [
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
      "loopitem": "yyy",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2,
      "loopitem": "yyy"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "yyy",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2
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
    --Step1: [: processing ..... ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.loopitem}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "processing .....",
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
      "loopitem": "bbbb",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "loopitem": "bbbb",
      "loopindex": 1,
      "loopindex1": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "bbbb",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    {{.loopitem}}
    ~~SubStep1: [print:  ]
    bbbb
    --Step2:
    {
      Name: "",
      Do: {
        "sub_task_layer2"
      },
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "xxx",
        "yyy"
      },
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "bbbb",
      "loopindex": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "bbbb",
      "loopindex": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "bbbb",
      "loopindex": 1
    })
    
    caller's vars to task (sub_task_layer2)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "xxx",
      "loopindex": 0,
      "loopindex1": 1
    })
    
      located task-> 3 [sub_task_layer2]: 
    ==Task3: [task/sub_task_layer1 ==> sub_task_layer2: without rescue, the execution will return a non-zero  return code in shell and also report the error
    with rescue, the program will return 0
     ]
    Executing task stack layer: 3
    
    ---Step1: [step1: step 1 ]
    {
      Name: "step1",
      Do: {
        "echo \"\"\"opening file: {{.loopitem}}\"\"\"",
        "echo \"hello\"|grep \"world\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "step 1",
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
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2,
      "loopitem": "xxx"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopitem": "xxx",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2,
      "loopitem": "xxx",
      "loopindex": 0
    })
    
    cmd( 1):
    echo """opening file: {{.loopitem}}"""
    
    cmd=>:
    echo """opening file: xxx"""
    -
    opening file: xxx
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=28) "echo \"\"\"opening file: xxx\"\"\"",
     Code: (int) 0,
     Output: (string) (len=17) "opening file: xxx",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello"|grep "world"
    
    cmd=>:
    echo "hello"|grep "world"
    -
    
    -
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=25) "echo \"hello\"|grep \"world\"",
     Code: (int) 1,
     Output: (string) "",
     ErrMsg: (string) (len=13) "exit status 1"
    }
    
     WARN: [ignoreError:] - [Error ignored!!!]
    ---Step2: [
    step2in this case, since there is no ignoreError, the exception was captured by task level finaly code block
    opened file is safely closed
    to make the flow to continue to reach step2, use ignoreError
    ]
    {
      Name: "step2",
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
      Desc: "in this case, since there is no ignoreError, the exception was captured by task level finaly code block\nopened file is safely closed\nto make the flow to continue to reach step2, use ignoreError\n",
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
      "up_runtime_task_layer_number": 2,
      "loopitem": "xxx",
      "loopindex": 0,
      "loopindex1": 1,
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
      "up_runtime_task_layer_number": 2,
      "loopitem": "xxx",
      "loopindex": 0,
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "up_runtime_task_layer_number": 2,
      "loopitem": "xxx"
    })
    
    step 2
    ~~~SubStep1: [print:  ]
    step 2
    task Finally:
    --Step1: [
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
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2,
      "loopitem": "xxx",
      "loopindex": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 2,
      "loopitem": "xxx",
      "loopindex": 0,
      "loopindex1": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "loopitem": "xxx",
      "loopindex": 0,
      "loopindex1": 1
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
    caller's vars to task (sub_task_layer2)::
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": "yyy",
      "loopindex": 1,
      "loopindex1": 2
    })
    
      located task-> 3 [sub_task_layer2]: 
    ==Task3: [task/sub_task_layer1 ==> sub_task_layer2: without rescue, the execution will return a non-zero  return code in shell and also report the error
    with rescue, the program will return 0
     ]
    Executing task stack layer: 3
    
    ---Step1: [step1: step 1 ]
    {
      Name: "step1",
      Do: {
        "echo \"\"\"opening file: {{.loopitem}}\"\"\"",
        "echo \"hello\"|grep \"world\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "step 1",
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
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 2,
      "loopitem": "yyy",
      "loopindex": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 2,
      "loopitem": "yyy",
      "loopindex": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 2,
      "loopitem": "yyy",
      "loopindex": 1
    })
    
    cmd( 1):
    echo """opening file: {{.loopitem}}"""
    
    cmd=>:
    echo """opening file: yyy"""
    -
    opening file: yyy
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=28) "echo \"\"\"opening file: yyy\"\"\"",
     Code: (int) 0,
     Output: (string) (len=17) "opening file: yyy",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello"|grep "world"
    
    cmd=>:
    echo "hello"|grep "world"
    -
    
    -
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=25) "echo \"hello\"|grep \"world\"",
     Code: (int) 1,
     Output: (string) "",
     ErrMsg: (string) (len=13) "exit status 1"
    }
    
     WARN: [ignoreError:] - [Error ignored!!!]
    ---Step2: [
    step2in this case, since there is no ignoreError, the exception was captured by task level finaly code block
    opened file is safely closed
    to make the flow to continue to reach step2, use ignoreError
    ]
    {
      Name: "step2",
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
      Desc: "in this case, since there is no ignoreError, the exception was captured by task level finaly code block\nopened file is safely closed\nto make the flow to continue to reach step2, use ignoreError\n",
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
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "up_runtime_task_layer_number": 2,
      "loopitem": "yyy",
      "loopindex": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopitem": "yyy",
      "loopindex": 1,
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "up_runtime_task_layer_number": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "loopitem": "yyy",
      "loopindex": 1,
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    })
    
    step 2
    ~~~SubStep1: [print:  ]
    step 2
    task Finally:
    --Step1: [
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
      "loopitem": "yyy",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopitem": "yyy",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "yyy",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2
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
    
```

##### Logs with different verbose level
* [c0187 log - verbose level v](../../logs/c0187_v)
* [c0187 log - verbose level vv](../../logs/c0187_vv)
* [c0187 log - verbose level vvv](../../logs/c0187_vvv)
* [c0187 log - verbose level vvvv](../../logs/c0187_vvvv)
* [c0187 log - verbose level vvvvv](../../logs/c0187_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0187)
