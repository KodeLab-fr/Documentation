# Exemple of function with sphinx

## Comment documenter une fonction python

## Formations
```{mermaid}
flowchart LR

%% Colors %%
classDef blue fill:#2374f7,stroke:#000,stroke-width:2px,color:#fff
classDef pink fill:#eb3dd6,stroke:#000,stroke-width:2px,color:#fff
classDef orange fill:#fc822b,stroke:#000,stroke-width:2px,color:#fff
classDef red fill:#ed2633,stroke:#000,stroke-width:2px,color:#fff
classDef green fill:#16b522,stroke:#000,stroke-width:2px,color:#fff

subgraph Formations
    Elec(Electronic):::blue
    Info(Informatique):::red
    Meca(Mecanic):::green
end

```
## Sub-Definitions
### Electronic
```{mermaid}
flowchart LR
%% Colors %%
classDef blue fill:#2374f7,stroke:#000,stroke-width:2px,color:#fff
classDef pink fill:#eb3dd6,stroke:#000,stroke-width:2px,color:#fff
classDef orange fill:#fc822b,stroke:#000,stroke-width:2px,color:#fff
classDef red fill:#ed2633,stroke:#000,stroke-width:2px,color:#fff
classDef green fill:#16b522,stroke:#000,stroke-width:2px,color:#fff

subgraph Elec
    direction LR
    subgraph First_Layer
        direction LR
        PCB(PCB):::blue
        Arduino(Arduino):::blue
        Rasp(Micro-Computer):::blue
    end
end
```

