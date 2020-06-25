---
title: "c0096_vvvv"
date: 2020-06-25T01:55:54+66:00
draft: false
weight: 10963

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
                 Verbose -> vvvv
              ModuleName -> boring_almeida3
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0096
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [boring_almeida3] instance id: [dev]
    merged[ dev ] runtime vars:
    {
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
    
    -------runtime global final merged with dvars-------
    
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
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "cmd": {
            "src": "./tests/functests/d0079.template",
            "dest": "/tmp/myschool.txt",
            "datakey": "school_details_object"
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
      }
    })
    
    boring_almeida3: overall final exec vars:
    
    (*core.Cache)({
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
    })
    
    ~SubStep1: [template: render the template file using above dynamic variable from defined var ]
    -Step2:
    {
      Name: "",
      Do: {
        {
          "desc": "read content of a file and register it to a var",
          "cmd": {
            "filename": "myschool.txt",
            "dir": "/tmp",
            "reg": "my_school"
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
    })
    
    boring_almeida3: overall final exec vars:
    
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
    })
    
    ~SubStep1: [readfile: read content of a file and register it to a var ]
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
          "desc": "render the template file using above dynamic variable from defined var",
          "cmd": {
            "datapath": "root.parent.school_details_object",
            "src": "./tests/functests/d0079.template",
            "dest": "/tmp/myschool.txt"
          },
          "name": "template"
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
    
    boring_almeida3: overall final exec vars:
    
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
    })
    
    ~SubStep1: [template: render the template file using above dynamic variable from defined var ]
    -Step4:
    {
      Name: "",
      Do: {
        {
          "name": "readfile",
          "desc": "read content of a file and register it to a var",
          "cmd": {
            "filename": "myschool.txt",
            "dir": "/tmp",
            "reg": "my_school"
          }
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
      "my_school": "\n\nMy school name is: sydney grammar, it is located\nat 1 fox road, sydney, nsw 2000\n\n\nWe have got  peter,  tom,  jane,  as our principals\n\nOur school ranking last year is No 5\n",
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
    })
    
    boring_almeida3: overall final exec vars:
    
    (*core.Cache)({
      "my_school": "\n\nMy school name is: sydney grammar, it is located\nat 1 fox road, sydney, nsw 2000\n\n\nWe have got  peter,  tom,  jane,  as our principals\n\nOur school ranking last year is No 5\n",
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
    })
    
    ~SubStep1: [readfile: read content of a file and register it to a var ]
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
