---
title: "c0169_vvvv"
date: 2020-09-18T00:51:54+99:00
draft: false
weight: 11693

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
    loading [Task]:  ./tests/functests/c0169
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
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com
     WARN: [explicit timeout:] - [500 milli seconds]
    -
    PING goole.com (217.160.0.201): 56 data bytes
    
    -
     WARN: [timeout] - [shell execution timed out]
     .. failed(suppressed if it is not the last step)
     WARN: [ignoreError:] - [Error ignored!!!]
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "PING goole.com (217.160.0.201): 56 data bytes",
        ErrMsg: "signal: killed"
      }),
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "PING goole.com (217.160.0.201): 56 data bytes",
        ErrMsg: "signal: killed"
      }),
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "hello, world"
    
    cmd=>:
    echo "hello, world"
     WARN: [explicit timeout:] - [500 milli seconds]
    -
    hello, world
    
    -
     .. ok
    cmd( 2):
    ping goole.com
    
    cmd=>:
    ping goole.com
     WARN: [explicit timeout:] - [500 milli seconds]
    -
    PING goole.com (217.160.0.201): 56 data bytes
    
    -
     WARN: [timeout] - [shell execution timed out]
     .. failed(suppressed if it is not the last step)
    cmd( 3):
    echo "hello, world"
    
    cmd=>:
    echo "hello, world"
     WARN: [explicit timeout:] - [500 milli seconds]
    -
    hello, world
    
    -
     .. ok
    . ok
    -Step3: [: an example of retry
    it tries to ping 4 times with a timeout of 2 seconds every time
     ]
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello, world\"",
        Code: 0,
        Output: "hello, world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello, world\"",
        Code: 0,
        Output: "hello, world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com
     WARN: [explicit timeout:] - [500 milli seconds]
    -
    PING goole.com (217.160.0.201): 56 data bytes
    
    -
     WARN: [timeout] - [shell execution timed out]
     .. failed(suppressed if it is not the last step)
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com
     WARN: [explicit timeout:] - [500 milli seconds]
    -
    PING goole.com (217.160.0.201): 56 data bytes
    
    -
     WARN: [timeout] - [shell execution timed out]
     .. failed(suppressed if it is not the last step)
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com
     WARN: [explicit timeout:] - [500 milli seconds]
    -
    PING goole.com (217.160.0.201): 56 data bytes
    
    -
     WARN: [timeout] - [shell execution timed out]
     .. failed(suppressed if it is not the last step)
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com
     WARN: [explicit timeout:] - [500 milli seconds]
    -
    PING goole.com (217.160.0.201): 56 data bytes
    
    -
     WARN: [timeout] - [shell execution timed out]
     .. failed(suppressed if it is not the last step)
     WARN: [ignoreError:] - [Error ignored!!!]
    -Step4: [: an example of retry
    it tries to ping 4 times with a timeout of 2 seconds every time
    with every attemp it puts a delay of 2 seconds
     ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "PING goole.com (217.160.0.201): 56 data bytes",
        ErrMsg: "signal: killed"
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "PING goole.com (217.160.0.201): 56 data bytes",
        ErrMsg: "signal: killed"
      }),
      "up_runtime_task_layer_number": 0
    })
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 1,
      "loopitem": "retry1",
      "up_runtime_task_layer_number": 0,
      "loopindex": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "loopindex": 0,
      "loopindex1": 1,
      "loopitem": "retry1"
    })
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com
     WARN: [explicit timeout:] - [500 milli seconds]
    -
    PING goole.com (217.160.0.201): 56 data bytes
    
    -
     WARN: [timeout] - [shell execution timed out]
     .. failed(suppressed if it is not the last step)
     WARN: [ignoreError:] - [Error ignored!!!]
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "loopitem": "retry1",
      "loopindex": 0,
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "PING goole.com (217.160.0.201): 56 data bytes",
        ErrMsg: "signal: killed"
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "PING goole.com (217.160.0.201): 56 data bytes",
        ErrMsg: "signal: killed"
      }),
      "up_runtime_task_layer_number": 0,
      "loopitem": "retry1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    ~SubStep1: [sleep: delay 2 seconds in each attemp ]
    sleeping 200 milli seconds
    ..
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "loopitem": "retry2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "loopitem": "retry2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com
     WARN: [explicit timeout:] - [500 milli seconds]
    -
    PING goole.com (217.160.0.201): 56 data bytes
    
    -
     WARN: [timeout] - [shell execution timed out]
     .. failed(suppressed if it is not the last step)
     WARN: [ignoreError:] - [Error ignored!!!]
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "PING goole.com (217.160.0.201): 56 data bytes",
        ErrMsg: "signal: killed"
      }),
      "up_runtime_task_layer_number": 0,
      "loopitem": "retry2",
      "loopindex": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "PING goole.com (217.160.0.201): 56 data bytes",
        ErrMsg: "signal: killed"
      }),
      "up_runtime_task_layer_number": 0,
      "loopitem": "retry2",
      "loopindex": 1
    })
    
    ~SubStep1: [sleep: delay 2 seconds in each attemp ]
    sleeping 200 milli seconds
    ..
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "loopitem": "retry3",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "loopitem": "retry3",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com
     WARN: [explicit timeout:] - [500 milli seconds]
    -
    PING goole.com (217.160.0.201): 56 data bytes
    
    -
     WARN: [timeout] - [shell execution timed out]
     .. failed(suppressed if it is not the last step)
     WARN: [ignoreError:] - [Error ignored!!!]
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "PING goole.com (217.160.0.201): 56 data bytes",
        ErrMsg: "signal: killed"
      }),
      "up_runtime_task_layer_number": 0,
      "loopitem": "retry3",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 3,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "PING goole.com (217.160.0.201): 56 data bytes",
        ErrMsg: "signal: killed"
      }),
      "up_runtime_task_layer_number": 0,
      "loopitem": "retry3",
      "loopindex": 2
    })
    
    ~SubStep1: [sleep: delay 2 seconds in each attemp ]
    sleeping 200 milli seconds
    ..
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "loopindex1": 4,
      "loopitem": "retry4",
      "loopindex": 3
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 4,
      "loopitem": "retry4",
      "loopindex": 3,
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com
     WARN: [explicit timeout:] - [500 milli seconds]
    -
    PING goole.com (217.160.0.201): 56 data bytes
    
    -
     WARN: [timeout] - [shell execution timed out]
     .. failed(suppressed if it is not the last step)
     WARN: [ignoreError:] - [Error ignored!!!]
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "PING goole.com (217.160.0.201): 56 data bytes",
        ErrMsg: "signal: killed"
      }),
      "up_runtime_task_layer_number": 0,
      "loopindex": 3,
      "loopindex1": 4,
      "loopitem": "retry4"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "retry4",
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "PING goole.com (217.160.0.201): 56 data bytes",
        ErrMsg: "signal: killed"
      }),
      "up_runtime_task_layer_number": 0,
      "loopindex": 3,
      "loopindex1": 4
    })
    
    ~SubStep1: [sleep: delay 2 seconds in each attemp ]
    sleeping 200 milli seconds
    ..
    -Step5: [: loop with customised range
     ]
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "PING goole.com (217.160.0.201): 56 data bytes",
        ErrMsg: "signal: killed"
      }),
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "PING goole.com (217.160.0.201): 56 data bytes",
        ErrMsg: "signal: killed"
      }),
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com
     WARN: [explicit timeout:] - [500 milli seconds]
    -
    PING goole.com (217.160.0.201): 56 data bytes
    
    -
     WARN: [timeout] - [shell execution timed out]
     .. failed(suppressed if it is not the last step)
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com
     WARN: [explicit timeout:] - [500 milli seconds]
    -
    PING goole.com (217.160.0.201): 56 data bytes
    
    -
     WARN: [timeout] - [shell execution timed out]
     .. failed(suppressed if it is not the last step)
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com
     WARN: [explicit timeout:] - [500 milli seconds]
    -
    PING goole.com (217.160.0.201): 56 data bytes
    
    -
     WARN: [timeout] - [shell execution timed out]
     .. failed(suppressed if it is not the last step)
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com
     WARN: [explicit timeout:] - [500 milli seconds]
    -
    PING goole.com (217.160.0.201): 56 data bytes
    
    -
     WARN: [timeout] - [shell execution timed out]
     .. failed(suppressed if it is not the last step)
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com
     WARN: [explicit timeout:] - [500 milli seconds]
    -
    PING goole.com (217.160.0.201): 56 data bytes
    
    -
     WARN: [timeout] - [shell execution timed out]
     .. failed(suppressed if it is not the last step)
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com
     WARN: [explicit timeout:] - [500 milli seconds]
    -
    PING goole.com (217.160.0.201): 56 data bytes
    
    -
     WARN: [timeout] - [shell execution timed out]
     .. failed(suppressed if it is not the last step)
     WARN: [ignoreError:] - [Error ignored!!!]
    -Step6: [: an example of retry
    it tries to ping 4 times with a timeout of 2 seconds every time
    with every attemp it puts a delay of 2 seconds
    it also uses dynamic loopRange instead of prepared list of value
     ]
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "PING goole.com (217.160.0.201): 56 data bytes",
        ErrMsg: "signal: killed"
      }),
      "myretry": {
        100,
        101,
        102,
        103,
        104,
        105
      },
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "PING goole.com (217.160.0.201): 56 data bytes",
        ErrMsg: "signal: killed"
      }),
      "myretry": {
        100,
        101,
        102,
        103,
        104,
        105
      },
      "up_runtime_task_layer_number": 0
    })
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "myretry": {
        100,
        101,
        102,
        103
      },
      "up_runtime_task_layer_number": 0,
      "loopitem": 100,
      "loopindex": 0,
      "loopindex1": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "loopitem": 100,
      "loopindex": 0,
      "loopindex1": 1,
      "myretry": {
        100,
        101,
        102,
        103
      }
    })
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com
     WARN: [explicit timeout:] - [500 milli seconds]
    -
    PING goole.com (217.160.0.201): 56 data bytes
    
    -
     WARN: [timeout] - [shell execution timed out]
     .. failed(suppressed if it is not the last step)
     WARN: [ignoreError:] - [Error ignored!!!]
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "PING goole.com (217.160.0.201): 56 data bytes",
        ErrMsg: "signal: killed"
      }),
      "myretry": {
        100,
        101,
        102,
        103
      },
      "up_runtime_task_layer_number": 0,
      "loopitem": 100,
      "loopindex": 0,
      "loopindex1": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "PING goole.com (217.160.0.201): 56 data bytes",
        ErrMsg: "signal: killed"
      }),
      "myretry": {
        100,
        101,
        102,
        103
      },
      "up_runtime_task_layer_number": 0,
      "loopitem": 100
    })
    
    ~SubStep1: [sleep: delay 2 seconds in each attemp ]
    sleeping 200 milli seconds
    ..
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 2,
      "myretry": {
        100,
        101,
        102,
        103
      },
      "up_runtime_task_layer_number": 0,
      "loopitem": 101,
      "loopindex": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "myretry": {
        100,
        101,
        102,
        103
      },
      "up_runtime_task_layer_number": 0,
      "loopitem": 101,
      "loopindex": 1,
      "loopindex1": 2
    })
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com
     WARN: [explicit timeout:] - [500 milli seconds]
    -
    PING goole.com (217.160.0.201): 56 data bytes
    
    -
     WARN: [timeout] - [shell execution timed out]
     .. failed(suppressed if it is not the last step)
     WARN: [ignoreError:] - [Error ignored!!!]
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "PING goole.com (217.160.0.201): 56 data bytes",
        ErrMsg: "signal: killed"
      }),
      "myretry": {
        100,
        101,
        102,
        103
      },
      "up_runtime_task_layer_number": 0,
      "loopitem": 101,
      "loopindex": 1,
      "loopindex1": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "myretry": {
        100,
        101,
        102,
        103
      },
      "up_runtime_task_layer_number": 0,
      "loopitem": 101,
      "loopindex": 1,
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "PING goole.com (217.160.0.201): 56 data bytes",
        ErrMsg: "signal: killed"
      })
    })
    
    ~SubStep1: [sleep: delay 2 seconds in each attemp ]
    sleeping 200 milli seconds
    ..
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "myretry": {
        100,
        101,
        102,
        103
      },
      "up_runtime_task_layer_number": 0,
      "loopindex1": 3,
      "loopitem": 102,
      "loopindex": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 2,
      "myretry": {
        100,
        101,
        102,
        103
      },
      "up_runtime_task_layer_number": 0,
      "loopindex1": 3,
      "loopitem": 102
    })
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com
     WARN: [explicit timeout:] - [500 milli seconds]
    -
    PING goole.com (217.160.0.201): 56 data bytes
    
    -
     WARN: [timeout] - [shell execution timed out]
     .. failed(suppressed if it is not the last step)
     WARN: [ignoreError:] - [Error ignored!!!]
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": 102,
      "loopindex": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "PING goole.com (217.160.0.201): 56 data bytes",
        ErrMsg: "signal: killed"
      }),
      "myretry": {
        100,
        101,
        102,
        103
      },
      "up_runtime_task_layer_number": 0,
      "loopindex1": 3
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 3,
      "loopitem": 102,
      "loopindex": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "PING goole.com (217.160.0.201): 56 data bytes",
        ErrMsg: "signal: killed"
      }),
      "myretry": {
        100,
        101,
        102,
        103
      },
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [sleep: delay 2 seconds in each attemp ]
    sleeping 200 milli seconds
    ..
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 4,
      "loopitem": 103,
      "myretry": {
        100,
        101,
        102,
        103
      },
      "up_runtime_task_layer_number": 0,
      "loopindex": 3
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 3,
      "loopindex1": 4,
      "loopitem": 103,
      "myretry": {
        100,
        101,
        102,
        103
      },
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    ping goole.com
    
    cmd=>:
    ping goole.com
     WARN: [explicit timeout:] - [500 milli seconds]
    -
    PING goole.com (217.160.0.201): 56 data bytes
    
    -
     WARN: [timeout] - [shell execution timed out]
     .. failed(suppressed if it is not the last step)
     WARN: [ignoreError:] - [Error ignored!!!]
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": 103,
      "loopindex": 3,
      "loopindex1": 4,
      "myretry": {
        100,
        101,
        102,
        103
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "ping goole.com",
        Code: -1,
        Output: "PING goole.com (217.160.0.201): 56 data bytes",
        ErrMsg: "signal: killed"
      }),
      "up_runtime_task_layer_number": 0
    })
    
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
        Output: "PING goole.com (217.160.0.201): 56 data bytes",
        ErrMsg: "signal: killed"
      }),
      "up_runtime_task_layer_number": 0,
      "loopitem": 103,
      "loopindex": 3,
      "loopindex1": 4
    })
    
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
