---
title: "c0033_vvvv"
date: 2020-06-25T01:55:42+66:00
draft: false
weight: 10333

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0033
                 Verbose -> vvvv
              ModuleName -> desperate_bartik1
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0033
    ---------group vars----------
    
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
    
    
    nonprod: {
      "c": "non-prod-c",
      "d": "non-prod-d",
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
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "a": "non-prod-a",
      "b": "non-prod-b"
    }
    
    
    groups members:[dev staging]
    module: [desperate_bartik1] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "a": "dev-a",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          }
        }
      },
      "b": "dev-b",
      "c": "non-prod-c",
      "d": "non-prod-d",
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
    
    -------runtime global final merged with dvars-------
    
    {
      "c": "non-prod-c",
      "d": "non-prod-d",
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
      "a": "dev-a",
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
      "b": "dev-b"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"\"\"1.school -> {{.school}}\"\"\"",
        "echo \"\"\"2.school object CBD -> {{.school_object.address.suburb.CBD}}\"\"\"",
        "echo \"\"\"3.school object-> {{.school_object.address.school}}\"\"\"",
        "echo \"\"\"4.school object-> {{.school_object.principal}}\"\"\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "a": "local-a",
        "b": "local-b"
      },
      Dvars: {
        {
          Name: "school",
          Value: "address:\n  state: NSW\n  city: sydney\n  suburb:\n    name: {{.student.address.suburb.name}}\n    postcode: 2000\n    CBD: LOCAL\n  school: {{.student.address.school}}\nprincipal: Mr Right\n",
          Desc: "",
          Expand: 0,
          Flags: {
            "to_object"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
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
      "student": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          }
        },
        "name": "Tom",
        "gender": "Male"
      },
      "b": "local-b",
      "c": "non-prod-c",
      "d": "non-prod-d",
      "school_object": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          }
        },
        "principal": "Mr Peter"
      },
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n",
      "a": "local-a"
    })
    
    desperate_bartik1: overall final exec vars:
    
    (*core.Cache)({
      "b": "local-b",
      "c": "non-prod-c",
      "d": "non-prod-d",
      "school_object": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "state": "NSW",
          "city": "sydney"
        },
        "principal": "Mr Peter"
      },
      "school": "address:\n  state: NSW\n  city: sydney\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: LOCAL\n  school: Sydney Grammar\nprincipal: Mr Right\n",
      "a": "local-a",
      "student": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          }
        },
        "name": "Tom",
        "gender": "Male"
      }
    })
    
    cmd( 1):
    echo """1.school -> {{.school}}"""
    
     \_ echo """1.school -> address:
      state: NSW
      city: sydney
      suburb:
        name: sydney
        postcode: 2000
        CBD: LOCAL
      school: Sydney Grammar
    principal: Mr Right
    """
    1.school -> address:
      state: NSW
      city: sydney
      suburb:
        name: sydney
        postcode: 2000
        CBD: LOCAL
      school: Sydney Grammar
    principal: Mr Right
     .. ok
    cmd( 2):
    echo """2.school object CBD -> {{.school_object.address.suburb.CBD}}"""
    
     \_ echo """2.school object CBD -> true"""
    2.school object CBD -> true
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
* [c0033 log - verbose level v](../../logs/c0033_v)
* [c0033 log - verbose level vv](../../logs/c0033_vv)
* [c0033 log - verbose level vvv](../../logs/c0033_vvv)
* [c0033 log - verbose level vvvv](../../logs/c0033_vvvv)
* [c0033 log - verbose level vvvvv](../../logs/c0033_vvvvv)

##### References
* [Related Chapter](../../dvars/c0033)