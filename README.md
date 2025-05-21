# CoRAL : Collaborative Robotic Aquatic Laboratory
Traditional methods of coral reef monitoring, such as diver-based surveys and airborne observatories, are costly, time-consuming, and pose significant risks to human operators. By integrating advanced technologies, such as autonomous surface and underwater vehicles, drone operations, and learning algorithms, our innovative robotic team overcomes these limitations, enabling high-resolution data collection and analysis across various depths and altitudes. This comprehensive approach is essential for understanding the complex dynamics of coral bleaching and its impact on marine biodiversity.
Our closed-loop approach allows for iterative improvements in experimental design and reduction of model uncertainties, leading to more accurate and efficient monitoring of coral reefs.


![image](https://github.com/user-attachments/assets/2156b735-ef3f-4663-aaa5-f18e4437f326)

Figure 2: Our proposed innovation, CoRAL mitigates limitations of current state of the art in coral reef monitoring by integrating vertical profiling robotic boat, underwater drone, aerial imagers, in a mixed-initiative paradigm for collaborative multi-experiment campaigns. 

Context of innovation: 
We have developed a collaborative robotic system for coral reef mapping and monitoring, capable of learning from and operating with expert ecologists and conservationists in the loop. Besides enabling multi-spectral and spectroscopic imaging at scale, the system will also be capable of optimal retrieval of water and coral samples, and can potentially assist in intervention operations such as planting of new corals, or establishment of artificial reefs. We are motivated by the fact that our understanding of the aquatic world is limited, in spite of the fact that more than 70% of earth's surface is covered by water. The constraints in our knowledge of dynamics of events such as coral bleaching and their impact on marine biodiversity can be attributed to difficulty in sampling the underwater environments at high spatial and temporal resolutions and scales. To monitor coral reefs that serve as critical components in maintaining marine biodiversity, reef ecologists carry out hazardous and expensive diving operations with diver propulsion vehicles to inspect and map reefs, often with onboard light sources and spectrometers. Airborne observatories such as the ASU Global Airborne Observatory (GAO) can map reefs from an altitude of about two kilometers. Robotics technologies are enabling reduction of costs, and increase of scale, for such operations. However, new innovations in sensing, automation, and learning are needed to embed robot teams effectively with human experts for marine conservation.

![image](https://github.com/user-attachments/assets/c0c40818-8ccb-44b7-a26b-063ec1e6a6a3)

Figure 3: Closing the loop on exploration of marine and coastal ecosystems may require life-long learning and model improvements for the robotic assets and AI tools, to adapt to varying environmental process dynamics 
Our proposed system will dramatically augment existing capabilities by enabling periodic autonomous revisitation and mapping of coral reefs and their local biogeochemistry. We are testing autonomous systems that span from a depth of 100 meters covering the photic zone, to an altitude of 100m for synoptic imaging of reefs. The proposed system to be carried forward to deployment and evaluation, consists of next generation autonomous surface and underwater vehicles, and an airborne projectile imaging system, and capability of drone operation where FAA permits allow. Our innovation, the robotic coral health mapping and intervention team, will leverage our ongoing research activities at SESE and GFL addressing the following three themes – a) lowering the barrier to entry to earth ecosystems monitoring, b) continuous learning systems that close the loop on data collection and analysis leveraging Bayesian optimization c) low-cost integrated open-source hardware sensing and computational ecosystem that make our innovations accessible to the general public.

Our innovation will allow us to close the loop on data collection, data analysis, expert introspection, learning, experimental design, and overall reduction of model uncertainties iteratively. 
The outcome of additional support from ASU or investors will be both technologies accessible to individual researchers and small teams, as well as integration of operations with mapping vehicles such as the GAO that carries out imaging spectroscopy of coral reefs from the air. A key novelty in our approach is the tight integration of hardware and software, with learning algorithms in the loop to address both the dynamics of the environment, and the robot team, for optimal knowledge acquisition and assimilation. For instance, the underwater drone developed with students, has the perception and avionics hardware and software components in place to be able to follow a diver, while registering regions of interest [9]. The robotic boat has been designed with the deployment and recovery of the underwater drone as an objective, while carrying out vertical profiling of the water column with a winched sonde system [10].
Description of Innovation: 
Our collaborative system consists of three main networked assets in the field, backed by high-end servers for AI-based model training and improvement, and mission simulations prior to field deployments. 
Robotic boat: Custom autonomous surface vessel codenamed ‘Robo-boat-o’, with two designs, one with fiberglass pontoons, the other portable design with buoy floats. Avionics package consists of a Pixhawk 4 flight controller running the PX4 flight stack, GPS, and a compass. Onboard compute is an Intel NUC i7, running ROS1 (transitioning to ROS2). A custom winching system controllable by flight controller, allows vertical profiling with a water quality sonde. Initial experiments have been carried out at Tempe Town Lake and Bermuda Institute of Ocean Sciences. A 4S Lithium Iron-Phosphate battery operates the system for 3-6 hours of operation, extendable to many days through optimal scheduling of missions. A sonar range depth sensor helps in autonomous bathymetric mapping. 




