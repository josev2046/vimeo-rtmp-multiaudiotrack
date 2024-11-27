# Vimeo-RTMP-MultiAudioTrack

This repository demonstrates **a multi-language live streaming solution using Vimeo**. Separate encoders send language-specific streams to Vimeo, and a web page dynamically switches between them based on user selection.

The key components of this solution are:

- **Multiple encoders.** Each encoder sends a unique RTMP stream to Vimeo, containing the same video content but with different audio tracks, each in a different language.

- **The Vimeo platform.** Vimeo ingests the streams and provides unique IDs for each.

- **A web server.** The web server hosts the HTML, JavaScript, and a mapping between language selections and Vimeo stream IDs.

- **The Vimeo player.** An embedded Vimeo player on the web page displays the selected stream.

- **JavaScript logic.** JavaScript handles user language selection and dynamically updates the Vimeo player's source URL to switch among streams.

See Figure 1 for a diagram of the architecture.

![multiaudiolive](https://github.com/user-attachments/assets/aa58f065-e2b2-469a-b9ce-939e7d038b7e)

<p align="center">Figure 1. Diagram of a multi-language live streaming solution.</p>


When the webpage loads, it initializes the Vimeo player and displays a dropdown menu for language selection. The JavaScript fetches the stream ID corresponding to the user’s language selection during playback and updates the Vimeo player's source accordingly, resulting in a seamless audio track switch.


The following short video shows the solution in action:


https://github.com/user-attachments/assets/13a69c62-7a60-4f85-b313-32c594c8c077





