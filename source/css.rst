.. slide:: Önyüz Geliştirme
   :subtitle: CSS
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
        <meta charset="utf-8">
        <title>Doğa Kâşifleri - Karga</title>
        <link rel="stylesheet" href="kik.css">
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

        font-family: 'Aile';

   - birden fazla yazı tipi ailesi verilebilir
   - sıradakini bulamıyorsan sonrakine geç


.. slide:: Google Fonts

   - serbestçe kullanılabilecek yazı tipleri

   ..

   - önce yazı tipi dosyaları alınmalı

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
        font-family: 'Cabin';
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
           font-family: 'Nunito';
         }


.. slide:: Yazı boyu

   .. container:: ref

      ::

        font-size: BOYUT;

   - boyut çeşitli birimlerde verilebilir

   ..

   - ``px``
   - ``em`` --- şu anki boya oranla

   .. speaker-notes::

      - ``rem`` tarayıcının seçtiği temel boy, masaüstünde genelde 16px.
      - Cabin yazı tipinin harf boyunun biraz küçük olduğuna dikkat çek.
      - 1.125rem = 18px


.. slide:: Yazı boyu
   :data-views: (0, 0, 0, 0.5)

   .. container:: columns

      .. container:: column mr-8

         .. code-block:: css

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

   - renk isimleri: ``white``, ``black``, ``red``, ...

   https://www.w3schools.com/cssref/css_colors.php

   .. speaker-notes::

      - Renklerin isimle verilmesi tercih edilmiyor.


.. slide:: Yazı rengi
   :data-views: (-250, 100, 0, 0.3) (450, 0, 0, 0.3)

   .. code-block:: css

      em {
        font-style: normal;
        color: crimson;
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
        font-family: 'Cabin';
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

        margin-KENAR: UZAKLIK;

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

   - tek değer: bütün kenarlardan aynı uzaklık

   .. code-block:: css

      figure {
        margin: 0;
      }

   .. container:: substep mt-4

      - 4 değer: ``üst sağ alt sol``

      ..

      - 2 değer: ``dikey yatay``

   .. speaker-notes::

      - Değerlerin verilişi saat yönünde.


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

      - navigasyon sağa dayansın
      - üstlükle resim arasına boşluk girsin
      - üstlük ile altlıkta aynı kenar payları olsun
      - tablo hücrelerinde kenar payı olsun

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

            <img src="karga.jpg" id="poster">

         .. code-block:: css

            #poster {
              width: 100%;
              height: auto;
            }

      .. container:: column

         .. image:: images/stil-id.*
            :alt: Kuraldan sonra resmin genişliği sayfayla aynı.


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

            .cift {
              background-color: lightgray;
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

      - gövde kenarlara dayansın
      - başlığın arka plan rengi, hizalaması, boşluklar

   .. container:: text-center

      .. image:: images/stil-icice-div.*
         :alt: Başlık kenarlara ve fotoya dayalı.


.. slide:: Tasarım düzenlemeleri

   .. container:: task

      - ana içeriği daraltıp topluca ortalayalım
      - giriş, beslenme, türler, künye, galeri


.. slide:: Eleman gruplama

   - gruplama elemanı: ``div``
   - çoğu zaman ``class`` niteliğiyle kullanılır

   .. code-block:: html

      <div class="icerik">
        <p>İri yapılı, düz gagalı...</p>
        ...
        <section>
          <h2>Galeri</h2>
          ...
        </section>
      </div>


.. slide:: Maksimum genişlik

   .. container:: ref

      ::

        max-width: BOYUT;

   - yatay ortalama için ``margin``: ``auto``

   .. code-block:: css

      .icerik {
        max-width: 50em;
        margin: 0 auto;
      }

   .. speaker-notes::

      - İstenirse bu kurallar ``header`` ve ``footer p``
        elemanlarına da uygulanabilir.


.. slide:: Sütunlar

   .. container:: task

      - galeri fotolarını sütunlara dizelim
      - yerleştirme için bir üst elemana ihtiyacımız var

   .. code-block:: html

      <div class="resimler">
        <figure>...</figure>
        <figure>...</figure>
        <figure>...</figure>
        <figure>...</figure>
      </div>


.. slide:: Eleman dizme
   :data-views: (200, 0, 0, 0.5)

   .. container:: ref

      ::

        display: flex;

   .. container:: columns mt-4

      .. container:: column

         .. code-block:: css

            .resimler {
              display: flex;
            }

            .resimler figure {
              width: 25%;
            }

      .. container:: column text-center

         .. image:: images/stil-flex.*
            :alt: Galeri fotoları dört sütun halinde dizilmiş.


.. slide:: Yerleştirme

   - içerik kısmında istenen yerleştirme::

       | bilgiler | künye |

       | galeri           |

   - elemanları sınıflarda toplayalım


.. slide:: Yerleştirme sınıfları

   .. container:: columns

      .. container:: column

         .. code-block:: html

            <div class="bilgi">
              <p>İri yapılı, ...</p>
              ...
              <ul>
                ...
              </ul>
            </div>

      .. container:: column

         .. code-block:: html

            <table class="kunye">
              ...
            </table>

   .. code-block:: html

      <section class="galeri">
        ...
      </section>


.. slide:: İki boyutlu yerleştirme

   .. container:: ref

      ::

        display: grid;
        grid-template-areas: YERLEŞİM;

   - yerleşim sayfadaki bölümlere isim verir
   - o bölüme gelecek eleman:

   .. container:: ref

      ::

        grid-area: İSİM;


.. slide:: Yerleştirilmiş sayfa

   .. container:: columns

      .. container:: column

         .. code-block:: css

            .icerik {
              display: grid;
              grid-template-areas:
                "bilgi  kunye"
                "galeri galeri";
              max-width: 50em;
              margin: 0 auto;
            }

      .. container:: column

         .. code-block:: css

            .bilgi {
              grid-area: bilgi;
            }

            .kunye {
              grid-area: kunye;
            }

            .galeri {
              grid-area: galeri;
            }


.. slide:: Tasarım düzenlemeleri

   .. container:: task

      - | bilgi ile künye arasında biraz boşluk olsun:
        | ``grid-column-gap``

      - | tablo satır yüksekliği artmasın:
        | ``fit-content``


.. slide:: Tasarım düzenlemeleri

   .. container:: task

      - | galeri fotoları yuvarlak olsun
        | ``border-radius``

      - foto altyazıları ortalansın

      .. container:: column text-center

         .. image:: images/stil-yuvarlak.*
            :alt: Galeri fotoları yuvarlak ve altyazıları ortalı.


.. slide:: Kapanış
   :noheading:
   :class: contents

   CSS bölümünün sonu
