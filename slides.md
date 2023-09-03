---
theme: seriph
background: /intro.png
class: text-center
lineNumbers: false
info: |
  ## Slidev Starter Template
drawings:
  persist: false
transition: slide-left
title:  
---
<style>
.slidev-layout.cover {
  background-image: linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 0)), url(/intro.png) !important; 
}
</style>
---
layout: default
---

<div>
  <img src="personalinfo.png">
</div>



---
transition: fade-out
layout: image-right
image: ./shiwa-id-Uae7ouMw91A-unsplash.jpg
---

# Native App First

Create a native app first as primary user experience of your app

<br>

```text {all|1|3|5|7|all}
💅🏻 Richer UI Interface

💪 More Computation Power

🔎 Easy to Find on Stores

📱 Easy to Start/Open
```
---
transition: fade-out
layout: image-right
image: ./faizur-rehman-dJpupM4LiS4-unsplash.jpg
---
# But Web Applications Evolved...

Thanks to PWAs, web applications became very similar to mobile apps

<br>

<cite>
A progressive web app (PWA) is an app that's built using web platform technologies, but that provides a user experience like that of a platform-specific app.
<br><br>Mozilla Docs
</cite>

<!-- 
- We can install PWAs on a user phone
- Offline Apps are possible 
- UX is almost identical to native apps
-->

---
transition: fade-out
layout: default
---

<div grid="~ cols-3 gap-4">
  <div>
    <div v-click="1">
      <img src="nativeTweetter.png" alt="phone" />
    </div>
    <div v-click="2">
      <div class="size_1">
        <img src="nativeSize.png" alt="phone" />
      </div>
    </div>
  </div>
  <div>
    <img src="phone.png" alt="phone" />
  </div>
  <div>
    <div v-click="1">
      <img src="pwaTweeter.jpg" alt="phone" />
    </div>
    <div class="size_2" v-click="2">
      <div>
        <img src="pwaSize.png" alt="phone" />
      </div>
    </div>
  </div>
</div>

<style>
.size_1 {
    position: absolute;
    bottom: 90px;
    left: 100px;
    width: 200px;
}
.size_2 {
    position: absolute;
    bottom: 90px;
    right: 95px;
    width: 200px;
}
</style>


---
transition: fade-out
layout: image-left
image: ./sarah-dorweiler-QeVmJxZOv3k-unsplash.jpg
---


# Web Application's Extra Benefits

<br>

```text {all|1|3|5|7|9|11|all}
✅ No store approval dependencies 

🛠️ Easier to mantain

💰 Lower development costs

🪽 Smaller memory footprint

🏎️ Faster live on the market

```

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/guide/syntax#embedded-styles
<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>
-->

---
transition: fade-out
layout: image
image: ./managelayout.png
---


<div class="logo">
  <img src="logoTweet.png">
</div>

---
transition: fade-out
layout: default
---

# Web Manifest

<br> 

```html {all|3}
<html lang="en">
  <head>
    <link rel="manifest" href="manifest.json" />
    <!-- ... -->
  </head>
  <body></body>
</html>
```

<!--
The web manifest is a JSON file containing a collection of properties, each of which defines some aspect 
of the PWA's appearance .
-->

---
transition: fade-out
layout: default
---

# Web Manifest

```json {all|2-3|6|7|8|9-22|all}
{
  "name": "angular-pwa",
  "short_name": "angular-pwa",
  "theme_color": "#1976d2",
  "background_color": "#fafafa",
  "display": "standalone",
  "scope": "./",
  "start_url": "./",
  "icons": [
    {
      "src": "assets/icons/icon-192x192.png",
      "sizes": "192x192",
      "type": "image/png"
      "purpose": "maskable"
    },
    {
      "src": "assets/icons/icon-512x512.png",
      "sizes": "512x512",
      "type": "image/png",
      "purpose": "maskable"
    }
  ]
}
```

<div v-click>
  <img src="installpwa.jpg" alt="phone" />
</div>

<arrow v-click x1="460" y1="480" x2="590" y2="480" color="#e9ff00" width="3" arrowSize="1" />

<style>
img {
  position: absolute;
  top: 20px;
  right: 115px;
  width: 250px;
}

.slidev-vclick-target {
  transition: opacity 200ms ease;
}

.slidev-vclick-hidden {
  opacity: 0;
  pointer-events: none;
}
</style>

---
transition: fade-out
layout: default
---

# Shortcuts

We can add <i>shortcuts</i> to the web manifest to enhance the user's engagement

<br>

<div grid="~ cols-2 gap-6">

  <img src="shortcuts.png" alt="phone" />

  <div v-click>
    <img src="shortcuts2.jpg" alt="phone" />
  </div>
</div>

<style>
.slidev-layout {
  padding-top: 0;
}

img {
  height: 100%;
  width: 250px;
}
</style>

<!--
<h2>We can add a shortcuts array in the manifest file to create direct links (shortcuts) to specific
actions of our PWA. <br><br>This way the user can access a desired funbctionality with just one click. No
need to browse through the application.</h2>
-->

---
transition: fade-out
layout: image
image: ./manageperf.png
---


<div class="logo">
  <img src="logoTweet.png">
</div>

<!-- 
<h1>So far we saw how it is possible to define the layout of our PWAs and how it is possible to make them <i>installable</i> </h1> 
 -->

---
transition: fade-out
layout: default
---

# Service Workers & Caching Strategies

