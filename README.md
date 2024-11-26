# Vimeo-RTMP-MultiAudioTrack

This repository demonstrates **a multi-language live streaming solution using Vimeo**. Separate encoders send language-specific streams to Vimeo, and a web page dynamically switches between them based on user selection.

![multiaudiolive](https://github.com/user-attachments/assets/cdd68dab-66ee-4120-be80-60e6bed9e05f)


**Key components:**

- **Multiple Encoders:** Each encoder sends a unique RTMP stream to Vimeo, containing the same video content but with different audio tracks (e.g., Language #1, Language #2, Language #3).

- **Vimeo Platform:** Vimeo ingests the streams and provides unique IDs for each.

- **Web Server:** Hosts the HTML, JavaScript, and a mapping between language selections and Vimeo stream IDs.

- **Vimeo Player:** An embedded Vimeo player on the web page displays the selected stream.

- **JavaScript Logic:** Handles user language selection and dynamically updates the Vimeo player's source URL to switch between streams.



**How does it work?**

This solution involves multiple encoders sending individual RTMP streams to Vimeo, each containing a different language audio track. Vimeo assigns unique IDs to each ingested stream. When the webpage loads, it initialises the Vimeo player and a dropdown menu for language selection. Upon selecting a language, JavaScript fetches the corresponding stream ID and updates the Vimeo player's source with the new ID, resulting in a seamless audio track switch.



https://github.com/user-attachments/assets/3f0a6550-8537-4ec6-8f23-ea18f1b5c0f8

