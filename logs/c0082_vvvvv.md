---
title: "c0082_vvvvv"
date: 2020-09-18T01:27:34+99:00
draft: false
weight: 10824

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
    loading [Task]:  ./tests/functests/c0082
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001f5260)(<nil>)
    
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
              "school": "Sydney Grammar",
              "name": "Tom",
              "gender": "Male"
            }
          }
        }
      },
      "aaa": "aaa",
      "datapointer": "student"
    }
    
    (core.Cache) (len=4) {
     (string) (len=3) "aaa": (string) (len=3) "aaa",
     (string) (len=11) "datapointer": (string) (len=7) "student",
     (string) (len=7) "student": (map[string]interface {}) (len=3) {
      (string) (len=4) "name": (string) (len=3) "Tom",
      (string) (len=6) "gender": (string) (len=4) "Male",
      (string) (len=6) "school": (string) (len=14) "Sydney Grammar"
     },
     (string) (len=3) "nsw": (map[string]interface {}) (len=1) {
      (string) (len=6) "sydney": (map[string]interface {}) (len=1) {
       (string) (len=8) "sgschool": (map[string]interface {}) (len=1) {
        (string) (len=7) "student": (map[string]interface {}) (len=3) {
         (string) (len=6) "gender": (string) (len=4) "Male",
         (string) (len=6) "school": (string) (len=14) "Sydney Grammar",
         (string) (len=4) "name": (string) (len=3) "Tom"
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
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
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
          DataKey: "student",
          DataPath: "",
          DataTemplate: ""
        }
      },
      Desc: "",
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
      "up_runtime_task_layer_number": 0,
      "aaa": "aaa"
    })
    
    dvar> student_info:
    "my name is:<no value> and I am in <no value>"
    
    -
    my name is:<no value> and I am in <no value>
    [local] dvar expanded result:
    {
      "student_info": "my name is:<no value> and I am in <no value>"
    }
    
    
    scope[local] merged: {
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
              "school": "Sydney Grammar",
              "name": "Tom",
              "gender": "Male"
            }
          }
        }
      },
      "up_runtime_task_layer_number": 0,
      "aaa": "aaa",
      "student_info": "my name is:<no value> and I am in <no value>"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "aaa": "aaa",
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
              "school": "Sydney Grammar",
              "name": "Tom",
              "gender": "Male"
            }
          }
        }
      },
      "up_runtime_task_layer_number": 0,
      "student_info": "my name is:<no value> and I am in <no value>"
    })
    
    {{.student_info}}
    ~SubStep1: [print:  ]
    my name is:<no value> and I am in <no value>
    -Step2:
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
          DataKey: "{{.datapointer}}",
          DataPath: "",
          DataTemplate: ""
        }
      },
      Desc: "",
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
      "aaa": "aaa",
      "datapointer": "student",
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "up_runtime_task_layer_number": 0
    })
    
    dvar> student_info:
    "my name is:<no value> and I am in <no value>"
    
    -
    my name is:<no value> and I am in <no value>
    [local] dvar expanded result:
    {
      "student_info": "my name is:<no value> and I am in <no value>"
    }
    
    
    scope[local] merged: {
      "aaa": "aaa",
      "student_info": "my name is:<no value> and I am in <no value>",
      "datapointer": "student",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "up_runtime_task_layer_number": 0,
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
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "up_runtime_task_layer_number": 0,
      "student_info": "my name is:<no value> and I am in <no value>",
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
      "aaa": "aaa",
      "datapointer": "student"
    })
    
    {{.student_info}}
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
