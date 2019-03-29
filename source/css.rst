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
