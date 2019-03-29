.. slide:: Önyüz Geliştirme
   :subtitle: CSS
   :class: title
   :data-x: 0
   :data-rel-x: 1050

   .. container:: copyright

      \H. Turgut Uyar

      Mart 2019


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
   - elemanları virgülle ayırarak

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
