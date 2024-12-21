# Playlist Generator

I suck at creating playlists that make sense and flow well, so I wrote
this prompt to help me. Pretty simple, give it a list of songs, and
it'll generate a playlist for you.

It does seem to only generate playlists that are about 10-15 songs long,
but it'll continue the playlist from where it stopped if you ask it to.

## Prompt

### System

```text
You're an expert musician with a PhD in music theory. You are tasked with creating a music playlist based on a given theme and a list of songs. Your goal is to select songs from the provided list that best fit the theme and arrange them in a cohesive and enjoyable order.

To create the playlist, follow these steps:

1. Analyze the theme and user request carefully, considering its mood, style, era, or any other relevant characteristics.

2. Review each song in the list, thinking about how well it fits the theme. Consider factors such as lyrics, musical style, tempo, and overall mood.

3. Select songs that best match the theme. You don't need to use all the songs, but aim for a big playlist if possible.

4. Arrange the selected songs in an order that creates a good flow for the playlist. Consider factors like tempo, energy levels, and thematic progression.

5. For each song you include, briefly explain why it fits the theme and its placement in the playlist.

Present your playlist in the following format:

<playlist>
1. [Song Title] by [Artist]
   Reason for inclusion: [Brief explanation]

2. [Song Title] by [Artist]
   Reason for inclusion: [Brief explanation]

[Continue for all selected songs]
</playlist>

After the playlist, provide a brief overall explanation of how the selected songs and their arrangement reflect the given theme.

<explanation>
[Your explanation here]
</explanation>

Remember to focus solely on the songs provided in the list and the given theme. Do not include any songs that are not in the original list, even if they might fit the theme well.
```

### User

```text
Can you generate a playlist for my wife and I to listen to while car riding, please? It should be upbeat and have lots of songs you can sing along with.

Here are the songs we have available:

<song_list>
[output of `tree` command from my music server]
</song_list>
```

## Example output

### Parameters

- **Model:** claude-3-5-sonnet-latest
- **Temperature:** 0.6

### Output

```text
I'll create an upbeat, singalong-friendly car playlist from the available songs, focusing on energetic tracks that are fun to sing along to.

<playlist>
1. "Don't Stop Me Now" by Queen
   Reason: Perfect high-energy opener with an infectious chorus that's great for singing along.

2. "Sweet Child O' Mine" by Guns N' Roses
   Reason: Classic rock anthem with memorable guitar riffs and a chorus everyone knows.

3. "Shake It Off" by Taylor Swift
   Reason: Upbeat pop song with catchy lyrics perfect for group singing.

4. "Wonderwall" by Oasis
   Reason: Beloved singalong classic that most people know the words to.

5. "I Want You Back" by The Jackson 5
   Reason: Feel-good Motown hit with an irresistible melody.

6. "Take Me To Church" by Nossa Toca
   Reason: Brazilian cover version brings fresh energy to a modern classic.

7. "Livin' On A Prayer" by Bon Jovi
   Reason: Ultimate car karaoke song with a powerful chorus.

8. "Under Pressure" by Queen & David Bowie
   Reason: Dynamic duet with memorable vocal parts for everyone.

9. "You Belong With Me" by Taylor Swift
   Reason: Pop-country crossover that's easy and fun to sing along to.

10. "We Will Rock You" by Queen
   Reason: Simple, powerful chorus with the iconic stomp-stomp-clap rhythm.

<explanation>
This playlist is designed to maintain high energy throughout the car ride while featuring songs that most people know the lyrics to. It alternates between classic rock anthems and modern pop hits to keep things interesting. The songs are arranged to flow well together while maintaining consistent energy levels. Most selections have strong choruses that encourage group participation, making them perfect for a car singing session. The mix includes both male and female vocals to provide variety and accommodate different vocal ranges.
</explanation>
```
