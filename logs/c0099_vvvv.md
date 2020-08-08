---
title: "c0099_vvvv"
date: 2020-08-09T01:36:13+88:00
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
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0099
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
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "nsw": {
        "sydney": {
          "sgschool": {
            "student": {
              "gender": "Female",
              "school": "MLC",
              "name": "Grace"
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
              "school": "MLC",
              "name": "Grace",
              "gender": "Female"
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
              "gender": "Female",
              "school": "MLC",
              "name": "Grace"
            }
          }
        }
      },
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    })
    
    dvar> student_info:
    "my name is:Grace and I am in MLC"
    
    -
    my name is:Grace and I am in MLC
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
    -Step2: [: use datatemplate as datasource ]
    current exec runtime vars:
    (*core.Cache)({
      "nsw": {
        "sydney": {
          "sgschool": {
            "student": {
              "school": "MLC",
              "name": "Grace",
              "gender": "Female"
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
    
    -
    my name is:Grace and I am in MLC
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "student_info": "my name is:Grace and I am in MLC",
      "nsw": {
        "sydney": {
          "sgschool": {
            "student": {
              "school": "MLC",
              "name": "Grace",
              "gender": "Female"
            }
          }
        }
      }
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
