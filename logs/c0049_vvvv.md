---
title: "c0049_vvvv"
date: 2020-07-20T02:01:38+77:00
draft: false
weight: 10493

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0049
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0049
    ---------group vars----------
    
    global: {
      "envVar_SCHOOL": "James Rules",
      "SCHOOL": "James Rules"
    }
    
    
    groups members:[]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [self] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "envVar_SCHOOL": "James Rules",
      "SCHOOL": "James Rules"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "envVar_SCHOOL": "James Rules",
      "SCHOOL": "James Rules",
      "STUDENT_NAME": "James Bond",
      "envVar_STUDENT_NAME": "James Bond",
      "STUDENT_AGE": "18",
      "envVar_STUDENT_AGE": "18"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "STUDENT_AGE": "18",
      "envVar_STUDENT_AGE": "18",
      "envVar_SCHOOL": "James Rules",
      "SCHOOL": "James Rules",
      "STUDENT_NAME": "James Bond",
      "envVar_STUDENT_NAME": "James Bond"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "SCHOOL": "James Rules",
      "STUDENT_NAME": "Tom Hanks",
      "envVar_STUDENT_NAME": "Tom Hanks",
      "STUDENT_AGE": "18",
      "envVar_STUDENT_AGE": "18",
      "envVar_SCHOOL": "James Rules"
    })
    
    cmd( 1):
    env |grep STUDENT_NAME
    
    cmd=>:
    env |grep STUDENT_NAME<=
    STUDENT_NAME=Tom Hanks
     .. ok
    cmd( 2):
    env |grep STUDENT_AGE
    
    cmd=>:
    env |grep STUDENT_AGE<=
    STUDENT_AGE=18
     .. ok
    . ok
    -Step2: [: since there is no local envVar for STUDENT_NAME
    it should use global envVar value 'james bond'
     ]
    current exec runtime vars:
    (*core.Cache)({
      "STUDENT_AGE": "18",
      "envVar_STUDENT_AGE": "18",
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep STUDENT_AGE",
        Code: 0,
        Output: "STUDENT_AGE=18",
        ErrMsg: ""
      }),
      "envVar_SCHOOL": "James Rules",
      "SCHOOL": "James Rules",
      "STUDENT_NAME": "James Bond",
      "envVar_STUDENT_NAME": "James Bond"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "envVar_SCHOOL": "James Rules",
      "SCHOOL": "James Rules",
      "STUDENT_NAME": "James Bond",
      "envVar_STUDENT_NAME": "James Bond",
      "STUDENT_AGE": "18",
      "envVar_STUDENT_AGE": "18",
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep STUDENT_AGE",
        Code: 0,
        Output: "STUDENT_AGE=18",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    env |grep STUDENT_NAME
    
    cmd=>:
    env |grep STUDENT_NAME<=
    STUDENT_NAME=James Bond
     .. ok
    cmd( 2):
    env |grep STUDENT_AGE
    
    cmd=>:
    env |grep STUDENT_AGE<=
    STUDENT_AGE=18
     .. ok
    cmd( 3):
    env |grep SCHOOL
    
    cmd=>:
    env |grep SCHOOL<=
    SCHOOL=James Rules
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0049 log - verbose level v](../../logs/c0049_v)
* [c0049 log - verbose level vv](../../logs/c0049_vv)
* [c0049 log - verbose level vvv](../../logs/c0049_vvv)
* [c0049 log - verbose level vvvv](../../logs/c0049_vvvv)
* [c0049 log - verbose level vvvvv](../../logs/c0049_vvvvv)

##### References
* [Related Chapter](../../env-vars/c0049)
