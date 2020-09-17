---
title: "c0099_vvvvv"
date: 2020-09-18T01:27:37+99:00
draft: false
weight: 10994

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
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0099
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001bf2e0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
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
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    }
    
    (core.Cache) (len=2) {
     (string) (len=7) "student": (map[string]interface {}) (len=3) {
      (string) (len=4) "name": (string) (len=3) "Tom",
      (string) (len=6) "gender": (string) (len=4) "Male",
      (string) (len=6) "school": (string) (len=14) "Sydney Grammar"
     },
     (string) (len=3) "nsw": (map[string]interface {}) (len=1) {
      (string) (len=6) "sydney": (map[string]interface {}) (len=1) {
       (string) (len=8) "sgschool": (map[string]interface {}) (len=1) {
        (string) (len=7) "student": (map[string]interface {}) (len=3) {
         (string) (len=4) "name": (string) (len=5) "Grace",
         (string) (len=6) "gender": (string) (len=6) "Female",
         (string) (len=6) "school": (string) (len=3) "MLC"
        }
       }
      }
     }
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
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
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: use datatemplate as datasource ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.student_info}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "student_info",
          Value: "my name is:{{.name}} and I am in {{.school}}",
          Desc: "",
          Expand: 0,
          Flags: {
            "vvv"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: "name: {{.nsw.sydney.sgschool.student.name}}\ngender: {{.nsw.sydney.sgschool.student.gender}}\nschool: {{.nsw.sydney.sgschool.student.school}}\n"
        }
      },
      Desc: "use datatemplate as datasource",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
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
      "up_runtime_task_layer_number": 0
    })
    
    dvar> student_info:
    "my name is:Grace and I am in MLC"
    
    -
    my name is:Grace and I am in MLC
    [local] dvar expanded result:
    {
      "student_info": "my name is:Grace and I am in MLC"
    }
    
    
    scope[local] merged: {
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
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
      "up_runtime_task_layer_number": 0,
      "student_info": "my name is:Grace and I am in MLC"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
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
      "up_runtime_task_layer_number": 0,
      "student_info": "my name is:Grace and I am in MLC"
    })
    
    {{.student_info}}
    ~SubStep1: [print:  ]
    my name is:Grace and I am in MLC
    -Step2: [: use datatemplate as datasource ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.student_info}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "student_info",
          Value: "my name is:{{.student.name}} and I am in {{.school.name}}",
          Desc: "",
          Expand: 0,
          Flags: {
            "vvv"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: "student:\n  name: {{.nsw.sydney.sgschool.student.name}}\n  gender: {{.nsw.sydney.sgschool.student.gender}}\nschool:\n  name: {{.nsw.sydney.sgschool.student.school}}\n"
        }
      },
      Desc: "use datatemplate as datasource",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
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
      "up_runtime_task_layer_number": 0
    })
    
    dvar> student_info:
    "my name is:Grace and I am in MLC"
    
    -
    my name is:Grace and I am in MLC
    [local] dvar expanded result:
    {
      "student_info": "my name is:Grace and I am in MLC"
    }
    
    
    scope[local] merged: {
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
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
      "up_runtime_task_layer_number": 0,
      "student_info": "my name is:Grace and I am in MLC"
    }
    
    
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
      "up_runtime_task_layer_number": 0,
      "student_info": "my name is:Grace and I am in MLC",
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    })
    
    {{.student_info}}
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
