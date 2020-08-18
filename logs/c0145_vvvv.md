---
title: "c0145_vvvv"
date: 2020-08-18T15:16:18+88:00
draft: false
weight: 11453

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0145
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
    loading [Task]:  ./tests/functests/c0145
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
    Task1: [task ==> task: mock up test to test module.template rendering ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
    })
    
    ~SubStep1: [template: render a template file to a file 1 ]
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    cat /tmp/mockup_doc.md
    
    cmd=>:
    cat /tmp/mockup_doc.md
    -
    title: "HelloWorld example"
    date: 2020-08-17T23:52:49+88:00
    draft: false-
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0145 log - verbose level v](../../logs/c0145_v)
* [c0145 log - verbose level vv](../../logs/c0145_vv)
* [c0145 log - verbose level vvv](../../logs/c0145_vvv)
* [c0145 log - verbose level vvvv](../../logs/c0145_vvvv)
* [c0145 log - verbose level vvvvv](../../logs/c0145_vvvvv)

##### References
* [Related Chapter](../../cmd-func/c0145)
