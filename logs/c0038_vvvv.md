---
title: "c0038_vvvv"
date: 2020-08-18T15:15:54+88:00
draft: false
weight: 10383

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0038
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
    loading [Task]:  ./tests/functests/c0038
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "student": {
        "name": "Tom",
        "gender": "Male",
        "teachers": {
          "tom",
          "jason",
          "alice"
        },
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          },
          "school": "Sydney Grammar"
        }
      },
      "ns": "prod",
      "pod_name": "web_app",
      "ha": true,
      "age": 34,
      "old": 54,
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "managers": {
        "tom",
        "jason",
        "alice"
      }
    }
    
    dvar> sprig_trim:
    "hello"
    
    -
    hello
    dvar> var_slice_index:
    "jason"
    
    -
    jason
    dvar> gtf_url_encoding:
    "http%3A%2F%2Fwww.example.org%2Ffoo%3Fa%3Db%26c%3Dd"
    
    -
    http%3A%2F%2Fwww.example.org%2Ffoo%3Fa%3Db%26c%3Dd
    dvar> gtf_ljust:
    "Hello!              "
    
    -
    Hello!              
    -------runtime global final merged with dvars-------
    
    {
      "ha": true,
      "var_slice_index": "jason",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "old": 54,
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "student": {
        "teachers": {
          "tom",
          "jason",
          "alice"
        },
        "address": {
          "suburb": {
            "postcode": 2000,
            "cbd": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom",
        "gender": "Male"
      },
      "ns": "prod",
      "pod_name": "web_app",
      "gtf_url_encoding": "http%3A%2F%2Fwww.example.org%2Ffoo%3Fa%3Db%26c%3Dd",
      "gtf_ljust": "Hello!              ",
      "age": 34,
      "sprig_trim": "hello"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "ns": "prod",
      "pod_name": "web_app",
      "gtf_url_encoding": "http%3A%2F%2Fwww.example.org%2Ffoo%3Fa%3Db%26c%3Dd",
      "ha": true,
      "gtf_ljust": "Hello!              ",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "student": {
        "name": "Tom",
        "gender": "Male",
        "teachers": {
          "tom",
          "jason",
          "alice"
        },
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          },
          "school": "Sydney Grammar"
        }
      },
      "sprig_trim": "hello",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "var_slice_index": "jason",
      "age": 34,
      "old": 54
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "var_slice_index": "jason",
      "age": 34,
      "old": 54,
      "student": {
        "address": {
          "suburb": {
            "postcode": 2000,
            "cbd": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom",
        "gender": "Male",
        "teachers": {
          "tom",
          "jason",
          "alice"
        }
      },
      "sprig_trim": "hello",
      "gtf_url_encoding": "http%3A%2F%2Fwww.example.org%2Ffoo%3Fa%3Db%26c%3Dd",
      "ha": true,
      "gtf_ljust": "Hello!              ",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "ns": "prod",
      "pod_name": "web_app"
    })
    
    cmd( 1):
    echo "check the value of other dvar using vvvv flag print out"
    
    cmd=>:
    echo "check the value of other dvar using vvvv flag print out"
    -
    check the value of other dvar using vvvv flag print out
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0038 log - verbose level v](../../logs/c0038_v)
* [c0038 log - verbose level vv](../../logs/c0038_vv)
* [c0038 log - verbose level vvv](../../logs/c0038_vvv)
* [c0038 log - verbose level vvvv](../../logs/c0038_vvvv)
* [c0038 log - verbose level vvvvv](../../logs/c0038_vvvvv)

##### References
* [Related Chapter](../../template/c0038)
