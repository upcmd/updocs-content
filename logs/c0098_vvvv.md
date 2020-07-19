---
title: "c0098_vvvv"
date: 2020-07-20T02:01:46+77:00
draft: false
weight: 10983

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0098
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0098
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
      "aaa": "aaa",
      "datapointer": "student",
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "nsw": {
        "sydney": {
          "sgschool": {
            "student": {
              "gender": "Male",
              "school": "Sydney Grammar",
              "name": "Tom"
            }
          }
        }
      }
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "nsw": {
        "sydney": {
          "sgschool": {
            "student": {
              "name": "Tom",
              "gender": "Male",
              "school": "Sydney Grammar"
            }
          }
        }
      },
      "aaa": "aaa",
      "datapointer": "student",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: use sub element of an var as context to render values ]
    current exec runtime vars:
    (*core.Cache)({
      "datapointer": "student",
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "nsw": {
        "sydney": {
          "sgschool": {
            "student": {
              "gender": "Male",
              "school": "Sydney Grammar",
              "name": "Tom"
            }
          }
        }
      },
      "aaa": "aaa"
    })
    
    dvar> student_info:
    "my name is:<no value> and I am in <no value>"
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "nsw": {
        "sydney": {
          "sgschool": {
            "student": {
              "gender": "Male",
              "school": "Sydney Grammar",
              "name": "Tom"
            }
          }
        }
      },
      "aaa": "aaa",
      "datapointer": "student",
      "student_info": "my name is:<no value> and I am in <no value>"
    })
    
    ~SubStep1: [print:  ]
    my name is:<no value> and I am in <no value>
    
```

##### Logs with different verbose level
* [c0098 log - verbose level v](../../logs/c0098_v)
* [c0098 log - verbose level vv](../../logs/c0098_vv)
* [c0098 log - verbose level vvv](../../logs/c0098_vvv)
* [c0098 log - verbose level vvvv](../../logs/c0098_vvvv)
* [c0098 log - verbose level vvvvv](../../logs/c0098_vvvvv)

##### References
* [Related Chapter](../../dvars/c0098)
