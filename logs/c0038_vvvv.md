---
title: "c0038_vvvv"
date: 2020-08-09T01:36:04+88:00
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
      },
      "student": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
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
      "ns": "prod",
      "pod_name": "web_app"
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
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_trim": "hello",
      "age": 34,
      "old": 54,
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "student": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "postcode": 2000,
            "cbd": true,
            "name": "sydney"
          }
        },
        "name": "Tom",
        "gender": "Male",
        "teachers": {
          "tom",
          "jason",
          "alice"
        }
      },
      "var_slice_index": "jason",
      "ns": "prod",
      "pod_name": "web_app",
      "ha": true,
      "gtf_url_encoding": "http%3A%2F%2Fwww.example.org%2Ffoo%3Fa%3Db%26c%3Dd",
      "gtf_ljust": "Hello!              "
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "managers": {
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
            "postcode": 2000,
            "cbd": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        }
      },
      "ns": "prod",
      "pod_name": "web_app",
      "ha": true,
      "old": 54,
      "gtf_url_encoding": "http%3A%2F%2Fwww.example.org%2Ffoo%3Fa%3Db%26c%3Dd",
      "gtf_ljust": "Hello!              ",
      "sprig_trim": "hello",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "var_slice_index": "jason",
      "age": 34
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "sprig_trim": "hello",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "var_slice_index": "jason",
      "age": 34,
      "gtf_url_encoding": "http%3A%2F%2Fwww.example.org%2Ffoo%3Fa%3Db%26c%3Dd",
      "gtf_ljust": "Hello!              ",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "student": {
        "gender": "Male",
        "teachers": {
          "tom",
          "jason",
          "alice"
        },
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "postcode": 2000,
            "cbd": true,
            "name": "sydney"
          }
        },
        "name": "Tom"
      },
      "ns": "prod",
      "pod_name": "web_app",
      "ha": true,
      "old": 54
    })
    
    cmd( 1):
    echo "check the value of other dvar using vvvv flag print out"
    
    cmd=>:
    echo "check the value of other dvar using vvvv flag print out"<=
    check the value of other dvar using vvvv flag print out
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