![image](https://github.com/user-attachments/assets/01255b10-2bf5-4ea1-8496-3e54a0d92abf)

Figure 4: Robo-boat-o evolutions starting with 2019 (left), and 2022 (center, right)

![image](https://github.com/user-attachments/assets/c2214de6-8d0a-436d-9b88-531c4a2df914)

Figure 5: ASU graduate student operating robo-boat-o at The Lakes (south Tempe), with a water quality sonde hanging at a depth of 0.5m. At that time in 2021, the boat did not have a winching system. Right panel shows various water quality parameters captured in real time by the boat computer, during the mission by the dock. 
Robo-boat-o test footage at The Lakes: https://www.youtube.com/watch?v=Wey2bst0cBY
Underwater drone: Custom autonomous underwater vehicle (AUV) codenamed ‘uDrone’, capable of operating tethered or untethered in tandem with the board. Tether allows tighter communication, especially during testing of new science autonomy algorithms, and guidance, navigation, and control tuning. However, tetherless operation is desirable for most field experiments. Onboard compute is chosen between an Intel NUC i7 with neural compute stick for machine vision, or a Jetson TX2 and a Celeron x86 compute together. Forward facing Intel Realsense T265 with stereo gray cameras with fisheye lens, and an RGB HD camera forms the vision package. Imagery is processed by onboard compute, along with state-estimation by the flight controller (INS), for visual-inertial odometry, and semantic SLAM. 


![image](https://github.com/user-attachments/assets/47905167-3245-42ad-a40f-4bcd8e650cd7)

Figure 6: uDrone design evolutions between 2020 [10] and 2023. The vehicle has been developed at Das home pool, and tested in Bermuda, with further testing planned in Hawaii if funds permit. 
Both the robotic boat and the underwater drone run stacked controllers, capable of position and velocity control for the boat, and position, velocity, attitude, and attitude rate control for the underwater drone. The vehicles communicate using MAVLink protocol, and networked using ROS.

![image](https://github.com/user-attachments/assets/7421add5-f83a-42a9-9a27-6e2771a10a56)

Figure 7: Footage from onboard cameras of uDrone (2023) vision system. The drone was being tested in Das’ pool. 
The underwater drone is primarily designed to follow terrain while carrying out semantic mapping of coral systems. The robotic boat can concurrently carry out sampling of the water column. 
Video footages:
	2020: https://www.youtube.com/watch?v=sM6XzXgjIlo
2022: https://www.youtube.com/watch?v=zxxR6npl8X8&t=2s 
2023: 
Internal cameras: https://youtu.be/JJ8X70HSR94
External test footage: https://www.youtube.com/shorts/YMnUrwg8ljE

ExoCam-aqua imager:  An extension of an ExoCam probe concept (NASA Flight Opportunities) with a GoPro MAX360 camera, can allow aerial synoptic imaging, as well as underwater imaging, without the need of a drone. It is good to avoid drone usage to the extent possible to avoid FAA permit requirements, however, when permissible, drone can be operated autonomously by the robotic boat that serves as a hub laboratory. The boat, in certain manifestations, can collect optimal water samples adaptively, using predictive models that consume realtime water quality measurements. 
Software ecosystem: 
Field operations are enabled by use of servers on the cloud, that runs OpenUAV collaborative mission simulation, and DeepGIS collaborative annotation and introspection tools (Figure 2). 



![image](https://github.com/user-attachments/assets/1379dcb9-9258-43fd-a466-4f60fe62c317)

Figure 8: Semantic mapping of aquatic features on image this capability, combined with robotics ‘tracking by detection’ algorithms enable estimation of 3D semantic mapping of features, for informative autonomous surveys, optimized for sampling efficiency. Data courtesy Gregg,WHOI, through Trembath-Reichert. 


![image](https://github.com/user-attachments/assets/b4282c31-7f3a-47db-9978-754079f1ae98)

Figure 9: Masters thesis work by collaborator Harish Anand, showing digital twin environments of reef systems, generated using reefs mapped using diver-held cameras and structure from motion algorithms [11]. 


![image](https://github.com/user-attachments/assets/250c6b88-11c9-437c-8f26-2f9d2b154b17)

Figure 10: DREAMS Lab member Antervedi et al, published work on autonomous terrain-relative reef mapping while following divers [9]. 

Funding sources and Acknowledgements: 
NSF CNS 1521617
NASA Flight Opportunities Tech Flights Lunar Lander Exocam 
Das personal funds 
Earth Innovation Hub pool facilities 

Usage rights: 

The hardware technology and bulk of software (DeepGIS and OpenUAV) will remain open-source for non-commercial and academic usage, except aspects that involve spectroscopy, and image processing. 

Media: 



![image](https://github.com/user-attachments/assets/468ae12c-2cb1-44f2-b005-1d4e55a65f94)

Photographs taken in Bermuda during a workshop for 14-16 year old students for Bermuda Institute of Ocean Sciences (BIOS) MARINE initiative. Picture shows Robo-boat-o next to a reef system, with co-inventors Rodney Staggers Jr. (top) and Aravind Adith PS (bottom)
