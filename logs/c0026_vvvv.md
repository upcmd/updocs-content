---
title: "c0026_vvvv"
date: 2020-09-18T01:27:24+99:00
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
    loading [Task]:  ./tests/functests/c0026
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
    
      located task-> 2 [test1]: 
    =Task2: [task ==> test1: test reg with an auto registered name
    in this case the step name is empty, then the idx will be used
     ]
    Executing task stack layer: 2
    
    --Step1: [: if this step does not have a name, then the auto reg name would be task_0_reslt ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
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
        "X-Amzn-Trace-Id": "Root=1-5f6376ee-d502734dc34ae7636805bb6c"
      }, 
      "origin": "118.211.72.135", 
      "url": "https://httpbin.org/get"
    }
    
    -
     .. ok
    . ok
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "test1_0_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376ee-d502734dc34ae7636805bb6c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376ee-d502734dc34ae7636805bb6c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "test1_0_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376ee-d502734dc34ae7636805bb6c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376ee-d502734dc34ae7636805bb6c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
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
        "X-Amzn-Trace-Id": "Root=1-5f6376ee-d502734dc34ae7636805bb6c"
      }, 
      "origin": "118.211.72.135", 
      "url": "https://httpbin.org/get"
    }
      located task-> 3 [test2]: 
    =Task3: [task ==> test2: test reg with a auto registered name and the step name is not empty
    in this case the registered reslt name is: test2_httpbinget_result
     ]
    Executing task stack layer: 2
    
    --Step1: [httpbinget: if this step does not have a name, then the auto reg name would be task_0_reslt ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "test1_0_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376ee-d502734dc34ae7636805bb6c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376ee-d502734dc34ae7636805bb6c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "test1_0_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376ee-d502734dc34ae7636805bb6c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376ee-d502734dc34ae7636805bb6c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
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
        "X-Amzn-Trace-Id": "Root=1-5f6376ef-653543bd7ebb8590c0716c32"
      }, 
      "origin": "118.211.72.135", 
      "url": "https://httpbin.org/get"
    }
    
    -
     .. ok
    . ok
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "test1_0_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376ee-d502734dc34ae7636805bb6c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376ef-653543bd7ebb8590c0716c32\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "test2_httpbinget_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376ef-653543bd7ebb8590c0716c32\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "test1_0_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376ee-d502734dc34ae7636805bb6c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376ef-653543bd7ebb8590c0716c32\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "test2_httpbinget_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376ef-653543bd7ebb8590c0716c32\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
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
        "X-Amzn-Trace-Id": "Root=1-5f6376ef-653543bd7ebb8590c0716c32"
      }, 
      "origin": "118.211.72.135", 
      "url": "https://httpbin.org/get"
    }
      located task-> 4 [test3]: 
    =Task4: [task ==> test3: test reg with a registered name
    in this case the registered reslt name is: test2_httpbinget_result
     ]
    Executing task stack layer: 2
    
    --Step1: [httpbinget: it will use the given name as var name to register the result ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "test1_0_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376ee-d502734dc34ae7636805bb6c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376ef-653543bd7ebb8590c0716c32\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "test2_httpbinget_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376ef-653543bd7ebb8590c0716c32\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "test1_0_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376ee-d502734dc34ae7636805bb6c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376ef-653543bd7ebb8590c0716c32\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "test2_httpbinget_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376ef-653543bd7ebb8590c0716c32\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
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
        "X-Amzn-Trace-Id": "Root=1-5f6376f0-1f223e70ed5c72308d3a65b2"
      }, 
      "origin": "118.211.72.135", 
      "url": "https://httpbin.org/get"
    }
    
    -
     .. ok
    . ok
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "test2_httpbinget_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376ef-653543bd7ebb8590c0716c32\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "httpbin_get_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f0-1f223e70ed5c72308d3a65b2\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "test1_0_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376ee-d502734dc34ae7636805bb6c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f0-1f223e70ed5c72308d3a65b2\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "test1_0_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376ee-d502734dc34ae7636805bb6c\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f0-1f223e70ed5c72308d3a65b2\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "test2_httpbinget_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376ef-653543bd7ebb8590c0716c32\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
        ErrMsg: ""
      }),
      "httpbin_get_result": (*utils.ExecResult)({
        Cmd: "curl -s -X GET \"https://httpbin.org/get\" -H \"accept: application/json\"",
        Code: 0,
        Output: "{\n  \"args\": {}, \n  \"headers\": {\n    \"Accept\": \"application/json\", \n    \"Host\": \"httpbin.org\", \n    \"User-Agent\": \"curl/7.70.0\", \n    \"X-Amzn-Trace-Id\": \"Root=1-5f6376f0-1f223e70ed5c72308d3a65b2\"\n  }, \n  \"origin\": \"118.211.72.135\", \n  \"url\": \"https://httpbin.org/get\"\n}",
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
        "X-Amzn-Trace-Id": "Root=1-5f6376f0-1f223e70ed5c72308d3a65b2"
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
