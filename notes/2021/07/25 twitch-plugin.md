# 2021-07-25 Twitch Streaming


> Subject: [Coding] twitch plugin for OBS - TypeScript / React.js / Next.js / Monorepo

<!--  
const div = document.querySelector('.sc-AxjAm .iltvOi');
div.innerText = 'https://hackmd.io/@koshuang/twitch-streaming';
div.style.fontSize='18px';
-->

<style>
#zombie {
  width: 80px;
}
</style>

Goal: 

- Can interact easilier with listeners
- Show something when someone follows
  - By using [streamlabs `Alert Box`](https://streamlabs.com/obs-widgets/alert-box)

## Agenda

1. Create a new repo from `Create React App`
2. Trying nodecg: https://github.com/nodecg/nodecg
3. Watch Youtube Videos
  - Better than StreamElements?! How to build your own with NodeCG: https://www.youtube.com/watch?v=APvl1OJvYxg
  - Parcel up with a bow - NodeCG with ParcelJS: https://www.youtube.com/watch?v=AjhDpCNNomw
4. Create a nodecg git repo
5. Create a twitch app
  - getting client id
  - setting redirect url: `http://localhost:8080`
  - getting user_id / channel_id
    - 697479002
6. Create a twitch pubsub example
  - doing oauth
  - setting scope: `user_read+chat:read+bits:read+whispers:read+channel:moderate`
  - setting topics: `channel-bits-events-v2.4602499`

## References
- 殭屍圖: 	![](https://streamlabs.com/images/gallery/default.gif)
- validate twitch oauth token: https://id.twitch.tv/oauth2/validate
- twitch npm api: https://github.com/twurple/twurple
- obs plugin with Preact: https://github.com/HorusGoul/preact-obs-plugin
- obs-browser: https://github.com/obsproject/obs-browser
- twitch pubsub (websock) 
  - API docs: https://dev.twitch.tv/docs/pubsub
  - examples:
    - https://github.com/BarryCarlyon/twitch_misc/tree/main/pubsub
    - https://github.com/twitchdev/pubsub-javascript-sample