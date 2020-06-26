---
title: "c0039_vvvvv"
date: 2020-06-27T03:09:19+66:00
draft: false
weight: 10394

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0039
                 Verbose -> vvvvv
              ModuleName -> insane_banach8
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0039
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ed5e0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [insane_banach8] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "ns": "prod",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "ha": true,
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "pod_name": "web_app",
      "old": 54,
      "student": {
        "gender": "Male",
        "teachers": {
          "tom",
          "jason",
          "alice"
        },
        "address": {
          "suburb": {
            "postcode": 2000,
            "cbd": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom"
      },
      "template_def_consume_dynamic_t3": "{{define \"T3\"}}student:\n  name: {{template \"T1\" .name}}\n  gender: {{template \"T2\" .gender}}{{end}}\n{{template \"T3\" .student}}\n",
      "template_def_consume_dynamic_t2": "{{define \"T2\"}}TWO: {{.}}{{end}}",
      "template_def_consume_dynamic_main": "{{.template_def_consume_dynamic_t1}}\n{{.template_def_consume_dynamic_t2}}\n{{.template_def_consume_dynamic_t3}}\n{{template \"T3\" .student}}\n",
      "age": 34,
      "template_def_consume_dynamic_t1": "{{define \"T1\"}}ONE: {{.}}{{end}}\n",
      "nobody": <nil>
    }
    
    (core.Cache) (len=13) {
     (string) (len=8) "managers": ([]interface {}) (len=3 cap=3) {
      (string) (len=3) "tom",
      (string) (len=5) "jason",
      (string) (len=5) "alice"
     },
     (string) (len=8) "pod_name": (string) (len=7) "web_app",
     (string) (len=2) "ns": (string) (len=4) "prod",
     (string) (len=6) "admins": ([]interface {}) (len=3 cap=3) {
      (string) (len=3) "tom",
      (string) (len=5) "jason",
      (string) (len=5) "alice"
     },
     (string) (len=2) "ha": (bool) true,
     (string) (len=31) "template_def_consume_dynamic_t1": (string) (len=33) "{{define \"T1\"}}ONE: {{.}}{{end}}\n",
     (string) (len=6) "nobody": (interface {}) <nil>,
     (string) (len=3) "old": (int) 54,
     (string) (len=7) "student": (map[string]interface {}) (len=4) {
      (string) (len=6) "gender": (string) (len=4) "Male",
      (string) (len=8) "teachers": ([]interface {}) (len=3 cap=3) {
       (string) (len=3) "tom",
       (string) (len=5) "jason",
       (string) (len=5) "alice"
      },
      (string) (len=7) "address": (map[string]interface {}) (len=2) {
       (string) (len=6) "suburb": (map[string]interface {}) (len=3) {
        (string) (len=3) "cbd": (bool) true,
        (string) (len=4) "name": (string) (len=6) "sydney",
        (string) (len=8) "postcode": (int) 2000
       },
       (string) (len=6) "school": (string) (len=14) "Sydney Grammar"
      },
      (string) (len=4) "name": (string) (len=3) "Tom"
     },
     (string) (len=31) "template_def_consume_dynamic_t3": (string) (len=126) "{{define \"T3\"}}student:\n  name: {{template \"T1\" .name}}\n  gender: {{template \"T2\" .gender}}{{end}}\n{{template \"T3\" .student}}\n",
     (string) (len=31) "template_def_consume_dynamic_t2": (string) (len=32) "{{define \"T2\"}}TWO: {{.}}{{end}}",
     (string) (len=33) "template_def_consume_dynamic_main": (string) (len=138) "{{.template_def_consume_dynamic_t1}}\n{{.template_def_consume_dynamic_t2}}\n{{.template_def_consume_dynamic_t3}}\n{{template \"T3\" .student}}\n",
     (string) (len=3) "age": (int) 34
    }
    
    dvar> usage_of_with:
    "  student name: Tom\n  school name: Sydney Grammar\n  Male\n  "
    
    dvar> usage_of_with_else:
    "  i am somebody  "
    
    dvar> template_def_plain:
    "\n\n\nONE TWO\"\n"
    
    dvar> template_def_consume:
    "\nshow example of how you can define reusable template\nand how you can pass in the parameters\n\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n"
    
          template rendering problem -> template: .:4:11: executing "." at <{{template "T3" .student}}>: template "T3" not defined
    WARN:
        1:{{.template_def_consume_dynamic_t1}}
        2:{{.template_def_consume_dynamic_t2}}
        3:{{.template_def_consume_dynamic_t3}}
        4:{{template "T3" .student}}
        5:
        6:
    
    -----trace for reference-----
    dvar> template_def_consume_dynamic:
    "\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n\n"
    
    dvar> template_use_block:
    "\n\nstudent:\n  name: ONE: Tom\ngender: TWO: Male\n\n"
    
    [runtime global] dvar expanded result:
    {
      "usage_of_with": "  student name: Tom\n  school name: Sydney Grammar\n  Male\n  ",
      "usage_of_with_else": "  i am somebody  ",
      "template_def_plain": "\n\n\nONE TWO\"\n",
      "template_def_consume": "\nshow example of how you can define reusable template\nand how you can pass in the parameters\n\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n",
      "template_def_consume_dynamic": "\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n\n",
      "template_use_block": "\n\nstudent:\n  name: ONE: Tom\ngender: TWO: Male\n\n"
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "template_def_consume_dynamic_t1": "{{define \"T1\"}}ONE: {{.}}{{end}}\n",
      "template_def_consume_dynamic_t3": "{{define \"T3\"}}student:\n  name: {{template \"T1\" .name}}\n  gender: {{template \"T2\" .gender}}{{end}}\n{{template \"T3\" .student}}\n",
      "ns": "prod",
      "template_use_block": "\n\nstudent:\n  name: ONE: Tom\ngender: TWO: Male\n\n",
      "template_def_plain": "\n\n\nONE TWO\"\n",
      "template_def_consume_dynamic_main": "{{.template_def_consume_dynamic_t1}}\n{{.template_def_consume_dynamic_t2}}\n{{.template_def_consume_dynamic_t3}}\n{{template \"T3\" .student}}\n",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "usage_of_with_else": "  i am somebody  ",
      "age": 34,
      "old": 54,
      "template_def_consume_dynamic_t2": "{{define \"T2\"}}TWO: {{.}}{{end}}",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "pod_name": "web_app",
      "ha": true,
      "usage_of_with": "  student name: Tom\n  school name: Sydney Grammar\n  Male\n  ",
      "nobody": <nil>,
      "student": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "cbd": true,
            "name": "sydney",
            "postcode": 2000
          }
        },
        "name": "Tom",
        "gender": "Male",
        "teachers": {
          "tom",
          "jason",
          "alice"
        }
      },
      "template_def_consume": "\nshow example of how you can define reusable template\nand how you can pass in the parameters\n\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n",
      "template_def_consume_dynamic": "\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n\n"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"value\\n {{.usage_of_with}}\"",
        "echo \"{{.usage_of_template}}\"",
        "echo \"{{.template_def_consume}}\"",
        "echo \"{{.template_def_consume_dynamic_t1}}\"",
        "echo \"{{.template_def_consume_dynamic_t2}}\"",
        "echo \"{{.template_def_consume_dynamic_t3}}\"",
        "echo \"{{.template_def_consume_dynamic}}\"",
        "echo \"{{.template_use_block}}\""
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "pod_name": "web_app",
      "usage_of_with": "  student name: Tom\n  school name: Sydney Grammar\n  Male\n  ",
      "template_def_consume_dynamic": "\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n\n",
      "ns": "prod",
      "template_def_consume_dynamic_t2": "{{define \"T2\"}}TWO: {{.}}{{end}}",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "age": 34,
      "template_use_block": "\n\nstudent:\n  name: ONE: Tom\ngender: TWO: Male\n\n",
      "template_def_plain": "\n\n\nONE TWO\"\n",
      "template_def_consume_dynamic_main": "{{.template_def_consume_dynamic_t1}}\n{{.template_def_consume_dynamic_t2}}\n{{.template_def_consume_dynamic_t3}}\n{{template \"T3\" .student}}\n",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "ha": true,
      "old": 54,
      "nobody": <nil>,
      "student": {
        "gender": "Male",
        "teachers": {
          "tom",
          "jason",
          "alice"
        },
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom"
      },
      "template_def_consume_dynamic_t1": "{{define \"T1\"}}ONE: {{.}}{{end}}\n",
      "template_def_consume_dynamic_t3": "{{define \"T3\"}}student:\n  name: {{template \"T1\" .name}}\n  gender: {{template \"T2\" .gender}}{{end}}\n{{template \"T3\" .student}}\n",
      "usage_of_with_else": "  i am somebody  ",
      "template_def_consume": "\nshow example of how you can define reusable template\nand how you can pass in the parameters\n\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "template_def_consume_dynamic_t3": "{{define \"T3\"}}student:\n  name: {{template \"T1\" .name}}\n  gender: {{template \"T2\" .gender}}{{end}}\n{{template \"T3\" .student}}\n",
      "usage_of_with_else": "  i am somebody  ",
      "age": 34,
      "ns": "prod",
      "ha": true,
      "student": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom",
        "gender": "Male",
        "teachers": {
          "tom",
          "jason",
          "alice"
        }
      },
      "usage_of_with": "  student name: Tom\n  school name: Sydney Grammar\n  Male\n  ",
      "template_def_consume_dynamic_t1": "{{define \"T1\"}}ONE: {{.}}{{end}}\n",
      "template_def_consume_dynamic_main": "{{.template_def_consume_dynamic_t1}}\n{{.template_def_consume_dynamic_t2}}\n{{.template_def_consume_dynamic_t3}}\n{{template \"T3\" .student}}\n",
      "old": 54,
      "nobody": <nil>,
      "template_use_block": "\n\nstudent:\n  name: ONE: Tom\ngender: TWO: Male\n\n",
      "template_def_plain": "\n\n\nONE TWO\"\n",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "template_def_consume": "\nshow example of how you can define reusable template\nand how you can pass in the parameters\n\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n",
      "template_def_consume_dynamic": "\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n\n",
      "pod_name": "web_app",
      "template_def_consume_dynamic_t2": "{{define \"T2\"}}TWO: {{.}}{{end}}",
      "managers": {
        "tom",
        "jason",
        "alice"
      }
    }
    
    
    insane_banach8: overall final exec vars:
    
    (*core.Cache)({
      "usage_of_with_else": "  i am somebody  ",
      "age": 34,
      "ns": "prod",
      "ha": true,
      "student": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom",
        "gender": "Male",
        "teachers": {
          "tom",
          "jason",
          "alice"
        }
      },
      "template_def_consume_dynamic_t3": "{{define \"T3\"}}student:\n  name: {{template \"T1\" .name}}\n  gender: {{template \"T2\" .gender}}{{end}}\n{{template \"T3\" .student}}\n",
      "usage_of_with": "  student name: Tom\n  school name: Sydney Grammar\n  Male\n  ",
      "template_def_consume_dynamic_t1": "{{define \"T1\"}}ONE: {{.}}{{end}}\n",
      "template_def_consume_dynamic_main": "{{.template_def_consume_dynamic_t1}}\n{{.template_def_consume_dynamic_t2}}\n{{.template_def_consume_dynamic_t3}}\n{{template \"T3\" .student}}\n",
      "old": 54,
      "nobody": <nil>,
      "template_use_block": "\n\nstudent:\n  name: ONE: Tom\ngender: TWO: Male\n\n",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "template_def_consume": "\nshow example of how you can define reusable template\nand how you can pass in the parameters\n\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n",
      "template_def_consume_dynamic": "\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n\n",
      "pod_name": "web_app",
      "template_def_consume_dynamic_t2": "{{define \"T2\"}}TWO: {{.}}{{end}}",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "template_def_plain": "\n\n\nONE TWO\"\n"
    })
    
    cmd( 1):
    echo "value\n {{.usage_of_with}}"
    
     \_ echo "value\n   student name: Tom
      school name: Sydney Grammar
      Male
      "
    value\n   student name: Tom
      school name: Sydney Grammar
      Male
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=64) "value\\n   student name: Tom\n  school name: Sydney Grammar\n  Male",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "{{.usage_of_template}}"
    
     \_ echo "<no value>"
    <no value>
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=10) "<no value>",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "{{.template_def_consume}}"
    
     \_ echo "
    show example of how you can define reusable template
    and how you can pass in the parameters
    
    
    
    
    student:
      name: ONE: Tom
      gender: TWO: Male
    "
    show example of how you can define reusable template
    and how you can pass in the parameters
    
    
    
    
    student:
      name: ONE: Tom
      gender: TWO: Male
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=141) "show example of how you can define reusable template\nand how you can pass in the parameters\n\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo "{{.template_def_consume_dynamic_t1}}"
    
     \_ echo "{{define "T1"}}ONE: {{.}}{{end}}
    "
    {{define T1}}ONE: {{.}}{{end}}
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=30) "{{define T1}}ONE: {{.}}{{end}}",
     ErrMsg: (string) ""
    }
    
    cmd( 5):
    echo "{{.template_def_consume_dynamic_t2}}"
    
     \_ echo "{{define "T2"}}TWO: {{.}}{{end}}"
    {{define T2}}TWO: {{.}}{{end}}
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=30) "{{define T2}}TWO: {{.}}{{end}}",
     ErrMsg: (string) ""
    }
    
    cmd( 6):
    echo "{{.template_def_consume_dynamic_t3}}"
    
     \_ echo "{{define "T3"}}student:
      name: {{template "T1" .name}}
      gender: {{template "T2" .gender}}{{end}}
    {{template "T3" .student}}
    "
    {{define T3}}student:
      name: {{template T1 .name}}
      gender: {{template T2 .gender}}{{end}}
    {{template T3 .student}}
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=117) "{{define T3}}student:\n  name: {{template T1 .name}}\n  gender: {{template T2 .gender}}{{end}}\n{{template T3 .student}}",
     ErrMsg: (string) ""
    }
    
    cmd( 7):
    echo "{{.template_def_consume_dynamic}}"
    
     \_ echo "
    
    
    
    student:
      name: ONE: Tom
      gender: TWO: Male
    
    "
    student:
      name: ONE: Tom
      gender: TWO: Male
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=45) "student:\n  name: ONE: Tom\n  gender: TWO: Male",
     ErrMsg: (string) ""
    }
    
    cmd( 8):
    echo "{{.template_use_block}}"
    
     \_ echo "
    
    student:
      name: ONE: Tom
    gender: TWO: Male
    
    "
    student:
      name: ONE: Tom
    gender: TWO: Male
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=43) "student:\n  name: ONE: Tom\ngender: TWO: Male",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0039 log - verbose level v](../../logs/c0039_v)
* [c0039 log - verbose level vv](../../logs/c0039_vv)
* [c0039 log - verbose level vvv](../../logs/c0039_vvv)
* [c0039 log - verbose level vvvv](../../logs/c0039_vvvv)
* [c0039 log - verbose level vvvvv](../../logs/c0039_vvvvv)

##### References
* [Related Chapter](../../template/c0039)
