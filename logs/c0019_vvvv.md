---
title: "c0019_vvvv"
date: 2020-07-20T02:01:32+77:00
draft: false
weight: 10193

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0019
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0019
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [self] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "sg": {
        "address": "Sydney, NSW 2000",
        "name": "sydney grammar"
      },
      "school": "sydney grammar"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "sg": {
        "name": "sydney grammar",
        "address": "Sydney, NSW 2000"
      },
      "school": "sydney grammar"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "sg": {
        "name": "sydney grammar",
        "address": "Sydney, NSW 2000"
      },
      "school": "sydney grammar",
      "studentname": "Tom"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "school": "sydney grammar",
      "studentname": "Tom",
      "sg": {
        "name": "sydney grammar",
        "address": "Sydney, NSW 2000"
      }
    })
    
    cmd( 1):
    echo "studentname -> {{.studentname}}"
    
    cmd=>:
    echo "studentname -> Tom"<=
    studentname -> Tom
     .. ok
    cmd( 2):
    echo "gender -> male"
    
    cmd=>:
    echo "gender -> male"<=
    gender -> male
     .. ok
    cmd( 3):
    echo "school -> {{.school}}"
    
    cmd=>:
    echo "school -> sydney grammar"<=
    school -> sydney grammar
     .. ok
    cmd( 4):
    echo "nonexist -> {{.notexist}}"
    
    cmd=>:
    echo "nonexist -> <no value>"<=
    nonexist -> <no value>
     .. ok
    cmd( 5):
    echo "SG details -> {{.sg.name}}/{{.sg.address}}"
    
    cmd=>:
    echo "SG details -> sydney grammar/Sydney, NSW 2000"<=
    SG details -> sydney grammar/Sydney, NSW 2000
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0019 log - verbose level v](../../logs/c0019_v)
* [c0019 log - verbose level vv](../../logs/c0019_vv)
* [c0019 log - verbose level vvv](../../logs/c0019_vvv)
* [c0019 log - verbose level vvvv](../../logs/c0019_vvvv)
* [c0019 log - verbose level vvvvv](../../logs/c0019_vvvvv)

##### References
* [Related Chapter](../../vars/c0019)
