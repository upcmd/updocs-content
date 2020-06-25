---
title: "c0030_vvvv"
date: 2020-06-25T01:55:41+66:00
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
              ModuleName -> cranky_davinci1
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0030
    ---------group vars----------
    
    nonprod: {
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
      "a": "non-prod-a",
      "b": "non-prod-b",
      "c": "non-prod-c",
      "d": "non-prod-d",
      "school_nonprod": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n"
    }
    
    
    prod: {
      "c": "prod-c",
      "d": "prod-d",
      "a": "prod-a",
      "b": "prod-b",
      "school_prod": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_prod_object": {
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
    module: [cranky_davinci1] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "school_global_object": {
        "address": {
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        }
      },
      "school_nonprod": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "a": "non-prod-a",
      "b": "non-prod-b",
      "d": "non-prod-d",
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
      "school_global": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
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
      "c": "non-prod-c"
    }
    
    -------runtime global final merged with dvars-------
    
    {
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
      "school_global": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "a": "non-prod-a",
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
      "school_nonprod": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "b": "non-prod-b",
      "d": "non-prod-d"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"\"\"1.school_global -> {{.school_global}}\"\"\" - echo \"\"\"2.school_global object -> {{.school_global_object.address.suburb.name}}\"\"\"",
        "echo \"\"\"3.school_nonprod -> {{.school_nonprod}}\"\"\"",
        "echo \"\"\"4.school_nonprod object -> {{.school_nonprod_object.address.suburb.name}}\"\"\"",
        "echo \"\"\"5.sgp address -> {{.sgp_address}}\"\"\"",
        "echo \"\"\"6.sgp address object -> {{.sgp_address_object.address.suburb.name}}\"\"\"",
        "echo \"\"\"7.school_prod -> {{.school_prod}}\"\"\"",
        "echo \"\"\"8.school_prod object -> {{.school_prod_object.address.suburb.name}}\"\"\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "a": "non-prod-a",
      "school_nonprod_object": {
        "address": {
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        }
      },
      "sgp_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "c": "non-prod-c",
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
      "d": "non-prod-d",
      "school_global": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
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
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom",
        "gender": "Male"
      },
      "school_nonprod": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "b": "non-prod-b"
    })
    
    cranky_davinci1: overall final exec vars:
    
    (*core.Cache)({
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
      "school_nonprod": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "b": "non-prod-b",
      "d": "non-prod-d",
      "a": "non-prod-a",
      "sgp_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_global": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
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
      "school_global_object": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          }
        }
      }
    })
    
    cmd( 1):
    echo """1.school_global -> {{.school_global}}""" - echo """2.school_global object -> {{.school_global_object.address.suburb.name}}"""
    
     \_ echo """1.school_global -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
    """ - echo """2.school_global object -> sydney"""
    1.school_global -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
     - echo 2.school_global object -> sydney
     .. ok
    cmd( 2):
    echo """3.school_nonprod -> {{.school_nonprod}}"""
    
     \_ echo """3.school_nonprod -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
    """
    3.school_nonprod -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
     .. ok
    cmd( 3):
    echo """4.school_nonprod object -> {{.school_nonprod_object.address.suburb.name}}"""
    
     \_ echo """4.school_nonprod object -> sydney"""
    4.school_nonprod object -> sydney
     .. ok
    cmd( 4):
    echo """5.sgp address -> {{.sgp_address}}"""
    
     \_ echo """5.sgp address -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
    """
    5.sgp address -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
     .. ok
    cmd( 5):
    echo """6.sgp address object -> {{.sgp_address_object.address.suburb.name}}"""
    
     \_ echo """6.sgp address object -> sydney"""
    6.sgp address object -> sydney
     .. ok
    cmd( 6):
    echo """7.school_prod -> {{.school_prod}}"""
    
     \_ echo """7.school_prod -> <no value>"""
    7.school_prod -> <no value>
     .. ok
    cmd( 7):
    echo """8.school_prod object -> {{.school_prod_object.address.suburb.name}}"""
    
     \_ echo """8.school_prod object -> <no value>"""
    8.school_prod object -> <no value>
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