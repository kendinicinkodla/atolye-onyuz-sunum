.. slide:: CSS
   :class: contents

   .. container:: flex flex-col justify-center

      - genel yapı
      - yazı stilleri
      - renkler
      - yerleştirme


.. slide:: Yazı tipi stili

   .. container:: ref

      ::

        font-style: STİL;

   - ``normal``, ``italic``

   .. container:: columns

      .. container:: column w-1/4

         .. image:: font-style-before.*

      .. container:: column

         .. code-block:: css

            em {
              font-style: normal;
            }

      .. container:: column w-1/4

         .. image:: font-style-after.*

   .. speaker-notes::

      - Vurgunun normal metinden farkı kalmadı, şimdi değiştireceğiz.


.. slide:: Yazı tipi ağırlığı

   .. container:: ref

      ::

        font-weight: AĞIRLIK;

   - ``normal``, ``bold``
   - ``400``, ``700``

   .. container:: columns

      .. container:: column w-1/4

         .. image:: font-style-before.*

      .. container:: column

         .. code-block:: css

            em {
              font-style: normal;
              font-weight: bold;
            }

      .. container:: column w-1/4

         .. image:: font-weight-after.*


.. slide:: Alt-üst çizgileri

   .. container:: ref

      ::

        text-decoration: ÇİZGİ;

   - ``none``, ``underline``, ``overline``, ``line-through``

   .. container:: columns

      .. container:: column w-1/4

         .. image:: font-style-before.*

      .. container:: column

         .. code-block:: css

            em {
              font-style: normal;
              text-decoration: underline;
            }

      .. container:: column w-1/4

         .. image:: text-decoration-after.*

   .. speaker-notes::

      - Altçizginin kötü görünümünden söz et (``g`` harflerini göster).


.. slide:: Metin rengi

   - ayar ismi: ``color``
   - RGB değer

   .. code-block:: css

      em {
        font-style: normal;
        color: #c00000;
      }


.. slide:: Arka plan rengi

   - ayar ismi: ``background-color``

   .. speaker-notes::

      Altlıklta şunları değiştirsinler:

      - arka plan rengi
      - metin rengi
      - metin hizalaması
      - yazı tipi boyu


.. slide:: Satır aralığı

   - ayar ismi: ``line-height``

   .. code-block:: css

      body {
        font-family: 'Arial', 'Helvetica', sans-serif;
        font-size: 16px;
        line-height: 1.5em;
      }


.. slide:: Dış boşluklar

   - ayar ismi: ``margin``
   - ``-left``, ``-right``, ``-top``, ``-bottom``
   - belirtilmezse hepsi

   .. code-block:: css

      footer {
        margin-top: 4em;
      }


.. slide:: İç boşluklar

   - ayar ismi: ``padding``

   .. code-block:: css

      footer {
        margin-top: 4em;
        padding: 1em;
      }


.. slide:: İçiçe eleman seçimi

   - başka bir elemanın altındaki elemanlar

   .. code-block:: css

      header a {
        text-decoration: none;
        margin-left: 1em;
      }

   .. speaker-notes::

      Üstlükte şunları ayarlasınlar:

      - iç boşluklar

      - arka plan rengi

        - siyah arka plan seçerlerse beyaz logo

      - arka plan rengine uygun link rengi

      - linklerde ``text-transform: uppercase``

        - sayfa dilini Türkçe vermenin etkisini tartış
        - büyük harfe göre uygun yazı tipi boyu


.. slide:: Eleman kaydırma

   - ayar ismi: ``float``
   - bir elemanı sağa veya sola kaydırma
   - diğer elemanlar bunun etrafından "akar"

   .. code-block:: css

      header nav {
        float: right;
      }

   .. speaker-notes::

      - Navigasyona boşluk vermek iyi olabilir.

      ..

      - Bu yansıdan sonra ara verilebilir. HTML dosyasında değişiklikler
        gerekecek.


.. slide:: Eleman genişliği

   - ayar ismi: ``width``
   - uzunluk ölçüsü

   .. code-block:: css

      img {
        width: 200px;
      }

   .. speaker-notes::

      - Bütün resimler 200px oluyor.


.. slide:: Tek eleman seçme

   - eleman niteliği: ``id``
   - bütün sayfada tek bir tane olmalı

   ..

   - seçerken ``#`` ile nitelik değeri
   - eleman ismi verilmeyebilir


.. slide:: Tek eleman ayarı

   .. container:: columns

      .. container:: column mr-4

         .. code-block:: html

            <img src="logo.png"
                 id="logo"
                 alt="Doğa Kaşifleri logosu"/>

            <img src="karga.jpg"
                 id="poster"
                 width="640"
                 alt="Karga"/>

      .. container:: column

         .. code-block:: css

            img#logo {
              width: 200px;
            }

            img#poster {
              width: 100%;
            }


