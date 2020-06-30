---
title: "c0082_vvvv"
date: 2020-07-01T15:34:32+77:00
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
              ModuleName -> backstabbing_mayer4
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0082
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [backstabbing_mayer4] instance id: [dev]
    merged[ dev ] runtime vars:
    {
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
              "name": "Tom",
              "gender": "Male",
              "school": "Sydney Grammar"
            }
          }
        }
      },
      "aaa": "aaa"
    }
    
    -------runtime global final merged with dvars-------
    
    {
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
      }
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
      VarsFile: ""
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
    
    dvar> student_info:
    "my name is:<no value> and I am in <no value>"
    
    backstabbing_mayer4: overall final exec vars:
    
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
      VarsFile: ""
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
    
    dvar> student_info:
    "my name is:<no value> and I am in <no value>"
    
    backstabbing_mayer4: overall final exec vars:
    
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
* [c0082 log - verbose level v](../../logs/c0082_v)
* [c0082 log - verbose level vv](../../logs/c0082_vv)
* [c0082 log - verbose level vvv](../../logs/c0082_vvv)
* [c0082 log - verbose level vvvv](../../logs/c0082_vvvv)
* [c0082 log - verbose level vvvvv](../../logs/c0082_vvvvv)

##### References
* [Related Chapter](../../dvars/c0082)
