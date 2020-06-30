---
title: "c0022_vvvvv"
date: 2020-07-01T15:34:23+77:00
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
              ModuleName -> trusting_cori2
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0022
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001eae60)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [trusting_cori2] instance id: [dev]
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "student": "Tom",
      "gender": "Male",
      "school": "Sydney Grammar",
      "info": "my student: {{.student}}\nstudent's gender: {{.gender}}\nschool's name: {{.school}}\n"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "student": "Tom",
      "gender": "Male",
      "school": "Sydney Grammar",
      "info": "my student: {{.student}}\nstudent's gender: {{.gender}}\nschool's name: {{.school}}\n"
    }
    
    
    trusting_cori2: overall final exec vars:
    
    (*core.Cache)({
      "student": "Tom",
      "gender": "Male",
      "school": "Sydney Grammar",
      "info": "my student: {{.student}}\nstudent's gender: {{.gender}}\nschool's name: {{.school}}\n"
    })
    
    cmd( 1):
    echo """{{.info}}"""
    
    
     \_ echo """my student: {{.student}}
    student's gender: {{.gender}}
    school's name: {{.school}}
    """
    
    my student: {{.student}}
    student's gender: {{.gender}}
    school's name: {{.school}}
     .. ok
    (utils.ExecResult) {
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
