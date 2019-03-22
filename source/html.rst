.. slide:: Önyüz Geliştirme
   :class: title
   :data-rel-x: 1050

   .. container:: flex flex-col items-center

      .. container:: subtitle

         HTML

      .. container:: copyright

         \H. Turgut Uyar

         Mart 2019


.. slide:: HTML

   - *HyperText Markup Language*

   ..

   - düz metin

   .. speaker-notes::

      - Katılımcılar ilk dosyalarını oluştursunlar: :file:`karga.html`
      - İçine herkes kendi hayvanının ismini yazsın.


.. slide:: Boşluklar

   - fazladan boşlukların bir önemi yok

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

         .. image:: karga_bosluklar.*
            :alt: Boşlukların önemi yok
            :width: 100%

   .. speaker-notes::

      - Herkes kendi hayvanının metin dosyasından paragrafını kopyalasın.
      - Boşlukların etkisini tartış.
      - Türkçe harflerin bozuk çıktığına dikkat çek.


.. slide:: Boşluklar
   :noheading:
   :data-rel-x: 200
   :data-scale: 0.5
   :class: bg-transparent shadow-none

   ..


.. slide:: Düz metin yetersiz
   :data-rel-x: 1050

   - başlığı nasıl belirteceğim?
   - nasıl tablo yapacağım?
   - bir yeri nasıl vurgulayacağım?

   ..

   - işaretler koyalım


.. slide:: İşaretleme

   - | işaretlemek istediğimiz yerin başına ve sonuna
     | *etiketler* yazıyoruz

   ..

   - paragraf: ``p``
   - başlık: ``h1``


.. slide:: İşaretleme

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

         .. image:: karga_etiketler.*
            :alt: Boşlukların önemi yok
            :width: 100%


.. slide:: İşaretleme
   :noheading:
   :data-rel-x: 200
   :data-scale: 0.5
   :class: bg-transparent shadow-none

   ..
