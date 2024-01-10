1. Her contract için Polygon kullanılarak bir smart contract oluşturulur.
2. Bunların yapacağı işlemleri belirleyen eventler solidity kullanılarak kodlanır ve bir akıllı sözleşme olarak deploy edilir.
3. Her bir event için bunları dinleyen listenerlar kodlanır.
4. Listener eventi dinler. Bu eventten gelen datayı event tipine göre kafkada topice producer yardımıyla koyar.
5. Kafka topicini dinleyen consumer, bu datayı alır ve type ile datayı bulk olarak, zamanı da real olarak sql e yazar.
6. Block bilgisini de aynı şekilde topikten alır ve kayıt eder.
7. Burada data uzun olacağı için, kayıttan zaman kazanmak adına işlem yapmadan consumerda sql e kayıt etme işini tercih ettim.
8. Data alınır, tipe göre datayı parse eden bir kod yazılır, bu kod frontende ilgili datayı websocket ile yollar.
9. Websocketten gelen datayı dinleyen frontend, ekrana datayı basar.

Eğer C# ile kodlama yapılacaksa nethereum, eğer nodejs ile kodlama yapılacaksa web3js kullanılmalıdır. 
DB olarak postgresql daha gelişmiş olduğundan kullanılabilir.

ÖNEMLİ NOKTALAR: 
Developera kolaylık açısından akıllı sözleşme içerikleri son derece önemlidir. 
Bu yüzden en önemli dökümantasyon burada yapılan olacaktır. Bu döküman, geliştirmeyi son derece hızlandıracaktır.
Swagger tarzı döküman uygulaması, geliştirme aşamasında kolaylıkl sağlayabilir.
