# cofre283
{
  "name": "Cofre 283 • 2027",
  "short_name": "Cofre 283",
  "start_url": "./",
  "display": "standalone",
  "background_color": "#07111f",
  "theme_color": "#07111f",
  "description": "Desafio de economia de 283 depósitos e calendário mensal",
  "icons": [
    {
      "src": "icon-192.png",
      "sizes": "192x192",
      "type": "image/png"
    },
    {
      "src": "icon-512.png",
      "sizes": "512x512",
      "type": "image/png"
    }
  ]
}
const CACHE='cofre283-2027-cache-v1';const FILES=['./','./index.html','./manifest.json','./icon-192.png','./icon-512.png'];self.addEventListener('install',e=>e.waitUntil(caches.open(CACHE).then(c=>c.addAll(FILES))));self.addEventListener('activate',e=>e.waitUntil(self.clients.claim()));self.addEventListener('fetch',e=>e.respondWith(caches.match(e.request).then(cached=>cached||fetch(e.request))));
