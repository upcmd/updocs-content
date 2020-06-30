---
title: "c0098_vvvvv"
date: 2020-07-01T15:34:34+77:00
draft: false
weight: 10984

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
                 Verbose -> vvvvv
              ModuleName -> kickass_kilby6
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0098
    -------full vars in scopes------
    (*impl.Scopes)(0xc000157060)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [kickass_kilby6] instance id: [dev]
    merged[ dev ] runtime vars:
    {
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
              "name": "Tom",
              "gender": "Male",
              "school": "Sydney Grammar"
            }
          }
        }
      }
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
         (string) (len=6) "school": (string) (len=14) "Sydney Grammar",
         (string) (len=4) "name": (string) (len=3) "Tom",
         (string) (len=6) "gender": (string) (len=4) "Male"
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
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
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
    
    -Step1: [: use sub element of an var as context to render values ]
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
          DataPath: "nsw.sydney.sgschool.student",
          DataTemplate: ""
        }
      },
      Desc: "use sub element of an var as context to render values",
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
    })
    
    (string) (len=11) "sub yml str"
    
    (string) (len=97) "sydney:\n  sgschool:\n    student:\n      gender: Male\n      name: Tom\n      school: Sydney Grammar\n"
    
    dvar> student_info:
    "my name is:<no value> and I am in <no value>"
    
    [local] dvar expanded result:
    {
      "student_info": "my name is:<no value> and I am in <no value>"
    }
    
    
    scope[local] merged: {
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
              "name": "Tom",
              "gender": "Male",
              "school": "Sydney Grammar"
            }
          }
        }
      },
      "student_info": "my name is:<no value> and I am in <no value>"
    }
    
    
    kickass_kilby6: overall final exec vars:
    
    (*core.Cache)({
      "student_info": "my name is:<no value> and I am in <no value>",
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
    })
    
    {{.student_info}}
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
