---
title: "c0151_vvvvv"
date: 2020-10-07T00:11:27+1010:00
draft: false
weight: 11514

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0151
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0151
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001e58a0)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "greet_to": "Tom",
      "weather": "sunny"
    })
    
    (*core.Cache)(0xc000126958)((len=2) {
     (string) (len=8) "greet_to": (string) (len=3) "Tom",
     (string) (len=7) "weather": (string) (len=5) "sunny"
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "weather": "sunny",
      "greet_to": "Tom"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task: main task of hello world demo of UPcmd ]
    Executing task stack layer: 1
    
    -Step1: [: greet to Tom ]
    {
      Name: "",
      Do: {
        "greet"
      },
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "greet to Tom",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "greet_to": "Tom",
      "weather": "sunny"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "greet_to": "Tom",
      "weather": "sunny",
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "greet_to": "Tom",
      "weather": "sunny"
    })
    
    caller's vars to task (greet)::
    (*core.Cache)({
      "greet_to": "Tom",
      "weather": "sunny",
      "up_runtime_task_layer_number": 0
    })
    
      located task-> 2 [greet]: 
    =Task2: [task ==> greet: greet to some one ]
    Executing task stack layer: 2
    
    --Step1: [: say hello ]
    {
      Name: "",
      Do: {
        "echo \"Hello, {{.greet_to}}\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "say hello",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "weather": "sunny",
      "up_runtime_task_layer_number": 1,
      "greet_to": "Tom"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "greet_to": "Tom",
      "weather": "sunny",
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "weather": "sunny",
      "up_runtime_task_layer_number": 1,
      "greet_to": "Tom"
    })
    
    cmd( 1):
    echo "Hello, {{.greet_to}}"
    
    cmd=>:
    echo "Hello, Tom"
    -
    Hello, Tom
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=17) "echo \"Hello, Tom\"",
     Code: (int) 0,
     Output: (string) (len=10) "Hello, Tom",
     ErrMsg: (string) ""
    }
    
    . ok
    --Step2: [: talk about weather ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "It is {{.weather}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "talk about weather",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Tom\"",
        Code: 0,
        Output: "Hello, Tom",
        ErrMsg: ""
      }),
      "greet_to": "Tom",
      "weather": "sunny"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "greet_to": "Tom",
      "weather": "sunny",
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Tom\"",
        Code: 0,
        Output: "Hello, Tom",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Tom\"",
        Code: 0,
        Output: "Hello, Tom",
        ErrMsg: ""
      }),
      "greet_to": "Tom",
      "weather": "sunny",
      "up_runtime_task_layer_number": 1
    })
    
    It is {{.weather}}
    ~~SubStep1: [print:  ]
    It is sunny
    --Step3: [: ice break ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "What a great day!"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "ice break",
      Reg: "",
      Flags: <nil>,
      If: "{{eq .weather \"sunny\"}}",
      Else: {
        {
          "func": "cmd",
          "do": {
            {
              "name": "print",
              "cmd": "What a bad day!!"
            }
          }
        }
      },
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "greet_to": "Tom",
      "weather": "sunny",
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Tom\"",
        Code: 0,
        Output: "Hello, Tom",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "weather": "sunny",
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Tom\"",
        Code: 0,
        Output: "Hello, Tom",
        ErrMsg: ""
      }),
      "greet_to": "Tom"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "greet_to": "Tom",
      "weather": "sunny",
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Tom\"",
        Code: 0,
        Output: "Hello, Tom",
        ErrMsg: ""
      })
    })
    
    What a great day!
    ~~SubStep1: [print:  ]
    What a great day!
    -Step2: [: greet to Grace ]
    {
      Name: "",
      Do: {
        "greet"
      },
      Dox: <nil>,
      Func: "call",
      Vars: {
        "greet_to": "Grace"
      },
      Dvars: <nil>,
      Desc: "greet to Grace",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "weather": "sunny",
      "greet_to": "Grace",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "weather": "sunny",
      "greet_to": "Grace",
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "greet_to": "Grace",
      "up_runtime_task_layer_number": 1,
      "weather": "sunny"
    })
    
    caller's vars to task (greet)::
    (*core.Cache)({
      "greet_to": "Grace",
      "up_runtime_task_layer_number": 1,
      "weather": "sunny"
    })
    
      located task-> 2 [greet]: 
    =Task2: [task ==> greet: greet to some one ]
    Executing task stack layer: 2
    
    --Step1: [: say hello ]
    {
      Name: "",
      Do: {
        "echo \"Hello, {{.greet_to}}\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "say hello",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "weather": "sunny",
      "greet_to": "Grace",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "weather": "sunny",
      "greet_to": "Grace"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "weather": "sunny",
      "greet_to": "Grace",
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    echo "Hello, {{.greet_to}}"
    
    cmd=>:
    echo "Hello, Grace"
    -
    Hello, Grace
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"Hello, Grace\"",
     Code: (int) 0,
     Output: (string) (len=12) "Hello, Grace",
     ErrMsg: (string) ""
    }
    
    . ok
    --Step2: [: talk about weather ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "It is {{.weather}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "talk about weather",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "weather": "sunny",
      "greet_to": "Grace",
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Grace\"",
        Code: 0,
        Output: "Hello, Grace",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Grace\"",
        Code: 0,
        Output: "Hello, Grace",
        ErrMsg: ""
      }),
      "weather": "sunny",
      "greet_to": "Grace",
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "weather": "sunny",
      "greet_to": "Grace",
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Grace\"",
        Code: 0,
        Output: "Hello, Grace",
        ErrMsg: ""
      })
    })
    
    It is {{.weather}}
    ~~SubStep1: [print:  ]
    It is sunny
    --Step3: [: ice break ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "What a great day!"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "ice break",
      Reg: "",
      Flags: <nil>,
      If: "{{eq .weather \"sunny\"}}",
      Else: {
        {
          "func": "cmd",
          "do": {
            {
              "name": "print",
              "cmd": "What a bad day!!"
            }
          }
        }
      },
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Grace\"",
        Code: 0,
        Output: "Hello, Grace",
        ErrMsg: ""
      }),
      "weather": "sunny",
      "greet_to": "Grace",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "weather": "sunny",
      "greet_to": "Grace",
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Grace\"",
        Code: 0,
        Output: "Hello, Grace",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "weather": "sunny",
      "greet_to": "Grace",
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Grace\"",
        Code: 0,
        Output: "Hello, Grace",
        ErrMsg: ""
      })
    })
    
    What a great day!
    ~~SubStep1: [print:  ]
    What a great day!
    -Step3: [: do  you get the idea? ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "Have you got a little taste of using the UPcmd?\n"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "do  you get the idea?",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "weather": "sunny",
      "greet_to": "Tom",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "weather": "sunny",
      "greet_to": "Tom"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "weather": "sunny",
      "greet_to": "Tom",
      "up_runtime_task_layer_number": 1
    })
    
    Have you got a little taste of using the UPcmd?
    
    ~SubStep1: [print:  ]
    Have you got a little taste of using the UPcmd?
    
    -Step4: [: greet to a team ]
    {
      Name: "",
      Do: {
        "sayhi"
      },
      Dox: <nil>,
      Func: "call",
      Vars: {
        "team": {
          "Jason",
          "Connie"
        },
        "weather": "stormy"
      },
      Dvars: <nil>,
      Desc: "greet to a team",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: "team",
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "team": {
        "Jason",
        "Connie"
      },
      "greet_to": "Tom",
      "weather": "stormy",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "greet_to": "Tom",
      "weather": "stormy",
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      }
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "greet_to": "Tom",
      "weather": "stormy",
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      }
    })
    
    caller's vars to task (sayhi)::
    (*core.Cache)({
      "loopindex1": 1,
      "greet_to": "Tom",
      "weather": "stormy",
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0
    })
    
      located task-> 3 [sayhi]: 
    =Task3: [task ==> sayhi: say hi to some one ]
    Executing task stack layer: 2
    
    --Step1: [: say hi to someone ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "Hi {{.loopitem}}, how are you?"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "say hi to someone",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "greet_to": "Tom",
      "weather": "stormy",
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "greet_to": "Tom",
      "weather": "stormy"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 1,
      "greet_to": "Tom",
      "weather": "stormy",
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0
    })
    
    Hi {{.loopitem}}, how are you?
    ~~SubStep1: [print:  ]
    Hi Jason, how are you?
    --Step2: [: greet to the team member ]
    {
      Name: "",
      Do: {
        "greet"
      },
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: {
        {
          Name: "greet_to",
          Value: "{{.loopitem}}",
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
      Desc: "greet to the team member",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "greet_to": "Tom",
      "weather": "stormy",
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      }
    })
    
    [local] dvar expanded result:
    {
      "greet_to": "Jason"
    }
    
    
    scope[local] merged: {
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "greet_to": "Jason",
      "weather": "stormy",
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "greet_to": "Jason",
      "weather": "stormy",
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason"
    })
    
    caller's vars to task (greet)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "greet_to": "Jason",
      "weather": "stormy"
    })
    
      located task-> 2 [greet]: 
    ==Task2: [task/sayhi ==> greet: greet to some one ]
    Executing task stack layer: 3
    
    ---Step1: [: say hello ]
    {
      Name: "",
      Do: {
        "echo \"Hello, {{.greet_to}}\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "say hello",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "greet_to": "Jason",
      "weather": "stormy",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "greet_to": "Jason",
      "weather": "stormy",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 1,
      "greet_to": "Jason",
      "weather": "stormy",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0
    })
    
    cmd( 1):
    echo "Hello, {{.greet_to}}"
    
    cmd=>:
    echo "Hello, Jason"
    -
    Hello, Jason
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"Hello, Jason\"",
     Code: (int) 0,
     Output: (string) (len=12) "Hello, Jason",
     ErrMsg: (string) ""
    }
    
    . ok
    ---Step2: [: talk about weather ]
    {
      Name: "",
      Do: {
        {
          "cmd": "It is {{.weather}}",
          "name": "print"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "talk about weather",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Jason\"",
        Code: 0,
        Output: "Hello, Jason",
        ErrMsg: ""
      }),
      "greet_to": "Jason",
      "weather": "stormy",
      "up_runtime_task_layer_number": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "greet_to": "Jason",
      "weather": "stormy",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Jason\"",
        Code: 0,
        Output: "Hello, Jason",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Jason\"",
        Code: 0,
        Output: "Hello, Jason",
        ErrMsg: ""
      }),
      "greet_to": "Jason",
      "weather": "stormy",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      }
    })
    
    It is {{.weather}}
    ~~~SubStep1: [print:  ]
    It is stormy
    ---Step3: [: ice break ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "What a great day!"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "ice break",
      Reg: "",
      Flags: <nil>,
      If: "{{eq .weather \"sunny\"}}",
      Else: {
        {
          "func": "cmd",
          "do": {
            {
              "name": "print",
              "cmd": "What a bad day!!"
            }
          }
        }
      },
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Jason\"",
        Code: 0,
        Output: "Hello, Jason",
        ErrMsg: ""
      }),
      "greet_to": "Jason",
      "weather": "stormy",
      "up_runtime_task_layer_number": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "greet_to": "Jason",
      "weather": "stormy",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Jason\"",
        Code: 0,
        Output: "Hello, Jason",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "weather": "stormy",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Jason\"",
        Code: 0,
        Output: "Hello, Jason",
        ErrMsg: ""
      }),
      "greet_to": "Jason"
    })
    
    ---Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "What a bad day!!"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "greet_to": "Jason",
      "weather": "stormy",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 1,
      "greet_to": "Jason",
      "weather": "stormy",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "weather": "stormy",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "greet_to": "Jason"
    })
    
    What a bad day!!
    ~~~SubStep1: [print:  ]
    What a bad day!!
    caller's vars to task (sayhi)::
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "greet_to": "Tom",
      "weather": "stormy",
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie"
    })
    
      located task-> 3 [sayhi]: 
    =Task3: [task ==> sayhi: say hi to some one ]
    Executing task stack layer: 2
    
    --Step1: [: say hi to someone ]
    {
      Name: "",
      Do: {
        {
          "cmd": "Hi {{.loopitem}}, how are you?",
          "name": "print"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "say hi to someone",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie",
      "loopindex": 1,
      "loopindex1": 2,
      "greet_to": "Tom",
      "weather": "stormy"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "greet_to": "Tom",
      "weather": "stormy",
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie",
      "loopindex": 1,
      "loopindex1": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie",
      "loopindex": 1,
      "loopindex1": 2,
      "greet_to": "Tom",
      "weather": "stormy"
    })
    
    Hi {{.loopitem}}, how are you?
    ~~SubStep1: [print:  ]
    Hi Connie, how are you?
    --Step2: [: greet to the team member ]
    {
      Name: "",
      Do: {
        "greet"
      },
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: {
        {
          Name: "greet_to",
          Value: "{{.loopitem}}",
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
      Desc: "greet to the team member",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie",
      "loopindex": 1,
      "loopindex1": 2,
      "greet_to": "Tom",
      "weather": "stormy",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
      "greet_to": "Connie"
    }
    
    
    scope[local] merged: {
      "loopindex": 1,
      "loopindex1": 2,
      "greet_to": "Connie",
      "weather": "stormy",
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "weather": "stormy",
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie",
      "loopindex": 1,
      "loopindex1": 2,
      "greet_to": "Connie"
    })
    
    caller's vars to task (greet)::
    (*core.Cache)({
      "loopitem": "Connie",
      "loopindex": 1,
      "loopindex1": 2,
      "greet_to": "Connie",
      "weather": "stormy",
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      }
    })
    
      located task-> 2 [greet]: 
    ==Task2: [task/sayhi ==> greet: greet to some one ]
    Executing task stack layer: 3
    
    ---Step1: [: say hello ]
    {
      Name: "",
      Do: {
        "echo \"Hello, {{.greet_to}}\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "say hello",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie",
      "loopindex": 1,
      "loopindex1": 2,
      "greet_to": "Connie",
      "weather": "stormy",
      "up_runtime_task_layer_number": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "weather": "stormy",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie",
      "loopindex": 1,
      "loopindex1": 2,
      "greet_to": "Connie"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 2,
      "greet_to": "Connie",
      "weather": "stormy",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie",
      "loopindex": 1
    })
    
    cmd( 1):
    echo "Hello, {{.greet_to}}"
    
    cmd=>:
    echo "Hello, Connie"
    -
    Hello, Connie
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=20) "echo \"Hello, Connie\"",
     Code: (int) 0,
     Output: (string) (len=13) "Hello, Connie",
     ErrMsg: (string) ""
    }
    
    . ok
    ---Step2: [: talk about weather ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "It is {{.weather}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "talk about weather",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "weather": "stormy",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Connie\"",
        Code: 0,
        Output: "Hello, Connie",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie",
      "loopindex": 1,
      "loopindex1": 2,
      "greet_to": "Connie"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie",
      "loopindex": 1,
      "loopindex1": 2,
      "greet_to": "Connie",
      "weather": "stormy",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Connie\"",
        Code: 0,
        Output: "Hello, Connie",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie",
      "loopindex": 1,
      "loopindex1": 2,
      "greet_to": "Connie",
      "weather": "stormy",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Connie\"",
        Code: 0,
        Output: "Hello, Connie",
        ErrMsg: ""
      })
    })
    
    It is {{.weather}}
    ~~~SubStep1: [print:  ]
    It is stormy
    ---Step3: [: ice break ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "What a great day!"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "ice break",
      Reg: "",
      Flags: <nil>,
      If: "{{eq .weather \"sunny\"}}",
      Else: {
        {
          "func": "cmd",
          "do": {
            {
              "name": "print",
              "cmd": "What a bad day!!"
            }
          }
        }
      },
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "weather": "stormy",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Connie\"",
        Code: 0,
        Output: "Hello, Connie",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie",
      "loopindex": 1,
      "loopindex1": 2,
      "greet_to": "Connie"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "weather": "stormy",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Connie\"",
        Code: 0,
        Output: "Hello, Connie",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie",
      "loopindex": 1,
      "loopindex1": 2,
      "greet_to": "Connie"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "Connie",
      "loopindex": 1,
      "loopindex1": 2,
      "greet_to": "Connie",
      "weather": "stormy",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Connie\"",
        Code: 0,
        Output: "Hello, Connie",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      }
    })
    
    ---Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "What a bad day!!"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "greet_to": "Connie",
      "weather": "stormy",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie",
      "loopindex": 1,
      "loopindex1": 2,
      "greet_to": "Connie",
      "weather": "stormy",
      "up_runtime_task_layer_number": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie",
      "loopindex": 1,
      "loopindex1": 2,
      "greet_to": "Connie",
      "weather": "stormy",
      "up_runtime_task_layer_number": 2
    })
    
    What a bad day!!
    ~~~SubStep1: [print:  ]
    What a bad day!!
    
```

##### Logs with different verbose level
* [c0151 log - verbose level v](../../logs/c0151_v)
* [c0151 log - verbose level vv](../../logs/c0151_vv)
* [c0151 log - verbose level vvv](../../logs/c0151_vvv)
* [c0151 log - verbose level vvvv](../../logs/c0151_vvvv)
* [c0151 log - verbose level vvvvv](../../logs/c0151_vvvvv)

##### References
* [Related Chapter](../../quick-start/c0151)
