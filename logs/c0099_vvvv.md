---
title: "c0099_vvvv"
date: 2020-07-20T02:01:46+77:00
draft: false
weight: 10993

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0099
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0099
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
      "nsw": {
        "sydney": {
          "sgschool": {
            "student": {
              "name": "Grace",
              "gender": "Female",
              "school": "MLC"
            }
          }
        }
      },
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "nsw": {
        "sydney": {
          "sgschool": {
            "student": {
              "name": "Grace",
              "gender": "Female",
              "school": "MLC"
            }
          }
        }
      },
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      }
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: use datatemplate as datasource ]
    current exec runtime vars:
    (*core.Cache)({
      "nsw": {
        "sydney": {
          "sgschool": {
            "student": {
              "name": "Grace",
              "gender": "Female",
              "school": "MLC"
            }
          }
        }
      },
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
    })
    
    dvar> student_info:
    "my name is:Grace and I am in MLC"
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "student_info": "my name is:Grace and I am in MLC",
      "nsw": {
        "sydney": {
          "sgschool": {
            "student": {
              "name": "Grace",
              "gender": "Female",
              "school": "MLC"
            }
          }
        }
      }
    })
    
    ~SubStep1: [print:  ]
    my name is:Grace and I am in MLC
    -Step2: [: use datatemplate as datasource ]
    current exec runtime vars:
    (*core.Cache)({
      "nsw": {
        "sydney": {
          "sgschool": {
            "student": {
              "name": "Grace",
              "gender": "Female",
              "school": "MLC"
            }
          }
        }
      },
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      }
    })
    
    dvar> student_info:
    "my name is:Grace and I am in MLC"
    
    self: final context exec vars:
    
    (*core.Cache)({
      "nsw": {
        "sydney": {
          "sgschool": {
            "student": {
              "name": "Grace",
              "gender": "Female",
              "school": "MLC"
            }
          }
        }
      },
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "student_info": "my name is:Grace and I am in MLC"
    })
    
    ~SubStep1: [print:  ]
    my name is:Grace and I am in MLC
    
```

##### Logs with different verbose level
* [c0099 log - verbose level v](../../logs/c0099_v)
* [c0099 log - verbose level vv](../../logs/c0099_vv)
* [c0099 log - verbose level vvv](../../logs/c0099_vvv)
* [c0099 log - verbose level vvvv](../../logs/c0099_vvvv)
* [c0099 log - verbose level vvvvv](../../logs/c0099_vvvvv)

##### References
* [Related Chapter](../../dvars/c0099)
