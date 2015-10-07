Anadolu Üniversitesi MOOCS (Open edX)
========
Anadolu Üniversitesi Open edX platformu için şablon çalışmasıdır.


![Alt text](/anadolu.jpg?raw=true "Anadolu Üniversitesi MOOCS")

Şablon Hakkında
===============
Temayı yüklemek için aşağıdaki adımları izleyiniz.:
- Projeyi fork ile kendi hesabınıza ekleyiniz.
- OpenEdx'i kurunuz (https://github.com/edx/configuration/wiki/edX-Ubuntu-12.04-64-bit-Installation)
- Daha sonra /edx/app/edxapp  dizini altına "themes" isimli bir klasör oluşturup themes klasörünün içine gidiniz.
- git clone https://github.com/{username}/anadolu.git dosyaları theme klasörünün içine indiriyoruz.
- Css ve görselleri kendinize göre düzenleyin.
- Tema ismini değiştirmek için static/sass/ anadolu.scss adını tüm dosyalarda anadolu ifadesi geçen kısımları düzeltmelisiniz.
- Özel şablonu edx te aktif etmek için /edx/app/edxapp klasörü altında bulunan lms.env.json dosyasında öncelikle 'USE_CUSTOM_THEME' parametresini True yapıp, 'THEME_NAME' kısmına ise tema isminizi yazmalısınız.
- cd /edx/app/edxapp/edx-platform
- source /edx/app/edxapp/edxapp_env
- paver update_assets lms --settings=aws
- servisleri tekrar başlatmayı unutmayınız.

/edx/bin/supervisorctl restart edxapp:
/edx/bin/supervisorctl restart edxapp_worker:
/edx/bin/supervisorctl status
