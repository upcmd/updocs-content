---
title: "f0186_vvvvv"
date: 2020-09-18T01:28:05+99:00
draft: false
weight: 11864

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> f0186
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
    loading [Task]:  ./tests/functests/f0186
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc00013f620)(<nil>)
    
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
      "loopitem": "item1",
      "up_runtime_task_layer_number": 0,
      "loopindex": 0,
      "loopindex1": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "loopindex": 0,
      "loopindex1": 1,
      "loopitem": "item1"
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
      "loopitem": "item1",
      "up_runtime_task_layer_number": 1,
      "loopindex": 0,
      "loopindex1": 1
    })
    
    in sub_task_layer1
    ~~SubStep1: [print:  ]
    in sub_task_layer1
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
        "aaa",
        "bbb"
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
      "loopitem": "item1",
      "up_runtime_task_layer_number": 1,
      "loopindex": 0
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
      "loopindex": 0,
      "loopindex1": 1,
      "loopitem": "item1",
      "up_runtime_task_layer_number": 1
    })
    
    caller's vars to task (sub_task_layer2)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopindex": 0,
      "loopindex1": 1,
      "loopitem": "aaa"
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
      "loopitem": "aaa",
      "up_runtime_task_layer_number": 2,
      "loopindex": 0,
      "loopindex1": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 2,
      "loopindex": 0,
      "loopindex1": 1,
      "loopitem": "aaa"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "aaa",
      "up_runtime_task_layer_number": 2,
      "loopindex": 0,
      "loopindex1": 1
    })
    
    cmd( 1):
    echo """opening file: {{.loopitem}}"""
    
    cmd=>:
    echo """opening file: aaa"""
    -
    opening file: aaa
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=28) "echo \"\"\"opening file: aaa\"\"\"",
     Code: (int) 0,
     Output: (string) (len=17) "opening file: aaa",
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
      "loopindex": 0,
      "loopindex1": 1,
      "loopitem": "aaa",
      "up_runtime_task_layer_number": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopitem": "aaa",
      "up_runtime_task_layer_number": 2,
      "loopindex": 0,
      "loopindex1": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "aaa",
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
     WARN: [Rescued in task level, but not advised!] - [setting rescue to yes/true to continue is not recommended
    it is advised to locate root cause of the problem, fix it and re-run the task again
    it is the best practice to test the execution in your ci pipeline to eliminate problems rather than dynamically fix using rescue]
    caller's vars to task (sub_task_layer2)::
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "bbb",
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      })
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
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "bbb",
      "up_runtime_task_layer_number": 3
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
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "bbb",
      "up_runtime_task_layer_number": 3
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "bbb",
      "up_runtime_task_layer_number": 3
    })
    
    cmd( 1):
    echo """opening file: {{.loopitem}}"""
    
    cmd=>:
    echo """opening file: bbb"""
    -
    opening file: bbb
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=28) "echo \"\"\"opening file: bbb\"\"\"",
     Code: (int) 0,
     Output: (string) (len=17) "opening file: bbb",
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
      "loopitem": "bbb",
      "up_runtime_task_layer_number": 3,
      "loopindex": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "bbb",
      "up_runtime_task_layer_number": 3
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 3,
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "bbb"
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
* [f0186 log - verbose level v](../../logs/f0186_v)
* [f0186 log - verbose level vv](../../logs/f0186_vv)
* [f0186 log - verbose level vvv](../../logs/f0186_vvv)
* [f0186 log - verbose level vvvv](../../logs/f0186_vvvv)
* [f0186 log - verbose level vvvvv](../../logs/f0186_vvvvv)

##### References
* [Related Chapter](../../flow-controll/f0186)
