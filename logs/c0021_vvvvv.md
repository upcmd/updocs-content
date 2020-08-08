---
title: "c0021_vvvvv"
date: 2020-08-09T01:36:02+88:00
draft: false
weight: 10214

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0021
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0021
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001c0fc0)(<nil>)
    
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
        "echo \"\"\"my student: {{.student}}\nstudent's gender: {{.gender}}\n school's name: {{.school}}\"\"\"\n",
        "{{$details := .}}\necho \"\"\"my student: {{$details.student}}\nstudent's gender: {{$details.gender}}\n school's name: {{$details.school}}\"\"\"\n",
        "{{$a := .student}}\n{{$b := .gender}}\n{{$c := .school}}\necho \"\"\"my student: {{$a}}\nstudent's gender: {{$b}}\n school's name: {{$c}}\"\"\"\n",
        "echo \"\"\"my school: {{.info.school}}\"\"\"\n",
        "echo \"\"\"my student: {{.info}}\"\"\"\n"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "student": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar",
        "info": "student: Tom\n gender: Male\n school: Sydney Grammar\n"
      },
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: {
        "ignoreError"
      },
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
      "student": "Tom",
      "gender": "Male",
      "school": "Sydney Grammar",
      "info": "student: Tom\n gender: Male\n school: Sydney Grammar\n"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "gender": "Male",
      "school": "Sydney Grammar",
      "info": "student: Tom\n gender: Male\n school: Sydney Grammar\n",
      "student": "Tom"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": "Tom",
      "gender": "Male",
      "school": "Sydney Grammar",
      "info": "student: Tom\n gender: Male\n school: Sydney Grammar\n"
    })
    
    cmd( 1):
    echo """my student: {{.student}}
    student's gender: {{.gender}}
     school's name: {{.school}}"""
    
    
    cmd=>:
    echo """my student: Tom
    student's gender: Male
     school's name: Sydney Grammar"""
    <=
    my student: Tom
    student's gender: Male
     school's name: Sydney Grammar
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=81) "echo \"\"\"my student: Tom\nstudent's gender: Male\n school's name: Sydney Grammar\"\"\"\n",
     Code: (int) 0,
     Output: (string) (len=69) "my student: Tom\nstudent's gender: Male\n school's name: Sydney Grammar",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    {{$details := .}}
    echo """my student: {{$details.student}}
    student's gender: {{$details.gender}}
     school's name: {{$details.school}}"""
    
    
    cmd=>:
    
    echo """my student: Tom
    student's gender: Male
     school's name: Sydney Grammar"""
    <=
    my student: Tom
    student's gender: Male
     school's name: Sydney Grammar
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=82) "\necho \"\"\"my student: Tom\nstudent's gender: Male\n school's name: Sydney Grammar\"\"\"\n",
     Code: (int) 0,
     Output: (string) (len=69) "my student: Tom\nstudent's gender: Male\n school's name: Sydney Grammar",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    {{$a := .student}}
    {{$b := .gender}}
    {{$c := .school}}
    echo """my student: {{$a}}
    student's gender: {{$b}}
     school's name: {{$c}}"""
    
    
    cmd=>:
    
    
    
    echo """my student: Tom
    student's gender: Male
     school's name: Sydney Grammar"""
    <=
    my student: Tom
    student's gender: Male
     school's name: Sydney Grammar
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=84) "\n\n\necho \"\"\"my student: Tom\nstudent's gender: Male\n school's name: Sydney Grammar\"\"\"\n",
     Code: (int) 0,
     Output: (string) (len=69) "my student: Tom\nstudent's gender: Male\n school's name: Sydney Grammar",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo """my school: {{.info.school}}"""
    
    
          template rendering -> template: .:1:26: executing "." at <.info.school>: can't evaluate field school in type interface {}
    WARN:
        1:echo """my school: {{.info.school}}"""
        2:
    
    trouble shooting tips:
    <incompatible types for comparison>: the variable might not be registered, use -v vvv to see the cache, or use inspect cmd to debug
    
    -----trace for reference-----
    cmd=>:
    echo """my school: <=
          exec wait -> exit status 2
    -----trace for reference-----
          exit status 2
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"\"\"my school: ",
     Code: (int) 2,
     Output: (string) "",
     ErrMsg: (string) (len=13) "exit status 2"
    }
    
    cmd( 5):
    echo """my student: {{.info}}"""
    
    
    cmd=>:
    echo """my student: student: Tom
     gender: Male
     school: Sydney Grammar
    """
    <=
    my student: student: Tom
     gender: Male
     school: Sydney Grammar
    
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=75) "echo \"\"\"my student: student: Tom\n gender: Male\n school: Sydney Grammar\n\"\"\"\n",
     Code: (int) 0,
     Output: (string) (len=62) "my student: student: Tom\n gender: Male\n school: Sydney Grammar",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0021 log - verbose level v](../../logs/c0021_v)
* [c0021 log - verbose level vv](../../logs/c0021_vv)
* [c0021 log - verbose level vvv](../../logs/c0021_vvv)
* [c0021 log - verbose level vvvv](../../logs/c0021_vvvv)
* [c0021 log - verbose level vvvvv](../../logs/c0021_vvvvv)

##### References
* [Related Chapter](../../vars/c0021)
