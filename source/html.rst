.. slide:: Önyüz Geliştirme
   :subtitle: HTML
   :class: title
   :data-x: 0
   :data-rel-x: 1050

   .. container:: copyright

      \H. Turgut Uyar

      Mart 2019


.. slide:: İçindekiler
   :class: contents

   - *genel yapı*
   - sayfa şablonu
   - içerik elemanları
   - gövde şablonu


.. slide:: HTML

   - *HyperText Markup Language*

   ..

   - düz metin

   .. container:: substep task

      - ilk dosyamızı oluşturalım
      - içine hayvanın ismini yazalım

   .. container:: substep task

      - ilk paragrafı ekleyelim

   .. speaker-notes::

      - Türkçe harflerin bozuk çıktığına dikkat çek.


.. slide:: Boşluklar
   :data-views: (200, 0, 0, 0.5)

   - fazladan boşlukların etkisi yok

   .. container:: columns

      .. container:: column w-1/2

         .. code-block:: html

            Karga

            İri yapılı, düz gagalı,
            pençeli, tüyleri çoğunlukla
            siyah, yüksek ve rahatsız
            edici sesli kuş. Daha büyük
            ve genellikle leş yiyici
            olanlarına "karakarga" veya
            "kuzgun" denir.

      .. container:: column w-1/2

         .. image:: images/karga_bosluklar.*
            :alt: Boşlukların etkisi olmadığından yazı tek blok halinde.


.. slide:: Düz metin yetersiz

   - başlığı nasıl belirteceğim?
   - nasıl tablo yapacağım?
   - bir yeri nasıl vurgulayacağım?

   ..

   - işaretler koyalım


.. slide:: İşaretleme

   - | işaretlemek istediğimiz yerin başına ve sonuna
     | *etiketler* yazıyoruz:

   .. code-block:: xml

      <etiket>işaretlenen bölge</etiket>

   ..

   - her etiket çifti bir *eleman* işaretliyor


.. slide:: Temel elemanlar
   :data-views: (-150, 150, 0, 0.5)

   - başlık: ``h1``
   - paragraf: ``p``

   .. container:: columns

      .. container:: column w-1/2

         .. code-block:: html

            <h1>Karga</h1>

            <p>İri yapılı, düz gagalı,
              pençeli, tüyleri çoğunlukla
              siyah, yüksek ve rahatsız
              edici sesli kuş. Daha büyük
              ve genellikle leş yiyici
              olanlarına "karakarga" veya
              "kuzgun" denir.</p>

      .. container:: column w-1/2

         .. image:: images/karga_etiketler.*
            :alt: Paragraf ve başlık elemanlarının kullanımı.

   .. speaker-notes::

      - Boşlukların düzeldiğine dikkat çek.


.. slide:: İçiçe elemanlar

   - bir elemanın içine başka bir eleman konabilir
   - sonra açılan eleman önce kapanmalı

   .. container:: columns items-center

      .. container:: column

         .. code-block:: xml

            <dış>dış bölge<iç>iç bölge</iç>dış bölge</dış>

      .. container:: column

         .. code-block:: xml

            <dış>
              dış bölge
              <iç>
                iç bölge
              </iç>
              dış bölge
            </dış>

   .. speaker-notes::

      - Editörde kod katlama özelliğini kullanarak açma/kapama etiketlerinin
        nasıl eşleştiklerini göster.


.. slide:: Vurgu
   :data-views: (-150, 200, 0, 0.5) (300, -100, 0, 0.25)

   - vurgu: ``em``
   - normalde italik gösterilir

   .. container:: columns

      .. container:: column w-1/2

         .. code-block:: html

            <h1>Karga</h1>

            <p>İri yapılı, düz gagalı,
              pençeli, tüyleri çoğunlukla
              siyah, yüksek ve rahatsız
              edici sesli kuş. Daha büyük
              ve genellikle leş yiyici
              olanlarına <em>karakarga</em>
              veya <em>kuzgun</em> denir.</p>

      .. container:: column w-1/2 ml-8

         .. image:: images/karga_vurgu.*
            :alt: Vurgu elemanının italik gösterilimi.


.. slide:: Boş elemanlar

   - bazı elemanların kapanış etiketi yok:

   .. code-block:: xml

      <etiket/>


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


.. slide:: İçindekiler
   :class: contents

   - genel yapı
   - *sayfa şablonu*
   - içerik elemanları
   - gövde şablonu


.. slide:: Sayfa elemanları

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

   .. container:: substep task

      - ömür ve ilginç bilgi paragraflarını ekleyelim


.. slide:: Baş

   - sayfa bilgileri

   ..

   - sayfa başlığı
   - sayfanın yazarı, tarihi, telif hakkı, ...

   .. container:: substep

      - hangi harflerle yazıldığı: ``charset``


