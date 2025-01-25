# Narration of the Holy Bible (Vamvas Greek Translation)

## Making It Available

This repository provides a narration of the Vamvas Greek Translation.

Special thanks to **Jean Baltatzis** for reading Greek text and to **Angelos Margaritis** for making this resource available through free CD source!

## Audio Preservation

This repository also contains the audio MP3 files, copied from the source, and located in the `ot_mp3` and `nt_mp3` folders:

- Each chapter is saved as a separate audio file. The mapping of chapter titles to MP3 files is provided in the `mp3chapters.csv` file.
- The first three characters of each file name represent the book name.
- The number following the book name indicates the chapter number.

## Audio Processing

MP3 files have been processed for noise, echo, and reverb reduction using the `ffmpeg` utility. The command used for this process is:

```bash
ffmpeg -i "input.mp3" -af "afftdn=nf=-50,firequalizer=gain_entry='entry(60,-12);entry(120,-10);entry(250,-8)'" "output.mp3"
```

## Vamvas Translation Origin and History

- **Translator**: The Vamvas Holy Bible was translated by Neofytos Vamvas (1776–1855), a Greek theologian, professor, and one of the prominent figures of the Greek Enlightenment.
- **Purpose**: Vamvas sought to create a modern Greek translation of the Bible that would make the scriptures accessible to the general population while maintaining theological accuracy.
- **Release**: The translation was first published in the 19th century, around 1850.
- **Language**: It was written in **Katharevousa**, a formal version of Greek that blends classical and modern Greek elements. This made it more accessible than older texts but still somewhat formal for today's readers.

## Web-Based Player

A player has been developed for the site `https://ebible.gr` utilizing the resources located in the `ot_mp3` and `nt_mp3` folders. The player offers a responsive web interface for listening to Bible chapters in MP3 format while concurrently reading the text.

### Player link

Narration of the Holy Bible (Vamvas Greek Translation): <a href="https://ebible.gr/vamvasaudio" target="_blank">https://ebible.gr/vamvasaudio</a>

### Features
1. **MP3 Listing**:
   - Displays MP3 chapters categorized by book.
     
2. **Player Controls**:
   - Play, Stop buttons.
   - Displays the current playing track.

3. **Search and Filter**:
   - Filter by book or search by chapter name.

4. **Reading text in Polytonic Greek**:  
   - Users can listen to Bible chapters in MP3 format while concurrently reading the corresponding text in polytonic Greek.
     
5. **Share chapter links**:
   - Click on the 🔗 icon next to a chapter in the listing to load a shareable link for the chapter.
   - Links follow the format: `https://ebible.gr/vamvasaudio?mp3=bbb-cc.mp3` where bbb is the short book name and cc is the chapter number (e.g., https://ebible.gr/vamvasaudio?mp3=mat-1.mp3).

6. **Responsive Design**:
   - Works seamlessly across desktop, tablet, and mobile devices.
