---
title: "c0038_vvvv"
date: 2020-07-01T15:34:26+77:00
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
              ModuleName -> fervent_mcclintock9
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
    module: [fervent_mcclintock9] instance id: [dev]
    merged[ dev ] runtime vars:
    {
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
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          }
        }
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
      "ns": "prod",
      "pod_name": "web_app",
      "student": {
        "teachers": {
          "tom",
          "jason",
          "alice"
        },
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          }
        },
        "name": "Tom",
        "gender": "Male"
      },
      "sprig_trim": "hello",
      "gtf_ljust": "Hello!              ",
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
      "var_slice_index": "jason",
      "gtf_url_encoding": "http%3A%2F%2Fwww.example.org%2Ffoo%3Fa%3Db%26c%3Dd"
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
      "admins": {
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
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "var_slice_index": "jason",
      "gtf_url_encoding": "http%3A%2F%2Fwww.example.org%2Ffoo%3Fa%3Db%26c%3Dd",
      "age": 34,
      "old": 54,
      "gtf_ljust": "Hello!              ",
      "ns": "prod",
      "pod_name": "web_app",
      "sprig_trim": "hello",
      "ha": true
    })
    
    fervent_mcclintock9: overall final exec vars:
    
    (*core.Cache)({
      "ha": true,
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "var_slice_index": "jason",
      "age": 34,
      "gtf_ljust": "Hello!              ",
      "pod_name": "web_app",
      "sprig_trim": "hello",
      "gtf_url_encoding": "http%3A%2F%2Fwww.example.org%2Ffoo%3Fa%3Db%26c%3Dd",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "ns": "prod",
      "old": 54,
      "student": {
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
        "name": "Tom",
        "gender": "Male"
      }
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
