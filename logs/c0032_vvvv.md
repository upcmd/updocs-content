---
title: "c0032_vvvv"
date: 2020-06-25T01:55:41+66:00
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
              ModuleName -> hopeful_yonath7
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0032
    ---------group vars----------
    
    nonprod: {
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
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
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
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          }
        }
      }
    }
    
    
    groups members:[dev staging]
    module: [hopeful_yonath7] instance id: [dev]
    merged[ dev ] runtime vars:
    {
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
      "b": "dev-b",
      "c": "non-prod-c",
      "d": "non-prod-d",
      "a": "dev-a",
      "school_object": {
        "principal": "Mr Peter",
        "address": {
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        }
      },
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n"
    }
    
    -------runtime global final merged with dvars-------
    
    {
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
      "b": "dev-b",
      "c": "non-prod-c",
      "d": "non-prod-d",
      "a": "dev-a",
      "school_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        },
        "principal": "Mr Peter"
      },
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"\"\"1.school -> {{.school}}\"\"\"",
        "echo \"\"\"2.school object-> {{.school_object.address.suburb.CBD}}\"\"\"",
        "echo \"\"\"3.school object-> {{.school_object.address.school}}\"\"\"",
        "echo \"\"\"4.school object-> {{.school_object.principal}}\"\"\""
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
      "b": "dev-b",
      "c": "non-prod-c",
      "d": "non-prod-d",
      "a": "dev-a",
      "school_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        },
        "principal": "Mr Peter"
      },
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n",
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
      }
    })
    
    hopeful_yonath7: overall final exec vars:
    
    (*core.Cache)({
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n",
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
      "b": "dev-b",
      "c": "non-prod-c",
      "d": "non-prod-d",
      "a": "dev-a",
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
      }
    })
    
    cmd( 1):
    echo """1.school -> {{.school}}"""
    
     \_ echo """1.school -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: no
      school: Sydney Grammar
    principal: Mr Peter
    """
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
    
     \_ echo """2.school object-> true"""
    2.school object-> true
     .. ok
    cmd( 3):
    echo """3.school object-> {{.school_object.address.school}}"""
    
     \_ echo """3.school object-> Sydney Grammar"""
    3.school object-> Sydney Grammar
     .. ok
    cmd( 4):
    echo """4.school object-> {{.school_object.principal}}"""
    
     \_ echo """4.school object-> Mr Peter"""
    4.school object-> Mr Peter
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