

.. slide:: Bileşenler

   .. container:: columns

      .. container:: column flex flex-col items-center justify-center

         .. rst-class:: border-b-2 px-4

            içerik

         ..

         - yazılar
         - resimler
         - ...

      .. container:: column flex flex-col items-center justify-center

         .. rst-class:: border-b-2 px-4

            biçim

         ..

         - renkler
         - yazı tipleri
         - ...

   .. container:: columns substep mt-8

      .. container:: column flex flex-col items-center

         *HTML*

      .. container:: column flex flex-col items-center

         *CSS*


.. slide:: HTML
   :class: contents

   .. container:: flex flex-col justify-center

      - genel yapı
      - içerik elemanları


.. slide:: HTML

   - *HyperText Markup Language*

   ..

   - düz metin

   .. speaker-notes::

      - Katılımcılar ilk dosyalarını oluştursunlar (``karga.html``).
      - İçine herkes kendi hayvanının ismini yazsın.


.. slide:: Boşluklar

   - fazladan boşlukların bir önemi yok
   - bir boşluk, iki boşluk, elli boşluk fark etmiyor
   - boş satırlar da aynı şekilde

   .. code-block:: html

      Karga

      İri yapılı, düz gagalı, pençeli, tüyleri çoğunlukla
      siyah, yüksek ve rahatsız edici sesli kuş. Daha büyük
      ve genellikle leş yiyici olanlarına "karakarga" veya
      "kuzgun" denir.

   .. speaker-notes::

      - Herkes kendi hayvanının metin dosyasından paragrafını kopyalasın.
      - Boşlukların etkisini tartış.


.. slide:: Düz metin yetersiz

   - başlığı nasıl belirteceğim?
   - nasıl tablo yapacağım?
   - bir yeri nasıl vurgulayacağım?

   ..

   - işaretler koyalım


.. slide:: İşaretleme

   - işaretlemek istediğimiz yerin başına ve sonuna *etiketler* yazıyoruz

   ..

   - başlığı işaretleyelim: ``h1``

   .. code-block:: html

      <h1>Karga</h1>

      İri yapılı, düz gagalı, pençeli, tüyleri çoğunlukla
      siyah, yüksek ve rahatsız edici sesli kuş. Daha büyük
      ve genellikle leş yiyici olanlarına "karakarga" veya
      "kuzgun" denir.


.. slide:: Etiketler

   - açılış etiketi: ``<isim>``
   - kapanış etiketi: ``</isim>``

   ..

   - her etiket çifti bir *eleman* işaretliyor

   ..

   - bazı elemanların kapanış etiketi yok
   - açılış etiketi: ``<isim/>``


.. slide:: Paragraf

   - paragraf elemanı: ``p``

   .. code-block:: html

      <h1>Karga</h1>

      <p>İri yapılı, düz gagalı, pençeli, tüyleri çoğunlukla
        siyah, yüksek ve rahatsız edici sesli kuş. Daha büyük
        ve genellikle leş yiyici olanlarına "karakarga" veya
        "kuzgun" denir.</p>


.. slide:: Eleman nitelikleri

   - elemanların nitelikleri olabilir
   - açılış etiketinde belirtilir

   ..

   - örneğin elemanın hangi dilde olduğu: ``lang``

   .. code-block:: html

      <p lang="tr">İri yapılı, düz gagalı, pençeli, tüyleri
        çoğunlukla siyah, yüksek ve rahatsız edici sesli kuş.
        Daha büyük ve genellikle leş yiyici olanlarına
        "karakarga" veya "kuzgun" denir.</p>


.. slide:: İçiçe elemanlar

   - bir elemanın içine başka bir eleman konabilir
   - sonra açılan eleman önce kapanmalı

   ..

   - vurgu elemanı: ``em``

   .. code-block:: html

      <h1>Karga</h1>

      <p>İri yapılı, düz gagalı, pençeli, tüyleri çoğunlukla
        siyah, yüksek ve rahatsız edici sesli kuş. Daha büyük
        ve genellikle leş yiyici olanlarına <em>karakarga</em>
        veya <em>kuzgun</em> denir.</p>


.. slide:: Temel elemanlar

   - sayfanın ana elemanı: ``html``

   ..

   - içinde iki eleman bulunur:

     - ``head``: sayfayla ilgili bilgiler (baş)
     - ``body``: sayfanın içeriği (gövde)

   ..

   - | HTML dosyası olduğunu belirtmek için başa:
     | ``DOCTYPE``


.. slide:: Şablon

   .. code-block:: html

      <!DOCTYPE html>
      <html lang="tr">
        <head>
          ... sayfa bilgileri ...
        </head>
        <body>
          ... sayfa içeriği ...
        </body>
      </html>


