---
title: "c0048_vvvv"
date: 2020-10-07T00:11:08+1010:00
draft: false
weight: 10483

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0048
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
    loading [Task]:  ./tests/functests/c0048
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
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [
    The envVar flag makes the dvar name STUDENT_NAME is accessible as environment vars
    ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "envVar_STUDENT_NAME": "Tom Hanks",
      "STUDENT_NAME": "Tom Hanks",
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    env |grep STUDENT_NAME
    
    cmd=>:
    env |grep STUDENT_NAME
    -
    STUDENT_NAME=Tom Hanks
    
    -
     .. ok
    . ok
    -Step2: [
    STUDENT_NAME is also accessible in dvar processing
    ]
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep STUDENT_NAME",
        Code: 0,
        Output: "STUDENT_NAME=Tom Hanks",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep STUDENT_NAME",
        Code: 0,
        Output: "STUDENT_NAME=Tom Hanks",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "envVar_STUDENT_NAME": "Tom Hanks",
      "student_name_re_map": "Tom Hanks",
      "STUDENT_NAME": "Tom Hanks"
    })
    
    cmd( 1):
    env |grep STUDENT_NAME
    
    cmd=>:
    env |grep STUDENT_NAME
    -
    STUDENT_NAME=Tom Hanks
    
    -
     .. ok
    cmd( 2):
    echo "student_name_re_map is [{{.student_name_re_map}}]"
    
    cmd=>:
    echo "student_name_re_map is [Tom Hanks]"
    -
    student_name_re_map is [Tom Hanks]
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0048 log - verbose level v](../../logs/c0048_v)
* [c0048 log - verbose level vv](../../logs/c0048_vv)
* [c0048 log - verbose level vvv](../../logs/c0048_vvv)
* [c0048 log - verbose level vvvv](../../logs/c0048_vvvv)
* [c0048 log - verbose level vvvvv](../../logs/c0048_vvvvv)

##### References
* [Related Chapter](../../env-vars/c0048)
