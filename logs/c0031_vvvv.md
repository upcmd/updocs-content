---
title: "c0031_vvvv"
date: 2020-07-20T02:01:34+77:00
draft: false
weight: 10313

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0031
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0031
    ---------group vars----------
    
    nonprod: {
      "b": "non-prod-b",
      "c": "non-prod-c",
      "d": "non-prod-d",
      "a": "non-prod-a",
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
    }
    
    
    global: {
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
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n"
    }
    
    
    groups members:[dev staging]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [self] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "a": "dev-a",
      "b": "dev-b",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          }
        }
      },
      "school_object": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          }
        },
        "principal": "Mr Peter"
      },
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n",
      "c": "non-prod-c",
      "d": "non-prod-d"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          }
        }
      },
      "school_object": {
        "address": {
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        },
        "principal": "Mr Peter"
      },
      "c": "non-prod-c",
      "sgp_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n",
      "d": "non-prod-d",
      "a": "dev-a",
      "b": "dev-b",
      "sgp_address_object": {
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
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "sgp_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "d": "non-prod-d",
      "b": "dev-b",
      "school_object": {
        "address": {
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        },
        "principal": "Mr Peter"
      },
      "c": "non-prod-c",
      "a": "dev-a",
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
      "student": {
        "address": {
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom",
        "gender": "Male"
      },
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "school_object": {
        "address": {
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        },
        "principal": "Mr Peter"
      },
      "c": "non-prod-c",
      "sgp_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "d": "non-prod-d",
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
      "a": "dev-a",
      "sgp_address_object": {
        "address": {
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        }
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
    """<=
    1.school -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: no
      school: Sydney Grammar
    principal: Mr Peter
     .. ok
    cmd( 2):
    echo """2.school object-> {{.school_object.address.suburb.CBD}}"""
    
    cmd=>:
    echo """2.school object-> true"""<=
    2.school object-> true
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
    . ok
    
```

##### Logs with different verbose level
* [c0031 log - verbose level v](../../logs/c0031_v)
* [c0031 log - verbose level vv](../../logs/c0031_vv)
* [c0031 log - verbose level vvv](../../logs/c0031_vvv)
* [c0031 log - verbose level vvvv](../../logs/c0031_vvvv)
* [c0031 log - verbose level vvvvv](../../logs/c0031_vvvvv)

##### References
* [Related Chapter](../../dvars/c0031)
