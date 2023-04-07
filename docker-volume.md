## Docker Volume

<img src="https://user-images.githubusercontent.com/100773960/228251804-3291230d-4c76-4e50-b091-abacd868f4fd.png" width="600" height="250">

Docker Volume, Docker konteynerlarının verilerinin saklanmasında kullanılan bir yöntemdir. Docker konteynerları, izole edilmiş bir ortamda çalıştığı için, konteynerın içindeki veriler normalde kalıcı değildir. Yani, konteyner silindiğinde veya yeniden oluşturulduğunda, tüm veriler kaybolur.

Docker Volume, bu sorunu çözmek için kullanılır. Bir Docker Volume oluşturarak, konteyner verilerini önceden belirlenmiş bir konumda depolayabilirsiniz. Bu, konteyner silinse bile verilerin korunmasını sağlar.

Docker Volume, farklı tiplerde veri saklama yöntemleri sağlar. Örneğin, host makinede bir klasör veya veritabanı sunucusunda bir veritabanı olabilir. Bu sayede, konteynerlar arasında veri paylaşımı kolaylaşır ve verilerin korunması sağlanır.

Aşağıdaki örnek Docker komutları, bir Docker volume oluşturma ve kullanma örneğini göstermektedir:

1. Öncelikle, bir Docker volume oluşturmak için aşağıdaki komutu kullanın:
```
docker volume create mydata
```
Bu komut, "mydata" adında bir Docker volume oluşturacaktır.

2. Daha sonra, bir konteyner oluştururken, oluşturduğumuz Docker volume'ı bağlamak için "-v" parametresini kullanabilirsiniz. Aşağıdaki komut, "mydata" adlı Docker volume'ı /data klasörüne bağlar:
```
docker run -d --name mycontainer -v mydata:/data nginx
```
Bu komut, "mycontainer" adında bir Nginx konteynerı oluşturacak ve "mydata" adlı Docker volume'ını /data klasörüne bağlayacaktır.

3. Son olarak, Docker volume'a veri yazmak için, oluşturduğumuz konteynera bağlanın ve /data klasörüne veri yazın. Aşağıdaki komut, "mycontainer" adlı konteynera bağlanır ve /data klasörüne bir index.html dosyası yazar:
```
docker exec -it mycontainer sh
echo "Hello World" > /data/index.html
exit
```
Bu komut, "mycontainer" adlı konteynera bağlanacak ve /data klasörüne bir index.html dosyası yazacaktır.

4. Son olarak, /data klasörüne yazdığınız veriyi, diğer konteynerlarda veya ana bilgisayarda kullanabilirsiniz. Örneğin, bir web tarayıcısını açarak, http://localhost/index.html adresine giderek, "Hello World" yazısını görüntüleyebilirsiniz.

Bu örnek, bir Docker volume oluşturma ve kullanma işlemini basit bir şekilde göstermektedir. Volume'ların kullanımı, veri yönetimi ve paylaşımı için çok kullanışlıdır.
