.. slide:: Önyüz Geliştirme
   :subtitle: CSS
   :class: title
   :data-x: 0
   :data-rel-x: 1050

   .. container:: copyright

      \H. Turgut Uyar

      Mart 2019


.. slide:: İçindekiler
   :id: genel-yapi
   :class: contents

   - *genel yapı*
   - `yazı stilleri <#yazi-stilleri>`_
   - `renkler <#renkler>`_
   - `boşluklar <#bosluklar>`_
   - `yerleştirme <#yerlestirme>`_


.. slide:: CSS

   - *Cascading Style Sheets*

   ..

   - düz metin

   .. container:: substep task

      - boş stil dosyasını oluşturalım


.. slide:: Stil bağlantısı

   - HTML dosyasının baş kısmında: ``link``
   - stil dosyası olduğunu belirtmek için: ``rel``
   - stil dosyası adresi: ``href``

   .. code-block:: html
      :emphasize-lines: 4

      <head>
        <meta charset="utf-8"/>
        <title>Doğa Kaşifleri - Karga</title>
        <link rel="stylesheet" href="kik.css"/>
      </head>


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

   - sola: ``left``
   - sağa: ``right``
   - ortaya: ``center``
   - çift yandan: ``justify``


.. slide:: Metin hizalama
   :data-views: (0, 0, 0, 0.5)

   .. code-block:: css

      th {
        text-align: left;
      }

   .. container:: columns justify-center mt-8

      .. container:: column flex-unset mr-12

         .. image:: images/stil-hizalama-once.*
            :alt: Normalde başlık hücreleri ortaya hizalı.

      .. container:: column flex-unset

         .. image:: images/stil-hizalama-sonra.*
            :alt: Kuraldan sonra başlık hücreleri sola hizalı.


.. slide:: İçindekiler
   :id: yazi-stilleri
   :class: contents

   - `genel yapı <#genel-yapi>`_
   - *yazı stilleri*
   - `renkler <#renkler>`_
   - `boşluklar <#bosluklar>`_
   - `yerleştirme <#yerlestirme>`_


.. slide:: Yazı tipi

   .. container:: ref

      ::

        font-family: 'Seçenek 1', 'Seçenek 2', 'Seçenek 3';

   - her seçenek bir yazı tipi "ailesi"
   - sıradaki seçeneği bulamıyorsan sonrakine geç

   - | son seçenek şunlardan biri olmalı:
     | ``serif``, ``sans-serif``, ``monospace``


.. slide:: Google Fonts

   - serbestçe kullanılabilecek yazı tipleri

   ..

   - önce stil dosyasına alınmalı

   .. rst-class:: small

   .. code-block:: css

      @import url('https://fonts.googleapis.com/css?family=Cabin:400,700|Nunito:400,700');

   .. container:: substep task mt-12

      - biri gövde, biri başlıklar için iki yazı tipi seçelim

   .. speaker-notes::

      - Seçerken ağırlıklar 400/700 olsun.
      - Latin Extended seçmek gerekebilir.


.. slide:: Varsayılan yazı tipi

   - | ``body`` elemanına uygulanırsa
     | bütün sayfa için geçerli olur


.. slide:: Varsayılan yazı tipi
   :data-views: (0, 0, 0, 0.5)

   .. code-block:: css

      body {
        font-family: 'Cabin', sans-serif;
      }

   .. container:: columns mt-8

      .. container:: column

         .. image:: images/stil-yazi-tipi-once.*
            :alt: Normalde yazılar tarayıcının standart yazı tipiyle gösteriliyor.

      .. container:: column

         .. image:: images/stil-yazi-tipi-sonra.*
            :alt: Kuraldan sonra yazılar bizim seçtiğimiz Cabin yazı tipiyle gösteriliyor.


