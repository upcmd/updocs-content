---
title: "c0040_vvvvv"
date: 2020-10-07T00:11:07+1010:00
draft: false
weight: 10404

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0040
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
    loading [Task]:  ./tests/functests/c0040
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001bf040)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc00000e8f0)({
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task: test the exit scenarios due to different types of validation ]
    Executing task stack layer: 1
    
    -Step1: [getcases:  ]
    {
      Name: "getcases",
      Do: {
        "cd ./tests/functests; ls f*.yml"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "cases",
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
    cd ./tests/functests; ls f*.yml
    
    cmd=>:
    cd ./tests/functests; ls f*.yml
    -
    f0001.yml
    f0002.yml
    f0009.yml
    f0016.yml
    f0018.yml
    f0031.yml
    f0037.yml
    f0045.yml
    f0053.yml
    f0060.yml
    f0061.yml
    f0067.yml
    f0077.yml
    f0088.yml
    f0097.yml
    f0116.yml
    f0117.yml
    f0125.yml
    f0171.yml
    f0172.yml
    f0176.yml
    f0178.yml
    f0185.yml
    f0186.yml
    f0188.yml
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=31) "cd ./tests/functests; ls f*.yml",
     Code: (int) 0,
     Output: (string) (len=249) "f0001.yml\nf0002.yml\nf0009.yml\nf0016.yml\nf0018.yml\nf0031.yml\nf0037.yml\nf0045.yml\nf0053.yml\nf0060.yml\nf0061.yml\nf0067.yml\nf0077.yml\nf0088.yml\nf0097.yml\nf0116.yml\nf0117.yml\nf0125.yml\nf0171.yml\nf0172.yml\nf0176.yml\nf0178.yml\nf0185.yml\nf0186.yml\nf0188.yml",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2: [: a real showcase of how to loop using template ]
    {
      Name: "",
      Do: {
        "{{ range $idx, $file := .cases | splitLines -}}\n{{$casename :=  $file | replace \".yml\" \"\"}}\necho \"==========failure case test {{$idx |add1}}===============\"\necho \"processing {{$casename}} ..\"\n{{end}}\n"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "a real showcase of how to loop using template",
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
      "cases": (*utils.ExecResult)({
        Cmd: "cd ./tests/functests; ls f*.yml",
        Code: 0,
        Output: "f0001.yml\nf0002.yml\nf0009.yml\nf0016.yml\nf0018.yml\nf0031.yml\nf0037.yml\nf0045.yml\nf0053.yml\nf0060.yml\nf0061.yml\nf0067.yml\nf0077.yml\nf0088.yml\nf0097.yml\nf0116.yml\nf0117.yml\nf0125.yml\nf0171.yml\nf0172.yml\nf0176.yml\nf0178.yml\nf0185.yml\nf0186.yml\nf0188.yml",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "cd ./tests/functests; ls f*.yml",
        Code: 0,
        Output: "f0001.yml\nf0002.yml\nf0009.yml\nf0016.yml\nf0018.yml\nf0031.yml\nf0037.yml\nf0045.yml\nf0053.yml\nf0060.yml\nf0061.yml\nf0067.yml\nf0077.yml\nf0088.yml\nf0097.yml\nf0116.yml\nf0117.yml\nf0125.yml\nf0171.yml\nf0172.yml\nf0176.yml\nf0178.yml\nf0185.yml\nf0186.yml\nf0188.yml",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "cases": (*utils.ExecResult)({
        Cmd: "cd ./tests/functests; ls f*.yml",
        Code: 0,
        Output: "f0001.yml\nf0002.yml\nf0009.yml\nf0016.yml\nf0018.yml\nf0031.yml\nf0037.yml\nf0045.yml\nf0053.yml\nf0060.yml\nf0061.yml\nf0067.yml\nf0077.yml\nf0088.yml\nf0097.yml\nf0116.yml\nf0117.yml\nf0125.yml\nf0171.yml\nf0172.yml\nf0176.yml\nf0178.yml\nf0185.yml\nf0186.yml\nf0188.yml",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "cd ./tests/functests; ls f*.yml",
        Code: 0,
        Output: "f0001.yml\nf0002.yml\nf0009.yml\nf0016.yml\nf0018.yml\nf0031.yml\nf0037.yml\nf0045.yml\nf0053.yml\nf0060.yml\nf0061.yml\nf0067.yml\nf0077.yml\nf0088.yml\nf0097.yml\nf0116.yml\nf0117.yml\nf0125.yml\nf0171.yml\nf0172.yml\nf0176.yml\nf0178.yml\nf0185.yml\nf0186.yml\nf0188.yml",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "cases": (*utils.ExecResult)({
        Cmd: "cd ./tests/functests; ls f*.yml",
        Code: 0,
        Output: "f0001.yml\nf0002.yml\nf0009.yml\nf0016.yml\nf0018.yml\nf0031.yml\nf0037.yml\nf0045.yml\nf0053.yml\nf0060.yml\nf0061.yml\nf0067.yml\nf0077.yml\nf0088.yml\nf0097.yml\nf0116.yml\nf0117.yml\nf0125.yml\nf0171.yml\nf0172.yml\nf0176.yml\nf0178.yml\nf0185.yml\nf0186.yml\nf0188.yml",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "cd ./tests/functests; ls f*.yml",
        Code: 0,
        Output: "f0001.yml\nf0002.yml\nf0009.yml\nf0016.yml\nf0018.yml\nf0031.yml\nf0037.yml\nf0045.yml\nf0053.yml\nf0060.yml\nf0061.yml\nf0067.yml\nf0077.yml\nf0088.yml\nf0097.yml\nf0116.yml\nf0117.yml\nf0125.yml\nf0171.yml\nf0172.yml\nf0176.yml\nf0178.yml\nf0185.yml\nf0186.yml\nf0188.yml",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    {{ range $idx, $file := .cases | splitLines -}}
    {{$casename :=  $file | replace ".yml" ""}}
    echo "==========failure case test {{$idx |add1}}==============="
    echo "processing {{$casename}} .."
    {{end}}
    
    
          template rendering -> template: .:1:33: executing "." at <splitLines>: wrong type for value; expected string; got *utils.ExecResult
    WARN:
        1:{{ range $idx, $file := .cases | splitLines -}}
        2:{{$casename :=  $file | replace ".yml" ""}}
        3:echo "==========failure case test {{$idx |add1}}==============="
        4:echo "processing {{$casename}} .."
        5:{{end}}
        6:
    
    trouble shooting tips:
    <incompatible types for comparison>: the variable might not be registered, use -v vvv to see the cache, or use inspect cmd to debug
    
    -----trace for reference-----
          template rendering -> template: .:1:33: executing "." at <splitLines>: wrong type for value; expected string; got *utils.ExecResult
    WARN:
        1:{{ range $idx, $file := .cases | splitLines -}}
        2:{{$casename :=  $file | replace ".yml" ""}}
        3:echo "==========failure case test {{$idx |add1}}==============="
        4:echo "processing {{$casename}} .."
        5:{{end}}
        6:
    
    trouble shooting tips:
    <incompatible types for comparison>: the variable might not be registered, use -v vvv to see the cache, or use inspect cmd to debug
    
    -----trace for reference-----
    cmd=>:
    
    -
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) "",
     Code: (int) 0,
     Output: (string) "",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0040 log - verbose level v](../../logs/c0040_v)
* [c0040 log - verbose level vv](../../logs/c0040_vv)
* [c0040 log - verbose level vvv](../../logs/c0040_vvv)
* [c0040 log - verbose level vvvv](../../logs/c0040_vvvv)
* [c0040 log - verbose level vvvvv](../../logs/c0040_vvvvv)

##### References
* [Related Chapter](../../template/c0040)
