### Game Development, Build, and Deployment Pipeline

```mermaid
flowchart TD
    subgraph "Development Process"
        A[Developer] --> B["Perforce Helix Core"]
        B -- "Commits Code & Assets" --> C["Main Repository"]
    end

    subgraph "Automated Build & CI/CD Pipeline"
        C -- "Triggers Build" --> D["CI/CD Tool: Jenkins"]
        D -- "Orchestrates" --> E["Build Servers"]
        E -- "Utilizes On-Premise Servers" --> F["On-Premise Server Farm"]
        E -- "Utilizes Cloud Services for Scaling" --> G["Cloud VMs: AWS, GCP, Azure"]
    end

    subgraph "Deployment & Live Environment"
        D -- "Runs Automated Tests" --> H["QA / Staging Environment"]
        D -- "Deploys Live Build" --> I["Global Cloud Servers"]
    end

    H -- "Manual & Final Testing" --> J["Game Ready"]
    I -- "Players Connect" --> K["The Live Game"]

    style A fill:#b3e5fc,stroke:#333,stroke-width:2px
    style K fill:#64b5f6,stroke:#333,stroke-width:2px
    style D fill:#c8e6c9,stroke:#333,stroke-width:2px
    style G fill:#fff59d,stroke:#333,stroke-width:2px
    style I fill:#ffe0b2,stroke:#333,stroke-width:2px
    style E fill:#e0e0e0,stroke:#333,stroke-width:2px
    style C fill:#cfd8dc,stroke:#333,stroke-width:2px
```


### Full-Stack JavaScript Execution Pipeline

```mermaid
flowchart TD
    %% User/Application Layer
    subgraph "1. User/Application Layer"
        A[User/Browser Request] --> B["Your Site's Code"]
        subgraph "Code Base"
            B --> C["Installed Packages"]
        end
        B -. "Uses Package Functions" .-> C
    end

    style A fill:#b3e5fc,stroke:#333,stroke-width:2px
    style C fill:#c8e6c9,stroke:#333,stroke-width:2px

    %% Runtime Environment
    subgraph "2. Runtime Environment"
        direction LR
        D["Browser JS Engine: V8"]
        E["Node.js Runtime"]
        B --> D
        B --> E
    end

    style D fill:#fff59d,stroke:#333,stroke-width:2px
    style E fill:#fff59d,stroke:#333,stroke-width:2px

    %% Operating System Layer
    subgraph "3. Operating System Layer"
        F["Operating System"] --> G["OS Kernel"]
        D -- "Makes System Calls" --> F
        E -- "Makes System Calls" --> F
    end

    style F fill:#ffe0b2,stroke:#333,stroke-width:2px
    style G fill:#ffcc80,stroke:#333,stroke-width:2px

    %% Hardware Layer
    subgraph "4. Hardware Layer"
        H["CPU"] --> I["Logic Gates & Transistors"]
        G -- "Machine Code (0s & 1s)" --> H
    end
```

### Software to Hardware Execution Pipeline (PC & Robotics)

```mermaid
flowchart TD
    %% 1. The Software Layer
    subgraph "1. The Software Layer"
        A["High-Level Software Instruction: e.g., Open a file, Move arm forward"] --> B["Your Code"]
        B -- "Uses Functions" --> C["Installed Packages"]
    end

    %% 2. The 'Brain' (Execution & Translation)
    subgraph "2. The 'Brain' (Execution & Translation)"
        subgraph "A. Standard PC"
            B --> D["Runtime Environment: JS Engine / Node.js"]
            D -- "Interprets & Executes Code" --> E["Operating System"]
            E --> F["Kernel"]
            F -- "Sends Machine Code: 0s & 1s" --> G["CPU"]
        end
        subgraph "B. Robot"
            B -- "Interprets & Executes Code" --> H["Microcontroller / Microprocessor"]
            H -- "Sends Electrical Signals" --> I["Motor Driver / Controller"]
            J["Sensors: Camera, Pressure"] -- "Provides Feedback" --> H
        end
    end

    %% 3. The Physical Components
    subgraph "3. The Physical Components"
        subgraph "A. PC Hardware"
            G --> K["Motherboard"]
            K --> L["RAM"]
            K --> M["GPU, SSD, etc."]
        end
        subgraph "B. Robot Hardware"
            I --> N["Actuators: Motors, Servos"]
        end
    end

    %% 4. The Fundamental Level
    subgraph "4. The Fundamental Level"
        G -. "Composed of" .-> O["Logic Gates"]
        O -. "Made of" .-> P["Transistors"]
        N -. "Powered by Signals from" .-> I
    end

    style A fill:#e0f7fa,stroke:#333,stroke-width:2px
    style B fill:#c8e6c9,stroke:#333,stroke-width:2px
    style C fill:#c8e6c9,stroke:#333,stroke-width:2px
    style D fill:#fff59d,stroke:#333,stroke-width:2px
    style E fill:#ffe0b2,stroke:#333,stroke-width:2px
    style F fill:#ffcc80,stroke:#333,stroke-width:2px
    style G fill:#f48fb1,stroke:#333,stroke-width:2px
    style H fill:#f48fb1,stroke:#333,stroke-width:2px
    style I fill:#f8bbd0,stroke:#333,stroke-width:2px
    style J fill:#b3e5fc,stroke:#333,stroke-width:2px
    style K fill:#cfd8dc,stroke:#333,stroke-width:2px
    style L fill:#cfd8dc,stroke:#333,stroke-width:2px
    style M fill:#cfd8dc,stroke:#333,stroke-width:2px
    style N fill:#a5d6a7,stroke:#333,stroke-width:2px
    style O fill:#e1bee7,stroke:#333,stroke-width:2px
    style P fill:#f06292,stroke:#333,stroke-width:2px
    style H fill:#f48fb1,stroke:#333,stroke-width:2px
    style I fill:#f8bbd0,stroke:#333,stroke-width:2px

    I --> J["Perform Hardware Operations"]
```