.. slide:: Gövde

   - şu ana kadar yazdıklarımız gövdenin içinde

   .. code-block:: html

      <body>
        <h1>Karga</h1>

        <p>İri yapılı, düz gagalı, pençeli, tüyleri çoğunlukla
          siyah, yüksek ve rahatsız edici sesli kuş. Daha büyük
          ve genellikle leş yiyici olanlarına <em>karakarga</em>
          veya <em>kuzgun</em> denir.</p>
      </body>

   .. speaker-notes::

      - Giriş metninden geri kalan paragrafları sayfaya eklesinler
        (ikinci paragraf/ömür ve ilginç bilgi, henüz link yok).


.. slide:: Sayfa bilgileri

   - sayfa başlığı elemanı: ``title``
   - yazarı, tarihi, ...

   ..

   - hangi harflerle yazıldığı: ``charset``


   .. speaker-notes::

      - Harfleri sayılara karşı düşürme tablolarından söz et.


.. slide:: Baş

   .. code-block:: html

      <!DOCTYPE html>
      <html lang="tr">
        <head>
          <meta charset="utf-8"/>
          <title>Doğa Kaşifleri - Karga</title>
        </head>
        <body>
          ...
        </body>
      </html>

   .. speaker-notes::

      Başlığın nerede göründüğünü sor.


.. slide:: Altbaşlıklar

   - | 6 düzey başlık var:
     | ``h1``, ``h2``, ``h3``, ``h4``, ``h5``, ``h6``

   .. speaker-notes::

      - Beslenme altbölümünü sayfaya eklesinler.


.. slide:: Bağlantılar

   - bağlantı elemanı: ``a``
   - bağlanılacak adres niteliği: ``href``

   .. code-block:: html
      :class: text-4xl

      <p>Kargalar tuhaf sesleri, siyah renkleri, parlak cisimlere olan
        düşkünlükleri ile bilinirler.
        <a href="https://awesci.com/ultimate-problem-solving-crow/">Bazı
        araştırmalar</a> kargaların çok zeki olduklarını
        göstermektedir.</p>

   .. speaker-notes::

      - Link adresini sitedeki listeden kopyalayabilirler.


.. slide:: Resimler

   - resim elemanı: ``img``
   - resim adresi niteliği: ``src``
   - boy niteliği: ``width``
   - yerine konacak metin niteliği: ``alt``

   .. code-block:: html
      :class: text-4xl

      <img src="karga.jpg"
           width="640"
           alt="Karga"/>

   .. speaker-notes::

      - Foto adresini sitedeki listeden kopyalayabilirler.
      - ``alt`` niteliğinin öneminden söz et: görme özürlü kullanıcılar.


.. slide:: Şekiller

   - resim, diyagram, ...
   - şekil elemanı: ``figure``
   - yazı elemanı: ``figcaption``

   .. code-block:: html
      :class: text-4xl

      <figure>
        <img src="karga_1.jpg"
             width="200"
             alt="Foto 1"/>
        <figcaption>Foto 1</figcaption>
      </figure>

   .. speaker-notes::

      - Bütün küçük resimleri eklesinler.


.. slide:: Listeler

   - liste elemanı: ``ul``
   - liste maddesi elemanı: ``li``

   .. code-block:: html
      :class: text-4xl

      <h2>Türler</h2>

      <ul>
        <li>Avustralya kargası</li>
        <li>Orman kargası</li>
        <li>Küçük karga</li>
      </ul>

   .. speaker-notes::

      - ``ul`` yerine ``ol`` kullanarak sıralı liste denesinler.
      - Hangisinin daha anlamlı olduğunu tartış.


.. slide:: Tablolar

   - tablo elemanı: ``table``
   - tablo satırı elemanı: ``tr``
   - tablo hücresi elemanı: ``td``
   - başlık hücresi elemanı: ``th``


.. slide:: Tablo

   .. code-block:: html

      <table>
        <tr>
          <th>Alem:</th>
          <td>Hayvanlar</td>
        </tr>
        <tr>
          <th>Şube:</th>
          <td>Kordalılar</td>
        </tr>
        <tr>
          <th>Sınıf:</th>
          <td>Kuşlar</td>
        </tr>
      </table>

   .. speaker-notes::

      - ``td`` ile ``th`` elemanlarının görüntülenme farklarını tartış.


.. slide:: Sayfa şablonu

   - bir sitedeki sayfalar aynı şablona uyar

   ..

   - üstlük (``header``): logo, navigasyon
   - ana içerik (``main``)
   - altlık (``footer``): site haritası, telif hakkı, ...


.. slide:: Gövde bileşenleri

   .. code-block:: html

      <body>
        <header>
          ... logo, navigasyon, ...
        </header>

        <main>
           ... ana içerik ...
        </main>

        <footer>
          ... site haritası, telif hakkı, ...
        </footer>
      <body>

   .. speaker-notes::

      - ``body`` altındaki bütün içeriği ``main`` içine alsınlar.


.. slide:: Altlık

   .. code-block:: html

      <footer>
        <p>(C) 2019, Kendin için Kodla</p>
      </footer>

   .. speaker-notes::

      - ``(C)`` yerine ``&copy;`` göster.


