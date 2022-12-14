.. slide:: Önyüz Geliştirme
   :subtitle: HTML
   :class: title
   :data-x: 0
   :data-rel-x: 1050

   .. container:: copyright

      \H. Turgut Uyar

      Aralık 2022

   .. container:: svg-invert mt-8

      .. image:: kik-logo.*
         :target: https://kendinicinkodla.org/
         :alt: Kendin için Kodla logosu.
         :width: 128


.. slide:: Lisans
   :class: contents

   .. container:: columns

      .. container:: column mr-4

         .. image:: cc-by-nc-sa.*
            :alt: Creative Commons BY-NC-SA lisansı.
            :width: 192

      .. container:: column text-xl

         | Creative Commons
         | Atıf - GayriTicari - AynıLisanslaPaylaş 4.0 Uluslararası

   .. container:: text-xl mt-12

      - yazarının adı belirtilmelidir
      - ticari amaçla kullanılamaz
      - türetilen eserler aynı lisansla paylaşılmalıdır

   .. container:: mt-8

      `ayrıntılı bilgi <https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode.tr>`_


.. slide:: İçindekiler
   :id: genel-yapi
   :class: contents

   - *genel yapı*
   - `sayfa şablonu <#sayfa-sablonu>`_
   - `içerik elemanları <#icerik-elemanlari>`_
   - `gövde şablonu <#govde-sablonu>`_


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

      .. container:: column

         .. code-block:: html

            Karga

            İri yapılı, düz gagalı,
            pençeli, tüyleri çoğunlukla
            siyah, yüksek ve rahatsız
            edici sesli kuş. Daha büyük
            ve genellikle leş yiyici
            olanlarına "karakarga" veya
            "kuzgun" denir.

      .. container:: column

         .. image:: images/karga_bosluklar.*
            :alt: Boşlukların etkisi olmadığından yazı tek blok halinde.


.. slide:: Düz metin yetersiz

   - başlığı nasıl belirteceğim?
   - nasıl tablo yapacağım?
   - bir yeri nasıl vurgulayacağım?

   .. container:: substep

      - işaretler koyalım


.. slide:: İşaretleme

   - | işaretlemek istediğimiz yerin başına ve sonuna
     | *takılar* yazıyoruz:

   .. code-block:: xml

      <takı>işaretlenen bölge</takı>

   .. rst-class:: mt-8

   - her takı çifti bir *eleman* işaretliyor


.. slide:: Temel elemanlar
   :data-views: (-150, 150, 0, 0.5)

   - başlık: ``h1``
   - paragraf: ``p``

   .. container:: columns

      .. container:: column

         .. code-block:: html

            <h1>Karga</h1>

            <p>İri yapılı, düz gagalı,
              pençeli, tüyleri çoğunlukla
              siyah, yüksek ve rahatsız
              edici sesli kuş. Daha büyük
              ve genellikle leş yiyici
              olanlarına "karakarga" veya
              "kuzgun" denir.</p>

      .. container:: column

         .. image:: images/karga_etiketler.*
            :alt: Paragraf ve başlık elemanlarının kullanımı.

   .. speaker-notes::

      - Boşlukların düzeldiğine dikkat çek.


.. slide:: İçiçe elemanlar
   :data-views: (-100, 0, 0, 0.6) (350, 50, 0, 0.6)

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
   :data-views: (-150, 220, 0, 0.5) (370, -60, 0, 0.35)

   - vurgu: ``em``
   - normalde italik gösterilir

   .. container:: columns

      .. container:: column mr-8

         .. code-block:: html

            <h1>Karga</h1>

            <p>İri yapılı, düz gagalı,
              pençeli, tüyleri çoğunlukla
              siyah, yüksek ve rahatsız
              edici sesli kuş. Daha büyük
              ve genellikle leş yiyici
              olanlarına <em>karakarga</em>
              veya <em>kuzgun</em> denir.</p>

      .. container:: column

         .. image:: images/karga_vurgu.*
            :alt: Vurgu elemanının italik gösterilimi.


.. slide:: Boş elemanlar

   - bazı elemanların kapanış takısı yok
   - örnek: yatay çizgi

   .. code-block:: xml

      <hr>


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
   :id: sayfa-sablonu
   :class: contents

   - `genel yapı <#genel-yapi>`_
   - *sayfa şablonu*
   - `içerik elemanları <#icerik-elemanlari>`_
   - `gövde şablonu <#govde-sablonu>`_


.. slide:: Sayfa elemanları

   - sayfanın ana elemanı: ``html``

   ..

   - içinde iki eleman bulunur:

     - ``head``: sayfayla ilgili bilgiler (baş)
     - ``body``: sayfanın içeriği (gövde)