.. slide:: Çoklu eleman seçme

   - eleman niteliği: ``class``
   - birden fazla eleman seçebilir

   ..

   - seçerken ``.`` ile nitelik değeri
   - eleman ismi verilmeyebilir


.. slide:: Eleman sınıfı ayarı

   .. container:: columns

      .. container:: column mr-4

         .. code-block:: html

            <tr>
              <th>Alem:</th>
              <td>Hayvanlar</td>
            </tr>
            <tr class="cift">
              <th>Şube:</th>
              <td>Kordalılar</td>
            </tr>
            <tr>
              <th>Sınıf:</th>
              <td>Kuşlar</td>
            </tr>
            <tr class="cift">
              <th>Takım:</th>
              <td>Ötücü kuşlar</td>
            </tr>

      .. container:: column

         .. code-block:: css

            tr.cift {
              background-color: #e0e0e0;
            }

   .. speaker-notes::

      Tablo görünümünü düzelt:

      - ``table { border-collapse: collapse }``
      - ``td, th { padding: 0.5em }``

      Tasarım üzerinden yerleştirmeyi tartış:

      - büyük resimde ve başlıkta marjin yok
      - altında var
      - nasıl marjin verip hizalayacağım?


.. slide:: Eleman gruplama

   - gruplama elemanı: ``div``
   - çoğu zaman ``class`` niteliğiyle kullanılır


.. slide:: Eleman gruplama

   .. code-block:: html

      <div class="bilgi">
        <table>
          ...
        </table>
        <section>
          <p>İri yapılı, ...</p>
        </section>
        <section>
          <h2>Beslenme</h2>
          ...
        </section>
        <section><h2>Türler</h2>...</section>
        <section><h2>Galeri</h2>...</section>
      </div>


.. slide:: Maksimum genişlik

   - ayar ismi: ``max-width``
   - ``margin`` için ``auto`` değeri ortaya hizalar

   .. code-block:: css

      .bilgi {
        max-width: 50em;
        margin: 0 auto;
      }


.. slide:: Paragraf içi grup

   - gruplama elemanı: ``span``

   .. code-block:: html

      <p><span class="ilk-harf">İ</span>ri yapılı, düz gagalı,
        pençeli, ...</p>

   .. code-block:: css

      .ilk-harf {
        float: left;
        font-family: 'Georgia', serif;
        font-size: 3em;
        line-height: 1em;
        padding-right: 0.15em;
      }


.. slide:: Sütunlar

   - birden fazla sütun oluşturma

   ..

   - ayar ismi: ``display``
   - ayar değeri: ``flex``

   .. speaker-notes::

      - galeri resimleri için hangi elemanları gruplayacağım?


.. slide:: Eleman gruplama

   .. code-block:: html

      <section>
        <h2>Galeri</h2>

        <div class="galeri">
          <figure>
            <img src="..."/>
            <figcaption>...</figcaption>
          </figure>

          <figure>
            <img src="..."/>
            <figcaption>...</figcaption>
          </figure>
        </div>
      </section>


.. slide:: Sütun ayarı

   .. code-block:: css

      .gallery {
        display: flex;
      }

      .gallery figure {
        width: 25%;
      }

      .gallery img {
        width: 100%;
      }

   .. speaker-notes::

      - resimler küçük, yanlarda çok boşluk var
      - ``.galeri figure { margin-left: 0; margin-right: 0; }``
      - resimlerin arasında boşluk kalmadı: ``.galeri figure { width: 22%; }``
      - boşluğu aralara dağıt: ``.galeri { justify-content: space-between; }``

      ..

      - resim altı yazılarını ortaya hizalasınlar
      - yuvarlak köşeli resimler: ``.galeri img { border-radius: 10%; }``

      ..

      - tabloyu ikinci sütuna alsınlar

      Başlıkta şunları değiştirsinler:

      - resme bitişsin
      - arka plan rengi olsun
      - metin ile hizalansın
      - yazı tip boyu büyüsün


.. slide:: Family Guy
   :noheading:

   .. container:: h-full flex justify-center items-center

      .. image:: family_guy.*

   .. speaker-notes::

      - CSS'i yönetmek zor
      - tarayıcılar arasında farklar olabiliyor
      - şu anda boya göre kendini ayarlıyor ama düzen değiştirmiyor
      - cep telefonunda tabloyu hala sağda çıkarmasın, aşağı devam etsin
      - hazır paketler yardımcı oluyor: gelecek oturum Bulma
