---
title: "c0141_vvvv"
date: 2020-07-01T15:34:41+77:00
draft: false
weight: 11413

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
                 Verbose -> vvvv
              ModuleName -> reverent_wright0
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0141
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [reverent_wright0] instance id: [dev]
    merged[ dev ] runtime vars:
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
    })
    
    reverent_wright0: overall final exec vars:
    
    (*core.Cache)({
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
        "X-Amzn-Trace-Id": "Root=1-5ef62b6b-ae2bb960bd1b10720f6e6560"
      }, 
      "origin": "118.211.191.165", 
      "url": "https://httpbin.org/get"
    }
     .. ok
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
            "exec_vars"
          }
        },
        {
          "name": "print",
          "cmd": "{{.api_response_object.headers.Host}}"
        },
        {
          "name": "printobj",
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
            "to_object",
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "httpbin_get_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62b6b-ae2bb960bd1b10720f6e6560\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62b6b-ae2bb960bd1b10720f6e6560\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      })
    })
    
    dvar> api_response:
    "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62b6b-ae2bb960bd1b10720f6e6560\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}"
    
    dvar> api_response_object:
    {
      "args": {
      },
      "headers": {
        "Accept": "application/json",
        "Host": "httpbin.org",
        "User-Agent": "curl/7.70.0",
        "X-Amzn-Trace-Id": "Root=1-5ef62b6b-ae2bb960bd1b10720f6e6560"
      },
      "origin": "118.211.191.165",
      "url": "https://httpbin.org/get"
    }
    
    dvar> api_response_headers:
    "map[Accept:application/json Host:httpbin.org User-Agent:curl/7.70.0 X-Amzn-Trace-Id:Root=1-5ef62b6b-ae2bb960bd1b10720f6e6560]"
    
    dvar> api_response_headers_host:
    "httpbin.org"
    
    reverent_wright0: overall final exec vars:
    
    (*core.Cache)({
      "httpbin_get_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62b6b-ae2bb960bd1b10720f6e6560\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62b6b-ae2bb960bd1b10720f6e6560\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "api_response_object": {
        "headers": {
          "Accept": "application/json",
          "Host": "httpbin.org",
          "User-Agent": "curl/7.70.0",
          "X-Amzn-Trace-Id": "Root=1-5ef62b6b-ae2bb960bd1b10720f6e6560"
        },
        "origin": "118.211.191.165",
        "url": "https://httpbin.org/get",
        "args": {
        }
      },
      "api_response_headers": "map[Accept:application/json Host:httpbin.org User-Agent:curl/7.70.0 X-Amzn-Trace-Id:Root=1-5ef62b6b-ae2bb960bd1b10720f6e6560]",
      "api_response_headers_host": "httpbin.org",
      "api_response": "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62b6b-ae2bb960bd1b10720f6e6560\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}"
    })
    
    ~SubStep1: [print:  ]
    0
    ~SubStep2: [print:  ]
    {
      "args": {}, 
      "headers": {
        "Accept": "application/json", 
        "Host": "httpbin.org", 
        "User-Agent": "curl/7.70.0", 
        "X-Amzn-Trace-Id": "Root=1-5ef62b6b-ae2bb960bd1b10720f6e6560"
      }, 
      "origin": "118.211.191.165", 
      "url": "https://httpbin.org/get"
    }
    ~SubStep3: [print:  ]
    {
      "args": {}, 
      "headers": {
        "Accept": "application/json", 
        "Host": "httpbin.org", 
        "User-Agent": "curl/7.70.0", 
        "X-Amzn-Trace-Id": "Root=1-5ef62b6b-ae2bb960bd1b10720f6e6560"
      }, 
      "origin": "118.211.191.165", 
      "url": "https://httpbin.org/get"
    }
    ~SubStep4: [inspect:  ]
     1: inspect[exec_vars](*core.Cache)({
      "api_response_headers": "map[Accept:application/json Host:httpbin.org User-Agent:curl/7.70.0 X-Amzn-Trace-Id:Root=1-5ef62b6b-ae2bb960bd1b10720f6e6560]",
      "api_response_headers_host": "httpbin.org",
      "api_response": "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62b6b-ae2bb960bd1b10720f6e6560\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
      "httpbin_get_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62b6b-ae2bb960bd1b10720f6e6560\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5ef62b6b-ae2bb960bd1b10720f6e6560\"\n  }, \n  \"origin\": \"118.211.191.165\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "api_response_object": {
        "args": {
        },
        "headers": {
          "Host": "httpbin.org",
          "User-Agent": "curl/7.70.0",
          "X-Amzn-Trace-Id": "Root=1-5ef62b6b-ae2bb960bd1b10720f6e6560",
          "Accept": "application/json"
        },
        "origin": "118.211.191.165",
        "url": "https://httpbin.org/get"
      }
    })
    
    ~SubStep5: [print:  ]
    httpbin.org
    ~SubStep6: [printobj:  ]
    (string) (len=20) "api_response_headers"
    
    object:
     api_response_headers: "map[Accept:application/json Host:httpbin.org User-Agent:curl/7.70.0 X-Amzn-Trace-Id:Root=1-5ef62b6b-ae2bb960bd1b10720f6e6560]"
    
    ~SubStep7: [print: you can not use this header directly, if you intend to use a sub node, then you should use query and register a sub node
     ]
    map[Accept:application/json Host:httpbin.org User-Agent:curl/7.70.0 X-Amzn-Trace-Id:Root=1-5ef62b6b-ae2bb960bd1b10720f6e6560]
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
* [Related Chapter](../../query-object/c0141)
