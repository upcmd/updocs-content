---
title: "c0036_vvvvv"
date: 2020-10-07T00:11:06+1010:00
draft: false
weight: 10364

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0036
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
    loading [Task]:  ./tests/functests/c0036
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001e5fa0)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "ns": "prod",
      "old": 54,
      "fieldnames": {
        "name-with-dash": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n"
      },
      "pod_name": "web_app",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "ha": true,
      "where_is_my_deploy": "pod_name",
      "age": 34
    })
    
    (*core.Cache)(0xc0001269f0)((len=9) {
     (string) (len=18) "where_is_my_deploy": (string) (len=8) "pod_name",
     (string) (len=2) "ha": (bool) true,
     (string) (len=3) "old": (int) 54,
     (string) (len=8) "pod_name": (string) (len=7) "web_app",
     (string) (len=3) "age": (int) 34,
     (string) (len=2) "ns": (string) (len=4) "prod",
     (string) (len=8) "managers": ([]interface {}) (len=3 cap=3) {
      (string) (len=3) "tom",
      (string) (len=5) "jason",
      (string) (len=5) "alice"
     },
     (string) (len=6) "admins": ([]interface {}) (len=3 cap=3) {
      (string) (len=3) "tom",
      (string) (len=5) "jason",
      (string) (len=5) "alice"
     },
     (string) (len=10) "fieldnames": (map[string]interface {}) (len=1) {
      (string) (len=14) "name-with-dash": (string) (len=148) "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n"
     }
    })
    
    dvar> var_with_range:
    " x  x  x "
    
    -
     x  x  x 
    dvar> var_with_range_item:
    " tom  jason  alice "
    
    -
     tom  jason  alice 
    dvar> var_with_range_item_simpler:
    " tom  jason  alice "
    
    -
     tom  jason  alice 
    dvar> var_test_log_auto_print:
    "prodweb_app"
    
    -
    prodweb_app
    dvar[object]> var_test_log_auto_print_object:
    "prodweb_app"
    
    dvar> var_with_and:
    "web_app"
    
    -
    web_app
    dvar> var_slice_index:
    "jason"
    
    -
    jason
    dvar> out_of_normal_field_name:
    "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n"
    
    -
    this_is_a_field_with_dash: you will have to use index func to access the field
    note: direct access this field will trigger template rendering error
    
    dvar> indirect_var_reference:
    "None"
    
    -
    None
    dvar> var_slice:
    "[jason]"
    
    -
    [jason]
    dvar> var_equal:
    "false"
    
    -
    false
    dvar> var_not_equal:
    "true"
    
    -
    true
    dvar> var_not_equal_another_way:
    "true"
    
    -
    true
    dvar> var_greater:
    "false"
    
    -
    false
    dvar> var_greater_and_equal:
    "true"
    
    -
    true
    dvar> var_greater_and_equal:
    "hello"
    
    -
    hello
    dvar> var_use_and_operator:
    "true"
    
    -
    true
    dvar> var_use_or_operator:
    "true"
    
    -
    true
    dvar> var_concat_values:
    "web_app: 34 years old"
    
    -
    web_app: 34 years old
    dvar> template_def:
    "\n\n\nONE TWO\"\n"
    
    -
    
    
    
    ONE TWO"
    
    [runtime global] dvar expanded result:
    {
      "var_with_print": "prodweb_app",
      "template_def": "\n\n\nONE TWO\"\n",
      "var_commented": " prod-web_app",
      "var_with_range": " x  x  x ",
      "var_with_range_item_simpler": " tom  jason  alice ",
      "var_with_and": "web_app",
      "var_space_trimmed": "prod-web_app",
      "var_commented_trimmed": "prod-web_app",
      "var_with_if": "prod-web_app-HA",
      "var_with_ifelse_multilines": "  prod-web_app-HA ",
      "out_of_normal_field_name": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n",
      "var_use_and_operator": "true",
      "var_use_or_operator": "true",
      "var_with_ifelse": "prod-web_app-HA",
      "var_test_log_auto_print_object": "prodweb_app",
      "var_slice": "[jason]",
      "var_with_or": "prod",
      "var_slice_index": "jason",
      "var_equal": "false",
      "var_greater": "false",
      "var_greater_and_equal": "hello",
      "instance_full_name": "prod-web_app",
      "var_with_range_item": " tom  jason  alice ",
      "var_length": "12",
      "var_concat_values": "web_app: 34 years old",
      "var_space_not_trimmed": "prod       -            web_app",
      "var_with_not_object": "prod-web_app",
      "var_not_equal_another_way": "true",
      "var_not_equal": "true",
      "var_with_not": "prod-web_app",
      "var_test_log_auto_print": "prodweb_app",
      "indirect_var_reference": "None"
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "var_with_and": "web_app",
      "var_with_ifelse_multilines": "  prod-web_app-HA ",
      "var_commented": " prod-web_app",
      "out_of_normal_field_name": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n",
      "var_space_trimmed": "prod-web_app",
      "var_with_not": "prod-web_app",
      "template_def": "\n\n\nONE TWO\"\n",
      "instance_full_name": "prod-web_app",
      "var_slice_index": "jason",
      "var_not_equal": "true",
      "var_with_print": "prodweb_app",
      "var_with_or": "prod",
      "age": 34,
      "var_greater_and_equal": "hello",
      "var_equal": "false",
      "var_with_range_item_simpler": " tom  jason  alice ",
      "var_with_ifelse": "prod-web_app-HA",
      "var_slice": "[jason]",
      "ns": "prod",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "var_test_log_auto_print": "prodweb_app",
      "var_test_log_auto_print_object": "prodweb_app",
      "indirect_var_reference": "None",
      "var_not_equal_another_way": "true",
      "ha": true,
      "var_with_range_item": " tom  jason  alice ",
      "var_with_not_object": "prod-web_app",
      "var_with_range": " x  x  x ",
      "var_use_or_operator": "true",
      "var_commented_trimmed": "prod-web_app",
      "var_length": "12",
      "where_is_my_deploy": "pod_name",
      "var_with_if": "prod-web_app-HA",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "pod_name": "web_app",
      "var_space_not_trimmed": "prod       -            web_app",
      "var_greater": "false",
      "var_concat_values": "web_app: 34 years old",
      "var_use_and_operator": "true",
      "fieldnames": {
        "name-with-dash": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n"
      },
      "old": 54
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"{{.instance_full_name}}\"",
        "echo \"{{.var_space_not_trimmed}}\"",
        "echo \"{{.var_space_trimmed}}\"",
        "echo \"{{.var_commented}}\"",
        "echo \"{{.var_commented_trimmed}}\"",
        "echo \"{{.var_with_if}}\"",
        "echo \"{{.var_with_ifelse}}\"",
        "echo \"{{.var_with_ifelse_multilines}}\"",
        "echo \"{{.var_with_not}}\"",
        "echo \"{{.var_with_not_object}}\"",
        "echo \"{{.var_length}}\"",
        "echo \"{{.var_with_or}}\"",
        "echo \"{{.var_with_print}}\"",
        "echo \"check the value of other dvar using vvvv flag print out\""
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
      "var_slice_index": "jason",
      "var_with_not_object": "prod-web_app",
      "var_greater": "false",
      "pod_name": "web_app",
      "var_space_not_trimmed": "prod       -            web_app",
      "fieldnames": {
        "name-with-dash": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n"
      },
      "var_with_ifelse_multilines": "  prod-web_app-HA ",
      "var_greater_and_equal": "hello",
      "out_of_normal_field_name": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n",
      "var_with_ifelse": "prod-web_app-HA",
      "var_length": "12",
      "var_space_trimmed": "prod-web_app",
      "var_not_equal_another_way": "true",
      "var_use_and_operator": "true",
      "age": 34,
      "var_slice": "[jason]",
      "where_is_my_deploy": "pod_name",
      "var_with_if": "prod-web_app-HA",
      "ha": true,
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "var_commented_trimmed": "prod-web_app",
      "ns": "prod",
      "var_with_and": "web_app",
      "var_commented": " prod-web_app",
      "template_def": "\n\n\nONE TWO\"\n",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "var_with_or": "prod",
      "up_runtime_task_layer_number": 0,
      "var_test_log_auto_print_object": "prodweb_app",
      "var_equal": "false",
      "old": 54,
      "var_not_equal": "true",
      "indirect_var_reference": "None",
      "var_with_range_item": " tom  jason  alice ",
      "var_with_range": " x  x  x ",
      "var_with_range_item_simpler": " tom  jason  alice ",
      "var_use_or_operator": "true",
      "var_concat_values": "web_app: 34 years old",
      "var_with_not": "prod-web_app",
      "instance_full_name": "prod-web_app",
      "var_with_print": "prodweb_app",
      "var_test_log_auto_print": "prodweb_app"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "age": 34,
      "var_slice_index": "jason",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "var_with_if": "prod-web_app-HA",
      "template_def": "\n\n\nONE TWO\"\n",
      "where_is_my_deploy": "pod_name",
      "var_length": "12",
      "instance_full_name": "prod-web_app",
      "var_concat_values": "web_app: 34 years old",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "var_greater_and_equal": "hello",
      "var_with_ifelse": "prod-web_app-HA",
      "var_space_trimmed": "prod-web_app",
      "old": 54,
      "out_of_normal_field_name": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n",
      "var_with_range": " x  x  x ",
      "var_space_not_trimmed": "prod       -            web_app",
      "var_with_not_object": "prod-web_app",
      "var_use_or_operator": "true",
      "var_with_or": "prod",
      "var_commented_trimmed": "prod-web_app",
      "var_with_not": "prod-web_app",
      "var_test_log_auto_print_object": "prodweb_app",
      "var_not_equal": "true",
      "var_test_log_auto_print": "prodweb_app",
      "ha": true,
      "var_with_range_item": " tom  jason  alice ",
      "var_with_and": "web_app",
      "var_with_ifelse_multilines": "  prod-web_app-HA ",
      "var_not_equal_another_way": "true",
      "var_commented": " prod-web_app",
      "pod_name": "web_app",
      "ns": "prod",
      "var_slice": "[jason]",
      "var_with_range_item_simpler": " tom  jason  alice ",
      "var_greater": "false",
      "indirect_var_reference": "None",
      "var_with_print": "prodweb_app",
      "var_use_and_operator": "true",
      "fieldnames": {
        "name-with-dash": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n"
      },
      "var_equal": "false"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "pod_name": "web_app",
      "var_with_and": "web_app",
      "var_space_not_trimmed": "prod       -            web_app",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "var_with_or": "prod",
      "ha": true,
      "old": 54,
      "var_equal": "false",
      "var_with_not_object": "prod-web_app",
      "var_with_ifelse_multilines": "  prod-web_app-HA ",
      "var_not_equal_another_way": "true",
      "var_with_not": "prod-web_app",
      "var_commented_trimmed": "prod-web_app",
      "var_greater_and_equal": "hello",
      "var_with_range": " x  x  x ",
      "instance_full_name": "prod-web_app",
      "var_greater": "false",
      "var_with_if": "prod-web_app-HA",
      "var_test_log_auto_print_object": "prodweb_app",
      "var_not_equal": "true",
      "var_slice_index": "jason",
      "var_length": "12",
      "var_use_or_operator": "true",
      "indirect_var_reference": "None",
      "fieldnames": {
        "name-with-dash": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n"
      },
      "ns": "prod",
      "out_of_normal_field_name": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n",
      "var_space_trimmed": "prod-web_app",
      "up_runtime_task_layer_number": 0,
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "var_with_print": "prodweb_app",
      "var_with_range_item": " tom  jason  alice ",
      "var_use_and_operator": "true",
      "where_is_my_deploy": "pod_name",
      "var_test_log_auto_print": "prodweb_app",
      "var_commented": " prod-web_app",
      "template_def": "\n\n\nONE TWO\"\n",
      "age": 34,
      "var_slice": "[jason]",
      "var_with_range_item_simpler": " tom  jason  alice ",
      "var_concat_values": "web_app: 34 years old",
      "var_with_ifelse": "prod-web_app-HA"
    })
    
    cmd( 1):
    echo "{{.instance_full_name}}"
    
    cmd=>:
    echo "prod-web_app"
    -
    prod-web_app
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"prod-web_app\"",
     Code: (int) 0,
     Output: (string) (len=12) "prod-web_app",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "{{.var_space_not_trimmed}}"
    
    cmd=>:
    echo "prod       -            web_app"
    -
    prod       -            web_app
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=38) "echo \"prod       -            web_app\"",
     Code: (int) 0,
     Output: (string) (len=31) "prod       -            web_app",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "{{.var_space_trimmed}}"
    
    cmd=>:
    echo "prod-web_app"
    -
    prod-web_app
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"prod-web_app\"",
     Code: (int) 0,
     Output: (string) (len=12) "prod-web_app",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo "{{.var_commented}}"
    
    cmd=>:
    echo " prod-web_app"
    -
     prod-web_app
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=20) "echo \" prod-web_app\"",
     Code: (int) 0,
     Output: (string) (len=12) "prod-web_app",
     ErrMsg: (string) ""
    }
    
    cmd( 5):
    echo "{{.var_commented_trimmed}}"
    
    cmd=>:
    echo "prod-web_app"
    -
    prod-web_app
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"prod-web_app\"",
     Code: (int) 0,
     Output: (string) (len=12) "prod-web_app",
     ErrMsg: (string) ""
    }
    
    cmd( 6):
    echo "{{.var_with_if}}"
    
    cmd=>:
    echo "prod-web_app-HA"
    -
    prod-web_app-HA
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=22) "echo \"prod-web_app-HA\"",
     Code: (int) 0,
     Output: (string) (len=15) "prod-web_app-HA",
     ErrMsg: (string) ""
    }
    
    cmd( 7):
    echo "{{.var_with_ifelse}}"
    
    cmd=>:
    echo "prod-web_app-HA"
    -
    prod-web_app-HA
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=22) "echo \"prod-web_app-HA\"",
     Code: (int) 0,
     Output: (string) (len=15) "prod-web_app-HA",
     ErrMsg: (string) ""
    }
    
    cmd( 8):
    echo "{{.var_with_ifelse_multilines}}"
    
    cmd=>:
    echo "  prod-web_app-HA "
    -
      prod-web_app-HA 
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=25) "echo \"  prod-web_app-HA \"",
     Code: (int) 0,
     Output: (string) (len=15) "prod-web_app-HA",
     ErrMsg: (string) ""
    }
    
    cmd( 9):
    echo "{{.var_with_not}}"
    
    cmd=>:
    echo "prod-web_app"
    -
    prod-web_app
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"prod-web_app\"",
     Code: (int) 0,
     Output: (string) (len=12) "prod-web_app",
     ErrMsg: (string) ""
    }
    
    cmd(10):
    echo "{{.var_with_not_object}}"
    
    cmd=>:
    echo "prod-web_app"
    -
    prod-web_app
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"prod-web_app\"",
     Code: (int) 0,
     Output: (string) (len=12) "prod-web_app",
     ErrMsg: (string) ""
    }
    
    cmd(11):
    echo "{{.var_length}}"
    
    cmd=>:
    echo "12"
    -
    12
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=9) "echo \"12\"",
     Code: (int) 0,
     Output: (string) (len=2) "12",
     ErrMsg: (string) ""
    }
    
    cmd(12):
    echo "{{.var_with_or}}"
    
    cmd=>:
    echo "prod"
    -
    prod
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=11) "echo \"prod\"",
     Code: (int) 0,
     Output: (string) (len=4) "prod",
     ErrMsg: (string) ""
    }
    
    cmd(13):
    echo "{{.var_with_print}}"
    
    cmd=>:
    echo "prodweb_app"
    -
    prodweb_app
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"prodweb_app\"",
     Code: (int) 0,
     Output: (string) (len=11) "prodweb_app",
     ErrMsg: (string) ""
    }
    
    cmd(14):
    echo "check the value of other dvar using vvvv flag print out"
    
    cmd=>:
    echo "check the value of other dvar using vvvv flag print out"
    -
    check the value of other dvar using vvvv flag print out
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=62) "echo \"check the value of other dvar using vvvv flag print out\"",
     Code: (int) 0,
     Output: (string) (len=55) "check the value of other dvar using vvvv flag print out",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0036 log - verbose level v](../../logs/c0036_v)
* [c0036 log - verbose level vv](../../logs/c0036_vv)
* [c0036 log - verbose level vvv](../../logs/c0036_vvv)
* [c0036 log - verbose level vvvv](../../logs/c0036_vvvv)
* [c0036 log - verbose level vvvvv](../../logs/c0036_vvvvv)

##### References
* [Related Chapter](../../template/c0036)
