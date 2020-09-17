---
title: "c0056_vvvv"
date: 2020-09-18T00:51:28+99:00
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
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0056
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
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
          "name": "Danmark",
          "population": "30m"
        }
      }
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
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
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
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
          "name": "Danmark",
          "population": "30m"
        }
      },
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "hello {{.loopitem}}"
    
    cmd=>:
    echo "hello tom"
    -
    hello tom
    
    -
     .. ok
    cmd( 1):
    echo "hello {{.loopitem}}"
    
    cmd=>:
    echo "hello peter"
    -
    hello peter
    
    -
     .. ok
    cmd( 1):
    echo "hello {{.loopitem}}"
    
    cmd=>:
    echo "hello james"
    -
    hello james
    
    -
     .. ok
    . ok
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
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
        Cmd: "echo \"hello james\"",
        Code: 0,
        Output: "hello james",
        ErrMsg: ""
      })
    })
    
    self: final context exec vars:
    
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
          "population": "30m",
          "name": "Danmark"
        }
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello james\"",
        Code: 0,
        Output: "hello james",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "name {{.loopitem.name}}"
    
    cmd=>:
    echo "name tom"
    -
    name tom
    
    -
     .. ok
    cmd( 2):
    echo "age {{.loopitem.age}}"
    
    cmd=>:
    echo "age 11"
    -
    age 11
    
    -
     .. ok
    cmd( 1):
    echo "name {{.loopitem.name}}"
    
    cmd=>:
    echo "name peter"
    -
    name peter
    
    -
     .. ok
    cmd( 2):
    echo "age {{.loopitem.age}}"
    
    cmd=>:
    echo "age 45"
    -
    age 45
    
    -
     .. ok
    cmd( 1):
    echo "name {{.loopitem.name}}"
    
    cmd=>:
    echo "name james"
    -
    name james
    
    -
     .. ok
    cmd( 2):
    echo "age {{.loopitem.age}}"
    
    cmd=>:
    echo "age 23"
    -
    age 23
    
    -
     .. ok
    . ok
    -Step3:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"age 23\"",
        Code: 0,
        Output: "age 23",
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
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"age 23\"",
        Code: 0,
        Output: "age 23",
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
      },
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "hello {{.loopitem}}"
    
    cmd=>:
    echo "hello Australia"
    -
    hello Australia
    
    -
     .. ok
    cmd( 1):
    echo "hello {{.loopitem}}"
    
    cmd=>:
    echo "hello British"
    -
    hello British
    
    -
     .. ok
    cmd( 1):
    echo "hello {{.loopitem}}"
    
    cmd=>:
    echo "hello China"
    -
    hello China
    
    -
     .. ok
    cmd( 1):
    echo "hello {{.loopitem}}"
    
    cmd=>:
    echo "hello Danmark"
    -
    hello Danmark
    
    -
     .. ok
    . ok
    -Step4: [: the loop point to a iteratable var countries
     ]
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
        Cmd: "echo \"hello Danmark\"",
        Code: 0,
        Output: "hello Danmark",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello Danmark\"",
        Code: 0,
        Output: "hello Danmark",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
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
    echo "hello {{.loopitem.name}}"
    
    cmd=>:
    echo "hello Australia"
    -
    hello Australia
    
    -
     .. ok
    cmd( 2):
    echo "hello {{.loopitem.population}}"
    
    cmd=>:
    echo "hello 20m"
    -
    hello 20m
    
    -
     .. ok
    cmd( 1):
    echo "hello {{.loopitem.name}}"
    
    cmd=>:
    echo "hello British"
    -
    hello British
    
    -
     .. ok
    cmd( 2):
    echo "hello {{.loopitem.population}}"
    
    cmd=>:
    echo "hello 2000m"
    -
    hello 2000m
    
    -
     .. ok
    cmd( 1):
    echo "hello {{.loopitem.name}}"
    
    cmd=>:
    echo "hello China"
    -
    hello China
    
    -
     .. ok
    cmd( 2):
    echo "hello {{.loopitem.population}}"
    
    cmd=>:
    echo "hello 1.4b"
    -
    hello 1.4b
    
    -
     .. ok
    cmd( 1):
    echo "hello {{.loopitem.name}}"
    
    cmd=>:
    echo "hello Danmark"
    -
    hello Danmark
    
    -
     .. ok
    cmd( 2):
    echo "hello {{.loopitem.population}}"
    
    cmd=>:
    echo "hello 30m"
    -
    hello 30m
    
    -
     .. ok
    . ok
    -Step5: [: the templated value will be eventually a var/dvar name
     ]
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
        Cmd: "echo \"hello 30m\"",
        Code: 0,
        Output: "hello 30m",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "listname": "countries",
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
          "name": "Danmark",
          "population": "30m"
        }
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello 30m\"",
        Code: 0,
        Output: "hello 30m",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "hello {{.loopindex}}"
    
    cmd=>:
    echo "hello 0"
    -
    hello 0
    
    -
     .. ok
    cmd( 2):
    echo "hello {{.loopindex1}}"
    
    cmd=>:
    echo "hello 1"
    -
    hello 1
    
    -
     .. ok
    cmd( 3):
    echo "hello {{.loopitem.name}}"
    
    cmd=>:
    echo "hello Australia"
    -
    hello Australia
    
    -
     .. ok
    cmd( 4):
    echo "hello {{.loopitem.population}}"
    
    cmd=>:
    echo "hello 20m"
    -
    hello 20m
    
    -
     .. ok
    cmd( 1):
    echo "hello {{.loopindex}}"
    
    cmd=>:
    echo "hello 1"
    -
    hello 1
    
    -
     .. ok
    cmd( 2):
    echo "hello {{.loopindex1}}"
    
    cmd=>:
    echo "hello 2"
    -
    hello 2
    
    -
     .. ok
    cmd( 3):
    echo "hello {{.loopitem.name}}"
    
    cmd=>:
    echo "hello British"
    -
    hello British
    
    -
     .. ok
    cmd( 4):
    echo "hello {{.loopitem.population}}"
    
    cmd=>:
    echo "hello 2000m"
    -
    hello 2000m
    
    -
     .. ok
    cmd( 1):
    echo "hello {{.loopindex}}"
    
    cmd=>:
    echo "hello 2"
    -
    hello 2
    
    -
     .. ok
    cmd( 2):
    echo "hello {{.loopindex1}}"
    
    cmd=>:
    echo "hello 3"
    -
    hello 3
    
    -
     .. ok
    cmd( 3):
    echo "hello {{.loopitem.name}}"
    
    cmd=>:
    echo "hello China"
    -
    hello China
    
    -
     .. ok
    cmd( 4):
    echo "hello {{.loopitem.population}}"
    
    cmd=>:
    echo "hello 1.4b"
    -
    hello 1.4b
    
    -
     .. ok
    cmd( 1):
    echo "hello {{.loopindex}}"
    
    cmd=>:
    echo "hello 3"
    -
    hello 3
    
    -
     .. ok
    cmd( 2):
    echo "hello {{.loopindex1}}"
    
    cmd=>:
    echo "hello 4"
    -
    hello 4
    
    -
     .. ok
    cmd( 3):
    echo "hello {{.loopitem.name}}"
    
    cmd=>:
    echo "hello Danmark"
    -
    hello Danmark
    
    -
     .. ok
    cmd( 4):
    echo "hello {{.loopitem.population}}"
    
    cmd=>:
    echo "hello 30m"
    -
    hello 30m
    
    -
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
