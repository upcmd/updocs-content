---
title: "c0162_vvvvv"
date: 2020-08-18T15:16:22+88:00
draft: false
weight: 11624

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0162
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
    loading [Task]:  ./tests/functests/c0162
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001c1280)(<nil>)
    
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
        {
          "name": "print",
          "cmd": "{{.countries}}"
        },
        {
          "name": "typeOf",
          "cmd": {
            "countries",
            "friends",
            "my_friend",
            "{{.who_is_trusted}}"
          }
        },
        {
          "cmd": "type of countries: {{.countries | typeOf}}\ntype of friends: {{.friends | typeOf}}\ntype of my_friends: {{.my_friend | typeOf}}\nwho is trusted: {{.who_is_trusted |typeOf}}\n",
          "name": "print"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "my_friend": "joe doe",
        "who_is_trusted": "my_friend",
        "friends": {
          "tom",
          "jane",
          "hans",
          "coook"
        }
      },
      Dvars: {
        {
          Name: "countries",
          Value: "- Austraila\n- US\n- China\n- Japan\n",
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
      "friends": {
        "tom",
        "jane",
        "hans",
        "coook"
      },
      "my_friend": "joe doe",
      "who_is_trusted": "my_friend"
    })
    
    [local] dvar expanded result:
    {
      "countries": "- Austraila\n- US\n- China\n- Japan\n"
    }
    
    
    scope[local] merged: {
      "friends": {
        "tom",
        "jane",
        "hans",
        "coook"
      },
      "countries": "- Austraila\n- US\n- China\n- Japan\n",
      "my_friend": "joe doe",
      "who_is_trusted": "my_friend"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "my_friend": "joe doe",
      "who_is_trusted": "my_friend",
      "friends": {
        "tom",
        "jane",
        "hans",
        "coook"
      },
      "countries": "- Austraila\n- US\n- China\n- Japan\n"
    })
    
    {{.countries}}
    ~SubStep1: [print:  ]
    - Austraila
    - US
    - China
    - Japan
    
    [countries friends my_friend {{.who_is_trusted}}]
    ~SubStep2: [typeOf:  ]
     1 -  type of [countries] > [string]
     2 -  type of [friends] > [[]interface {}]
     3 -  type of [my_friend] > [string]
     4 -  type of [my_friend] > [string]
    type of countries: {{.countries | typeOf}}
    type of friends: {{.friends | typeOf}}
    type of my_friends: {{.my_friend | typeOf}}
    who is trusted: {{.who_is_trusted |typeOf}}
    
    ~SubStep3: [print:  ]
    type of countries: string
    type of friends: []interface {}
    type of my_friends: string
    who is trusted: string
    
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "hello: {{.my_friend}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "my_friend": "john"
      },
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "{{.my_friend |typeIs \"string\"}}",
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
      "my_friend": "john"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "my_friend": "john"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "my_friend": "john"
    })
    
    hello: {{.my_friend}}
    ~SubStep1: [print:  ]
    hello: john
    
```

##### Logs with different verbose level
* [c0162 log - verbose level v](../../logs/c0162_v)
* [c0162 log - verbose level vv](../../logs/c0162_vv)
* [c0162 log - verbose level vvv](../../logs/c0162_vvv)
* [c0162 log - verbose level vvvv](../../logs/c0162_vvvv)
* [c0162 log - verbose level vvvvv](../../logs/c0162_vvvvv)

##### References
* [Related Chapter](../../template/c0162)
