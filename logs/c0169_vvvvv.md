---
title: "c0169_vvvvv"
date: 2020-08-09T01:36:26+88:00
draft: false
weight: 11694

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0169
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0169
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001bf960)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
    }
    
    (core.Cache) {
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "ping goole.com"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: {
        "ignoreError"
      },
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 500,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com<=
     WARN: [explicit timeout:] - [500 milli seconds]
    PING goole.com (217.160.0.201): 56 data bytes
          exec wait -> signal: killed
    -----trace for reference-----
     WARN: [timeout] - [shell execution timed out]
          signal: killed
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=14) "ping goole.com",
     Code: (int) -1,
     Output: (string) "",
     ErrMsg: (string) (len=14) "signal: killed"
    }
    
     WARN: [HightLight:] - [Error ignored!!!]
    -Step2:
    {
      Name: "",
      Do: {
        "echo \"hello, world\"",
        "ping goole.com",
        "echo \"hello, world\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: {
        "ignoreError"
      },
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 500,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      })
    })
    
    cmd( 1):
    echo "hello, world"
    
    cmd=>:
    echo "hello, world"<=
     WARN: [explicit timeout:] - [500 milli seconds]
    hello, world
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"hello, world\"",
     Code: (int) 0,
     Output: (string) (len=12) "hello, world",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    ping goole.com
    
    cmd=>:
    ping goole.com<=
     WARN: [explicit timeout:] - [500 milli seconds]
    PING goole.com (217.160.0.201): 56 data bytes
          exec wait -> signal: killed
    -----trace for reference-----
     WARN: [timeout] - [shell execution timed out]
          signal: killed
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=14) "ping goole.com",
     Code: (int) -1,
     Output: (string) "",
     ErrMsg: (string) (len=14) "signal: killed"
    }
    
    cmd( 3):
    echo "hello, world"
    
    cmd=>:
    echo "hello, world"<=
     WARN: [explicit timeout:] - [500 milli seconds]
    hello, world
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"hello, world\"",
     Code: (int) 0,
     Output: (string) (len=12) "hello, world",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step3: [: an example of retry
    it tries to ping 4 times with a timeout of 2 seconds every time
     ]
    {
      Name: "",
      Do: {
        "ping goole.com"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "an example of retry\nit tries to ping 4 times with a timeout of 2 seconds every time\n",
      Reg: "",
      Flags: {
        "ignoreError"
      },
      If: "",
      Else: <nil>,
      Loop: {
        "retry1",
        "retry2",
        "retry3",
        "retry4"
      },
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 500,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello, world\"",
        Code: 0,
        Output: "hello, world",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello, world\"",
        Code: 0,
        Output: "hello, world",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello, world\"",
        Code: 0,
        Output: "hello, world",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com<=
     WARN: [explicit timeout:] - [500 milli seconds]
    PING goole.com (217.160.0.201): 56 data bytes
          exec wait -> signal: killed
    -----trace for reference-----
     WARN: [timeout] - [shell execution timed out]
          signal: killed
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=14) "ping goole.com",
     Code: (int) -1,
     Output: (string) "",
     ErrMsg: (string) (len=14) "signal: killed"
    }
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com<=
     WARN: [explicit timeout:] - [500 milli seconds]
    PING goole.com (217.160.0.201): 56 data bytes
          exec wait -> signal: killed
    -----trace for reference-----
     WARN: [timeout] - [shell execution timed out]
          signal: killed
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=14) "ping goole.com",
     Code: (int) -1,
     Output: (string) "",
     ErrMsg: (string) (len=14) "signal: killed"
    }
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com<=
     WARN: [explicit timeout:] - [500 milli seconds]
    PING goole.com (217.160.0.201): 56 data bytes
          exec wait -> signal: killed
    -----trace for reference-----
     WARN: [timeout] - [shell execution timed out]
          signal: killed
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=14) "ping goole.com",
     Code: (int) -1,
     Output: (string) "",
     ErrMsg: (string) (len=14) "signal: killed"
    }
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com<=
     WARN: [explicit timeout:] - [500 milli seconds]
    PING goole.com (217.160.0.201): 56 data bytes
          exec wait -> signal: killed
    -----trace for reference-----
     WARN: [timeout] - [shell execution timed out]
          signal: killed
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=14) "ping goole.com",
     Code: (int) -1,
     Output: (string) "",
     ErrMsg: (string) (len=14) "signal: killed"
    }
    
     WARN: [HightLight:] - [Error ignored!!!]
    -Step4: [: an example of retry
    it tries to ping 4 times with a timeout of 2 seconds every time
    with every attemp it puts a delay of 2 seconds
     ]
    {
      Name: "",
      Do: {
        {
          "func": "shell",
          "do": {
            "ping goole.com"
          },
          "timeout": 500,
          "flags": {
            "ignoreError"
          }
        },
        {
          "do": {
            {
              "name": "sleep",
              "desc": "delay 2 seconds in each attemp",
              "cmd": 200
            }
          },
          "func": "cmd"
        }
      },
      Dox: <nil>,
      Func: "block",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "an example of retry\nit tries to ping 4 times with a timeout of 2 seconds every time\nwith every attemp it puts a delay of 2 seconds\n",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "retry1",
        "retry2",
        "retry3",
        "retry4"
      },
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
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      })
    })
    
    -Step1:
    {
      Name: "",
      Do: {
        "ping goole.com"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: {
        "ignoreError"
      },
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 500,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "loopitem": "retry1"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "loopitem": "retry1"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "retry1",
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      })
    })
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com<=
     WARN: [explicit timeout:] - [500 milli seconds]
    PING goole.com (217.160.0.201): 56 data bytes
          exec wait -> signal: killed
    -----trace for reference-----
     WARN: [timeout] - [shell execution timed out]
          signal: killed
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=14) "ping goole.com",
     Code: (int) -1,
     Output: (string) "",
     ErrMsg: (string) (len=14) "signal: killed"
    }
    
     WARN: [HightLight:] - [Error ignored!!!]
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "sleep",
          "desc": "delay 2 seconds in each attemp",
          "cmd": 200
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
      "loopitem": "retry1",
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopitem": "retry1",
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "loopitem": "retry1",
      "loopindex1": 1
    })
    
    %!s(int=200)
    ~SubStep1: [sleep: delay 2 seconds in each attemp ]
    sleeping 200 milli seconds
    ..
    -Step1:
    {
      Name: "",
      Do: {
        "ping goole.com"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: {
        "ignoreError"
      },
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 500,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "loopitem": "retry2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "loopitem": "retry2",
      "loopindex": 1,
      "loopindex1": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "loopitem": "retry2"
    })
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com<=
     WARN: [explicit timeout:] - [500 milli seconds]
    PING goole.com (217.160.0.201): 56 data bytes
          exec wait -> signal: killed
    -----trace for reference-----
     WARN: [timeout] - [shell execution timed out]
          signal: killed
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=14) "ping goole.com",
     Code: (int) -1,
     Output: (string) "",
     ErrMsg: (string) (len=14) "signal: killed"
    }
    
     WARN: [HightLight:] - [Error ignored!!!]
    -Step2:
    {
      Name: "",
      Do: {
        {
          "desc": "delay 2 seconds in each attemp",
          "cmd": 200,
          "name": "sleep"
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
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "loopitem": "retry2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopitem": "retry2",
      "loopindex": 1,
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "loopitem": "retry2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    %!s(int=200)
    ~SubStep1: [sleep: delay 2 seconds in each attemp ]
    sleeping 200 milli seconds
    ..
    -Step1:
    {
      Name: "",
      Do: {
        "ping goole.com"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: {
        "ignoreError"
      },
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 500,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 3,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "loopitem": "retry3",
      "loopindex": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "loopitem": "retry3",
      "loopindex": 2,
      "loopindex1": 3
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 3,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "loopitem": "retry3",
      "loopindex": 2
    })
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com<=
     WARN: [explicit timeout:] - [500 milli seconds]
    PING goole.com (217.160.0.201): 56 data bytes
          exec wait -> signal: killed
    -----trace for reference-----
     WARN: [timeout] - [shell execution timed out]
          signal: killed
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=14) "ping goole.com",
     Code: (int) -1,
     Output: (string) "",
     ErrMsg: (string) (len=14) "signal: killed"
    }
    
     WARN: [HightLight:] - [Error ignored!!!]
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "sleep",
          "desc": "delay 2 seconds in each attemp",
          "cmd": 200
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
      "loopindex1": 3,
      "loopitem": "retry3",
      "loopindex": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "loopindex1": 3,
      "loopitem": "retry3",
      "loopindex": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "loopindex1": 3,
      "loopitem": "retry3",
      "loopindex": 2
    })
    
    %!s(int=200)
    ~SubStep1: [sleep: delay 2 seconds in each attemp ]
    sleeping 200 milli seconds
    ..
    -Step1:
    {
      Name: "",
      Do: {
        "ping goole.com"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: {
        "ignoreError"
      },
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 500,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "loopitem": "retry4",
      "loopindex": 3,
      "loopindex1": 4
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopitem": "retry4",
      "loopindex": 3,
      "loopindex1": 4,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 4,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "loopitem": "retry4",
      "loopindex": 3
    })
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com<=
     WARN: [explicit timeout:] - [500 milli seconds]
    PING goole.com (217.160.0.201): 56 data bytes
          exec wait -> signal: killed
    -----trace for reference-----
     WARN: [timeout] - [shell execution timed out]
          signal: killed
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=14) "ping goole.com",
     Code: (int) -1,
     Output: (string) "",
     ErrMsg: (string) (len=14) "signal: killed"
    }
    
     WARN: [HightLight:] - [Error ignored!!!]
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "sleep",
          "desc": "delay 2 seconds in each attemp",
          "cmd": 200
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
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "loopitem": "retry4",
      "loopindex": 3,
      "loopindex1": 4
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "loopitem": "retry4",
      "loopindex": 3,
      "loopindex1": 4
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "loopitem": "retry4",
      "loopindex": 3,
      "loopindex1": 4
    })
    
    %!s(int=200)
    ~SubStep1: [sleep: delay 2 seconds in each attemp ]
    sleeping 200 milli seconds
    ..
    -Step5: [: loop with customised range
     ]
    {
      Name: "",
      Do: {
        "ping goole.com"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "loop with customised range\n",
      Reg: "",
      Flags: {
        "ignoreError"
      },
      If: "",
      Else: <nil>,
      Loop: "{{loopRange 100 105 \"myretry\"}}",
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 500,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      })
    })
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com<=
     WARN: [explicit timeout:] - [500 milli seconds]
    PING goole.com (217.160.0.201): 56 data bytes
          exec wait -> signal: killed
    -----trace for reference-----
     WARN: [timeout] - [shell execution timed out]
          signal: killed
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=14) "ping goole.com",
     Code: (int) -1,
     Output: (string) "",
     ErrMsg: (string) (len=14) "signal: killed"
    }
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com<=
     WARN: [explicit timeout:] - [500 milli seconds]
    PING goole.com (217.160.0.201): 56 data bytes
          exec wait -> signal: killed
    -----trace for reference-----
     WARN: [timeout] - [shell execution timed out]
          signal: killed
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=14) "ping goole.com",
     Code: (int) -1,
     Output: (string) "",
     ErrMsg: (string) (len=14) "signal: killed"
    }
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com<=
     WARN: [explicit timeout:] - [500 milli seconds]
    PING goole.com (217.160.0.201): 56 data bytes
          exec wait -> signal: killed
    -----trace for reference-----
     WARN: [timeout] - [shell execution timed out]
          signal: killed
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=14) "ping goole.com",
     Code: (int) -1,
     Output: (string) "",
     ErrMsg: (string) (len=14) "signal: killed"
    }
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com<=
     WARN: [explicit timeout:] - [500 milli seconds]
    PING goole.com (217.160.0.201): 56 data bytes
          exec wait -> signal: killed
    -----trace for reference-----
     WARN: [timeout] - [shell execution timed out]
          signal: killed
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=14) "ping goole.com",
     Code: (int) -1,
     Output: (string) "",
     ErrMsg: (string) (len=14) "signal: killed"
    }
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com<=
     WARN: [explicit timeout:] - [500 milli seconds]
    PING goole.com (217.160.0.201): 56 data bytes
          exec wait -> signal: killed
    -----trace for reference-----
     WARN: [timeout] - [shell execution timed out]
          signal: killed
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=14) "ping goole.com",
     Code: (int) -1,
     Output: (string) "",
     ErrMsg: (string) (len=14) "signal: killed"
    }
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com<=
     WARN: [explicit timeout:] - [500 milli seconds]
    PING goole.com (217.160.0.201): 56 data bytes
          exec wait -> signal: killed
    -----trace for reference-----
     WARN: [timeout] - [shell execution timed out]
          signal: killed
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=14) "ping goole.com",
     Code: (int) -1,
     Output: (string) "",
     ErrMsg: (string) (len=14) "signal: killed"
    }
    
     WARN: [HightLight:] - [Error ignored!!!]
    -Step6: [: an example of retry
    it tries to ping 4 times with a timeout of 2 seconds every time
    with every attemp it puts a delay of 2 seconds
    it also uses dynamic loopRange instead of prepared list of value
     ]
    {
      Name: "",
      Do: {
        {
          "func": "shell",
          "do": {
            "ping goole.com"
          },
          "timeout": 500,
          "flags": {
            "ignoreError"
          }
        },
        {
          "func": "cmd",
          "do": {
            {
              "name": "sleep",
              "desc": "delay 2 seconds in each attemp",
              "cmd": 200
            }
          }
        }
      },
      Dox: <nil>,
      Func: "block",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "an example of retry\nit tries to ping 4 times with a timeout of 2 seconds every time\nwith every attemp it puts a delay of 2 seconds\nit also uses dynamic loopRange instead of prepared list of value\n",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: "{{loopRange 100 103 \"myretry\"}}",
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "myretry": {
        100,
        101,
        102,
        103,
        104,
        105
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "myretry": {
        100,
        101,
        102,
        103,
        104,
        105
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "myretry": {
        100,
        101,
        102,
        103,
        104,
        105
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      })
    })
    
    -Step1:
    {
      Name: "",
      Do: {
        "ping goole.com"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: {
        "ignoreError"
      },
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 500,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "myretry": {
        100,
        101,
        102,
        103
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "loopindex1": 1,
      "loopitem": 100
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "myretry": {
        100,
        101,
        102,
        103
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "loopindex1": 1,
      "loopitem": 100
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "myretry": {
        100,
        101,
        102,
        103
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "loopindex1": 1,
      "loopitem": 100
    })
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com<=
     WARN: [explicit timeout:] - [500 milli seconds]
    PING goole.com (217.160.0.201): 56 data bytes
          exec wait -> signal: killed
    -----trace for reference-----
     WARN: [timeout] - [shell execution timed out]
          signal: killed
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=14) "ping goole.com",
     Code: (int) -1,
     Output: (string) "",
     ErrMsg: (string) (len=14) "signal: killed"
    }
    
     WARN: [HightLight:] - [Error ignored!!!]
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "sleep",
          "desc": "delay 2 seconds in each attemp",
          "cmd": 200
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
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "myretry": {
        100,
        101,
        102,
        103
      },
      "loopitem": 100,
      "loopindex1": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "myretry": {
        100,
        101,
        102,
        103
      },
      "loopitem": 100,
      "loopindex1": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "myretry": {
        100,
        101,
        102,
        103
      },
      "loopitem": 100,
      "loopindex1": 1
    })
    
    %!s(int=200)
    ~SubStep1: [sleep: delay 2 seconds in each attemp ]
    sleeping 200 milli seconds
    ..
    -Step1:
    {
      Name: "",
      Do: {
        "ping goole.com"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: {
        "ignoreError"
      },
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 500,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "myretry": {
        100,
        101,
        102,
        103
      },
      "loopitem": 101,
      "loopindex": 1,
      "loopindex1": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopitem": 101,
      "loopindex": 1,
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "myretry": {
        100,
        101,
        102,
        103
      }
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "myretry": {
        100,
        101,
        102,
        103
      },
      "loopitem": 101,
      "loopindex": 1,
      "loopindex1": 2
    })
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com<=
     WARN: [explicit timeout:] - [500 milli seconds]
    PING goole.com (217.160.0.201): 56 data bytes
          exec wait -> signal: killed
    -----trace for reference-----
     WARN: [timeout] - [shell execution timed out]
          signal: killed
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=14) "ping goole.com",
     Code: (int) -1,
     Output: (string) "",
     ErrMsg: (string) (len=14) "signal: killed"
    }
    
     WARN: [HightLight:] - [Error ignored!!!]
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "sleep",
          "desc": "delay 2 seconds in each attemp",
          "cmd": 200
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
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "myretry": {
        100,
        101,
        102,
        103
      },
      "loopindex1": 2,
      "loopitem": 101,
      "loopindex": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 2,
      "loopitem": 101,
      "loopindex": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "myretry": {
        100,
        101,
        102,
        103
      }
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "myretry": {
        100,
        101,
        102,
        103
      },
      "loopindex1": 2,
      "loopitem": 101,
      "loopindex": 1
    })
    
    %!s(int=200)
    ~SubStep1: [sleep: delay 2 seconds in each attemp ]
    sleeping 200 milli seconds
    ..
    -Step1:
    {
      Name: "",
      Do: {
        "ping goole.com"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: {
        "ignoreError"
      },
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 500,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "myretry": {
        100,
        101,
        102,
        103
      },
      "loopindex": 2,
      "loopindex1": 3,
      "loopitem": 102
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 2,
      "loopindex1": 3,
      "loopitem": 102,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "myretry": {
        100,
        101,
        102,
        103
      }
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": 102,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "myretry": {
        100,
        101,
        102,
        103
      },
      "loopindex": 2,
      "loopindex1": 3
    })
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com<=
     WARN: [explicit timeout:] - [500 milli seconds]
    PING goole.com (217.160.0.201): 56 data bytes
          exec wait -> signal: killed
    -----trace for reference-----
     WARN: [timeout] - [shell execution timed out]
          signal: killed
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=14) "ping goole.com",
     Code: (int) -1,
     Output: (string) "",
     ErrMsg: (string) (len=14) "signal: killed"
    }
    
     WARN: [HightLight:] - [Error ignored!!!]
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "sleep",
          "desc": "delay 2 seconds in each attemp",
          "cmd": 200
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
      "myretry": {
        100,
        101,
        102,
        103
      },
      "loopitem": 102,
      "loopindex": 2,
      "loopindex1": 3,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 3,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "myretry": {
        100,
        101,
        102,
        103
      },
      "loopitem": 102,
      "loopindex": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "myretry": {
        100,
        101,
        102,
        103
      },
      "loopitem": 102,
      "loopindex": 2,
      "loopindex1": 3,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      })
    })
    
    %!s(int=200)
    ~SubStep1: [sleep: delay 2 seconds in each attemp ]
    sleeping 200 milli seconds
    ..
    -Step1:
    {
      Name: "",
      Do: {
        "ping goole.com"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: {
        "ignoreError"
      },
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 500,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "myretry": {
        100,
        101,
        102,
        103
      },
      "loopitem": 103,
      "loopindex": 3,
      "loopindex1": 4,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "myretry": {
        100,
        101,
        102,
        103
      },
      "loopitem": 103,
      "loopindex": 3,
      "loopindex1": 4,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 3,
      "loopindex1": 4,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "myretry": {
        100,
        101,
        102,
        103
      },
      "loopitem": 103
    })
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com<=
     WARN: [explicit timeout:] - [500 milli seconds]
    PING goole.com (217.160.0.201): 56 data bytes
          exec wait -> signal: killed
    -----trace for reference-----
     WARN: [timeout] - [shell execution timed out]
          signal: killed
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=14) "ping goole.com",
     Code: (int) -1,
     Output: (string) "",
     ErrMsg: (string) (len=14) "signal: killed"
    }
    
     WARN: [HightLight:] - [Error ignored!!!]
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "sleep",
          "desc": "delay 2 seconds in each attemp",
          "cmd": 200
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
      "loopitem": 103,
      "loopindex": 3,
      "loopindex1": 4,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "myretry": {
        100,
        101,
        102,
        103
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "myretry": {
        100,
        101,
        102,
        103
      },
      "loopitem": 103,
      "loopindex": 3,
      "loopindex1": 4
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "",
        ErrMsg: "signal: killed"
      }),
      "myretry": {
        100,
        101,
        102,
        103
      },
      "loopitem": 103,
      "loopindex": 3,
      "loopindex1": 4
    })
    
    %!s(int=200)
    ~SubStep1: [sleep: delay 2 seconds in each attemp ]
    sleeping 200 milli seconds
    ..
    
```

##### Logs with different verbose level
* [c0169 log - verbose level v](../../logs/c0169_v)
* [c0169 log - verbose level vv](../../logs/c0169_vv)
* [c0169 log - verbose level vvv](../../logs/c0169_vvv)
* [c0169 log - verbose level vvvv](../../logs/c0169_vvvv)
* [c0169 log - verbose level vvvvv](../../logs/c0169_vvvvv)

##### References
* [Related Chapter](../../loop/c0169)
