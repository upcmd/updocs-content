---
title: "f0178_vvvv"
date: 2020-08-18T15:16:30+88:00
draft: false
weight: 11783

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
    loading [Task]:  ./tests/functests/f0178
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
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
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
     WARN: [Not rescued in task level] - [please assess the panic problem and cause, fix it before re-run the task]
    task finally ->   ERROR: Failed And Not Ignored! [You may want to continue and ignore the error]
    
    
```

##### Logs with different verbose level
* [f0178 log - verbose level v](../../logs/f0178_v)
* [f0178 log - verbose level vv](../../logs/f0178_vv)
* [f0178 log - verbose level vvv](../../logs/f0178_vvv)
* [f0178 log - verbose level vvvv](../../logs/f0178_vvvv)
* [f0178 log - verbose level vvvvv](../../logs/f0178_vvvvv)

##### References
* [Related Chapter](../../shell-func/f0178)