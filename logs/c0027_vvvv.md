---
title: "c0027_vvvv"
date: 2020-07-20T02:01:33+77:00
draft: false
weight: 10273

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0027
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0027
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
      "tom": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "a_smart_guy": "name: Tom\ngender: Male\nschool: Sydney Grammar\n",
      "a_smart_guy_object": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "postcode": 2000,
            "cbd": true,
            "name": "sydney"
          }
        }
      },
      "school_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n  tom:\n    name: Tom\n",
      "school_address_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar",
          "tom": {
            "name": "Tom"
          }
        }
      }
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "a_smart_guy_object": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "postcode": 2000,
            "cbd": true,
            "name": "sydney"
          }
        }
      },
      "school_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n  tom:\n    name: Tom\n",
      "school_address_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar",
          "tom": {
            "name": "Tom"
          }
        }
      },
      "tom": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "a_smart_guy": "name: Tom\ngender: Male\nschool: Sydney Grammar\n"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "school_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n  tom:\n    name: Tom\n",
      "school_address_object": {
        "address": {
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar",
          "tom": {
            "name": "Tom"
          }
        }
      },
      "tom": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "a_smart_guy": "name: Tom\ngender: Male\nschool: Sydney Grammar\n",
      "a_smart_guy_object": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "postcode": 2000,
            "cbd": true,
            "name": "sydney"
          }
        }
      }
    })
    
    cmd( 1):
    echo """a smart guy=>{{.a_smart_guy}}"""
    
    cmd=>:
    echo """a smart guy=>name: Tom
    gender: Male
    school: Sydney Grammar
    """<=
    a smart guy=>name: Tom
    gender: Male
    school: Sydney Grammar
     .. ok
    cmd( 2):
    echo """postcode=>{{.student.address.suburb.postcode}}"""
    
    cmd=>:
    echo """postcode=>2000"""<=
    postcode=>2000
     .. ok
    cmd( 3):
    echo """school address {{.school_address}}"""
    
    cmd=>:
    echo """school address address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
      tom:
        name: Tom
    """<=
    school address address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
      tom:
        name: Tom
     .. ok
    cmd( 4):
    echo """this guy is in =>{{.a_smart_guy_object.school}} school"""
    
    cmd=>:
    echo """this guy is in =>Sydney Grammar school"""<=
    this guy is in =>Sydney Grammar school
     .. ok
    cmd( 5):
    echo """school address object {{.school_address_object.suburb.name}}"""
    
    cmd=>:
    echo """school address object <no value>"""<=
    school address object <no value>
     .. ok
    cmd( 6):
    echo """school address object -> {{.school_address_object.address.suburb.name}}"""
    
    cmd=>:
    echo """school address object -> sydney"""<=
    school address object -> sydney
     .. ok
    . ok
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"\"\"school address object -> sydney\"\"\"",
        Code: 0,
        Output: "school address object -> sydney",
        ErrMsg: ""
      }),
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "postcode": 2000,
            "cbd": true,
            "name": "sydney"
          }
        }
      },
      "school_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n  tom:\n    name: Tom\n",
      "school_address_object": {
        "address": {
          "tom": {
            "name": "Tom"
          },
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        }
      },
      "tom": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "a_smart_guy": "name: Tom\ngender: Male\nschool: Sydney Grammar\n",
      "a_smart_guy_object": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "school_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n  tom:\n    name: Tom\n",
      "school_address_object": {
        "address": {
          "school": "Sydney Grammar",
          "tom": {
            "name": "Tom"
          },
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          }
        }
      },
      "tom": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "a_smart_guy": "name: Tom\ngender: Male\nschool: Sydney Grammar\n",
      "a_smart_guy_object": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"\"\"school address object -> sydney\"\"\"",
        Code: 0,
        Output: "school address object -> sydney",
        ErrMsg: ""
      }),
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "cbd": true,
            "name": "sydney",
            "postcode": 2000
          }
        }
      }
    })
    
    cmd( 1):
    echo hello
    
    cmd=>:
    echo hello<=
    hello
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0027 log - verbose level v](../../logs/c0027_v)
* [c0027 log - verbose level vv](../../logs/c0027_vv)
* [c0027 log - verbose level vvv](../../logs/c0027_vvv)
* [c0027 log - verbose level vvvv](../../logs/c0027_vvvv)
* [c0027 log - verbose level vvvvv](../../logs/c0027_vvvvv)

##### References
* [Related Chapter](../../dvars/c0027)