.. slide:: Çoklu elemanlar

   - birden fazla elemana aynı stil uygulanabilir
   - elemanları virgülle ayırarak:

   .. code-block:: css

      eleman_1, eleman_2 {
         ayar_ismi: ayar_değeri;
      }

   .. container:: substep mt-8

      .. code-block:: css

         h1, h2 {
           font-family: 'Nunito', sans-serif;
         }


.. slide:: Yazı boyu

   .. container:: ref

      ::

        font-size: BOYUT;

   - boyut çeşitli birimlerde verilebilir

   ..

   - ``px``
   - ``em`` --- geçerli boya göre ölçek
   - ``rem`` --- taban boya göre ölçek

   .. speaker-notes::

      - ``rem`` tarayıcının seçtiği temel boy, masaüstünde genelde 16px.
      - Cabin yazı tipinin harf boyunun biraz küçük olduğuna dikkat çek.
      - 1.125rem = 18px


.. slide:: Yazı boyu
   :data-views: (250, 0, 0, 0.5)

   .. container:: columns

      .. container:: column mr-8

         .. code-block:: css

            body {
              font-family: 'Cabin', sans-serif;
              font-size: 1.125rem;
            }

            h1 {
              font-size: 3em;
            }

      .. container:: column

         .. image:: images/stil-yazi-boyu-once.*
            :alt: Normalde yazılar tarayıcının standart yazı boylarıyla gösteriliyor.

         .. rst-class:: mt-12

         .. image:: images/stil-yazi-boyu-sonra.*
            :alt: Kuraldan sonra gövde yazı boyu ve başlığın bu boya oranı değişiyor.

   .. speaker-notes::

      - Tarayıcının normal ayarında ``h1`` boyu ``1.5em``.
      - Eskisinde ``body`` 16px, ``h1`` 24px.
      - Yenisinde ``body`` 18px, ``h1`` 54px.


.. slide:: Yazı tipi stili

   .. container:: ref

      ::

        font-style: STİL;

   - normal: ``normal``
   - italik: ``italic``


.. slide:: Yazı tipi stili
   :data-views: (-250, 0, 0, 0.3) (450, 0, 0, 0.3)

   .. code-block:: css

      em {
        font-style: normal;
      }

   .. container:: columns mt-8

      .. container:: column

         .. image:: images/stil-yazi-stili-once.*
            :alt: Normalde vurgular italik gösteriliyor.

      .. container:: column

         .. image:: images/stil-yazi-stili-sonra.*
            :alt: Kuraldan sonra vurgular normal gösteriliyor.

   .. speaker-notes::

      - Vurgunun düz metinden farkı kalmıyor, değiştirmek gerek.


.. slide:: Yazı tipi ağırlığı

   .. container:: ref

      ::

        font-weight: AĞIRLIK;

   - normal: ``normal``
   - kalın: ``bold``
   - veya: ``400``, ``700``


.. slide:: Yazı tipi ağırlığı
   :data-views: (-250, 100, 0, 0.3) (450, 0, 0, 0.3)

   .. code-block:: css

      em {
        font-style: normal;
        font-weight: bold;
      }

   .. container:: columns mt-8

      .. container:: column

         .. image:: images/stil-yazi-stili-once.*
            :alt: Normalde vurgular italik gösteriliyor.

      .. container:: column

         .. image:: images/stil-yazi-agirligi-sonra.*
            :alt: Kuraldan sonra vurgular kalın gösteriliyor.


.. slide:: Alt-üst çizgileri

   .. container:: ref

      ::

        text-decoration: ÇİZGİ;

   - yok: ``none``
   - altına: ``underline``
   - üstüne: ``overline``
   - ortasına: ``line-through``


.. slide:: Alt-üst çizgileri
   :data-views: (-250, 100, 0, 0.3) (450, 0, 0, 0.3)

   .. code-block:: css

      em {
        font-style: normal;
        text-decoration: underline;
      }

   .. container:: columns mt-8

      .. container:: column

         .. image:: images/stil-yazi-stili-once.*
            :alt: Normalde vurgular italik gösteriliyor.

      .. container:: column

         .. image:: images/stil-yazi-altcizgisi-sonra.*
            :alt: Kuraldan sonra vurgular altı çizili gösteriliyor.

   .. speaker-notes::

      - Altçizginin kötü görünümünden söz et (``g`` harflerini göster).


