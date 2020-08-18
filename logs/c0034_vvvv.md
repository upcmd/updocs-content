---
title: "c0034_vvvv"
date: 2020-08-18T15:15:53+88:00
draft: false
weight: 10343

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0034
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
    loading [Task]:  ./tests/functests/c0034
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    nonprod: {
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      },
      "b": "non-prod-b",
      "c": "non-prod-c",
      "d": "non-prod-d",
      "a": "non-prod-a"
    }
    
    
    global: {
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      }
    }
    
    
    groups members:[dev staging]
    merged[ dev ] runtime vars:
    {
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        }
      },
      "d": "non-prod-d",
      "a": "non-prod-a",
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      },
      "b": "non-prod-b",
      "c": "non-prod-c"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "school_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      },
      "b": "non-prod-b",
      "c": "non-prod-c",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        }
      },
      "d": "non-prod-d",
      "a": "non-prod-a",
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "school_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      },
      "b": "local-b",
      "c": "non-prod-c",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        }
      },
      "d": "non-prod-d",
      "a": "local-a",
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "c": "non-prod-c",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        }
      },
      "d": "non-prod-d",
      "a": "local-a",
      "school": "address:\n  state: NSW\n  city: sydney\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: LOCAL\n  school: Sydney Grammar\nprincipal: Mr Right\n",
      "school_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar",
          "city": "sydney"
        }
      },
      "b": "local-b"
    })
    
      located task-> 2 [show_school_details]: 
    =Task2: [task ==> show_school_details:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "school_object": {
        "address": {
          "school": "Sydney Grammar",
          "city": "sydney",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          }
        }
      },
      "c": "non-prod-c",
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
      "d": "non-prod-d",
      "a": "local-a",
      "b": "local-b",
      "school": "address:\n  state: NSW\n  city: sydney\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: LOCAL\n  school: Sydney Grammar\nprincipal: Mr Right\n"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "school_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar",
          "city": "sydney"
        },
        "principal": "Mr Peter",
        "something": "ref task does not have this field"
      },
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      },
      "d": "non-prod-d",
      "a": "local-a",
      "b": "local-b",
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\nsomething: ref task does not have this field\n",
      "c": "non-prod-c",
      "class_room": "3K"
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
    something: ref task does not have this field
    """
    -
    1.school -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: no
      school: Sydney Grammar
    principal: Mr Peter
    something: ref task does not have this field
    
    -
     .. ok
    cmd( 2):
    echo """2.school object CBD -> {{.school_object.address.suburb.CBD}}"""
    
    cmd=>:
    echo """2.school object CBD -> true"""
    -
    2.school object CBD -> true
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
    cmd( 5):
    echo """5.a {{.a}}"""
    
    cmd=>:
    echo """5.a local-a"""
    -
    5.a local-a
    -
     .. ok
    cmd( 6):
    echo """6.b {{.b}}"""
    
    cmd=>:
    echo """6.b local-b"""
    -
    6.b local-b
    -
     .. ok
    cmd( 7):
    echo """7.school object-> {{.school_object|printObj}}"""
    
    {
      "something": "ref task does not have this field",
      "address": {
        "suburb": {
          "name": "sydney",
          "postcode": 2000,
          "CBD": true
        },
        "school": "Sydney Grammar",
        "city": "sydney"
      },
      "principal": "Mr Peter"
    }
    
    cmd=>:
    echo """7.school object-> {
      "principal": "Mr Peter",
      "something": "ref task does not have this field",
      "address": {
        "suburb": {
          "postcode": 2000,
          "CBD": true,
          "name": "sydney"
        },
        "school": "Sydney Grammar",
        "city": "sydney"
      }
    }
    
    """
    -
    7.school object-> {
      principal: Mr Peter,
      something: ref task does not have this field,
      address: {
        suburb: {
          postcode: 2000,
          CBD: true,
          name: sydney
        },
        school: Sydney Grammar,
        city: sydney
      }
    }
    
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0034 log - verbose level v](../../logs/c0034_v)
* [c0034 log - verbose level vv](../../logs/c0034_vv)
* [c0034 log - verbose level vvv](../../logs/c0034_vvv)
* [c0034 log - verbose level vvvv](../../logs/c0034_vvvv)
* [c0034 log - verbose level vvvvv](../../logs/c0034_vvvvv)

##### References
* [Related Chapter](../../dvars/c0034)