<br>

Service Workers allow to optimise our web applications' performance, introducing:
<br><br>

<v-click>
  <h4> ✅ <span class="highlight">Local Caching</span> for static assets and network requests</h4>
</v-click>
<br>
<v-click>
 <h4> ✅ <span class="highlight">Offline Capabilities</span></h4>
</v-click>
<br>
<v-click>
 <h4> ✅ <span class="highlight">Advanced Business Logic</span> thanks to different caching strategies</h4>
</v-click>

<!-- 
<h3>Service workers are similar to web workers, running on a separate thread than the one used by our web application. But they
have the specific task to intercept all the traffic from and to our application. A sort of proxy.
</h3>

<h4>caching: for quick responses, no need to go over the network
<br><br>
offline: as the requested assets are already on the client side, we can deliver them even without an internet connection
<br><br>
caching strategies allow to cover complex scenarios to retrieve data from the server and delivber it to the client in an optimal way
</h4> 
 -->

---
transition: fade-out
layout: default
---

# Registering a Service Worker

<br>

```ts {all|1|3|5-7|8-10|11-13|all}
  if ("serviceWorker" in navigator) {
    try {
      const registration = await navigator.serviceWorker.register("/serviceWorker.js", { scope: "./"});

      if (registration.installing) {
        // Service worker is installing...

      } else if (registration.waiting) {
        // Service worker is now installed and waits to be activated!

      } else if (registration.active) {
        // Service worker has been actived.
      }
    } catch (error) {
      console.error(`Registration failed with error: ${error}`);
    }
  }
```

<!--
Waiting: SW remains in this state until there are no more pages under the control of the old SW. The browser can this way ensure that only 1 version is running at the time.
-->

---
transition: fade-out
layout: default
---

# Caching Strategies
We can implement different strategies according to our needs:
<br><br>

<div v-click>
  <h5><span class="highlight">Cache First</span>: maximize performance & allows offline behaviour</h5>
</div>
<br>

<div v-click>
 <h5><span class="highlight">Network First</span>: preference for fresh data, but allows to fallback to cache</h5>
</div>
<br>

<div v-click>
 <h5><span class="highlight">Stale While Revalidate</span>: hybrid solution, allowing quick responses with <i>fresher</i> data</h5>
</div>

<style>
  b {
    color: var(--slidev-theme-primary);
  }
</style>

---
transition: fade-out
layout: default
---

# Stale While Revalidate

```ts {all|5-6|17|7-14|17|all}
    self.addEventListener('fetch', (event) => {
      event.respondWith(
        (async function () {

          const cache = await caches.open('cache_V1');
          const cachedResponse = await cache.match(event.request);
          const serverResponsePromise = fetch(event.request);

          event.waitUntil(
            (async function () {
              const serverResponse = await serverResponsePromise;
              await cache.put(event.request, serverResponse.clone());
            })(),
          );

          // Provide the response in the cache if available or fetch it from the server, otherwise.
          return cachedResponse || serverResponsePromise;
        })(),
      );
    });
```
<div class="cache">
  <img src="stalecache.png" />
</div>


<style>
.cache {
    img {
    position: absolute;
    top: 100px;
    right: 60px;
    width: 330px;
  }
}
</style>

<!--
We implement caching strategies inside our SW file. The SW can listen to fetch events and, depending  to the strategy implemented, act accordingly. 

https://jakearchibald.com/2014/offline-cookbook/#stale-while-revalidate
-->

---
transition: fade-out
layout: image
image: ./demooffline.png
---

<div class="logo">
  <img src="logoTweet.png">
</div>

<div class="angular">
  <img src="angular-logo.png">
</div>

<div class="firestore">
  <img src="firebase-logo.png">
</div>

<style>
  .angular {
    position: absolute;
    left:50px;
    bottom:300px;
    width:100px;
  }
  .firestore {
    position: absolute;
    left:50px;
    bottom:150px;
    width:100px;
  }
</style>

<!-- Show in demo: 
- Angular + Firestore
- Standalone App
- APGT (?)
- Going offline + Auto Sync -->

---
transition: fade-out
layout: image
image: ./webapi.png
---

---
transition: fade-out
layout: default
---

<div class="logso">
  <img src="webcando.png">
</div>

<div class="url">
  <h4>https://whatwebcando.today/</h4>
</div>

<div class="logo">
  <img src="logoTweet.png">
</div>

<style>
.url {
  position: absolute;
  top: 155px;
  right: 150px;
  color: #585858;
}
</style>

---
transition: fade-out
layout: image
image: ./light.png
---

<div class="logo">
  <img src="logoTweet.png">
</div>


---
layout: image
image: ./bread.png
---


<div class="logo">
  <img src="logoTweet.png">
</div>

---
transition: fade-out
layout: image
image: ./lock.png
---

<div class="logo">
  <img src="logoTweet.png">
</div>


---
transition: fade-out
layout: image
image: ./limits.png
---

<!-- 
Limits of PWAs
https://www.luxidgroup.com/blog/the-limitations-of-pwas 

Web Push Notifications iOS 16.4, Apple has finally delivered its promise
-->

---
transition: fade-out
layout: image
image: ./future.png
---

<div class="logo">
  <img src="logoTweet.png">
</div>


---
transition: fade-out
layout: image
image: ./thanks.jpg
---

---
layout: default
---

<div>
  <img src="personalinfo_end.png">
</div>
