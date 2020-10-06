---
title: "0004_vvvvv"
date: 2020-10-07T00:12:02+1010:00
draft: false
weight: 100404

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/modtests/0004/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/modtests/0004
                 WorkDir -> refdir
              AbsWorkDir -> /up_project/up/tests/modtests/0004
                TaskFile -> up.yml
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> Main
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up/tests/modtests/0004
    -exec task: Main
    loading [Task]:  ./up.yml
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001f5100)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc0000b68c8)({
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
    })
    
      located task-> 1 [Main]: 
    Task1: [Main ==> Main: main entry ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: "internal_task",
      Dox: <nil>,
      Func: "call",
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
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    caller's vars to task (internal_task)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
      located task-> 2 [internal_task]: 
    =Task2: [Main ==> internal_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "cmd": "this is a internal task in caller",
          "name": "print"
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
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    this is a internal task in caller
    ~~SubStep1: [print:  ]
    this is a internal task in caller
    --Step2:
    {
      Name: "",
      Do: {
        "ls -lart",
        "ls |grep up",
        "pwd",
        "ls ../..|grep modtests"
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
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    ls -lart
    
    cmd=>:
    ls -lart
    -
    total 12
    -rw-r--r--    1 root     root           253 Jun 11 09:38 upconfig.yml
    -rw-r--r--    1 root     root           521 Jun 11 09:38 up.yml
    drwxr-xr-x    3 root     root            96 Jun 11 09:38 hello-module
    -rw-r--r--    1 root     root          1019 Jun 11 09:38 doc.yml
    drwxr-xr-x    6 root     root           192 Jun 11 09:38 .
    drwxr-xr-x   19 root     root           608 Oct  1 21:59 ..
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=8) "ls -lart",
     Code: (int) 0,
     Output: (string) (len=396) "total 12\n-rw-r--r--    1 root     root           253 Jun 11 09:38 upconfig.yml\n-rw-r--r--    1 root     root           521 Jun 11 09:38 up.yml\ndrwxr-xr-x    3 root     root            96 Jun 11 09:38 hello-module\n-rw-r--r--    1 root     root          1019 Jun 11 09:38 doc.yml\ndrwxr-xr-x    6 root     root           192 Jun 11 09:38 .\ndrwxr-xr-x   19 root     root           608 Oct  1 21:59 ..",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    ls |grep up
    
    cmd=>:
    ls |grep up
    -
    up.yml
    upconfig.yml
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=11) "ls |grep up",
     Code: (int) 0,
     Output: (string) (len=19) "up.yml\nupconfig.yml",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    pwd
    
    cmd=>:
    pwd
    -
    /up_project/up/tests/modtests/0004
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=3) "pwd",
     Code: (int) 0,
     Output: (string) (len=34) "/up_project/up/tests/modtests/0004",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    ls ../..|grep modtests
    
    cmd=>:
    ls ../..|grep modtests
    -
    modtests
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=22) "ls ../..|grep modtests",
     Code: (int) 0,
     Output: (string) (len=8) "modtests",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2:
    {
      Name: "",
      Do: "hello-module.Say_world",
      Dox: <nil>,
      Func: "call",
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
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    caller's vars to task (hello-module.Say_world)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
     WARN: [config file does not exist] - [use builtin defaults]
    loading [Task]:  ./up.yml
    module: [hello-module], instance id: [nonamed], exec profile: []
     WARN: [*be aware*] - [both instance id and exec profile are not set]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc000277f00)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ nonamed ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc0000b6cc0)({
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
    })
    
    =>call module: [hello-module] task: [Say_world]
    Executing tasker layer: 2
    
      located task-> 1 [Say_world]: 
    Task1: [TODO: Main Caller Taskname ==> Say_world:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "ls -lart",
        "ls |grep up",
        "pwd",
        "ls ../../..|grep modtests"
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
      "up_runtime_tasker_layer_number": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 0
    }
    
    
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 2
    })
    
    cmd( 1):
    ls -lart
    
    cmd=>:
    ls -lart
    -
    total 4
    -rw-r--r--    1 root     root           796 Jun 11 09:38 up.yml
    drwxr-xr-x    6 root     root           192 Jun 11 09:38 ..
    drwxr-xr-x    3 root     root            96 Jun 11 09:38 .
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=8) "ls -lart",
     Code: (int) 0,
     Output: (string) (len=190) "total 4\n-rw-r--r--    1 root     root           796 Jun 11 09:38 up.yml\ndrwxr-xr-x    6 root     root           192 Jun 11 09:38 ..\ndrwxr-xr-x    3 root     root            96 Jun 11 09:38 .",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    ls |grep up
    
    cmd=>:
    ls |grep up
    -
    up.yml
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=11) "ls |grep up",
     Code: (int) 0,
     Output: (string) (len=6) "up.yml",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    pwd
    
    cmd=>:
    pwd
    -
    /up_project/up/tests/modtests/0004/hello-module
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=3) "pwd",
     Code: (int) 0,
     Output: (string) (len=47) "/up_project/up/tests/modtests/0004/hello-module",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    ls ../../..|grep modtests
    
    cmd=>:
    ls ../../..|grep modtests
    -
    modtests
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=25) "ls ../../..|grep modtests",
     Code: (int) 0,
     Output: (string) (len=8) "modtests",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2: [
    this should call its own internal task
    ]
    {
      Name: "",
      Do: "internal_task",
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "this should call its own internal task\n",
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
      "last_result": (*utils.ExecResult)({
        Cmd: "ls ../../..|grep modtests",
        Code: 0,
        Output: "modtests",
        ErrMsg: ""
      }),
      "up_runtime_tasker_layer_number": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "ls ../../..|grep modtests",
        Code: 0,
        Output: "modtests",
        ErrMsg: ""
      })
    }
    
    
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ls ../../..|grep modtests",
        Code: 0,
        Output: "modtests",
        ErrMsg: ""
      }),
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 0
    })
    
    caller's vars to task (internal_task)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "ls ../../..|grep modtests",
        Code: 0,
        Output: "modtests",
        ErrMsg: ""
      }),
      "up_runtime_tasker_layer_number": 2
    })
    
      located task-> 3 [internal_task]: 
    =Task3: [TODO: Main Caller Taskname/Say_world ==> internal_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "this is a internal task in module"
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
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "ls ../../..|grep modtests",
        Code: 0,
        Output: "modtests",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "ls ../../..|grep modtests",
        Code: 0,
        Output: "modtests",
        ErrMsg: ""
      }),
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1
    }
    
    
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ls ../../..|grep modtests",
        Code: 0,
        Output: "modtests",
        ErrMsg: ""
      }),
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1
    })
    
    this is a internal task in module
    ~~SubStep1: [print:  ]
    this is a internal task in module
    --Step2:
    {
      Name: "",
      Do: {
        "ls -lart",
        "ls |grep up",
        "pwd",
        "ls ../../..|grep modtests"
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
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "ls ../../..|grep modtests",
        Code: 0,
        Output: "modtests",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "ls ../../..|grep modtests",
        Code: 0,
        Output: "modtests",
        ErrMsg: ""
      }),
      "up_runtime_tasker_layer_number": 2
    }
    
    
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "ls ../../..|grep modtests",
        Code: 0,
        Output: "modtests",
        ErrMsg: ""
      }),
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    ls -lart
    
    cmd=>:
    ls -lart
    -
    total 4
    -rw-r--r--    1 root     root           796 Jun 11 09:38 up.yml
    drwxr-xr-x    6 root     root           192 Jun 11 09:38 ..
    drwxr-xr-x    3 root     root            96 Jun 11 09:38 .
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=8) "ls -lart",
     Code: (int) 0,
     Output: (string) (len=190) "total 4\n-rw-r--r--    1 root     root           796 Jun 11 09:38 up.yml\ndrwxr-xr-x    6 root     root           192 Jun 11 09:38 ..\ndrwxr-xr-x    3 root     root            96 Jun 11 09:38 .",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    ls |grep up
    
    cmd=>:
    ls |grep up
    -
    up.yml
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=11) "ls |grep up",
     Code: (int) 0,
     Output: (string) (len=6) "up.yml",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    pwd
    
    cmd=>:
    pwd
    -
    /up_project/up/tests/modtests/0004/hello-module
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=3) "pwd",
     Code: (int) 0,
     Output: (string) (len=47) "/up_project/up/tests/modtests/0004/hello-module",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    ls ../../..|grep modtests
    
    cmd=>:
    ls ../../..|grep modtests
    -
    modtests
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=25) "ls ../../..|grep modtests",
     Code: (int) 0,
     Output: (string) (len=8) "modtests",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step3:
    {
      Name: "",
      Do: "internal_task",
      Dox: <nil>,
      Func: "call",
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
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2
    })
    
    caller's vars to task (internal_task)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2
    })
    
      located task-> 2 [internal_task]: 
    =Task2: [Main ==> internal_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "this is a internal task in caller"
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
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2
    })
    
    this is a internal task in caller
    ~~SubStep1: [print:  ]
    this is a internal task in caller
    --Step2:
    {
      Name: "",
      Do: {
        "ls -lart",
        "ls |grep up",
        "pwd",
        "ls ../..|grep modtests"
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
      "up_runtime_tasker_layer_number": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2
    })
    
    cmd( 1):
    ls -lart
    
    cmd=>:
    ls -lart
    -
    total 12
    -rw-r--r--    1 root     root           253 Jun 11 09:38 upconfig.yml
    -rw-r--r--    1 root     root           521 Jun 11 09:38 up.yml
    drwxr-xr-x    3 root     root            96 Jun 11 09:38 hello-module
    -rw-r--r--    1 root     root          1019 Jun 11 09:38 doc.yml
    drwxr-xr-x    6 root     root           192 Jun 11 09:38 .
    drwxr-xr-x   19 root     root           608 Oct  1 21:59 ..
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=8) "ls -lart",
     Code: (int) 0,
     Output: (string) (len=396) "total 12\n-rw-r--r--    1 root     root           253 Jun 11 09:38 upconfig.yml\n-rw-r--r--    1 root     root           521 Jun 11 09:38 up.yml\ndrwxr-xr-x    3 root     root            96 Jun 11 09:38 hello-module\n-rw-r--r--    1 root     root          1019 Jun 11 09:38 doc.yml\ndrwxr-xr-x    6 root     root           192 Jun 11 09:38 .\ndrwxr-xr-x   19 root     root           608 Oct  1 21:59 ..",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    ls |grep up
    
    cmd=>:
    ls |grep up
    -
    up.yml
    upconfig.yml
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=11) "ls |grep up",
     Code: (int) 0,
     Output: (string) (len=19) "up.yml\nupconfig.yml",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    pwd
    
    cmd=>:
    pwd
    -
    /up_project/up/tests/modtests/0004
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=3) "pwd",
     Code: (int) 0,
     Output: (string) (len=34) "/up_project/up/tests/modtests/0004",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    ls ../..|grep modtests
    
    cmd=>:
    ls ../..|grep modtests
    -
    modtests
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=22) "ls ../..|grep modtests",
     Code: (int) 0,
     Output: (string) (len=8) "modtests",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [m0004 log - verbose level v](../../logs/m0004_v)
* [m0004 log - verbose level vv](../../logs/m0004_vv)
* [m0004 log - verbose level vvv](../../logs/m0004_vvv)
* [m0004 log - verbose level vvvv](../../logs/m0004_vvvv)
* [m0004 log - verbose level vvvvv](../../logs/m0004_vvvvv)

##### References
* [Related Chapter](../../module/0004)
