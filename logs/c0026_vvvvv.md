---
title: "c0026_vvvvv"
date: 2020-09-18T01:27:24+99:00
draft: false
weight: 10264

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0026
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0026
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc000175700)(<nil>)
    
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
        "test1",
        "test2",
        "test3"
      },
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
    
    caller's vars to task (test1)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
      located task-> 2 [test1]: 
    =Task2: [task ==> test1: test reg with an auto registered name
    in this case the step name is empty, then the idx will be used
     ]
    Executing task stack layer: 2
    
    --Step1: [: if this step does not have a name, then the auto reg name would be task_0_reslt ]
    {
      Name: "",
      Do: {
        "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "if this step does not have a name, then the auto reg name would be task_0_reslt",
      Reg: "auto",
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
    curl -s -X GET "https://httpbin.org/get" -H "accept: application/json"
    
    cmd=>:
    curl -s -X GET "https://httpbin.org/get" -H "accept: application/json"
    -
    {
      "args": {}, 
      "headers": {
        "Accept": "application/json", 
        "Host": "httpbin.org", 
        "User-Agent": "curl/7.70.0", 
        "X-Amzn-Trace-Id": "Root=1-5f6376f1-7cf65d565e981f00ef83af45"
      }, 
      "origin": "118.211.72.135", 
      "url": "https://httpbin.org/get"
    }
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=70) "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
     Code: (int) 0,
     Output: (string) (len=268) "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f1-7cf65d565e981f00ef83af45\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
     ErrMsg: (string) ""
    }
    
    . ok
    --Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.test1_0_result.Code}}"
        },
        {
          "name": "print",
          "cmd": "{{.test1_0_result.Output}}"
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
      "test1_0_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f1-7cf65d565e981f00ef83af45\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f1-7cf65d565e981f00ef83af45\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "test1_0_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f1-7cf65d565e981f00ef83af45\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f1-7cf65d565e981f00ef83af45\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "test1_0_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f1-7cf65d565e981f00ef83af45\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f1-7cf65d565e981f00ef83af45\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      })
    })
    
    {{.test1_0_result.Code}}
    ~~SubStep1: [print:  ]
    0
    {{.test1_0_result.Output}}
    ~~SubStep2: [print:  ]
    {
      "args": {}, 
      "headers": {
        "Accept": "application/json", 
        "Host": "httpbin.org", 
        "User-Agent": "curl/7.70.0", 
        "X-Amzn-Trace-Id": "Root=1-5f6376f1-7cf65d565e981f00ef83af45"
      }, 
      "origin": "118.211.72.135", 
      "url": "https://httpbin.org/get"
    }
    caller's vars to task (test2)::
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f1-7cf65d565e981f00ef83af45\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "test1_0_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f1-7cf65d565e981f00ef83af45\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      })
    })
    
      located task-> 3 [test2]: 
    =Task3: [task ==> test2: test reg with a auto registered name and the step name is not empty
    in this case the registered reslt name is: test2_httpbinget_result
     ]
    Executing task stack layer: 2
    
    --Step1: [httpbinget: if this step does not have a name, then the auto reg name would be task_0_reslt ]
    {
      Name: "httpbinget",
      Do: {
        "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "if this step does not have a name, then the auto reg name would be task_0_reslt",
      Reg: "auto",
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
      "test1_0_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f1-7cf65d565e981f00ef83af45\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f1-7cf65d565e981f00ef83af45\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "test1_0_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f1-7cf65d565e981f00ef83af45\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f1-7cf65d565e981f00ef83af45\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "test1_0_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f1-7cf65d565e981f00ef83af45\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f1-7cf65d565e981f00ef83af45\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    curl -s -X GET "https://httpbin.org/get" -H "accept: application/json"
    
    cmd=>:
    curl -s -X GET "https://httpbin.org/get" -H "accept: application/json"
    -
    {
      "args": {}, 
      "headers": {
        "Accept": "application/json", 
        "Host": "httpbin.org", 
        "User-Agent": "curl/7.70.0", 
        "X-Amzn-Trace-Id": "Root=1-5f6376f3-4b78bf0a81331ffca6664417"
      }, 
      "origin": "118.211.72.135", 
      "url": "https://httpbin.org/get"
    }
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=70) "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
     Code: (int) 0,
     Output: (string) (len=268) "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f3-4b78bf0a81331ffca6664417\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
     ErrMsg: (string) ""
    }
    
    . ok
    --Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.test2_httpbinget_result.Code}}"
        },
        {
          "name": "print",
          "cmd": "{{.test2_httpbinget_result.Output}}"
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
      "test1_0_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f1-7cf65d565e981f00ef83af45\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f3-4b78bf0a81331ffca6664417\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "test2_httpbinget_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f3-4b78bf0a81331ffca6664417\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "test1_0_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f1-7cf65d565e981f00ef83af45\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f3-4b78bf0a81331ffca6664417\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "test2_httpbinget_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f3-4b78bf0a81331ffca6664417\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "test1_0_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f1-7cf65d565e981f00ef83af45\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f3-4b78bf0a81331ffca6664417\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "test2_httpbinget_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f3-4b78bf0a81331ffca6664417\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      })
    })
    
    {{.test2_httpbinget_result.Code}}
    ~~SubStep1: [print:  ]
    0
    {{.test2_httpbinget_result.Output}}
    ~~SubStep2: [print:  ]
    {
      "args": {}, 
      "headers": {
        "Accept": "application/json", 
        "Host": "httpbin.org", 
        "User-Agent": "curl/7.70.0", 
        "X-Amzn-Trace-Id": "Root=1-5f6376f3-4b78bf0a81331ffca6664417"
      }, 
      "origin": "118.211.72.135", 
      "url": "https://httpbin.org/get"
    }
    caller's vars to task (test3)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "test1_0_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f1-7cf65d565e981f00ef83af45\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f3-4b78bf0a81331ffca6664417\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "test2_httpbinget_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f3-4b78bf0a81331ffca6664417\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      })
    })
    
      located task-> 4 [test3]: 
    =Task4: [task ==> test3: test reg with a registered name
    in this case the registered reslt name is: test2_httpbinget_result
     ]
    Executing task stack layer: 2
    
    --Step1: [httpbinget: it will use the given name as var name to register the result ]
    {
      Name: "httpbinget",
      Do: {
        "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "it will use the given name as var name to register the result",
      Reg: "httpbin_get_result",
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
      "test2_httpbinget_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f3-4b78bf0a81331ffca6664417\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "test1_0_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f1-7cf65d565e981f00ef83af45\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f3-4b78bf0a81331ffca6664417\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "test1_0_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f1-7cf65d565e981f00ef83af45\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f3-4b78bf0a81331ffca6664417\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "test2_httpbinget_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f3-4b78bf0a81331ffca6664417\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "test2_httpbinget_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f3-4b78bf0a81331ffca6664417\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "test1_0_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f1-7cf65d565e981f00ef83af45\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f3-4b78bf0a81331ffca6664417\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    curl -s -X GET "https://httpbin.org/get" -H "accept: application/json"
    
    cmd=>:
    curl -s -X GET "https://httpbin.org/get" -H "accept: application/json"
    -
    {
      "args": {}, 
      "headers": {
        "Accept": "application/json", 
        "Host": "httpbin.org", 
        "User-Agent": "curl/7.70.0", 
        "X-Amzn-Trace-Id": "Root=1-5f6376f4-a3c2cf90f97d19f000848a70"
      }, 
      "origin": "118.211.72.135", 
      "url": "https://httpbin.org/get"
    }
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=70) "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
     Code: (int) 0,
     Output: (string) (len=268) "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f4-a3c2cf90f97d19f000848a70\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
     ErrMsg: (string) ""
    }
    
    . ok
    --Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.httpbin_get_result.Code}}"
        },
        {
          "name": "print",
          "cmd": "{{.httpbin_get_result.Output}}"
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
      "up_runtime_task_layer_number": 1,
      "test1_0_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f1-7cf65d565e981f00ef83af45\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f4-a3c2cf90f97d19f000848a70\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "test2_httpbinget_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f3-4b78bf0a81331ffca6664417\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "httpbin_get_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f4-a3c2cf90f97d19f000848a70\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f4-a3c2cf90f97d19f000848a70\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "test2_httpbinget_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f3-4b78bf0a81331ffca6664417\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "httpbin_get_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f4-a3c2cf90f97d19f000848a70\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "test1_0_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f1-7cf65d565e981f00ef83af45\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "test1_0_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f1-7cf65d565e981f00ef83af45\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f4-a3c2cf90f97d19f000848a70\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "test2_httpbinget_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f3-4b78bf0a81331ffca6664417\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "httpbin_get_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f4-a3c2cf90f97d19f000848a70\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    {{.httpbin_get_result.Code}}
    ~~SubStep1: [print:  ]
    0
    {{.httpbin_get_result.Output}}
    ~~SubStep2: [print:  ]
    {
      "args": {}, 
      "headers": {
        "Accept": "application/json", 
        "Host": "httpbin.org", 
        "User-Agent": "curl/7.70.0", 
        "X-Amzn-Trace-Id": "Root=1-5f6376f4-a3c2cf90f97d19f000848a70"
      }, 
      "origin": "118.211.72.135", 
      "url": "https://httpbin.org/get"
    }
    
```

##### Logs with different verbose level
* [c0026 log - verbose level v](../../logs/c0026_v)
* [c0026 log - verbose level vv](../../logs/c0026_vv)
* [c0026 log - verbose level vvv](../../logs/c0026_vvv)
* [c0026 log - verbose level vvvv](../../logs/c0026_vvvv)
* [c0026 log - verbose level vvvvv](../../logs/c0026_vvvvv)

##### References
* [Related Chapter](../../shell-func/c0026)
