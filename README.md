## Inspiration
Within the current music tech industry, there is great interest in the use of AI for music generation, but most tools currently being developed do not quite cater to musician’s needs and remain in primitive, unusable stages. There are many various “song generation” tools being developed, but they all work exactly as you would expect: they generate entire songs. However, as musicians, we know that artists want to have more control over their own work. Our tool, Harmonize, which generates appropriate harmonies for given melodies, is meant to facilitate creativity for musicians, not to replace them. We want to allow singers and other musicians (especially new artists who may not have a strong music theory background or have an existing band to workshop with) to still be able to imagine what a more complete project could sound like and realize their musical imagination. In the end, musicians keep autonomy over their musical ideas and are able to iterate through them more efficiently.

## What it does
Our product generates harmonies and accompanimental textures for given melodies. The user sings or hums a melody into a voice recorder and the plugin immediately processes it and provides possible arrangements of harmony and texture to accompany your melody.

## How we built it                                                                                                                                                                                                                                                                                                                                                                      
Our product takes the form of a webapp. The front-facing interface is built using clean HTML and JS. We used Flask for the backend to process audio data, and information is sent back and forth between the two components.

## Challenges we ran into
We trained multiple versions of ML models, but we had a myriad of issues with finding a dataset that suited our needs exactly. For example, many datasets contain different styles of music, like folk songs and classical music, that we were not focusing on. Ultimately, after much review of the current research literature, we pivoted to using a dynamic programming-based model that was more stable than machine learning approaches and could still yield very impressive results. 

## Accomplishments that we're proud of
Creating a fully-fledged audio processing and synthesizing webapp in the span of a hackathon was no easy feat. We are proud of our Flask-based backend that seamlessly integrates with our audio recording to provide quick results. Because our app integrates the necessary audio components end-to-end, it creates an easy-to-use experience for the end-user.

## What we learned

We learned to be bold when taking risky but rewarding steps. While we didn't end up using our initial ML-based approach, we learned a lot about the structure of audio components, working with melodies and harmonies, and designing fast, workable representations. In particular, we created a proprietary vectorized melody/harmony encoding format that is suitable to be trained on by a Transformer model, and if we decide to revisit this approach in the future, we will work off this format. Ultimately, we're happy that our initial missteps led to greated rewards down the line.


## What's next for Harmonize
There’s a lot of places we could go from here: we spent most of our time trying to prepare the dataset and use ML, but it didn’t really work out in the end, and that’s an idea we’d love to return to with a better-scraped dataset and more time to tune the model. We’d also like to implement this as a plugin directly into any music editing software, such as Ableton Live or GarageBand, so that any musician could easily integrate it into their work. Long-term, we’d love to see Harmonize become a larger suite of tools for musicians, this tool being one of them.



built with:
Python, Javascript, HTML, Flask, MIDI

Other sources we used:
https://github.com/spotify/basic-pitch \
https://github.com/GabrielDelight/gabriel-voice-recorder-app \
https://arxiv.org/abs/2108.11213 \
https://magenta.tensorflow.org/music-transformer 

