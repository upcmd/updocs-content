---
title: "c0026_vvvv"
date: 2020-07-01T15:34:24+77:00
draft: false
weight: 10263

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
                 Verbose -> vvvv
              ModuleName -> fervent_tesla1
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0026
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [fervent_tesla1] instance id: [dev]
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
    })
    
    fervent_tesla1: overall final exec vars:
    
    (*core.Cache)({
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    fervent_tesla1: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    curl -s -X GET "https://httpbin.org/get" -H "accept: application/json"
    
     \_ curl -s -X GET "https://httpbin.org/get" -H "accept: application/json"
    {
      "args": {}, 
      "headers": {
        "Accept": "application/json", 
        "Host": "httpbin.org", 
        "User-Agent": "curl/7.70.0", 
        "X-Amzn-Trace-Id": "Root=1-5ef62af9-25e72c31aff1a7cae4355d05"
      }, 
      "origin": "118.211.191.165", 
      "url": "https://httpbin.org/get"
    }
     .. ok
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "test1_0_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62af9-25e72c31aff1a7cae4355d05\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62af9-25e72c31aff1a7cae4355d05\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    fervent_tesla1: overall final exec vars:
    
    (*core.Cache)({
      "test1_0_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62af9-25e72c31aff1a7cae4355d05\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62af9-25e72c31aff1a7cae4355d05\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    0
    ~~SubStep2: [print:  ]
    {
      "args": {}, 
      "headers": {
        "Accept": "application/json", 
        "Host": "httpbin.org", 
        "User-Agent": "curl/7.70.0", 
        "X-Amzn-Trace-Id": "Root=1-5ef62af9-25e72c31aff1a7cae4355d05"
      }, 
      "origin": "118.211.191.165", 
      "url": "https://httpbin.org/get"
    }
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "test1_0_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62af9-25e72c31aff1a7cae4355d05\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62af9-25e72c31aff1a7cae4355d05\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    fervent_tesla1: overall final exec vars:
    
    (*core.Cache)({
      "test1_0_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62af9-25e72c31aff1a7cae4355d05\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62af9-25e72c31aff1a7cae4355d05\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    curl -s -X GET "https://httpbin.org/get" -H "accept: application/json"
    
     \_ curl -s -X GET "https://httpbin.org/get" -H "accept: application/json"
    {
      "args": {}, 
      "headers": {
        "Accept": "application/json", 
        "Host": "httpbin.org", 
        "User-Agent": "curl/7.70.0", 
        "X-Amzn-Trace-Id": "Root=1-5ef62afa-dd2686b8988eec20f4aed5e0"
      }, 
      "origin": "118.211.191.165", 
      "url": "https://httpbin.org/get"
    }
     .. ok
    . ok
    --Step2:
    {
      Name: "",
      Do: {
        {
          "cmd": "{{.test2_httpbinget_result.Code}}",
          "name": "print"
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "test1_0_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62af9-25e72c31aff1a7cae4355d05\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62afa-dd2686b8988eec20f4aed5e0\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "test2_httpbinget_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62afa-dd2686b8988eec20f4aed5e0\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    fervent_tesla1: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62afa-dd2686b8988eec20f4aed5e0\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "test2_httpbinget_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62afa-dd2686b8988eec20f4aed5e0\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "test1_0_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62af9-25e72c31aff1a7cae4355d05\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      })
    })
    
    ~~SubStep1: [print:  ]
    0
    ~~SubStep2: [print:  ]
    {
      "args": {}, 
      "headers": {
        "Accept": "application/json", 
        "Host": "httpbin.org", 
        "User-Agent": "curl/7.70.0", 
        "X-Amzn-Trace-Id": "Root=1-5ef62afa-dd2686b8988eec20f4aed5e0"
      }, 
      "origin": "118.211.191.165", 
      "url": "https://httpbin.org/get"
    }
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62afa-dd2686b8988eec20f4aed5e0\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "test2_httpbinget_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62afa-dd2686b8988eec20f4aed5e0\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "test1_0_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62af9-25e72c31aff1a7cae4355d05\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      })
    })
    
    fervent_tesla1: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "test2_httpbinget_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62afa-dd2686b8988eec20f4aed5e0\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "test1_0_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62af9-25e72c31aff1a7cae4355d05\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62afa-dd2686b8988eec20f4aed5e0\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    curl -s -X GET "https://httpbin.org/get" -H "accept: application/json"
    
     \_ curl -s -X GET "https://httpbin.org/get" -H "accept: application/json"
    {
      "args": {}, 
      "headers": {
        "Accept": "application/json", 
        "Host": "httpbin.org", 
        "User-Agent": "curl/7.70.0", 
        "X-Amzn-Trace-Id": "Root=1-5ef62afb-ca7c72904a7a94b8bfab1b5b"
      }, 
      "origin": "118.211.191.165", 
      "url": "https://httpbin.org/get"
    }
     .. ok
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
          "cmd": "{{.httpbin_get_result.Output}}",
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "test2_httpbinget_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62afa-dd2686b8988eec20f4aed5e0\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "httpbin_get_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62afb-ca7c72904a7a94b8bfab1b5b\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "test1_0_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62af9-25e72c31aff1a7cae4355d05\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62afb-ca7c72904a7a94b8bfab1b5b\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    fervent_tesla1: overall final exec vars:
    
    (*core.Cache)({
      "test2_httpbinget_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62afa-dd2686b8988eec20f4aed5e0\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "httpbin_get_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62afb-ca7c72904a7a94b8bfab1b5b\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "test1_0_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62af9-25e72c31aff1a7cae4355d05\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62afb-ca7c72904a7a94b8bfab1b5b\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    0
    ~~SubStep2: [print:  ]
    {
      "args": {}, 
      "headers": {
        "Accept": "application/json", 
        "Host": "httpbin.org", 
        "User-Agent": "curl/7.70.0", 
        "X-Amzn-Trace-Id": "Root=1-5ef62afb-ca7c72904a7a94b8bfab1b5b"
      }, 
      "origin": "118.211.191.165", 
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
