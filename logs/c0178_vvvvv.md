---
title: "c0178_vvvvv"
date: 2020-10-06T23:46:25+1010:00
draft: false
weight: 11784

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0178
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
    loading [Task]:  ./tests/functests/c0178
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001d94a0)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc000104908)({
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [
    this will get a response of:
    Output: {
      "LoadBalancerDescriptions": [
        {
          "LoadBalancerName": "xx-elb",
          "DNSName": "x-y-z.elb.amazonaws.com",
          ...........
          "Instances": [
            {
              "InstanceId": "i-1234567890"
            },
            {
              "InstanceId": "i-9876543210"
            }
          ],
          ...........
        }
      ]
    }
    ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "desc": "mock only - pretent to call it",
          "cmd": "aws elb describe-load-balancers --load-balancer-names my-web-app-elb"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "this will get a response of:\nOutput: {\n  \"LoadBalancerDescriptions\": [\n    {\n      \"LoadBalancerName\": \"xx-elb\",\n      \"DNSName\": \"x-y-z.elb.amazonaws.com\",\n      ...........\n      \"Instances\": [\n        {\n          \"InstanceId\": \"i-1234567890\"\n        },\n        {\n          \"InstanceId\": \"i-9876543210\"\n        }\n      ],\n      ...........\n    }\n  ]\n}\n",
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
    
    aws elb describe-load-balancers --load-balancer-names my-web-app-elb
    ~SubStep1: [print: mock only - pretent to call it ]
    aws elb describe-load-balancers --load-balancer-names my-web-app-elb
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "printObj",
          "cmd": "instances_1"
        },
        {
          "name": "printObj",
          "cmd": "instances_2"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "last_result": {
          "Output": "{\n \"LoadBalancerDescriptions\": [\n   {\n     \"LoadBalancerName\": \"xx-elb\",\n     \"DNSName\": \"x-y-z.elb.amazonaws.com\",\n     \"Instances\": [\n       {\n         \"InstanceId\": \"i-1234567890\"\n       },\n       {\n         \"InstanceId\": \"i-9876543210\"\n       }\n     ],\n   }\n ]\n }\n"
        }
      },
      Dvars: {
        {
          Name: "elb",
          Value: "{{.last_result.Output}}",
          Desc: "this will map the reponse to name of elb\nthen convert it to an object and register to cache\nthe object name would be kept the same called elb, so now elb is a object instead of string content\nit is marked as in taskScope, means that it will be available to be acessible in the next func call in Main task\n",
          Expand: 0,
          Flags: {
            "keepName",
            "toObj",
            "reg",
            "taskScope",
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
          Name: "void",
          Value: "{{(index .elb.LoadBalancerDescriptions 0).Instances |objToYml|ymlToObj|reg \"instances_1\"}}",
          Desc: "index .elb.LoadBalancerDescriptions 0 will locate the sub object of Instances\nobjToYml template func is chained and called to to convert the objToYml\nthen the yml is again converted to an object\nthen registered as name of instances_1 which is a object\nthe dvar name \"void\" means it does not register the string value to cached\n\n* note: instances_1 is a object of type of *interface{}\n\n\"instances_1\": (*[]interface {})({\n  {\n    \"InstanceId\": \"i-02f5cf3cdb572d627\"\n  },\n  {\n    \"InstanceId\": \"i-00e53fd8688e9193a\"\n  }\n})\n\nSo you can use access and reference instances_1 in template value, however this internal type will not match what is required for loop tag, even though it looks like it is iteratable\n\nYou can access, reference to sub element and iterate it using the go template though, for example:\n'{{(index .instances_1. 0).Instances}}' => \"i-02f5cf3cdb572d627\"\n",
          Expand: 0,
          Flags: <nil>,
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        },
        {
          Name: "void",
          Value: "{{(index .elb.LoadBalancerDescriptions 0).Instances |regObj \"instances_2\"}}",
          Desc: "regObj is a template func as short hand to register the chain through object into the cache\nthe name of the object is instances_2\n",
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
      "last_result": {
        "Output": "{\n \"LoadBalancerDescriptions\": [\n   {\n     \"LoadBalancerName\": \"xx-elb\",\n     \"DNSName\": \"x-y-z.elb.amazonaws.com\",\n     \"Instances\": [\n       {\n         \"InstanceId\": \"i-1234567890\"\n       },\n       {\n         \"InstanceId\": \"i-9876543210\"\n       }\n     ],\n   }\n ]\n }\n"
      },
      "up_runtime_task_layer_number": 0
    })
    
    dvar> elb:
    "{\n \"LoadBalancerDescriptions\": [\n   {\n     \"LoadBalancerName\": \"xx-elb\",\n     \"DNSName\": \"x-y-z.elb.amazonaws.com\",\n     \"Instances\": [\n       {\n         \"InstanceId\": \"i-1234567890\"\n       },\n       {\n         \"InstanceId\": \"i-9876543210\"\n       }\n     ],\n   }\n ]\n }\n"
    
    -
    {
     "LoadBalancerDescriptions": [
       {
         "LoadBalancerName": "xx-elb",
         "DNSName": "x-y-z.elb.amazonaws.com",
         "Instances": [
           {
             "InstanceId": "i-1234567890"
           },
           {
             "InstanceId": "i-9876543210"
           }
         ],
       }
     ]
     }
    
    dvar[object]> elb:
    {
      "LoadBalancerDescriptions": {
        {
          "LoadBalancerName": "xx-elb",
          "DNSName": "x-y-z.elb.amazonaws.com",
          "Instances": {
            {
              "InstanceId": "i-1234567890"
            },
            {
              "InstanceId": "i-9876543210"
            }
          }
        }
      }
    }
    
    objToYml:
    "- InstanceId: i-1234567890\n- InstanceId: i-9876543210\n"
    
    ymlToObj:
    (*[]interface {})({
      {
        "InstanceId": "i-1234567890"
      },
      {
        "InstanceId": "i-9876543210"
      }
    })
    
    ymlToObj:
    (*[]interface {})({
      {
        "InstanceId": "i-1234567890"
      },
      {
        "InstanceId": "i-9876543210"
      }
    })
    
    [local] dvar expanded result:
    {
      "elb": {
        "LoadBalancerDescriptions": {
          {
            "LoadBalancerName": "xx-elb",
            "DNSName": "x-y-z.elb.amazonaws.com",
            "Instances": {
              {
                "InstanceId": "i-1234567890"
              },
              {
                "InstanceId": "i-9876543210"
              }
            }
          }
        }
      },
      "instances_1": (*[]interface {})({
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      }),
      "instances_2": (*[]interface {})({
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      })
    }
    
    
    scope[local] merged: {
      "last_result": {
        "Output": "{\n \"LoadBalancerDescriptions\": [\n   {\n     \"LoadBalancerName\": \"xx-elb\",\n     \"DNSName\": \"x-y-z.elb.amazonaws.com\",\n     \"Instances\": [\n       {\n         \"InstanceId\": \"i-1234567890\"\n       },\n       {\n         \"InstanceId\": \"i-9876543210\"\n       }\n     ],\n   }\n ]\n }\n"
      },
      "up_runtime_task_layer_number": 0,
      "instances_2": (*[]interface {})({
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      }),
      "elb": {
        "LoadBalancerDescriptions": {
          {
            "DNSName": "x-y-z.elb.amazonaws.com",
            "Instances": {
              {
                "InstanceId": "i-1234567890"
              },
              {
                "InstanceId": "i-9876543210"
              }
            },
            "LoadBalancerName": "xx-elb"
          }
        }
      },
      "instances_1": (*[]interface {})({
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "instances_1": (*[]interface {})({
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      }),
      "up_runtime_task_layer_number": 0,
      "last_result": {
        "Output": "{\n \"LoadBalancerDescriptions\": [\n   {\n     \"LoadBalancerName\": \"xx-elb\",\n     \"DNSName\": \"x-y-z.elb.amazonaws.com\",\n     \"Instances\": [\n       {\n         \"InstanceId\": \"i-1234567890\"\n       },\n       {\n         \"InstanceId\": \"i-9876543210\"\n       }\n     ],\n   }\n ]\n }\n"
      },
      "instances_2": (*[]interface {})({
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      }),
      "elb": {
        "LoadBalancerDescriptions": {
          {
            "LoadBalancerName": "xx-elb",
            "DNSName": "x-y-z.elb.amazonaws.com",
            "Instances": {
              {
                "InstanceId": "i-1234567890"
              },
              {
                "InstanceId": "i-9876543210"
              }
            }
          }
        }
      }
    })
    
    instances_1
    ~SubStep1: [printObj:  ]
    (string) (len=11) "instances_1"
    
    object:
     instances_1: (*[]interface {})({
      {
        "InstanceId": "i-1234567890"
      },
      {
        "InstanceId": "i-9876543210"
      }
    })
    
    instances_2
    ~SubStep2: [printObj:  ]
    (string) (len=11) "instances_2"
    
    object:
     instances_2: (*[]interface {})({
      {
        "InstanceId": "i-1234567890"
      },
      {
        "InstanceId": "i-9876543210"
      }
    })
    
    -Step3:
    {
      Name: "",
      Do: {
        {
          "name": "inspect",
          "cmd": {
            "debug_vars"
          }
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
      "elb": {
        "LoadBalancerDescriptions": {
          {
            "DNSName": "x-y-z.elb.amazonaws.com",
            "Instances": {
              {
                "InstanceId": "i-1234567890"
              },
              {
                "InstanceId": "i-9876543210"
              }
            },
            "LoadBalancerName": "xx-elb"
          }
        }
      },
      "instances_1": (*[]interface {})({
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      }),
      "instances_2": (*[]interface {})({
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      }),
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "elb": {
        "LoadBalancerDescriptions": {
          {
            "Instances": {
              {
                "InstanceId": "i-1234567890"
              },
              {
                "InstanceId": "i-9876543210"
              }
            },
            "LoadBalancerName": "xx-elb",
            "DNSName": "x-y-z.elb.amazonaws.com"
          }
        }
      },
      "instances_1": (*[]interface {})({
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      }),
      "instances_2": (*[]interface {})({
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      }),
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "instances_2": (*[]interface {})({
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      }),
      "up_runtime_task_layer_number": 0,
      "elb": {
        "LoadBalancerDescriptions": {
          {
            "LoadBalancerName": "xx-elb",
            "DNSName": "x-y-z.elb.amazonaws.com",
            "Instances": {
              {
                "InstanceId": "i-1234567890"
              },
              {
                "InstanceId": "i-9876543210"
              }
            }
          }
        }
      },
      "instances_1": (*[]interface {})({
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      })
    })
    
    [debug_vars]
    ~SubStep1: [inspect:  ]
     1: inspect[debug_vars]
    -debug vars-
    "UpRunTimeVars"
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    "RuntimeVarsAndDvarsMerged"
    (*core.Cache)({
      "elb": {
        "LoadBalancerDescriptions": {
          {
            "LoadBalancerName": "xx-elb",
            "DNSName": "x-y-z.elb.amazonaws.com",
            "Instances": {
              {
                "InstanceId": "i-1234567890"
              },
              {
                "InstanceId": "i-9876543210"
              }
            }
          }
        }
      },
      "instances_1": (*[]interface {})({
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      }),
      "instances_2": (*[]interface {})({
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      })
    })
    
    "ExecbaseVars"
    (*core.Cache)({
      "elb": {
        "LoadBalancerDescriptions": {
          {
            "LoadBalancerName": "xx-elb",
            "DNSName": "x-y-z.elb.amazonaws.com",
            "Instances": {
              {
                "InstanceId": "i-1234567890"
              },
              {
                "InstanceId": "i-9876543210"
              }
            }
          }
        }
      },
      "instances_1": (*[]interface {})({
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      }),
      "instances_2": (*[]interface {})({
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      })
    })
    
    "TaskVars"
    (*core.Cache)({
      "elb": {
        "LoadBalancerDescriptions": {
          {
            "LoadBalancerName": "xx-elb",
            "DNSName": "x-y-z.elb.amazonaws.com",
            "Instances": {
              {
                "InstanceId": "i-1234567890"
              },
              {
                "InstanceId": "i-9876543210"
              }
            }
          }
        }
      }
    })
    
    "ExecContextVars"
    (*core.Cache)({
      "elb": {
        "LoadBalancerDescriptions": {
          {
            "Instances": {
              {
                "InstanceId": "i-1234567890"
              },
              {
                "InstanceId": "i-9876543210"
              }
            },
            "LoadBalancerName": "xx-elb",
            "DNSName": "x-y-z.elb.amazonaws.com"
          }
        }
      },
      "instances_1": (*[]interface {})({
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      }),
      "instances_2": (*[]interface {})({
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      }),
      "up_runtime_task_layer_number": 0
    })
    
    --
    -Step4:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.loopitem.InstanceId}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "instances_3",
          Value: "{{(index .elb.LoadBalancerDescriptions 0).Instances | objToYml}}",
          Desc: "index .elb.LoadBalancerDescriptions 0 will locate the sub object of Instances\nobjToYml template func is chained and called to to convert the objToYml, now the result is yml string\ntoObj flag decorate the behavior to convert the yml string to an object and the object name is kept the same as instances_3\n\n* note the different of instances_3 and ( instances_1 or instances_2) is the internal data type\n\ninstances_3 data type is a plain slice/array and we can use this for the loop tag\n{\n  {\n    \"InstanceId\": \"i-02f5cf3cdb572d627\"\n  },\n  {\n    \"InstanceId\": \"i-00e53fd8688e9193a\"\n  }\n}\n",
          Expand: 0,
          Flags: {
            "v",
            "keepName",
            "toObj"
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
      Loop: "instances_3",
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "elb": {
        "LoadBalancerDescriptions": {
          {
            "LoadBalancerName": "xx-elb",
            "DNSName": "x-y-z.elb.amazonaws.com",
            "Instances": {
              {
                "InstanceId": "i-1234567890"
              },
              {
                "InstanceId": "i-9876543210"
              }
            }
          }
        }
      },
      "instances_1": (*[]interface {})({
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      }),
      "instances_2": (*[]interface {})({
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      }),
      "up_runtime_task_layer_number": 0
    })
    
    objToYml:
    "- InstanceId: i-1234567890\n- InstanceId: i-9876543210\n"
    
    dvar> instances_3:
    "- InstanceId: i-1234567890\n- InstanceId: i-9876543210\n"
    
    -
    - InstanceId: i-1234567890
    - InstanceId: i-9876543210
    
    dvar[object]> instances_3:
    {
      {
        "InstanceId": "i-1234567890"
      },
      {
        "InstanceId": "i-9876543210"
      }
    }
    
    [local] dvar expanded result:
    {
      "instances_3": {
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      }
    }
    
    
    scope[local] merged: {
      "instances_2": (*[]interface {})({
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      }),
      "up_runtime_task_layer_number": 0,
      "instances_3": {
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      },
      "elb": {
        "LoadBalancerDescriptions": {
          {
            "Instances": {
              {
                "InstanceId": "i-1234567890"
              },
              {
                "InstanceId": "i-9876543210"
              }
            },
            "LoadBalancerName": "xx-elb",
            "DNSName": "x-y-z.elb.amazonaws.com"
          }
        }
      },
      "instances_1": (*[]interface {})({
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "instances_3": {
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      },
      "elb": {
        "LoadBalancerDescriptions": {
          {
            "DNSName": "x-y-z.elb.amazonaws.com",
            "Instances": {
              {
                "InstanceId": "i-1234567890"
              },
              {
                "InstanceId": "i-9876543210"
              }
            },
            "LoadBalancerName": "xx-elb"
          }
        }
      },
      "instances_1": (*[]interface {})({
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      }),
      "instances_2": (*[]interface {})({
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      })
    })
    
    {{.loopitem.InstanceId}}
    ~SubStep1: [print:  ]
    i-1234567890
    {{.loopitem.InstanceId}}
    ~SubStep1: [print:  ]
    i-9876543210
    
```

##### Logs with different verbose level
* [c0178 log - verbose level v](../../logs/c0178_v)
* [c0178 log - verbose level vv](../../logs/c0178_vv)
* [c0178 log - verbose level vvv](../../logs/c0178_vvv)
* [c0178 log - verbose level vvvv](../../logs/c0178_vvvv)
* [c0178 log - verbose level vvvvv](../../logs/c0178_vvvvv)

##### References
* [Related Chapter](../../object-oriented/c0178)