.. slide:: Harf tabloları
   :data-views: (200, 0, 0, 0.5)

   - hangi sayı hangi harfe karşı düşecek?
   - en yaygın kullanılan tablo: ``utf-8``

      .. container:: columns mt-8

         .. container:: column w-1/2

            .. code-block:: html

               <head>
                 <meta charset="utf-8"/>
               </head>

         .. container:: column w-1/2

            .. image:: images/karga_charset.*
               :alt: Harf tablosu belirtilince Türkçe harfler doğru çıkıyor.

   .. speaker-notes::

      - Türkçe harflerin düzeldiğine dikkat çek.
      - Editörün kullandığını seçmek gerektiğini vurgula.


.. slide:: Sayfa başlığı

   - sayfa başlığı: ``title``

   .. code-block:: html

      <head>
        <meta charset="utf-8"/>
        <title>Doğa Kaşifleri - Karga</title>
      </head>

   .. speaker-notes::

      - Başlığın nerede göründüğünü sor.


.. slide:: İçindekiler
   :class: contents

   - genel yapı
   - sayfa şablonu
   - *içerik elemanları*
   - gövde şablonu


.. slide:: Altbaşlıklar

   - | 6 düzey başlık var:
     | ``h1``, ``h2``, ``h3``, ``h4``, ``h5``, ``h6``

   .. container:: substep task

      - beslenme altbölümünü sayfaya ekleyelim


.. slide:: Bağlantılar

   - bağlantı: ``a``
   - hedef adres niteliği: ``href``
   - normalde mavi renkte ve altı çizili gösterilir


.. slide:: Bağlantılar
   :data-views: (20, 140, 0, 0.75)

   .. code-block:: html

      <p>Kargalar tuhaf sesleri, siyah renkleri, parlak cisimlere olan
        düşkünlükleri ile bilinirler.
        <a href="https://awesci.com/ultimate-problem-solving-crow/">Bazı
        araştırmalar</a> kargaların çok zeki olduklarını
        göstermektedir.</p>

   .. container:: text-center mt-8

      .. image:: images/karga_baglanti.*
         :alt: Seçilen sözcükler bağlantının metnini oluşturuyor.

   .. speaker-notes::

      - Link adresi sitedeki listeden kopyalanabilir.
      - Linkin metni ile adresinin farklı şeyler olduğunu vurgula.


.. slide:: Resimler

   - resim: ``img``
   - adres niteliği: ``src``
   - genişlik ve yükseklik nitelikleri: ``width``, ``height``
   - yerine konacak metin niteliği: ``alt``

   .. speaker-notes::

      - Genişlik ve yükseklik için dosyanın orijinal boyutları verilmeli.
      - ``alt`` niteliğinin öneminden söz et: görme özürlü kullanıcılar.


.. slide:: Resimler

   .. code-block:: html

      <img src="karga.jpg"
           width="1280"
           height="427"
           alt="Bir parkta çimenlerin önüne konmuş bir karga."/>

   .. container:: w-2/3 m-auto mt-2

      .. image:: images/karga_foto.*
         :alt: Foto belirtilen boya ölçekli olarak yerleştirilir.

   .. container:: task substep

      - galeri altbölümüne küçük fotoların ilkini koyalım

   .. speaker-notes::

      - Foto adresi sitedeki listeden kopyalanabilir.
      - Küçük foto genişliği 128.


.. slide:: Şekiller

   - | şekiller değişik türden olabilir:
     | foto, resim, diyagram, ...

   ..

   - şekil: ``figure``
   - yazı eklemek istersek: ``figcaption``


.. slide:: Şekiller

   .. code-block:: html

      <figure>
        <img src="karga_1.jpg"
             width="128"
             height="128"
             alt="Foto 1"/>
        <figcaption>Foto 1</figcaption>
      </figure>

   .. container:: task substep mt-4

      - büyük fotoyu ``figure`` içine alalım, yazısı olmasın
      - bütün küçük resimleri ekleyelim

   .. speaker-notes::

      - ``figure`` olmasa ``img`` elemanları yanyana diziliyor
      - ``figure`` ayrıca resmin etrafına boşluk ekliyor


.. slide:: Listeler
   :data-views: (-100, 100, 0, 0.5) (300, 0, 0, 0.5)

   - sırasız liste: ``ul``
   - sıralı liste: ``ol``
   - liste maddesi: ``li``

   .. container:: columns

      .. container:: column w-1/2

         .. code-block:: html

            <h2>Türler</h2>

            <ul>
              <li>Avustralya kargası</li>
              <li>Orman kargası</li>
              <li>Küçük karga</li>
            </ul>

      .. container:: column

         .. image:: images/karga_liste.*
            :alt: Sırasız listeler maddeler halinde gösterilir.

   .. speaker-notes::

      - ``ul`` yerine ``ol`` kullanarak sıralı liste denesinler.
      - Hangisinin daha anlamlı olduğunu tartış.


