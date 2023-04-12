## Dockerfile 

<img src="https://user-images.githubusercontent.com/100773960/228255022-ca779169-2594-422c-907e-286964c9a98a.png" width="250" height="250"> 

Container yapısının metin bazlı olarak tutulduğu dosya Dockerfile’dır. Dosya sistemine eklenen Dockerfile (tam olarak böyle yazılmalıdır çünkü Docker CLI büyük küçük harf duyarlıdır.) içindeki Instruction’lar (yönergeler) Docker Daemon tarafından okunur, değerlendirilir ve yeni bir Image bu Instruction’lar çerçevesinde oluşturulur.

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
