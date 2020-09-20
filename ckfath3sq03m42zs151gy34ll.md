## How I got C# to work with Godot (Full Tutorial)

I am a hobbyist game developer. While researching for an appropriate game engine, I finalized a few for production, namely [Unity](https://unity3d.com/get-unity/download), [Unreal](https://www.unrealengine.com/en-US/auth?state=https://www.unrealengine.com/en-US/eulacheck/publishing) *(ps, you need to make an epic ID and login with it to download)* and  [Godot](https://godotengine.org/), of which I chose to make with Godot, for more reasons than one. 

I'll talk about my reasons to choose Godot over other engines, its positives and its negatives in another blog, right now, this blog about is **only** about how did I get C# to work with Godot. *I assume you already know how to code in C# and what how to code in GDScript in Godot and now want to combine both.* I'll keep it short and crisp so that you can follow along easily and get set up and coding quickly. 

1. Download Godot [here](https://godotengine.org/)

2. Download Visual Studio Code [here](https://code.visualstudio.com/Download)
-  **(Important)** On Visual Studio Code, go to extensions and install the following extensions, namely **C#** by microsoft and **C# Extensions** by jchannon

- **(Also important)** Set these in Vscode C# Extension settings for intellisense ;
        "omnisharp.monoPath": ***(path to your mono installation. For my mac, it's located at)***"/Library/Frameworks/Mono.framework/Versions/Current/Commands/mono", 
        "omnisharp.useGlobalMono": "always",

3. Open Godot

4. Create a new project, pick a name, empty directory and choose OpenGL ES 3.0

5. Go to Editor (top bar) > Editor Settings > Mono, choose external editor

6. There's a "Create Root Node" in scene on top-left, choose 3D Scene

7. Right click newly created Spatial, choose "Attach Script"

8. Change language to C# and hit "Create" (it should open it in VS Code)

9. Open ```<ProjectName>.csproj``` 
 file from VS Code file explorer and add ```<ItemGroup><Compile Include="**\*.cs" /></ItemGroup>``` between ```<Project>``` tags, this tells the compiler to compile all your C# files (otherwise have to add 1 file at a time)

Et voila. Now any script that you attach in your godot project, as long as it is a C# script, it will work with Godot. 


------------------

Hello, I am ***Sarthak Batra***. I have been a software engineer for 6 years now but I've only just began blogging about it, so I *am* prone to errors by making it unclear or confusing. If you think this blog does NOT sufficiently explains the subject it says, reach out to me on my twitter at www.twitter.com/sarthakbatra and I'll be more than happy to help. After all, when we learn together and help each other, we all grow! 

