---
title: "c0099_vvvvv"
date: 2020-06-25T01:55:54+66:00
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
              ModuleName -> suspicious_rosalind6
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0099
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ed200)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [suspicious_rosalind6] instance id: [dev]
    merged[ dev ] runtime vars:
    {
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
    }
    
    (core.Cache) (len=2) {
     (string) (len=7) "student": (map[string]interface {}) (len=3) {
      (string) (len=6) "school": (string) (len=14) "Sydney Grammar",
      (string) (len=4) "name": (string) (len=3) "Tom",
      (string) (len=6) "gender": (string) (len=4) "Male"
     },
     (string) (len=3) "nsw": (map[string]interface {}) (len=1) {
      (string) (len=6) "sydney": (map[string]interface {}) (len=1) {
       (string) (len=8) "sgschool": (map[string]interface {}) (len=1) {
        (string) (len=7) "student": (map[string]interface {}) (len=3) {
         (string) (len=6) "gender": (string) (len=6) "Female",
         (string) (len=6) "school": (string) (len=3) "MLC",
         (string) (len=4) "name": (string) (len=5) "Grace"
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
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    })
    
    dvar> student_info:
    "my name is:Grace and I am in MLC"
    
    [local] dvar expanded result:
    {
      "student_info": "my name is:Grace and I am in MLC"
    }
    
    
    scope[local] merged: {
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
      },
      "student_info": "my name is:Grace and I am in MLC"
    }
    
    
    suspicious_rosalind6: overall final exec vars:
    
    (*core.Cache)({
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
      },
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
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
      VarsFile: ""
    }
    
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
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
    })
    
    dvar> student_info:
    "my name is:Grace and I am in MLC"
    
    [local] dvar expanded result:
    {
      "student_info": "my name is:Grace and I am in MLC"
    }
    
    
    scope[local] merged: {
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
      },
      "student_info": "my name is:Grace and I am in MLC"
    }
    
    
    suspicious_rosalind6: overall final exec vars:
    
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
