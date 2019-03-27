.. slide:: Önyüz Geliştirme
   :subtitle: HTML
   :class: title
   :data-x: 0
   :data-rel-x: 1050

   .. container:: flex flex-col items-center

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

         .. image:: karga_bosluklar.*
            :alt: Boşlukların etkisi olmadığından yazı tek blok halinde.

   .. speaker-notes::

      - Herkes kendi hayvanının metin dosyasından paragrafını kopyalasın.
      - Boşlukların etkisini tartış.
      - Türkçe harflerin bozuk çıktığına dikkat çek.


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
   :data-views: (200, 120, 0, 0.5)

   - paragraf: ``p``
   - başlık: ``h1``

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
            :alt: Paragraf ve başlık elemanlarının kullanımı.


.. slide:: İçiçe elemanlar

   - bir elemanın içine başka bir eleman konabilir
   - sonra açılan eleman önce kapanmalı

   .. code-block:: xml

      <dış>dış bölge<iç>iç bölge</iç>dış bölge</dış>

   .. code-block:: xml

      <dış>
        dış bölge
        <iç>
          iç bölge
        </iç>
        dış bölge
      </dış>


.. slide:: Vurgu
   :data-views: (-150, 200, 0, 0.5) (350, -100, 0, 0.5)

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

         .. image:: karga_vurgu.*
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
