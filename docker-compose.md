## Docker Compose

<img src="https://user-images.githubusercontent.com/100773960/228244163-4d5bcc14-3ce4-4efd-8e54-b73a776ea75d.png" width="500" height="300">

Docker Compose, birden fazla Docker konteynerının bir arada çalıştırılmasını kolaylaştıran bir araçtır. Compose, Docker ortamınızda birden fazla konteyner oluşturmanıza, yapılandırmanıza ve çalıştırmanıza olanak tanır. 

Docker Compose, bir YAML dosyası kullanarak konteynerlarınızın yapılandırmasını tanımlamanızı sağlar.Bu YAML dosyasında, her konteynerın imajı, bağlantı noktaları, bağımlılıkları ve diğer yapılandırma ayarları belirtilir. Daha sonra, Compose kullanarak bu dosyayı yürütürsünüz ve Docker Compose, bu yapılandırmaya göre konteynerları oluşturur ve başlatır.

Compose, birkaç adımda kurulabilir ve birden fazla ortamda kullanılabilir. Bu sayede, geliştirme, test ve üretim ortamlarında konteynerları kolayca yönetebilirsiniz. Ayrıca, Compose, uygulamanızın birden fazla bileşenini bir arada çalıştırmanızı ve bu bileşenlerin birbirleriyle etkileşim kurmasını kolaylaştırır.

<br>

Aşağıdaki örnek docker-compose.yml dosyası, Nginx web sunucusunu ve bir Node.js uygulamasını içeren basit bir Docker Compose örneğidir:

```
version: "3" 
services: 
  nginx: 
    image: nginx:latest 
    ports: 
      - "80:80" 
    volumes: 
      - ./nginx.conf:/etc/nginx/nginx.conf 
      - ./html:/usr/share/nginx/html 
    depends_on: 
      - node 
  node: 
    build: . 
    ports: 
      - "3000:3000" 
    volumes: 
      - .:/usr/src/app
```

Yukarıdaki örnekte, iki adet servis tanımlanmıştır: Nginx ve Node.js. Her servis, bir Docker imajı ve konteyneri oluşturmak için gereken özellikleri içerir.

Nginx servisi, resmi Nginx imajını kullanır ve 80 numaralı portu konteyner içindeki 80 numaralı porta yönlendirir. Ayrıca, nginx.conf ve html dosyalarını Docker Compose dosyasının bulunduğu dizindeki dosyalardan monte eder. Bu sayede Nginx yapılandırma dosyasını ve web sayfalarını Docker Compose dosyasının bulunduğu dizindeki dosyalardan okuyabilir.

Node servisi, .dockerignore ve Dockerfile dosyalarının bulunduğu dizindeki kaynak kodunu kullanarak bir Node.js uygulaması oluşturur. Hizmet, 3000 numaralı portu konteyner içindeki 3000 numaralı porta yönlendirir ve kodun değiştirilmesini izlemek için kaynak kodunu Docker Compose dosyasının bulunduğu dizindeki /usr/src/app klasörüne bağlar.

Bu örnek Docker Compose dosyasını çalıştırmak için, dosyanın bulunduğu dizine gidin ve aşağıdaki komutu çalıştırın:
```
docker-compose up
```

Bu komut, Nginx ve Node.js konteynerlarınızı oluşturacak ve Docker Compose dosyasında belirtilen bağımlılıkları yönetecektir. Web tarayıcınızı açarak http://localhost adresine giderek Nginx web sunucusu ve Node.js uygulamasını çalışır halde görebilirsiniz.
