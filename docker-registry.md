## Docker Registry

<img src="https://user-images.githubusercontent.com/100773960/228250317-cff87343-379d-438e-bb1e-f1809a5e70c7.png" width="700" height="250"> 

Docker Registry, Docker imajlarının merkezi bir depolanmasını ve yönetimini sağlayan bir araçtır. Registry, Docker imajlarını depolamanız, yönetmeniz ve dağıtmanızı kolaylaştırır.

Docker Registry, Docker imajlarınızın merkezi bir yerde depolanmasını sağlar. Bu, farklı Docker motorları veya Docker Swarm kümesindeki konteynerlar arasında imajların paylaşılmasını kolaylaştırır. Ayrıca, imajların yönetimini de sağlar. Registry, imajların sürümlerini yönetmenize ve imajların erişilebilirliğini kontrol etmenize olanak tanır.

Docker Hub, Docker'in resmi, bulut tabanlı bir Registry'sidir. Docker Hub, imajların kolayca depolanmasını, paylaşılmasını ve dağıtılmasını sağlar. Ancak, kendi özel Registry'nizi de kurabilirsiniz. Bu, Docker imajlarınızın kendi özel ağınızda veya bulut hizmetinizde depolanmasını sağlar.

Docker Registry, birkaç adımda kurulabilir ve farklı yapılandırmalarda kullanılabilir. Bu sayede, uygulama geliştirme, test ve üretim aşamalarında imajların yönetimini kolaylaştırabilirsiniz.

<br>
Aşağıda örnekte kullanımı gösterilmiştir.
<br>

1. İlk olarak, bir Docker imajı oluşturmanız gerekiyor. Bunun için, bir Dockerfile oluşturun ve Docker imajınızı bu dosyayı kullanarak oluşturun. Örneğin, basit bir Node.js uygulaması için aşağıdaki Dockerfile'i kullanabilirsiniz:

```
FROM node:latest
WORKDIR /app
COPY . /app
RUN npm install
EXPOSE 3000
CMD ["npm", "start"]

```

2. Docker imajınızı oluşturduktan sonra, bu imajı Docker Registry'e yüklemeniz gerekiyor. Bunun için, önce Docker Registry'i çalıştırmalısınız. Docker Compose kullanarak Docker Registry'i aşağıdaki şekilde çalıştırabilirsiniz:

```
version: '3'

services:
  registry:
    image: registry:2
    ports:
      - 5000:5000

```

Bu, yerel makinenizde 5000 portunu dinleyen bir Docker Registry sunucusu çalıştıracaktır.

3. Docker imajınızı Docker Registry'e yüklemek için, imajı önce Docker Registry formatında etiketlemeniz gerekiyor. Örneğin, aşağıdaki komutla imajınızı "my-registry.com/my-image:latest" adıyla etiketleyebilirsiniz:
```
docker tag my-image:latest my-registry.com/my-image:latest
```
4. Docker imajınızı Docker Registry'e yüklemek için, aşağıdaki komutu kullanabilirsiniz:

```
docker push my-registry.com/my-image:latest
```

Bu, imajı Docker Registry'e yükleyecektir.

5. Docker imajınızı başka bir makinede kullanmak için, Docker Registry adresini kullanarak imajı çekebilirsiniz. Örneğin, aşağıdaki komutla imajı başka bir makineden çekebilirsiniz:

```
docker pull my-registry.com/my-image:latest
```

Bu, imajı yerel makinenize indirecektir.

Bu şekilde, Docker Registry kullanarak Docker imajlarını depolayabilir ve paylaşabilirsiniz.
