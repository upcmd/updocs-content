---
title: "c0038_vvvv"
date: 2020-10-07T00:11:07+1010:00
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
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
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
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
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
      "ha": true
    })
    
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
    
    (*core.Cache)({
      "gtf_ljust": "Hello!              ",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "old": 54,
      "sprig_trim": "hello",
      "gtf_url_encoding": "http%3A%2F%2Fwww.example.org%2Ffoo%3Fa%3Db%26c%3Dd",
      "ns": "prod",
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
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          },
          "school": "Sydney Grammar"
        }
      },
      "var_slice_index": "jason",
      "pod_name": "web_app",
      "ha": true,
      "age": 34
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "pod_name": "web_app",
      "old": 54,
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "gtf_ljust": "Hello!              ",
      "sprig_trim": "hello",
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
            "cbd": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        }
      },
      "up_runtime_task_layer_number": 0,
      "gtf_url_encoding": "http%3A%2F%2Fwww.example.org%2Ffoo%3Fa%3Db%26c%3Dd",
      "age": 34,
      "ha": true,
      "var_slice_index": "jason",
      "ns": "prod",
      "managers": {
        "tom",
        "jason",
        "alice"
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "var_slice_index": "jason",
      "gtf_ljust": "Hello!              ",
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
      "up_runtime_task_layer_number": 0,
      "age": 34,
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "old": 54,
      "ns": "prod",
      "gtf_url_encoding": "http%3A%2F%2Fwww.example.org%2Ffoo%3Fa%3Db%26c%3Dd",
      "ha": true,
      "sprig_trim": "hello",
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
