---
title: "c0100_vvvv"
date: 2020-10-07T00:11:17+1010:00
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
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0100
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
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
      }
    })
    
    -------runtime global final merged with dvars-------
    
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
      }
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
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
      "up_runtime_task_layer_number": 0,
      "ymlstr": "student:\n  name: jason\n  gender: Male\n  school: The Kings\n",
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "query_name": "jason",
      "up_runtime_task_layer_number": 0,
      "ymlstr": "student:\n  name: jason\n  gender: Male\n  school: The Kings\n",
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
      }
    })
    
    ~SubStep1: [query: query using ref var ymlstr and query a registered var by default in global ]
    -Step2:
    current exec runtime vars:
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
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "school_name": (*string)("The Kings"),
      "up_runtime_task_layer_number": 0,
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    })
    
    self: final context exec vars:
    
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
      "query_name": "jason",
      "school_name": (*string)("The Kings"),
      "up_runtime_task_layer_number": 0,
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
    })
    
    ~SubStep1: [print:  ]
    The Kings
    -Step3:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "ymlstr": "student: |\n  name: jason\n  gender: Male\n  school: The Kings\n",
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
      "school_name": (*string)("The Kings")
    })
    
    self: final context exec vars:
    
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
      "school_name": (*string)("The Kings"),
      "up_runtime_task_layer_number": 0,
      "ymlstr": "student: |\n  name: jason\n  gender: Male\n  school: The Kings\n",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
    })
    
    ~SubStep1: [query: query using ref var ymlstr and query a registered var by default in global ]
    -Step4:
    current exec runtime vars:
    (*core.Cache)({
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "up_runtime_task_layer_number": 0,
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
      "school_name": (*string)("The Kings")
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
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
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "school": "The Kings",
        "name": "jason",
        "gender": "Male"
      })
    })
    
    ~SubStep1: [print:  ]
    map[gender:Male name:jason school:The Kings]
    -Step5:
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
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "up_runtime_task_layer_number": 0,
      "ymlstr": "student:\n  name: jason\n  gender: Male\n  school: The Kings\n"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "ymlstr": "student:\n  name: jason\n  gender: Male\n  school: The Kings\n",
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
      "school_name": (*string)("The Kings"),
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
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [query: query and query a registered var in local ]
    -Step6:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
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
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "up_runtime_task_layer_number": 0,
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
      "query_name": "jason"
    })
    
    ~SubStep1: [print:  ]
    None
    -Step7:
    current exec runtime vars:
    (*core.Cache)({
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
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
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
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      })
    })
    
    ~SubStep1: [query: query from cached vars only ]
    -Step8:
    current exec runtime vars:
    (*core.Cache)({
      "query_name": "jason",
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "data_school_name": "",
      "up_runtime_task_layer_number": 0,
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
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "data_school_name": "",
      "up_runtime_task_layer_number": 0,
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
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      })
    })
    
    ~SubStep1: [print:  ]
    
    -Step9:
    current exec runtime vars:
    (*core.Cache)({
      "data_school_name": "",
      "up_runtime_task_layer_number": 0,
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
      "query_name": "jason",
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "gender": "Male",
        "school": "The Kings",
        "name": "jason"
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "query_name": "jason",
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "data_school_name": "",
      "up_runtime_task_layer_number": 0,
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
    
    ~SubStep1: [query: query from cached vars and put result into a list/array ]
    ~SubStep2: [printObj:  ]
    (string) (len=21) "{{.school_name_list}}"
    
    object:
     [MLC KINGS]: (interface {}) <nil>
    
    ~SubStep3: [print:  ]
    [MLC KINGS]
    -Step10:
    current exec runtime vars:
    (*core.Cache)({
      "query_name": "jason",
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
      "up_runtime_task_layer_number": 0,
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
      }
    })
    
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
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        }
      },
      "query_name": "jason",
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
      "up_runtime_task_layer_number": 0,
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    })
    
    ~SubStep1: [query: query a sub node ]
    ~SubStep2: [printObj:  ]
    (string) (len=9) "{{.city}}"
    
    object:
     [[map[sg:map[student:map[gender:Female name:Grace school:MLC]]] map[kings:map[student:map[gender:Female name:Emily school:KINGS]]]]]: (interface {}) <nil>
    
    ~SubStep3: [print:  ]
    [[map[sg:map[student:map[gender:Female name:Grace school:MLC]]] map[kings:map[student:map[gender:Female name:Emily school:KINGS]]]]]
    -Step11:
    current exec runtime vars:
    (*core.Cache)({
      "school_name": (*string)("The Kings"),
      "data_school_name": "",
      "up_runtime_task_layer_number": 0,
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
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
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "school_name": (*string)("The Kings"),
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "query_name": "jason",
      "data_school_name": "",
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
      "student_info": (*map[interface {}]interface {})({
        "school": "The Kings",
        "name": "jason",
        "gender": "Male"
      })
    })
    
    ~SubStep1: [query: query a selected indexed node from a array ]
    ~SubStep2: [printObj:  ]
    (string) (len=10) "{{.city1}}"
    
    object:
     map[kings:map[student:map[gender:Female name:Emily school:KINGS]]]: (interface {}) <nil>
    
    ~SubStep3: [print:  ]
    map[kings:map[student:map[gender:Female name:Emily school:KINGS]]]
    -Step12:
    current exec runtime vars:
    (*core.Cache)({
      "query_name": "jason",
      "up_runtime_task_layer_number": 0,
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
                "name": "Emily",
                "school": "KINGS",
                "gender": "Female"
              }
            }
          }
        }
      }),
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
      "school_name": (*string)("The Kings")
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
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
      "up_runtime_task_layer_number": 0,
      "student_info": (*map[interface {}]interface {})({
        "school": "The Kings",
        "name": "jason",
        "gender": "Male"
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
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "query_name": "jason",
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    })
    
    ~SubStep1: [query: query all nodes from an array ]
    ~SubStep2: [printObj:  ]
    (string) (len=12) "{{.cityall}}"
    
    object:
     map[kings:map[student:map[gender:Female name:Emily school:KINGS]] sg:map[student:map[gender:Female name:Grace school:MLC]]]: (interface {}) <nil>
    
    ~SubStep3: [print:  ]
    map[kings:map[student:map[gender:Female name:Emily school:KINGS]] sg:map[student:map[gender:Female name:Grace school:MLC]]]
    -Step13:
    current exec runtime vars:
    (*core.Cache)({
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "up_runtime_task_layer_number": 0,
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
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
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
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "data_school_name": "",
      "up_runtime_task_layer_number": 0,
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
                "name": "Jason",
                "gender": "Mail",
                "school": "Public High School"
              }
            }
          }
        }
      },
      "query_name": "jason",
      "student_info": (*map[interface {}]interface {})({
        "school": "The Kings",
        "name": "jason",
        "gender": "Male"
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
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
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
    ~SubStep2: [printObj:  ]
    (string) (len=13) "{{.studentx}}"
    
    object:
     map[gender:Female name:Emily school:KINGS]: (interface {}) <nil>
    
    ~SubStep3: [print:  ]
    map[gender:Female name:Emily school:KINGS]
    -Step14:
    current exec runtime vars:
    (*core.Cache)({
      "studentx": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "query_name": "jason",
      "city1": (*map[interface {}]interface {})({
        "kings": {
          "student": {
            "school": "KINGS",
            "gender": "Female",
            "name": "Emily"
          }
        }
      }),
      "school_name": (*string)("The Kings"),
      "student_info": (*map[interface {}]interface {})({
        "school": "The Kings",
        "name": "jason",
        "gender": "Male"
      }),
      "data_school_name": "",
      "up_runtime_task_layer_number": 0,
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
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
                "name": "Emily",
                "gender": "Female",
                "school": "KINGS"
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
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "studentx": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
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
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "query_name": "jason"
    })
    
    ~SubStep1: [query: query result matching the criteria ]
    ~SubStep2: [printObj:  ]
    (string) (len=13) "{{.studenty}}"
    
    object:
     map[gender:Female name:Emily school:KINGS]: (interface {}) <nil>
    
    -Step15:
    current exec runtime vars:
    (*core.Cache)({
      "data_school_name": "",
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "school_name": (*string)("The Kings"),
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
      "up_runtime_task_layer_number": 0,
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
      "studenty": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "studentx": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "student_info": (*map[interface {}]interface {})({
        "school": "The Kings",
        "name": "jason",
        "gender": "Male"
      }),
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
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
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
      "data_school_name": "",
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
      "studentx": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "student_info": (*map[interface {}]interface {})({
        "gender": "Male",
        "school": "The Kings",
        "name": "jason"
      }),
      "query_name": "jason",
      "up_runtime_task_layer_number": 0,
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "studenty": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
    })
    
    ~SubStep1: [query: query result matching the criteria ]
    ~SubStep2: [printObj:  ]
    (string) (len=13) "{{.studentz}}"
    
    object:
     map[gender:Female name:Emily school:KINGS]: (interface {}) <nil>
    
    -Step16:
    current exec runtime vars:
    (*core.Cache)({
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
      "studentx": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "query_name": "jason",
      "studenty": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "data_school_name": "",
      "up_runtime_task_layer_number": 0,
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
        "school": "The Kings",
        "name": "jason",
        "gender": "Male"
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
    
    self: final context exec vars:
    
    (*core.Cache)({
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
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
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "studentz": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "data_school_name": "",
      "studentx": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
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
            "school": "KINGS",
            "gender": "Female",
            "name": "Emily"
          }
        }
      }),
      "up_runtime_task_layer_number": 0,
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
      "query_name": "jason"
    })
    
    ~SubStep1: [query: query result matching the criteria ]
    ~SubStep2: [printObj:  ]
    (string) (len=13) "{{.studentm}}"
    
    object:
     map[gender:Female name:Emily school:KINGS]: (interface {}) <nil>
    
    -Step17:
    current exec runtime vars:
    (*core.Cache)({
      "query_name": "jason",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
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
      "student_info": (*map[interface {}]interface {})({
        "gender": "Male",
        "school": "The Kings",
        "name": "jason"
      }),
      "studentz": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "data_school_name": "",
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
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "school_name": (*string)("The Kings"),
      "studenty": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "up_runtime_task_layer_number": 0,
      "studentx": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student_info": (*map[interface {}]interface {})({
        "gender": "Male",
        "school": "The Kings",
        "name": "jason"
      }),
      "up_runtime_task_layer_number": 0,
      "school_name": (*string)("The Kings"),
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
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "studentz": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
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
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "studentm": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
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
                "school": "KINGS",
                "gender": "Female",
                "name": "Emily"
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
      "studentx": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      })
    })
    
    ~SubStep1: [query: query result matching the criteria ]
    ~SubStep2: [printObj:  ]
    (string) (len=13) "{{.studentn}}"
    
    object:
     map[gender:Female name:Grace school:MLC]: (interface {}) <nil>
    
    -Step18:
    current exec runtime vars:
    (*core.Cache)({
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
      "studentn": (*map[interface {}]interface {})({
        "name": "Grace",
        "school": "MLC",
        "gender": "Female"
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
      "studentm": (*map[interface {}]interface {})({
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
      "studenty": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "studentx": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "up_runtime_task_layer_number": 0,
      "studentz": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "student_info": (*map[interface {}]interface {})({
        "gender": "Male",
        "school": "The Kings",
        "name": "jason"
      }),
      "data_school_name": ""
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "query_name": "jason",
      "studenty": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
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
      "studentn": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Grace",
        "school": "MLC"
      }),
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "up_runtime_task_layer_number": 0,
      "data_school_name": "",
      "studentm": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "studentz": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
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
      "studentx": (*map[interface {}]interface {})({
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
      })
    })
    
    ~SubStep1: [query: query result matching the criteria ]
    ~SubStep2: [printObj:  ]
    (string) (len=13) "{{.studento}}"
    
    object:
     map[chatswood_high:map[student:map[gender:Mail name:Jason school:Public High School]]]: (interface {}) <nil>
    
    -Step19:
    current exec runtime vars:
    (*core.Cache)({
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
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
      "data_school_name": "",
      "studentx": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "school_name": (*string)("The Kings"),
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
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
      "query_name": "jason",
      "studentn": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Grace",
        "school": "MLC"
      }),
      "up_runtime_task_layer_number": 0,
      "studentm": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
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
      "student_info": (*map[interface {}]interface {})({
        "gender": "Male",
        "school": "The Kings",
        "name": "jason"
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
      }
    })
    
    self: final context exec vars:
    
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
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "studentm": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "studenty": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
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
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
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
      "data_school_name": "",
      "student_info": (*map[interface {}]interface {})({
        "gender": "Male",
        "school": "The Kings",
        "name": "jason"
      }),
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
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "up_runtime_task_layer_number": 0,
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
      "query_name": "jason",
      "school_name": (*string)("The Kings")
    })
    
    ~SubStep1: [query: query and register result as a yml string instead of object ]
    ~SubStep2: [trace:  ]
    Trace:====>
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
    current exec runtime vars:
    (*core.Cache)({
      "studentx": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "studentn": (*map[interface {}]interface {})({
        "school": "MLC",
        "gender": "Female",
        "name": "Grace"
      }),
      "studenty": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "up_runtime_task_layer_number": 0,
      "school_name": (*string)("The Kings"),
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
      "studentm": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "data_school_name": "",
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
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
      "student_info": (*map[interface {}]interface {})({
        "school": "The Kings",
        "name": "jason",
        "gender": "Male"
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "studentz": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "student_info": (*map[interface {}]interface {})({
        "name": "jason",
        "gender": "Male",
        "school": "The Kings"
      }),
      "studentm": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
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
      "school_name": (*string)("The Kings"),
      "studenty": (*map[interface {}]interface {})({
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
      "city2": "chatswood:\n- chatswood_high:\n    student:\n      gender: Mail\n      name: Jason\n      school: Public High School\nsydney:\n- sg:\n    student:\n      gender: Female\n      name: Grace\n      school: MLC\n- kings:\n    student:\n      gender: Female\n      name: Emily\n      school: KINGS\n",
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
      "studentx": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "data_school_name": "",
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "up_runtime_task_layer_number": 0,
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "studentn": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Grace",
        "school": "MLC"
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
    current exec runtime vars:
    (*core.Cache)({
      "query_name": "jason",
      "studenty": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
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
            "name": "Emily",
            "school": "KINGS",
            "gender": "Female"
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
      "student_info": (*map[interface {}]interface {})({
        "gender": "Male",
        "school": "The Kings",
        "name": "jason"
      }),
      "studentx": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
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
      "studentm": (*map[interface {}]interface {})({
        "name": "Emily",
        "school": "KINGS",
        "gender": "Female"
      }),
      "data_school_name": "",
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
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
            "name": "Emily",
            "school": "KINGS",
            "gender": "Female"
          }
        }
      }),
      "city2": "sydney:\n- sg:\n    student:\n      name: Grace\n      gender: Female\n      school: MLC\n- kings:\n    student:\n      name: Emily\n      gender: Female\n      school: KINGS\nchatswood:\n- chatswood_high:\n    student:\n      name: Jason\n      gender: Mail\n      school: Public High School\n",
      "up_runtime_task_layer_number": 0,
      "studentz": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
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
      "studentz": (*map[interface {}]interface {})({
        "school": "KINGS",
        "gender": "Female",
        "name": "Emily"
      }),
      "city2": "sydney:\n- sg:\n    student:\n      name: Grace\n      gender: Female\n      school: MLC\n- kings:\n    student:\n      name: Emily\n      gender: Female\n      school: KINGS\nchatswood:\n- chatswood_high:\n    student:\n      name: Jason\n      gender: Mail\n      school: Public High School\n",
      "student_info": (*map[interface {}]interface {})({
        "gender": "Male",
        "school": "The Kings",
        "name": "jason"
      }),
      "studentx": (*map[interface {}]interface {})({
        "gender": "Female",
        "name": "Emily",
        "school": "KINGS"
      }),
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "school_name_list": (*[]interface {})({
        "MLC",
        "KINGS"
      }),
      "studenty": (*map[interface {}]interface {})({
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
      "up_runtime_task_layer_number": 0,
      "school_name": (*string)("The Kings"),
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
      })
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
* [Related Chapter](../../object-oriented/c0100)
