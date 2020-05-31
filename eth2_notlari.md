---
title: Ethereum 2.0 Notları
description: Ethereum 2.0 güncellemesi ve ölçeklenme problemi hakkında notlar
---

*Son güncelleme: 30.05.2020*



**Okumadım özet geç**
> *Ethereum'un geniş çaplı kullanıma hazır olması için tüm blockchainlerin yaşadığı ölçeklenme problemini çözmesi gerekiyor. Ethereum 2.0 bu problemi (beraberinde başka şeyleri de) çözmeyi hedefleyen çok aşamalı, büyük bir güncelleme.*
> 
**Mining bitecek mi?**
> *Hemen değil, Staking'le paralel bir süre daha devam edecek*
> 
**Etherumlarım, Tokenlarım var ne yapmalıyım?**
> *Hiçbirşey yapmanıza gerek yok, validator adayı değilseniz sizin için herşey normal seyrinde devam edecek. İster exchange'lerde ister kendi cüzdanlarınızda olsun önemi yok, herhangibir aksiyon almanıza gerek yok. Tüm transferlerinizi, işlemlerinizi aynı şekilde endişelenmeden yapmaya devam edebileceksiniz bütün süreç boyunca.*
> 
**Staking nasıl yapabilirim?**
> *PoS aktifleştirildiği zaman validator olup staking yapabilmek için minimum 32 Ether kilitleme gereksinimi olacak. Nasıl yapılacağıyla ilgili detayları henüz konuşmak için erken. Detayları bu dökümanı sürekli güncelleyerek ekleyebiliriz.* 
> 
ETH 2.0 Terminolojisi
-----
- **PoS**: *Proof-of-Stake konsensus protokolü.*
- **Validator**: *PoS konsensus'ta karar alma sürecine (blok üretimi/doğrulaması) dahil olan aktörler.* 
- **Staking**: *Kısaca: "Bitcoin ve ETH2 öncesi Ethereumdaki PoW'da bulunan madenciliğin PoS versiyonudur." 
PoW'da madenciliğin şekli elektrik enerjisi ve çeşitli operasyonel maliyetleri kullanarak, aynı maliyete maruz kalmadan taklitleri üretilemeyen kanıtları yaratmaktır. PoS'ta aynı prensip, ağın kendi para birimini teminat göstererek aynı taklit edilemez kanıtları oluşturmaktır. Bu kanıtları oluşturma sürecine dahil olanların yaptıkları işe verilen isim Staking.*
- **Sharding**: *Dağıtık veritabanı sistemlerinin verimliliğini arttırmaya yönelik teknoloji mimarisi.*
- **Beacon Chain**: Ethereum'un yeni tasarımındaki parçalarıyla (shardlarıyla) ilgili metadata ve kanıtları bulunduran ana zincir.




5 dakikada ölçeklenme mevzusu
-----
Ethereum 2.0'ı anlamak için, önce blokchainlerdeki ölçeklenme problemini anlamalıyız.

Katılımcıların birbirini tanımadığı ve güvenmediği istemciler arası ağlarda (örn. blockchain) kolayca doğrulanabilen ortak kararlara varabilmek zor bir problem.

**Blockchainler bu probleme çözüm sağlıyor ancak katılımcı/kullanıcı sayısı ve veri miktarı arttıkça ağdaki karar alabilme kapasitesini de aynı oranda arttırmak zorlaşıyor.** 

Blockchainlerdeki ölçeklenme problemi özetle budur.

Tron, EOS, XRP, {$RANDOM_SHITCOIN} hızlıyken (TPS geyikleri) neden ETH, BTC gibi chainler yavaş? Bu sorunun cevabını kendinize şu iki soruyu sorarak bulabilirsiniz:

- **10.000 kişi mi daha hızlı ortak karar alır yoksa 5 kişi mi?**
- **10.000 kişinin ortak kararına mı güvenirsiniz, yoksa 5 kişinin mi?**

