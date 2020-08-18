---
title: "c0141_vvvv"
date: 2020-08-18T15:16:17+88:00
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
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0141
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
    Task1: [task ==> task: test reg with a registered name
    in this case the registered reslt name is: test2_httpbinget_result
     ]
    Executing task stack layer: 1
    
    -Step1: [httpbinget: it will use the given name as var name to register the result ]
    current exec runtime vars:
    (*core.Cache)({
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
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
        "X-Amzn-Trace-Id": "Root=1-5f3a8baf-da56199a7bc175adb04e386f"
      }, 
      "origin": "118.208.99.251", 
      "url": "https://httpbin.org/get"
    }
    -
     .. ok
    . ok
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f3a8baf-da56199a7bc175adb04e386f\"\n  }, \n  \"origin\": \"118.208.99.251\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "httpbin_get_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f3a8baf-da56199a7bc175adb04e386f\"\n  }, \n  \"origin\": \"118.208.99.251\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      })
    })
    
    dvar> api_response:
    "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f3a8baf-da56199a7bc175adb04e386f\"\n  }, \n  \"origin\": \"118.208.99.251\", \n  \"url\": \"https://httpbin.org/get\"\n}"
    
    -
    {
      "args": {}, 
      "headers": {
        "Accept": "application/json", 
        "Host": "httpbin.org", 
        "User-Agent": "curl/7.70.0", 
        "X-Amzn-Trace-Id": "Root=1-5f3a8baf-da56199a7bc175adb04e386f"
      }, 
      "origin": "118.208.99.251", 
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
        "X-Amzn-Trace-Id": "Root=1-5f3a8baf-da56199a7bc175adb04e386f"
      },
      "origin": "118.208.99.251",
      "url": "https://httpbin.org/get"
    }
    
    dvar> api_response_headers:
    "map[Accept:application/json Host:httpbin.org User-Agent:curl/7.70.0 X-Amzn-Trace-Id:Root=1-5f3a8baf-da56199a7bc175adb04e386f]"
    
    -
    map[Accept:application/json Host:httpbin.org User-Agent:curl/7.70.0 X-Amzn-Trace-Id:Root=1-5f3a8baf-da56199a7bc175adb04e386f]
    dvar> api_response_headers_host:
    "httpbin.org"
    
    -
    httpbin.org
    self: final context exec vars:
    
    (*core.Cache)({
      "api_response_object": {
        "args": {
        },
        "headers": {
          "Host": "httpbin.org",
          "User-Agent": "curl/7.70.0",
          "X-Amzn-Trace-Id": "Root=1-5f3a8baf-da56199a7bc175adb04e386f",
          "Accept": "application/json"
        },
        "origin": "118.208.99.251",
        "url": "https://httpbin.org/get"
      },
      "api_response_headers": "map[Accept:application/json Host:httpbin.org User-Agent:curl/7.70.0 X-Amzn-Trace-Id:Root=1-5f3a8baf-da56199a7bc175adb04e386f]",
      "api_response_headers_host": "httpbin.org",
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f3a8baf-da56199a7bc175adb04e386f\"\n  }, \n  \"origin\": \"118.208.99.251\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "httpbin_get_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f3a8baf-da56199a7bc175adb04e386f\"\n  }, \n  \"origin\": \"118.208.99.251\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "api_response": "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f3a8baf-da56199a7bc175adb04e386f\"\n  }, \n  \"origin\": \"118.208.99.251\", \n  \"url\": \"https://httpbin.org/get\"\n}"
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
        "X-Amzn-Trace-Id": "Root=1-5f3a8baf-da56199a7bc175adb04e386f"
      }, 
      "origin": "118.208.99.251", 
      "url": "https://httpbin.org/get"
    }
    ~SubStep3: [print:  ]
    {
      "args": {}, 
      "headers": {
        "Accept": "application/json", 
        "Host": "httpbin.org", 
        "User-Agent": "curl/7.70.0", 
        "X-Amzn-Trace-Id": "Root=1-5f3a8baf-da56199a7bc175adb04e386f"
      }, 
      "origin": "118.208.99.251", 
      "url": "https://httpbin.org/get"
    }
    ~SubStep4: [inspect:  ]
     1: inspect[exec_vars]
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f3a8baf-da56199a7bc175adb04e386f\"\n  }, \n  \"origin\": \"118.208.99.251\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "httpbin_get_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f3a8baf-da56199a7bc175adb04e386f\"\n  }, \n  \"origin\": \"118.208.99.251\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "api_response": "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f3a8baf-da56199a7bc175adb04e386f\"\n  }, \n  \"origin\": \"118.208.99.251\", \n  \"url\": \"https://httpbin.org/get\"\n}",
      "api_response_object": {
        "args": {
        },
        "headers": {
          "Accept": "application/json",
          "Host": "httpbin.org",
          "User-Agent": "curl/7.70.0",
          "X-Amzn-Trace-Id": "Root=1-5f3a8baf-da56199a7bc175adb04e386f"
        },
        "origin": "118.208.99.251",
        "url": "https://httpbin.org/get"
      },
      "api_response_headers": "map[Accept:application/json Host:httpbin.org User-Agent:curl/7.70.0 X-Amzn-Trace-Id:Root=1-5f3a8baf-da56199a7bc175adb04e386f]",
      "api_response_headers_host": "httpbin.org"
    })
    
    ~SubStep5: [print:  ]
    httpbin.org
    ~SubStep6: [printObj:  ]
    (string) (len=20) "api_response_headers"
    
    object:
     api_response_headers: "map[Accept:application/json Host:httpbin.org User-Agent:curl/7.70.0 X-Amzn-Trace-Id:Root=1-5f3a8baf-da56199a7bc175adb04e386f]"
    
    ~SubStep7: [print: you can not use this header directly, if you intend to use a sub node, then you should use query and register a sub node
     ]
    map[Accept:application/json Host:httpbin.org User-Agent:curl/7.70.0 X-Amzn-Trace-Id:Root=1-5f3a8baf-da56199a7bc175adb04e386f]
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
