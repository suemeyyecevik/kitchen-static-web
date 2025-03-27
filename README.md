# Project-101 : Kittens Carousel Static Website deployed on AWS EC2 using Cloudformation
### Proje-101 : Cloudformation kullanılarak AWS EC2 üzerinde dağıtılan Kittens Carousel Statik Web Sitesi
## Description
Kittens Carousel is a static website application deployed with Apache Web Server on AWS Elastic Compute Cloud (EC2) Instance using AWS Cloudformation Service. 
### Kittens Carousel, AWS Cloudformation Service kullanılarak AWS Elastic Compute Cloud (EC2) Instance üzerinde Apache Web Server ile dağıtılan statik bir web sitesi uygulamasıdır.
## Problem Statement

![Project_101](Pro_Project_101.png)

- Your company has recently started a web application project that will serve as an attraction point for pet lovers. As a first step of the project, developers in your team have prepared a preliminary design of kittens carousel application and pushed necessary files for the project to the repository on Github. 
### Şirketiniz yakın zamanda evcil hayvan severler için bir cazibe noktası olarak hizmet verecek bir web uygulaması projesine başladı. Projenin ilk adımı olarak ekibinizdeki geliştiriciler yavru kedi carousel uygulamasının ön tasarımını hazırladılar ve proje için gerekli dosyaları Github'daki depoya gönderdiler.

- Your task is to show the how the design of application looks as static web page in the development environment. Thus, you need to deploy the web application using the `index.html` and an images given within the `static-web` folder. Note the followings for your web application.
   ### Göreviniz, uygulamanın tasarımının geliştirme ortamında statik web sayfası olarak nasıl göründüğünü göstermektir. Bu nedenle, `index.html` dosyasını ve `static-web` klasöründe verilen bir resmi kullanarak web uygulamasını dağıtmanız gerekir. Web uygulamanız için aşağıdakilere dikkat edin.
   - User should face first with `index.html` when web app started.
###  Web uygulaması başlatıldığında kullanıcı ilk olarak `index.html` ile karşılaşmalıdır.
   - Application should be deployed on Apache Web Server.
###  Uygulama Apache Web Sunucusu üzerinde konuşlandırılmalıdır.
   - Application should be deployed in the development environment on AWS EC2 Instance using AWS Cloudformation Service. In the development environment, you can configure your Cloudformation template using the followings,
### Uygulama, AWS Cloudformation Service kullanılarak AWS EC2 Instance üzerinde geliştirme ortamında dağıtılmalıdır. Geliştirme ortamında, Cloudformation şablonunuzu aşağıdakileri kullanarak yapılandırabilirsiniz,
      - The application stack should be created with new AWS resources. 
