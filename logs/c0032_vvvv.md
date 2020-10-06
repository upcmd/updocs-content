---
title: "c0032_vvvv"
date: 2020-10-06T23:45:56+1010:00
draft: false
weight: 10323

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0032
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
    loading [Task]:  ./tests/functests/c0032
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    nonprod: (*core.Cache)({
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_object": {
        "address": {
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        }
      },
      "c": "non-prod-c",
      "d": "non-prod-d",
      "a": "non-prod-a",
      "b": "non-prod-b"
    })
    
    
    global: (*core.Cache)({
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        }
      }
    })
    
    
    groups members:[dev staging]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "c": "non-prod-c",
      "d": "non-prod-d",
      "a": "dev-a",
      "b": "dev-b",
      "student": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom",
        "gender": "Male"
      },
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n",
      "school_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": false
          },
          "school": "Sydney Grammar"
        },
        "principal": "Mr Peter"
      }
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "school_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": false
          },
          "school": "Sydney Grammar"
        },
        "principal": "Mr Peter"
      },
      "c": "non-prod-c",
      "d": "non-prod-d",
      "a": "dev-a",
      "b": "dev-b",
      "student": {
        "gender": "Male",
        "address": {
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom"
      },
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "a": "dev-a",
      "b": "dev-b",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        }
      },
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n",
      "up_runtime_task_layer_number": 0,
      "school_object": {
        "principal": "Mr Peter",
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "CBD": false,
            "name": "sydney",
            "postcode": 2000
          }
        }
      },
      "c": "non-prod-c",
      "d": "non-prod-d"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "b": "dev-b",
      "student": {
        "gender": "Male",
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom"
      },
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n",
      "up_runtime_task_layer_number": 0,
      "school_object": {
        "address": {
          "suburb": {
            "postcode": 2000,
            "CBD": false,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        },
        "principal": "Mr Peter"
      },
      "c": "non-prod-c",
      "d": "non-prod-d",
      "a": "dev-a"
    })
    
    cmd( 1):
    echo """1.school -> {{.school}}"""
    
    cmd=>:
    echo """1.school -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: no
      school: Sydney Grammar
    principal: Mr Peter
    """
    -
    1.school -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: no
      school: Sydney Grammar
    principal: Mr Peter
    
    
    -
     .. ok
    cmd( 2):
    echo """2.school object-> {{.school_object.address.suburb.CBD}}"""
    
    cmd=>:
    echo """2.school object-> false"""
    -
    2.school object-> false
    
    -
     .. ok
    cmd( 3):
    echo """3.school object-> {{.school_object.address.school}}"""
    
    cmd=>:
    echo """3.school object-> Sydney Grammar"""
    -
    3.school object-> Sydney Grammar
    
    -
     .. ok
    cmd( 4):
    echo """4.school object-> {{.school_object.principal}}"""
    
    cmd=>:
    echo """4.school object-> Mr Peter"""
    -
    4.school object-> Mr Peter
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0032 log - verbose level v](../../logs/c0032_v)
* [c0032 log - verbose level vv](../../logs/c0032_vv)
* [c0032 log - verbose level vvv](../../logs/c0032_vvv)
* [c0032 log - verbose level vvvv](../../logs/c0032_vvvv)
* [c0032 log - verbose level vvvvv](../../logs/c0032_vvvvv)

##### References
* [Related Chapter](../../dvars/c0032)
