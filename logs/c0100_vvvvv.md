---
title: "c0100_vvvvv"
date: 2020-07-20T02:01:47+77:00
draft: false
weight: 11004

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0100
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0100
    -------full vars in scopes------
    (*impl.Scopes)(0xc000205de0)(<nil>)
    
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
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        }
      },
      "query_name": "jason"
    }
    
    (core.Cache) (len=3) {
     (string) (len=3) "nsw": (map[string]interface {}) (len=2) {
      (string) (len=9) "chatswood": ([]interface {}) (len=1 cap=1) {
       (map[interface {}]interface {}) (len=1) {
        (string) (len=14) "chatswood_high": (map[interface {}]interface {}) (len=1) {
         (string) (len=7) "student": (map[interface {}]interface {}) (len=3) {
          (string) (len=4) "name": (string) (len=5) "Jason",
          (string) (len=6) "gender": (string) (len=4) "Mail",
          (string) (len=6) "school": (string) (len=18) "Public High School"
         }
        }
       }
      },
      (string) (len=6) "sydney": ([]interface {}) (len=2 cap=2) {
       (map[interface {}]interface {}) (len=1) {
        (string) (len=2) "sg": (map[interface {}]interface {}) (len=1) {
         (string) (len=7) "student": (map[interface {}]interface {}) (len=3) {
          (string) (len=4) "name": (string) (len=5) "Grace",
          (string) (len=6) "gender": (string) (len=6) "Female",
          (string) (len=6) "school": (string) (len=3) "MLC"
         }
        }
       },
       (map[interface {}]interface {}) (len=1) {
        (string) (len=5) "kings": (map[interface {}]interface {}) (len=1) {
         (string) (len=7) "student": (map[interface {}]interface {}) (len=3) {
          (string) (len=4) "name": (string) (len=5) "Emily",
          (string) (len=6) "gender": (string) (len=6) "Female",
          (string) (len=6) "school": (string) (len=5) "KINGS"
         }
        }
       }
      }
     },
     (string) (len=10) "query_name": (string) (len=5) "jason",
     (string) (len=7) "student": (map[string]interface {}) (len=3) {
      (string) (len=6) "gender": (string) (len=4) "Male",
      (string) (len=6) "school": (string) (len=14) "Sydney Grammar",
      (string) (len=4) "name": (string) (len=3) "Tom"
     }
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "query_name": "jason",
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "school": "Public High School",
                "name": "Jason",
                "gender": "Mail"
              }
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
          "name": "query",
          "desc": "query using ref var ymlstr and query a registered var by default in global",
          "cmd": {
            "ymlkey": "ymlstr",
            "path": "student.school",
            "reg": "school_name"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "ymlstr": "student:\n  name: jason\n  gender: Male\n  school: The Kings\n"
      },
      Dvars: <nil>,
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
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "school": "KINGS",
                "name": "Emily",
                "gender": "Female"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "gender": "Mail",
                "school": "Public High School",
                "name": "Jason"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "ymlstr": "student:\n  name: jason\n  gender: Male\n  school: The Kings\n"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "ymlstr": "student:\n  name: jason\n  gender: Male\n  school: The Kings\n",
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "school": "KINGS",
                "name": "Emily"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "school": "Public High School",
                "name": "Jason",
                "gender": "Mail"
              }
            }
          }
        }
      },
      "query_name": "jason"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "nsw": {
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "school": "Public High School",
                "name": "Jason",
                "gender": "Mail"
              }
            }
          }
        },
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "school": "KINGS",
                "name": "Emily"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "ymlstr": "student:\n  name: jason\n  gender: Male\n  school: The Kings\n"
    })
    
    map[path:student.school reg:school_name ymlkey:ymlstr]
    ~SubStep1: [query: query using ref var ymlstr and query a registered var by default in global ]
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.school_name}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
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
      "school_name": (*string)("The Kings"),
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "school": "MLC",
                "name": "Grace"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "school_name": (*string)("The Kings"),
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "school": "MLC",
                "name": "Grace"
              }
            }
          },
          {
            "kings": {
              "student": {
                "school": "KINGS",
                "name": "Emily",
                "gender": "Female"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "gender": "Mail",
                "school": "Public High School",
                "name": "Jason"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "school_name": (*string)("The Kings"),
      "nsw": {
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "gender": "Mail",
                "school": "Public High School",
                "name": "Jason"
              }
            }
          }
        },
        "sydney": {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "name": "Grace",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "school": "KINGS",
                "name": "Emily"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    })
    
    {{.school_name}}
    ~SubStep1: [print:  ]
    The Kings
    -Step3:
    {
      Name: "",
      Do: {
        {
          "name": "query",
          "desc": "query using ref var ymlstr and query a registered var by default in global",
          "cmd": {
            "path": "student",
            "reg": "student_info",
            "ymlkey": "ymlstr"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "ymlstr": "student: |\n  name: jason\n  gender: Male\n  school: The Kings\n"
      },
      Dvars: <nil>,
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
      "school_name": (*string)("The Kings"),
      "ymlstr": "student: |\n  name: jason\n  gender: Male\n  school: The Kings\n",
      "nsw": {
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "school": "Public High School",
                "name": "Jason",
                "gender": "Mail"
              }
            }
          }
        },
        "sydney": {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "school": "MLC",
                "name": "Grace"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "school": "KINGS",
                "name": "Emily"
              }
            }
          }
        }
      },
      "query_name": "jason"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "school_name": (*string)("The Kings"),
      "ymlstr": "student: |\n  name: jason\n  gender: Male\n  school: The Kings\n",
      "nsw": {
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "school": "Public High School",
                "name": "Jason",
                "gender": "Mail"
              }
            }
          }
        },
        "sydney": {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "name": "Grace",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "school": "KINGS",
                "name": "Emily",
                "gender": "Female"
              }
            }
          }
        }
      },
      "query_name": "jason"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "school_name": (*string)("The Kings"),
      "ymlstr": "student: |\n  name: jason\n  gender: Male\n  school: The Kings\n",
      "nsw": {
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "school": "Public High School",
                "name": "Jason",
                "gender": "Mail"
              }
            }
          }
        },
        "sydney": {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "name": "Grace",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "school": "KINGS",
                "name": "Emily",
                "gender": "Female"
              }
            }
          }
        }
      },
      "query_name": "jason"
    })
    
    map[path:student reg:student_info ymlkey:ymlstr]
    ~SubStep1: [query: query using ref var ymlstr and query a registered var by default in global ]
    -Step4:
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
      Dvars: <nil>,
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
      "nsw": {
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        },
        "sydney": {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "name": "Grace",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "school": "KINGS",
                "name": "Emily"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "school": "The Kings",
        "name": "jason",
        "gender": "Male"
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "nsw": {
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        },
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "school": "KINGS",
                "name": "Emily",
                "gender": "Female"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "nsw": {
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        },
        "sydney": {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "school": "MLC",
                "name": "Grace"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        }
      },
      "query_name": "jason"
    })
    
    {{.student_info}}
    ~SubStep1: [print:  ]
    map[gender:Male name:jason school:The Kings]
    -Step5:
    {
      Name: "",
      Do: {
        {
          "name": "query",
          "desc": "query and query a registered var in local",
          "cmd": {
            "reg": "local_school_name",
            "ymlkey": "ymlstr",
            "path": "student.school"
          },
          "flags": {
            "localOnly"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "ymlstr": "student:\n  name: jason\n  gender: Male\n  school: The Kings\n"
      },
      Dvars: <nil>,
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
      "ymlstr": "student:\n  name: jason\n  gender: Male\n  school: The Kings\n",
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "name": "Grace",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "school": "The Kings",
        "name": "jason",
        "gender": "Male"
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "ymlstr": "student:\n  name: jason\n  gender: Male\n  school: The Kings\n",
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "name": "Grace",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "gender": "Mail",
                "school": "Public High School",
                "name": "Jason"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "school": "The Kings",
        "name": "jason",
        "gender": "Male"
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "ymlstr": "student:\n  name: jason\n  gender: Male\n  school: The Kings\n",
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "name": "Grace",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "school": "KINGS",
                "name": "Emily"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "gender": "Mail",
                "school": "Public High School",
                "name": "Jason"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "school": "The Kings",
        "name": "jason",
        "gender": "Male"
      })
    })
    
    map[path:student.school reg:local_school_name ymlkey:ymlstr]
    ~SubStep1: [query: query and query a registered var in local ]
    -Step6:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.local_school_name}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
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
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "school": "The Kings",
        "name": "jason",
        "gender": "Male"
      }),
      "nsw": {
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        },
        "sydney": {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "name": "Grace",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        }
      },
      "query_name": "jason"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "gender": "Mail",
                "school": "Public High School",
                "name": "Jason"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "school_name": (*string)("The Kings")
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "school": "KINGS",
                "name": "Emily",
                "gender": "Female"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "school": "Public High School",
                "name": "Jason",
                "gender": "Mail"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      })
    })
    
    {{.local_school_name}}
    ~SubStep1: [print:  ]
    None
    -Step7:
    {
      Name: "",
      Do: {
        {
          "name": "query",
          "desc": "query from cached vars only",
          "cmd": {
            "path": "nsw.sydney.sg.student.school",
            "reg": "data_school_name"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
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
      "query_name": "jason",
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "name": "Grace",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "school": "KINGS",
                "name": "Emily"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "gender": "Mail",
                "school": "Public High School",
                "name": "Jason"
              }
            }
          }
        }
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "name": "Grace",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "school": "KINGS",
                "name": "Emily",
                "gender": "Female"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "school": "Public High School",
                "name": "Jason",
                "gender": "Mail"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "gender": "Male",
        "school": "The Kings",
        "name": "jason"
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student_info": (*map[interface {}]interface {})({
        "gender": "Male",
        "school": "The Kings",
        "name": "jason"
      }),
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "name": "Grace",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "school_name": (*string)("The Kings")
    })
    
    map[path:nsw.sydney.sg.student.school reg:data_school_name]
    ~SubStep1: [query: query from cached vars only ]
    (string) (len=11) "sub yml str"
    
    (string) (len=277) "chatswood:\n- chatswood_high:\n    student:\n      gender: Mail\n      name: Jason\n      school: Public High School\nsydney:\n- sg:\n    student:\n      gender: Female\n      name: Grace\n      school: MLC\n- kings:\n    student:\n      gender: Female\n      name: Emily\n      school: KINGS\n"
    
    -Step8:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.data_school_name}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
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
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "gender": "Male",
        "school": "The Kings",
        "name": "jason"
      }),
      "data_school_name": "",
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "school": "KINGS",
                "name": "Emily"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "gender": "Mail",
                "school": "Public High School",
                "name": "Jason"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "data_school_name": "",
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "name": "Grace",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "school": "KINGS",
                "name": "Emily"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "data_school_name": "",
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "school": "MLC",
                "name": "Grace"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "school": "KINGS",
                "name": "Emily"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "gender": "Male",
        "school": "The Kings",
        "name": "jason"
      })
    })
    
    {{.data_school_name}}
    ~SubStep1: [print:  ]
    
    -Step9:
    {
      Name: "",
      Do: {
        {
          "name": "query",
          "desc": "query from cached vars and put result into a list/array",
          "cmd": {
            "path": "nsw.sydney.**.student.school",
            "reg": "school_name_list"
          },
          "flags": {
            "collect"
          }
        },
        {
          "cmd": "{{.school_name_list}}",
          "name": "printObj"
        },
        {
          "name": "print",
          "cmd": "{{.school_name_list}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
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
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "data_school_name": ""
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "name": "Grace",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "data_school_name": ""
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "nsw": {
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        },
        "sydney": {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "school": "MLC",
                "name": "Grace"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "gender": "Male",
        "school": "The Kings",
        "name": "jason"
      }),
      "data_school_name": ""
    })
    
    map[path:nsw.sydney.**.student.school reg:school_name_list]
    ~SubStep1: [query: query from cached vars and put result into a list/array ]
    (string) (len=11) "sub yml str"
    
    (string) (len=277) "chatswood:\n- chatswood_high:\n    student:\n      gender: Mail\n      name: Jason\n      school: Public High School\nsydney:\n- sg:\n    student:\n      gender: Female\n      name: Grace\n      school: MLC\n- kings:\n    student:\n      gender: Female\n      name: Emily\n      school: KINGS\n"
    
    {{.school_name_list}}
    ~SubStep2: [printObj:  ]
    (string) (len=21) "{{.school_name_list}}"
    
    object:
     [MLC KINGS]: (interface {}) <nil>
    
    {{.school_name_list}}
    ~SubStep3: [print:  ]
    [MLC KINGS]
    -Step10:
    {
      Name: "",
      Do: {
        {
          "name": "query",
          "desc": "query a sub node",
          "cmd": {
            "path": "nsw.sydney",
            "reg": "city"
          },
          "flags": {
            "collect"
          }
        },
        {
          "cmd": "{{.city}}",
          "name": "printObj"
        },
        {
          "name": "print",
          "cmd": "{{.city}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
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
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "gender": "Male",
        "school": "The Kings",
        "name": "jason"
      }),
      "data_school_name": "",
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        }
      },
      "query_name": "jason"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "name": "Grace",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "data_school_name": ""
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "gender": "Male",
        "school": "The Kings",
        "name": "jason"
      }),
      "data_school_name": "",
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "gender": "Mail",
                "school": "Public High School",
                "name": "Jason"
              }
            }
          }
        }
      },
      "query_name": "jason"
    })
    
    map[path:nsw.sydney reg:city]
    ~SubStep1: [query: query a sub node ]
    (string) (len=11) "sub yml str"
    
    (string) (len=277) "chatswood:\n- chatswood_high:\n    student:\n      gender: Mail\n      name: Jason\n      school: Public High School\nsydney:\n- sg:\n    student:\n      gender: Female\n      name: Grace\n      school: MLC\n- kings:\n    student:\n      gender: Female\n      name: Emily\n      school: KINGS\n"
    
    {{.city}}
    ~SubStep2: [printObj:  ]
    (string) (len=9) "{{.city}}"
    
    object:
     [[map[sg:map[student:map[gender:Female name:Grace school:MLC]]] map[kings:map[student:map[gender:Female name:Emily school:KINGS]]]]]: (interface {}) <nil>
    
    {{.city}}
    ~SubStep3: [print:  ]
    [[map[sg:map[student:map[gender:Female name:Grace school:MLC]]] map[kings:map[student:map[gender:Female name:Emily school:KINGS]]]]]
    -Step11:
    {
      Name: "",
      Do: {
        {
          "name": "query",
          "desc": "query a selected indexed node from a array",
          "cmd": {
            "path": "nsw.sydney.[1]",
            "reg": "city1"
          }
        },
        {
          "name": "printObj",
          "cmd": "{{.city1}}"
        },
        {
          "name": "print",
          "cmd": "{{.city1}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
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
      "nsw": {
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        },
        "sydney": {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "name": "Grace",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "school": "The Kings",
        "name": "jason",
        "gender": "Male"
      }),
      "data_school_name": "",
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "name": "Grace",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "school": "KINGS",
                "gender": "Female",
                "name": "Emily"
              }
            }
          }
        }
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "school": "The Kings",
        "name": "jason",
        "gender": "Male"
      }),
      "data_school_name": "",
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "name": "Grace",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "school": "KINGS",
                "gender": "Female",
                "name": "Emily"
              }
            }
          }
        }
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "query_name": "jason",
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "school": "The Kings",
        "name": "jason",
        "gender": "Male"
      }),
      "data_school_name": "",
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "school": "MLC",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "school": "KINGS",
                "gender": "Female",
                "name": "Emily"
              }
            }
          }
        }
      }),
      "nsw": {
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        },
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "school": "KINGS",
                "name": "Emily",
                "gender": "Female"
              }
            }
          }
        }
      }
    })
    
    map[path:nsw.sydney.[1] reg:city1]
    ~SubStep1: [query: query a selected indexed node from a array ]
    (string) (len=11) "sub yml str"
    
    (string) (len=277) "chatswood:\n- chatswood_high:\n    student:\n      gender: Mail\n      name: Jason\n      school: Public High School\nsydney:\n- sg:\n    student:\n      gender: Female\n      name: Grace\n      school: MLC\n- kings:\n    student:\n      gender: Female\n      name: Emily\n      school: KINGS\n"
    
    {{.city1}}
    ~SubStep2: [printObj:  ]
    (string) (len=10) "{{.city1}}"
    
    object:
     map[kings:map[student:map[gender:Female name:Emily school:KINGS]]]: (interface {}) <nil>
    
    {{.city1}}
    ~SubStep3: [print:  ]
    map[kings:map[student:map[gender:Female name:Emily school:KINGS]]]
    -Step12:
    {
      Name: "",
      Do: {
        {
          "name": "query",
          "desc": "query all nodes from an array",
          "cmd": {
            "path": "nsw.sydney.[*]",
            "reg": "cityall"
          }
        },
        {
          "name": "printObj",
          "cmd": "{{.cityall}}"
        },
        {
          "name": "print",
          "cmd": "{{.cityall}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
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
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "school_name": (*string)("The Kings"),
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "name": "Grace",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "name": "Emily",
                "school": "KINGS"
              }
            }
          }
        }
      }),
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "school": "KINGS",
            "gender": "Female",
            "name": "Emily"
          }
        }
      }),
      "data_school_name": "",
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "school": "Public High School",
                "name": "Jason",
                "gender": "Mail"
              }
            }
          }
        }
      },
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "query_name": "jason"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "data_school_name": "",
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "query_name": "jason",
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "name": "Grace",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "school": "KINGS",
                "gender": "Female",
                "name": "Emily"
              }
            }
          }
        }
      }),
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        }
      }),
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "school": "MLC",
                "name": "Grace"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "school": "KINGS",
                "name": "Emily"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        }
      },
      "school_name": (*string)("The Kings"),
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "query_name": "jason",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        }
      }),
      "data_school_name": "",
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "school": "MLC",
                "name": "Grace"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "school": "KINGS",
                "name": "Emily"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        }
      },
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "school_name": (*string)("The Kings"),
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "name": "Grace",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "name": "Emily",
                "school": "KINGS"
              }
            }
          }
        }
      })
    })
    
    map[path:nsw.sydney.[*] reg:cityall]
    ~SubStep1: [query: query all nodes from an array ]
    (string) (len=11) "sub yml str"
    
    (string) (len=277) "chatswood:\n- chatswood_high:\n    student:\n      gender: Mail\n      name: Jason\n      school: Public High School\nsydney:\n- sg:\n    student:\n      gender: Female\n      name: Grace\n      school: MLC\n- kings:\n    student:\n      gender: Female\n      name: Emily\n      school: KINGS\n"
    
    {{.cityall}}
    ~SubStep2: [printObj:  ]
    (string) (len=12) "{{.cityall}}"
    
    object:
     map[kings:map[student:map[gender:Female name:Emily school:KINGS]] sg:map[student:map[gender:Female name:Grace school:MLC]]]: (interface {}) <nil>
    
    {{.cityall}}
    ~SubStep3: [print:  ]
    map[kings:map[student:map[gender:Female name:Emily school:KINGS]] sg:map[student:map[gender:Female name:Grace school:MLC]]]
    -Step13:
    {
      Name: "",
      Do: {
        {
          "name": "query",
          "desc": "query result matching the criteria",
          "cmd": {
            "path": "nsw.sydney.[*].*(name==Emily)",
            "reg": "studentx"
          }
        },
        {
          "name": "printObj",
          "cmd": "{{.studentx}}"
        },
        {
          "name": "print",
          "cmd": "{{.studentx}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
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
      "cityall": (*map[interface {}]interface {})({
        "sg": {
          "student": {
            "gender": "Female",
            "name": "Grace",
            "school": "MLC"
          }
        },
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        }
      }),
      "school_name": (*string)("The Kings"),
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "name": "Grace",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "school": "KINGS",
                "gender": "Female",
                "name": "Emily"
              }
            }
          }
        }
      }),
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "school": "KINGS",
            "gender": "Female",
            "name": "Emily"
          }
        }
      }),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "gender": "Mail",
                "school": "Public High School",
                "name": "Jason"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "data_school_name": "",
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "cityall": (*map[interface {}]interface {})({
        "sg": {
          "student": {
            "name": "Grace",
            "school": "MLC",
            "gender": "Female"
          }
        },
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        }
      }),
      "school_name": (*string)("The Kings"),
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "name": "Grace",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "school": "KINGS",
                "gender": "Female"
              }
            }
          }
        }
      }),
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "name": "Emily",
            "school": "KINGS",
            "gender": "Female"
          }
        }
      }),
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "nsw": {
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "school": "Public High School",
                "name": "Jason",
                "gender": "Mail"
              }
            }
          }
        },
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "data_school_name": ""
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "query_name": "jason",
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "cityall": (*map[interface {}]interface {})({
        "sg": {
          "student": {
            "name": "Grace",
            "school": "MLC",
            "gender": "Female"
          }
        },
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        }
      }),
      "school_name": (*string)("The Kings"),
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "name": "Grace",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "school": "KINGS",
                "gender": "Female"
              }
            }
          }
        }
      }),
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "name": "Emily",
            "school": "KINGS",
            "gender": "Female"
          }
        }
      }),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "school": "KINGS",
                "name": "Emily"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "school": "Public High School",
                "name": "Jason",
                "gender": "Mail"
              }
            }
          }
        }
      },
      "data_school_name": "",
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      })
    })
    
    map[path:nsw.sydney.[*].*(name==Emily) reg:studentx]
    ~SubStep1: [query: query result matching the criteria ]
    (string) (len=11) "sub yml str"
    
    (string) (len=277) "chatswood:\n- chatswood_high:\n    student:\n      gender: Mail\n      name: Jason\n      school: Public High School\nsydney:\n- sg:\n    student:\n      gender: Female\n      name: Grace\n      school: MLC\n- kings:\n    student:\n      gender: Female\n      name: Emily\n      school: KINGS\n"
    
    {{.studentx}}
    ~SubStep2: [printObj:  ]
    (string) (len=13) "{{.studentx}}"
    
    object:
     map[gender:Female name:Emily school:KINGS]: (interface {}) <nil>
    
    {{.studentx}}
    ~SubStep3: [print:  ]
    map[gender:Female name:Emily school:KINGS]
    -Step14:
    {
      Name: "",
      Do: {
        {
          "desc": "query result matching the criteria",
          "cmd": {
            "path": "nsw.sydney.[1].*(name==Emily)",
            "reg": "studenty"
          },
          "name": "query"
        },
        {
          "name": "printObj",
          "cmd": "{{.studenty}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
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
      "school_name": (*string)("The Kings"),
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "studentx": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        }
      }),
      "cityall": (*map[interface {}]interface {})({
        "sg": {
          "student": {
            "gender": "Female",
            "name": "Grace",
            "school": "MLC"
          }
        },
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        }
      }),
      "data_school_name": "",
      "nsw": {
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "gender": "Mail",
                "school": "Public High School",
                "name": "Jason"
              }
            }
          }
        },
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "school": "MLC",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "school": "KINGS",
                "gender": "Female",
                "name": "Emily"
              }
            }
          }
        }
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "data_school_name": "",
      "nsw": {
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "gender": "Mail",
                "school": "Public High School",
                "name": "Jason"
              }
            }
          }
        },
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        }
      },
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "studentx": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "cityall": (*map[interface {}]interface {})({
        "sg": {
          "student": {
            "name": "Grace",
            "school": "MLC",
            "gender": "Female"
          }
        },
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        }
      }),
      "school_name": (*string)("The Kings"),
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "school": "MLC",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "school": "KINGS",
                "gender": "Female",
                "name": "Emily"
              }
            }
          }
        }
      }),
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        }
      }),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "query_name": "jason"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "name": "Emily",
            "school": "KINGS",
            "gender": "Female"
          }
        }
      }),
      "cityall": (*map[interface {}]interface {})({
        "sg": {
          "student": {
            "name": "Grace",
            "school": "MLC",
            "gender": "Female"
          }
        },
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        }
      }),
      "school_name": (*string)("The Kings"),
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "studentx": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "data_school_name": "",
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "name": "Grace",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "school": "Public High School",
                "name": "Jason",
                "gender": "Mail"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "school": "MLC",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "school": "KINGS",
                "gender": "Female",
                "name": "Emily"
              }
            }
          }
        }
      })
    })
    
    map[path:nsw.sydney.[1].*(name==Emily) reg:studenty]
    ~SubStep1: [query: query result matching the criteria ]
    (string) (len=11) "sub yml str"
    
    (string) (len=277) "chatswood:\n- chatswood_high:\n    student:\n      gender: Mail\n      name: Jason\n      school: Public High School\nsydney:\n- sg:\n    student:\n      gender: Female\n      name: Grace\n      school: MLC\n- kings:\n    student:\n      gender: Female\n      name: Emily\n      school: KINGS\n"
    
    {{.studenty}}
    ~SubStep2: [printObj:  ]
    (string) (len=13) "{{.studenty}}"
    
    object:
     map[gender:Female name:Emily school:KINGS]: (interface {}) <nil>
    
    -Step15:
    {
      Name: "",
      Do: {
        {
          "name": "query",
          "desc": "query result matching the criteria",
          "cmd": {
            "path": "nsw.sydney.**(name==Emily)",
            "reg": "studentz"
          }
        },
        {
          "name": "printObj",
          "cmd": "{{.studentz}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
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
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "school": "MLC",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "name": "Emily",
                "school": "KINGS"
              }
            }
          }
        }
      }),
      "cityall": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "school": "KINGS",
            "gender": "Female",
            "name": "Emily"
          }
        },
        "sg": {
          "student": {
            "school": "MLC",
            "gender": "Female",
            "name": "Grace"
          }
        }
      }),
      "query_name": "jason",
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "student_info": (*map[interface {}]interface {})({
        "gender": "Male",
        "school": "The Kings",
        "name": "jason"
      }),
      "data_school_name": "",
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "studentx": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "school_name": (*string)("The Kings"),
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "name": "Emily",
            "school": "KINGS",
            "gender": "Female"
          }
        }
      }),
      "studenty": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "nsw": {
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "gender": "Mail",
                "school": "Public High School",
                "name": "Jason"
              }
            }
          }
        },
        "sydney": {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "name": "Grace",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        }
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "studenty": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "student_info": (*map[interface {}]interface {})({
        "gender": "Male",
        "school": "The Kings",
        "name": "jason"
      }),
      "data_school_name": "",
      "query_name": "jason",
      "studentx": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "name": "Emily",
            "school": "KINGS",
            "gender": "Female"
          }
        }
      }),
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "school": "Public High School",
                "name": "Jason",
                "gender": "Mail"
              }
            }
          }
        }
      },
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "school": "MLC",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "name": "Emily",
                "school": "KINGS"
              }
            }
          }
        }
      }),
      "cityall": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "name": "Emily",
            "school": "KINGS",
            "gender": "Female"
          }
        },
        "sg": {
          "student": {
            "gender": "Female",
            "name": "Grace",
            "school": "MLC"
          }
        }
      }),
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "school_name": (*string)("The Kings")
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        }
      }),
      "studenty": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "nsw": {
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        },
        "sydney": {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "name": "Grace",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "school": "KINGS",
                "name": "Emily",
                "gender": "Female"
              }
            }
          }
        }
      },
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "data_school_name": "",
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "studentx": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "school_name": (*string)("The Kings"),
      "cityall": (*map[interface {}]interface {})({
        "sg": {
          "student": {
            "gender": "Female",
            "name": "Grace",
            "school": "MLC"
          }
        },
        "kings": {
          "student": {
            "school": "KINGS",
            "gender": "Female",
            "name": "Emily"
          }
        }
      }),
      "query_name": "jason",
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "school": "MLC",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "school": "KINGS",
                "gender": "Female"
              }
            }
          }
        }
      })
    })
    
    map[path:nsw.sydney.**(name==Emily) reg:studentz]
    ~SubStep1: [query: query result matching the criteria ]
    (string) (len=11) "sub yml str"
    
    (string) (len=277) "chatswood:\n- chatswood_high:\n    student:\n      gender: Mail\n      name: Jason\n      school: Public High School\nsydney:\n- sg:\n    student:\n      gender: Female\n      name: Grace\n      school: MLC\n- kings:\n    student:\n      gender: Female\n      name: Emily\n      school: KINGS\n"
    
    {{.studentz}}
    ~SubStep2: [printObj:  ]
    (string) (len=13) "{{.studentz}}"
    
    object:
     map[gender:Female name:Emily school:KINGS]: (interface {}) <nil>
    
    -Step16:
    {
      Name: "",
      Do: {
        {
          "name": "query",
          "desc": "query result matching the criteria",
          "cmd": {
            "path": "nsw.sydney.[*].kings(name==Emily)",
            "reg": "studentm"
          }
        },
        {
          "name": "printObj",
          "cmd": "{{.studentm}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
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
      "studentx": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "studentz": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "name": "Grace",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "school": "Public High School",
                "name": "Jason",
                "gender": "Mail"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        }
      }),
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "data_school_name": "",
      "school_name": (*string)("The Kings"),
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "gender": "Female",
                "name": "Grace"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "school": "KINGS",
                "gender": "Female"
              }
            }
          }
        }
      }),
      "cityall": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        },
        "sg": {
          "student": {
            "name": "Grace",
            "school": "MLC",
            "gender": "Female"
          }
        }
      }),
      "studenty": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "school_name": (*string)("The Kings"),
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "cityall": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "name": "Emily",
            "school": "KINGS",
            "gender": "Female"
          }
        },
        "sg": {
          "student": {
            "gender": "Female",
            "name": "Grace",
            "school": "MLC"
          }
        }
      }),
      "studenty": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "student_info": (*map[interface {}]interface {})({
        "school": "The Kings",
        "name": "jason",
        "gender": "Male"
      }),
      "data_school_name": "",
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "gender": "Female",
                "name": "Grace"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "name": "Emily",
                "school": "KINGS"
              }
            }
          }
        }
      }),
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        }
      }),
      "studentx": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "studentz": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "school": "MLC",
                "name": "Grace"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "school": "KINGS",
                "name": "Emily"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        }
      },
      "query_name": "jason"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "query_name": "jason",
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        }
      }),
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "studentx": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "studentz": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        }
      },
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "name": "Grace",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "school": "KINGS",
                "gender": "Female"
              }
            }
          }
        }
      }),
      "cityall": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        },
        "sg": {
          "student": {
            "name": "Grace",
            "school": "MLC",
            "gender": "Female"
          }
        }
      }),
      "studenty": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "data_school_name": "",
      "school_name": (*string)("The Kings")
    })
    
    map[path:nsw.sydney.[*].kings(name==Emily) reg:studentm]
    ~SubStep1: [query: query result matching the criteria ]
    (string) (len=11) "sub yml str"
    
    (string) (len=277) "chatswood:\n- chatswood_high:\n    student:\n      gender: Mail\n      name: Jason\n      school: Public High School\nsydney:\n- sg:\n    student:\n      gender: Female\n      name: Grace\n      school: MLC\n- kings:\n    student:\n      gender: Female\n      name: Emily\n      school: KINGS\n"
    
    {{.studentm}}
    ~SubStep2: [printObj:  ]
    (string) (len=13) "{{.studentm}}"
    
    object:
     map[gender:Female name:Emily school:KINGS]: (interface {}) <nil>
    
    -Step17:
    {
      Name: "",
      Do: {
        {
          "cmd": {
            "path": "nsw.sydney.[*].*(name==Grace)",
            "reg": "studentn"
          },
          "name": "query",
          "desc": "query result matching the criteria"
        },
        {
          "name": "printObj",
          "cmd": "{{.studentn}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
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
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "name": "Grace",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "name": "Emily",
                "school": "KINGS"
              }
            }
          }
        }
      }),
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        }
      }),
      "studentm": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "query_name": "jason",
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "school_name": (*string)("The Kings"),
      "cityall": (*map[interface {}]interface {})({
        "sg": {
          "student": {
            "school": "MLC",
            "gender": "Female",
            "name": "Grace"
          }
        },
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        }
      }),
      "studenty": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "school": "MLC",
                "name": "Grace"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "gender": "Mail",
                "school": "Public High School",
                "name": "Jason"
              }
            }
          }
        }
      },
      "data_school_name": "",
      "studentx": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "studentz": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "studentm": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "school": "Public High School",
                "name": "Jason",
                "gender": "Mail"
              }
            }
          }
        }
      },
      "studentz": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        }
      }),
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "data_school_name": "",
      "studentx": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "query_name": "jason",
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "school": "MLC",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "school": "KINGS",
                "gender": "Female"
              }
            }
          }
        }
      }),
      "cityall": (*map[interface {}]interface {})({
        "sg": {
          "student": {
            "gender": "Female",
            "name": "Grace",
            "school": "MLC"
          }
        },
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        }
      }),
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "studenty": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "school_name": (*string)("The Kings")
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "studenty": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "school_name": (*string)("The Kings"),
      "cityall": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        },
        "sg": {
          "student": {
            "name": "Grace",
            "school": "MLC",
            "gender": "Female"
          }
        }
      }),
      "nsw": {
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "school": "Public High School",
                "name": "Jason",
                "gender": "Mail"
              }
            }
          }
        },
        "sydney": {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "name": "Grace",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "school": "KINGS",
                "name": "Emily"
              }
            }
          }
        }
      },
      "data_school_name": "",
      "studentz": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "studentx": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "student_info": (*map[interface {}]interface {})({
        "school": "The Kings",
        "name": "jason",
        "gender": "Male"
      }),
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "name": "Grace",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "name": "Emily",
                "school": "KINGS"
              }
            }
          }
        }
      }),
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "school": "KINGS",
            "gender": "Female",
            "name": "Emily"
          }
        }
      }),
      "studentm": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "query_name": "jason"
    })
    
    map[path:nsw.sydney.[*].*(name==Grace) reg:studentn]
    ~SubStep1: [query: query result matching the criteria ]
    (string) (len=11) "sub yml str"
    
    (string) (len=277) "chatswood:\n- chatswood_high:\n    student:\n      gender: Mail\n      name: Jason\n      school: Public High School\nsydney:\n- sg:\n    student:\n      gender: Female\n      name: Grace\n      school: MLC\n- kings:\n    student:\n      gender: Female\n      name: Emily\n      school: KINGS\n"
    
    {{.studentn}}
    ~SubStep2: [printObj:  ]
    (string) (len=13) "{{.studentn}}"
    
    object:
     map[gender:Female name:Grace school:MLC]: (interface {}) <nil>
    
    -Step18:
    {
      Name: "",
      Do: {
        {
          "name": "query",
          "desc": "query result matching the criteria",
          "cmd": {
            "reg": "studento",
            "path": "nsw.chatswood.[*]"
          }
        },
        {
          "name": "printObj",
          "cmd": "{{.studento}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
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
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "name": "Grace",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "name": "Emily",
                "school": "KINGS"
              }
            }
          }
        }
      }),
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "school": "KINGS",
            "gender": "Female",
            "name": "Emily"
          }
        }
      }),
      "studenty": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "studentz": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "studentx": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "studentn": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Grace",
        "school": "MLC"
      }),
      "school_name": (*string)("The Kings"),
      "studentm": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "nsw": {
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        },
        "sydney": {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "name": "Grace",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "school": "KINGS",
                "name": "Emily",
                "gender": "Female"
              }
            }
          }
        }
      },
      "student_info": (*map[interface {}]interface {})({
        "school": "The Kings",
        "name": "jason",
        "gender": "Male"
      }),
      "data_school_name": "",
      "cityall": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        },
        "sg": {
          "student": {
            "school": "MLC",
            "gender": "Female",
            "name": "Grace"
          }
        }
      }),
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "query_name": "jason",
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "cityall": (*map[interface {}]interface {})({
        "sg": {
          "student": {
            "gender": "Female",
            "name": "Grace",
            "school": "MLC"
          }
        },
        "kings": {
          "student": {
            "name": "Emily",
            "school": "KINGS",
            "gender": "Female"
          }
        }
      }),
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "data_school_name": "",
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "school": "KINGS",
                "name": "Emily"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        }
      },
      "studentn": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Grace",
        "school": "MLC"
      }),
      "studentm": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "query_name": "jason",
      "studenty": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "studentz": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "school": "The Kings",
        "name": "jason",
        "gender": "Male"
      }),
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "gender": "Female",
                "name": "Grace"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "name": "Emily",
                "school": "KINGS"
              }
            }
          }
        }
      }),
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        }
      }),
      "studentx": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "studenty": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "studentz": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "gender": "Female",
                "name": "Grace"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "name": "Emily",
                "school": "KINGS"
              }
            }
          }
        }
      }),
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "name": "Emily",
            "school": "KINGS",
            "gender": "Female"
          }
        }
      }),
      "school_name": (*string)("The Kings"),
      "studentm": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "studentx": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "studentn": (*map[interface {}]interface {})({
        "school": "MLC",
        "gender": "Female",
        "name": "Grace"
      }),
      "data_school_name": "",
      "cityall": (*map[interface {}]interface {})({
        "sg": {
          "student": {
            "school": "MLC",
            "gender": "Female",
            "name": "Grace"
          }
        },
        "kings": {
          "student": {
            "school": "KINGS",
            "gender": "Female",
            "name": "Emily"
          }
        }
      }),
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "nsw": {
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        },
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "school": "KINGS",
                "name": "Emily"
              }
            }
          }
        }
      },
      "student_info": (*map[interface {}]interface {})({
        "school": "The Kings",
        "name": "jason",
        "gender": "Male"
      }),
      "query_name": "jason",
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      }
    })
    
    map[path:nsw.chatswood.[*] reg:studento]
    ~SubStep1: [query: query result matching the criteria ]
    (string) (len=11) "sub yml str"
    
    (string) (len=277) "chatswood:\n- chatswood_high:\n    student:\n      gender: Mail\n      name: Jason\n      school: Public High School\nsydney:\n- sg:\n    student:\n      gender: Female\n      name: Grace\n      school: MLC\n- kings:\n    student:\n      gender: Female\n      name: Emily\n      school: KINGS\n"
    
    {{.studento}}
    ~SubStep2: [printObj:  ]
    (string) (len=13) "{{.studento}}"
    
    object:
     map[chatswood_high:map[student:map[gender:Mail name:Jason school:Public High School]]]: (interface {}) <nil>
    
    -Step19:
    {
      Name: "",
      Do: {
        {
          "name": "query",
          "desc": "query and register result as a yml string instead of object",
          "cmd": {
            "path": "nsw.",
            "reg": "city2"
          },
          "flags": {
            "ymlOnly"
          }
        },
        {
          "name": "trace",
          "cmd": "====>"
        },
        {
          "name": "printObj",
          "cmd": "{{.city2}}"
        },
        {
          "name": "print",
          "cmd": "{{.city2}}"
        },
        {
          "cmd": "{{.city2|len}}",
          "name": "print"
        },
        {
          "name": "trace",
          "cmd": "<===="
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
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
      "studentm": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "data_school_name": "",
      "studentx": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "name": "Emily",
            "school": "KINGS",
            "gender": "Female"
          }
        }
      }),
      "school_name": (*string)("The Kings"),
      "query_name": "jason",
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "name": "Grace",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "name": "Emily",
                "school": "KINGS"
              }
            }
          }
        }
      }),
      "studenty": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "studentz": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "student_info": (*map[interface {}]interface {})({
        "school": "The Kings",
        "name": "jason",
        "gender": "Male"
      }),
      "cityall": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        },
        "sg": {
          "student": {
            "school": "MLC",
            "gender": "Female",
            "name": "Grace"
          }
        }
      }),
      "nsw": {
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        },
        "sydney": {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "name": "Grace",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        }
      },
      "studento": (*map[interface {}]interface {})({
        "chatswood_high": {
          "student": {
            "gender": "Mail",
            "name": "Jason",
            "school": "Public High School"
          }
        }
      }),
      "studentn": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Grace",
        "school": "MLC"
      }),
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "studentx": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "name": "Emily",
            "school": "KINGS",
            "gender": "Female"
          }
        }
      }),
      "studentz": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "school_name": (*string)("The Kings"),
      "studentn": (*map[interface {}]interface {})({
        "school": "MLC",
        "gender": "Female",
        "name": "Grace"
      }),
      "query_name": "jason",
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "gender": "Female",
                "name": "Grace"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "name": "Emily",
                "school": "KINGS"
              }
            }
          }
        }
      }),
      "cityall": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        },
        "sg": {
          "student": {
            "school": "MLC",
            "gender": "Female",
            "name": "Grace"
          }
        }
      }),
      "data_school_name": "",
      "studentm": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "studenty": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "studento": (*map[interface {}]interface {})({
        "chatswood_high": {
          "student": {
            "school": "Public High School",
            "gender": "Mail",
            "name": "Jason"
          }
        }
      }),
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "nsw": {
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        },
        "sydney": {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "school": "MLC",
                "name": "Grace"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        }
      }
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "cityall": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        },
        "sg": {
          "student": {
            "school": "MLC",
            "gender": "Female",
            "name": "Grace"
          }
        }
      }),
      "nsw": {
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "gender": "Mail",
                "school": "Public High School",
                "name": "Jason"
              }
            }
          }
        },
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        }
      },
      "studento": (*map[interface {}]interface {})({
        "chatswood_high": {
          "student": {
            "school": "Public High School",
            "gender": "Mail",
            "name": "Jason"
          }
        }
      }),
      "studentn": (*map[interface {}]interface {})({
        "name": "Grace",
        "school": "MLC",
        "gender": "Female"
      }),
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "studentm": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "data_school_name": "",
      "studentx": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "name": "Emily",
            "school": "KINGS",
            "gender": "Female"
          }
        }
      }),
      "school_name": (*string)("The Kings"),
      "query_name": "jason",
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "school": "MLC",
                "gender": "Female",
                "name": "Grace"
              }
            }
          },
          {
            "kings": {
              "student": {
                "school": "KINGS",
                "gender": "Female",
                "name": "Emily"
              }
            }
          }
        }
      }),
      "studenty": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "studentz": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      })
    })
    
    map[path:nsw. reg:city2]
    ~SubStep1: [query: query and register result as a yml string instead of object ]
    (string) (len=11) "sub yml str"
    
    (string) (len=277) "chatswood:\n- chatswood_high:\n    student:\n      gender: Mail\n      name: Jason\n      school: Public High School\nsydney:\n- sg:\n    student:\n      gender: Female\n      name: Grace\n      school: MLC\n- kings:\n    student:\n      gender: Female\n      name: Emily\n      school: KINGS\n"
    
    ====>
    ~SubStep2: [trace:  ]
    Trace:====>
    {{.city2}}
    ~SubStep3: [printObj:  ]
    (string) (len=10) "{{.city2}}"
    
    object:
     chatswood:
    - chatswood_high:
        student:
          gender: Mail
          name: Jason
          school: Public High School
    sydney:
    - sg:
        student:
          gender: Female
          name: Grace
          school: MLC
    - kings:
        student:
          gender: Female
          name: Emily
          school: KINGS
    : (interface {}) <nil>
    
    {{.city2}}
    ~SubStep4: [print:  ]
    chatswood:
    - chatswood_high:
        student:
          gender: Mail
          name: Jason
          school: Public High School
    sydney:
    - sg:
        student:
          gender: Female
          name: Grace
          school: MLC
    - kings:
        student:
          gender: Female
          name: Emily
          school: KINGS
    
    {{.city2|len}}
    ~SubStep5: [print:  ]
    277
    <====
    ~SubStep6: [trace:  ]
    Trace:<====
    -Step20:
    {
      Name: "",
      Do: {
        {
          "name": "query",
          "desc": "query result from yml file using refdir",
          "cmd": {
            "path": "nsw.",
            "reg": "city2",
            "ymlfile": "d0100.yml",
            "refdir": "./tests/functests"
          },
          "flags": {
            "ymlOnly"
          }
        },
        {
          "name": "print",
          "cmd": "{{.city2}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
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
      "studentz": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "city2": "chatswood:\n- chatswood_high:\n    student:\n      gender: Mail\n      name: Jason\n      school: Public High School\nsydney:\n- sg:\n    student:\n      gender: Female\n      name: Grace\n      school: MLC\n- kings:\n    student:\n      gender: Female\n      name: Emily\n      school: KINGS\n",
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "school": "KINGS",
                "name": "Emily",
                "gender": "Female"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        }
      },
      "studentx": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "cityall": (*map[interface {}]interface {})({
        "sg": {
          "student": {
            "gender": "Female",
            "name": "Grace",
            "school": "MLC"
          }
        },
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        }
      }),
      "studentn": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Grace",
        "school": "MLC"
      }),
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "query_name": "jason",
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "studenty": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "school_name": (*string)("The Kings"),
      "data_school_name": "",
      "studentm": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "studento": (*map[interface {}]interface {})({
        "chatswood_high": {
          "student": {
            "gender": "Mail",
            "name": "Jason",
            "school": "Public High School"
          }
        }
      }),
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "school": "MLC",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "school": "KINGS",
                "gender": "Female"
              }
            }
          }
        }
      }),
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "school": "KINGS",
            "gender": "Female",
            "name": "Emily"
          }
        }
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "query_name": "jason",
      "school_name": (*string)("The Kings"),
      "data_school_name": "",
      "studentz": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "studentn": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Grace",
        "school": "MLC"
      }),
      "studenty": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "studentm": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "school": "MLC",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "school": "KINGS",
                "gender": "Female"
              }
            }
          }
        }
      }),
      "city2": "chatswood:\n- chatswood_high:\n    student:\n      gender: Mail\n      name: Jason\n      school: Public High School\nsydney:\n- sg:\n    student:\n      gender: Female\n      name: Grace\n      school: MLC\n- kings:\n    student:\n      gender: Female\n      name: Emily\n      school: KINGS\n",
      "cityall": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        },
        "sg": {
          "student": {
            "name": "Grace",
            "school": "MLC",
            "gender": "Female"
          }
        }
      }),
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        }
      }),
      "studentx": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "studento": (*map[interface {}]interface {})({
        "chatswood_high": {
          "student": {
            "name": "Jason",
            "school": "Public High School",
            "gender": "Mail"
          }
        }
      }),
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "school": "MLC",
                "name": "Grace"
              }
            }
          },
          {
            "kings": {
              "student": {
                "school": "KINGS",
                "name": "Emily",
                "gender": "Female"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        }
      },
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "studentz": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "city2": "chatswood:\n- chatswood_high:\n    student:\n      gender: Mail\n      name: Jason\n      school: Public High School\nsydney:\n- sg:\n    student:\n      gender: Female\n      name: Grace\n      school: MLC\n- kings:\n    student:\n      gender: Female\n      name: Emily\n      school: KINGS\n",
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "school": "MLC",
                "name": "Grace"
              }
            }
          },
          {
            "kings": {
              "student": {
                "school": "KINGS",
                "name": "Emily",
                "gender": "Female"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        }
      },
      "studentx": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "cityall": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        },
        "sg": {
          "student": {
            "gender": "Female",
            "name": "Grace",
            "school": "MLC"
          }
        }
      }),
      "studentn": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Grace",
        "school": "MLC"
      }),
      "query_name": "jason",
      "student_info": (*map[interface {}]interface {})({
        "school": "The Kings",
        "name": "jason",
        "gender": "Male"
      }),
      "studenty": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "school_name": (*string)("The Kings"),
      "data_school_name": "",
      "studentm": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "studento": (*map[interface {}]interface {})({
        "chatswood_high": {
          "student": {
            "name": "Jason",
            "school": "Public High School",
            "gender": "Mail"
          }
        }
      }),
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "school": "MLC",
                "gender": "Female"
              }
            }
          },
          {
            "kings": {
              "student": {
                "school": "KINGS",
                "gender": "Female",
                "name": "Emily"
              }
            }
          }
        }
      }),
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        }
      })
    })
    
    map[path:nsw. refdir:./tests/functests reg:city2 ymlfile:d0100.yml]
    ~SubStep1: [query: query result from yml file using refdir ]
    {{.city2}}
    ~SubStep2: [print:  ]
    sydney:
    - sg:
        student:
          name: Grace
          gender: Female
          school: MLC
    - kings:
        student:
          name: Emily
          gender: Female
          school: KINGS
    chatswood:
    - chatswood_high:
        student:
          name: Jason
          gender: Mail
          school: Public High School
    
    -Step21:
    {
      Name: "",
      Do: {
        {
          "name": "query",
          "desc": "query result from yml file using implicit global refdir",
          "cmd": {
            "ymlfile": "d0100.yml",
            "path": "nsw.",
            "reg": "city2"
          },
          "flags": {
            "ymlOnly"
          }
        },
        {
          "name": "print",
          "cmd": "{{.city2}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
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
      "school_name": (*string)("The Kings"),
      "studentx": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        }
      }),
      "studentm": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "city2": "sydney:\n- sg:\n    student:\n      name: Grace\n      gender: Female\n      school: MLC\n- kings:\n    student:\n      name: Emily\n      gender: Female\n      school: KINGS\nchatswood:\n- chatswood_high:\n    student:\n      name: Jason\n      gender: Mail\n      school: Public High School\n",
      "studento": (*map[interface {}]interface {})({
        "chatswood_high": {
          "student": {
            "gender": "Mail",
            "name": "Jason",
            "school": "Public High School"
          }
        }
      }),
      "query_name": "jason",
      "studentn": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Grace",
        "school": "MLC"
      }),
      "studentz": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "school": "Public High School",
                "name": "Jason",
                "gender": "Mail"
              }
            }
          }
        }
      },
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "name": "Grace",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "name": "Emily",
                "school": "KINGS"
              }
            }
          }
        }
      }),
      "data_school_name": "",
      "cityall": (*map[interface {}]interface {})({
        "sg": {
          "student": {
            "gender": "Female",
            "name": "Grace",
            "school": "MLC"
          }
        },
        "kings": {
          "student": {
            "name": "Emily",
            "school": "KINGS",
            "gender": "Female"
          }
        }
      }),
      "studenty": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "query_name": "jason",
      "nsw": {
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        },
        "sydney": {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "school": "MLC",
                "name": "Grace"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "school": "KINGS",
                "name": "Emily"
              }
            }
          }
        }
      },
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "city2": "sydney:\n- sg:\n    student:\n      name: Grace\n      gender: Female\n      school: MLC\n- kings:\n    student:\n      name: Emily\n      gender: Female\n      school: KINGS\nchatswood:\n- chatswood_high:\n    student:\n      name: Jason\n      gender: Mail\n      school: Public High School\n",
      "studentm": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "cityall": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "school": "KINGS",
            "gender": "Female",
            "name": "Emily"
          }
        },
        "sg": {
          "student": {
            "school": "MLC",
            "gender": "Female",
            "name": "Grace"
          }
        }
      }),
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "studentx": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "school_name": (*string)("The Kings"),
      "studento": (*map[interface {}]interface {})({
        "chatswood_high": {
          "student": {
            "school": "Public High School",
            "gender": "Mail",
            "name": "Jason"
          }
        }
      }),
      "studentn": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Grace",
        "school": "MLC"
      }),
      "studentz": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "name": "Grace",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "school": "KINGS",
                "gender": "Female"
              }
            }
          }
        }
      }),
      "data_school_name": "",
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        }
      }),
      "studenty": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "studenty": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "data_school_name": "",
      "cityall": (*map[interface {}]interface {})({
        "sg": {
          "student": {
            "school": "MLC",
            "gender": "Female",
            "name": "Grace"
          }
        },
        "kings": {
          "student": {
            "name": "Emily",
            "school": "KINGS",
            "gender": "Female"
          }
        }
      }),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        }
      }),
      "school_name": (*string)("The Kings"),
      "studentx": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "studento": (*map[interface {}]interface {})({
        "chatswood_high": {
          "student": {
            "school": "Public High School",
            "gender": "Mail",
            "name": "Jason"
          }
        }
      }),
      "query_name": "jason",
      "studentn": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Grace",
        "school": "MLC"
      }),
      "studentz": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "studentm": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "city2": "sydney:\n- sg:\n    student:\n      name: Grace\n      gender: Female\n      school: MLC\n- kings:\n    student:\n      name: Emily\n      gender: Female\n      school: KINGS\nchatswood:\n- chatswood_high:\n    student:\n      name: Jason\n      gender: Mail\n      school: Public High School\n",
      "nsw": {
        "sydney": {
          {
            "sg": {
              "student": {
                "name": "Grace",
                "gender": "Female",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        },
        "chatswood": {
          {
            "chatswood_high": {
              "student": {
                "school": "Public High School",
                "name": "Jason",
                "gender": "Mail"
              }
            }
          }
        }
      },
      "city": (*[]interface {})({
        {
          {
            "sg": {
              "student": {
                "gender": "Female",
                "name": "Grace",
                "school": "MLC"
              }
            }
          },
          {
            "kings": {
              "student": {
                "gender": "Female",
                "name": "Emily",
                "school": "KINGS"
              }
            }
          }
        }
      })
    })
    
    map[path:nsw. reg:city2 ymlfile:d0100.yml]
    ~SubStep1: [query: query result from yml file using implicit global refdir ]
    {{.city2}}
    ~SubStep2: [print:  ]
    sydney:
    - sg:
        student:
          name: Grace
          gender: Female
          school: MLC
    - kings:
        student:
          name: Emily
          gender: Female
          school: KINGS
    chatswood:
    - chatswood_high:
        student:
          name: Jason
          gender: Mail
          school: Public High School
    
    
```

##### Logs with different verbose level
* [c0100 log - verbose level v](../../logs/c0100_v)
* [c0100 log - verbose level vv](../../logs/c0100_vv)
* [c0100 log - verbose level vvv](../../logs/c0100_vvv)
* [c0100 log - verbose level vvvv](../../logs/c0100_vvvv)
* [c0100 log - verbose level vvvvv](../../logs/c0100_vvvvv)

##### References
* [Related Chapter](../../object-oriented/c0100)
