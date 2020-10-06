---
title: "c0020_vvvv"
date: 2020-10-06T23:45:53+1010:00
draft: false
weight: 10203

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0020
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0020
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "school": "sydney grammar"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "school": "sydney grammar"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: call function with different vars ]
    current exec runtime vars:
    (*core.Cache)({
      "studentname": "Tom",
      "gender": "male",
      "school": "sydney grammar",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "school": "sydney grammar",
      "up_runtime_task_layer_number": 0,
      "studentname": "Tom",
      "gender": "male"
    })
    
      located task-> 2 [function]: 
    =Task2: [task ==> function: as a design pattern, this is a function task
    it's better to not to use any local vars, in this
    way, the vars are passed in from caller call so
    that this function could be used by multiple ref tasks
     ]
    Executing task stack layer: 2
    
    --Step1: [: show school and student info ]
    current exec runtime vars:
    (*core.Cache)({
      "school": "sydney grammar",
      "up_runtime_task_layer_number": 1,
      "studentname": "Tom",
      "gender": "male"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "studentname": "Tom",
      "gender": "male",
      "school": "sydney grammar"
    })
    
    cmd( 1):
    echo "studentname -> {{.studentname}} | gender -> {{.gender}}"
    
    cmd=>:
    echo "studentname -> Tom | gender -> male"
    -
    studentname -> Tom | gender -> male
    
    -
     .. ok
    cmd( 2):
    echo "school -> {{.school}}"
    
    cmd=>:
    echo "school -> sydney grammar"
    -
    school -> sydney grammar
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0020 log - verbose level v](../../logs/c0020_v)
* [c0020 log - verbose level vv](../../logs/c0020_vv)
* [c0020 log - verbose level vvv](../../logs/c0020_vvv)
* [c0020 log - verbose level vvvv](../../logs/c0020_vvvv)
* [c0020 log - verbose level vvvvv](../../logs/c0020_vvvvv)

##### References
* [Related Chapter](../../call-func/c0020)
