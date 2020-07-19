---
title: "c0069_vvvv"
date: 2020-07-20T02:01:41+77:00
draft: false
weight: 10693

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0069
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0069
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
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          },
          "school": "Sydney Grammar"
        }
      }
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          },
          "school": "Sydney Grammar"
        }
      },
      "school_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "school_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          },
          "school": "Sydney Grammar"
        }
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "suburb": {
            "cbd": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        }
      },
      "school_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n"
    })
    
    cmd( 1):
    echo """school address {{.school_address}}"""
    
    cmd=>:
    echo """school address address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
    """<=
    school address address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
     .. ok
    cmd( 2):
    echo """school address {{.school_address}}""" > /tmp/school.txt
    
    cmd=>:
    echo """school address address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
    """ > /tmp/school.txt<=
    
     .. ok
    cmd( 3):
    cat /tmp/school.txt
    
    cmd=>:
    cat /tmp/school.txt<=
    school address address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0069 log - verbose level v](../../logs/c0069_v)
* [c0069 log - verbose level vv](../../logs/c0069_vv)
* [c0069 log - verbose level vvv](../../logs/c0069_vvv)
* [c0069 log - verbose level vvvv](../../logs/c0069_vvvv)
* [c0069 log - verbose level vvvvv](../../logs/c0069_vvvvv)

##### References
* [Related Chapter](../../templating/c0069)
