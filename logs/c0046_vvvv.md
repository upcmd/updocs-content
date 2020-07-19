---
title: "c0046_vvvv"
date: 2020-07-20T02:01:37+77:00
draft: false
weight: 10463

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0046
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0046
    ---------group vars----------
    
    global: {
      "student_age": "28",
      "student_name": "Tom Hanks"
    }
    
    
    groups members:[]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [self] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "student_name": "Tom Hanks",
      "student_age": "28"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "student_name": "Tom Hanks",
      "student_age": "28",
      "cli": "echo \"\"\"\nstudent details:\nname: Tom Hanks\nage: 28\n\"\"\"\n"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    
```

##### Logs with different verbose level
* [c0046 log - verbose level v](../../logs/c0046_v)
* [c0046 log - verbose level vv](../../logs/c0046_vv)
* [c0046 log - verbose level vvv](../../logs/c0046_vvv)
* [c0046 log - verbose level vvvv](../../logs/c0046_vvvv)
* [c0046 log - verbose level vvvvv](../../logs/c0046_vvvvv)

##### References
* [Related Chapter](../../env-vars/c0046)