.. slide:: İçindekiler
   :id: renkler
   :class: contents

   - `genel yapı <#genel-yapi>`_
   - `yazı stilleri <#yazi-stilleri>`_
   - *renkler*
   - `boşluklar <#bosluklar>`_
   - `yerleştirme <#yerlestirme>`_


.. slide:: Yazı rengi

   .. container:: ref

      ::

        color: RENK;

   - rengin ismi: ``white``, ``black``, ``red``, ...
   - RGB değeri

   .. speaker-notes::

      - Renklerin isimle verilmesi tercih edilmiyor.


.. slide:: Yazı rengi
   :data-views: (-250, 100, 0, 0.3) (450, 0, 0, 0.3)

   .. code-block:: css

      em {
        font-style: normal;
        color: #C00000;
      }

   .. container:: columns mt-8

      .. container:: column

         .. image:: images/stil-yazi-stili-once.*
            :alt: Normalde vurgular italik ce siyah gösteriliyor.

      .. container:: column

         .. image:: images/stil-yazi-rengi-sonra.*
            :alt: Kuraldan sonra vurgular düz ve kırmızı gösteriliyor.


.. slide:: Arka plan rengi
   :data-views: (0, 200, 0, 0.6)

   .. container:: ref

      ::

        background-color: RENK;

   .. container:: task mt-8

      - altlıkta şunları ayarlayalım:

        - arka plan rengi, yazı rengi
        - yazı boyu
        - metin hizalaması

   .. container:: substep mt-8 text-center

      .. image:: images/stil-arkaplan-rengi-sonra.*
         :alt: Altlıkta siyah arka plan, beyaz yazı, küçük boy, sağa dayalı.


.. slide:: Satır aralığı

   .. container:: ref

      ::

        line-height: YÜKSEKLİK;

   - yazı boyuna göre katsayı


.. slide:: Satır aralığı
   :data-views: (0, 0, 0, 0.5)

   .. code-block:: css

      body {
        font-family: 'Cabin', sans-serif;
        font-size: 1.125rem;
        line-height: 1.5;
      }

   .. container:: columns mt-8

      .. container:: column

         .. image:: images/stil-satir-araligi-once.*
            :alt: Normalde satır aralığı az.

      .. container:: column

         .. image:: images/stil-satir-araligi-sonra.*
            :alt: Kuraldan sonra satır aralığı artıyor.


.. slide:: İçindekiler
   :id: bosluklar
   :class: contents

   - `genel yapı <#genel-yapi>`_
   - `yazı stilleri <#yazi-stilleri>`_
   - `renkler <#renkler>`_
   - *boşluklar*
   - `yerleştirme <#yerlestirme>`_


.. slide:: Boşluklar
   :data-views: (0, -50, 0, 0.5)

   .. container:: w-1/2 m-auto

      .. image:: images/kutu-modeli.*
         :alt: Elemandan dışarı yönde boşluklar marjin, içeri yöndekiler dolgu.

   - elemandan dışarıya doğru: ``margin``
   - elemandan içeriye doğru: ``padding``


.. slide:: Dış boşluklar

   .. container:: ref

      ::

        margin-YÖN: UZAKLIK;

   - sol: ``margin-left``
   - sağ: ``margin-right``
   - üst: ``margin-top``
   - alt: ``margin-bottom``


.. slide:: Dış boşluklar
   :data-views: (-100, 0, 0, 0.6)

   .. code-block:: css

      footer {
        margin-top: 4em;
      }

   .. container:: columns mt-8 items-end

      .. container:: column

         .. image:: images/stil-bosluk-ust-once.*
            :alt: Normalde altlığın ana gövdeye uzaklığı az.

      .. container:: column

         .. image:: images/stil-bosluk-ust-sonra.*
            :alt: Kuraldan sonra altlığın ana gövdeye uzaklığı artıyor.


