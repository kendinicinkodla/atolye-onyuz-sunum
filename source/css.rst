.. slide:: Önyüz Geliştirme
   :subtitle: CSS
   :class: title
   :data-x: 0
   :data-rel-x: 1050

   .. container:: copyright

      \H. Turgut Uyar

      Mart 2019


.. slide:: İçindekiler
   :class: contents

   - *genel yapı*
   - yazı stilleri
   - renkler
   - boşluklar
   - yerleştirme


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
            :alt: Kuraldan önce başlık hücreleri ortaya hizalı.

      .. container:: column flex-unset

         .. image:: images/stil-hizalama-sonra.*
            :alt: Kuraldan sonra başlık hücreleri sola hizalı.


.. slide:: İçindekiler
   :class: contents

   - genel yapı
   - *yazı stilleri*
   - renkler
   - boşluklar
   - yerleştirme


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

      .. container:: column w-1/2 text-center

         .. image:: images/stil-yazi-tipi-once.*
            :alt: Yazılar tarayıcının standart yazı tipiyle gösteriliyor.

      .. container:: column w-1/2 text-center

         .. image:: images/stil-yazi-tipi-sonra.*
            :alt: Yazılar bizim seçtiğimiz Cabin yazı tipiyle gösteriliyor.


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
   :data-views: (0, 100, 0, 0.65)

   .. container:: columns

      .. container:: column w-1/2

         .. code-block:: css

            body {
              font-family: 'Cabin', sans-serif;
              font-size: 1.125rem;
            }

      .. container:: column w-1/2

         .. code-block:: css

            h1 {
              font-size: 3em;
            }

   .. container:: columns mt-8

      .. container:: column text-center

         .. image:: images/stil-yazi-boyu-once.*
            :alt: Yazılar tarayıcının standart yazı boylarıyla gösteriliyor.

      .. container:: column text-center

         .. image:: images/stil-yazi-boyu-sonra.*
            :alt: Gövde yazı boyu ve başlığın bu boya oranı değişiyor.

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

      .. container:: column w-1/2 text-center

         .. image:: images/stil-yazi-stili-once.*
            :alt: Kuraldan önce vurgular italik gösteriliyor.

      .. container:: column w-1/2 text-center

         .. image:: images/stil-yazi-stili-sonra.*
            :alt: Kuraldan sonra vurgular normal gösteriliyor.

   .. container:: substep task mt-12

      - vurgunun düz metinden farkı kalmadı, değiştirelim


.. slide:: Yazı tipi ağırlığı

   .. container:: ref

      ::

        font-weight: AĞIRLIK;

   - normal: ``normal``
   - kalın: ``bold``
   - veya: ``400``, ``700``


.. slide:: Yazı tipi ağırlığı
   :data-views: (-250, 0, 0, 0.3) (450, 0, 0, 0.3)

   .. code-block:: css

      em {
        font-style: normal;
        font-weight: bold;
      }

   .. container:: columns mt-8

      .. container:: column w-1/2 text-center

         .. image:: images/stil-yazi-stili-sonra.*
            :alt: Kuraldan önce vurgular normal gösteriliyor.

      .. container:: column w-1/2 text-center

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
   :data-views: (-250, 0, 0, 0.3) (450, 0, 0, 0.3)

   .. code-block:: css

      em {
        font-style: normal;
        text-decoration: underline;
      }

   .. container:: columns mt-8

      .. container:: column w-1/2 text-center

         .. image:: images/stil-yazi-stili-sonra.*
            :alt: Kuraldan önce vurgular normal gösteriliyor.

      .. container:: column w-1/2 text-center

         .. image:: images/stil-yazi-altcizgisi-sonra.*
            :alt: Kuraldan sonra vurgular altı çizili gösteriliyor.

   .. speaker-notes::

      - Altçizginin kötü görünümünden söz et (``g`` harflerini göster).


.. slide:: İçindekiler
   :class: contents

   - genel yapı
   - yazı stilleri
   - *renkler*
   - boşluklar
   - yerleştirme


.. slide:: Yazı rengi

   .. container:: ref

      ::

        color: RENK;

   - rengin ismi: ``white``, ``black``, ``red``, ...
   - RGB değeri

   .. speaker-notes::

      - Renklerin isimle verilmesi tercih edilmiyor.


