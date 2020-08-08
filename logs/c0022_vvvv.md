---
title: "c0022_vvvv"
date: 2020-08-09T01:36:02+88:00
draft: false
weight: 10223

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0022
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
    loading [Task]:  ./tests/functests/c0022
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
      "student": "Tom",
      "gender": "Male",
      "school": "Sydney Grammar",
      "info": "my student: {{.student}}\nstudent's gender: {{.gender}}\nschool's name: {{.school}}\n"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": "Tom",
      "gender": "Male",
      "school": "Sydney Grammar",
      "info": "my student: {{.student}}\nstudent's gender: {{.gender}}\nschool's name: {{.school}}\n"
    })
    
    cmd( 1):
    echo """{{.info}}"""
    
    
    cmd=>:
    echo """my student: {{.student}}
    student's gender: {{.gender}}
    school's name: {{.school}}
    """
    <=
    my student: {{.student}}
    student's gender: {{.gender}}
    school's name: {{.school}}
    
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0022 log - verbose level v](../../logs/c0022_v)
* [c0022 log - verbose level vv](../../logs/c0022_vv)
* [c0022 log - verbose level vvv](../../logs/c0022_vvv)
* [c0022 log - verbose level vvvv](../../logs/c0022_vvvv)
* [c0022 log - verbose level vvvvv](../../logs/c0022_vvvvv)

##### References
* [Related Chapter](../../vars/c0022)
