**Vimeo-RTMP-MultiAudioTrack**

This repository demonstrates a multi-language live streaming solution using Vimeo. Separate encoders send language-specific streams to Vimeo, and a web page dynamically switches between them based on user selection.

![image](https://github.com/user-attachments/assets/8762d57a-27e6-46fd-9f47-a858b561126a)


**Key components:**

**Multiple Encoders:** Each encoder sends a unique RTMP stream to Vimeo, containing the same video content but with different audio tracks (e.g., Language #1, Language #2, Language #3).

**Vimeo Platform:** Vimeo ingests the streams and provides unique IDs for each.

**Web Server:** Hosts the HTML, JavaScript, and a mapping between language selections and Vimeo stream IDs.

**Vimeo Player:** An embedded Vimeo player on the web page displays the selected stream.

**JavaScript Logic:** Handles user language selection and dynamically updates the Vimeo player's source URL to switch between streams.



**How does it work?**

**Stream Encoding:** Multiple encoders send individual RTMP streams to Vimeo, each with a different language audio track.

**Stream IDs:** Vimeo assigns unique IDs to each ingested stream.

**Web Page Loading:** The web page loads the Vimeo player and a dropdown menu for language selection.

**Language Selection:** The user selects a language from the dropdown.

**JavaScript Action:** JavaScript fetches the corresponding stream ID based on the selected language.

**Vimeo Player Update:** The Vimeo player's source is updated with the new stream ID, seamlessly switching the audio track.



https://github.com/user-attachments/assets/3f0a6550-8537-4ec6-8f23-ea18f1b5c0f8



**This solution provides:**

**Flexibility:** Easily add or remove languages by adding/removing encoders and updating the stream ID mapping.

**Scalability:** Vimeo handles the streaming infrastructure, allowing for a large number of viewers.

**User Experience:** Viewers can seamlessly switch between languages without interrupting the video stream.



**Implementation:**

**Obtain Vimeo Stream IDs:** Create live events on Vimeo for each language and obtain their unique IDs.

**Update videoIds array:** In script.js, replace the placeholder IDs (ID#1, ID#2, etc.) with your actual Vimeo stream IDs.

**Update Language Labels:** In index.html, change the language labels in the dropdown (Language #1, Language #2, etc.) to match your actual languages.

**Host the files:** Host index.html and script.js on a web server.

**Open index.html in a browser:** Access the hosted index.html file to view the multi-language live stream.

This is a basic example and can be further enhanced with features like:

**Automatic language detection:** Detect the user's browser language and pre-select the appropriate stream.

**Subtitles/Closed Captions:** Integrate subtitles or closed captions for accessibility.

**More sophisticated UI:** Improve the user interface for language selection and other controls.

**Error handling:** Implement error handling for scenarios like stream unavailability.

**Adaptive streaming:** Utilize Vimeo's adaptive streaming capabilities for optimal playback quality.
