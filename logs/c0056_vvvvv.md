---
title: "c0056_vvvvv"
date: 2020-07-20T02:01:39+77:00
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
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0056
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001bd5a0)(<nil>)
    
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
       (string) (len=10) "population": (string) (len=5) "2000m",
       (string) (len=4) "name": (string) (len=7) "British"
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
          "name": "British",
          "population": "2000m"
        },
        {
          "population": "1.4b",
          "name": "China"
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
          "population": "20m",
          "name": "Australia"
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
    
    [local] dvar expanded result:
    {
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
          "population": "1.4b",
          "name": "China"
        },
        {
          "population": "30m",
          "name": "Danmark"
        }
      }
    }
    
    
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
          "population": "1.4b",
          "name": "China"
        },
        {
          "population": "30m",
          "name": "Danmark"
        }
      }
    })
    
    cmd( 1):
    echo "hello {{.loopitem}}"
    
    cmd=>:
    echo "hello tom"<=
    hello tom
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=16) "echo \"hello tom\"",
     Code: (int) 0,
     Output: (string) (len=9) "hello tom",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "hello {{.loopitem}}"
    
    cmd=>:
    echo "hello peter"<=
    hello peter
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"hello peter\"",
     Code: (int) 0,
     Output: (string) (len=11) "hello peter",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "hello {{.loopitem}}"
    
    cmd=>:
    echo "hello james"<=
    hello james
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"hello james\"",
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
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello james\"",
        Code: 0,
        Output: "hello james",
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
          "population": "1.4b",
          "name": "China"
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
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello james\"",
        Code: 0,
        Output: "hello james",
        ErrMsg: ""
      }),
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
          "population": "1.4b",
          "name": "China"
        },
        {
          "name": "Danmark",
          "population": "30m"
        }
      }
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello james\"",
        Code: 0,
        Output: "hello james",
        ErrMsg: ""
      }),
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
      }
    })
    
    cmd( 1):
    echo "name {{.loopitem.name}}"
    
    cmd=>:
    echo "name tom"<=
    name tom
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=15) "echo \"name tom\"",
     Code: (int) 0,
     Output: (string) (len=8) "name tom",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "age {{.loopitem.age}}"
    
    cmd=>:
    echo "age 11"<=
    age 11
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=13) "echo \"age 11\"",
     Code: (int) 0,
     Output: (string) (len=6) "age 11",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "name {{.loopitem.name}}"
    
    cmd=>:
    echo "name peter"<=
    name peter
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=17) "echo \"name peter\"",
     Code: (int) 0,
     Output: (string) (len=10) "name peter",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "age {{.loopitem.age}}"
    
    cmd=>:
    echo "age 45"<=
    age 45
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=13) "echo \"age 45\"",
     Code: (int) 0,
     Output: (string) (len=6) "age 45",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "name {{.loopitem.name}}"
    
    cmd=>:
    echo "name james"<=
    name james
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=17) "echo \"name james\"",
     Code: (int) 0,
     Output: (string) (len=10) "name james",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "age {{.loopitem.age}}"
    
    cmd=>:
    echo "age 23"<=
    age 23
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=13) "echo \"age 23\"",
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
          "population": "30m",
          "name": "Danmark"
        }
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"age 23\"",
        Code: 0,
        Output: "age 23",
        ErrMsg: ""
      })
    }
    
    
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
          "population": "1.4b",
          "name": "China"
        },
        {
          "population": "30m",
          "name": "Danmark"
        }
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"age 23\"",
        Code: 0,
        Output: "age 23",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "hello {{.loopitem}}"
    
    cmd=>:
    echo "hello Australia"<=
    hello Australia
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=22) "echo \"hello Australia\"",
     Code: (int) 0,
     Output: (string) (len=15) "hello Australia",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "hello {{.loopitem}}"
    
    cmd=>:
    echo "hello British"<=
    hello British
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=20) "echo \"hello British\"",
     Code: (int) 0,
     Output: (string) (len=13) "hello British",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "hello {{.loopitem}}"
    
    cmd=>:
    echo "hello China"<=
    hello China
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"hello China\"",
     Code: (int) 0,
     Output: (string) (len=11) "hello China",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "hello {{.loopitem}}"
    
    cmd=>:
    echo "hello Danmark"<=
    hello Danmark
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=20) "echo \"hello Danmark\"",
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
          "population": "1.4b",
          "name": "China"
        },
        {
          "population": "30m",
          "name": "Danmark"
        }
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello Danmark\"",
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
          "name": "Danmark",
          "population": "30m"
        }
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello Danmark\"",
        Code: 0,
        Output: "hello Danmark",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello Danmark\"",
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
          "population": "30m",
          "name": "Danmark"
        }
      }
    })
    
    cmd( 1):
    echo "hello {{.loopitem.name}}"
    
    cmd=>:
    echo "hello Australia"<=
    hello Australia
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=22) "echo \"hello Australia\"",
     Code: (int) 0,
     Output: (string) (len=15) "hello Australia",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello {{.loopitem.population}}"
    
    cmd=>:
    echo "hello 20m"<=
    hello 20m
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=16) "echo \"hello 20m\"",
     Code: (int) 0,
     Output: (string) (len=9) "hello 20m",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "hello {{.loopitem.name}}"
    
    cmd=>:
    echo "hello British"<=
    hello British
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=20) "echo \"hello British\"",
     Code: (int) 0,
     Output: (string) (len=13) "hello British",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello {{.loopitem.population}}"
    
    cmd=>:
    echo "hello 2000m"<=
    hello 2000m
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"hello 2000m\"",
     Code: (int) 0,
     Output: (string) (len=11) "hello 2000m",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "hello {{.loopitem.name}}"
    
    cmd=>:
    echo "hello China"<=
    hello China
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"hello China\"",
     Code: (int) 0,
     Output: (string) (len=11) "hello China",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello {{.loopitem.population}}"
    
    cmd=>:
    echo "hello 1.4b"<=
    hello 1.4b
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=17) "echo \"hello 1.4b\"",
     Code: (int) 0,
     Output: (string) (len=10) "hello 1.4b",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "hello {{.loopitem.name}}"
    
    cmd=>:
    echo "hello Danmark"<=
    hello Danmark
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=20) "echo \"hello Danmark\"",
     Code: (int) 0,
     Output: (string) (len=13) "hello Danmark",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello {{.loopitem.population}}"
    
    cmd=>:
    echo "hello 30m"<=
    hello 30m
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=16) "echo \"hello 30m\"",
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
        Cmd: "echo \"hello 30m\"",
        Code: 0,
        Output: "hello 30m",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
      "listname": "countries"
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
          "population": "1.4b",
          "name": "China"
        },
        {
          "population": "30m",
          "name": "Danmark"
        }
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello 30m\"",
        Code: 0,
        Output: "hello 30m",
        ErrMsg: ""
      }),
      "listname": "countries"
    }
    
    
    self: final context exec vars:
    
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
          "name": "China",
          "population": "1.4b"
        },
        {
          "population": "30m",
          "name": "Danmark"
        }
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello 30m\"",
        Code: 0,
        Output: "hello 30m",
        ErrMsg: ""
      }),
      "listname": "countries"
    })
    
    cmd( 1):
    echo "hello {{.loopindex}}"
    
    cmd=>:
    echo "hello 0"<=
    hello 0
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=14) "echo \"hello 0\"",
     Code: (int) 0,
     Output: (string) (len=7) "hello 0",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello {{.loopindex1}}"
    
    cmd=>:
    echo "hello 1"<=
    hello 1
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=14) "echo \"hello 1\"",
     Code: (int) 0,
     Output: (string) (len=7) "hello 1",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "hello {{.loopitem.name}}"
    
    cmd=>:
    echo "hello Australia"<=
    hello Australia
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=22) "echo \"hello Australia\"",
     Code: (int) 0,
     Output: (string) (len=15) "hello Australia",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo "hello {{.loopitem.population}}"
    
    cmd=>:
    echo "hello 20m"<=
    hello 20m
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=16) "echo \"hello 20m\"",
     Code: (int) 0,
     Output: (string) (len=9) "hello 20m",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "hello {{.loopindex}}"
    
    cmd=>:
    echo "hello 1"<=
    hello 1
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=14) "echo \"hello 1\"",
     Code: (int) 0,
     Output: (string) (len=7) "hello 1",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello {{.loopindex1}}"
    
    cmd=>:
    echo "hello 2"<=
    hello 2
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=14) "echo \"hello 2\"",
     Code: (int) 0,
     Output: (string) (len=7) "hello 2",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "hello {{.loopitem.name}}"
    
    cmd=>:
    echo "hello British"<=
    hello British
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=20) "echo \"hello British\"",
     Code: (int) 0,
     Output: (string) (len=13) "hello British",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo "hello {{.loopitem.population}}"
    
    cmd=>:
    echo "hello 2000m"<=
    hello 2000m
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"hello 2000m\"",
     Code: (int) 0,
     Output: (string) (len=11) "hello 2000m",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "hello {{.loopindex}}"
    
    cmd=>:
    echo "hello 2"<=
    hello 2
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=14) "echo \"hello 2\"",
     Code: (int) 0,
     Output: (string) (len=7) "hello 2",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello {{.loopindex1}}"
    
    cmd=>:
    echo "hello 3"<=
    hello 3
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=14) "echo \"hello 3\"",
     Code: (int) 0,
     Output: (string) (len=7) "hello 3",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "hello {{.loopitem.name}}"
    
    cmd=>:
    echo "hello China"<=
    hello China
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"hello China\"",
     Code: (int) 0,
     Output: (string) (len=11) "hello China",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo "hello {{.loopitem.population}}"
    
    cmd=>:
    echo "hello 1.4b"<=
    hello 1.4b
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=17) "echo \"hello 1.4b\"",
     Code: (int) 0,
     Output: (string) (len=10) "hello 1.4b",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "hello {{.loopindex}}"
    
    cmd=>:
    echo "hello 3"<=
    hello 3
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=14) "echo \"hello 3\"",
     Code: (int) 0,
     Output: (string) (len=7) "hello 3",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello {{.loopindex1}}"
    
    cmd=>:
    echo "hello 4"<=
    hello 4
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=14) "echo \"hello 4\"",
     Code: (int) 0,
     Output: (string) (len=7) "hello 4",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "hello {{.loopitem.name}}"
    
    cmd=>:
    echo "hello Danmark"<=
    hello Danmark
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=20) "echo \"hello Danmark\"",
     Code: (int) 0,
     Output: (string) (len=13) "hello Danmark",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo "hello {{.loopitem.population}}"
    
    cmd=>:
    echo "hello 30m"<=
    hello 30m
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=16) "echo \"hello 30m\"",
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
