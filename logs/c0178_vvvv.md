---
title: "c0178_vvvv"
date: 2020-09-18T00:51:56+99:00
draft: false
weight: 11783

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
    loading [Task]:  ./tests/functests/c0178
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
    
    -Step1: [: this will get a response of:
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
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print: mock only - pretent to call it ]
    aws elb describe-load-balancers --load-balancer-names my-web-app-elb
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "last_result": {
        "Output": "{\n \"LoadBalancerDescriptions\": [\n   {\n     \"LoadBalancerName\": \"xx-elb\",\n     \"DNSName\": \"x-y-z.elb.amazonaws.com\",\n     \"Instances\": [\n       {\n         \"InstanceId\": \"i-1234567890\"\n       },\n       {\n         \"InstanceId\": \"i-9876543210\"\n       }\n     ],\n   }\n ]\n }\n"
      }
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
    
    self: final context exec vars:
    
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
      "up_runtime_task_layer_number": 0,
      "last_result": {
        "Output": "{\n \"LoadBalancerDescriptions\": [\n   {\n     \"LoadBalancerName\": \"xx-elb\",\n     \"DNSName\": \"x-y-z.elb.amazonaws.com\",\n     \"Instances\": [\n       {\n         \"InstanceId\": \"i-1234567890\"\n       },\n       {\n         \"InstanceId\": \"i-9876543210\"\n       }\n     ],\n   }\n ]\n }\n"
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
    current exec runtime vars:
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
    })
    
    self: final context exec vars:
    
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
    
    --
    -Step4:
    current exec runtime vars:
    (*core.Cache)({
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
      "up_runtime_task_layer_number": 0
    })
    
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
      },
      "up_runtime_task_layer_number": 0,
      "instances_3": {
        {
          "InstanceId": "i-1234567890"
        },
        {
          "InstanceId": "i-9876543210"
        }
      }
    })
    
    ~SubStep1: [print:  ]
    i-1234567890
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