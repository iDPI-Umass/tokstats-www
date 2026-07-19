<main>
    <section class="tube-copy">

        <h1>About TokStats</h1>

            <p>
                TokStats is an interactive dashboard that provides users with information about TikTok based on random sampling. We periodically create a random sample of TikTok big enough to find basic statistics about the site, like how many videos it hosts, how many are uploaded from Argentina or Bangladesh, and how many views videos get on average. This is fundamental information about one of the most important platforms in the world, and the sort of data that researchers, journalists, and others need in order to properly study the content TikTok hosts. 
            </p>
            <p>
                This site is an outgrowth of a long research project in the <a href="https://publicinfrastructure.org" target="_blank" rel="noopener noreferrer">Initiative for Digital Public Infrastructure</a> at the University of Massachusetts Amherst. We initially wanted to study certain kinds of content on YouTube and quickly realized it was impossible to contextualize findings because there was no way to produce a truly random sample of YouTube to use as a basis for comparison. That led to <a href="https://tubestats.org/">TubeStats</a>, which TokStats is modeled after.
            </p>
            <p>
                A random sample can tell you how representative your sample is. If you find 1,000 instances of a type of video in a study, a random sample can answer "out of how many?" If you rely on TikTok's search or recommendation algorithms to produce a collection of videos, a random sample can help inform how the algorithm is guiding your selection. In short, random samples are essential to understand a subject, but can be difficult to obtain.
            </p>
            <p>
                TikTok is one of the largest and most important websites in the world, but it does not provide a way to produce a random sample or aggregate data from its videos. In addition, videos are more difficult for computers to parse than content from text-based websites. Our random sampling method works to mitigate the challenges of researching TikTok.
            </p>
            <p>
                The primary output of our project was a paper, currently under review, that includes an analysis of a random sample we produced through our own method in 2024.
            </p>
    </section>

</main>

<!--<h2>Introduction</h2>-->
<!--<p>-->
<!--    TubeStats is an interactive dashboard that allows users to explore platform-wide data for YouTube based on random prefix sampling and metadata analysis. The method used to collect data for this dashboard is described in <a href="https://journalqd.org/article/view/4066" target="_blank" rel="noopener noreferrer">Dialing for Videos: A Random Sample of YouTube</a>.-->
<!--</p>-->

<!--<p>-->
<!--    <a href="https://github.com/iDPI-Umass/tubestats-www" target="_blank" rel="noopener noreferrer">View source code here</a>-->
<!--</p>-->
<!--<h2>Randomly Sampling YouTube</h2>-->
<!--<p>-->
<!--    A large, random sample of YouTube enables the estimation of the platform's size, viewership, and growth over time. Videos suggested by the recommender system or surfaced by topic-based queries to the search engine—how most users interact with YouTube—are not representative of the entire platform, but rather tend towards higher view and quality videos that are in the user's inferred language.-->
<!--</p>-->
<!--<p>-->
<!--    Our <a href="https://journalqd.org/article/view/4066" target="_blank" rel="noopener noreferrer">Dialing for Videos</a> paper establishes random sampling method for YouTube, based on generating trillions of random 11 character-long video identifiers. We then applied the dialing for videos method to confirm the randomness of the "random prefix sampling" method, first described in a <a href="https://doi.org/10.1145/2068816.2068851" target="_blank" rel="noopener noreferrer">2011 paper by Zhou et al.</a>. Prefix sampling's 1000x efficiency advantage over our provably random dialing method makes it the preferred random sampling method, and all samples on TubeStats will be prefix sampled.-->
<!--</p>-->
<!--<h3>-->
<!--    Estimating YouTube's Total Size-->
<!--</h3>-->
<!--<p>-->
<!--    Obtaining the exact number of videos hosted on YouTube would require checking each of the 18.4 quintillion valid video IDs to see if a video existed at that URL, as not every valid ID has been assigned to a video. Random sampling allows us to more efficiently estimate YouTube's size without checking every valid video ID.-->
<!--</p>-->
<!--<p>-->
<!--    By counting the number of random video IDs we generate and the number of IDs associated with videos, we can calculate the average rate at which videos are randomly distributed across the entire ID address space and use this rate to estimate YouTube's size.-->
<!--</p>-->
<!--<h2>Extracting Metadata</h2>-->
<!--<p>-->
<!--    We extracted metadata for each randomly sampled video using the <a href="https://github.com/yt-dlp/yt-dlp" target="_blank" rel="noopener noreferrer">yt-dlp</a> package. TubeStats presents only the aggregated metadata statistics of our random samples.-->
<!--</p>-->
<!--<h3>-->
<!--    Spoken Language Classification-->
<!--</h3>-->
<!--<p>-->
<!--    The near-global use of YouTube means that the platform likely hosts videos in nearly every spoken language on the planet. By identifying languages spoken in the tens of thousands of videos in our random samples, we can begin to study language group-specific trends on YouTube.-->
<!--</p>-->
<!--<p>-->
<!--    The <b>Detectable Language</b> chart on TubeStats displays the results of our language analysis using a pre-trained speech recognition model. We first extract the audio for each randomly sampled video using the <a href="https://github.com/yt-dlp/yt-dlp" target="_blank" rel="noopener noreferrer">yt-dlp</a> package. Each audio file is then passed into <a href="https://arxiv.org/abs/2212.04356" target="_blank" rel="noopener noreferrer">OpenAI's Whisper automatic speech recognition model</a>, and we record the automatically detected language token from the model's output. For the purposes of this chart, we exclude videos with model output probabilities less than 0.75.-->
<!--</p>-->
<!--<p>-->
<!--    We believe that this approach to spoken language detection is more comprehensive than one that relies solely on metadata analysis. Although automatic captions are increasingly common on YouTube, only a small fraction of our random samples have been captioned in one of the only <a href="https://support.google.com/youtube/answer/6373554" target="_blank" rel="noopener noreferrer">14 languages</a> that YouTube has the capability of generating captions for.-->
<!--</p>-->


<style>
    main {
        flex: 1 1 0;
        min-height: 0;
        max-width: 100vw;
        padding: 1rem;
        display: flex;
        flex-direction: column;
        flex-wrap: nowrap;
        justify-content: flex-start;
        align-items: center;
        overflow-y: scroll;
        background-color: var(--tube-color-null);
    }
    .logo {
        padding: 1rem;
        flex: 1 1 30%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    .logo img {
        border: none;
        border-radius: 0;
        max-width: 175px;
    }
</style>