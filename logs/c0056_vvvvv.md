---
title: "c0056_vvvvv"
date: 2020-06-27T03:09:21+66:00
draft: false
weight: 10564

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
                 Verbose -> vvvvv
              ModuleName -> ecstatic_pike8
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0056
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001eb540)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [ecstatic_pike8] instance id: [dev]
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
    
    (core.Cache) (len=1) {
     (string) (len=9) "countries": ([]interface {}) (len=4 cap=4) {
      (map[interface {}]interface {}) (len=2) {
       (string) (len=4) "name": (string) (len=9) "Australia",
       (string) (len=10) "population": (string) (len=3) "20m"
      },
      (map[interface {}]interface {}) (len=2) {
       (string) (len=4) "name": (string) (len=7) "British",
       (string) (len=10) "population": (string) (len=5) "2000m"
      },
      (map[interface {}]interface {}) (len=2) {
       (string) (len=4) "name": (string) (len=5) "China",
       (string) (len=10) "population": (string) (len=4) "1.4b"
      },
      (map[interface {}]interface {}) (len=2) {
       (string) (len=4) "name": (string) (len=7) "Danmark",
       (string) (len=10) "population": (string) (len=3) "30m"
      }
     }
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
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
          "population": "2000m",
          "name": "British"
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
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
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
    
    
    ecstatic_pike8: overall final exec vars:
    
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
    echo "hello {{.loopitem}}"
    
     \_ echo "hello tom"
    hello tom
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=9) "hello tom",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "hello {{.loopitem}}"
    
     \_ echo "hello peter"
    hello peter
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=11) "hello peter",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "hello {{.loopitem}}"
    
     \_ echo "hello james"
    hello james
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=11) "hello james",
     ErrMsg: (string) ""
    }
    
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
        Output: "hello james",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
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
        Code: 0,
        Output: "hello james",
        ErrMsg: ""
      })
    }
    
    
    ecstatic_pike8: overall final exec vars:
    
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
        Code: 0,
        Output: "hello james",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "name {{.loopitem.name}}"
    
     \_ echo "name tom"
    name tom
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=8) "name tom",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "age {{.loopitem.age}}"
    
     \_ echo "age 11"
    age 11
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=6) "age 11",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "name {{.loopitem.name}}"
    
     \_ echo "name peter"
    name peter
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=10) "name peter",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "age {{.loopitem.age}}"
    
     \_ echo "age 45"
    age 45
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=6) "age 45",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "name {{.loopitem.name}}"
    
     \_ echo "name james"
    name james
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=10) "name james",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "age {{.loopitem.age}}"
    
     \_ echo "age 23"
    age 23
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=6) "age 23",
     ErrMsg: (string) ""
    }
    
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
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "age 23",
        ErrMsg: ""
      }),
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
          "name": "China",
          "population": "1.4b"
        },
        {
          "name": "Danmark",
          "population": "30m"
        }
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
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
    }
    
    
    ecstatic_pike8: overall final exec vars:
    
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
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=15) "hello Australia",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "hello {{.loopitem}}"
    
     \_ echo "hello British"
    hello British
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=13) "hello British",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "hello {{.loopitem}}"
    
     \_ echo "hello China"
    hello China
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=11) "hello China",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "hello {{.loopitem}}"
    
     \_ echo "hello Danmark"
    hello Danmark
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=13) "hello Danmark",
     ErrMsg: (string) ""
    }
    
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
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
        Code: 0,
        Output: "hello Danmark",
        ErrMsg: ""
      })
    }
    
    
    ecstatic_pike8: overall final exec vars:
    
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
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=15) "hello Australia",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello {{.loopitem.population}}"
    
     \_ echo "hello 20m"
    hello 20m
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=9) "hello 20m",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "hello {{.loopitem.name}}"
    
     \_ echo "hello British"
    hello British
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=13) "hello British",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello {{.loopitem.population}}"
    
     \_ echo "hello 2000m"
    hello 2000m
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=11) "hello 2000m",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "hello {{.loopitem.name}}"
    
     \_ echo "hello China"
    hello China
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=11) "hello China",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello {{.loopitem.population}}"
    
     \_ echo "hello 1.4b"
    hello 1.4b
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=10) "hello 1.4b",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "hello {{.loopitem.name}}"
    
     \_ echo "hello Danmark"
    hello Danmark
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=13) "hello Danmark",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello {{.loopitem.population}}"
    
     \_ echo "hello 30m"
    hello 30m
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=9) "hello 30m",
     ErrMsg: (string) ""
    }
    
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
          "name": "China",
          "population": "1.4b"
        },
        {
          "name": "Danmark",
          "population": "30m"
        }
      }
    })
    
    [local] dvar expanded result:
    {
      "listname": "countries"
    }
    
    
    scope[local] merged: {
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
        Code: 0,
        Output: "hello 30m",
        ErrMsg: ""
      }),
      "listname": "countries"
    }
    
    
    ecstatic_pike8: overall final exec vars:
    
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
          "population": "30m",
          "name": "Danmark"
        }
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello 30m",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "hello {{.loopindex}}"
    
     \_ echo "hello 0"
    hello 0
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=7) "hello 0",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello {{.loopindex1}}"
    
     \_ echo "hello 1"
    hello 1
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=7) "hello 1",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "hello {{.loopitem.name}}"
    
     \_ echo "hello Australia"
    hello Australia
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=15) "hello Australia",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo "hello {{.loopitem.population}}"
    
     \_ echo "hello 20m"
    hello 20m
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=9) "hello 20m",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "hello {{.loopindex}}"
    
     \_ echo "hello 1"
    hello 1
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=7) "hello 1",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello {{.loopindex1}}"
    
     \_ echo "hello 2"
    hello 2
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=7) "hello 2",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "hello {{.loopitem.name}}"
    
     \_ echo "hello British"
    hello British
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=13) "hello British",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo "hello {{.loopitem.population}}"
    
     \_ echo "hello 2000m"
    hello 2000m
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=11) "hello 2000m",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "hello {{.loopindex}}"
    
     \_ echo "hello 2"
    hello 2
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=7) "hello 2",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello {{.loopindex1}}"
    
     \_ echo "hello 3"
    hello 3
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=7) "hello 3",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "hello {{.loopitem.name}}"
    
     \_ echo "hello China"
    hello China
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=11) "hello China",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo "hello {{.loopitem.population}}"
    
     \_ echo "hello 1.4b"
    hello 1.4b
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=10) "hello 1.4b",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "hello {{.loopindex}}"
    
     \_ echo "hello 3"
    hello 3
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=7) "hello 3",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello {{.loopindex1}}"
    
     \_ echo "hello 4"
    hello 4
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=7) "hello 4",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "hello {{.loopitem.name}}"
    
     \_ echo "hello Danmark"
    hello Danmark
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=13) "hello Danmark",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo "hello {{.loopitem.population}}"
    
     \_ echo "hello 30m"
    hello 30m
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=9) "hello 30m",
     ErrMsg: (string) ""
    }
    
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
