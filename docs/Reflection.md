## Lessons Learned 
1. We should always read the component datasheets thoroughly before making any purchases to ensure compatibility and avoid costly mistakes.

2. We discovered that setting the silk screen clearance to 0.1 mils is crucial for successful PCB fabrication.

3. Working with ESP32 microcontrollers proved to be both enjoyable and highly productive for rapid prototyping.

4. Reinforcing Ohm’s Law—voltage equals current times resistance—helped us diagnose circuit issues more effectively.

5. Implementing a structured message-passing system significantly simplified data communication between modules.

6. We learned that supply voltages can fluctuate based on the outlet and environment, so our regulator designs must accommodate these variations.

7. Individually testing every component before full system integration prevented cascading failures and saved debugging time.

8. We recognized that engineering is fundamentally about systematic problem solving and iterative improvement.

9. Including test points at every critical node on the PCB made signal measurement and fault isolation much easier.

10. Labeling every I/O pin on the board with a clear pinout diagram proved invaluable when unexpected wiring needs arose.

## Recommendations for future students

1. This class is entirely focused on problem solving, so be prepared to encounter and overcome new challenges continuously.

2. Expect to invest significantly more time in this course than in a typical three-unit class due to its hands-on nature.

3. Review weekly assignments and milestones well in advance and avoid leaving all work until the night before deadlines.

4. Use JLCPCB for your board fabrication because of its affordability, fast turnaround, and reliable quality.

5. Start developing and testing your message-passing infrastructure early, even if your PCBs have not yet arrived.

## Version 2.0

To avoid last‐minute crunches, we would establish hard deadlines for each major deliverable—message protocol definition, software driver stub, PCB layout, and integration test. Each deadline would carry a simple consequence for the team, such as shifting noncritical scope items to a later sprint, so everyone understands the trade-offs of missing a milestone. To keep us honest, we would designate a “scrum master” or leading voice whose sole responsibility is to send twice-weekly reminders and to call out approaching deadlines in our group chat. Finally, we would require that the core message‐passing routines be fully implemented and unit‐tested before the boards arrive, so software and hardware integration can begin immediately once PCBs are populated.

Debug : Use of a hardware logic‐analyzer header exposing TX, RX, CTS, and RTS signals so that we can monitor traffic in real time. A simple heartbeat LED on the board that blinks green when the link is healthy and red if a CRC or sequence error is detected.

By combining disciplined project management—strict deadlines, clear ownership, and early software completion—with a more modular, feature-rich communication stack and improved hardware support, Version 2.0 of our architecture would be far more reliable, maintainable, and scalable for future classes and projects.
