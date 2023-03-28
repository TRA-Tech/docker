
# Docker 
## İçindekiler
- [Docker Swarm](https://github.com/TRA-Tech/docker/blob/main/docker-swarm.md)
- Docker Compose 
- Docker Volume
- Docker Registry
- Dockerfile


![image](https://user-images.githubusercontent.com/100773960/228240739-661990d7-be4e-4e52-a273-8f9c44f2519e.png)

Docker, uygulamaların taşınabilirliğini sağlayan ve yazılım geliştirme sürecini hızlandıran bir konteyner platformudur. 

Docker, açık kaynaklı bir platform olması nedeniyle, geniş bir topluluk tarafından desteklenmektedir ve sürekli olarak geliştirilmektedir. Docker, hızlı ve kolay bir şekilde uygulama oluşturmanızı, dağıtmanızı ve yönetmenizi sağlar.
Ayrıca, Docker Hub gibi birçok farklı kaynak, hazır konteyner görüntüleri ve konfigürasyon dosyaları sunarak, uygulama geliştirme ve dağıtım sürecini hızlandırır.
Docker, birçok farklı platformda çalışabilir ve uygulamaları hızlı ve güvenli bir şekilde dağıtmak için yaygın olarak kullanılır. Docker, uygulamaların taşınabilirliğini artırırken, uygulama geliştiricileri ve sistem yöneticileri arasındaki işbirliğini kolaylaştırır.

Sonuç olarak, Docker, uygulama geliştirme ve dağıtım süreçlerinde büyük bir fark yaratan güçlü bir platformdur.

Docker teknolojisinden önce, uygulama geliştirme ve dağıtımı için sanal makineler (virtual machines - VMs) kullanılıyordu. Sanal makineler, bir fiziksel bilgisayarda çalışan bir işletim sistemine benzer bir sanal işletim sistemi çalıştıran ve uygulama ve kaynakları birlikte paketleyen bir sanal ortam sağlarlar. Bu şekilde, uygulama geliştiricileri ve sistem yöneticileri, uygulamaların farklı bilgisayarlarda ve işletim sistemlerinde sorunsuz bir şekilde çalışmasını sağlayabilirler.

Ancak, sanal makinelerin kullanımı bazı dezavantajlar da taşır. Sanal makineler, daha fazla bellek ve işlemci gücü gerektirdiğinden daha yavaş performans gösterirler. Ayrıca, sanal makinelerin ölçeklendirilmesi zor ve yavaş olabilir. Bu nedenle, Docker teknolojisi, sanal makinelerin yerini alarak daha hafif ve hızlı bir alternatif sunar. 

Sanal mimari ve Konteyner mimarisinin farkları aşağıdaki gibidir.

![image](https://user-images.githubusercontent.com/100773960/228242016-c8b49f09-4a89-45ac-b1f1-b7595010c06a.png)


## Docker Bileşenleri


Docker Engine, Docker'ın temel bileşenidir ve uygulamaların Docker konteynerleri içinde çalıştırılmasını sağlayan bir açık kaynaklı konteyner çalıştırma motorudur. Docker Engine, işletim sistemi düzeyinde sanallaştırma teknolojisi kullanır ve birden fazla konteynerin aynı işletim sistemi çekirdeği üzerinde çalışmasına olanak tanır.

Docker Engine, birçok bileşeni içerir. Bunlar arasında Docker Daemon, Docker API, Docker CLI, Docker imajları ve Docker registry yer alır.

- **Docker Daemon**, Docker Engine'in kalbidir. Konteynerleri yönetir, imajları indirir ve saklar, ağları oluşturur ve yönetir, sistem kaynaklarını konteynerler arasında paylaştırır ve diğer Docker bileşenleriyle iletişim kurar.
- **Docker API**, uygulamaların Docker Engine'e erişmesine olanak tanır. Docker CLI gibi araçlar, Docker API'ye istek gönderir ve konteynerlerin, imajların ve diğer kaynakların yönetimini sağlar.
- **Docker CLI**, kullanıcıların Docker Engine ile etkileşim kurmalarını sağlar. Kullanıcılar, konteynerlerin, imajların ve diğer Docker kaynaklarının oluşturulmasını, yönetilmesini ve silinmesini sağlayabilirler.
- **Docker imajları**, konteynerlerin temel yapı taşıdır. İmajlar, bir uygulama ve bağımlılıklarını içerir ve konteynerlerin oluşturulmasında kullanılır.
- **Docker registry**, Docker imajlarının depolanmasını ve paylaşılmasını sağlar. Docker Hub, Docker'ın varsayılan imaj deposudur ancak diğer registriesler de kullanılabilir.

Docker Engine, birçok platformda çalışabilir ve birçok programlama dili ve araç setiyle uyumlu olabilir. Bu nedenle, Docker Engine, uygulamaların hızlı ve güvenli bir şekilde dağıtılması için yaygın olarak kullanılan bir teknolojidir.

## Docker Container


Container teknolojisi, yazılım uygulamalarını izole edilmiş bir çalışma ortamında çalıştırmak için kullanılan bir sanallaştırma yöntemidir. Containerlar, uygulamaların çalışması için gerekli olan tüm dosyaları, bağımlılıkları ve yapılandırmaları bir arada tutan taşınabilir bir paketleme formatıdır.

![container](https://user-images.githubusercontent.com/100773960/228242830-2d2c4a56-29cf-473d-a1dc-c67199955789.jpeg)

Bu teknoloji, uygulamaların farklı ortamlarda çalışmasını kolaylaştırır ve taşınabilir hale getirir. Herhangi bir sistemdeki container uygulamaları, sistemdeki diğer uygulamaları etkilemeden çalıştırılabilir.
Container teknolojisi, çeşitli avantajlar sağlar. Örneğin, daha yüksek işletim sistemi yoğunluğu sağlar, daha hızlı uygulama dağıtımı için kullanılabilir, uygulama izolasyonunu sağlar ve daha az donanım kaynağı gerektirir. En popüler container teknolojileri arasında **Docker**, Kubernetes ve Apache Mesos bulunur.

## Docker Swarm

<img src="https://user-images.githubusercontent.com/100773960/228243346-090fc49b-463d-4bfa-9f46-937dff5214ab.png" width="500" height="300">

Docker Swarm, Docker motorunu kullanarak, birden fazla Docker konteynerını birden yönetmenizi sağlayan bir araçtır. Swarm, bir Docker ortamını yüksek erişilebilirlik, ölçeklenebilirlik ve dayanıklılık ile çalıştırmak için tasarlanmıştır. Bu sayede, uygulama hizmetleri sürekli çalışır ve talep arttıkça ölçeklenebilir.

Swarm, birden fazla Docker motorunu bir arada yönetmenizi sağlar. Bir Swarm kümesinde, Docker konteynerlarının dağıtımı ve yönetimi Swarm yöneticisi tarafından gerçekleştirilir. Bu yönetici, Swarm kümesindeki tüm Docker motorlarına komutlar gönderir ve konteynerların başlatılması, durdurulması ve ölçeklendirilmesi gibi işlemleri koordine eder.

Swarm, birkaç adımda kurulabilir ve birkaç komutla kullanılabilir. Ayrıca, Swarm ile konteynerları kolayca ölçeklendirebilir ve yüksek kullanılabilirlik sağlayabilirsiniz. Bu sayede, uygulama hizmetlerinin sürekli çalışması ve yüksek erişilebilirlik sağlanabilir.

## Docker Compose

<img src="https://user-images.githubusercontent.com/100773960/228244163-4d5bcc14-3ce4-4efd-8e54-b73a776ea75d.png" width="500" height="300">

Docker Compose, birden fazla Docker konteynerının bir arada çalıştırılmasını kolaylaştıran bir araçtır. Compose, Docker ortamınızda birden fazla konteyner oluşturmanıza, yapılandırmanıza ve çalıştırmanıza olanak tanır. 

Docker Compose, bir YAML dosyası kullanarak konteynerlarınızın yapılandırmasını tanımlamanızı sağlar.Bu YAML dosyasında, her konteynerın imajı, bağlantı noktaları, bağımlılıkları ve diğer yapılandırma ayarları belirtilir. Daha sonra, Compose kullanarak bu dosyayı yürütürsünüz ve Docker Compose, bu yapılandırmaya göre konteynerları oluşturur ve başlatır.

Compose, birkaç adımda kurulabilir ve birden fazla ortamda kullanılabilir. Bu sayede, geliştirme, test ve üretim ortamlarında konteynerları kolayca yönetebilirsiniz. Ayrıca, Compose, uygulamanızın birden fazla bileşenini bir arada çalıştırmanızı ve bu bileşenlerin birbirleriyle etkileşim kurmasını kolaylaştırır.

## Docker Volume

<img src="https://user-images.githubusercontent.com/100773960/228251804-3291230d-4c76-4e50-b091-abacd868f4fd.png" width="600" height="250">

Docker Volume, Docker konteynerlarının verilerinin saklanmasında kullanılan bir yöntemdir. Docker konteynerları, izole edilmiş bir ortamda çalıştığı için, konteynerın içindeki veriler normalde kalıcı değildir. Yani, konteyner silindiğinde veya yeniden oluşturulduğunda, tüm veriler kaybolur.

Docker Volume, bu sorunu çözmek için kullanılır. Bir Docker Volume oluşturarak, konteyner verilerini önceden belirlenmiş bir konumda depolayabilirsiniz. Bu, konteyner silinse bile verilerin korunmasını sağlar.

Docker Volume, farklı tiplerde veri saklama yöntemleri sağlar. Örneğin, host makinede bir klasör veya veritabanı sunucusunda bir veritabanı olabilir. Bu sayede, konteynerlar arasında veri paylaşımı kolaylaşır ve verilerin korunması sağlanır.

## Docker Registry

<img src="https://user-images.githubusercontent.com/100773960/228250317-cff87343-379d-438e-bb1e-f1809a5e70c7.png" width="700" height="250"> 

Docker Registry, Docker imajlarının merkezi bir depolanmasını ve yönetimini sağlayan bir araçtır. Registry, Docker imajlarını depolamanız, yönetmeniz ve dağıtmanızı kolaylaştırır.

Docker Registry, Docker imajlarınızın merkezi bir yerde depolanmasını sağlar. Bu, farklı Docker motorları veya Docker Swarm kümesindeki konteynerlar arasında imajların paylaşılmasını kolaylaştırır. Ayrıca, imajların yönetimini de sağlar. Registry, imajların sürümlerini yönetmenize ve imajların erişilebilirliğini kontrol etmenize olanak tanır.

Docker Hub, Docker'in resmi, bulut tabanlı bir Registry'sidir. Docker Hub, imajların kolayca depolanmasını, paylaşılmasını ve dağıtılmasını sağlar. Ancak, kendi özel Registry'nizi de kurabilirsiniz. Bu, Docker imajlarınızın kendi özel ağınızda veya bulut hizmetinizde depolanmasını sağlar.

Docker Registry, birkaç adımda kurulabilir ve farklı yapılandırmalarda kullanılabilir. Bu sayede, uygulama geliştirme, test ve üretim aşamalarında imajların yönetimini kolaylaştırabilirsiniz.

## Dockerfile 

<img src="https://user-images.githubusercontent.com/100773960/228255022-ca779169-2594-422c-907e-286964c9a98a.png" width="250" height="250"> 

Dockerfile, Docker konteynerlarının yapılandırılması ve imajlarının oluşturulması için kullanılan bir dosyadır. Dockerfile, konteyner için gereken tüm bileşenleri belirler ve bu bileşenleri kullanarak Docker imajının oluşturulmasını sağlar.

Dockerfile, basit bir metin dosyasıdır ve birkaç anahtar kelime içerir. Bu anahtar kelimeler, Docker imajının oluşturulması için gereken adımları belirler. Dockerfile, bir temel imaj, ek bileşenler, çalıştırılacak komutlar ve yapılandırma ayarları gibi unsurları içerebilir.

Dockerfile, imaj oluşturma sürecini otomatikleştirir ve bu sayede tekrar edilebilir ve ölçeklenebilir bir imaj oluşturma süreci sağlar. Ayrıca, Dockerfile, konteynerlarınızın yapısını ve bileşenlerini tanımladığı için, uygulamanızın taşınabilirliğini arttırır.

Dockerfile, birkaç adımda oluşturulabilir ve Docker CLI aracılığıyla Docker imajlarının oluşturulmasını sağlamak için kullanılabilir. Dockerfile'ın yapısı ve kullanımı, Docker'in temel bileşenlerinden biridir ve Docker konteyner teknolojisinin anlaşılmasında önemli bir rol oynar.

Örnek bir Dockerfile aşağıdaki gibidir;

```
# Temel imaj belirleme 
FROM python:3.9-alpine

# Çalışma dizini ayarlama 
WORKDIR /app

# Gerekli dosyaları kopyalama 
COPY requirements.txt 

# Gerekli paketleri yükleme 
RUN pip install --no-cache-dir -r requirements.txt

# Uygulama kodlarını kopyalama 
COPY . .

# Uygulamayı çalıştırma komutu 
CMD ["python", "app.py"]

```

Bu Dockerfile, bir Python uygulamasını çalıştırmak için kullanılabilir. Dockerfile, bir Alpine Linux tabanlı Python 3.9 imajından başlar. İmajın çalışma dizini /app olarak ayarlanır ve requirements.txt dosyası imaja kopyalanır. Daha sonra, pip aracılığıyla requirements.txt dosyasındaki gereksinimler yüklenir. Kod, Dockerfile ile aynı dizinde bulunan uygulama kodlarıyla kopyalanır. Son olarak, Docker imajı, uygulamanın çalıştırılması için gerekli komut olan "python app.py" komutunu içeren bir CMD komutuyla ayarlanır.

Bu Dockerfile, docker build komutu kullanılarak bir Docker imajı oluşturmak için kullanılabilir. Bu imaj, Python uygulamasını çalıştırmak için kullanılabilir.
