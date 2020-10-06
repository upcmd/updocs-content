---
title: "c0024_vvvv"
date: 2020-10-06T23:45:54+1010:00
draft: false
weight: 10243

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0024
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
    loading [Task]:  ./tests/functests/c0024
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
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "studentgender": "Male",
      "studentname": "Tom"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "studentgender": "Male",
      "studentname": "Tom",
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "studentgender": "Male",
      "studentname": "Tom",
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "student=>{{.student}}"
    
    cmd=>:
    echo "student=>map[gender:Male name:Tom school:Sydney Grammar]"
    -
    student=>map[gender:Male name:Tom school:Sydney Grammar]
    
    -
     .. ok
    cmd( 2):
    echo "name=>{{.studentname}}"
    
    cmd=>:
    echo "name=>Tom"
    -
    name=>Tom
    
    -
     .. ok
    cmd( 3):
    echo "gender=>{{.studentgender}}"
    
    cmd=>:
    echo "gender=>Male"
    -
    gender=>Male
    
    -
     .. ok
    cmd( 4):
    echo "school=>{{.student.school}}"
    
    cmd=>:
    echo "school=>Sydney Grammar"
    -
    school=>Sydney Grammar
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0024 log - verbose level v](../../logs/c0024_v)
* [c0024 log - verbose level vv](../../logs/c0024_vv)
* [c0024 log - verbose level vvv](../../logs/c0024_vvv)
* [c0024 log - verbose level vvvv](../../logs/c0024_vvvv)
* [c0024 log - verbose level vvvvv](../../logs/c0024_vvvvv)

##### References
* [Related Chapter](../../dvars/c0024)
