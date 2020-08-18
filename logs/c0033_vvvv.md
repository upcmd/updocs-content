---
title: "c0033_vvvv"
date: 2020-08-18T15:15:53+88:00
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
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0033
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    nonprod: {
      "a": "non-prod-a",
      "b": "non-prod-b",
      "c": "non-prod-c",
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
      "d": "non-prod-d"
    }
    
    
    global: {
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
      }
    }
    
    
    groups members:[dev staging]
    merged[ dev ] runtime vars:
    {
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n",
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
      "a": "dev-a",
      "b": "dev-b",
      "c": "non-prod-c"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "c": "non-prod-c",
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n",
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
      "a": "dev-a",
      "b": "dev-b"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "c": "non-prod-c",
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n",
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
      "b": "local-b"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "school": "address:\n  state: NSW\n  city: sydney\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: LOCAL\n  school: Sydney Grammar\nprincipal: Mr Right\n",
      "school_object": {
        "address": {
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar",
          "state": "NSW",
          "city": "sydney"
        },
        "principal": "Mr Peter"
      },
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
      "c": "non-prod-c"
    })
    
    cmd( 1):
    echo """1.school -> {{.school}}"""
    
    cmd=>:
    echo """1.school -> address:
      state: NSW
      city: sydney
      suburb:
        name: sydney
        postcode: 2000
        CBD: LOCAL
      school: Sydney Grammar
    principal: Mr Right
    """
    -
    1.school -> address:
      state: NSW
      city: sydney
      suburb:
        name: sydney
        postcode: 2000
        CBD: LOCAL
      school: Sydney Grammar
    principal: Mr Right
    
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
