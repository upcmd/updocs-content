---
title: "c0038_vvvv"
date: 2020-06-25T01:55:43+66:00
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
              ModuleName -> suspicious_wozniak8
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0038
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [suspicious_wozniak8] instance id: [dev]
    merged[ dev ] runtime vars:
    {
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
      "age": 34,
      "old": 54,
      "admins": {
        "tom",
        "jason",
        "alice"
      }
    }
    
    dvar> sprig_trim:
    "hello"
    
    dvar> var_slice_index:
    "jason"
    
    dvar> gtf_url_encoding:
    "http%3A%2F%2Fwww.example.org%2Ffoo%3Fa%3Db%26c%3Dd"
    
    dvar> gtf_ljust:
    "Hello!              "
    
    -------runtime global final merged with dvars-------
    
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
      "var_slice_index": "jason",
      "sprig_trim": "hello",
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
      "ns": "prod",
      "pod_name": "web_app",
      "gtf_url_encoding": "http%3A%2F%2Fwww.example.org%2Ffoo%3Fa%3Db%26c%3Dd",
      "gtf_ljust": "Hello!              ",
      "ha": true
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"check the value of other dvar using vvvv flag print out\""
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
      "age": 34,
      "var_slice_index": "jason",
      "ns": "prod",
      "pod_name": "web_app",
      "gtf_ljust": "Hello!              ",
      "old": 54,
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
      "sprig_trim": "hello",
      "gtf_url_encoding": "http%3A%2F%2Fwww.example.org%2Ffoo%3Fa%3Db%26c%3Dd",
      "ha": true,
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
    })
    
    suspicious_wozniak8: overall final exec vars:
    
    (*core.Cache)({
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
      "sprig_trim": "hello",
      "old": 54,
      "age": 34,
      "var_slice_index": "jason",
      "pod_name": "web_app",
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
      "gtf_ljust": "Hello!              ",
      "ns": "prod",
      "gtf_url_encoding": "http%3A%2F%2Fwww.example.org%2Ffoo%3Fa%3Db%26c%3Dd",
      "ha": true
    })
    
    cmd( 1):
    echo "check the value of other dvar using vvvv flag print out"
    
     \_ echo "check the value of other dvar using vvvv flag print out"
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
