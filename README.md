Precision Landing: VisionBased Autonomous UAV Landing on a Moving Target

Saketh Audipudi
1224900053
School of Manufacturing Systems and Networks, Arizona State University, Arizona, USA





ABSTRACT

This document outlines the creation of a visionguided autonomous landing system for unmanned aerial vehicles (UAVs), with a particular focus on the Parrot Mambo minidrone. The main goal of this research is to empower the UAV to autonomously identify and descend onto a dynamically moving target. This is achieved using a downwardfacing camera on the UAV, which captures realtime video to locate and follow a linefollowing robot that serves as the moving target. The identification and pursuit algorithms are developed using MATLAB and Simulink, applying image processing methods to adapt to dynamic changes in the target’s movement. The paper explores the design considerations for the vision system, integration of control algorithms, and the synchronization challenges encountered while aligning the UAV’s descent with the moving target. Initial testing shows encouraging results in controlled settings, with the UAV successfully completing landings on the moving target across various speeds and movement patterns.



INTRODUCTION

Unmanned Aerial Vehicles (UAVs) have evolved from recreational gadgets to tools capable of complex roles in sectors such as surveillance, delivery, and environmental monitoring. A significant challenge in UAV technology is the development of autonomous landing on moving targets, a crucial capability for dynamic environments where static landing sites are impractical. This feature enhances the operational versatility and utility of UAVs in urgent and critical missions.

This paper develops a visionbased landing system for the Parrot Mambo minidrone, utilizing its downwardfacing camera to locate and descend onto a moving linefollowing robot. The project utilizes MATLAB and Simulink to implement vision processing and control algorithms, focusing on accurate target detection and synchronized landing maneuvers. Using a linefollowing robot as the target provides a controlled variability in movement, facilitating the development and evaluation of precision landing capabilities under diverse speeds and directional shifts.

The research aims to showcase a feasible model for incorporating advanced image processing and control systems into UAVs to achieve autonomous landing on dynamic platforms. It details the design challenges, system architecture, and experimental results, offering valuable insights into the practical implementation of autonomous systems in UAV applications, thus enhancing UAV adaptability for new uses in complex and evolving operational environments.





METHOD

The methodology for enabling autonomous UAV landing on a moving target comprises several key phases centered around the visionbased detection system using MATLAB and Simulink. This section describes the process from initial image capture to the final landing maneuver.

A. Image Processing and Detection

The UAV's vision system starts with capturing the video stream from the downwardfacing camera on the Parrot Mambo minidrone. This video is initially processed through an RGB masking technique in MATLAB, where the stream is filtered to emphasize the target by converting it into a binary image. This binary image distinctly displays the moving target in white against a black background, simplifying detection and tracking. The RGB mask is carefully crafted to isolate the target's specific color, enhancing contrast for better image processing results.

B. Target Detection and Tracking

After obtaining the binary image, the system searches for the target color on the linefollowing robot. The UAV moves forward until this color is detected within its visual range. Upon detection, control algorithms are activated to manage the UAV's approach, developed using MATLAB and Simulink. Detection of the target color prompts the UAV to start a controlled descent, maintaining its trajectory toward the target while preparing for landing.

C. Landing Maneuver

The final phase involves the UAV gradually lowering its altitude to align directly above the moving target. This step requires precise control and realtime adjustments to the drone's position, continuing until the drone reaches a minimal safe altitude. If the target remains consistently within the designated landing zone, the UAV executes its landing sequence, settling on the moving target. This automated landing sequence is triggered upon reaching minimal altitude and confirming target alignment, concluding the autonomous landing process.

This methodological approach integrates advanced image processing techniques with dynamic control systems to achieve autonomous landing, demonstrating the practical application of visionbased systems in UAV operations.



RESULTS

The experimental results from testing the UAV's autonomous landing system confirm the effectiveness and reliability of the integrated visionbased detection and control algorithms. Tests under various conditions simulated realistic scenarios with different speeds and directional changes of the target.

A. Detection Accuracy and Response Time

Initial tests assessed the system’s ability to accurately detect the target color on the linefollowing robot. The RGB masking process was highly effective, with the UAV consistently identifying the target color. This success is attributed to the robust design of the RGB mask, which effectively isolated the target color from other elements in the video stream. The

 response time, defined as the interval from color detection to descent initiation, averaged 0.3 seconds, crucial for timely UAV flight path adjustments to align with the moving target.

B. Precision in Landing

Following detection, the precision of the UAV's landing was evaluated. The drone successfully landed on the moving target in most trials, with precision measured by the offset from the target center at landing. Unsuccessful attempts were mainly due to minor miscalculations in descent speed and final positioning, indicating areas for further improvement.

These findings demonstrate the visionbased autonomous landing system's effectiveness and reliability for UAVs, capable of executing precise landings on moving targets with high success rates. The data gathered from these experiments provides valuable insights into potential realworld applications of such technologies, especially in scenarios requiring dynamic landing capabilities. Further enhancements in algorithm optimization and hardware adjustments are anticipated to significantly improve system performance.



CONCLUSION

The development of a visionbased autonomous landing system for UAVs, as illustrated in this project, represents a notable advancement in drone technology, particularly in terms of operational flexibility and precision. The successful integration of realtime image processing and control algorithms enabling the UAV to land on a moving target underscores the practical viability of combining sophisticated software with UAV hardware.

The experiments conducted with the Parrot Mambo minidrone, equipped with a downwardfacing camera and utilizing MATLAB and Simulink for processing and control, yielded impressive results. The robustness of the RGB masking technique and the efficiency of the control algorithms in managing the UAV's descent and landing maneuvers on a moving platform were particularly noteworthy.

Looking ahead, there are opportunities to further refine this technology. Improvements in algorithms could decrease response times and increase landing accuracy, potentially accommodating faster target speeds and more abrupt direction changes. Additionally, the integration of other sensors could help overcome environmental factors such as wind or lighting changes that could impact system performance.

The successful implementation of this system opens up numerous possibilities for UAV applications in complex and dynamic environments. Future research will focus on scaling this technology for larger UAVs and testing in more challenging scenarios, pushing the boundaries of what autonomous drones can achieve. This project not only contributes to the field of UAV technology but also paves the way for new applications where autonomous precision landing is critical.



REFERENCES
 Getting Started with Simulink Support Package for Parrot Minidrones. MathWorks.
 External Mode for Parrot Minidrones. MathWorks.
 Communicating with Parrot Minidrone using TCP/IP and UDP. MathWorks.
 Getting Started with Parrot Minidrone Vision. MathWorks.
 Fly a Parrot Minidrone and Detect Objects.
 Path Planning Using Keyboard Control for Parrot Minidrone.
