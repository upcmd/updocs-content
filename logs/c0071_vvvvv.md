---
title: "c0071_vvvvv"
date: 2020-08-18T15:16:00+88:00
draft: false
weight: 10714

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
    loading [Task]:  ./tests/functests/c0071
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc000175040)(<nil>)
    
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
      "mystory": "  Once when I was six years old I saw a magnificent picture in a book, called True Stories from Nature, about the primeval forest. It was a picture of a boa constrictor in the act of swallowing an animal. Here is a copy of the drawing.\n\n    boa constrictor swallowing an animal\n  In the book it said: \"Boa constrictors swallow their prey whole, without chewing it. After that they are not able to move, and they sleep through the six months that they need for digestion.\"\n\n  I pondered deeply, then, over the adventures of the jungle. And after some work with a colored pencil I succeeded in making my first drawing. My Drawing Number One. It looked something like this:\n\n    Drawing Number One\n    I showed my masterpiece to the grown-ups, and asked them whether the drawing frightened them.\n\n  But they answered: \"Frighten? Why should any one be frightened by a hat?\"\n\n  My drawing was not a picture of a hat. It was a picture of a boa constrictor digesting an elephant. But since the grown-ups were not able to understand it, I made another drawing: I drew the inside of a boa constrictor, so that the grown-ups could see it clearly. They always need to have things explained. My Drawing Number Two looked like this:w"
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
          "name": "writeFile",
          "desc": "write content to a file",
          "cmd": {
            "content": "{{.mystory}}",
            "filename": "mystory.txt",
            "dir": "/tmp"
          }
        },
        {
          "name": "readFile",
          "desc": "read content of a file and register it to a var",
          "cmd": {
            "filename": "mystory.txt",
            "dir": "/tmp",
            "reg": "my_interesting_story"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "mystory": "  Once when I was six years old I saw a magnificent picture in a book, called True Stories from Nature, about the primeval forest. It was a picture of a boa constrictor in the act of swallowing an animal. Here is a copy of the drawing.\n\n    boa constrictor swallowing an animal\n  In the book it said: \"Boa constrictors swallow their prey whole, without chewing it. After that they are not able to move, and they sleep through the six months that they need for digestion.\"\n\n  I pondered deeply, then, over the adventures of the jungle. And after some work with a colored pencil I succeeded in making my first drawing. My Drawing Number One. It looked something like this:\n\n    Drawing Number One\n    I showed my masterpiece to the grown-ups, and asked them whether the drawing frightened them.\n\n  But they answered: \"Frighten? Why should any one be frightened by a hat?\"\n\n  My drawing was not a picture of a hat. It was a picture of a boa constrictor digesting an elephant. But since the grown-ups were not able to understand it, I made another drawing: I drew the inside of a boa constrictor, so that the grown-ups could see it clearly. They always need to have things explained. My Drawing Number Two looked like this:w"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "mystory": "  Once when I was six years old I saw a magnificent picture in a book, called True Stories from Nature, about the primeval forest. It was a picture of a boa constrictor in the act of swallowing an animal. Here is a copy of the drawing.\n\n    boa constrictor swallowing an animal\n  In the book it said: \"Boa constrictors swallow their prey whole, without chewing it. After that they are not able to move, and they sleep through the six months that they need for digestion.\"\n\n  I pondered deeply, then, over the adventures of the jungle. And after some work with a colored pencil I succeeded in making my first drawing. My Drawing Number One. It looked something like this:\n\n    Drawing Number One\n    I showed my masterpiece to the grown-ups, and asked them whether the drawing frightened them.\n\n  But they answered: \"Frighten? Why should any one be frightened by a hat?\"\n\n  My drawing was not a picture of a hat. It was a picture of a boa constrictor digesting an elephant. But since the grown-ups were not able to understand it, I made another drawing: I drew the inside of a boa constrictor, so that the grown-ups could see it clearly. They always need to have things explained. My Drawing Number Two looked like this:w"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "mystory": "  Once when I was six years old I saw a magnificent picture in a book, called True Stories from Nature, about the primeval forest. It was a picture of a boa constrictor in the act of swallowing an animal. Here is a copy of the drawing.\n\n    boa constrictor swallowing an animal\n  In the book it said: \"Boa constrictors swallow their prey whole, without chewing it. After that they are not able to move, and they sleep through the six months that they need for digestion.\"\n\n  I pondered deeply, then, over the adventures of the jungle. And after some work with a colored pencil I succeeded in making my first drawing. My Drawing Number One. It looked something like this:\n\n    Drawing Number One\n    I showed my masterpiece to the grown-ups, and asked them whether the drawing frightened them.\n\n  But they answered: \"Frighten? Why should any one be frightened by a hat?\"\n\n  My drawing was not a picture of a hat. It was a picture of a boa constrictor digesting an elephant. But since the grown-ups were not able to understand it, I made another drawing: I drew the inside of a boa constrictor, so that the grown-ups could see it clearly. They always need to have things explained. My Drawing Number Two looked like this:w"
    })
    
    {{.mystory}}
    ~SubStep1: [print:  ]
      Once when I was six years old I saw a magnificent picture in a book, called True Stories from Nature, about the primeval forest. It was a picture of a boa constrictor in the act of swallowing an animal. Here is a copy of the drawing.
    
        boa constrictor swallowing an animal
      In the book it said: "Boa constrictors swallow their prey whole, without chewing it. After that they are not able to move, and they sleep through the six months that they need for digestion."
    
      I pondered deeply, then, over the adventures of the jungle. And after some work with a colored pencil I succeeded in making my first drawing. My Drawing Number One. It looked something like this:
    
        Drawing Number One
        I showed my masterpiece to the grown-ups, and asked them whether the drawing frightened them.
    
      But they answered: "Frighten? Why should any one be frightened by a hat?"
    
      My drawing was not a picture of a hat. It was a picture of a boa constrictor digesting an elephant. But since the grown-ups were not able to understand it, I made another drawing: I drew the inside of a boa constrictor, so that the grown-ups could see it clearly. They always need to have things explained. My Drawing Number Two looked like this:w
    map[content:{{.mystory}} dir:/tmp filename:mystory.txt]
    ~SubStep2: [writeFile: write content to a file ]
    map[dir:/tmp filename:mystory.txt reg:my_interesting_story]
    ~SubStep3: [readFile: read content of a file and register it to a var ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "mystory": "  Once when I was six years old I saw a magnificent picture in a book, called True Stories from Nature, about the primeval forest. It was a picture of a boa constrictor in the act of swallowing an animal. Here is a copy of the drawing.\n\n    boa constrictor swallowing an animal\n  In the book it said: \"Boa constrictors swallow their prey whole, without chewing it. After that they are not able to move, and they sleep through the six months that they need for digestion.\"\n\n  I pondered deeply, then, over the adventures of the jungle. And after some work with a colored pencil I succeeded in making my first drawing. My Drawing Number One. It looked something like this:\n\n    Drawing Number One\n    I showed my masterpiece to the grown-ups, and asked them whether the drawing frightened them.\n\n  But they answered: \"Frighten? Why should any one be frightened by a hat?\"\n\n  My drawing was not a picture of a hat. It was a picture of a boa constrictor digesting an elephant. But since the grown-ups were not able to understand it, I made another drawing: I drew the inside of a boa constrictor, so that the grown-ups could see it clearly. They always need to have things explained. My Drawing Number Two looked like this:w",
      "my_interesting_story": "  Once when I was six years old I saw a magnificent picture in a book, called True Stories from Nature, about the primeval forest. It was a picture of a boa constrictor in the act of swallowing an animal. Here is a copy of the drawing.\n\n    boa constrictor swallowing an animal\n  In the book it said: \"Boa constrictors swallow their prey whole, without chewing it. After that they are not able to move, and they sleep through the six months that they need for digestion.\"\n\n  I pondered deeply, then, over the adventures of the jungle. And after some work with a colored pencil I succeeded in making my first drawing. My Drawing Number One. It looked something like this:\n\n    Drawing Number One\n    I showed my masterpiece to the grown-ups, and asked them whether the drawing frightened them.\n\n  But they answered: \"Frighten? Why should any one be frightened by a hat?\"\n\n  My drawing was not a picture of a hat. It was a picture of a boa constrictor digesting an elephant. But since the grown-ups were not able to understand it, I made another drawing: I drew the inside of a boa constrictor, so that the grown-ups could see it clearly. They always need to have things explained. My Drawing Number Two looked like this:w"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "mystory": "  Once when I was six years old I saw a magnificent picture in a book, called True Stories from Nature, about the primeval forest. It was a picture of a boa constrictor in the act of swallowing an animal. Here is a copy of the drawing.\n\n    boa constrictor swallowing an animal\n  In the book it said: \"Boa constrictors swallow their prey whole, without chewing it. After that they are not able to move, and they sleep through the six months that they need for digestion.\"\n\n  I pondered deeply, then, over the adventures of the jungle. And after some work with a colored pencil I succeeded in making my first drawing. My Drawing Number One. It looked something like this:\n\n    Drawing Number One\n    I showed my masterpiece to the grown-ups, and asked them whether the drawing frightened them.\n\n  But they answered: \"Frighten? Why should any one be frightened by a hat?\"\n\n  My drawing was not a picture of a hat. It was a picture of a boa constrictor digesting an elephant. But since the grown-ups were not able to understand it, I made another drawing: I drew the inside of a boa constrictor, so that the grown-ups could see it clearly. They always need to have things explained. My Drawing Number Two looked like this:w",
      "my_interesting_story": "  Once when I was six years old I saw a magnificent picture in a book, called True Stories from Nature, about the primeval forest. It was a picture of a boa constrictor in the act of swallowing an animal. Here is a copy of the drawing.\n\n    boa constrictor swallowing an animal\n  In the book it said: \"Boa constrictors swallow their prey whole, without chewing it. After that they are not able to move, and they sleep through the six months that they need for digestion.\"\n\n  I pondered deeply, then, over the adventures of the jungle. And after some work with a colored pencil I succeeded in making my first drawing. My Drawing Number One. It looked something like this:\n\n    Drawing Number One\n    I showed my masterpiece to the grown-ups, and asked them whether the drawing frightened them.\n\n  But they answered: \"Frighten? Why should any one be frightened by a hat?\"\n\n  My drawing was not a picture of a hat. It was a picture of a boa constrictor digesting an elephant. But since the grown-ups were not able to understand it, I made another drawing: I drew the inside of a boa constrictor, so that the grown-ups could see it clearly. They always need to have things explained. My Drawing Number Two looked like this:w"
    })
    
    {{.my_interesting_story}}
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
