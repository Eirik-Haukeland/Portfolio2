<script>
  import holidazeImg from './assets/holidaze-09-03-24.png'
  import ShopATonImg from './assets/shop-a-ton-2024-03-09.png'
  import gotStoreImg from './assets/got-store-2024-03-09.png'
  import Card from './components/Card.svelte'

  const pagesInfo = [
    {
      imgSrc: holidazeImg,
      imgAlt: 'image of home page for "holidaze"',
      projectTitle: 'holidaze',
      desc: 'holidaze is a site for booking hotells and other holiday venues',
      repoUrl: 'https://github.com/Eirik-Haukeland/ProjectExam2',
      liveUrl: 'https://main--ebhholidaze.netlify.app/',
    }, 
    {
      imgSrc: gotStoreImg,
      imgAlt: 'image of home page to "Got Store"',
      projectTitle: 'Got Store',
      desc: 'Got Store is a webshop',
      repoUrl: 'https://github.com/Eirik-Haukeland/front-end-frameworks-ca',
      liveUrl: 'https://main--astounding-kleicha-407922.netlify.app/',
    }, 
    {
      imgSrc: ShopATonImg,
      imgAlt: 'this is a image of the home page for "Shop a Ton"',
      projectTitle: 'Shop a Ton',
      desc: 'shop a ton is a auction site where you can by and sell.',
      repoUrl: 'https://github.com/Eirik-Haukeland/semester-project-2',
      liveUrl: 'https://eirik-haukeland.github.io/semester-project-2/',
    }, 
  ]
</script>

<main class="flex flex-col gap-7 w-fit mt-7 mx-auto">
  <section class="flex flex-col gap-3">
    <h1 class="text-4xl sm:text-5xl 2xl:text-6xl font-bold">Portfolio Page</h1>
    <a href="https://github.com/Eirik-Haukeland" class="text-blue-500 hover:text-blue-800 focus:text-blue-800 2xl:text-xl">for: Eirik Berget Haukeland</a>
  </section>
  <section class="grid gap-4 grid-cols-1 sm:grid-cols-2 lg:grid-cols-3">
    {#each pagesInfo as page (page.projectTitle)}
      <Card
        imgSrc={page.imgSrc}
        imgAlt={page.imgAlt}
        projectTitle={page.projectTitle}
        desc={page.desc}
        repoUrl={page.repoUrl}
        liveUrl={page.liveUrl} />
    {/each}
  </section>
</main>
