---
title: "c0100_vvvv"
date: 2020-07-01T15:34:34+77:00
draft: false
weight: 11003

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
                 Verbose -> vvvv
              ModuleName -> sharp_wozniak9
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0100
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [sharp_wozniak9] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "query_name": "jason",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
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
      }
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "query_name": "jason",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
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
      "query_name": "jason",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
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
                "gender": "Mail",
                "school": "Public High School",
                "name": "Jason"
              }
            }
          }
        }
      },
      "ymlstr": "student:\n  name: jason\n  gender: Male\n  school: The Kings\n"
    })
    
    sharp_wozniak9: overall final exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
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
      "ymlstr": "student:\n  name: jason\n  gender: Male\n  school: The Kings\n",
      "query_name": "jason"
    })
    
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
      "school_name": (*string)("The Kings"),
      "query_name": "jason",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
    })
    
    sharp_wozniak9: overall final exec vars:
    
    (*core.Cache)({
      "school_name": (*string)("The Kings"),
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
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        }
      }
    })
    
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
            "ymlkey": "ymlstr",
            "path": "student",
            "reg": "student_info"
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
      "ymlstr": "student: |\n  name: jason\n  gender: Male\n  school: The Kings\n",
      "query_name": "jason",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
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
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        }
      },
      "school_name": (*string)("The Kings")
    })
    
    sharp_wozniak9: overall final exec vars:
    
    (*core.Cache)({
      "query_name": "jason",
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
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        }
      },
      "school_name": (*string)("The Kings"),
      "ymlstr": "student: |\n  name: jason\n  gender: Male\n  school: The Kings\n"
    })
    
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
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "query_name": "jason",
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    })
    
    sharp_wozniak9: overall final exec vars:
    
    (*core.Cache)({
      "query_name": "jason",
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
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
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      })
    })
    
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
            "path": "student.school",
            "reg": "local_school_name",
            "ymlkey": "ymlstr"
          },
          "flags": {
            "localonly"
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
      "query_name": "jason",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
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
      "school_name": (*string)("The Kings"),
      "ymlstr": "student:\n  name: jason\n  gender: Male\n  school: The Kings\n",
      "student_info": (*map[interface {}]interface {})({
        "gender": "Male",
        "school": "The Kings",
        "name": "jason"
      })
    })
    
    sharp_wozniak9: overall final exec vars:
    
    (*core.Cache)({
      "student_info": (*map[interface {}]interface {})({
        "school": "The Kings",
        "name": "jason",
        "gender": "Male"
      }),
      "query_name": "jason",
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
      "ymlstr": "student:\n  name: jason\n  gender: Male\n  school: The Kings\n"
    })
    
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
      "query_name": "jason",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
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
                "school": "Public High School",
                "name": "Jason",
                "gender": "Mail"
              }
            }
          }
        }
      },
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      })
    })
    
    sharp_wozniak9: overall final exec vars:
    
    (*core.Cache)({
      "query_name": "jason",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
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
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "gender": "Male",
        "school": "The Kings",
        "name": "jason"
      })
    })
    
    ~SubStep1: [print:  ]
    <no value>
    -Step7:
    {
      Name: "",
      Do: {
        {
          "desc": "query from cached vars only",
          "cmd": {
            "path": "nsw.sydney.sg.student.school",
            "reg": "data_school_name"
          },
          "name": "query"
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
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "query_name": "jason",
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
      }
    })
    
    sharp_wozniak9: overall final exec vars:
    
    (*core.Cache)({
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "query_name": "jason",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
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
      "school_name": (*string)("The Kings")
    })
    
    ~SubStep1: [query: query from cached vars only ]
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
      "student_info": (*map[interface {}]interface {})({
        "school": "The Kings",
        "name": "jason",
        "gender": "Male"
      }),
      "data_school_name": "",
      "query_name": "jason",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
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
      "school_name": (*string)("The Kings")
    })
    
    sharp_wozniak9: overall final exec vars:
    
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
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "school": "The Kings",
        "name": "jason",
        "gender": "Male"
      }),
      "data_school_name": "",
      "query_name": "jason",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
    })
    
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
          "name": "printobj"
        },
        {
          "cmd": "{{.school_name_list}}",
          "name": "print"
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
        "gender": "Male",
        "school": "The Kings",
        "name": "jason"
      }),
      "data_school_name": "",
      "query_name": "jason",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
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
      "school_name": (*string)("The Kings")
    })
    
    sharp_wozniak9: overall final exec vars:
    
    (*core.Cache)({
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
      },
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "data_school_name": "",
      "query_name": "jason",
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    })
    
    ~SubStep1: [query: query from cached vars and put result into a list/array ]
    ~SubStep2: [printobj:  ]
    (string) (len=21) "{{.school_name_list}}"
    
    object:
     [MLC KINGS]: (interface {}) <nil>
    
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
          "name": "printobj"
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
      "school_name": (*string)("The Kings"),
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
      "query_name": "jason",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
    })
    
    sharp_wozniak9: overall final exec vars:
    
    (*core.Cache)({
      "query_name": "jason",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
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
      })
    })
    
    ~SubStep1: [query: query a sub node ]
    ~SubStep2: [printobj:  ]
    (string) (len=9) "{{.city}}"
    
    object:
     [[map[sg:map[student:map[gender:Female name:Grace school:MLC]]] map[kings:map[student:map[gender:Female name:Emily school:KINGS]]]]]: (interface {}) <nil>
    
    ~SubStep3: [print:  ]
    [[map[sg:map[student:map[gender:Female name:Grace school:MLC]]] map[kings:map[student:map[gender:Female name:Emily school:KINGS]]]]]
    -Step11:
    {
      Name: "",
      Do: {
        {
          "desc": "query a selected indexed node from a array",
          "cmd": {
            "path": "nsw.sydney.[1]",
            "reg": "city1"
          },
          "name": "query"
        },
        {
          "cmd": "{{.city1}}",
          "name": "printobj"
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
      "query_name": "jason",
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
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      })
    })
    
    sharp_wozniak9: overall final exec vars:
    
    (*core.Cache)({
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
                "gender": "Female",
                "name": "Emily",
                "school": "KINGS"
              }
            }
          }
        }
      }),
      "query_name": "jason",
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
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "school": "The Kings",
        "name": "jason",
        "gender": "Male"
      }),
      "data_school_name": ""
    })
    
    ~SubStep1: [query: query a selected indexed node from a array ]
    ~SubStep2: [printobj:  ]
    (string) (len=10) "{{.city1}}"
    
    object:
     map[kings:map[student:map[gender:Female name:Emily school:KINGS]]]: (interface {}) <nil>
    
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
          "name": "printobj",
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
      "query_name": "jason",
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
                "gender": "Female",
                "name": "Emily",
                "school": "KINGS"
              }
            }
          }
        }
      }),
      "school_name": (*string)("The Kings"),
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
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
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
                "school": "Public High School",
                "name": "Jason",
                "gender": "Mail"
              }
            }
          }
        }
      }
    })
    
    sharp_wozniak9: overall final exec vars:
    
    (*core.Cache)({
      "student_info": (*map[interface {}]interface {})({
        "gender": "Male",
        "school": "The Kings",
        "name": "jason"
      }),
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
                "school": "Public High School",
                "name": "Jason",
                "gender": "Mail"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "data_school_name": "",
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
      "school_name": (*string)("The Kings"),
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
      })
    })
    
    ~SubStep1: [query: query all nodes from an array ]
    ~SubStep2: [printobj:  ]
    (string) (len=12) "{{.cityall}}"
    
    object:
     map[kings:map[student:map[gender:Female name:Emily school:KINGS]] sg:map[student:map[gender:Female name:Grace school:MLC]]]: (interface {}) <nil>
    
    ~SubStep3: [print:  ]
    map[kings:map[student:map[gender:Female name:Emily school:KINGS]] sg:map[student:map[gender:Female name:Grace school:MLC]]]
    -Step13:
    {
      Name: "",
      Do: {
        {
          "desc": "query result matching the criteria",
          "cmd": {
            "path": "nsw.sydney.[*].*(name==Emily)",
            "reg": "studentx"
          },
          "name": "query"
        },
        {
          "name": "printobj",
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
      "query_name": "jason",
      "school_name": (*string)("The Kings"),
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
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
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "data_school_name": ""
    })
    
    sharp_wozniak9: overall final exec vars:
    
    (*core.Cache)({
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
                "school": "KINGS",
                "name": "Emily",
                "gender": "Female"
              }
            }
          }
        }
      },
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
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
      "query_name": "jason",
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
      "data_school_name": ""
    })
    
    ~SubStep1: [query: query result matching the criteria ]
    ~SubStep2: [printobj:  ]
    (string) (len=13) "{{.studentx}}"
    
    object:
     map[gender:Female name:Emily school:KINGS]: (interface {}) <nil>
    
    ~SubStep3: [print:  ]
    map[gender:Female name:Emily school:KINGS]
    -Step14:
    {
      Name: "",
      Do: {
        {
          "name": "query",
          "desc": "query result matching the criteria",
          "cmd": {
            "path": "nsw.sydney.[1].*(name==Emily)",
            "reg": "studenty"
          }
        },
        {
          "name": "printobj",
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
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "data_school_name": "",
      "studentx": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
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
      "school_name": (*string)("The Kings"),
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
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
      "query_name": "jason",
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
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
      })
    })
    
    sharp_wozniak9: overall final exec vars:
    
    (*core.Cache)({
      "query_name": "jason",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
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
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
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
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
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
      "school_name": (*string)("The Kings"),
      "studentx": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      })
    })
    
    ~SubStep1: [query: query result matching the criteria ]
    ~SubStep2: [printobj:  ]
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
          "name": "printobj",
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
                "gender": "Female",
                "name": "Emily",
                "school": "KINGS"
              }
            }
          }
        }
      }),
      "query_name": "jason",
      "student_info": (*map[interface {}]interface {})({
        "gender": "Male",
        "school": "The Kings",
        "name": "jason"
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
      "studenty": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "data_school_name": "",
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "name": "Emily",
            "school": "KINGS",
            "gender": "Female"
          }
        }
      }),
      "studentx": (*map[interface {}]interface {})({
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
      "school_name": (*string)("The Kings")
    })
    
    sharp_wozniak9: overall final exec vars:
    
    (*core.Cache)({
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "query_name": "jason",
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "name": "Emily",
            "school": "KINGS",
            "gender": "Female"
          }
        }
      }),
      "studentx": (*map[interface {}]interface {})({
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
        }
      },
      "data_school_name": "",
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
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
      "studenty": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "school_name": (*string)("The Kings"),
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
    
    ~SubStep1: [query: query result matching the criteria ]
    ~SubStep2: [printobj:  ]
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
          "name": "printobj",
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
      "studentz": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
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
      "studenty": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
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
      "query_name": "jason",
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
      "school_name": (*string)("The Kings"),
      "data_school_name": "",
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "studentx": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      })
    })
    
    sharp_wozniak9: overall final exec vars:
    
    (*core.Cache)({
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "school": "KINGS",
            "gender": "Female",
            "name": "Emily"
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
      "studentz": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "data_school_name": "",
      "query_name": "jason",
      "student_info": (*map[interface {}]interface {})({
        "gender": "Male",
        "school": "The Kings",
        "name": "jason"
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
      },
      "school_name": (*string)("The Kings"),
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "studentx": (*map[interface {}]interface {})({
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
      })
    })
    
    ~SubStep1: [query: query result matching the criteria ]
    ~SubStep2: [printobj:  ]
    (string) (len=13) "{{.studentm}}"
    
    object:
     map[gender:Female name:Emily school:KINGS]: (interface {}) <nil>
    
    -Step17:
    {
      Name: "",
      Do: {
        {
          "name": "query",
          "desc": "query result matching the criteria",
          "cmd": {
            "path": "nsw.sydney.[*].*(name==Grace)",
            "reg": "studentn"
          }
        },
        {
          "name": "printobj",
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
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "school": "KINGS",
            "gender": "Female",
            "name": "Emily"
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
      "query_name": "jason",
      "studentz": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
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
      "school_name": (*string)("The Kings"),
      "studenty": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      })
    })
    
    sharp_wozniak9: overall final exec vars:
    
    (*core.Cache)({
      "studentz": (*map[interface {}]interface {})({
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
      "studenty": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
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
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
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
                "gender": "Mail",
                "school": "Public High School",
                "name": "Jason"
              }
            }
          }
        }
      },
      "studentm": (*map[interface {}]interface {})({
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
            "name": "Emily",
            "school": "KINGS",
            "gender": "Female"
          }
        }
      }),
      "query_name": "jason"
    })
    
    ~SubStep1: [query: query result matching the criteria ]
    ~SubStep2: [printobj:  ]
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
            "path": "nsw.chatswood.[*]",
            "reg": "studento"
          }
        },
        {
          "name": "printobj",
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
      "data_school_name": "",
      "studentz": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "studenty": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "studentn": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Grace",
        "school": "MLC"
      }),
      "query_name": "jason",
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
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
      "studentm": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
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
    })
    
    sharp_wozniak9: overall final exec vars:
    
    (*core.Cache)({
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "school_name": (*string)("The Kings"),
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "studenty": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "studentm": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "data_school_name": "",
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
      "studentn": (*map[interface {}]interface {})({
        "name": "Grace",
        "school": "MLC",
        "gender": "Female"
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
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "school": "KINGS",
            "gender": "Female",
            "name": "Emily"
          }
        }
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
      "query_name": "jason"
    })
    
    ~SubStep1: [query: query result matching the criteria ]
    ~SubStep2: [printobj:  ]
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
            "ymlonly"
          }
        },
        {
          "name": "trace",
          "cmd": "====>"
        },
        {
          "name": "printobj",
          "cmd": "{{.city2}}"
        },
        {
          "name": "print",
          "cmd": "{{.city2}}"
        },
        {
          "name": "print",
          "cmd": "{{.city2|len}}"
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
      "studento": (*map[interface {}]interface {})({
        "chatswood_high": {
          "student": {
            "school": "Public High School",
            "gender": "Mail",
            "name": "Jason"
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
      "school_name": (*string)("The Kings"),
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
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
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "data_school_name": "",
      "studentz": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
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
      "studentx": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      })
    })
    
    sharp_wozniak9: overall final exec vars:
    
    (*core.Cache)({
      "school_name": (*string)("The Kings"),
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
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
      "studentz": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "studentn": (*map[interface {}]interface {})({
        "name": "Grace",
        "school": "MLC",
        "gender": "Female"
      }),
      "query_name": "jason",
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
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "studentx": (*map[interface {}]interface {})({
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
      "studentm": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
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
      "data_school_name": "",
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "name": "Emily",
            "school": "KINGS",
            "gender": "Female"
          }
        }
      })
    })
    
    ~SubStep1: [query: query and register result as a yml string instead of object ]
    ~SubStep2: [trace:  ]
    Trace:====>
    ~SubStep3: [printobj:  ]
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
    
    ~SubStep5: [print:  ]
    277
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
            "ymlfile": "d0100.yml",
            "refdir": "./tests/functests",
            "path": "nsw.",
            "reg": "city2"
          },
          "flags": {
            "ymlonly"
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
      "data_school_name": "",
      "query_name": "jason",
      "school_name": (*string)("The Kings"),
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "gender": "Female",
            "name": "Emily",
            "school": "KINGS"
          }
        }
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
      "studentx": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
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
      "studenty": (*map[interface {}]interface {})({
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
      "studentm": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
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
      "studento": (*map[interface {}]interface {})({
        "chatswood_high": {
          "student": {
            "gender": "Mail",
            "name": "Jason",
            "school": "Public High School"
          }
        }
      }),
      "studentz": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "city2": "chatswood:\n- chatswood_high:\n    student:\n      gender: Mail\n      name: Jason\n      school: Public High School\nsydney:\n- sg:\n    student:\n      gender: Female\n      name: Grace\n      school: MLC\n- kings:\n    student:\n      gender: Female\n      name: Emily\n      school: KINGS\n"
    })
    
    sharp_wozniak9: overall final exec vars:
    
    (*core.Cache)({
      "studento": (*map[interface {}]interface {})({
        "chatswood_high": {
          "student": {
            "name": "Jason",
            "school": "Public High School",
            "gender": "Mail"
          }
        }
      }),
      "query_name": "jason",
      "studentz": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "city2": "chatswood:\n- chatswood_high:\n    student:\n      gender: Mail\n      name: Jason\n      school: Public High School\nsydney:\n- sg:\n    student:\n      gender: Female\n      name: Grace\n      school: MLC\n- kings:\n    student:\n      gender: Female\n      name: Emily\n      school: KINGS\n",
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
      "school_name": (*string)("The Kings"),
      "studenty": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "data_school_name": "",
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "name": "Emily",
            "school": "KINGS",
            "gender": "Female"
          }
        }
      }),
      "studentn": (*map[interface {}]interface {})({
        "name": "Grace",
        "school": "MLC",
        "gender": "Female"
      }),
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
      "studentm": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
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
      "student_info": (*map[interface {}]interface {})({
        "gender": "Male",
        "school": "The Kings",
        "name": "jason"
      })
    })
    
    ~SubStep1: [query: query result from yml file using refdir ]
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
            "ymlonly"
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
      "studentn": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Grace",
        "school": "MLC"
      }),
      "query_name": "jason",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "studentm": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
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
      "data_school_name": "",
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
            "name": "Grace",
            "school": "MLC",
            "gender": "Female"
          }
        }
      }),
      "school_name": (*string)("The Kings"),
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
      "studentx": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "city2": "sydney:\n- sg:\n    student:\n      name: Grace\n      gender: Female\n      school: MLC\n- kings:\n    student:\n      name: Emily\n      gender: Female\n      school: KINGS\nchatswood:\n- chatswood_high:\n    student:\n      name: Jason\n      gender: Mail\n      school: Public High School\n",
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
      "studento": (*map[interface {}]interface {})({
        "chatswood_high": {
          "student": {
            "gender": "Mail",
            "name": "Jason",
            "school": "Public High School"
          }
        }
      }),
      "studentz": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "studenty": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      })
    })
    
    sharp_wozniak9: overall final exec vars:
    
    (*core.Cache)({
      "data_school_name": "",
      "studentz": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "studentn": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Grace",
        "school": "MLC"
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
      "studentx": (*map[interface {}]interface {})({
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
      "studentm": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "studenty": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "city2": "sydney:\n- sg:\n    student:\n      name: Grace\n      gender: Female\n      school: MLC\n- kings:\n    student:\n      name: Emily\n      gender: Female\n      school: KINGS\nchatswood:\n- chatswood_high:\n    student:\n      name: Jason\n      gender: Mail\n      school: Public High School\n",
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
    
    ~SubStep1: [query: query result from yml file using implicit global refdir ]
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
* [Related Chapter](../../query-object/c0100)
