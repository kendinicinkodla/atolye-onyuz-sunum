

.. slide:: Sütunlar

   - birden fazla sütun oluşturma

   ..

   - ayar ismi: ``display``
   - ayar değeri: ``flex``

   .. speaker-notes::

      - galeri resimleri için hangi elemanları gruplayacağım?


.. slide:: Eleman gruplama

   .. code-block:: html

      <section>
        <h2>Galeri</h2>

        <div class="galeri">
          <figure>
            <img src="..."/>
            <figcaption>...</figcaption>
          </figure>

          <figure>
            <img src="..."/>
            <figcaption>...</figcaption>
          </figure>
        </div>
      </section>


.. slide:: Sütun ayarı

   .. code-block:: css

      .gallery {
        display: flex;
      }

      .gallery figure {
        width: 25%;
      }

      .gallery img {
        width: 100%;
      }

   .. speaker-notes::

      - resimler küçük, yanlarda çok boşluk var
      - ``.galeri figure { margin-left: 0; margin-right: 0; }``
      - resimlerin arasında boşluk kalmadı: ``.galeri figure { width: 22%; }``
      - boşluğu aralara dağıt: ``.galeri { justify-content: space-between; }``

      ..

      - resim altı yazılarını ortaya hizalasınlar
      - yuvarlak köşeli resimler: ``.galeri img { border-radius: 10%; }``

      ..

      - tabloyu ikinci sütuna alsınlar

      Başlıkta şunları değiştirsinler:

      - resme bitişsin
      - arka plan rengi olsun
      - metin ile hizalansın
      - yazı tip boyu büyüsün


.. slide:: Family Guy
   :noheading:

   .. container:: h-full flex justify-center items-center

      .. image:: family_guy.*

   .. speaker-notes::

      - CSS'i yönetmek zor
      - tarayıcılar arasında farklar olabiliyor
      - şu anda boya göre kendini ayarlıyor ama düzen değiştirmiyor
      - cep telefonunda tabloyu hala sağda çıkarmasın, aşağı devam etsin
      - hazır paketler yardımcı oluyor: gelecek oturum Bulma