Denklem basit: 

**Az güvenlik** (yüksek merkezileşme) = **Yüksek Hız**
**Yüksek güvenlik** (az merkezileşme) = **Düşük Hız**

### Çözüm Türleri

[[The State of Layer-2 Protocol Development][3]]

**Layer-1**: *Zincirin işlem kapasitesini arttıran çözümlerdir.*
> 
> Orjinal protokolde ve zincirde **zorunlu** (segwit özelinde *yarı-zorunlu*) güncellemeler gerektirir. (Sharding, Casper, Segwit vs.).

**Layer-2**: *Zincirin işlem kapasitesini değiştirmeden, zincir dışı destekleyici çözümlerle işlem kapasitesini arttıran çözümlerdir.*

> Orjinal protokolde değişiklik gerektirmezler. (Lightning Network, Liquid,  Optimistic Rollup, State-channels, Plasma, ZK-STARKS) 


Bitcoin için Layer-1 konuşulduğunda kan gövdeyi götürüyor (Blockstream, Bitcoin XT, Bitcoin Cash), Layer-2 de zaten hayalet kasabadan farksız. (Vicdanı sızlamadan burda "Lightning Network" diyebilecek var mı gerçekten?)

Ethereum Layer-1 ve Layer-2'yi birden paralel yürütüyor fakat yaklaşımlardaki görüş farklılıkları, zaten yeterince kompleks olan problemlere daha da kompleks çözümler geliştirilmesi, çok fazla farklı şirket ve geliştirici grubunun birbirilerinden bağımsız çalışıyor olması gibi faktörler hızlı ilerlemeyi ve uygulamayı zorlaştırıyor.



### Ethereum nasıl ölçeklenecek?

[[Prysmatic Labs: How to Scale Ethereum Sharding Explained][2]]

Ethereum 2.0'ın yol haritasında ölçeklenme için nihahi hedefi **sharding**  implementasyonu.

Sharding’i tek başına bir konu olarak ayrıca incelemek lazım, özellikle Ethereum’a sharding'i dahil ettiğinizde genelde sorularınızın sayfalarca cevapları olmasına rağmen asla emin olamıyorsunuz, ki duruma bakılırsa kimse olamıyor demekki. Zaten 3. aşamayla tam entegre edilecek halinin spesifikasyonu henüz tamamlanmış değil.

Eski MMORPG severler Ultima Online'ı duymuştur. Bazı rivayetlere göre sharding
onların isimlendirdiği ve popülerleştirdiği bir teknoloji. **Sharding** ismi de
oyunun veritabanını ölçeklendirmek için yaptıkları güncellemeyi, oyunun
hikayesine yedirmek için kullandıkları isim. [[Ultima Online Shards][3]]

Ama blockchainlerde **sharding** kısaca: **Blockchaini parçalayıp minik blockchainler yapalım, bütün parçalar bilmesi gerektiği kadar bilsin (dolayısıyla az veriye ihtiyaç duysun, daha hızlı kararlar alabilsin) ama gerektiğinde parçalar birbiri arasında kolayca iletişim kurabilsin.**


**Yapmak neden zor?** [[Ethereum Sharding Wiki][4]]
1. Parçalar’ın kendi içinde tutarlı olduğunu kim, nasıl, hangi teşvikle kontrol edecek? 
2. Parçaların birbiri arasındaki güvenli iletişimini kim, nasıl, hangi teşvikle sağlayacak?
3. Teşvikler hangi tip rasyonel davranışları ne tür bir ekonomik tasarımda enforse etmeli?


Sharding'in mümkün olması için öncelikle ağın ekonomik tasarımının uygun şekilde güncellenmesi gerekiyor. Ağın güvenliğinin de bağlı olduğu bu faktör çok hassas bir dengeye sahip.

