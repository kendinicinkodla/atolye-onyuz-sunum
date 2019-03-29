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

      .. container:: column w-1/2 text-center

         .. image:: images/stil-yazi-tipi-sonra.*
