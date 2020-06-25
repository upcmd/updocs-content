---
title: "c0099_vvvv"
date: 2020-06-25T01:55:54+66:00
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
              ModuleName -> evil_brattain4
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
    module: [evil_brattain4] instance id: [dev]
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
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
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
      VarsFile: ""
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
              "school": "MLC",
              "name": "Grace",
              "gender": "Female"
            }
          }
        }
      }
    })
    
    dvar> student_info:
    "my name is:Grace and I am in MLC"
    
    evil_brattain4: overall final exec vars:
    
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
      "student_info": "my name is:Grace and I am in MLC"
    })
    
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
      VarsFile: ""
    }
    
    current exec runtime vars:
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
              "school": "MLC",
              "name": "Grace",
              "gender": "Female"
            }
          }
        }
      }
    })
    
    dvar> student_info:
    "my name is:Grace and I am in MLC"
    
    evil_brattain4: overall final exec vars:
    
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
      "student_info": "my name is:Grace and I am in MLC",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
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
