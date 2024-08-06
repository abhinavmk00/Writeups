#  OSI (Open Systems Interconnection) (Tryhackme)
## Assignment 4

### The OSI model consists of seven layers
![](./pics/1.png)

**Layer 7 - Application** Provides networking services directly to applications. It handles data for applications and passes it to the presentation layer.

**Layer 6 - Presentation** Translates, encrypts, and compresses data from the application layer into a standardized format. Prepares data for the session layer.

**Layer 5 - Session** Manages and maintains sessions between applications on different devices. It establishes, controls, and ends connections, ensuring smooth communication.

**Layer 4 - Transport** Chooses the transport protocol (TCP or UDP) and breaks data into segments or datagrams. Ensures reliable or faster transmission depending on the protocol used.

**Layer 3 - Network** Determines the best path to send data across the network using IP addresses. Handles logical addressing and routing.

**Layer 2 - Data Link** Adds physical MAC addresses to packets and ensures data integrity during transmission. Handles error detection and correction.

**Layer 1 - Physical** Converts binary data into electrical or optical signals for transmission over physical media and vice versa. Handles the hardware aspects of data transfer.