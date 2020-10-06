---
title: "c0021_vvvv"
date: 2020-10-07T00:11:04+1010:00
draft: false
weight: 10213

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0021
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
    loading [Task]:  ./tests/functests/c0021
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
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "student": "Tom",
      "gender": "Male",
      "school": "Sydney Grammar",
      "info": "student: Tom\n gender: Male\n school: Sydney Grammar\n",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "student": "Tom",
      "gender": "Male",
      "school": "Sydney Grammar",
      "info": "student: Tom\n gender: Male\n school: Sydney Grammar\n"
    })
    
    cmd( 1):
    echo """my student: {{.student}}
    student's gender: {{.gender}}
     school's name: {{.school}}"""
    
    
    cmd=>:
    echo """my student: Tom
    student's gender: Male
     school's name: Sydney Grammar"""
    
    -
    my student: Tom
    student's gender: Male
     school's name: Sydney Grammar
    
    -
     .. ok
    cmd( 2):
    {{$details := .}}
    echo """my student: {{$details.student}}
    student's gender: {{$details.gender}}
     school's name: {{$details.school}}"""
    
    
    cmd=>:
    
    echo """my student: Tom
    student's gender: Male
     school's name: Sydney Grammar"""
    
    -
    my student: Tom
    student's gender: Male
     school's name: Sydney Grammar
    
    -
     .. ok
    cmd( 3):
    {{$a := .student}}
    {{$b := .gender}}
    {{$c := .school}}
    echo """my student: {{$a}}
    student's gender: {{$b}}
     school's name: {{$c}}"""
    
    
    cmd=>:
    
    
    
    echo """my student: Tom
    student's gender: Male
     school's name: Sydney Grammar"""
    
    -
    my student: Tom
    student's gender: Male
     school's name: Sydney Grammar
    
    -
     .. ok
    cmd( 4):
    echo """my school: {{.info.school}}"""
    
    
          template rendering -> template: .:1:26: executing "." at <.info.school>: can't evaluate field school in type interface {}
    WARN:
        1:echo """my school: {{.info.school}}"""
        2:
    
    trouble shooting tips:
    <incompatible types for comparison>: the variable might not be registered, use -v vvv to see the cache, or use inspect cmd to debug
    
          template rendering -> template: .:1:26: executing "." at <.info.school>: can't evaluate field school in type interface {}
    WARN:
        1:echo """my school: {{.info.school}}"""
        2:
    
    trouble shooting tips:
    <incompatible types for comparison>: the variable might not be registered, use -v vvv to see the cache, or use inspect cmd to debug
    
    cmd=>:
    echo """my school: 
    -
    /bin/sh: syntax error: unterminated quoted string
    
    -
     .. failed(suppressed if it is not the last step)
    cmd( 5):
    echo """my student: {{.info}}"""
    
    
    cmd=>:
    echo """my student: student: Tom
     gender: Male
     school: Sydney Grammar
    """
    
    -
    my student: student: Tom
     gender: Male
     school: Sydney Grammar
    
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0021 log - verbose level v](../../logs/c0021_v)
* [c0021 log - verbose level vv](../../logs/c0021_vv)
* [c0021 log - verbose level vvv](../../logs/c0021_vvv)
* [c0021 log - verbose level vvvv](../../logs/c0021_vvvv)
* [c0021 log - verbose level vvvvv](../../logs/c0021_vvvvv)

##### References
* [Related Chapter](../../vars/c0021)