Ölçeklenme çözümünün getirdiği merkezileşme ve güvenlik sorunlarının kompanse edileceği güncel bir mekanizmaya geçilmesi şart. Bu yüzden Ethereum 2.0 aşama aşama uygulamaya geçecek.


## Ethereum 2.0
[[Bitmex Research: Ethereum 2.0][1]]

Tahmini zamanı: Temmuz 2020

Ethereum'un ölçeklenmesini sağlayacak olan *sharding* teknolojisi ve sharding'in öngereksinimleri olan diğer protokol geliştirmeleri ve değişikliklerini barındıran çok aşamalı güncelleme.

Aşamalar kısaca: 
- **Beacon Chain**
Ethereum 1.0 zincirine paralel PoS kullanan Ethereum 2.0 zinciri çalışmaya başlayacak. 1.0 zincirinden 2.0'a tek yönlü Ether aktarımı mümkün olacak. 2.0 zincirinde bulunan Ether sadece staking için kullanılabilecek.
- **Shard Chains**
Yeni yaratılan ana zinciri daha ufak parçalara bölen *Sharding* implemente edilecek.
- **State Execution**
Ethereum 1.0 zincirindeki bütün veri Ethereum 2.0 zincirine aktarılacak. Böylece Ethereum 1.0 zinciri artık ana zincirin ufak bir parçası (*shard'ı*) olarak devam edecek.


**Beacon Chain** ile birlikte Ethereum 2.0, mevcut Ethereum 1.0 zincirine paralel PoS testnet olarak başlayacak. Güncellemedeki aşamaların hepsi tamamlanana dek aktivitenin çoğu Ethereum 1.0 chaininde devam ediyor olacak. Bunun anlamı, Ethereum 2.0'deki PoS mekanizması Ethereum 1.0'daki blokları üretecek.

**Ethereum 2.0 ile 1.0 ağlarının farklı para birimleri olmayacak. İki farklı ağ gibi düşünülmesin. Sadece aralarında tek yönlü aktarım bulunuyor (1->2).**

Ethereum’da ölçeklenme yaklaşımı olarak sharding benimsendiği için, bu değişiklikler ve geliştirmeler, sharding’in öngereksinimleri olarak test edilmek zorundalar.

Buradaki esas mücadele, ölçeklendirme çözümlerinin beraberinde getirdiği güvenlik problemlerini ortadan kaldırabilmek ve tutarlı oyun teorisini kurabilmek konusunda. Eğer doğru ekonomik tasarım sağlanamazsa ağ merkezileşmeye zorlanabilir.

Böylesine geniş çaplı ve olası sonuçları iyi ölçülemeyen bir güncelleme Ethereum açısından elbette çok riskli. Kötü gidebilecek çok fazla senaryo var. Ama bunlar er ya da geç denemek zorunda kalınacaktı, başka türlü hedeflenen ölçeklere ulaşmak pratik olarak mümkün değil.



---

*Thanks: [Kemal Kocabıyık](https://twitter.com/kkocabiyik), [Onur Solmaz](https://twitter.com/onurhsolmaz)*

Kaynaklar
-----
1. [Bitmex Research: Ethereum 2.0][1]
2. [Prysmatic Labs: How to Scale Ethereum Sharding Explained][2]
3. [Ultima Online Shards][3]
4. [Consensys: The State of Ethereum Layer 2 Protocol Development][4]
5. [Ethereum Sharding Wiki][5]

[1]: https://blog.bitmex.com/ethereum-2-0/
[2]: https://medium.com/prysmatic-labs/how-to-scale-ethereum-sharding-explained-ba2e283b7fce
[3]:https://www.reddit.com/r/ultimaonline/comments/6wsl1y/new_player_confused_about_shards/
[4]: https://media.consensys.net/the-state-of-ethereum-layer-2-protocol-development-2-f22b2603abd6
[5]: https://github.com/ethereum/wiki/wiki/Sharding-FAQ