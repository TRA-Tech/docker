## Docker Volume

<img src="https://user-images.githubusercontent.com/100773960/228251804-3291230d-4c76-4e50-b091-abacd868f4fd.png" width="600" height="250">

Docker Volume, Docker konteynerlarının verilerinin saklanmasında kullanılan bir yöntemdir. Docker konteynerları, izole edilmiş bir ortamda çalıştığı için, konteynerın içindeki veriler normalde kalıcı değildir. Yani, konteyner silindiğinde veya yeniden oluşturulduğunda, tüm veriler kaybolur.

Docker Volume, bu sorunu çözmek için kullanılır. Bir Docker Volume oluşturarak, konteyner verilerini önceden belirlenmiş bir konumda depolayabilirsiniz. Bu, konteyner silinse bile verilerin korunmasını sağlar.

Docker Volume, farklı tiplerde veri saklama yöntemleri sağlar. Örneğin, host makinede bir klasör veya veritabanı sunucusunda bir veritabanı olabilir. Bu sayede, konteynerlar arasında veri paylaşımı kolaylaşır ve verilerin korunması sağlanır.
