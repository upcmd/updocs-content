---
title: "c0096_vvvv"
date: 2020-07-20T02:01:46+77:00
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
              ModuleName -> self
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
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [self] instance id: [dev]
    merged[ dev ] runtime vars:
    {
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
    
    -------runtime global final merged with dvars-------
    
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
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
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
    
    self: final context exec vars:
    
    (*core.Cache)({
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
      }
    })
    
    ~SubStep1: [template: render the template file using above dynamic variable from defined var ]
    -Step2:
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
      }
    })
    
    self: final context exec vars:
    
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
    
    ~SubStep1: [readFile: read content of a file and register it to a var ]
    ~SubStep2: [print:  ]
    
    
    My school name is: sydney grammar, it is located
    at 1 fox road, sydney, nsw 2000
    
    
    We have got  peter,  tom,  jane,  as our principals
    
    Our school ranking last year is No 5
    
    -Step3:
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
      "my_school": "\n\nMy school name is: sydney grammar, it is located\nat 1 fox road, sydney, nsw 2000\n\n\nWe have got  peter,  tom,  jane,  as our principals\n\nOur school ranking last year is No 5\n"
    })
    
    self: final context exec vars:
    
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
      "my_school": "\n\nMy school name is: sydney grammar, it is located\nat 1 fox road, sydney, nsw 2000\n\n\nWe have got  peter,  tom,  jane,  as our principals\n\nOur school ranking last year is No 5\n"
    })
    
    ~SubStep1: [template: render the template file using above dynamic variable from defined var ]
    -Step4:
    current exec runtime vars:
    (*core.Cache)({
      "my_school": "\n\nMy school name is: sydney grammar, it is located\nat 1 fox road, sydney, nsw 2000\n\n\nWe have got  peter,  tom,  jane,  as our principals\n\nOur school ranking last year is No 5\n",
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
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "my_school": "\n\nMy school name is: sydney grammar, it is located\nat 1 fox road, sydney, nsw 2000\n\n\nWe have got  peter,  tom,  jane,  as our principals\n\nOur school ranking last year is No 5\n",
      "root": {
        "parent": {
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
    
    ~SubStep1: [readFile: read content of a file and register it to a var ]
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