.. slide:: Dış boşluklar

   - yön belirtilmezse: bütün yönlerden aynı uzaklık

   .. code-block:: css

      figure {
        margin: 0;
      }

   .. container:: substep mt-4

      - 4 yön birden: ``üst sağ alt sol`` sırasıyla

      ..

      - ``auto`` niteliği kullanılırsa iki yandan aynı boşluk

   .. speaker-notes::

      - Yönlerin verilişi saat yönünde.


.. slide:: İç boşluklar

   .. container:: ref

      ::

        padding: UZAKLIK;

   - dış boşluklarla aynı yazım


.. slide:: İç boşluklar
   :data-views: (100, 0, 0, 0.6)

   .. code-block:: css

      footer {
        margin-top: 4em;
        padding: 1em;
      }

   .. container:: columns mt-8

      .. container:: column

         .. image:: images/stil-bosluk-ic-once.*
            :alt: Normalde altlıktaki metnin etrafında boşluk yok.

      .. container:: column

         .. image:: images/stil-bosluk-ic-sonra.*
            :alt: Kuraldan sonra altlıktaki metnin dört yanında boşluk var.


.. slide:: İçiçe eleman seçimi

   .. container:: task

      - üstlükteki bağlantıların altı çizili olmasın

   .. container:: substep task

      - ama metin içindekiler eskisi gibi kalsın

   .. container:: substep

      - alt eleman seçmek için:

      .. code-block:: css

         üst_eleman alt_eleman {
            ayar_ismi: ayar_değeri;
         }

   .. speaker-notes::

      - Önce ``a { text-decoration: none; }`` göster.


.. slide:: İçiçe eleman seçimi
   :data-views: (150, -100, 0, 0.5) (0, 300, 0, 0.5)

   .. container:: columns

      .. container:: column mr-8

         .. code-block:: css

            header a {
              text-decoration: none;
            }

            header nav a {
              margin-left: 1em;
            }

      .. container:: column w-1/3

         .. image:: images/stil-icice.*
            :alt: Kuraldan sonra sadece üstlükteki bağlantıların altı çizili değil.


.. slide:: Düzenlemeler

   .. container:: task

      - üstlüğü düzenleyelim:

        - renkler
        - logo
        - yazı tipleri
        - boşluklar

   .. speaker-notes::

      - Linklerde ``text-transform: uppercase`` göster.
      - Sayfa dilini Türkçe vermenin etkisini tartış.

      ..

      - Bu yansıdan sonra ara verilebilir. HTML dosyasında değişiklikler
        gerekecek.


.. slide:: İçindekiler
   :id: yerlestirme
   :class: contents

   - `genel yapı <#genel-yapi>`_
   - `yazı stilleri <#yazi-stilleri>`_
   - `renkler <#renkler>`_
   - `boşluklar <#bosluklar>`_
   - *yerleştirme*


.. slide:: Eleman boyutları

   .. container:: ref

      ::

        width: BOYUT;
        height: BOYUT;

   - uzunluk ölçüsü
   - bulunulan alana göre ``%``
   - diğer boyuta göre ölçekle: ``auto``


.. slide:: Eleman boyutları

   .. container:: task

      - büyük resim bulunduğu alanın tüm enini kaplasın

   .. code-block:: css

      img {
        width: 100%;
        height: auto;
      }

   .. container:: substep

      - bütün resimler %100 oluyor
      - sadece o resmi nasıl seçeceğim?


.. slide:: Tek eleman ayarı

   .. container:: columns

      .. container:: column flex flex-col items-center justify-center

         .. rst-class:: border-b-2 border-grey px-4 mb-8

         HTML

         - kimlik niteliği: ``id``
         - değeri sayfada tek olmalı

      .. container:: column flex flex-col items-center justify-center

         .. rst-class:: text-center border-b-2 px-2

         CSS

         - ``eleman#kimlik``
         - veya: ``#kimlik``


