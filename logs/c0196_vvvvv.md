---
title: "c0196_vvvvv"
date: 2020-10-06T23:46:28+1010:00
draft: false
weight: 11964

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0196
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
    loading [Task]:  ./tests/functests/c0196
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc00025b1c0)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "my_secrete_file_reg_name": "my_secret"
    })
    
    (*core.Cache)(0xc000182908)((len=1) {
     (string) (len=24) "my_secrete_file_reg_name": (string) (len=9) "my_secret"
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "my_secrete_file_reg_name": "my_secret"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "tmpFile",
          "cmd": {
            "reg": "{{.my_secrete_file_reg_name}}",
            "content": "hello, world"
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
      "my_secrete_file_reg_name": "my_secret",
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "my_secrete_file_reg_name": "my_secret"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "my_secrete_file_reg_name": "my_secret",
      "up_runtime_task_layer_number": 0
    })
    
    map[content:hello, world reg:{{.my_secrete_file_reg_name}}]
    ~SubStep1: [tmpFile:  ]
    tmp file handler: my_secret
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "inspect",
          "cmd": {
            "debug_vars"
          }
        },
        {
          "name": "readFile",
          "cmd": {
            "filename": "{{.filepath}}",
            "reg": "my_file_content"
          }
        },
        {
          "name": "print",
          "cmd": "file content: {{.my_file_content}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "filepath",
          Value: "{{index . .my_secrete_file_reg_name}}",
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
      "my_secrete_file_reg_name": "my_secret",
      "my_secret": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84968505168",
      "up_runtime_task_layer_number": 0
    })
    
    dvar> filepath:
    "/tmp/BpLnfgDsc2WD8F2qNfHK5a84968505168"
    
    -
    /tmp/BpLnfgDsc2WD8F2qNfHK5a84968505168
    [local] dvar expanded result:
    {
      "filepath": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84968505168"
    }
    
    
    scope[local] merged: {
      "my_secret": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84968505168",
      "up_runtime_task_layer_number": 0,
      "my_secrete_file_reg_name": "my_secret",
      "filepath": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84968505168"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "my_secrete_file_reg_name": "my_secret",
      "my_secret": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84968505168",
      "up_runtime_task_layer_number": 0,
      "filepath": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84968505168"
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
      "my_secrete_file_reg_name": "my_secret",
      "my_secret": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84968505168"
    })
    
    "ExecbaseVars"
    (*core.Cache)({
      "my_secrete_file_reg_name": "my_secret",
      "my_secret": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84968505168"
    })
    
    "TaskVars"
    (*core.Cache)({
    })
    
    "ExecContextVars"
    (*core.Cache)({
      "my_secrete_file_reg_name": "my_secret",
      "my_secret": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84968505168",
      "up_runtime_task_layer_number": 0,
      "filepath": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84968505168"
    })
    
    --
    map[filename:{{.filepath}} reg:my_file_content]
    ~SubStep2: [readFile:  ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "my_secrete_file_reg_name": "my_secret",
      "my_secret": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84968505168",
      "my_file_content": "hello, world"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "my_secrete_file_reg_name": "my_secret",
      "my_secret": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84968505168",
      "up_runtime_task_layer_number": 0,
      "filepath": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84968505168",
      "my_file_content": "hello, world"
    })
    
    file content: {{.my_file_content}}
    ~SubStep3: [print:  ]
    file content: hello, world
    
```

##### Logs with different verbose level
* [c0196 log - verbose level v](../../logs/c0196_v)
* [c0196 log - verbose level vv](../../logs/c0196_vv)
* [c0196 log - verbose level vvv](../../logs/c0196_vvv)
* [c0196 log - verbose level vvvv](../../logs/c0196_vvvv)
* [c0196 log - verbose level vvvvv](../../logs/c0196_vvvvv)

##### References
* [Related Chapter](../../cmd-func/c0196)
