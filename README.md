# PWA - Progressive Web Application

- ## Pwa Nedir

  ### Pwa ile tek bir codebase üzerinden web,mobil ve masaüstü uygulamalar üretebiliriz.

  ### Kullanıcı siteye ilk kez girdiğinde karşısına bir dialog çıkar bu dialogta eğer onay verirse uygulamanın kısa yolu telefona kayıt edililir. Veya ayarlar kısmından bu sayfayı kaydet seçeneğini kullanarak kısayol oluşturabilir.

  ![dialog](https://i.pinimg.com/originals/16/3f/3f/163f3f034cc07ef569fc0c1ef1a9cd26.png)

  ### Karşımıza bunun gibi bir mesaj çıkar.

  ### Aynı bilgisayar üzerinde masaüstüne kayıt edip desktop versiyon olarak kullabiliriz.

  ### Pwa uygulamamızı Google Play Store için de yükleyebiliriz.

  [https://medium.com/@firt/google-play-store-now-open-for-progressive-web-apps-ec6f3c6ff3cc](Google Play Store now open for Progressive Web Apps)`
  **(Ama appstore üzerinde yayımlanmıyor yine de kısayol olarak kayıt edilebilir)**

- ## Gereklilikler

  ### manifest.json dosyası oluşturma

  ### manifest.json dosyasında uygulama hakkında bilgiler ve ikonların çeşitli boyutları olacak

  ```
      {
          "theme_color": "#006994",
          "background_color": "#006994",
          "display": "standalone",
          "scope": "/",
          "start_url": "/",
          "name": "Travel",
          "short_name": "Travel",
          "description": "Travel Point on map",
          "icons": [
              {
                  "src": "/icon-192x192.png",
                  "sizes": "192x192",
                  "type": "image/png"
              },
              {
                  "src": "/icon-256x256.png",
                  "sizes": "256x256",
                  "type": "image/png"
              },
              {
                  "src": "/icon-384x384.png",
                  "sizes": "384x384",
                  "type": "image/png"
              },
              {
                  "src": "/icon-512x512.png",
                  "sizes": "512x512",
                  "type": "image/png"
              }
          ]
      }
  ```

  ### manifest.json dosyamızın yolunu **head** içerisinde vereceğiz.

  ```
      <link rel="manifest" href="/manifest.json" />
      <meta name="theme-color" content="#006994" />
  ```

  ### Apple telefonlar için gereklilik:

  `<link rel="apple-touch-icon" href="/icon-192x192.png"></link>`

  ### Şimdi uygulamanın kısayolunu telefonumuza kayıt edebiliriz.

  ### [Next.js üzerinde kullanmak](https://github.com/vercel/next.js/tree/canary/examples/progressive-web-app)

  ### Google Chrome DevTools'ta Lighthouse kullanılarak PWA gerekliliklerini sağlayıp sağlayamadığını kontrol edebiliriz.
