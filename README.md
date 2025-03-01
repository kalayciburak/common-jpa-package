# Common JPA Package

Bu proje, [common-package](https://github.com/kalayciburak/common-package) projesinin **JPA (Java Persistence API)**
özelliklerini içeren bir uzantısıdır. **Spring Boot** uygulamalarında veritabanı işlemlerini standartlaştırmak ve
kolaylaştırmak için tasarlanmıştır.

## 🚀 Özellikler

- ⚡ **Spring Data JPA** entegrasyonu
- ⚙️ **Temel JPA yapılandırmaları**
- 🔗 **Common Package** ile tam uyumlu
- ☕ **Java 21** desteği

## 📋 Gereksinimler

- **Java 21**
- **Maven**
- **Spring Boot 3.4.3**
- **GitHub Package Registry** erişimi

## 📥 Kurulum

### 1️⃣ GitHub Package Registry Yapılandırması

Projenizi **GitHub Package Registry**'den bağımlılık çekebilecek şekilde yapılandırmanız gerekmektedir.
`settings.xml` dosyanıza aşağıdaki yapılandırmayı ekleyin:

```xml
<settings>
    <servers>
        <server>
            <id>github</id>
            <username>GITHUB_KULLANICI_ADINIZ</username>
            <password>GITHUB_TOKEN</password>
        </server>
    </servers>
</settings>
```

### 2️⃣ Bağımlılık Ekleme

Projenizin `pom.xml` dosyasına aşağıdaki bağımlılığı ekleyin:

```xml
<dependency>
    <groupId>com.kalayciburak</groupId>
    <artifactId>common-jpa-package</artifactId>
    <version>0.0.1-SNAPSHOT</version>
</dependency>
```

## 💡 Kullanım

Bu paket, **JPA ile ilgili temel yapılandırmaları ve özellikleri** içerir.
**Common Package**’in sunduğu özelliklere ek olarak, veritabanı işlemleri için gerekli olan **JPA özelliklerini** sağlar.

### 🏗 Örnek Kullanım

```java
@Entity
public class ExampleEntity extends BaseEntity {
    // Entity özellikleri
}

@Repository
public interface ExampleRepository extends BaseRepository<ExampleEntity, String> {
    // Repository metodları
}

@Component
public class SecurityAuditorProvider implements AuditorProvider {
    // AuditorProvider implementasyonu
    @Override
    public String getCurrentAuditor() {
        Authentication auth = SecurityContextHolder.getContext().getAuthentication();
        return (auth != null && auth.isAuthenticated()) ? auth.getName() : "anonymousUser";
    }
}
```

## 📚 Dokümantasyon

Daha detaylı bilgi için:

- 📖 [Spring Data JPA Dokümantasyonu](https://docs.spring.io/spring-data/jpa/docs/current/reference/html/)
- 📖 [Common Package Dokümantasyonu](https://github.com/kalayciburak/common-package)

## 🤝 Katkıda Bulun

Her türlü katkıya açığız! **Pull Request** göndermekten çekinmeyin. 🚀

## 📜 Lisans

Bu proje, repoda belirtilen lisans koşulları altında sunulmaktadır.

## 📬 İletişim

👨‍💻 **Geliştirici:** Burak Kalaycı  
📧 **E-posta:** kalayciburak1996@gmail.com  
🐙 **GitHub:** [kalayciburak](https://github.com/kalayciburak)

---

> "Kodunuzu akıllıca, veritabanınızı zahmetsizce yönetin!" 🚀