---
title: "c0096_vvvvv"
date: 2020-06-25T01:55:54+66:00
draft: false
weight: 10964

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0096
                 Verbose -> vvvvv
              ModuleName -> sharp_banach7
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0096
    -------full vars in scopes------
    (*impl.Scopes)(0xc00017d3c0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [sharp_banach7] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "school_details_object": {
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        },
        "ranking": "No 5"
      },
      "root": {
        "parent": {
          "school_details_object": {
            "school": {
              "name": "sydney grammar",
              "address": "1 fox road, sydney, nsw 2000"
            },
            "principals": {
              "peter",
              "tom",
              "jane"
            },
            "ranking": "No 5"
          }
        }
      }
    }
    
    (core.Cache) (len=2) {
     (string) (len=4) "root": (map[string]interface {}) (len=1) {
      (string) (len=6) "parent": (map[string]interface {}) (len=1) {
       (string) (len=21) "school_details_object": (map[string]interface {}) (len=3) {
        (string) (len=6) "school": (map[string]interface {}) (len=2) {
         (string) (len=4) "name": (string) (len=14) "sydney grammar",
         (string) (len=7) "address": (string) (len=28) "1 fox road, sydney, nsw 2000"
        },
        (string) (len=10) "principals": ([]interface {}) (len=3 cap=3) {
         (string) (len=5) "peter",
         (string) (len=3) "tom",
         (string) (len=4) "jane"
        },
        (string) (len=7) "ranking": (string) (len=4) "No 5"
       }
      }
     },
     (string) (len=21) "school_details_object": (map[string]interface {}) (len=3) {
      (string) (len=6) "school": (map[string]interface {}) (len=2) {
       (string) (len=4) "name": (string) (len=14) "sydney grammar",
       (string) (len=7) "address": (string) (len=28) "1 fox road, sydney, nsw 2000"
      },
      (string) (len=10) "principals": ([]interface {}) (len=3 cap=3) {
       (string) (len=5) "peter",
       (string) (len=3) "tom",
       (string) (len=4) "jane"
      },
      (string) (len=7) "ranking": (string) (len=4) "No 5"
     }
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "root": {
        "parent": {
          "school_details_object": {
            "principals": {
              "peter",
              "tom",
              "jane"
            },
            "ranking": "No 5",
            "school": {
              "name": "sydney grammar",
              "address": "1 fox road, sydney, nsw 2000"
            }
          }
        }
      },
      "school_details_object": {
        "ranking": "No 5",
        "school": {
          "address": "1 fox road, sydney, nsw 2000",
          "name": "sydney grammar"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
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
          "name": "template",
          "desc": "render the template file using above dynamic variable from defined var",
          "cmd": {
            "src": "./tests/functests/d0079.template",
            "dest": "/tmp/myschool.txt",
            "datakey": "school_details_object"
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
      "root": {
        "parent": {
          "school_details_object": {
            "school": {
              "name": "sydney grammar",
              "address": "1 fox road, sydney, nsw 2000"
            },
            "principals": {
              "peter",
              "tom",
              "jane"
            },
            "ranking": "No 5"
          }
        }
      },
      "school_details_object": {
        "ranking": "No 5",
        "school": {
          "address": "1 fox road, sydney, nsw 2000",
          "name": "sydney grammar"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        }
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "root": {
        "parent": {
          "school_details_object": {
            "ranking": "No 5",
            "school": {
              "name": "sydney grammar",
              "address": "1 fox road, sydney, nsw 2000"
            },
            "principals": {
              "peter",
              "tom",
              "jane"
            }
          }
        }
      },
      "school_details_object": {
        "ranking": "No 5",
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        }
      }
    }
    
    
    sharp_banach7: overall final exec vars:
    
    (*core.Cache)({
      "root": {
        "parent": {
          "school_details_object": {
            "school": {
              "name": "sydney grammar",
              "address": "1 fox road, sydney, nsw 2000"
            },
            "principals": {
              "peter",
              "tom",
              "jane"
            },
            "ranking": "No 5"
          }
        }
      },
      "school_details_object": {
        "principals": {
          "peter",
          "tom",
          "jane"
        },
        "ranking": "No 5",
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        }
      }
    })
    
    map[datakey:school_details_object dest:/tmp/myschool.txt src:./tests/functests/d0079.template]
    ~SubStep1: [template: render the template file using above dynamic variable from defined var ]
    -Step2:
    {
      Name: "",
      Do: {
        {
          "desc": "read content of a file and register it to a var",
          "cmd": {
            "dir": "/tmp",
            "reg": "my_school",
            "filename": "myschool.txt"
          },
          "name": "readfile"
        },
        {
          "name": "print",
          "cmd": "{{.my_school}}"
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
      "root": {
        "parent": {
          "school_details_object": {
            "school": {
              "name": "sydney grammar",
              "address": "1 fox road, sydney, nsw 2000"
            },
            "principals": {
              "peter",
              "tom",
              "jane"
            },
            "ranking": "No 5"
          }
        }
      },
      "school_details_object": {
        "principals": {
          "peter",
          "tom",
          "jane"
        },
        "ranking": "No 5",
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        }
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "root": {
        "parent": {
          "school_details_object": {
            "principals": {
              "peter",
              "tom",
              "jane"
            },
            "ranking": "No 5",
            "school": {
              "name": "sydney grammar",
              "address": "1 fox road, sydney, nsw 2000"
            }
          }
        }
      },
      "school_details_object": {
        "principals": {
          "peter",
          "tom",
          "jane"
        },
        "ranking": "No 5",
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        }
      }
    }
    
    
    sharp_banach7: overall final exec vars:
    
    (*core.Cache)({
      "root": {
        "parent": {
          "school_details_object": {
            "school": {
              "name": "sydney grammar",
              "address": "1 fox road, sydney, nsw 2000"
            },
            "principals": {
              "peter",
              "tom",
              "jane"
            },
            "ranking": "No 5"
          }
        }
      },
      "school_details_object": {
        "ranking": "No 5",
        "school": {
          "address": "1 fox road, sydney, nsw 2000",
          "name": "sydney grammar"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        }
      }
    })
    
    map[dir:/tmp filename:myschool.txt reg:my_school]
    ~SubStep1: [readfile: read content of a file and register it to a var ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "school_details_object": {
        "ranking": "No 5",
        "school": {
          "address": "1 fox road, sydney, nsw 2000",
          "name": "sydney grammar"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        }
      },
      "my_school": "\n\nMy school name is: sydney grammar, it is located\nat 1 fox road, sydney, nsw 2000\n\n\nWe have got  peter,  tom,  jane,  as our principals\n\nOur school ranking last year is No 5\n",
      "root": {
        "parent": {
          "school_details_object": {
            "school": {
              "name": "sydney grammar",
              "address": "1 fox road, sydney, nsw 2000"
            },
            "principals": {
              "peter",
              "tom",
              "jane"
            },
            "ranking": "No 5"
          }
        }
      }
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "root": {
        "parent": {
          "school_details_object": {
            "school": {
              "address": "1 fox road, sydney, nsw 2000",
              "name": "sydney grammar"
            },
            "principals": {
              "peter",
              "tom",
              "jane"
            },
            "ranking": "No 5"
          }
        }
      },
      "school_details_object": {
        "principals": {
          "peter",
          "tom",
          "jane"
        },
        "ranking": "No 5",
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        }
      },
      "my_school": "\n\nMy school name is: sydney grammar, it is located\nat 1 fox road, sydney, nsw 2000\n\n\nWe have got  peter,  tom,  jane,  as our principals\n\nOur school ranking last year is No 5\n"
    })
    
    {{.my_school}}
    ~SubStep2: [print:  ]
    
    
    My school name is: sydney grammar, it is located
    at 1 fox road, sydney, nsw 2000
    
    
    We have got  peter,  tom,  jane,  as our principals
    
    Our school ranking last year is No 5
    
    -Step3:
    {
      Name: "",
      Do: {
        {
          "cmd": {
            "src": "./tests/functests/d0079.template",
            "dest": "/tmp/myschool.txt",
            "datapath": "root.parent.school_details_object"
          },
          "name": "template",
          "desc": "render the template file using above dynamic variable from defined var"
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
      "root": {
        "parent": {
          "school_details_object": {
            "school": {
              "name": "sydney grammar",
              "address": "1 fox road, sydney, nsw 2000"
            },
            "principals": {
              "peter",
              "tom",
              "jane"
            },
            "ranking": "No 5"
          }
        }
      },
      "school_details_object": {
        "ranking": "No 5",
        "school": {
          "address": "1 fox road, sydney, nsw 2000",
          "name": "sydney grammar"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        }
      },
      "my_school": "\n\nMy school name is: sydney grammar, it is located\nat 1 fox road, sydney, nsw 2000\n\n\nWe have got  peter,  tom,  jane,  as our principals\n\nOur school ranking last year is No 5\n"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "root": {
        "parent": {
          "school_details_object": {
            "principals": {
              "peter",
              "tom",
              "jane"
            },
            "ranking": "No 5",
            "school": {
              "name": "sydney grammar",
              "address": "1 fox road, sydney, nsw 2000"
            }
          }
        }
      },
      "school_details_object": {
        "ranking": "No 5",
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        }
      },
      "my_school": "\n\nMy school name is: sydney grammar, it is located\nat 1 fox road, sydney, nsw 2000\n\n\nWe have got  peter,  tom,  jane,  as our principals\n\nOur school ranking last year is No 5\n"
    }
    
    
    sharp_banach7: overall final exec vars:
    
    (*core.Cache)({
      "my_school": "\n\nMy school name is: sydney grammar, it is located\nat 1 fox road, sydney, nsw 2000\n\n\nWe have got  peter,  tom,  jane,  as our principals\n\nOur school ranking last year is No 5\n",
      "root": {
        "parent": {
          "school_details_object": {
            "school": {
              "name": "sydney grammar",
              "address": "1 fox road, sydney, nsw 2000"
            },
            "principals": {
              "peter",
              "tom",
              "jane"
            },
            "ranking": "No 5"
          }
        }
      },
      "school_details_object": {
        "ranking": "No 5",
        "school": {
          "address": "1 fox road, sydney, nsw 2000",
          "name": "sydney grammar"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        }
      }
    })
    
    map[datapath:root.parent.school_details_object dest:/tmp/myschool.txt src:./tests/functests/d0079.template]
    ~SubStep1: [template: render the template file using above dynamic variable from defined var ]
    (string) (len=11) "sub yml str"
    
    (string) (len=183) "parent:\n  school_details_object:\n    principals:\n    - peter\n    - tom\n    - jane\n    ranking: No 5\n    school:\n      address: 1 fox road, sydney, nsw 2000\n      name: sydney grammar\n"
    
    sub object::
    (*map[interface {}]interface {})({
      "principals": {
        "peter",
        "tom",
        "jane"
      },
      "ranking": "No 5",
      "school": {
        "name": "sydney grammar",
        "address": "1 fox road, sydney, nsw 2000"
      }
    })
    
    -Step4:
    {
      Name: "",
      Do: {
        {
          "cmd": {
            "filename": "myschool.txt",
            "dir": "/tmp",
            "reg": "my_school"
          },
          "name": "readfile",
          "desc": "read content of a file and register it to a var"
        },
        {
          "name": "print",
          "cmd": "{{.my_school}}"
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
      "root": {
        "parent": {
          "school_details_object": {
            "principals": {
              "peter",
              "tom",
              "jane"
            },
            "ranking": "No 5",
            "school": {
              "name": "sydney grammar",
              "address": "1 fox road, sydney, nsw 2000"
            }
          }
        }
      },
      "school_details_object": {
        "ranking": "No 5",
        "school": {
          "address": "1 fox road, sydney, nsw 2000",
          "name": "sydney grammar"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        }
      },
      "my_school": "\n\nMy school name is: sydney grammar, it is located\nat 1 fox road, sydney, nsw 2000\n\n\nWe have got  peter,  tom,  jane,  as our principals\n\nOur school ranking last year is No 5\n"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "root": {
        "parent": {
          "school_details_object": {
            "principals": {
              "peter",
              "tom",
              "jane"
            },
            "ranking": "No 5",
            "school": {
              "address": "1 fox road, sydney, nsw 2000",
              "name": "sydney grammar"
            }
          }
        }
      },
      "school_details_object": {
        "ranking": "No 5",
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        }
      },
      "my_school": "\n\nMy school name is: sydney grammar, it is located\nat 1 fox road, sydney, nsw 2000\n\n\nWe have got  peter,  tom,  jane,  as our principals\n\nOur school ranking last year is No 5\n"
    }
    
    
    sharp_banach7: overall final exec vars:
    
    (*core.Cache)({
      "school_details_object": {
        "ranking": "No 5",
        "school": {
          "address": "1 fox road, sydney, nsw 2000",
          "name": "sydney grammar"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        }
      },
      "my_school": "\n\nMy school name is: sydney grammar, it is located\nat 1 fox road, sydney, nsw 2000\n\n\nWe have got  peter,  tom,  jane,  as our principals\n\nOur school ranking last year is No 5\n",
      "root": {
        "parent": {
          "school_details_object": {
            "school": {
              "name": "sydney grammar",
              "address": "1 fox road, sydney, nsw 2000"
            },
            "principals": {
              "peter",
              "tom",
              "jane"
            },
            "ranking": "No 5"
          }
        }
      }
    })
    
    map[dir:/tmp filename:myschool.txt reg:my_school]
    ~SubStep1: [readfile: read content of a file and register it to a var ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "my_school": "\n\nMy school name is: sydney grammar, it is located\nat 1 fox road, sydney, nsw 2000\n\n\nWe have got  peter,  tom,  jane,  as our principals\n\nOur school ranking last year is No 5\n",
      "root": {
        "parent": {
          "school_details_object": {
            "school": {
              "name": "sydney grammar",
              "address": "1 fox road, sydney, nsw 2000"
            },
            "principals": {
              "peter",
              "tom",
              "jane"
            },
            "ranking": "No 5"
          }
        }
      },
      "school_details_object": {
        "ranking": "No 5",
        "school": {
          "address": "1 fox road, sydney, nsw 2000",
          "name": "sydney grammar"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        }
      }
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "root": {
        "parent": {
          "school_details_object": {
            "principals": {
              "peter",
              "tom",
              "jane"
            },
            "ranking": "No 5",
            "school": {
              "address": "1 fox road, sydney, nsw 2000",
              "name": "sydney grammar"
            }
          }
        }
      },
      "school_details_object": {
        "school": {
          "address": "1 fox road, sydney, nsw 2000",
          "name": "sydney grammar"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        },
        "ranking": "No 5"
      },
      "my_school": "\n\nMy school name is: sydney grammar, it is located\nat 1 fox road, sydney, nsw 2000\n\n\nWe have got  peter,  tom,  jane,  as our principals\n\nOur school ranking last year is No 5\n"
    })
    
    {{.my_school}}
    ~SubStep2: [print:  ]
    
    
    My school name is: sydney grammar, it is located
    at 1 fox road, sydney, nsw 2000
    
    
    We have got  peter,  tom,  jane,  as our principals
    
    Our school ranking last year is No 5
    
    
```

##### Logs with different verbose level
* [c0096 log - verbose level v](../../logs/c0096_v)
* [c0096 log - verbose level vv](../../logs/c0096_vv)
* [c0096 log - verbose level vvv](../../logs/c0096_vvv)
* [c0096 log - verbose level vvvv](../../logs/c0096_vvvv)
* [c0096 log - verbose level vvvvv](../../logs/c0096_vvvvv)

##### References
* [Related Chapter](../../templating/c0096)