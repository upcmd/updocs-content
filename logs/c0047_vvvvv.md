---
title: "c0047_vvvvv"
date: 2020-10-07T00:11:08+1010:00
draft: false
weight: 10474

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0047
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
    loading [Task]:  ./tests/functests/c0047
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc000173240)((len=1 cap=1) {
     (impl.Scope) {
      Name: (string) (len=6) "global",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) <nil>,
      Vars: (core.Cache) <nil>,
      Dvars: (impl.Dvars) (len=2 cap=2) {
       (impl.Dvar) {
        Name: (string) (len=12) "student_name",
        Value: (string) (len=45) "{{ env \"STUDENT_NAME\" |default \"Tom Hanks\" }}",
        Desc: (string) "",
        Expand: (int) 0,
        Flags: ([]string) <nil>,
        Rendered: (string) "",
        Secure: (*utils.SecureSetting)(<nil>),
        Ref: (string) "",
        RefDir: (string) "",
        DataKey: (string) "",
        DataPath: (string) "",
        DataTemplate: (string) ""
       },
       (impl.Dvar) {
        Name: (string) (len=11) "student_age",
        Value: (string) (len=35) "{{ env \"STUDENT_AGE\" |default 28 }}",
        Desc: (string) "",
        Expand: (int) 0,
        Flags: ([]string) <nil>,
        Rendered: (string) "",
        Secure: (*utils.SecureSetting)(<nil>),
        Ref: (string) "",
        RefDir: (string) "",
        DataKey: (string) "",
        DataPath: (string) "",
        DataTemplate: (string) ""
       }
      }
     }
    })
    
    [global] dvar expanded result:
    {
      "student_name": "Tom Hanks",
      "student_age": "28"
    }
    
    
    scope[global] merged: {
      "student_name": "Tom Hanks",
      "student_age": "28"
    }
    
    
    ---------group vars----------
    
    global: (*core.Cache)({
      "student_name": "Tom Hanks",
      "student_age": "28"
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "student_name": "Tom Hanks",
      "student_age": "28"
    })
    
    (*core.Cache)(0xc0000b6960)((len=2) {
     (string) (len=12) "student_name": (string) (len=9) "Tom Hanks",
     (string) (len=11) "student_age": (string) (len=2) "28"
    })
    
    [runtime global] dvar expanded result:
    {
      "cli": "echo \"\"\"\nstudent details:\nname: Tom Hanks\nage: 28\n\"\"\"\n"
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "student_age": "28",
      "cli": "echo \"\"\"\nstudent details:\nname: Tom Hanks\nage: 28\n\"\"\"\n",
      "student_name": "Tom Hanks"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "{{.cli}}"
      },
      Dox: <nil>,
      Func: "shell",
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
      "student_name": "Tom Hanks",
      "student_age": "28",
      "cli": "echo \"\"\"\nstudent details:\nname: Tom Hanks\nage: 28\n\"\"\"\n",
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "student_name": "Tom Hanks",
      "student_age": "28",
      "cli": "echo \"\"\"\nstudent details:\nname: Tom Hanks\nage: 28\n\"\"\"\n",
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student_name": "Tom Hanks",
      "student_age": "28",
      "cli": "echo \"\"\"\nstudent details:\nname: Tom Hanks\nage: 28\n\"\"\"\n",
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    {{.cli}}
    
    cmd=>:
    echo """
    student details:
    name: Tom Hanks
    age: 28
    """
    
    -
    
    student details:
    name: Tom Hanks
    age: 28
    
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=54) "echo \"\"\"\nstudent details:\nname: Tom Hanks\nage: 28\n\"\"\"\n",
     Code: (int) 0,
     Output: (string) (len=40) "student details:\nname: Tom Hanks\nage: 28",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0047 log - verbose level v](../../logs/c0047_v)
* [c0047 log - verbose level vv](../../logs/c0047_vv)
* [c0047 log - verbose level vvv](../../logs/c0047_vvv)
* [c0047 log - verbose level vvvv](../../logs/c0047_vvvv)
* [c0047 log - verbose level vvvvv](../../logs/c0047_vvvvv)

##### References
* [Related Chapter](../../design-patterns/c0047)