###  Uygulama yığını yeni AWS kaynakları ile oluşturulmalıdır.
      - Bonus:!!!The application should run on the latest version of Amazon Linux 2023 Image . Here is the link where you can find information about this challenge. ( https://docs.aws.amazon.com/linux/al2023/ug/ec2.html#launch-from-cloudformation )
###  - Bonus:!!!Uygulama Amazon Linux 2023 Image'in en son sürümünde çalışmalıdır. İşte bu meydan okuma hakkında bilgi bulabileceğiniz bağlantı. ( https://docs.aws.amazon.com/linux/al2023/ug/ec2.html#launch-from-cloudformation )
      - EC2 Instance type can be configured as `t2.micro`.
###  EC2 Instance tipi `t2.micro` olarak yapılandırılabilir.
      - Instance launched by Cloudformation should be tagged `Web Server of StackName` 
###  - Cloudformation tarafından başlatılan örnek `Web Server of StackName` olarak etiketlenmelidir
      - The Web Application should be accessible via web browser from anywhere.
### - Web Uygulamasına web tarayıcısı aracılığıyla her yerden erişilebilmelidir.
      - The Application files should be downloaded from Github repo and deployed on EC2 Instance using user data script within cloudformation template. 
### - Uygulama dosyaları Github repo'sundan indirilmeli ve cloudformation şablonu içindeki kullanıcı verileri komut dosyası kullanılarak EC2 Örneğine dağıtılmalıdır.
      - Kittens Carousel Application Website URL should be given as output by Cloudformation Service, after the stack created.
 ### - Kittens Carousel Uygulama Web Sitesi URL'si, yığın oluşturulduktan sonra Cloudformation Service tarafından çıktı olarak verilmelidir.

## Project Skeleton 

```
101-kittens-carousel-static-website-ec2 (folder)
|
|----readme.md         # Given to the students (Definition of the project)          
|----cfn-template.yml  # To be delivered by students (Cloudformation template)
|----static-web
        |----index.html  # Given to the students (HTML file)
        |----cat0.jpg    # Given to the students (image file)
        |----cat1.jpg    # Given to the students (image file)
        |----cat2.jpg    # Given to the students (image file)
```

## Expected Outcome

![Project 101 : Kittens Carousel Application Snapshot](./project-101-snapshot.png)

### At the end of the project, following topics are to be covered;
### Proje sonunda aşağıdaki konular ele alınacaktır;
- Apache Web Server Installation on Linux
### Linux'ta Apache Web Sunucusu Kurulumu
- Static Website Deployment
### Statik Web Sitesi Dağıtımı
- Bash scripting
### Bash komut dosyası oluşturma
- AWS EC2 Service
### 
- AWS Security Groups Configuration
###  AWS Güvenlik Grupları Yapılandırması
- AWS Cloudformation Service
### - AWS Cloudformation Hizmeti
- AWS Cloudformation Template Design
### AWS Cloudformation Şablon Tasarımı
- Git & Github for Version Control System
### Sürüm Kontrol Sistemi için Git & Github

### At the end of the project, students will be able to;
### Projenin sonunda öğrenciler şunları yapabileceklerdir;
- install Apache Web Server on Amazon Linux 2.
### Amazon Linux 2'ye Apache Web Sunucusu yükleyin.
- improve bash scripting skills using `user data` section in Cloudformation to install and setup web application on EC2 Instance.
### EC2 Instance'a web uygulaması yüklemek ve kurmak için Cloudformation'daki `kullanıcı verileri` bölümünü kullanarak bash komut dosyası yazma becerilerini geliştirin.
- configure AWS EC2 Instance and Security Groups.
### AWS EC2 Örneği ve Güvenlik Gruplarını yapılandırın.

- configure Cloudformation template to use AWS Resources.
###  AWS Kaynaklarını kullanmak için Cloudformation şablonunu yapılandırın.
- use AWS Cloudformation Service to launch stacks.
### yığınları başlatmak için AWS Cloudformation Service'i kullanın.
- use git commands (push, pull, commit, add etc.) and Github as Version Control System.
### git komutlarını (push, pull, commit, add vb.) ve Sürüm Kontrol Sistemi olarak Github'ı kullanabilir.
## Steps to Solution
  
- Step 1: Download or clone project definition from `ondia` repo on Github 
### Adım 1: Github'daki `ondia` reposundan proje tanımını indirin veya klonlayın
- Step 2: Create project folder for local public repo on your pc
###  Adım 2: Bilgisayarınızda yerel genel repo için proje klasörü oluşturun
- Step 3: Prepare a cloudformation template to deploy your app on EC2 Instance
###  Adım 3: Uygulamanızı EC2 Instance'a dağıtmak için bir cloudformation şablonu hazırlayın
- Step 4: Push your application into your own public repo on Github
### Adım 4: Uygulamanızı Github'da kendi genel reponuza aktarın
- Step 5: Deploy your application on AWS Cloud using Cloudformation template to showcase your app within your team.
###  Adım 5: Uygulamanızı ekibinizde sergilemek için Cloudformation şablonunu kullanarak uygulamanızı AWS Cloud'da dağıtın.

## Notes

- Customize the application by hard-coding your name instead of `student_name` within `index.html`.
### Uygulamayı `index.html` içinde `student_name` yerine kendi adınızı kodlayarak özelleştirin.

## Resources

- [AWS Cloudformation User Guide](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/Welcome.html)
