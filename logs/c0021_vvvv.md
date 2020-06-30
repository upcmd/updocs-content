---
title: "c0021_vvvv"
date: 2020-07-01T15:34:23+77:00
draft: false
weight: 10213

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
                 Verbose -> vvvv
              ModuleName -> insane_goldstine6
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0021
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [insane_goldstine6] instance id: [dev]
    merged[ dev ] runtime vars:
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
        "school": "Sydney Grammar",
        "info": "student: Tom\n gender: Male\n school: Sydney Grammar\n",
        "student": "Tom",
        "gender": "Male"
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
    
    insane_goldstine6: overall final exec vars:
    
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
