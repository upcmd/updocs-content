---
title: "f0178_vvvvv"
date: 2020-09-18T00:52:03+99:00
draft: false
weight: 11784

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> f0178
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
    loading [Task]:  ./tests/functests/f0178
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc000172e40)(<nil>)
    
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
        "./tests/functests/mock_error.sh"
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
    ./tests/functests/mock_error.sh
    
    cmd=>:
    ./tests/functests/mock_error.sh
    -
    executing workflow .......
    step 1 .......
    step m .......
    encountering an error ......
    error 1 ......
    error 2 ......
    ./tests/functests/mock_error.sh: exit: line 11: Illegal number: -1
    
    -
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=31) "./tests/functests/mock_error.sh",
     Code: (int) 2,
     Output: (string) (len=56) "executing workflow .......\nstep 1 .......\nstep m .......",
     ErrMsg: (string) (len=126) "encountering an error ......\nerror 1 ......\nerror 2 ......\n./tests/functests/mock_error.sh: exit: line 11: Illegal number: -1\n"
    }
    
    Recovered from:   ERROR: Failed And Not Ignored! [You may want to continue and ignore the error]
    
     WARN: [Not rescued in task level] - [please assess the panic problem and cause, fix it before re-run the task]
    task finally ->   ERROR: Failed And Not Ignored! [You may want to continue and ignore the error]
    
    -----trace for reference-----
    
```

##### Logs with different verbose level
* [f0178 log - verbose level v](../../logs/f0178_v)
* [f0178 log - verbose level vv](../../logs/f0178_vv)
* [f0178 log - verbose level vvv](../../logs/f0178_vvv)
* [f0178 log - verbose level vvvv](../../logs/f0178_vvvv)
* [f0178 log - verbose level vvvvv](../../logs/f0178_vvvvv)

##### References
* [Related Chapter](../../shell-func/f0178)