.. slide:: Şablon

   .. code-block:: html

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

   .. speaker-notes::

      - Görüntülemeye bir etkisi yok.


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

         .. container:: column mr-8 self-center

            .. code-block:: html

               <head>
                 <meta charset="utf-8">
               </head>

         .. container:: column self-center

            .. image:: images/karga_charset.*
               :alt: Harf tablosu belirtilince Türkçe harfler doğru çıkıyor.

   .. speaker-notes::

      - Türkçe harflerin düzeldiğine dikkat çek.
      - Editörün kullandığını seçmek gerektiğini vurgula.


.. slide:: Sayfa başlığı

   - sayfa başlığı: ``title``

   .. code-block:: html

      <head>
        <meta charset="utf-8">
        <title>Doğa Kâşifleri - Karga</title>
      </head>

   .. speaker-notes::

      - Başlığın nerede göründüğünü sor.


.. slide:: İçindekiler
   :id: icerik-elemanlari
   :class: contents

   - `genel yapı <#genel-yapi>`_
   - `sayfa şablonu <#sayfa-sablonu>`_
   - *içerik elemanları*
   - `gövde şablonu <#govde-sablonu>`_


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
   - kapatma takısı yok

   .. speaker-notes::

      - Genişlik ve yükseklik için dosyanın orijinal boyutları verilmeli.
      - ``alt`` niteliğinin öneminden söz et: görme özürlü kullanıcılar.


.. slide:: Resimler

   .. code-block:: html

      <img src="karga.jpg">

   .. container:: text-center mt-4

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
        <img src="karga_1.jpg">
        <figcaption>Tür 1</figcaption>
      </figure>

   .. container:: task substep mt-4

      - bütün küçük resimleri altyazılarıyla ekleyelim

   .. speaker-notes::

      - ``figure`` olmasa ``img`` elemanları yanyana diziliyor
      - ``figure`` ayrıca resmin etrafına boşluk ekliyor


.. slide:: Listeler
   :data-views: (-150, 100, 0, 0.5) (350, 0, 0, 0.5)

   .. container:: columns

      .. container:: column mr-8

         - sırasız liste: ``ul``
         - sıralı liste: ``ol``
         - liste maddesi: ``li``

         .. code-block:: html

            <h2>Türler</h2>

            <ul>
              <li>Avustralya kargası</li>
              <li>Orman kargası</li>
              <li>Küçük karga</li>
            </ul>

      .. container:: column self-end

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
   :data-views: (-110, 0, 0, 0.5)

   .. container:: columns

      .. container:: column mr-8

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

      .. container:: column self-center

         .. image:: images/karga_tablo.*
            :alt: Sırasız listeler maddeler halinde gösterilir.

   .. speaker-notes::

      - ``td`` ile ``th`` elemanlarının görüntülenme farklarını tartış.


.. slide:: İçindekiler
   :id: govde-sablonu
   :class: contents

   - `genel yapı <#genel-yapi>`_
   - `sayfa şablonu <#sayfa-sablonu>`_
   - `içerik elemanları <#icerik-elemanlari>`_
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

   - altlığa ana içerikle aynı türden elemanlar yazılır

   .. code-block:: html

      <footer>
        <p>(C) 2019, Kendin için Kodla</p>
      </footer>

   .. container:: text-center mt-8

      .. image:: images/karga_altlik.*
         :alt: Altlık ana içerikle aynı şekilde görüntülenir.

   .. speaker-notes::

      - Görüntülemeye bir etkisi yok.
      - ``(C)`` yerine ``&copy;`` gösterilebilir.
      - Unicode sembol seçtirilebilir: shapecatcher.com


.. slide:: Üstlük

   .. container:: columns mt-12

      .. container:: column mr-8

         - üstlük de aynı şekilde

         .. code-block:: html

            <header>
              <img src="logo_siyah.png"/>
            </header>

         .. container:: substep task

            - logoyu ana sayfaya bağlantı haline getirelim

      .. container:: column w-1/2

         .. image:: images/karga_ustluk.*
            :alt: Üstlük de ana içerikle aynı şekilde görüntülenir.

   .. speaker-notes::

      - Görüntülemeye bir etkisi yok.
      - Ana sayfanın bağlantı adresi: ``index.html``


.. slide:: Navigasyon
   :data-views: (250, 0, 0, 0.5)

   - navigasyon menüsü: ``nav``

   .. container:: columns mt-12

      .. container:: column mr-8

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

      - Görüntülemeye bir etkisi yok.


.. slide:: Kapanış
   :noheading:
   :class: contents

   HTML bölümünün sonu

   ➤ `CSS <css.html>`_
