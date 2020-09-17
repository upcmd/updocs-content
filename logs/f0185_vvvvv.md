---
title: "f0185_vvvvv"
date: 2020-09-18T01:28:05+99:00
draft: false
weight: 11854

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> f0185
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
    loading [Task]:  ./tests/functests/f0185
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001e5420)(<nil>)
    
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
    
    -Step1: [: task ]
    {
      Name: "",
      Do: {
        "sub_task_layer1"
      },
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "task",
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
    
    caller's vars to task (sub_task_layer1)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
      located task-> 2 [sub_task_layer1]: 
    =Task2: [task ==> sub_task_layer1: sub_task_layer1 ]
    Executing task stack layer: 2
    
    --Step1:
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
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    caller's vars to task (sub_task_layer2)::
    (*core.Cache)({
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "loopitem": "item1",
      "loopindex": 0
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
      "loopitem": "item1",
      "loopindex": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 2,
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    cmd( 1):
    echo """opening file: {{.loopitem}}"""
    
    cmd=>:
    echo """opening file: item1"""
    -
    opening file: item1
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=30) "echo \"\"\"opening file: item1\"\"\"",
     Code: (int) 0,
     Output: (string) (len=19) "opening file: item1",
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
    
    task Finally:
    Recovered from:   ERROR: Failed And Not Ignored! [You may want to continue and ignore the error]
    
    ---Step1: [close_file: ensure the opened file is closed
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
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2,
      "loopitem": "item1",
      "loopindex": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "loopitem": "item1",
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
     WARN: [Rescued in task level, but not advised!] - [setting rescue to yes/true to continue is not recommended
    it is advised to locate root cause of the problem, fix it and re-run the task again
    it is the best practice to test the execution in your ci pipeline to eliminate problems rather than dynamically fix using rescue]
    caller's vars to task (sub_task_layer2)::
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
      located task-> 3 [sub_task_layer2]: 
    ===Task3: [task/sub_task_layer1/sub_task_layer2 ==> sub_task_layer2: without rescue, the execution will return a non-zero  return code in shell and also report the error
    with rescue, the program will return 0
     ]
    Executing task stack layer: 4
    
    ----Step1: [step1: step 1 ]
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
      "up_runtime_task_layer_number": 3,
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2,
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
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 3,
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 3,
      "loopitem": "item2"
    })
    
    cmd( 1):
    echo """opening file: {{.loopitem}}"""
    
    cmd=>:
    echo """opening file: item2"""
    -
    opening file: item2
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=30) "echo \"\"\"opening file: item2\"\"\"",
     Code: (int) 0,
     Output: (string) (len=19) "opening file: item2",
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
    
    task Finally:
    Recovered from:   ERROR: Failed And Not Ignored! [You may want to continue and ignore the error]
    
    ----Step1: [close_file: ensure the opened file is closed
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
      "up_runtime_task_layer_number": 3,
      "loopitem": "item2",
      "loopindex": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 2,
      "up_runtime_task_layer_number": 3,
      "loopitem": "item2",
      "loopindex": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 3,
      "loopitem": "item2"
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
     WARN: [Rescued in task level, but not advised!] - [setting rescue to yes/true to continue is not recommended
    it is advised to locate root cause of the problem, fix it and re-run the task again
    it is the best practice to test the execution in your ci pipeline to eliminate problems rather than dynamically fix using rescue]
    Recovered from:   ERROR: Failed And Not Ignored! [You may want to continue and ignore the error]
    
     WARN: [Not rescued in task level] - [please assess the panic problem and cause, fix it before re-run the task]
    task finally ->   ERROR: Failed And Not Ignored! [You may want to continue and ignore the error]
    
    -----trace for reference-----
    
```

##### Logs with different verbose level
* [f0185 log - verbose level v](../../logs/f0185_v)
* [f0185 log - verbose level vv](../../logs/f0185_vv)
* [f0185 log - verbose level vvv](../../logs/f0185_vvv)
* [f0185 log - verbose level vvvv](../../logs/f0185_vvvv)
* [f0185 log - verbose level vvvvv](../../logs/f0185_vvvvv)

##### References
* [Related Chapter](../../flow-controll/f0185)