.. slide:: Yazı rengi
   :data-views: (-250, 0, 0, 0.3) (450, 0, 0, 0.3)

   .. code-block:: css

      em {
        font-style: normal;
        color: #C00000;
      }

   .. container:: columns mt-8

      .. container:: column w-1/2 text-center

         .. image:: images/stil-yazi-stili-sonra.*
            :alt: Kuraldan önce vurgular siyah gösteriliyor.

      .. container:: column w-1/2 text-center

         .. image:: images/stil-yazi-rengi-sonra.*
            :alt: Kuraldan sonra vurgular kırmızı gösteriliyor.


.. slide:: Arka plan rengi
   :data-views: (0, 0, 0, 0.6)

   .. container:: ref

      ::

        background-color: RENK;

   .. container:: mt-8 text-center

      .. image:: images/stil-altlik-sonra.*
         :alt: Altlıkta siyah arka plan, beyaz yazı, küçük boy, sağa dayalı.

   .. container:: substep task mt-8

      - altlıkta şunları ayarlayalım:

        - arka plan rengi, yazı rengi
        - yazı boyu
        - metin hizalaması


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

      .. container:: column w-1/2 text-center

         .. image:: images/stil-satir-araligi-once.*
            :alt: Kuraldan önce satır aralıkları az.

      .. container:: column w-1/2 text-center

         .. image:: images/stil-satir-araligi-sonra.*
            :alt: Kuraldan sonra satır aralıkları artıyor.


.. slide:: İçindekiler
   :class: contents

   - genel yapı
   - yazı stilleri
   - renkler
   - *boşluklar*
   - yerleştirme


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

        margin: UZAKLIK;

   - soldan: ``margin-left``
   - sağdan: ``margin-right``
   - üstten: ``margin-top``
   - alttan: ``margin-bottom``

   ..

   - yön belirtilmezse: bütün yönlerden aynı uzaklık
   - veya: ``üst sağ alt sol``

   .. speaker-notes::

      - Yönlerin verilişi saat yönünde.


.. slide:: Dış boşluklar
   :data-views: (0, 0, 0, 0.6)

   .. code-block:: css

      footer {
        margin-top: 4em;
      }

   .. container:: columns mt-8

      .. container:: column w-1/2 text-center

         .. image:: images/stil-altlik-sonra.*
            :alt: Kuraldan önce altlığın ana gövdeye uzaklığı az.

      .. container:: column w-1/2 text-center

         .. image:: images/stil-bosluk-ust-sonra.*
            :alt: Kuraldan sonra altlığın ana gövdeye uzaklığı artıyor.


.. slide:: İç boşluklar

   .. container:: ref

      ::

        padding: UZAKLIK;

   - dış boşluklarla aynı yazım


.. slide:: Dış boşluk
   :data-views: (0, 0, 0, 0.6)

   .. code-block:: css

      footer {
        margin-top: 4em;
        padding: 1em;
      }

   .. container:: columns mt-8

      .. container:: column w-1/2 text-center

         .. image:: images/stil-bosluk-ust-sonra.*
            :alt: Kuraldan önce altlıktaki metnin etrafında boşluk yok.

      .. container:: column w-1/2 text-center

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
   :data-views: (200, -100, 0, 0.5) (0, 300, 0, 0.5)

   .. container:: columns

      .. container:: column

         .. code-block:: css

            header a {
              text-decoration: none;
              margin-right: 1em;
            }

      .. container:: column w-1/2 text-center

         .. image:: images/stil-ustluk-baglanti-sonra.*
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


.. slide:: İçindekiler
   :class: contents

   - genel yapı
   - yazı stilleri
   - renkler
   - boşluklar
   - *yerleştirme*


.. slide:: Eleman yüzdürme

   .. container:: ref

      ::

        float: YÖN;

   - sol: ``left``
   - sağ: ``right``

   ..

   - diğer elemanlar bunun etrafından "akar"


.. slide:: Eleman yüzdürme
   :data-views: (-100, 100, 0, 0.5)

   .. code-block:: css

      header figure {
        float: left;
      }

   .. container:: text-center mt-8

      .. image:: images/stil-yuzdurme-once.*
         :alt: Kuraldan önce logonun yanındaki bağlantılar alt satıra iniyor.

   .. container:: text-center mt-12

      .. image:: images/stil-yuzdurme-sonra.*
         :alt: Kuraldan sonra logonun yanındaki bağlantılar aynı satırda kalıyor.

   .. speaker-notes::

      - Navigasyon linklerine boşluk vermek iyi olabilir.

      - Bu yansıdan sonra ara verilebilir. HTML dosyasında değişiklikler
        gerekecek.
