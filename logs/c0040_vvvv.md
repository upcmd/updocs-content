---
title: "c0040_vvvv"
date: 2020-10-06T23:45:57+1010:00
draft: false
weight: 10403

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
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0040
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task: test the exit scenarios due to different types of validation ]
    Executing task stack layer: 1
    
    -Step1: [getcases:  ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
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
    . ok
    -Step2: [: a real showcase of how to loop using template ]
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
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "cd ./tests/functests; ls f*.yml",
        Code: 0,
        Output: "f0001.yml\nf0002.yml\nf0009.yml\nf0016.yml\nf0018.yml\nf0031.yml\nf0037.yml\nf0045.yml\nf0053.yml\nf0060.yml\nf0061.yml\nf0067.yml\nf0077.yml\nf0088.yml\nf0097.yml\nf0116.yml\nf0117.yml\nf0125.yml\nf0171.yml\nf0172.yml\nf0176.yml\nf0178.yml\nf0185.yml\nf0186.yml\nf0188.yml",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "cases": (*utils.ExecResult)({
        Cmd: "cd ./tests/functests; ls f*.yml",
        Code: 0,
        Output: "f0001.yml\nf0002.yml\nf0009.yml\nf0016.yml\nf0018.yml\nf0031.yml\nf0037.yml\nf0045.yml\nf0053.yml\nf0060.yml\nf0061.yml\nf0067.yml\nf0077.yml\nf0088.yml\nf0097.yml\nf0116.yml\nf0117.yml\nf0125.yml\nf0171.yml\nf0172.yml\nf0176.yml\nf0178.yml\nf0185.yml\nf0186.yml\nf0188.yml",
        ErrMsg: ""
      })
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
    
    cmd=>:
    
    -
    
    -
     .. ok
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
