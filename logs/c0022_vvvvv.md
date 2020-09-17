---
title: "c0022_vvvvv"
date: 2020-09-18T01:27:23+99:00
draft: false
weight: 10224

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0022
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
    loading [Task]:  ./tests/functests/c0022
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc000240f40)(<nil>)
    
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
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"\"\"{{.info}}\"\"\"\n"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "student": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar",
        "info": "my student: {{.student}}\nstudent's gender: {{.gender}}\nschool's name: {{.school}}\n"
      },
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
      "school": "Sydney Grammar",
      "info": "my student: {{.student}}\nstudent's gender: {{.gender}}\nschool's name: {{.school}}\n",
      "up_runtime_task_layer_number": 0,
      "student": "Tom",
      "gender": "Male"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "school": "Sydney Grammar",
      "info": "my student: {{.student}}\nstudent's gender: {{.gender}}\nschool's name: {{.school}}\n",
      "up_runtime_task_layer_number": 0,
      "student": "Tom",
      "gender": "Male"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "info": "my student: {{.student}}\nstudent's gender: {{.gender}}\nschool's name: {{.school}}\n",
      "up_runtime_task_layer_number": 0,
      "student": "Tom",
      "gender": "Male",
      "school": "Sydney Grammar"
    })
    
    cmd( 1):
    echo """{{.info}}"""
    
    
    cmd=>:
    echo """my student: {{.student}}
    student's gender: {{.gender}}
    school's name: {{.school}}
    """
    
    -
    my student: {{.student}}
    student's gender: {{.gender}}
    school's name: {{.school}}
    
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=94) "echo \"\"\"my student: {{.student}}\nstudent's gender: {{.gender}}\nschool's name: {{.school}}\n\"\"\"\n",
     Code: (int) 0,
     Output: (string) (len=81) "my student: {{.student}}\nstudent's gender: {{.gender}}\nschool's name: {{.school}}",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0022 log - verbose level v](../../logs/c0022_v)
* [c0022 log - verbose level vv](../../logs/c0022_vv)
* [c0022 log - verbose level vvv](../../logs/c0022_vvv)
* [c0022 log - verbose level vvvv](../../logs/c0022_vvvv)
* [c0022 log - verbose level vvvvv](../../logs/c0022_vvvvv)

##### References
* [Related Chapter](../../vars/c0022)
