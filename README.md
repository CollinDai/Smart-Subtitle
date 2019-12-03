# Smart-Subtitle
A real-time subtitle player.

## Tell us what your idea is.
Smart-Subtitle is a movie subtitle player. It listens to the movie and shows the dialogs to user sentence by sentence in a language user selected.

Smart-Subtitle will first try to convert the speech to text using [live-transcribe-speech-engine](https://github.com/google/live-transcribe-speech-engine).
Then it'll use **Firebase ML Kit's on-device translation API** to translate the text.

Google Translate does a good job listening and translating, but the presentation of the translated text is not too friendly to a movie audience.

In this challenge, I'm hoping to solve these problems

1. Speech-to-Text offline
2. Use on-device machine learning to find the end of each sentence and show only one sentence at a time.
3. Minimize the delay from the speech to the displaying the translated text on screen

## Tell us how you plan on bringing it to life. 
I've built a subtitle dipslay app ([link](https://github.com/CollinDai/Subtytle)) several years ago with following features:

1. search and download `.srt` subtitle source file from subtitle provider ([link](https://www.opensubtitles.org/en/))
2. parse the source file and play the subtitle synchronously with movie time.
3. Jump back to review past subtitles. And resume to live playing.

What its shortage is that it only provide subtitles that's available from the subittle provider. If the provider doesn't have a specific movie's subtitle, then the app can't provide that either.
And usually a movie will have its subtitle available couple of weeks after the movie's release. Or sometimes it only has subtitle in languages that user doesn't know.

So the best solution is to let the app listen and display the subtitle autonomously. And that'll rely on the on-device speech-to-text and translation technology.

Another shortage is that a movie theater sometimes has very bad cell/wifi signal. It'll make the speech-to-text engine, which currently needs online support, much less stable.
So I would like Google's help on implementing a offline speech-to-text solution.

I'd also like to get Google's help on improving the on-device translation api to better support the need to find sentence end.

### Timeline
I plan to start building on top of the Subtytle project by adding two new modules `stot` (speech to text) `translation`. So I can leverage the existing subtitle player.
#### Before February
Finish implementing online version of speech-to-text and on-device translation.

#### February - April
Attempt to bring the offine speech-to-text up.
Attempt to minimize the delay from the speech is heard to the displaying of the translated text.

## Tell us about you.
I used to be foreign student studying in the U.S.. Watching Hollywood movies is one of my favourite things to do. 
But being in the US for only one or two years, I couldn't understand all the jokes and detailed background.

So I decided to make Subtytle. But because of those shortage, it is not sufficient for those more needed scenarios. At that times I don't think it was even possible to do live speech-to-text and live translation.

Now I could understand those movies more, but I couldn't help thinking that there are always people coming to the US, trying enjoy the movie but can't because they are not good at English.
Or there are people going abroad and trying to watch a foreign movie, but like us, they can't understand.

Google has made brilliant things like Live Transcribe and Live Caption. It makes me realize that the technology has made all those impossibles possible.

So I'd give it another try.
