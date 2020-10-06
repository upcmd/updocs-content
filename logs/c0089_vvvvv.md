---
title: "c0089_vvvvv"
date: 2020-10-06T23:46:06+1010:00
draft: false
weight: 10894

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0089
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
    loading [Task]:  ./tests/functests/c0089
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc00023ee60)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "dynadir": "./tests/functests"
    })
    
    (*core.Cache)(0xc00000e8f8)((len=1) {
     (string) (len=7) "dynadir": (string) (len=17) "./tests/functests"
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "dynadir": "./tests/functests"
    })
    
    loading [flow ref]:  ./tests/functests/c0089-task-main.yml
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"task step 1\"",
        "echo \"task step 2\""
      },
      Dox: <nil>,
      Func: "shell",
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
      "dynadir": "./tests/functests",
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "dynadir": "./tests/functests"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "dynadir": "./tests/functests",
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "task step 1"
    
    cmd=>:
    echo "task step 1"
    -
    task step 1
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"task step 1\"",
     Code: (int) 0,
     Output: (string) (len=11) "task step 1",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "task step 2"
    
    cmd=>:
    echo "task step 2"
    -
    task step 2
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"task step 2\"",
     Code: (int) 0,
     Output: (string) (len=11) "task step 2",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0089 log - verbose level v](../../logs/c0089_v)
* [c0089 log - verbose level vv](../../logs/c0089_vv)
* [c0089 log - verbose level vvv](../../logs/c0089_vvv)
* [c0089 log - verbose level vvvv](../../logs/c0089_vvvv)
* [c0089 log - verbose level vvvvv](../../logs/c0089_vvvvv)

##### References
* [Related Chapter](../../organization/c0089)
