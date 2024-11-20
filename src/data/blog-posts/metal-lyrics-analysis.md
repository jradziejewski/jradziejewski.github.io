---
title: Lyrics of Metal Music Across Decades
publishDate: 11.11.2024
description: Exploring lyrical landscape of metal music by analyzing top 50 albums of each decade, starting from 70s.
---

<img src="/assets/blog/lyrics-analysis/Sabs.jpg" width="400" alt="black sabbath" style="margin-left:50%; transform: translateX(-50%);" />

Metal music has undergone a remarkable evolution over the decades, starting with the groundbreaking riffs of Black Sabbath in 70s, the pioneers of heavy metal, and expanding into the diverse and skillful artistry of today’s modern metal scene. In this article, we’ll take an in-depth look at how the lyrical themes in metal music have developed and transformed by analyzing the top 50 user-rated albums from each decade.

> **Important disclaimer** <br>
> This article will contain some explicit language and themes that may not be suitable for all audiences.

## Methodology

<br>

### 1. Data Collection

- Top 50 albums of each decade were scraped using Python library `BeautifulSoup` from [AlbumOfTheYear.org](https://www.albumoftheyear.org/)
- Then, for each album the lyrics were retrieved using `lyricsgenius` package and then cleaned up using custom scripts.

### 2. Data Analysis

- Python library, `nltk` was used to analyze sentiment of songs.
- Wordclouds generated using `some library etc` and visualized using `matplotlib`.

### 3. Comparison Across Decades

<img src="/assets/blog/lyrics-analysis/wordcloud_decades.png" width="800" alt="wordcloud across decades" style="margin-left:50%; transform: translateX(-50%);" />
<p style="text-align:center; font-size: 12px"><i>Fig. 1 - Wordcloud across decades. By observing the most dominant words, we can infer common themes or cultural trends that were influential in each decade. We can also detect linguistic shifts, although this won't be our focus in this case.</i></p>

The word cloud illustrates how heavy metal's roots trace back to the hard rock and blues in the 1970s. Notably, this is the only decade where themes of love are prominently featured. From a linguistic perspective, the 1970s also stand out for a higher frequency of words with vague or non-specific meanings, such as know, get, and take.

The 1980s and 1990s marked the golden era of thrash metal, dominated by iconic bands like Metallica, Death, Slayer, Iron Maiden, and Megadeth. The music from this period was intensely aggressive, often paired with lyrics that delved into themes like death, hell, destruction, pain, and blood. As evident from the word cloud, these words were a staple of heavy metal's lyrical landscape. Now _that's_ heavy metal!

But that’s not all that metal of the 1980s and 1990s had to offer. Beyond the high-energy and aggressive anthems, the era also featured numerous (_still heavy_) ballads that explored deeper themes like time, life, and the soul. This highlights that metal isn’t just about aggression; it is also a genre rich with introspection and reflection. This diversity is evident in the word cloud, where words like time, life, soul, and mind also stand out.

From the 2000s onward, metal evolved with the rise of sub-genres like nu metal, metalcore, deathcore, and djent. During this period, depressive and dark themes became increasingly prominent. Interestingly, the word time remains significant across each decade in the word cloud, but starting in the 2000s, other words like life, never, away, and can’t suggest a shift towards a more negative and somber lyrical tone. The music began to paint a bleaker, more introspective picture.

That being said, it’s important to note that our analysis is based on the most popular albums, as rated by listeners. This means the findings are skewed towards the most well-known songs and may not fully represent the entire genre. Today, metal is incredibly diverse, offering something for everyone—from the most aggressive and brutal sounds to melodic and deeply introspective compositions.

<img src="/assets/blog/lyrics-analysis/sentiment_decades.png" width="800" alt="sentiment across decades" style="margin-left:50%; transform: translateX(-50%);" />
<p style="text-align:center; font-size: 12px"><i>Fig. 2 - Setiment across decades</i></p>

When it comes to sentiment analysis, we can observe that the 1970s were the least negative of all decades. This isn’t surprising, as metal was still in its infancy and was heavily influenced by blues and hard rock (a point that I probably repeat a little bit too often).

The sentiment across other decades remains relatively similar, with the 1990s standing out as the most negative. It’s important to understand how sentiment is classified using the `NLTK` library: the system evaluates sentiment based on the presence of certain words in the lyrics. If a song features more negative words, it is classified as having a negative sentiment, and vice versa.

Higher level of negative sentiment doesn’t necessarily mean the song is more depressing; it could also reflect themes of aggression or anger. Since this classification system is designed primarily for general text, it isn’t perfect for analyzing song lyrics. Nonetheless, it provides a useful general idea of how sentiment in metal music has evolved over the decades.

<img src="/assets/blog/lyrics-analysis/sentiment_mean_decades.png" width="400" alt="mean sentiment across decades" style="margin-left:50%; transform: translateX(-50%);" />
<p style="text-align:center; font-size: 12px">Fig. 3 - Mean lyrics sentiment by decade</p>

<hr>

## In-Depth Analysis of Decades

<br>

### The 70s

70s is considered by most people the very beginning of metal music, with _Black Sabbath_ being the first band to be classified as heavy metal. As we can see in top albums of the 70s, first of all - we don't even have 50 albums classified in this genre.
Let's take look at them:

| rank | artist        | album                            | year |
| ---- | ------------- | -------------------------------- | ---- |
| 1    | Black Sabbath | Paranoid                         | 1970 |
| 2    | Black Sabbath | Master of Reality                | 1971 |
| 3    | Black Sabbath | Black Sabbath                    | 1970 |
| 4    | Rainbow       | Rising                           | 1976 |
| 5    | Black Sabbath | Black Sabbath Vol                | 1972 |
| 6    | Black Sabbath | Sabbath Bloody Sabbath           | 1973 |
| 7    | Judas Priest  | Stained Class                    | 1978 |
| 8    | Budgie        | Never Turn Your Back on a Friend | 1973 |
| 9    | Van Halen     | Van Halen                        | 1978 |
| 10   | Motörhead     | Overkill                         | 1979 |
| ..   | ..            | ..                               | ..   |
| 33   | Accept        | Accept                           | 1979 |

_You can see the full list [here](https://www.albumoftheyear.org/ratings/user-highest-rated/1970s/metal/), or the full dataset in my [GitHub repo](https://github.com/jradziejewski/song-lyric-analysis/blob/main/albums_data.xlsx)._

The genre in early 70s was still in its infancy. Later in this decade, bands like _Judas Priest_ and _Motörhead_ started to shape the genre into what we know today. Some of the lyrics in 70s were dark and introspective, often reflecting the social and political turmoil of the time.

<img src="/assets/blog/lyrics-analysis/70s_sentiment.png" width="400" alt="sentiment in 70s" style="margin-left:50%; transform: translateX(-50%);" />
<p style="text-align:center; font-size: 12px"><i>Fig. 4 - Sentiment of songs in the 70s</i></p>

Interestingly, the sentiment analysis reveals that a significant number of songs from the 1970s carry a positive sentiment.
Despite the emergence of heavier and darker themes in metal, the lyrics of this era also explored themes of love, empowerment, and even humor.
This can partly be attributed to the fact that many albums leaned more toward hard rock than pure metal.
This blending of influences likely explains why the 1970s stands out as the decade with the most positive sentiment in its music.

<img src="/assets/blog/lyrics-analysis/70s_wordcloud.png" width="400" alt="sentiment in 70s" style="margin-left:50%; transform: translateX(-50%);" />
<p style="text-align:center; font-size: 12px"><i>Fig. 5 - wordcloud of the 70s</i></p>

From the word cloud above, it’s clear that some of the most commonly used words in the lyrics of the 1970s include “love,” “time,” and “life.”
The size of the word “love” is particularly interesting, as it’s not a term typically associated with the heavier themes of metal music.
However, it's important to remember that during the 1970s, metal was still in its infancy, drawing significant influence from blues and hard rock, genres where love is a frequent and central theme.

#### Example lyrics from 70s

_Black Sabbath_ stands out as one of the most influential bands of all time, and 70s was the decade when they released some of their most iconic songs.
One of my favorite lyrics from this era is from their song _War Pigs_, a song that resonates deeply as a protest anthem against the horrors of war:

> Politicians hide themselves away
> <br>
> They only started the war
> <br>
> Why should they go out to fight?
> <br>
> They leave that all to the poor, yeah
>
> [...]
>
> Now, in darkness, world stops turning
> <br>
> Ashes where their bodies burning
> <br>
> No more war pigs have the power
> <br>
> Hand of God has struck the hour
> <br>
> Day of Judgment, God is calling
> <br>
> On their knees, the war pigs crawling
> <br>
> Begging mercies for their sins
> <br>
> Satan, laughing, spreads his wings
>
> -- _Black Sabbath, War Pigs_

This song remains a powerful and timeless anti-war anthem, resonating as strongly today as it did when it was first released.
It delivers a critique of politicians and leaders who instigate wars, yet flee from the dire consequences, leaving the suffering and death to the less privileged.

The final verse is particularly impactful, vividly depicting the end of war and the arrival of Judgment Day.
The roles are reversed - those who once wielded power — the "war pigs" — are now on their knees, pleading for mercy as they face divine retribution.

### The 80s

The 1980s was a pivotal era in the evolution of metal music. The genre truly began to take shape and diversify.
This decade saw the emergence of legendary bands such as Metallica, Iron Maiden, Slayer, Megadeth and Death.
Each of them, and many more of those years, left an indelible mark on the metal landscape.
Let's see the top 10 albums of 1980s:

| rank | artist      | album                        | year |
| ---- | ----------- | ---------------------------- | ---- |
| 1    | Metallica   | Master of Puppets            | 1986 |
| 2    | Metallica   | Ride the Lightning           | 1984 |
| 3    | Iron Maiden | Powerslave                   | 1984 |
| 4    | Iron Maiden | The Number of the Beast      | 1982 |
| 5    | Iron Maiden | Seventh Son of a Seventh Son | 1988 |
| 6    | Candlemass  | Epicus Doomicus Metallicus   | 1986 |
| 7    | Slayer      | Reign in Blood               | 1986 |
| 8    | Metallica   | ...And Justice for All       | 1988 |
| 9    | Death       | Leprosy                      | 1988 |
| 10   | Iron Maiden | Somewhere in Time            | 1986 |

_You can see the full list [here](https://www.albumoftheyear.org/ratings/user-highest-rated/1980s/metal/), or the full dataset in my [GitHub repo](https://github.com/jradziejewski/song-lyric-analysis/blob/main/albums_data.xlsx)._

The sheer number of influential bands from this period makes it nearly impossible to list them all.
The 1980s were a time of experimentation and innovation, with bands pushing the boundaries of what metal could be.

<img src="/assets/blog/lyrics-analysis/80s_sentiment.png" width="400" alt="sentiment in 70s" style="margin-left:50%; transform: translateX(-50%);" />
<p style="text-align:center; font-size: 12px"><i>Fig. 6 - sentiment analysis of songs in the 80s</i></p>

We can see that the plot is heavier on the negative side. As we remember from the general sentiment analysis, 1980s were the most negative of all decades.
The aggressive and intense nature of metal music was what set it apart from other genres, and this intensity is evident in the lyrics of the 1980s,
which often explored themes of death, destruction, and darkness.

<img src="/assets/blog/lyrics-analysis/80s_wordcloud.png" width="400" alt="sentiment in 70s" style="margin-left:50%; transform: translateX(-50%);" />
<p style="text-align:center; font-size: 12px"><i>Fig. 7 - wordcloud of the 80s</i></p>

The wordcloud shows that lyrics of the 80s were characterized by aggression and intensity, often exploring themes of death, destruction, and darkness.
They reflected not only social and political challenges of the era, but also the personal struggles and deep emotions of the artists.

Common themes included rebellion and anti-authority sentiments, the Cold War and nuclear threats, social issues and personal challenges,
though they were not always explicit in their lyrics. Musicians often used metaphorical language and symbolism to convey their messages.

Some lyrics had strong storytelling element, often drawing inspiration from history or fantasy -- _Iron Maiden_ being a notable example.

The technological advancements of the music industry allowed bands to experiment with new sounds and styles.
New recording techniques and equipment allowed for heavier guitar tones and faster drumming, which allowed artists of time to create music more intense and aggressive than ever before.
Heavy sound allowed musicians to also explore more darker and complex themes in their music, without much contrast between the music and lyrics.

#### Example lyrics from 80s

One of the most iconic songs from the 1980s is _The Trooper_ by _Iron Maiden_, a band that has become synonymous with the heavy metal genre.

> The bugle sounds, the charge begins
> <br>
> But on this battlefield, no one wins
> <br>
> The smell of acrid smoke and horse's breath
> <br>
> As I plunge on into certain death
>
> [...]
>
> He pulls the trigger and I feel the blow
> <br>
> A burst of rounds takes my horse below
> <br>
> And as I lay there, gazing at the sky
> <br>
> My body's numb and my throat is dry
> <br>
> And as I lay forgotten and alone
> <br>
> Without a tear, I draw my parting groan
>
> -- _Iron Maiden, The Trooper_

The song is inspired by the Charge of the Light Brigade, a well-known military engagement during the Crimean War. It’s a great example of the themes found in 1980s metal, as it blends storytelling -- that can be taken both literally and figuratively -- with intense music. The lyrics delve into the harsh realities of war, death, and sacrifice—topics that can be interpreted beyond their literal meaning to address broader social and political issues. The energy of the track is palpable, with the galloping rhythm and powerful vocals creating a sense of urgency and intensity that captures the spirit of heavy metal.

## The 90s

In the 90s, trends from the 80s continued to evolve. To me personally, 90s are about the emergence of extreme metal sub-genres like death metal and its varieties,
and one of my favorite subgenres - progressive metal. Here are top 10 albums of the decade:

| rank | artist                   | album                     | year |
| ---- | ------------------------ | ------------------------- | ---- |
| 1    | Death                    | Symbolic                  | 1995 |
| 2    | Death                    | The Sound of Perseverance | 1998 |
| 3    | Rage Against the Machine | Rage Against the Machine  | 1992 |
| 4    | TOOL                     | Ænima                     | 1996 |
| 5    | Death                    | Human                     | 1991 |
| 6    | Alice in Chains          | Dirt                      | 1992 |
| 7    | Megadeth                 | Rust in Peace             | 1990 |
| 8    | System of a Down         | System of a Down          | 1998 |
| 9    | Opeth                    | Still Life                | 1999 |
| 10   | Nine Inch Nails          | Broken                    | 1992 |

_You can see the full list [here](https://www.albumoftheyear.org/ratings/user-highest-rated/1990s/metal/), or the full dataset in my [GitHub repo](https://github.com/jradziejewski/song-lyric-analysis/blob/main/albums_data.xlsx)._

The variety of sub-genres that emerged in the 90s is reflected in the top albums of the decade. From death metal, through rapcore, some grunge, to progressive metal - we can find it all there.

<img src="/assets/blog/lyrics-analysis/90s_sentiment.png" width="400" alt="sentiment in 70s" style="margin-left:50%; transform: translateX(-50%);" />
<p style="text-align:center; font-size: 12px"><i>Fig. 8 - Wordcloud across decades. By observing the most dominant words, we can infer common themes or cultural trends that were influential in each decade. We can also detect linguistic shifts, although this won't be our focus in this case.</i></p>

Metal of this era was heavily influenced by a lot of genres, such as _grunge_, and even _hip-hop_.
The diversity of incluences is reflected in the lyrics.
The sentiment of the 1990s is less negative than the 1980s.
It is still visibly heavier on the negative side, but the gap between positive and negative sentiment is smaller.
This can be attributed to the increasing variety within the genre.

Music of the 90s was less dominated by aggressive and intense themes and began to explore a much wider range of topics, as shown in the following wordcloud.

<img src="/assets/blog/lyrics-analysis/90s_wordcloud.png" width="400" alt="sentiment in 70s" style="margin-left:50%; transform: translateX(-50%);" />
<p style="text-align:center; font-size: 12px"><i>Fig. 9 - Wordcloud across decades. By observing the most dominant words, we can infer common themes or cultural trends that were influential in each decade. We can also detect linguistic shifts, although this won't be our focus in this case.</i></p>

Words that point to more introspective themes, such as _“time” “life”, "mind" and “soul”_ are the most prominent.
This suggests that the music of the 90s was more reflective. Even when the music remained aggressive, it often explored
heavy themes in less explicit way.

The _grunge_, in metal most notably represented by _Alice in Chains_, was a genre that often dealt with themes of depression, addiction, and loss.
On the other hand, bands like _Rage Against the Machine_ and _System of a Down_ used their music to address social and political issues, often with a more direct and confrontational approach.
If we're talking about the 90s, we can't forget the band _Pantera_, which stayed true to the aggressive and intense roots of metal, but extending it even further, giving birth to a new sub-genre - _groove metal_.

But to me, the most interesting part of the 90s was the rise of progressive metal with bands like _Dream Theater_, _Opeth_, and _Tool_.
Their lyrics often explored deep philosophical and existential themes, and the music itself was incredibly intricate and complex.
The depth and emotional intensity is what I value the most in music, and progressive metal has always delivered on that front.

#### Example lyrics from 90s

There is a ton of great lyrics from the 90s, something that I could definitely explore at its own.
But I wanted to include only one example for each decade in this article, and for 90s, I chose _Tool_'s _Ænema_.

> Some say the end is near
> <br>
> Some say we'll see Armageddon soon
> <br>
> I certainly hope we will
> <br>
> I sure could use a vacation from this
>
> Bullshit three-ring
> <br>
> Circus sideshow of
> <br>
> Freaks
>
> Here in this hopeless fucking hole we call L.A.
> <br>
> The only way to fix it is to flush it all away
> <br>
> Any fucking time, any fucking day
> <br>
> Learn to swim, I'll see you down in Arizona bay

## The 00s

In the 2000s, metal was already diverse and well-established genre.
This decade metal diversified even further, with the rise of a lot of new subgenres.
Here are top 10 albums of the 2000s:

| rank | artist           | album                      | year |
| ---- | ---------------- | -------------------------- | ---- |
| 1    | System of a Down | Toxicity                   | 2001 |
| 2    | Converge         | Jane Doe                   | 2001 |
| 3    | Opeth            | Blackwater Park            | 2001 |
| 4    | TOOL             | Lateralus                  | 2001 |
| 5    | Gojira           | From Mars to Sirius        | 2005 |
| 6    | Deftones         | White Pony                 | 2000 |
| 7    | Boris            | Boris at Last -Feedbacker- | 2003 |
| 8    | Gris             | Il était une forêt...      | 2007 |
| 9    | Opeth            | Ghost Reveries             | 2005 |
| 10   | Electric Wizard  | Dopethrone                 | 2000 |

_You can see the full list [here](https://www.albumoftheyear.org/ratings/user-highest-rated/2000s/metal/), or the full dataset in my [GitHub repo](https://github.com/jradziejewski/song-lyric-analysis/blob/main/albums_data.xlsx)._

Genres like metalcore, deathcore and djent became increasingly popular in the 2000s.
A lot of genres also evolved. Some bands that were very influential in this era are one of my all-time favorites: _Mastodon_, _Gojira_ and _Opeth_.

<img src="/assets/blog/lyrics-analysis/00s_sentiment.png" width="400" alt="sentiment in 70s" style="margin-left:50%; transform: translateX(-50%);" />
<p style="text-align:center; font-size: 12px"><i>Fig. 10 - Wordcloud across decades. By observing the most dominant words, we can infer common themes or cultural trends that were influential in each decade. We can also detect linguistic shifts, although this won't be our focus in this case.</i></p>

Sentiment in the 2000s, is like all the other decades, heavier on the negative side, although the gap between positive and negative sentiment is smaller compared to 90s and 80s.
The music of the 2000s continued to explore a wide range of themes, which is probably why the sentiment is more balanced.

<img src="/assets/blog/lyrics-analysis/00s_wordcloud.png" width="400" alt="sentiment in 70s" style="margin-left:50%; transform: translateX(-50%);" />
<p style="text-align:center; font-size: 12px"><i>Fig. 11 - Wordcloud across decades. By observing the most dominant words, we can infer common themes or cultural trends that were influential in each decade. We can also detect linguistic shifts, although this won't be our focus in this case.</i></p>

We can see in the wordcloud that words _life_ and _time_ are the most prominent, suggesting that the music of the 2000s continued to explore introspective themes.
Also there is something in the word _eye_ which makes it very popular in 90s, 00s and 10s.
This is interesting, but so are eyes, I guess, and also this word can be used in multiple contexts which may explain why it's so popular.

The wordcloud shows that range of themes in 00s was very wide, and it's hard to pinpoint one specific theme that dominated the era.
It seems to be a combination of themes from previous decades, and artists were interested in the general state of the world, as well as feelings, and personal experiences.
Aggressive themes were still present, but words such as _heart_, _soul_, _mind_, _light_ suggest that the listeners valued in the music of 2000s more introspective and reflective themes.

#### Example lyrics from 00s

For the 2000s, I wanted to choose something different, and it's from _Mastodon_'s concept album _"Leviathan"_,
an album inspired by the novel _"Moby Dick"_ written by _Herman Melville_.

> I think that someone is trying to kill me
> <br>
> Infecting my blood and destroying my mind
> <br>
> No man of the flesh could ever stop me
> <br>
> The fight for this fish is a fight to the death
>
> [...]
>
> What remorseless emperor commands me?
> <br>
> I no longer govern my soul
> <br>
> I am completely immersed in darkness
> <br>
> As I turn my body away from the sun
>
> -- _Mastodon_, _Blood and Thunder_

The explores with Captain Ahab's obsession with seeking revenge on the _White Whale_, mirroring the main theme of the novel.
On the surface it appears to be about hunting a massive creature, but on a deeper level,
it's a story about revenge, and the dangers of unchecked ambition, and the destructive power of obsession.

I love how this song captures the essence of Captain Ahab's mind, both lyrically and musically.
This album inspired me to read _Moby Dick_ and appreciate its value.
Before, I saw it as just an old, boring and strange book, but this song changed my perspective.

## The 10s

| rank | artist              | album                       | year |
| ---- | ------------------- | --------------------------- | ---- |
| 1    | DM DOKURO           | The Tale of a Cruel World   | 2019 |
| 2    | Deafheaven          | Sunbather                   | 2013 |
| 3    | Mick Gordon         | Doom ( Game Soundtrack)     | 2016 |
| 4    | Deftones            | Koi No Yokan                | 2012 |
| 5    | MAXIMUM THE HORMONE | Yoshū Fukushū               | 2013 |
| 6    | Converge            | All We Love We Leave Behind | 2012 |
| 7    | Ne Obliviscaris     | Citadel                     | 2014 |
| 8    | Ne Obliviscaris     | Portal of I                 | 2012 |
| 9    | Dying Fetus         | Reign Supreme               | 2012 |
| 10   | Deathspell Omega    | Paracletus                  | 2010 |

_You can see the full list [here](https://www.albumoftheyear.org/ratings/user-highest-rated/2010s/metal/), or the full dataset in my [GitHub repo](https://github.com/jradziejewski/song-lyric-analysis/blob/main/albums_data.xlsx)._

<img src="/assets/blog/lyrics-analysis/10s_sentiment.png" width="400" alt="sentiment in 70s" style="margin-left:50%; transform: translateX(-50%);" />
<p style="text-align:center; font-size: 12px"><i>Fig. 12 - Wordcloud across decades. By observing the most dominant words, we can infer common themes or cultural trends that were influential in each decade. We can also detect linguistic shifts, although this won't be our focus in this case.</i></p>
<img src="/assets/blog/lyrics-analysis/10s_wordcloud.png" width="400" alt="sentiment in 70s" style="margin-left:50%; transform: translateX(-50%);" />
<p style="text-align:center; font-size: 12px"><i>Fig. 13 - Wordcloud across decades. By observing the most dominant words, we can infer common themes or cultural trends that were influential in each decade. We can also detect linguistic shifts, although this won't be our focus in this case.</i></p>

## The 20s

| rank | artist            | album                              | year |
| ---- | ----------------- | ---------------------------------- | ---- |
| 1    | Knocked Loose     | A Tear in the Fabric of Life       | 2021 |
| 2    | Mick Gordon       | DOOM Eternal (Game Soundtrack)     | 2020 |
| 3    | life              | demo three                         | 2020 |
| 4    | Vildhjarta        | måsstaden under vatten             | 2021 |
| 5    | Blood Incantation | Absolute Elsewhere                 | 2024 |
| 6    | Knocked Loose     | You Won't Go Before You're Supp... | 2024 |
| 7    | Chat Pile         | Cool World                         | 2024 |
| 8    | Heaven Pierce Her | ULTRAKILL: INFINITE HYPERDEATH     | 2020 |
| 9    | Loathe            | I Let It in and It Took Everything | 2020 |
| 10   | Chat Pile         | God’s Country                      | 2022 |

_You can see the full list [here](https://www.albumoftheyear.org/ratings/user-highest-rated/2020s/metal/), or the full dataset in my [GitHub repo](https://github.com/jradziejewski/song-lyric-analysis/blob/main/albums_data.xlsx)._

<img src="/assets/blog/lyrics-analysis/20s_sentiment.png" width="400" alt="sentiment in 70s" style="margin-left:50%; transform: translateX(-50%);" />
<p style="text-align:center; font-size: 12px"><i>Fig. 14 - Wordcloud across decades. By observing the most dominant words, we can infer common themes or cultural trends that were influential in each decade. We can also detect linguistic shifts, although this won't be our focus in this case.</i></p>
<img src="/assets/blog/lyrics-analysis/20s_wordcloud.png" width="400" alt="sentiment in 70s" style="margin-left:50%; transform: translateX(-50%);" />
<p style="text-align:center; font-size: 12px"><i>Fig. 15 - Wordcloud across decades. By observing the most dominant words, we can infer common themes or cultural trends that were influential in each decade. We can also detect linguistic shifts, although this won't be our focus in this case.</i></p>
