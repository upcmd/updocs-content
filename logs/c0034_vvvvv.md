---
title: "c0034_vvvvv"
date: 2020-10-06T23:45:56+1010:00
draft: false
weight: 10344

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0034
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
    loading [Task]:  ./tests/functests/c0034
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc000098c20)((len=3 cap=3) {
     (impl.Scope) {
      Name: (string) (len=6) "global",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) <nil>,
      Vars: (core.Cache) (len=1) {
       (string) (len=7) "student": (map[interface {}]interface {}) (len=3) {
        (string) (len=4) "name": (string) (len=3) "Tom",
        (string) (len=6) "gender": (string) (len=4) "Male",
        (string) (len=7) "address": (map[interface {}]interface {}) (len=2) {
         (string) (len=6) "school": (string) (len=14) "Sydney Grammar",
         (string) (len=6) "suburb": (map[interface {}]interface {}) (len=3) {
          (string) (len=4) "name": (string) (len=6) "sydney",
          (string) (len=8) "postcode": (int) 2000,
          (string) (len=3) "CBD": (bool) true
         }
        }
       }
      },
      Dvars: (impl.Dvars) <nil>
     },
     (impl.Scope) {
      Name: (string) (len=7) "nonprod",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) (len=2 cap=2) {
       (string) (len=3) "dev",
       (string) (len=7) "staging"
      },
      Vars: (core.Cache) (len=4) {
       (string) (len=1) "a": (string) (len=10) "non-prod-a",
       (string) (len=1) "b": (string) (len=10) "non-prod-b",
       (string) (len=1) "c": (string) (len=10) "non-prod-c",
       (string) (len=1) "d": (string) (len=10) "non-prod-d"
      },
      Dvars: (impl.Dvars) (len=1 cap=1) {
       (impl.Dvar) {
        Name: (string) (len=6) "school",
        Value: (string) (len=132) "address:\n  suburb:\n    name: {{.student.address.suburb.name}}\n    postcode: 2000\n    CBD: yes\n  school: {{.student.address.school}}\n",
        Desc: (string) "",
        Expand: (int) 0,
        Flags: ([]string) (len=1 cap=1) {
         (string) (len=5) "toObj"
        },
        Rendered: (string) "",
        Secure: (*utils.SecureSetting)(<nil>),
        Ref: (string) "",
        RefDir: (string) "",
        DataKey: (string) "",
        DataPath: (string) "",
        DataTemplate: (string) ""
       }
      }
     },
     (impl.Scope) {
      Name: (string) (len=3) "dev",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) <nil>,
      Vars: (core.Cache) <nil>,
      Dvars: (impl.Dvars) <nil>
     }
    })
    
    [global] dvar expanded result:
    {
    }
    
    
    scope[global] merged: {
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      }
    }
    
    
    [nonprod] dvar expanded result:
    {
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      }
    }
    
    
    scope[nonprod] merged: {
      "school_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      },
      "b": "non-prod-b",
      "c": "non-prod-c",
      "d": "non-prod-d",
      "a": "non-prod-a",
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n"
    }
    
    
    ---------group vars----------
    
    nonprod: (*core.Cache)({
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_object": {
        "address": {
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        }
      },
      "b": "non-prod-b",
      "c": "non-prod-c",
      "d": "non-prod-d",
      "a": "non-prod-a"
    })
    
    
    global: (*core.Cache)({
      "student": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom",
        "gender": "Male"
      }
    })
    
    
    groups members:[dev staging]
    [dev] dvar expanded result:
    {
    }
    
    
    scope[dev] merged: {
    }
    
    
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "c": "non-prod-c",
      "d": "non-prod-d",
      "a": "non-prod-a",
      "student": {
        "gender": "Male",
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom"
      },
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_object": {
        "address": {
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        }
      },
      "b": "non-prod-b"
    })
    
    (*core.Cache)(0xc0000c8340)((len=7) {
     (string) (len=1) "b": (string) (len=10) "non-prod-b",
     (string) (len=1) "c": (string) (len=10) "non-prod-c",
     (string) (len=1) "d": (string) (len=10) "non-prod-d",
     (string) (len=1) "a": (string) (len=10) "non-prod-a",
     (string) (len=7) "student": (map[interface {}]interface {}) (len=3) {
      (string) (len=7) "address": (map[interface {}]interface {}) (len=2) {
       (string) (len=6) "suburb": (map[interface {}]interface {}) (len=3) {
        (string) (len=4) "name": (string) (len=6) "sydney",
        (string) (len=8) "postcode": (int) 2000,
        (string) (len=3) "CBD": (bool) true
       },
       (string) (len=6) "school": (string) (len=14) "Sydney Grammar"
      },
      (string) (len=4) "name": (string) (len=3) "Tom",
      (string) (len=6) "gender": (string) (len=4) "Male"
     },
     (string) (len=6) "school": (string) (len=93) "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
     (string) (len=13) "school_object": (map[interface {}]interface {}) (len=1) {
      (string) (len=7) "address": (map[interface {}]interface {}) (len=2) {
       (string) (len=6) "suburb": (map[interface {}]interface {}) (len=3) {
        (string) (len=4) "name": (string) (len=6) "sydney",
        (string) (len=8) "postcode": (int) 2000,
        (string) (len=3) "CBD": (bool) true
       },
       (string) (len=6) "school": (string) (len=14) "Sydney Grammar"
      }
     }
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "a": "non-prod-a",
      "student": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom",
        "gender": "Male"
      },
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_object": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          }
        }
      },
      "b": "non-prod-b",
      "c": "non-prod-c",
      "d": "non-prod-d"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "show_school_details"
      },
      Dox: <nil>,
      Func: "call",
      Vars: {
        "b": "local-b",
        "a": "local-a"
      },
      Dvars: {
        {
          Name: "school",
          Value: "address:\n  state: NSW\n  city: sydney\n  suburb:\n    name: {{.student.address.suburb.name}}\n    postcode: 2000\n    CBD: LOCAL\n  school: {{.student.address.school}}\nprincipal: Mr Right\n",
          Desc: "",
          Expand: 0,
          Flags: {
            "toObj"
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
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_object": {
        "address": {
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        }
      },
      "b": "local-b",
      "c": "non-prod-c",
      "up_runtime_task_layer_number": 0,
      "d": "non-prod-d",
      "a": "local-a",
      "student": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom",
        "gender": "Male"
      }
    })
    
    [local] dvar expanded result:
    {
      "school": "address:\n  state: NSW\n  city: sydney\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: LOCAL\n  school: Sydney Grammar\nprincipal: Mr Right\n",
      "school_object": {
        "address": {
          "school": "Sydney Grammar",
          "state": "NSW",
          "city": "sydney",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": "LOCAL"
          }
        },
        "principal": "Mr Right"
      }
    }
    
    
    scope[local] merged: {
      "d": "non-prod-d",
      "a": "local-a",
      "student": {
        "gender": "Male",
        "address": {
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom"
      },
      "school": "address:\n  state: NSW\n  city: sydney\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: LOCAL\n  school: Sydney Grammar\nprincipal: Mr Right\n",
      "school_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": "LOCAL"
          },
          "school": "Sydney Grammar",
          "state": "NSW",
          "city": "sydney"
        },
        "principal": "Mr Right"
      },
      "b": "local-b",
      "c": "non-prod-c",
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        }
      },
      "school": "address:\n  state: NSW\n  city: sydney\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: LOCAL\n  school: Sydney Grammar\nprincipal: Mr Right\n",
      "school_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": "LOCAL"
          },
          "school": "Sydney Grammar",
          "state": "NSW",
          "city": "sydney"
        },
        "principal": "Mr Right"
      },
      "b": "local-b",
      "c": "non-prod-c",
      "up_runtime_task_layer_number": 0,
      "d": "non-prod-d",
      "a": "local-a"
    })
    
    caller's vars to task (show_school_details)::
    (*core.Cache)({
      "d": "non-prod-d",
      "a": "local-a",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      },
      "school": "address:\n  state: NSW\n  city: sydney\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: LOCAL\n  school: Sydney Grammar\nprincipal: Mr Right\n",
      "school_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": "LOCAL"
          },
          "school": "Sydney Grammar",
          "state": "NSW",
          "city": "sydney"
        },
        "principal": "Mr Right"
      },
      "b": "local-b",
      "c": "non-prod-c",
      "up_runtime_task_layer_number": 0
    })
    
      located task-> 2 [show_school_details]: 
    =Task2: [task ==> show_school_details:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        "echo \"\"\"1.school -> {{.school}}\"\"\"",
        "echo \"\"\"2.school object CBD -> {{.school_object.address.suburb.CBD}}\"\"\"",
        "echo \"\"\"3.school object-> {{.school_object.address.school}}\"\"\"",
        "echo \"\"\"4.school object-> {{.school_object.principal}}\"\"\"",
        "echo \"\"\"5.a {{.a}}\"\"\"",
        "echo \"\"\"6.b {{.b}}\"\"\"",
        "echo \"\"\"7.school object-> {{.school_object|printObj}}\"\"\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "a": "show-school-details-a",
        "b": "show-school-details-b"
      },
      Dvars: {
        {
          Name: "class_room",
          Value: "3K",
          Desc: "",
          Expand: 0,
          Flags: <nil>,
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        },
        {
          Name: "school",
          Value: "address:\n  suburb:\n    name: {{.student.address.suburb.name}}\n    postcode: 2000\n    CBD: no\n  school: {{.student.address.school}}\nprincipal: Mr Peter\nsomething: ref task does not have this field\n",
          Desc: "",
          Expand: 0,
          Flags: {
            "toObj"
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
      "up_runtime_task_layer_number": 1,
      "d": "non-prod-d",
      "a": "local-a",
      "b": "local-b",
      "student": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom",
        "gender": "Male"
      },
      "school": "address:\n  state: NSW\n  city: sydney\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: LOCAL\n  school: Sydney Grammar\nprincipal: Mr Right\n",
      "school_object": {
        "principal": "Mr Right",
        "address": {
          "city": "sydney",
          "suburb": {
            "postcode": 2000,
            "CBD": "LOCAL",
            "name": "sydney"
          },
          "school": "Sydney Grammar",
          "state": "NSW"
        }
      },
      "c": "non-prod-c"
    })
    
    [local] dvar expanded result:
    {
      "class_room": "3K",
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\nsomething: ref task does not have this field\n",
      "school_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": false
          },
          "school": "Sydney Grammar"
        },
        "principal": "Mr Peter",
        "something": "ref task does not have this field"
      }
    }
    
    
    scope[local] merged: {
      "b": "local-b",
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\nsomething: ref task does not have this field\n",
      "school_object": {
        "something": "ref task does not have this field",
        "address": {
          "school": "Sydney Grammar",
          "state": "NSW",
          "city": "sydney",
          "suburb": {
            "postcode": 2000,
            "CBD": false,
            "name": "sydney"
          }
        },
        "principal": "Mr Peter"
      },
      "up_runtime_task_layer_number": 1,
      "d": "non-prod-d",
      "a": "local-a",
      "student": {
        "gender": "Male",
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom"
      },
      "c": "non-prod-c",
      "class_room": "3K"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "d": "non-prod-d",
      "student": {
        "address": {
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom",
        "gender": "Male"
      },
      "up_runtime_task_layer_number": 1,
      "class_room": "3K",
      "b": "local-b",
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\nsomething: ref task does not have this field\n",
      "school_object": {
        "address": {
          "city": "sydney",
          "suburb": {
            "postcode": 2000,
            "CBD": false,
            "name": "sydney"
          },
          "school": "Sydney Grammar",
          "state": "NSW"
        },
        "principal": "Mr Peter",
        "something": "ref task does not have this field"
      },
      "c": "non-prod-c",
      "a": "local-a"
    })
    
    cmd( 1):
    echo """1.school -> {{.school}}"""
    
    cmd=>:
    echo """1.school -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: no
      school: Sydney Grammar
    principal: Mr Peter
    something: ref task does not have this field
    """
    -
    1.school -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: no
      school: Sydney Grammar
    principal: Mr Peter
    something: ref task does not have this field
    
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=180) "echo \"\"\"1.school -> address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\nsomething: ref task does not have this field\n\"\"\"",
     Code: (int) 0,
     Output: (string) (len=168) "1.school -> address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\nsomething: ref task does not have this field",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo """2.school object CBD -> {{.school_object.address.suburb.CBD}}"""
    
    cmd=>:
    echo """2.school object CBD -> false"""
    -
    2.school object CBD -> false
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=39) "echo \"\"\"2.school object CBD -> false\"\"\"",
     Code: (int) 0,
     Output: (string) (len=28) "2.school object CBD -> false",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo """3.school object-> {{.school_object.address.school}}"""
    
    cmd=>:
    echo """3.school object-> Sydney Grammar"""
    -
    3.school object-> Sydney Grammar
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=43) "echo \"\"\"3.school object-> Sydney Grammar\"\"\"",
     Code: (int) 0,
     Output: (string) (len=32) "3.school object-> Sydney Grammar",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo """4.school object-> {{.school_object.principal}}"""
    
    cmd=>:
    echo """4.school object-> Mr Peter"""
    -
    4.school object-> Mr Peter
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=37) "echo \"\"\"4.school object-> Mr Peter\"\"\"",
     Code: (int) 0,
     Output: (string) (len=26) "4.school object-> Mr Peter",
     ErrMsg: (string) ""
    }
    
    cmd( 5):
    echo """5.a {{.a}}"""
    
    cmd=>:
    echo """5.a local-a"""
    -
    5.a local-a
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=22) "echo \"\"\"5.a local-a\"\"\"",
     Code: (int) 0,
     Output: (string) (len=11) "5.a local-a",
     ErrMsg: (string) ""
    }
    
    cmd( 6):
    echo """6.b {{.b}}"""
    
    cmd=>:
    echo """6.b local-b"""
    -
    6.b local-b
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=22) "echo \"\"\"6.b local-b\"\"\"",
     Code: (int) 0,
     Output: (string) (len=11) "6.b local-b",
     ErrMsg: (string) ""
    }
    
    cmd( 7):
    echo """7.school object-> {{.school_object|printObj}}"""
    
    {
      "address": {
        "school": "Sydney Grammar",
        "state": "NSW",
        "city": "sydney",
        "suburb": {
          "postcode": 2000,
          "CBD": false,
          "name": "sydney"
        }
      },
      "principal": "Mr Peter",
      "something": "ref task does not have this field"
    }
    
    {
      "something": "ref task does not have this field",
      "address": {
        "school": "Sydney Grammar",
        "state": "NSW",
        "city": "sydney",
        "suburb": {
          "CBD": false,
          "name": "sydney",
          "postcode": 2000
        }
      },
      "principal": "Mr Peter"
    }
    
    cmd=>:
    echo """7.school object-> {
      "address": {
        "school": "Sydney Grammar",
        "state": "NSW",
        "city": "sydney",
        "suburb": {
          "postcode": 2000,
          "CBD": false,
          "name": "sydney"
        }
      },
      "principal": "Mr Peter",
      "something": "ref task does not have this field"
    }
    
    """
    -
    7.school object-> {
      principal: Mr Peter,
      something: ref task does not have this field,
      address: {
        school: Sydney Grammar,
        state: NSW,
        city: sydney,
        suburb: {
          postcode: 2000,
          CBD: false,
          name: sydney
        }
      }
    }
    
    
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=295) "echo \"\"\"7.school object-> {\n  \"principal\": \"Mr Peter\",\n  \"something\": \"ref task does not have this field\",\n  \"address\": {\n    \"school\": \"Sydney Grammar\",\n    \"state\": \"NSW\",\n    \"city\": \"sydney\",\n    \"suburb\": {\n      \"postcode\": 2000,\n      \"CBD\": false,\n      \"name\": \"sydney\"\n    }\n  }\n}\n\n\"\"\"",
     Code: (int) 0,
     Output: (string) (len=250) "7.school object-> {\n  principal: Mr Peter,\n  something: ref task does not have this field,\n  address: {\n    school: Sydney Grammar,\n    state: NSW,\n    city: sydney,\n    suburb: {\n      postcode: 2000,\n      CBD: false,\n      name: sydney\n    }\n  }\n}",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0034 log - verbose level v](../../logs/c0034_v)
* [c0034 log - verbose level vv](../../logs/c0034_vv)
* [c0034 log - verbose level vvv](../../logs/c0034_vvv)
* [c0034 log - verbose level vvvv](../../logs/c0034_vvvv)
* [c0034 log - verbose level vvvvv](../../logs/c0034_vvvvv)

##### References
* [Related Chapter](../../dvars/c0034)
