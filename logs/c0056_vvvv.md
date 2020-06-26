---
title: "c0056_vvvv"
date: 2020-06-27T03:09:21+66:00
draft: false
weight: 10563

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0056
                 Verbose -> vvvv
              ModuleName -> elegant_euclid0
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0056
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [elegant_euclid0] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "countries": {
        {
          "name": "Australia",
          "population": "20m"
        },
        {
          "population": "2000m",
          "name": "British"
        },
        {
          "name": "China",
          "population": "1.4b"
        },
        {
          "name": "Danmark",
          "population": "30m"
        }
      }
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "countries": {
        {
          "name": "Australia",
          "population": "20m"
        },
        {
          "name": "British",
          "population": "2000m"
        },
        {
          "name": "China",
          "population": "1.4b"
        },
        {
          "population": "30m",
          "name": "Danmark"
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
        "echo \"hello {{.loopitem}}\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "tom",
        "peter",
        "james"
      },
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "countries": {
        {
          "name": "Australia",
          "population": "20m"
        },
        {
          "name": "British",
          "population": "2000m"
        },
        {
          "population": "1.4b",
          "name": "China"
        },
        {
          "name": "Danmark",
          "population": "30m"
        }
      }
    })
    
    elegant_euclid0: overall final exec vars:
    
    (*core.Cache)({
      "countries": {
        {
          "population": "20m",
          "name": "Australia"
        },
        {
          "population": "2000m",
          "name": "British"
        },
        {
          "population": "1.4b",
          "name": "China"
        },
        {
          "name": "Danmark",
          "population": "30m"
        }
      }
    })
    
    cmd( 1):
    echo "hello {{.loopitem}}"
    
     \_ echo "hello tom"
    hello tom
     .. ok
    cmd( 1):
    echo "hello {{.loopitem}}"
    
     \_ echo "hello peter"
    hello peter
     .. ok
    cmd( 1):
    echo "hello {{.loopitem}}"
    
     \_ echo "hello james"
    hello james
     .. ok
    . ok
    -Step2:
    {
      Name: "",
      Do: {
        "echo \"name {{.loopitem.name}}\"",
        "echo \"age {{.loopitem.age}}\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        {
          "name": "tom",
          "age": 11
        },
        {
          "name": "peter",
          "age": 45
        },
        {
          "name": "james",
          "age": 23
        }
      },
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "countries": {
        {
          "name": "Australia",
          "population": "20m"
        },
        {
          "population": "2000m",
          "name": "British"
        },
        {
          "population": "1.4b",
          "name": "China"
        },
        {
          "name": "Danmark",
          "population": "30m"
        }
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello james",
        ErrMsg: ""
      })
    })
    
    elegant_euclid0: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello james",
        ErrMsg: ""
      }),
      "countries": {
        {
          "name": "Australia",
          "population": "20m"
        },
        {
          "name": "British",
          "population": "2000m"
        },
        {
          "name": "China",
          "population": "1.4b"
        },
        {
          "name": "Danmark",
          "population": "30m"
        }
      }
    })
    
    cmd( 1):
    echo "name {{.loopitem.name}}"
    
     \_ echo "name tom"
    name tom
     .. ok
    cmd( 2):
    echo "age {{.loopitem.age}}"
    
     \_ echo "age 11"
    age 11
     .. ok
    cmd( 1):
    echo "name {{.loopitem.name}}"
    
     \_ echo "name peter"
    name peter
     .. ok
    cmd( 2):
    echo "age {{.loopitem.age}}"
    
     \_ echo "age 45"
    age 45
     .. ok
    cmd( 1):
    echo "name {{.loopitem.name}}"
    
     \_ echo "name james"
    name james
     .. ok
    cmd( 2):
    echo "age {{.loopitem.age}}"
    
     \_ echo "age 23"
    age 23
     .. ok
    . ok
    -Step3:
    {
      Name: "",
      Do: {
        "echo \"hello {{.loopitem}}\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "Australia",
        "British",
        "China",
        "Danmark"
      },
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "countries": {
        {
          "population": "20m",
          "name": "Australia"
        },
        {
          "name": "British",
          "population": "2000m"
        },
        {
          "name": "China",
          "population": "1.4b"
        },
        {
          "population": "30m",
          "name": "Danmark"
        }
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "age 23",
        ErrMsg: ""
      })
    })
    
    elegant_euclid0: overall final exec vars:
    
    (*core.Cache)({
      "countries": {
        {
          "name": "Australia",
          "population": "20m"
        },
        {
          "name": "British",
          "population": "2000m"
        },
        {
          "name": "China",
          "population": "1.4b"
        },
        {
          "name": "Danmark",
          "population": "30m"
        }
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "age 23",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "hello {{.loopitem}}"
    
     \_ echo "hello Australia"
    hello Australia
     .. ok
    cmd( 1):
    echo "hello {{.loopitem}}"
    
     \_ echo "hello British"
    hello British
     .. ok
    cmd( 1):
    echo "hello {{.loopitem}}"
    
     \_ echo "hello China"
    hello China
     .. ok
    cmd( 1):
    echo "hello {{.loopitem}}"
    
     \_ echo "hello Danmark"
    hello Danmark
     .. ok
    . ok
    -Step4: [: the loop point to a iteratable var countries
     ]
    {
      Name: "",
      Do: {
        "echo \"hello {{.loopitem.name}}\"",
        "echo \"hello {{.loopitem.population}}\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "the loop point to a iteratable var countries\n",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: "countries",
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello Danmark",
        ErrMsg: ""
      }),
      "countries": {
        {
          "name": "Australia",
          "population": "20m"
        },
        {
          "name": "British",
          "population": "2000m"
        },
        {
          "name": "China",
          "population": "1.4b"
        },
        {
          "name": "Danmark",
          "population": "30m"
        }
      }
    })
    
    elegant_euclid0: overall final exec vars:
    
    (*core.Cache)({
      "countries": {
        {
          "name": "Australia",
          "population": "20m"
        },
        {
          "name": "British",
          "population": "2000m"
        },
        {
          "name": "China",
          "population": "1.4b"
        },
        {
          "name": "Danmark",
          "population": "30m"
        }
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello Danmark",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "hello {{.loopitem.name}}"
    
     \_ echo "hello Australia"
    hello Australia
     .. ok
    cmd( 2):
    echo "hello {{.loopitem.population}}"
    
     \_ echo "hello 20m"
    hello 20m
     .. ok
    cmd( 1):
    echo "hello {{.loopitem.name}}"
    
     \_ echo "hello British"
    hello British
     .. ok
    cmd( 2):
    echo "hello {{.loopitem.population}}"
    
     \_ echo "hello 2000m"
    hello 2000m
     .. ok
    cmd( 1):
    echo "hello {{.loopitem.name}}"
    
     \_ echo "hello China"
    hello China
     .. ok
    cmd( 2):
    echo "hello {{.loopitem.population}}"
    
     \_ echo "hello 1.4b"
    hello 1.4b
     .. ok
    cmd( 1):
    echo "hello {{.loopitem.name}}"
    
     \_ echo "hello Danmark"
    hello Danmark
     .. ok
    cmd( 2):
    echo "hello {{.loopitem.population}}"
    
     \_ echo "hello 30m"
    hello 30m
     .. ok
    . ok
    -Step5: [: the templated value will be eventually a var/dvar name
     ]
    {
      Name: "",
      Do: {
        "echo \"hello {{.loopindex}}\"",
        "echo \"hello {{.loopindex1}}\"",
        "echo \"hello {{.loopitem.name}}\"",
        "echo \"hello {{.loopitem.population}}\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: {
        {
          Name: "listname",
          Value: "countries",
          Desc: "",
          Expand: 0,
          Flags: <nil>,
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
      Desc: "the templated value will be eventually a var/dvar name\n",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: "{{.listname}}",
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "countries": {
        {
          "name": "Australia",
          "population": "20m"
        },
        {
          "name": "British",
          "population": "2000m"
        },
        {
          "name": "China",
          "population": "1.4b"
        },
        {
          "name": "Danmark",
          "population": "30m"
        }
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello 30m",
        ErrMsg: ""
      })
    })
    
    elegant_euclid0: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello 30m",
        ErrMsg: ""
      }),
      "countries": {
        {
          "name": "Australia",
          "population": "20m"
        },
        {
          "name": "British",
          "population": "2000m"
        },
        {
          "population": "1.4b",
          "name": "China"
        },
        {
          "name": "Danmark",
          "population": "30m"
        }
      },
      "listname": "countries"
    })
    
    cmd( 1):
    echo "hello {{.loopindex}}"
    
     \_ echo "hello 0"
    hello 0
     .. ok
    cmd( 2):
    echo "hello {{.loopindex1}}"
    
     \_ echo "hello 1"
    hello 1
     .. ok
    cmd( 3):
    echo "hello {{.loopitem.name}}"
    
     \_ echo "hello Australia"
    hello Australia
     .. ok
    cmd( 4):
    echo "hello {{.loopitem.population}}"
    
     \_ echo "hello 20m"
    hello 20m
     .. ok
    cmd( 1):
    echo "hello {{.loopindex}}"
    
     \_ echo "hello 1"
    hello 1
     .. ok
    cmd( 2):
    echo "hello {{.loopindex1}}"
    
     \_ echo "hello 2"
    hello 2
     .. ok
    cmd( 3):
    echo "hello {{.loopitem.name}}"
    
     \_ echo "hello British"
    hello British
     .. ok
    cmd( 4):
    echo "hello {{.loopitem.population}}"
    
     \_ echo "hello 2000m"
    hello 2000m
     .. ok
    cmd( 1):
    echo "hello {{.loopindex}}"
    
     \_ echo "hello 2"
    hello 2
     .. ok
    cmd( 2):
    echo "hello {{.loopindex1}}"
    
     \_ echo "hello 3"
    hello 3
     .. ok
    cmd( 3):
    echo "hello {{.loopitem.name}}"
    
     \_ echo "hello China"
    hello China
     .. ok
    cmd( 4):
    echo "hello {{.loopitem.population}}"
    
     \_ echo "hello 1.4b"
    hello 1.4b
     .. ok
    cmd( 1):
    echo "hello {{.loopindex}}"
    
     \_ echo "hello 3"
    hello 3
     .. ok
    cmd( 2):
    echo "hello {{.loopindex1}}"
    
     \_ echo "hello 4"
    hello 4
     .. ok
    cmd( 3):
    echo "hello {{.loopitem.name}}"
    
     \_ echo "hello Danmark"
    hello Danmark
     .. ok
    cmd( 4):
    echo "hello {{.loopitem.population}}"
    
     \_ echo "hello 30m"
    hello 30m
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0056 log - verbose level v](../../logs/c0056_v)
* [c0056 log - verbose level vv](../../logs/c0056_vv)
* [c0056 log - verbose level vvv](../../logs/c0056_vvv)
* [c0056 log - verbose level vvvv](../../logs/c0056_vvvv)
* [c0056 log - verbose level vvvvv](../../logs/c0056_vvvvv)

##### References
* [Related Chapter](../../loop/c0056)