.. slide:: Tablolar

   - tablo: ``table``
   - tablo satırı: ``tr``
   - tablo hücresi: ``td``
   - başlık hücresi: ``th``


.. slide:: Tablolar
   :data-views: (-100, 0, 0, 0.5) (250, -100, 0, 0.5)

   .. container:: columns

      .. container:: column w-1/2

         .. code-block:: html

            <table>
              <tr>
                <th>Sınıf:</th>
                <td>Kuşlar</td>
              </tr>
              <tr>
                <th>Familya:</th>
                <td>Kargagiller</td>
              </tr>
              <tr>
                <th>Cins:</th>
                <td>Corvus</td>
              </tr>
            </table>

      .. container:: column w-1/2

         .. image:: images/karga_tablo.*
            :alt: Sırasız listeler maddeler halinde gösterilir.

   .. speaker-notes::

      - ``td`` ile ``th`` elemanlarının görüntülenme farklarını tartış.


.. slide:: İçindekiler
   :class: contents

   - genel yapı
   - sayfa şablonu
   - içerik elemanları
   - *gövde şablonu*


.. slide:: Gövde şablonu

   - bir sitedeki sayfalar aynı şablona uyar

   ..

   - üstlük: logo, navigasyon menüsü, ...
   - ana içerik
   - altlık: site haritası, telif hakkı, ...


.. slide:: Gövde bileşenleri

   .. container:: columns

      .. container:: column mr-8

         .. code-block:: html

            <body>
              <header>
                ... logo, navigasyon, ...
              </header>

              <main>
                 ... ana içerik ...
              </main>

              <footer>
                ... site haritası, ...
              </footer>
            <body>

      .. container:: column

         - üstlük: ``header``
         - ana: ``main``
         - altlık: ``footer``

         .. container:: task substep m-0

            - ``body`` altındakileri ``main`` içine alalım

   .. speaker-notes::

      - Görüntülemeye bir etkisi yok.


.. slide:: Altlık
   :data-views: (250, 0, 0, 0.5)

   - altlığa ana içerikle aynı türden elemanlar yazılır

   .. container:: columns mt-12

      .. container:: column w-2/3

         .. code-block:: html

            <footer>
              <p>(C) 2019, Kendin için Kodla</p>
            </footer>

      .. container:: column

         .. image:: images/karga_altlik.*
            :alt: Altlık ana içerikle aynı şekilde görüntülenir.

   .. speaker-notes::

      - Görüntülemeye bir etkisi yok.
      - ``(C)`` yerine ``&copy;`` gösterilebilir.
      - Unicode sembol seçtirilebilir: shapecatcher.com


.. slide:: Üstlük
   :data-views: (200, 0, 0, 0.5)

   - üstlük de aynı şekilde

   .. container:: columns mt-12 mr-8

      .. container:: column w-2/3

         .. code-block:: html

            <header>
              <img src="logo_siyah.png"
                   width="434"
                   height="88"
                   alt="Doğa Kaşifleri logosu"/>
            </header>

      .. container:: column

         .. image:: images/karga_ustluk.*
            :alt: Üstlük de ana içerikle aynı şekilde görüntülenir.

   .. container:: substep task

      - logoyu ana sayfaya bağlantı haline getirelim

   .. speaker-notes::

      - Görüntülemeye bir etkisi yok.
      - Ana sayfanın bağlantı adresi: ``index.html``


.. slide:: Navigasyon
   :data-views: (250, 0, 0, 0.5)

   - navigasyon menüsü: ``nav``

   .. container:: columns mt-12 mr-4

      .. container:: column w-2/3

         .. code-block:: html

            <nav>
              <a href="turler.html">Hayvan türleri</a>
              <a href="oyun.html">Biliyor musun?</a>
            </nav>

      .. container:: column

         .. image:: images/karga_menu.*
            :alt: Navigasyona yalnızca linklerin yazılması yeterli.


.. slide:: Metin bölümleri

   - ana içerik bölümler içine alınabilir: ``section``

   .. code-block:: html

      <section>
        <h2>Galeri</h2>

        <figure>
          ...
        </figure>

        <figure>
          ...
        </figure>
      </section>

   .. speaker-notes::

      - Görünür bir etkisi yok.


.. slide:: Kapanış
   :noheading:
   :class: title

   birinci oturumun sonu
