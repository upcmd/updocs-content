---
title: "c0189_vvvvv"
date: 2020-09-18T01:27:58+99:00
draft: false
weight: 11894

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0189
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
    loading [Task]:  ./tests/functests/c0189
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001e7100)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "global_aa": "aa"
    }
    
    (core.Cache) (len=1) {
     (string) (len=9) "global_aa": (string) (len=2) "aa"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "global_aa": "aa"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task: without rescue, the execution will return a non-zero  return code in shell and also report the error
    with rescue, the program will return 0
     ]
    Executing task stack layer: 1
    
    -Step1: [step1: step 1 ]
    {
      Name: "step1",
      Do: {
        "echo \"opening file\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "local_bb": "bb"
      },
      Dvars: {
        {
          Name: "task_tt",
          Value: "tt",
          Desc: "",
          Expand: 0,
          Flags: {
            "taskScope"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
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
      "global_aa": "aa",
      "up_runtime_task_layer_number": 0,
      "local_bb": "bb"
    })
    
    [local] dvar expanded result:
    {
      "task_tt": "tt"
    }
    
    
    scope[local] merged: {
      "global_aa": "aa",
      "up_runtime_task_layer_number": 0,
      "local_bb": "bb",
      "task_tt": "tt"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "global_aa": "aa",
      "up_runtime_task_layer_number": 0,
      "local_bb": "bb",
      "task_tt": "tt"
    })
    
    cmd( 1):
    echo "opening file"
    
    cmd=>:
    echo "opening file"
    -
    opening file
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"opening file\"",
     Code: (int) 0,
     Output: (string) (len=12) "opening file",
     ErrMsg: (string) ""
    }
    
    . ok
    task Finally:
    Step1: [close_file: ensure the opened file is closed
     ]
    {
      Name: "close_file",
      Do: {
        "echo \"close the file .....\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "finally_cc": "cc"
      },
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
      "task_tt": "tt",
      "finally_cc": "cc",
      "global_aa": "aa",
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "task_tt": "tt",
      "finally_cc": "cc",
      "global_aa": "aa",
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "global_aa": "aa",
      "up_runtime_task_layer_number": 0,
      "task_tt": "tt",
      "finally_cc": "cc"
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
* [c0189 log - verbose level v](../../logs/c0189_v)
* [c0189 log - verbose level vv](../../logs/c0189_vv)
* [c0189 log - verbose level vvv](../../logs/c0189_vvv)
* [c0189 log - verbose level vvvv](../../logs/c0189_vvvv)
* [c0189 log - verbose level vvvvv](../../logs/c0189_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0189)
