---
title: "c0034_vvvv"
date: 2020-07-20T02:01:35+77:00
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
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0034
    ---------group vars----------
    
    global: {
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
      }
    }
    
    
    nonprod: {
      "a": "non-prod-a",
      "b": "non-prod-b",
      "c": "non-prod-c",
      "d": "non-prod-d",
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_object": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          }
        }
      }
    }
    
    
    groups members:[dev staging]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [self] instance id: [dev]
    merged[ dev ] runtime vars:
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
      "a": "non-prod-a",
      "b": "non-prod-b",
      "c": "non-prod-c",
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
      "d": "non-prod-d",
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "c": "non-prod-c",
      "student": {
        "address": {
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom",
        "gender": "Male"
      },
      "d": "non-prod-d",
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_object": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          }
        }
      },
      "a": "non-prod-a",
      "b": "non-prod-b"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "d": "non-prod-d",
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_object": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          }
        }
      },
      "a": "local-a",
      "b": "local-b",
      "c": "non-prod-c",
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
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "c": "non-prod-c",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          }
        }
      },
      "d": "non-prod-d",
      "school": "address:\n  state: NSW\n  city: sydney\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: LOCAL\n  school: Sydney Grammar\nprincipal: Mr Right\n",
      "school_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar",
          "state": "NSW",
          "city": "sydney"
        }
      },
      "a": "local-a",
      "b": "local-b"
    })
    
      located task-> 2 [show_school_details]: 
    =Task2: [task ==> show_school_details:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "c": "non-prod-c",
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
      "a": "local-a",
      "b": "local-b",
      "d": "non-prod-d",
      "school": "address:\n  state: NSW\n  city: sydney\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: LOCAL\n  school: Sydney Grammar\nprincipal: Mr Right\n",
      "school_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar",
          "state": "NSW",
          "city": "sydney"
        }
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "b": "local-b",
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\nsomething: ref task does not have this field\n",
      "school_object": {
        "address": {
          "school": "Sydney Grammar",
          "state": "NSW",
          "city": "sydney",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          }
        },
        "principal": "Mr Peter",
        "something": "ref task does not have this field"
      },
      "class_room": "3K",
      "a": "local-a",
      "d": "non-prod-d",
      "up_runtime_task_layer_number": 1,
      "c": "non-prod-c",
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
      }
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
    """<=
    1.school -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: no
      school: Sydney Grammar
    principal: Mr Peter
    something: ref task does not have this field
     .. ok
    cmd( 2):
    echo """2.school object CBD -> {{.school_object.address.suburb.CBD}}"""
    
    cmd=>:
    echo """2.school object CBD -> true"""<=
    2.school object CBD -> true
     .. ok
    cmd( 3):
    echo """3.school object-> {{.school_object.address.school}}"""
    
    cmd=>:
    echo """3.school object-> Sydney Grammar"""<=
    3.school object-> Sydney Grammar
     .. ok
    cmd( 4):
    echo """4.school object-> {{.school_object.principal}}"""
    
    cmd=>:
    echo """4.school object-> Mr Peter"""<=
    4.school object-> Mr Peter
     .. ok
    cmd( 5):
    echo """5.a {{.a}}"""
    
    cmd=>:
    echo """5.a local-a"""<=
    5.a local-a
     .. ok
    cmd( 6):
    echo """6.b {{.b}}"""
    
    cmd=>:
    echo """6.b local-b"""<=
    6.b local-b
     .. ok
    cmd( 7):
    echo """7.school object-> {{.school_object|printObj}}"""
    
    {
      "address": {
        "city": "sydney",
        "suburb": {
          "name": "sydney",
          "postcode": 2000,
          "CBD": true
        },
        "school": "Sydney Grammar",
        "state": "NSW"
      },
      "principal": "Mr Peter",
      "something": "ref task does not have this field"
    }
    
    cmd=>:
    echo """7.school object-> {
      "address": {
        "suburb": {
          "CBD": true,
          "name": "sydney",
          "postcode": 2000
        },
        "school": "Sydney Grammar",
        "state": "NSW",
        "city": "sydney"
      },
      "principal": "Mr Peter",
      "something": "ref task does not have this field"
    }
    
    """<=
    7.school object-> {
      address: {
        suburb: {
          CBD: true,
          name: sydney,
          postcode: 2000
        },
        school: Sydney Grammar,
        state: NSW,
        city: sydney
      },
      principal: Mr Peter,
      something: ref task does not have this field
    }
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
