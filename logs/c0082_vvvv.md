---
title: "c0082_vvvv"
date: 2020-10-07T00:11:13+1010:00
draft: false
weight: 10823

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0082
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
    loading [Task]:  ./tests/functests/c0082
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
      "aaa": "aaa",
      "datapointer": "student",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "nsw": {
        "sydney": {
          "sgschool": {
            "student": {
              "school": "Sydney Grammar",
              "name": "Tom",
              "gender": "Male"
            }
          }
        }
      }
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
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
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "datapointer": "student",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
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
      "aaa": "aaa"
    })
    
    dvar> student_info:
    "my name is:<no value> and I am in <no value>"
    
    -
    my name is:<no value> and I am in <no value>
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "student_info": "my name is:<no value> and I am in <no value>",
      "datapointer": "student",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "nsw": {
        "sydney": {
          "sgschool": {
            "student": {
              "school": "Sydney Grammar",
              "name": "Tom",
              "gender": "Male"
            }
          }
        }
      },
      "aaa": "aaa"
    })
    
    ~SubStep1: [print:  ]
    my name is:<no value> and I am in <no value>
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "aaa": "aaa",
      "up_runtime_task_layer_number": 0,
      "datapointer": "student",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
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
      }
    })
    
    dvar> student_info:
    "my name is:<no value> and I am in <no value>"
    
    -
    my name is:<no value> and I am in <no value>
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "student_info": "my name is:<no value> and I am in <no value>",
      "datapointer": "student",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
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
      "aaa": "aaa"
    })
    
    ~SubStep1: [print:  ]
    my name is:<no value> and I am in <no value>
    
```

##### Logs with different verbose level
* [c0082 log - verbose level v](../../logs/c0082_v)
* [c0082 log - verbose level vv](../../logs/c0082_vv)
* [c0082 log - verbose level vvv](../../logs/c0082_vvv)
* [c0082 log - verbose level vvvv](../../logs/c0082_vvvv)
* [c0082 log - verbose level vvvvv](../../logs/c0082_vvvvv)

##### References
* [Related Chapter](../../dvars/c0082)