.. slide:: Navigasyon

   - navigasyon elemanı: ``nav``

   .. code-block:: html

      <header>
        <nav>
          <a href="index.html">Ana sayfa</a>
          <a href="hayvan-turleri.html">Hayvan türleri</a>
          <a href="biliyor-musun.html">Biliyor musun?</a>
        </nav>
      </header>

   .. speaker-notes::

      - Logoyu üstlüğe eklesinler.
      - Logo ana sayfaya link olsun.


.. slide:: Metin bölümleri

   - ana içerik bölümler içine alınabilir: ``section``

   .. code-block:: html

      <section>
        <h2>Beslenme</h2>

        <p>Kargalar hemen hemen her şeyi yerler. Yetişkin bir karga
          günde 300 gramdan fazla yiyecek tüketir.
          Bilindiği kadarıyla kargalar ceviz, palamut, incir gibi
          orman ürünlerini de tüketirler. Onları tüketirken
          bir yandan da yayılmalarını sağlayarak doğaya katkıda
          bulunurlar.</p>
      </section>

   .. speaker-notes::

      - Giriş, türler ve galeri bölümlerini ``section`` içine alsınlar.
      - Galeri için ``h2`` başlık eklesinler.


.. slide:: CSS
   :class: contents

   .. container:: flex flex-col justify-center

      - genel yapı
      - yazı stilleri
      - renkler
      - yerleştirme


.. slide:: CSS

   - *Cascading Style Sheets*

   - düz metin


.. slide:: Stil bağlantısı

   - HTML dosyasının baş kısmında: ``link``
   - stil dosyası olduğunu belirtmek için: ``rel``
   - stil dosyası adresi: ``href``

   .. code-block:: html

      <head>
        <meta charset="utf-8"/>
        <title>Doğa Kaşifleri - Karga</title>
        <link rel="stylesheet" href="kik.css"/>
      </head>

   .. speaker-notes::

      - Boş ``kik.css`` dosyasını oluştursunlar ve bağlasınlar.


.. slide:: Stil ayarları

   - hangi elemanlara uygulanacak?
   - ayar ismi
   - ayar değeri

   .. code-block:: css

      eleman {
        ayar_ismi: ayar_değeri;
        ayar_ismi: ayar_değeri;
      }


.. slide:: Metin hizalama

   .. container:: ref

      ::

        text-align: HİZA_YÖNÜ;

   - ``left``, ``right``, ``center``, ``justify``

   .. container:: columns

      .. container:: column w-1/4

         .. image:: text-align-before.*

      .. container:: column

         .. code-block:: css

            th {
              text-align: left;
            }

      .. container:: column w-1/4

         .. image:: text-align-after.*


.. slide:: Yazı tipi

   .. container:: ref

      ::

        font-family: 'Seçenek 1', 'Seçenek 2', 'Seçenek 3';

   - her seçenek bir yazı tipi "ailesi"
   - sıradaki seçeneği bulamıyorsan sonrakine geç

   - | son seçenek şunlardan biri olmalı:
     | ``serif``, ``sans-serif``, ``monospace``

   .. speaker-notes::

      - Çoğu makinada bulunan yazı tiplerinden bahset: ``Arial``,
        ``Helvetica``, ``Georgia``, ...


.. slide:: Google Fonts

   - serbestçe kullanılabilecek yazı tipleri

   |

   - önce stil dosyasına alınmalı

   .. rst-class:: small

   .. code-block:: css

      @import url('https://fonts.googleapis.com/css?family=Cabin:400,700|Nunito:400,700');

   .. speaker-notes::

      - Google Fonts'dan biri gövde biri başlıklar için iki yazı tipi
        seçsinler. 400/700 (latin ext?).


.. slide:: Varsayılan yazı tipi

   - ``body`` elemanına uygulanırsa bütün sayfa için geçerli olur

   .. container::

      .. code-block:: css

         body {
           font-family: 'Cabin', sans-serif;
         }

   .. container:: columns mt-8

      .. container:: column w-1/2 text-center

         .. image:: font-family-before.*

      .. container:: column w-1/2 text-center

         .. image:: font-family-after.*


.. slide:: Çoklu elemanlar

   - birden fazla elemana aynı stil uygulanabilir
   - elemanları virgülle ayırarak

   .. container::

      .. code-block:: css

         h1, h2 {
           font-family: 'Nunito', sans-serif;
         }


.. slide:: Yazı boyu

   .. container:: ref

      ::

        font-size: BOYUT;

   - boyut çeşitli birimlerde verilebilir
   - ``px``
   - ``em`` --- geçerli boya göre ölçek


.. slide:: Yazı boyu

   .. container:: columns

      .. container:: column w-1/2

         .. code-block:: css

            body {
              font-family: 'Cabin', sans-serif;
              font-size: 18px;
            }

      .. container:: column w-1/2

         .. code-block:: css

            h1 {
              font-size: 2em;
            }

   .. container:: columns mt-8

      .. container:: column text-center

         .. image:: font-size-before.*

      .. container:: column text-center

         .. image:: font-size-after.*

   .. speaker-notes::

      - Asıl halinde ``h1`` boyu ``1.5em``.


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
