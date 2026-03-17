---
date created: mardi, mars 17 2026, 9:47:42 am
date modified: mardi, mars 17 2026, 3:56:13 pm
---
# Veritas Engineering
- Veritas pre-2020 faced issues scaling because conventions and integrations with customers (Tesla, Lucid, Snowflake) were not clear across project managers and technicians. Doing specific projects like card access, security cameras or integrating campus-wide access points were limited to specific project managers and technicians that specifically had experience in that domain.
- We were facing issues where projects e.g. card access at Tesla were delayed because they were bottlenecked by the lack of resources and people in the company knowledgeable in card access at Tesla.
- Implemented a playbook grouping all conventions and technologies for each customer. This created a database where technicians and project managers could reference conventions in one place.
- This playbook contributed to increasing Veritas' lines of business, allowing us to work on more advanced low voltage projects that were not possible before.
- This playbook allowed for rapid training of new employees and contributed to technician morale, as they felt capable on their own relying on the conventions outlined on our playbook without having to rely on senior technicians waiting on opportunities with specific project managers to learn new processes
# SRAM Research
- Radiation plays a big part in affecting device stability at the scales currently in cutting-edge manufacturing. Ions striking different areas introduce bit flips, especially when the ions hit the channel region of the transistors
- Plays a big role in space environments where there is no atmosphere
- Research on SRAM (memory) devices at the 3nm node: using Gate All Around-FET devices, we showed how we can improve existing GAA-FET transistors in manufacturing to make them more radiation-resistant.
- Using TCAD simulations, we worked on creating new BDI structures under the channel. To analogize, we had a dam where the water was leaking out of the reservoir from under the dam, and we worked on creating a solid floor under the reservoir to make sure the ground was properly sealing the water inside of the reservoir.
- Albeit, the implementation of this new BDI structure is difficult to implement in manufacturing, adding several steps in the process depending on the structure. We worked on finding the most effective structure that would require the least steps added in manufacturing, eventually finding a structure where it would only increase the time in two specific manufacturing steps already in manufacturing.
- Using BDI on a GAA-FET device increases the radiation energy needed to flip a bit, meaning it is overall more radiation resistant.
# Graduate School
- Entering graduate school in electrical engineering from a background in physics was a particularly challenging transition where expectations of knowledge and were not always met, and the culture was fundamentally different. Classes in graduate school presented the challenge of adopting new tools for a physics major that EEs had been using for the past couple years, and reaching a graduate level proficiency in a time-sensitive manner. While physics dealt with understanding theorems and applying mathematics to difficult problems in quantum mechanics, electrical engineering culture revolves towards learning tools to implement those theorems, and learning how your devices will function in their environment. It's a game of improving and comprehensively mastering all details and tangential aspects of your designs.
- Such a major shift required me to embrace a new routine where I was able to embrace electrical engineering fully. I left my job at Veritas and replaced it with an opportunity as a research assistant in the EE department where I could both learn from and build relationships with professors in the department.
- I reprioritized where my focus should be, looking to make time for transparency and open communication with my professors, going to office hours for face to face time filling in knowledge gaps. This allowed me to become engaged in their classes and created opportunities in research in their laboratories. I also became heavily engaged in IEEE, looking to build a rapport with other EE graduates as fellow students and future coworkers.

# Apple's Mission

Articulate _why_ you are drawn to hardware engineering and how your personal passion for "hard tech" aligns with Apple's mission to leave the world better than we found it

I recently had issues with my truck not correctly displaying an accurate speed, since I changed the gear ratios. I realized that the signal going to the speedometer came from a sensor in the drive train, which outputted a square wave. I took the signal and placed an arduino in between the sensor and speedometer which modified the frequency of the input to send an accurate speed value to the speedometer. I also realized this was a common issue in many friend's vehicles, where modified vehicles

VeL systems was an opportunity

# Global Manufacturing

Working with vendors from all backgrounds understanding of the global hardware supply chain (such as sourcing components like single-board computers internationally) and how you approach clear, rigorous technical documentation

# Data Tools

how you analyze data using other tools (like Python, MATLAB, or Excel)

# Semiconductor Packaging

- SiP integrates multiple integrated circuits into a single package, much smaller than a traditional PCB.
- Compared to SoCs or PCBs: shorter time-to-market, reduced assembly and test costs, improved electrical performance, better signal integrity.
- SiP assembly involves:
	  1. Squeezing solder paste onto the substrate pads, then placing passives onto the pads. The substrate passes through a multi-zone reflow oven, where the metallic connection forms to the passives
	  2. The face-up dies are then placed and epoxied onto the substrate and wire-bonded to pads on the substrate
	  3. The face-down dies use a flip-chip process with solder bumps which are melted to pads on the substrate and an underfill epoxy which helps relieve stress
	  4. Modern processes also use die-to-die interconnects which are routed in the substrate or using a silicon interposer

- I have experience in the manufacturing process with VeL systems, where I am a project manager for all of our work involving vision systems. I integrate additions to the production line for quality assurance. Our latest work with Mettler-Toledo involved detecting manufacturing defects and particles in the pipette filters down to 0.1 mm, analyzing 96 pipettes in a couple milliseconds with a trained model.
- The system then has two sides of reporting:
	1. immediate feedback to the operator which takes pictures of the filters from the vision system and draws attention to the defects it detects 
	2. a report of past data which shows number of defect types per day, heatmap of defect positions and having an acce
- I have experience in integrating circuits myself through coursework and projects, but mainly through building and racing drones. I model and 3d print frames for the drone, then source electronics (flight controllers, speed controllers, GPS, video and controller transmitters) motors, cameras, antennas, controllers, batteries and headsets.

# Collaborative Processes

ongoing research collaboration with Lawrence Livermore National Labs and SJSU as a prime example of your ability to work with a wide range of people with varying degrees of experience

Understanding but firm requirements: communication is key in building relationships.

President of the Frassati youth group
