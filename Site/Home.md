---
    layout: false
    title: Home
    file: Site/Home.md
    description: Starsiegeplayers.com Home Page

---

<script>
import HomeData from "../../src/store/home.js";
import TileGroup from "../../src/components/TileGroup.svelte";
import DiscordOnline from "../../src/components/DiscordOnline.svelte";
import News from "../../src/components/News.svelte";
</script>

::: div bg-primary rounded-3 boarder-3 p-4 mb-5

<img src="/static/img/logo.png" alt="Starsiege Players - Keeping the dream alive since 1999" />

<hr />

**Starsiege Players** is a dedicated community of individuals that have been playing, improving, and supporting the
Mecha-style game *Starsiege* since **1999**!

We are committed to proving a space for like-minded retro gamers, developers, historians, and archivists to create,
collaborate, discuss, and enjoy *Starsiege* the way it's meant to be played.

**Starsiege Players** is home to the official community patches of *Starsiege* that work on modern Windows computers and
is compatible with Windows 10

:::

::: div row

::: div col-md-8
<TileGroup tiles={HomeData.TileData} />
:::

::: div col-md-4
<DiscordOnline guildID={HomeData.Discord.GuildID} invite={HomeData.Discord.Invite} theme={HomeData.Discord.Theme}/>
:::

:::

::: div row
::: div col-md-8
<News header="Community News" limit=5 />
:::
:::