.. slide:: Tek eleman ayarı

   .. container:: columns

      .. container:: column flex flex-col items-start mr-8

         .. code-block:: html

            <img src="karga.jpg"
                 id="poster"
                 width="1280"
                 height="427"
                 alt="Bir parkta ..."/>

         .. code-block:: css

            img#poster {
              width: 100%;
              height: auto;
            }

      .. container:: column

         .. image:: images/stil-id.*
            :alt: Kuraldan sonra resmin genişliği sayfayla aynı.


.. slide:: Maksimum genişlik

   .. container:: ref

      ::

        max-width: BOYUT;

   .. container:: task mt-8

      - logonun genişliği en fazla 360px olsun


.. slide:: Çoklu eleman seçme

   .. container:: task

      - tablonun çift satırlarının arka plan rengini değiştirelim

   .. container:: substep

      - birden fazla eleman nasıl seçeceğim?


.. slide:: Eleman sınıfı ayarı

   .. container:: columns

      .. container:: column flex flex-col items-center justify-center

         .. rst-class:: border-b-2 border-grey px-4 mb-8

         HTML

         - sınıf niteliği: ``class``
         - bir çok elemanda olabilir

      .. container:: column flex flex-col items-center justify-center

         .. rst-class:: text-center border-b-2 px-2

         CSS

         - ``eleman.sınıf``
         - veya: ``.sınıf``


.. slide:: Eleman sınıfı ayarı
   :data-views: (200, 50, 0, 0.5)

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
              background-color: #E0E0E0;
            }

         .. container:: flex justify-around mt-8

            .. image:: images/stil-sinif-once.*
               :alt: Normalde hücre arka planları beyaz.

            .. image:: images/stil-sinif-sonra.*
               :alt: Kuraldan sonra çift numaralı hücrelerin arka planları gri.

   .. speaker-notes::

      - Tablo görünümü düzeltilmek istenirse::

           table {
             border-collapse: collapse;
           }

           td, th {
             padding: 0.5em;
           }


.. slide:: Tasarım düzenlemeleri

   .. container:: task

      - içerik kısmına yanlardan boşluk bırakalım

      ..

      - büyük resim kenarlara dayalı
      - başlığın arka plan rengi var

   - kuralı hangi elemana uygulayacağız?


.. slide:: Eleman gruplama

   - gruplama elemanı: ``div``
   - çoğu zaman ``class`` niteliğiyle kullanılır


.. slide:: Eleman gruplama
   :data-views: (200, 200, 0, 0.5)

   .. container:: columns

      .. container:: column flex flex-col items-start mr-12

         .. code-block:: html

            <div class="icerik">
              <p>İri yapılı, ...</p>
              ...
              <section>
                ...
              </section>
            </div>

         .. code-block:: css

            .icerik {
              max-width: 50em;
              margin: 0 auto;
            }

      .. container:: column

         .. image:: images/stil-div.*
            :alt: Kuraldan sonra içerik kısmı daha dar ve ortaya hizalı.


.. slide:: Kod açıklamaları

   - hangi elemanı kapattığını takip etmek zorlaşıyor

   ..

   - açıklama yazmak okurken yardımcı olur:

   .. container:: columns

      .. container:: column

         - ``<!--`` ile başla
         - ``-->`` ile bitir

      .. container:: column

         .. code-block:: html

            <div class="icerik">
              <p>İri yapılı, ...</p>
              ...
              <section>
                ...
              </section>
            </div> <!-- icerik -->


.. slide:: Tasarım düzenlemeleri

   .. container:: task

      - başlığın arka plan rengini ayarlayalım
      - kenarlara ve büyük fotoya dayayalım

   .. container:: text-center

      .. image:: images/stil-icice-div.*
         :alt: Başlık kenarlara ve fotoya dayalı.