### Mecanic
```{mermaid}
flowchart LR
%% Colors %%
classDef blue fill:#2374f7,stroke:#000,stroke-width:2px,color:#fff
classDef pink fill:#eb3dd6,stroke:#000,stroke-width:2px,color:#fff
classDef orange fill:#fc822b,stroke:#000,stroke-width:2px,color:#fff
classDef red fill:#ed2633,stroke:#000,stroke-width:2px,color:#fff
classDef green fill:#16b522,stroke:#000,stroke-width:2px,color:#fff

subgraph Meca
direction LR
    subgraph First_Layer
        Modelisation(Modelisation):::green
        3D(3D Printing):::green
        CNC(CNC):::green
        Molding(Molding):::green
    end
    subgraph Neophyte
        Modelisation --> SW1(SolidWorks I, base):::green
        Modelisation --> Blender1(Blender I):::green
        3D --> FDM(FDM):::green
        3D --> PrusaSlicer(PrusaSlicer):::green
        3D --> Cura(Cura):::green
        CNC --> Laser(Laser Cutter):::green
        Molding --> InjectionI(Injection I):::green
        end
    subgraph Intermediaire
        SW1 --> SW2(SolidWorks II, Play with 2D plans):::green
        Blender1 --> Blender2(Blender II):::green
        FDM --> SLA(SLA):::green
        FDM --> Repair(Repair 3D Print):::green
        Laser --> Lathe(Engine Lathe):::green
        InjectionI --> InjectionII(Injection II):::green
    end
    subgraph COnfirmed
        SW2 --> SW3(SolidWorks III):::green
        Blender2 --> Blender3(Blender III):::green
        Lathe --> Milling(Milling Machine):::green
        Lathe --> Wood(CNC Wood):::green
        Lathe --> Iron(CNC Iron):::green
        Lathe --> InformaticLathe(CNC Lathe with Informatic):::green
        InjectionII --> InjectionIII(Injection III):::green
    end
end
```
### Informatique
```{mermaid}
flowchart
%% Colors %%
classDef blue fill:#2374f7,stroke:#000,stroke-width:2px,color:#fff
classDef pink fill:#eb3dd6,stroke:#000,stroke-width:2px,color:#fff
classDef orange fill:#fc822b,stroke:#000,stroke-width:2px,color:#fff
classDef red fill:#ed2633,stroke:#000,stroke-width:2px,color:#fff
classDef green fill:#16b522,stroke:#000,stroke-width:2px,color:#fff

subgraph Info
    direction LR
    subgraph First_Layer
        CICD(CI/CD):::blue
        Linux(Linux):::blue
        Workspace(Workspace):::blue
        AI(AI and Data):::blue
        Web(Web):::blue
        Mobile(Mobile Apps):::blue
        Games(Games):::blue
    end
    subgraph Beginner
        CICD --> MD("Documentation (Markdown)"):::blue
        CICD --> Git(Git):::blue
        CICD --> Docker(Docker):::blue
        Linux --> Docker(Docker):::blue
        Linux --> Linux1(Linux bash commands):::blue
        Workspace --> Shell(Shell):::blue
        Linux --> Shell
        Workspace --> IDE(IDE):::blue
        AI --> Py(Python and Jupyter):::blue
        AI --> SQL(SQL):::blue
        Web --> HTML(HTML):::blue
        Web --> Requests(Requests):::blue
        Mobile --> Flutter1(Flutter layer first):::blue
        Games --> C#1(C#1):::blue
    end
    subgraph Neophyte
        MD --> Latex(Latex):::blue
        MD --> Sphinx(Sphinx):::blue
        Docker --> DF(DokcerFile):::blue
        Git --> Git2(Github):::blue
        Git --> WorkTree(Git WorkTree):::blue
        Linux1 --> Linux2(Manage linux computer):::blue
        Linux1 --> Bash1(DotFiles and Bashrc):::blue
        Shell --> Bash1
        IDE --> VSC(VSCode):::blue
        IDE --> NVim(NVim):::blue
        Py --> AI1(AI first steps Machine Learning):::blue
        SQL --> CRON_SQL(CRON SQL):::blue
        HTML --> CSS(HTML/CSS):::blue
        HTML --> JS(JavaScript):::blue
        Requests --> API(API):::blue
        Requests --> Scrapping:::blue
        Flutter1 --> Flutter2(Flutter feature first with api):::blue
        Requests --> Flutter2
        C#1 --> Unity1(Unity first steps):::blue
        C#1 --> C#2(C# advanced):::blue
    end
    subgraph Intermediaire["Intermediaire"]
        Latex --> Latex2(Latex advanced - write report):::blue
        Git2 --> Mermaid(Mermaid):::blue
        Sphinx --> Mermaid
        DF --> DC(Docker Compose):::blue
        Git2 --> Git3(Git project management):::blue
        Linux2 --> Linux3(Linux advanced):::blue
        Bash1 --> zsh(ZSH):::blue
        VSC --> VSC2(VSCode extensions):::blue
        NVim --> NVim2(NVim advanced):::blue
        AI1 --> AI2(AI deep learning Mnist):::blue
        CRON_SQL --> NO_SQL(NoSQL):::blue
        JS --> JS2(JS framework):::blue
        Scrapping --> Dataset(Dataset Creation):::blue
        API --> WebAPI(Web/Json API):::blue
        API --> ServerSideEvent(Server Side Event):::blue
        CSS --> Nginx(Nginx):::blue
        JS --> WebAPI
        Flutter2 --> Flutter3(Flutter advanced):::blue
        Unity1 --> Unity3D1(3D first steps):::blue
        Unity1 --> Unity2D1(Entity management):::blue
        C#2 --> Docfx(Docfx):::blue
    end
    subgraph Confirmed
        Latex2 --> Latex3(Latex advanced - write resume):::blue
        Git3 --> Git4(Github Actions):::blue
        DC --> K8S(Kubernetes):::blue
        zsh --> OhMyZsh(OhMyZsh):::blue
        zsh --> Tmux(Tmux):::blue
        NVim2 --> NVim3(Nvim Extensions Management):::blue
        AI2 --> AI3(YOLO and fine tunning):::blue
        NO_SQL --> GraphQL(GraphQL):::blue
        NO_SQL --> GraphDB(Graph oriented Database):::blue
        Nginx --> ReverseNginx(Reverse Proxy with Nginx):::blue
        ServerSideEvent --> WebSocket(WebSocket):::blue
        Flutter3 --> Getx(Getx):::blue
        Unity2D1 --> Unity2D2(Unity2D advanced):::blue
        Unity3D1 --> Unity3D2(Unity3D advanced):::blue
        Unity3D1 --> Unity3(Management clean project):::blue
    end
end
```
intermediaire
cofirme
avance

couture et craft

