---
title: "c0141_vvvvv"
date: 2020-09-18T01:27:47+99:00
draft: false
weight: 11414

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0141
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
    loading [Task]:  ./tests/functests/c0141
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ed360)(<nil>)
    
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
    Task1: [task ==> task: test reg with a registered name
    in this case the registered reslt name is: test2_httpbinget_result
     ]
    Executing task stack layer: 1
    
    -Step1: [httpbinget: it will use the given name as var name to register the result ]
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
        "X-Amzn-Trace-Id": "Root=1-5f637736-a5d36d28057ce354f670723c"
      }, 
      "origin": "118.211.72.135", 
      "url": "https://httpbin.org/get"
    }
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=70) "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
     Code: (int) 0,
     Output: (string) (len=268) "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f637736-a5d36d28057ce354f670723c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2:
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
        },
        {
          "name": "print",
          "cmd": "{{.api_response}}"
        },
        {
          "name": "inspect",
          "cmd": {
            "exec_vars",
            "debug_vars"
          }
        },
        {
          "name": "print",
          "cmd": "{{.api_response_object.headers.Host}}"
        },
        {
          "name": "printObj",
          "cmd": "api_response_headers"
        },
        {
          "name": "print",
          "desc": "you can not use this header directly, if you intend to use a sub node, then you should use query and register a sub node\n",
          "cmd": "{{.api_response_headers}}"
        },
        {
          "name": "print",
          "cmd": "{{.api_response_headers_host}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "api_response",
          Value: "{{.httpbin_get_result.Output}}",
          Desc: "",
          Expand: 0,
          Flags: {
            "toObj",
            "v"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        },
        {
          Name: "api_response_headers",
          Value: "{{.api_response_object.headers}}",
          Desc: "test if I can get immediately access of converted object",
          Expand: 0,
          Flags: {
            "v"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        },
        {
          Name: "api_response_headers_host",
          Value: "{{.api_response_object.headers.Host}}",
          Desc: "",
          Expand: 0,
          Flags: {
            "v"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
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
      "httpbin_get_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f637736-a5d36d28057ce354f670723c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f637736-a5d36d28057ce354f670723c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    dvar> api_response:
    "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f637736-a5d36d28057ce354f670723c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}"
    
    -
    {
      "args": {}, 
      "headers": {
        "Accept": "application/json", 
        "Host": "httpbin.org", 
        "User-Agent": "curl/7.70.0", 
        "X-Amzn-Trace-Id": "Root=1-5f637736-a5d36d28057ce354f670723c"
      }, 
      "origin": "118.211.72.135", 
      "url": "https://httpbin.org/get"
    }
    dvar[object]> api_response_object:
    {
      "args": {
      },
      "headers": {
        "Accept": "application/json",
        "Host": "httpbin.org",
        "User-Agent": "curl/7.70.0",
        "X-Amzn-Trace-Id": "Root=1-5f637736-a5d36d28057ce354f670723c"
      },
      "origin": "118.211.72.135",
      "url": "https://httpbin.org/get"
    }
    
    dvar> api_response_headers:
    "map[Accept:application/json Host:httpbin.org User-Agent:curl/7.70.0 X-Amzn-Trace-Id:Root=1-5f637736-a5d36d28057ce354f670723c]"
    
    -
    map[Accept:application/json Host:httpbin.org User-Agent:curl/7.70.0 X-Amzn-Trace-Id:Root=1-5f637736-a5d36d28057ce354f670723c]
    dvar> api_response_headers_host:
    "httpbin.org"
    
    -
    httpbin.org
    [local] dvar expanded result:
    {
      "api_response_headers_host": "httpbin.org",
      "api_response": "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f637736-a5d36d28057ce354f670723c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
      "api_response_object": {
        "headers": {
          "Accept": "application/json",
          "Host": "httpbin.org",
          "User-Agent": "curl/7.70.0",
          "X-Amzn-Trace-Id": "Root=1-5f637736-a5d36d28057ce354f670723c"
        },
        "origin": "118.211.72.135",
        "url": "https://httpbin.org/get",
        "args": {
        }
      },
      "api_response_headers": "map[Accept:application/json Host:httpbin.org User-Agent:curl/7.70.0 X-Amzn-Trace-Id:Root=1-5f637736-a5d36d28057ce354f670723c]"
    }
    
    
    scope[local] merged: {
      "api_response_headers_host": "httpbin.org",
      "up_runtime_task_layer_number": 0,
      "httpbin_get_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f637736-a5d36d28057ce354f670723c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f637736-a5d36d28057ce354f670723c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "api_response": "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f637736-a5d36d28057ce354f670723c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
      "api_response_object": {
        "origin": "118.211.72.135",
        "url": "https://httpbin.org/get",
        "args": {
        },
        "headers": {
          "Accept": "application/json",
          "Host": "httpbin.org",
          "User-Agent": "curl/7.70.0",
          "X-Amzn-Trace-Id": "Root=1-5f637736-a5d36d28057ce354f670723c"
        }
      },
      "api_response_headers": "map[Accept:application/json Host:httpbin.org User-Agent:curl/7.70.0 X-Amzn-Trace-Id:Root=1-5f637736-a5d36d28057ce354f670723c]"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "httpbin_get_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f637736-a5d36d28057ce354f670723c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f637736-a5d36d28057ce354f670723c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "api_response_headers": "map[Accept:application/json Host:httpbin.org User-Agent:curl/7.70.0 X-Amzn-Trace-Id:Root=1-5f637736-a5d36d28057ce354f670723c]",
      "api_response_headers_host": "httpbin.org",
      "api_response": "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f637736-a5d36d28057ce354f670723c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
      "api_response_object": {
        "origin": "118.211.72.135",
        "url": "https://httpbin.org/get",
        "args": {
        },
        "headers": {
          "Accept": "application/json",
          "Host": "httpbin.org",
          "User-Agent": "curl/7.70.0",
          "X-Amzn-Trace-Id": "Root=1-5f637736-a5d36d28057ce354f670723c"
        }
      }
    })
    
    {{.httpbin_get_result.Code}}
    ~SubStep1: [print:  ]
    0
    {{.httpbin_get_result.Output}}
    ~SubStep2: [print:  ]
    {
      "args": {}, 
      "headers": {
        "Accept": "application/json", 
        "Host": "httpbin.org", 
        "User-Agent": "curl/7.70.0", 
        "X-Amzn-Trace-Id": "Root=1-5f637736-a5d36d28057ce354f670723c"
      }, 
      "origin": "118.211.72.135", 
      "url": "https://httpbin.org/get"
    }
    {{.api_response}}
    ~SubStep3: [print:  ]
    {
      "args": {}, 
      "headers": {
        "Accept": "application/json", 
        "Host": "httpbin.org", 
        "User-Agent": "curl/7.70.0", 
        "X-Amzn-Trace-Id": "Root=1-5f637736-a5d36d28057ce354f670723c"
      }, 
      "origin": "118.211.72.135", 
      "url": "https://httpbin.org/get"
    }
    [exec_vars debug_vars]
    ~SubStep4: [inspect:  ]
     1: inspect[exec_vars]
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "api_response_headers": "map[Accept:application/json Host:httpbin.org User-Agent:curl/7.70.0 X-Amzn-Trace-Id:Root=1-5f637736-a5d36d28057ce354f670723c]",
      "api_response_headers_host": "httpbin.org",
      "api_response": "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f637736-a5d36d28057ce354f670723c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
      "api_response_object": {
        "args": {
        },
        "headers": {
          "Accept": "application/json",
          "Host": "httpbin.org",
          "User-Agent": "curl/7.70.0",
          "X-Amzn-Trace-Id": "Root=1-5f637736-a5d36d28057ce354f670723c"
        },
        "origin": "118.211.72.135",
        "url": "https://httpbin.org/get"
      },
      "httpbin_get_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f637736-a5d36d28057ce354f670723c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f637736-a5d36d28057ce354f670723c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      })
    })
    
     2: inspect[debug_vars]
    -debug vars-
    "UpRunTimeVars"
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    "RuntimeVarsAndDvarsMerged"
    (*core.Cache)({
      "httpbin_get_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f637736-a5d36d28057ce354f670723c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f637736-a5d36d28057ce354f670723c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      })
    })
    
    "ExecbaseVars"
    (*core.Cache)({
      "httpbin_get_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f637736-a5d36d28057ce354f670723c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f637736-a5d36d28057ce354f670723c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      })
    })
    
    "TaskVars"
    (*core.Cache)({
    })
    
    "ExecContextVars"
    (*core.Cache)({
      "httpbin_get_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f637736-a5d36d28057ce354f670723c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f637736-a5d36d28057ce354f670723c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "api_response_headers": "map[Accept:application/json Host:httpbin.org User-Agent:curl/7.70.0 X-Amzn-Trace-Id:Root=1-5f637736-a5d36d28057ce354f670723c]",
      "api_response_headers_host": "httpbin.org",
      "api_response": "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f637736-a5d36d28057ce354f670723c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
      "api_response_object": {
        "args": {
        },
        "headers": {
          "Accept": "application/json",
          "Host": "httpbin.org",
          "User-Agent": "curl/7.70.0",
          "X-Amzn-Trace-Id": "Root=1-5f637736-a5d36d28057ce354f670723c"
        },
        "origin": "118.211.72.135",
        "url": "https://httpbin.org/get"
      }
    })
    
    --
    {{.api_response_object.headers.Host}}
    ~SubStep5: [print:  ]
    httpbin.org
    api_response_headers
    ~SubStep6: [printObj:  ]
    (string) (len=20) "api_response_headers"
    
    object:
     api_response_headers: "map[Accept:application/json Host:httpbin.org User-Agent:curl/7.70.0 X-Amzn-Trace-Id:Root=1-5f637736-a5d36d28057ce354f670723c]"
    
    {{.api_response_headers}}
    ~SubStep7: [print: you can not use this header directly, if you intend to use a sub node, then you should use query and register a sub node
     ]
    map[Accept:application/json Host:httpbin.org User-Agent:curl/7.70.0 X-Amzn-Trace-Id:Root=1-5f637736-a5d36d28057ce354f670723c]
    {{.api_response_headers_host}}
    ~SubStep8: [print:  ]
    httpbin.org
    
```

##### Logs with different verbose level
* [c0141 log - verbose level v](../../logs/c0141_v)
* [c0141 log - verbose level vv](../../logs/c0141_vv)
* [c0141 log - verbose level vvv](../../logs/c0141_vvv)
* [c0141 log - verbose level vvvv](../../logs/c0141_vvvv)
* [c0141 log - verbose level vvvvv](../../logs/c0141_vvvvv)

##### References
* [Related Chapter](../../object-oriented/c0141)