.. slide:: Tasarım düzenlemeleri

   .. container:: columns

      .. container:: column mr-12

         .. code-block:: html

            <div class="afis">
              <div class="icerik">
                <h1>Karga</h1>
              </div> <!-- icerik -->
            </div> <!-- afis -->

      .. container:: column flex flex-col items-start

         .. code-block:: css

            .afis {
              background-color: #E0E0E0;
            }

            .afis h1 {
              margin-top: 0;
            }

         .. container:: substep mt-8

            .. code-block:: css

               img#poster {
                 display: block;
               }


.. slide:: Paragraf içi eleman gruplama
   :data-views: (-20, 0, 0, 0.5)

   .. container:: task

      - ilk harfin boyunu büyütüp arka plan rengini değiştirelim

   .. container:: column text-center

      .. image:: images/stil-span.*
         :alt: İlk harf daha büyük ve arka planı farklı.

   .. container:: substep mt-8

      - ``div`` paragraf düzeyinde gruplama için
      - paragraf içi: ``span``


.. slide:: Paragraf içi eleman gruplama

   .. container:: flex flex-col items-start

      .. code-block:: html

         <p><span class="ilk-harf">İ</span>ri yapılı,
           düz gagalı, ...</p>

      .. code-block:: css

         .ilk-harf {
           font-family: Georgia, serif;
           font-size: 3em;
           float: left;
           width: 1em;
           margin-right: 0.15em;
           background-color: #E0E0E0;
           text-align: center;
         }


.. slide:: Sütunlar

   .. container:: task

      - galeri fotolarını sütunlara dizelim
      - her sütun için bir ``div`` tanımlayalım
      - sütunları gruplamak için de bir üst ``div``


.. slide:: Sütunlar

   .. container:: columns

      .. container:: column mr-12

         .. code-block:: html

            <div class="sutun">
              <figure>
                ...
              </figure>
            </div> <!-- sutun: 1 -->

      .. container:: column flex flex-col items-start

         .. code-block:: html

            <div class="sutunlar">

               <div class="sutun">
                   ...
               </div> <!-- sutun: 1 -->

               ...

               <div class="sutun">
                   ...
               </div> <!-- sutun: 4 -->

            </div> <!-- sutunlar -->


.. slide:: Eleman dizme

   .. container:: ref

      ::

        display: flex;

   .. container:: columns mt-8

      .. container:: column

         .. code-block:: css

            .sutunlar {
              display: flex;
            }

            .sutun {
              margin-right: 1em;
            }

      .. container:: column text-center

         .. image:: images/stil-flex.*
            :alt: Galeri fotoları dört sütun halinde dizilmiş.

   .. container:: substep task mt-4

      - resimleri yuvarlatalım, yazıları ortalayalım


.. slide:: Yuvarlak fotolar

   .. container:: flex flex-col items-start

      .. code-block:: html
         :emphasize-lines: 1

         <section class="galeri">
           <h2>Galeri</h2>
             ...
         </section> <!-- galeri -->

   .. container:: columns mt-8

      .. container:: column

         .. code-block:: css

            .galeri img {
              border-radius: 50%;
            }

            .galeri figcaption {
              text-align: center;
            }

      .. container:: column

         .. image:: images/stil-yuvarlak.*
            :alt: Galeri fotoları yuvarlak, foto yazıları ortadan hizalı.

   .. speaker-notes::

      - Değişik ``border-radius`` ayarları denesinler.


.. slide:: Yerleştirme düzenlemesi
   :data-views: (-20, 0, 0, 0.6)

   .. container:: task

      - yazıları birinci, tabloyu ikinci sütuna alalım

   .. container:: w-1/2 m-auto

      .. image:: images/stil-ana-sutunlar.*
         :alt: Tablo ikinci sütunda.


.. slide:: Kapanış
   :noheading:
   :class: contents

   CSS bölümünün sonu
