---
title: "c0021_vvvvv"
date: 2020-06-27T03:09:16+66:00
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
              ModuleName -> mad_hawking1
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0021
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001eaf00)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [mad_hawking1] instance id: [dev]
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
        "ignore_error"
      },
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "gender": "Male",
      "school": "Sydney Grammar",
      "info": "student: Tom\n gender: Male\n school: Sydney Grammar\n",
      "student": "Tom"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "student": "Tom",
      "gender": "Male",
      "school": "Sydney Grammar",
      "info": "student: Tom\n gender: Male\n school: Sydney Grammar\n"
    }
    
    
    mad_hawking1: overall final exec vars:
    
    (*core.Cache)({
      "info": "student: Tom\n gender: Male\n school: Sydney Grammar\n",
      "student": "Tom",
      "gender": "Male",
      "school": "Sydney Grammar"
    })
    
    cmd( 1):
    echo """my student: {{.student}}
    student's gender: {{.gender}}
     school's name: {{.school}}"""
    
    
     \_ echo """my student: Tom
    student's gender: Male
     school's name: Sydney Grammar"""
    
    my student: Tom
    student's gender: Male
     school's name: Sydney Grammar
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=69) "my student: Tom\nstudent's gender: Male\n school's name: Sydney Grammar",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    {{$details := .}}
    echo """my student: {{$details.student}}
    student's gender: {{$details.gender}}
     school's name: {{$details.school}}"""
    
    
     \_ 
    echo """my student: Tom
    student's gender: Male
     school's name: Sydney Grammar"""
    
    my student: Tom
    student's gender: Male
     school's name: Sydney Grammar
     .. ok
    (utils.ExecResult) {
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
    
    
     \_ 
    
    
    echo """my student: Tom
    student's gender: Male
     school's name: Sydney Grammar"""
    
    my student: Tom
    student's gender: Male
     school's name: Sydney Grammar
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=69) "my student: Tom\nstudent's gender: Male\n school's name: Sydney Grammar",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo """my school: {{.info.school}}"""
    
    
          template rendering problem -> template: .:1:26: executing "." at <.info.school>: can't evaluate field school in type interface {}
    WARN:
        1:echo """my school: {{.info.school}}"""
        2:
    
    -----trace for reference-----
     \_ echo """my school: 
          exec error: -> exit status 1
    -----trace for reference-----
    
          /bin/sh: -c: line 0: unexpected EOF while looking for matching `"'
    /bin/sh: -c: line 1: syntax error: unexpected end of file
    
     .. failed(suppressed if not last step)
    (utils.ExecResult) {
     Code: (int) 1,
     Output: (string) "",
     ErrMsg: (string) (len=125) "/bin/sh: -c: line 0: unexpected EOF while looking for matching `\"'\n/bin/sh: -c: line 1: syntax error: unexpected end of file\n"
    }
    
    cmd( 5):
    echo """my student: {{.info}}"""
    
    
     \_ echo """my student: student: Tom
     gender: Male
     school: Sydney Grammar
    """
    
    my student: student: Tom
     gender: Male
     school: Sydney Grammar
     .. ok
    (utils.ExecResult) {
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