### Software to Hardware Execution Pipeline (PC & Robotics)

```mermaid
flowchart TD
    subgraph "The World of Software & Signals"
        A["Software Instruction: e.g., Rotate motor"] --> B["Runtime Environment: Translates Code"]
        B -- "Sends Electrical Signal" --> C["Microcontroller / CPU"]
    end

    subgraph "The World of Physics & Electromagnetism"
        C -- "Sends Signal to" --> D["Actuator Driver / Controller: Motor Driver"]
        D -- "Regulates Power" --> E["Electric Motor / Actuator"]
        subgraph "How a Motor Works"
            E --> F["Coil of Wire"]
            F -- "Current creates Magnetic Field" --> G["Electromagnet"]
            G -- "Repulsion & Attraction" --> H["Rotor (Spinning part)"]
            H --> I["Generates Mechanical Motion"]
        end
    end

    subgraph "The World of Sensing"
        J["Physical Property: Temperature, Light"] --> K["Sensor: Thermistor, Photodiode"]
        K -- "Converts to Electrical Signal" --> C
    end

    subgraph "The Fundamental Building Blocks"
        I --> L["Robot Arm Moves"]
        H -- "Causes" --> L
        G --> M["Physics: Electromagnetism"]
        D --> M
        C -- "Made of" --> N["Transistors"]
        N --> O["Physics: Quantum Mechanics"]
        O --> P["Control of Electrons"]
    end

    style A fill:#e0f7fa,stroke:#333,stroke-width:2px
    style B fill:#fff59d,stroke:#333,stroke-width:2px
    style C fill:#f48fb1,stroke:#333,stroke-width:2px
    style D fill:#f8bbd0,stroke:#333,stroke-width:2px
    style E fill:#a5d6a7,stroke:#333,stroke-width:2px
    style F fill:#c8e6c9,stroke:#333,stroke-width:2px
    style G fill:#c8e6c9,stroke:#333,stroke-width:2px
    style H fill:#b3e5fc,stroke:#333,stroke-width:2px
    style I fill:#81c784,stroke:#333,stroke-width:2px
    style J fill:#cfd8dc,stroke:#333,stroke-width:2px
    style K fill:#e1bee7,stroke:#333,stroke-width:2px
    style L fill:#64b5f6,stroke:#333,stroke-width:2px
    style M fill:#e6ee9c,stroke:#333,stroke-width:2px
    style N fill:#ffe0b2,stroke:#333,stroke-width:2px
    style O fill:#e0e0e0,stroke:#333,stroke-width:2px
    style P fill:#ffe0b2,stroke:#333,stroke-width:2px
```

### Docker Container Execution Pipeline

```mermaid
flowchart TD
    subgraph "The User's Command"
        A["User types: docker run ..."]
    end

    subgraph "The Docker Engine"
        B["Docker Client (Terminal)"] --> C["Docker Daemon: Processes Request"]
        C -- "Uses API" --> D["Docker API"]
    end

    subgraph "The Host OS"
        E["Host OS: Linux"] 
        F["Linux Kernel"]
        E -- "Relies on" --> F
    end

    subgraph "Core Kernel Features"
        G["Namespaces: Isolation"]
        H["Cgroups: Resource Limits"]
    end

    subgraph "The Container"
        I["Application"] --> J["Dependencies"]
        J --> K["Container Layer"]
    end

    C -- "Sends System Calls" --> F
    F -- "Utilizes" --> G
    F -- "Utilizes" --> H
    G --> K
    H --> K

    K -- "Executes" --> I
    K -- "Runs" --> J

    style A fill:#e0f7fa,stroke:#333,stroke-width:2px
    style B fill:#fff59d,stroke:#333,stroke-width:2px
    style C fill:#ffe0b2,stroke:#333,stroke-width:2px
    style E fill:#c8e6c9,stroke:#333,stroke-width:2px
    style F fill:#a5d6a7,stroke:#333,stroke-width:2px
    style G fill:#b3e5fc,stroke:#333,stroke-width:2px
    style H fill:#b3e5fc,stroke:#333,stroke-width:2px
    style I fill:#f48fb1,stroke:#333,stroke-width:2px
    style J fill:#f8bbd0,stroke:#333,stroke-width:2px
    style K fill:#e1bee7,stroke:#333,stroke-width:2px
```
