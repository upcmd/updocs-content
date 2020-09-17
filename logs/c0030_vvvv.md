---
title: "c0030_vvvv"
date: 2020-09-18T01:27:25+99:00
draft: false
weight: 10303

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0030
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0030
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    nonprod: {
      "c": "non-prod-c",
      "d": "non-prod-d",
      "a": "non-prod-a",
      "b": "non-prod-b",
      "school_nonprod": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_nonprod_object": {
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
    
    
    prod: {
      "a": "prod-a",
      "b": "prod-b",
      "c": "prod-c",
      "d": "prod-d",
      "school_prod": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_prod_object": {
        "address": {
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        }
      }
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
      },
      "school_global": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_global_object": {
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
    
    
    groups members:[dev staging prod]
    merged[ dev ] runtime vars:
    {
      "school_global": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_global_object": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          }
        }
      },
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
      "b": "non-prod-b",
      "school_nonprod_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      },
      "c": "non-prod-c",
      "a": "non-prod-a",
      "school_nonprod": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "d": "non-prod-d"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "student": {
        "gender": "Male",
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          }
        },
        "name": "Tom"
      },
      "b": "non-prod-b",
      "school_nonprod_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      },
      "c": "non-prod-c",
      "school_global": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_global_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      },
      "sgp_address_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      },
      "school_nonprod": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "d": "non-prod-d",
      "a": "non-prod-a",
      "sgp_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "sgp_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "sgp_address_object": {
        "address": {
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        }
      },
      "student": {
        "gender": "Male",
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          }
        },
        "name": "Tom"
      },
      "school_nonprod_object": {
        "address": {
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        }
      },
      "c": "non-prod-c",
      "school_nonprod": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "d": "non-prod-d",
      "a": "non-prod-a",
      "up_runtime_task_layer_number": 0,
      "school_global_object": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          }
        }
      },
      "b": "non-prod-b",
      "school_global": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "school_global_object": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          }
        }
      },
      "b": "non-prod-b",
      "school_global": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
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
      "school_nonprod_object": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          }
        }
      },
      "c": "non-prod-c",
      "school_nonprod": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "d": "non-prod-d",
      "a": "non-prod-a",
      "sgp_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "sgp_address_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      },
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo """1.school_global -> {{.school_global}}""" - echo """2.school_global object -> {{.school_global_object.address.suburb.name}}"""
    
    cmd=>:
    echo """1.school_global -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
    """ - echo """2.school_global object -> sydney"""
    -
    1.school_global -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
     - echo 2.school_global object -> sydney
    
    -
     .. ok
    cmd( 2):
    echo """3.school_nonprod -> {{.school_nonprod}}"""
    
    cmd=>:
    echo """3.school_nonprod -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
    """
    -
    3.school_nonprod -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
    
    
    -
     .. ok
    cmd( 3):
    echo """4.school_nonprod object -> {{.school_nonprod_object.address.suburb.name}}"""
    
    cmd=>:
    echo """4.school_nonprod object -> sydney"""
    -
    4.school_nonprod object -> sydney
    
    -
     .. ok
    cmd( 4):
    echo """5.sgp address -> {{.sgp_address}}"""
    
    cmd=>:
    echo """5.sgp address -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
    """
    -
    5.sgp address -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
    
    
    -
     .. ok
    cmd( 5):
    echo """6.sgp address object -> {{.sgp_address_object.address.suburb.name}}"""
    
    cmd=>:
    echo """6.sgp address object -> sydney"""
    -
    6.sgp address object -> sydney
    
    -
     .. ok
    cmd( 6):
    echo """7.school_prod -> {{.school_prod}}"""
    
    cmd=>:
    echo """7.school_prod -> <no value>"""
    -
    7.school_prod -> <no value>
    
    -
     .. ok
    cmd( 7):
    echo """8.school_prod object -> {{.school_prod_object.address.suburb.name}}"""
    
    cmd=>:
    echo """8.school_prod object -> <no value>"""
    -
    8.school_prod object -> <no value>
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0030 log - verbose level v](../../logs/c0030_v)
* [c0030 log - verbose level vv](../../logs/c0030_vv)
* [c0030 log - verbose level vvv](../../logs/c0030_vvv)
* [c0030 log - verbose level vvvv](../../logs/c0030_vvvv)
* [c0030 log - verbose level vvvvv](../../logs/c0030_vvvvv)

##### References
* [Related Chapter](../../dvars/c0030)
