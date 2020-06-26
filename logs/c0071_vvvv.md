---
title: "c0071_vvvv"
date: 2020-06-27T03:09:23+66:00
draft: false
weight: 10713

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0071
                 Verbose -> vvvv
              ModuleName -> fervent_bell0
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0071
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [fervent_bell0] instance id: [dev]
    merged[ dev ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "mystory": "  Once when I was six years old I saw a magnificent picture in a book, called True Stories from Nature, about the primeval forest. It was a picture of a boa constrictor in the act of swallowing an animal. Here is a copy of the drawing.\n\n    boa constrictor swallowing an animal\n  In the book it said: \"Boa constrictors swallow their prey whole, without chewing it. After that they are not able to move, and they sleep through the six months that they need for digestion.\"\n\n  I pondered deeply, then, over the adventures of the jungle. And after some work with a colored pencil I succeeded in making my first drawing. My Drawing Number One. It looked something like this:\n\n    Drawing Number One\n    I showed my masterpiece to the grown-ups, and asked them whether the drawing frightened them.\n\n  But they answered: \"Frighten? Why should any one be frightened by a hat?\"\n\n  My drawing was not a picture of a hat. It was a picture of a boa constrictor digesting an elephant. But since the grown-ups were not able to understand it, I made another drawing: I drew the inside of a boa constrictor, so that the grown-ups could see it clearly. They always need to have things explained. My Drawing Number Two looked like this:w"
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
          "cmd": "{{.mystory}}"
        },
        {
          "name": "writefile",
          "desc": "write content to a file",
          "cmd": {
            "content": "{{.mystory}}",
            "filename": "mystory.txt",
            "dir": "/tmp"
          }
        },
        {
          "name": "readfile",
          "desc": "read content of a file and register it to a var",
          "cmd": {
            "dir": "/tmp",
            "reg": "my_interesting_story",
            "filename": "mystory.txt"
          }
        },
        {
          "name": "print",
          "cmd": "{{.my_interesting_story}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
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
      "mystory": "  Once when I was six years old I saw a magnificent picture in a book, called True Stories from Nature, about the primeval forest. It was a picture of a boa constrictor in the act of swallowing an animal. Here is a copy of the drawing.\n\n    boa constrictor swallowing an animal\n  In the book it said: \"Boa constrictors swallow their prey whole, without chewing it. After that they are not able to move, and they sleep through the six months that they need for digestion.\"\n\n  I pondered deeply, then, over the adventures of the jungle. And after some work with a colored pencil I succeeded in making my first drawing. My Drawing Number One. It looked something like this:\n\n    Drawing Number One\n    I showed my masterpiece to the grown-ups, and asked them whether the drawing frightened them.\n\n  But they answered: \"Frighten? Why should any one be frightened by a hat?\"\n\n  My drawing was not a picture of a hat. It was a picture of a boa constrictor digesting an elephant. But since the grown-ups were not able to understand it, I made another drawing: I drew the inside of a boa constrictor, so that the grown-ups could see it clearly. They always need to have things explained. My Drawing Number Two looked like this:w"
    })
    
    fervent_bell0: overall final exec vars:
    
    (*core.Cache)({
      "mystory": "  Once when I was six years old I saw a magnificent picture in a book, called True Stories from Nature, about the primeval forest. It was a picture of a boa constrictor in the act of swallowing an animal. Here is a copy of the drawing.\n\n    boa constrictor swallowing an animal\n  In the book it said: \"Boa constrictors swallow their prey whole, without chewing it. After that they are not able to move, and they sleep through the six months that they need for digestion.\"\n\n  I pondered deeply, then, over the adventures of the jungle. And after some work with a colored pencil I succeeded in making my first drawing. My Drawing Number One. It looked something like this:\n\n    Drawing Number One\n    I showed my masterpiece to the grown-ups, and asked them whether the drawing frightened them.\n\n  But they answered: \"Frighten? Why should any one be frightened by a hat?\"\n\n  My drawing was not a picture of a hat. It was a picture of a boa constrictor digesting an elephant. But since the grown-ups were not able to understand it, I made another drawing: I drew the inside of a boa constrictor, so that the grown-ups could see it clearly. They always need to have things explained. My Drawing Number Two looked like this:w"
    })
    
    ~SubStep1: [print:  ]
      Once when I was six years old I saw a magnificent picture in a book, called True Stories from Nature, about the primeval forest. It was a picture of a boa constrictor in the act of swallowing an animal. Here is a copy of the drawing.
    
        boa constrictor swallowing an animal
      In the book it said: "Boa constrictors swallow their prey whole, without chewing it. After that they are not able to move, and they sleep through the six months that they need for digestion."
    
      I pondered deeply, then, over the adventures of the jungle. And after some work with a colored pencil I succeeded in making my first drawing. My Drawing Number One. It looked something like this:
    
        Drawing Number One
        I showed my masterpiece to the grown-ups, and asked them whether the drawing frightened them.
    
      But they answered: "Frighten? Why should any one be frightened by a hat?"
    
      My drawing was not a picture of a hat. It was a picture of a boa constrictor digesting an elephant. But since the grown-ups were not able to understand it, I made another drawing: I drew the inside of a boa constrictor, so that the grown-ups could see it clearly. They always need to have things explained. My Drawing Number Two looked like this:w
    ~SubStep2: [writefile: write content to a file ]
    ~SubStep3: [readfile: read content of a file and register it to a var ]
    ~SubStep4: [print:  ]
      Once when I was six years old I saw a magnificent picture in a book, called True Stories from Nature, about the primeval forest. It was a picture of a boa constrictor in the act of swallowing an animal. Here is a copy of the drawing.
    
        boa constrictor swallowing an animal
      In the book it said: "Boa constrictors swallow their prey whole, without chewing it. After that they are not able to move, and they sleep through the six months that they need for digestion."
    
      I pondered deeply, then, over the adventures of the jungle. And after some work with a colored pencil I succeeded in making my first drawing. My Drawing Number One. It looked something like this:
    
        Drawing Number One
        I showed my masterpiece to the grown-ups, and asked them whether the drawing frightened them.
    
      But they answered: "Frighten? Why should any one be frightened by a hat?"
    
      My drawing was not a picture of a hat. It was a picture of a boa constrictor digesting an elephant. But since the grown-ups were not able to understand it, I made another drawing: I drew the inside of a boa constrictor, so that the grown-ups could see it clearly. They always need to have things explained. My Drawing Number Two looked like this:w
    
```

##### Logs with different verbose level
* [c0071 log - verbose level v](../../logs/c0071_v)
* [c0071 log - verbose level vv](../../logs/c0071_vv)
* [c0071 log - verbose level vvv](../../logs/c0071_vvv)
* [c0071 log - verbose level vvvv](../../logs/c0071_vvvv)
* [c0071 log - verbose level vvvvv](../../logs/c0071_vvvvv)

##### References
* [Related Chapter](../../cmd-func/c0071)
