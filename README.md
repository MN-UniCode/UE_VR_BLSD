# UE_VR_BLSD

**VR-BLSD** (Virtual Reality for Life-Saving Skills) was developed in collaboration with the University of Genoa for the Augmented and Virtual Reality course and it is an immersive simulation designed to teach the fundamentals of Basic Life Support and Defibrillation (BLSD). <br>
The application places users in high-fidelity emergency scenarios where they must practice recognizing cardiac arrests and operating an Automated External Defibrillator (AED). A core innovation of this project is the integration of a Conversational AI virtual instructor, which provides real-time, adaptive procedural feedback and helps users manage their emotional response during simulated panic-inducing events.

---

## Overview
The simulation strictly follows the official Basic Life Support and Defibrillation chain of survival.
The scenario begins dynamically in a public indoor environment when a virtual character collapses from sudden cardiac arrest. 
The AI tutor immediately encourages the user to step forward and begin the rescue procedure.

The simulation flow is divided into the following critical phases:
* **Step 1: Scene Safety and Victim Assessment:** The user visually inspects the area for hazards. Once safe, the user assesses the victim's responsiveness and breathing, guided dynamically by the AI tutor.
* **Step 2: Calling Emergency Services:** The AI instructs the user to alert emergency medical services.
* **Step 3: Cardiopulmonary Resuscitation (CPR):** Currently marked for future improvement, this step conceptually covers early chest compressions and rescue breaths to maintain blood flow.
* **Step 4: Early Defibrillation (AED Usage):** The user is directed to locate a public AED. The virtual guide provides verbal and visual instructions on exposing the chest, placing electrode pads, ensuring safety during rhythm analysis, and delivering a shock if advised.

---

## Technologies Used
The project leverages industry-standard tools for real-time 3D rendering and advanced conversational AI integration:
* **Unreal Engine (v5.2.1):** The core game engine used to build the immersive environment, with logic and event triggers developed entirely using Blueprints.
* **ConvAI Plugin (v4.0.0 beta 11):** Connects the Unreal Engine environment to the AI backend for real-time, low-latency voice interactions and adaptive feedback.
* **MetaHuman Plugin:** Integrates high-fidelity, realistic 3D characters for both the virtual instructor and the unconscious victim.
* **Hardware / Platforms:** Designed primarily for standalone Virtual Reality via Meta Quest headsets, but also fully supports a Desktop version (keyboard and mouse) for cross-accessibility.

---

## Configurations & Setup

> **Important Note:** This repository uses **Git Large File Storage (Git LFS)** to manage heavy assets like 3D models and textures. **You cannot simply download the .zip file from GitHub**, as the project will not work correctly.

### Prerequisites
* **Git & Git LFS:** Both must be installed on your system to correctly pull all project assets.
* **Unreal Engine 5.2.1:** The project is built specifically for this version.
* **MetaHuman Plugin:** This plugin must be installed and enabled within your Unreal Engine environment to handle the high-fidelity characters.

### Local Setup
1.  **Clone the repository** using the terminal (do not use the ZIP download):
    ```bash
    git clone https://github.com/MN-UniCode/UE_VR_BLSD.git
    ```
2.  **ConvAI Plugin:** The plugin is integrated directly into the project via LFS and is locked to the stable version used during development to prevent compatibility issues.

### ConvAI Configuration
To utilize the conversational features, an account and specific setup are required:
1.  **Account Creation:** Register on the [ConvAI Portal](https://convai.com/).
2.  **Character Setup:** Create a new character on the portal. The specific personality traits and settings used for the project's instructor can be found in the [character settings file](./docs/convai/hadley_config.json).
3.  **In-Engine Integration:**
    * Log in to the ConvAI plugin within Unreal Engine using your registered account.
    * Enter your **API Key** (this should happen automatically after login).
    * Locate the **Hadley** character in the editor and enter your new **Character ID** in the designated section.

### Interaction Modes
The simulation is designed for cross-platform accessibility:
* **Virtual Reality:** Full immersion using Meta Quest or compatible VR headsets.
* **Desktop Mode:** Interaction via standard mouse and keyboard.

---

## Project's Insights
To get a closer look at the simulation in action, including video demonstrations and deeper technical insights into our development process (such as our custom modular interaction system and conversational AI psychology design), please visit our dedicated project page:

**[https://mn-unicode.github.io/UE_VR_BLSD/](https://mn-unicode.github.io/UE_VR_BLSD/)**
