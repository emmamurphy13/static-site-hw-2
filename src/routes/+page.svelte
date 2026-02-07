<!--
  This is your page!
-->
<script>
  // Import all the news furniture components
  import ArticleHeader from '$lib/components/ArticleHeader.svelte';
  import ArticleBody from '$lib/components/ArticleBody.svelte';
  import Image from '$lib/components/Image.svelte';
  import RelatedLinks from '$lib/components/RelatedLinks.svelte';

  // Article metadata
  let headline = 'The Blue House Girls';
  let byline = 'NYCity News Service';
  let pubDate = '2026-02-07';

  // Related stories
  const relatedStories = [
    { headline: 'How America\'s top news organizations escape rigid publishing systems to design beautiful data-driven stories on deadline.', href: 'https://palewi.re/docs/coding-the-news/' },
    { headline: 'How to install, configure and use Visual Studio Code, GitHub and Copilot', href: 'https://palewi.re/docs/coding-the-news/scripts/week-1/' },
    { headline: "How to publish a website with Node.JS and GitHub Actions", href:"https://palewi.re/docs/coding-the-news/scripts/week-2/"},
  ];
</script>

<!-- This sets the page title in the browser tab -->
<svelte:head>
  <title>{headline} | NYCity News Service</title>
  <meta name="description" content="At the Craig Newmark Graduate School of Journalism at the City University of New York, change is in our DNA. That comes of being born in 2006, as the digital revolution was transforming our profession in ways none of us could have imagined." />
</svelte:head>

<!-- Your page content goes here -->
<div class="container">
  
  <!-- Article Header: Headline, byline, and publication date -->
  <ArticleHeader
    {headline}
    {byline}
    {pubDate}
  />

  <!-- Lead Image: Animated gif of students at the journalism school -->
  <Image
    src="Screenshot 2026-02-07 at 2.24.28 PM.png"
    alt="Just days before moving out of 564 East 191st St., Emma, Ava, Katie, Gaby, Alice, and Lusa pose for Graduation pictures."
    caption="Just days before moving out of 564 East 191st St., Emma, Ava, Katie, Gaby, Alice, and Lusa pose for Graduation pictures."
    credit="Delainy Winter"
  />

  <!-- Article Body: The main story text with proper typography -->
  <ArticleBody>
    <p>
      Less than a year post grad, here's what the girls are up to:
    </p>

    <p>
      Emma is getting her masters degree in journalism from the Craig Newmark Graduate School of Journalism at CUNY and also works as an editorial assistant at People Inc..
    </p>

    <p>
      Ava is conducting nueroscience research at Northeastern University.
    </p>

    <p>
      Katie is attening Harvard Law School.
    </p>

    <p>
      Gaby works in marketing for AMC Networks.
    </p>

    <p>
      Alice is a paralegal.
    </p>

    <p>
      Lusa is a hostess at Moxy in Williamsburg.
    </p>

  </ArticleBody>

  <!-- Related Stories: Links to other articles -->
  <RelatedLinks
    title="Related Stories"
    links={relatedStories}
  />

</div>

<style>
  /* Styles here only apply to this page */
  .container {
    padding: var(--spacing-lg) var(--spacing-md);
  }
</style>