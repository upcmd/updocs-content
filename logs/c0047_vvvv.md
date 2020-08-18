---
title: "c0047_vvvv"
date: 2020-08-18T15:15:55+88:00
draft: false
weight: 10473

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0047
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
    loading [Task]:  ./tests/functests/c0047
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: {
      "student_name": "Tom Hanks",
      "student_age": "28"
    }
    
    
    groups members:[]
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
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "student_name": "Tom Hanks",
      "student_age": "28",
      "cli": "echo \"\"\"\nstudent details:\nname: Tom Hanks\nage: 28\n\"\"\"\n"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "cli": "echo \"\"\"\nstudent details:\nname: Tom Hanks\nage: 28\n\"\"\"\n",
      "student_name": "Tom Hanks",
      "student_age": "28"
    })
    
    cmd( 1):
    {{.cli}}
    
    cmd=>:
    echo """
    student details:
    name: Tom Hanks
    age: 28
    """
    
    -
    
    student details:
    name: Tom Hanks
    age: 28
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0047 log - verbose level v](../../logs/c0047_v)
* [c0047 log - verbose level vv](../../logs/c0047_vv)
* [c0047 log - verbose level vvv](../../logs/c0047_vvv)
* [c0047 log - verbose level vvvv](../../logs/c0047_vvvv)
* [c0047 log - verbose level vvvvv](../../logs/c0047_vvvvv)

##### References
* [Related Chapter](../../design-patterns/c0047)
