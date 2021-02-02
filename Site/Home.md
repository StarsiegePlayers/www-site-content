---
    layout: false
    title: Home
    file: Site/Home.md
    description: Starsiegeplayers.com Home Page
---

<script>
    import DiscordOnline from "../../src/components/DiscordOnline.svelte";
    import News from "../../src/components/News.svelte";
    import TileGroup from "../../src/components/TileGroup.svelte";
    import HomeData from "../../src/store/home";
</script>

::: div row
    ::: div col-md-8
        <TileGroup tiles={HomeData.TileData} />
    :::
    ::: div col-md-4
        <DiscordOnline guildID={HomeData.Discord.GuildID} invite={HomeData.Discord.Invite} theme={HomeData.Discord.Theme}/>
    :::
:::

<News header="Community News" limit=10 />
