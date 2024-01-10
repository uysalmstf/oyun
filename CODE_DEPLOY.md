1. Uygulamanın root dizininde appspec.yml dosyası istenen özelliklerle hazırlanır.(hooks özellikleri ile)
2. AWS'de IAM role ü CodeDeploy olan role oluşturulur.
3. AWS'de (eğer kaldıracaksa) free plan olan ec2 instance launch edilir.
4. Ayağa kalkarken uygulanacak scriptler instance oluşturulurken yazılır.
5. Daha rahat tqanımak için Tag eklenir.
6. Security group sekmesinden http için 80 portu ve ihtiyaç olan diğer portlar açılır. Eğer özel güvenlik eklenecekse(ip bazlı gibi) eklenir.
7. CodeDeploy bölümünden Application oluşturulur.
8. Buradan yine deployement group oluşturulur.
9. Oluştururken üstte oluşturduğumuz codedeployrole seçimi son derece önemlidir.
10. Üstte oluşturduğumuz tag seçilir.
11. İhtiyaca göre load balancer ayarı seçilir - boş bırakılır.
12. Pipeline alanına girilip create pipeline ile pipeline oluşturma aşamasına geçilir.
13. Source stage kısmında github v2 seçilir. 
14. Buradan giithubda ilgili repository e bağlanılır.
15. Main branch da burada seçilir.
16. Deploy sekmesinde AWS CodeDeploy seçilir.
17. Oluşturulan application ve deployement group seçim işlemleri yapılır.