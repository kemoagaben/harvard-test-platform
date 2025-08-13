import React, { useState } from 'react';
import { CheckCircle, BookOpen, Brain, Calculator, Globe, User, Monitor, Heart, Zap } from 'lucide-react';

const TestPlatform = () => {
  const [currentPage, setCurrentPage] = useState('home');
  const [currentTest, setCurrentTest] = useState(null);
  const [currentQuestion, setCurrentQuestion] = useState(0);
  const [answers, setAnswers] = useState({});
  const [testCompleted, setTestCompleted] = useState(false);
  const [score, setScore] = useState(0);

  // Test verileri
  const tests = {
    english: {
      title: "İngilizce Anlama ve Algılama Testi",
      icon: <Globe className="w-8 h-8" />,
      questions: [
        {
          question: "What does 'compromise' mean?",
          options: ["To argue", "To find a middle ground", "To give up completely", "To be stubborn"],
          correct: 1
        },
        {
          question: "Choose the correct sentence:",
          options: ["He don't like coffee", "He doesn't likes coffee", "He doesn't like coffee", "He not like coffee"],
          correct: 2
        },
        {
          question: "What is the synonym of 'significant'?",
          options: ["Small", "Important", "Funny", "Quick"],
          correct: 1
        },
        {
          question: "Complete the sentence: 'If I _____ you, I would study harder.'",
          options: ["am", "was", "were", "be"],
          correct: 2
        },
        {
          question: "What does 'inevitable' mean?",
          options: ["Avoidable", "Uncertain", "Unavoidable", "Optional"],
          correct: 2
        },
        {
          question: "Choose the correct form: 'She has _____ working here for five years.'",
          options: ["been", "being", "be", "was"],
          correct: 0
        },
        {
          question: "What is the opposite of 'artificial'?",
          options: ["Fake", "Natural", "Modern", "Complex"],
          correct: 1
        },
        {
          question: "Complete: 'The book _____ I read yesterday was fascinating.'",
          options: ["who", "which", "where", "when"],
          correct: 1
        },
        {
          question: "What does 'contemporary' mean?",
          options: ["Old", "Modern", "Future", "Past"],
          correct: 1
        },
        {
          question: "Choose the correct sentence:",
          options: ["I have went there", "I have gone there", "I have go there", "I have going there"],
          correct: 1
        },
        {
          question: "What is the meaning of 'elaborate'?",
          options: ["Simple", "Detailed", "Quick", "Boring"],
          correct: 1
        },
        {
          question: "Complete: 'Neither John _____ Mary came to the party.'",
          options: ["or", "and", "nor", "but"],
          correct: 2
        },
        {
          question: "What does 'emphasize' mean?",
          options: ["To hide", "To stress", "To forget", "To avoid"],
          correct: 1
        },
        {
          question: "Choose the correct form: 'I wish I _____ speak French.'",
          options: ["can", "could", "will", "would"],
          correct: 1
        },
        {
          question: "What is the synonym of 'abundant'?",
          options: ["Scarce", "Plentiful", "Empty", "Small"],
          correct: 1
        },
        {
          question: "Complete: 'The meeting was postponed _____ next week.'",
          options: ["until", "since", "during", "while"],
          correct: 0
        },
        {
          question: "What does 'objective' mean?",
          options: ["Biased", "Emotional", "Impartial", "Personal"],
          correct: 2
        },
        {
          question: "Choose the correct sentence:",
          options: ["Less people came", "Fewer people came", "Lesser people came", "Few people came"],
          correct: 1
        },
        {
          question: "What is the meaning of 'comprehensive'?",
          options: ["Partial", "Complete", "Simple", "Narrow"],
          correct: 1
        },
        {
          question: "Complete: 'She acted _____ she knew everything.'",
          options: ["like", "as if", "such as", "similar"],
          correct: 1
        }
      ]
    },
    ethics: {
      title: "Etik Değerler Testi",
      icon: <Heart className="w-8 h-8" />,
      questions: [
        {
          question: "Bir arkadaşınız sizden sınavda kopya çekmenize yardım etmenizi isterse ne yaparsınız?",
          options: ["Yardım ederim", "Kibarca reddederim", "Öğretmene söylerim", "Durumu görmezden gelirim"],
          correct: 1
        },
        {
          question: "İş yerinde hata yapan bir meslektaşınızı gördüğünüzde ne yaparsınız?",
          options: ["Hemen patrona söylerim", "Önce kendisiyle konuşurum", "Hiçbir şey yapmam", "Başka arkadaşlara anlatırım"],
          correct: 1
        },
        {
          question: "Etik davranışın temel özelliği nedir?",
          options: ["Kârlı olmak", "Dürüst olmak", "Hızlı olmak", "Popüler olmak"],
          correct: 1
        },
        {
          question: "Çıkar çatışması durumunda ne yapmalısınız?",
          options: ["Kişisel çıkarımı tercih ederim", "Durumu açık bir şekilde bildiririm", "Sessiz kalırım", "Başkalarının ne yaptığına bakarım"],
          correct: 1
        },
        {
          question: "Gizli bilgiyi paylaşmak konusunda doğru yaklaşım nedir?",
          options: ["Güvendiğim kişilerle paylaşırım", "Asla paylaşmam", "Duruma göre karar veririm", "Faydası varsa paylaşırım"],
          correct: 1
        },
        {
          question: "Adil olmak ne demektir?",
          options: ["Herkesi aynı şekilde cezalandırmak", "Herkese eşit fırsat vermek", "En güçlüyü desteklemek", "Çoğunluğun istediğini yapmak"],
          correct: 1
        },
        {
          question: "Sorumlu davranış ne gerektirir?",
          options: ["Sadece kurallara uymak", "Sonuçları düşünmek", "Hızlı karar vermek", "Popüler olmak"],
          correct: 1
        },
        {
          question: "Takım çalışmasında en önemli etik değer nedir?",
          options: ["Rekabet", "İş birliği", "Liderlik", "Bireysellik"],
          correct: 1
        },
        {
          question: "Bir hata yaptığınızda ne yaparsınız?",
          options: ["Gizlerim", "Kabul eder ve düzeltirim", "Başkasını suçlarım", "Önemli değilmiş gibi davranırım"],
          correct: 1
        },
        {
          question: "Güven oluşturmanın temel şartı nedir?",
          options: ["Güçlü olmak", "Tutarlı olmak", "Zengin olmak", "Tanınmış olmak"],
          correct: 1
        },
        {
          question: "Etik ikilem yaşadığınızda ne yaparsınız?",
          options: ["Hızlıca karar veririm", "Farklı seçenekleri değerlendiririm", "Başkalarının ne yaptığına bakarım", "Karar vermekten kaçınırım"],
          correct: 1
        },
        {
          question: "Saygı göstermenin anlamı nedir?",
          options: ["Korkmak", "Farklılıkları kabul etmek", "Sessiz kalmak", "Aynı fikirde olmak"],
          correct: 1
        },
        {
          question: "Mesleki etik kuralların amacı nedir?",
          options: ["Ceza vermek", "Standart oluşturmak", "Kontrol sağlamak", "Korku yaratmak"],
          correct: 1
        },
        {
          question: "İnsan hakları konusunda doğru yaklaşım nedir?",
          options: ["Sadece kendi haklarımı düşünürüm", "Herkesin eşit haklara sahip olduğunu kabul ederim", "Güçlünün hakkı vardır", "Duruma göre değişir"],
          correct: 1
        },
        {
          question: "Şeffaflık ne demektir?",
          options: ["Her şeyi söylemek", "Açık ve dürüst olmak", "Gizli bilgi paylaşmak", "Hiçbir şey gizlememek"],
          correct: 1
        },
        {
          question: "Çevre sorumluluğu konusunda doğru yaklaşım nedir?",
          options: ["Sadece yasal zorunlulukları yerine getiririm", "Gelecek nesilleri de düşünürüm", "Ekonomik çıkarları öncelik veririm", "Başkalarının ne yaptığına bakarım"],
          correct: 1
        },
        {
          question: "Empati kurmanın önemi nedir?",
          options: ["Zayıflık göstergesidir", "İlişkileri güçlendirir", "Zaman kaybıdır", "Gereksizdir"],
          correct: 1
        },
        {
          question: "Etik liderliğin özelliği nedir?",
          options: ["Otoriter olmak", "Örnek davranış sergilemek", "Sert kurallar koymak", "Herkesi kontrol etmek"],
          correct: 1
        },
        {
          question: "Sosyal sorumluluk ne gerektirir?",
          options: ["Sadece kendimi düşünmek", "Topluma katkı sağlamak", "Kâr maksimizasyonu", "Rekabet avantajı"],
          correct: 1
        },
        {
          question: "Etik davranışın uzun vadeli faydası nedir?",
          options: ["Hızlı zenginlik", "Güven ve saygınlık", "Popülerlik", "Kontrol gücü"],
          correct: 1
        }
      ]
    },
    math: {
      title: "Matematik ve Zeka Testi",
      icon: <Calculator className="w-8 h-8" />,
      questions: [
        {
          question: "15 + 28 - 12 = ?",
          options: ["29", "31", "33", "35"],
          correct: 1
        },
        {
          question: "Bir dizide 2, 6, 18, 54, ... sonraki sayı nedir?",
          options: ["108", "162", "216", "270"],
          correct: 1
        },
        {
          question: "25'in %40'ı nedir?",
          options: ["8", "10", "12", "15"],
          correct: 1
        },
        {
          question: "Hangi sayı dizisi mantıklıdır: 1, 4, 9, 16, ?",
          options: ["20", "23", "25", "30"],
          correct: 2
        },
        {
          question: "144 ÷ 12 + 8 × 3 = ?",
          options: ["36", "48", "60", "72"],
          correct: 0
        },
        {
          question: "Bir üçgenin iç açıları toplamı kaç derecedir?",
          options: ["90", "180", "270", "360"],
          correct: 1
        },
        {
          question: "0.75'i kesir olarak ifade edelim:",
          options: ["3/4", "2/3", "4/5", "5/6"],
          correct: 0
        },
        {
          question: "Hangi sayı asal değildir?",
          options: ["13", "17", "19", "21"],
          correct: 3
        },
        {
          question: "X + 15 = 32 ise X = ?",
          options: ["15", "17", "19", "21"],
          correct: 1
        },
        {
          question: "Bir dairenin çevresini bulmak için hangi formülü kullanırız?",
          options: ["πr²", "2πr", "πd", "r²"],
          correct: 1
        },
        {
          question: "3² + 4² = ?",
          options: ["7", "14", "25", "49"],
          correct: 2
        },
        {
          question: "Hangi sayı 7'ye tam bölünür?",
          options: ["48", "52", "56", "60"],
          correct: 2
        },
        {
          question: "2, 3, 5, 8, 12, 17, ? sonraki sayı:",
          options: ["21", "23", "25", "27"],
          correct: 1
        },
        {
          question: "Bir kenarı 5 cm olan karenin alanı kaç cm²'dir?",
          options: ["20", "25", "30", "35"],
          correct: 1
        },
        {
          question: "(-3) × (-4) = ?",
          options: ["-12", "-7", "7", "12"],
          correct: 3
        },
        {
          question: "1/2 + 1/4 = ?",
          options: ["1/6", "2/6", "3/4", "1/8"],
          correct: 2
        },
        {
          question: "100'ün karekökü nedir?",
          options: ["5", "10", "15", "20"],
          correct: 1
        },
        {
          question: "Hangi sayı çift ve asal sayıdır?",
          options: ["0", "1", "2", "4"],
          correct: 2
        },
        {
          question: "5! (5 faktöriyel) nedir?",
          options: ["25", "60", "120", "240"],
          correct: 2
        },
        {
          question: "Bir dikdörtgenin alanı 48 cm², eni 6 cm ise boyu kaç cm'dir?",
          options: ["6", "7", "8", "9"],
          correct: 2
        }
      ]
    },
    culture: {
      title: "Genel Kültür Testi",
      icon: <BookOpen className="w-8 h-8" />,
      questions: [
        {
          question: "Türkiye'nin başkenti neresidir?",
          options: ["İstanbul", "İzmir", "Ankara", "Bursa"],
          correct: 2
        },
        {
          question: "Hangi gezegen Güneş'e en yakındır?",
          options: ["Venüs", "Merkür", "Mars", "Dünya"],
          correct: 1
        },
        {
          question: "İnsan vücudunda kaç kemik vardır (yaklaşık)?",
          options: ["106", "206", "306", "406"],
          correct: 1
        },
        {
          question: "Hangi yıl 1. Dünya Savaşı başlamıştır?",
          options: ["1912", "1914", "1916", "1918"],
          correct: 1
        },
        {
          question: "Dünyanın en büyük okyanusu hangisidir?",
          options: ["Atlantik", "Hint", "Pasifik", "Arktik"],
          correct: 2
        },
        {
          question: "Mozart hangi ülkeden bir besteciydi?",
          options: ["Almanya", "Avusturya", "İtalya", "Fransa"],
          correct: 1
        },
        {
          question: "Su'nun kimyasal formülü nedir?",
          options: ["H2O", "CO2", "O2", "H2SO4"],
          correct: 0
        },
        {
          question: "Hangi vitamin güneş ışığından elde edilir?",
          options: ["Vitamin A", "Vitamin B", "Vitamin C", "Vitamin D"],
          correct: 3
        },
        {
          question: "Roma İmparatorluğu'nun kurucusu kimdir?",
          options: ["Julius Caesar", "Augustus", "Romulus", "Nero"],
          correct: 1
        },
        {
          question: "Dünyanın en yüksek dağı hangisidir?",
          options: ["K2", "Everest", "Kilimanjaro", "Denali"],
          correct: 1
        },
        {
          question: "İnsan beyninin yaklaşık yüzde kaçı sudur?",
          options: ["%60", "%70", "%75", "%80"],
          correct: 2
        },
        {
          question: "Hangi element periyodik tabloda 'Au' sembolü ile gösterilir?",
          options: ["Gümüş", "Altın", "Alüminyum", "Arsenik"],
          correct: 1
        },
        {
          question: "Shakespeare'in ünlü oyunu 'Hamlet' hangi ülkede geçer?",
          options: ["İngiltere", "Fransa", "Danimarka", "Almanya"],
          correct: 2
        },
        {
          question: "Işık hızı saniyede yaklaşık kaç kilometre eder?",
          options: ["200.000 km", "300.000 km", "400.000 km", "500.000 km"],
          correct: 1
        },
        {
          question: "Osmanlı İmparatorluğu kaç yıl sürmüştür (yaklaşık)?",
          options: ["500 yıl", "600 yıl", "700 yıl", "800 yıl"],
          correct: 1
        },
        {
          question: "Hangi gezegen Güneş Sistemi'nde 'Kırmızı Gezegen' olarak bilinir?",
          options: ["Venüs", "Mars", "Jüpiter", "Satürn"],
          correct: 1
        },
        {
          question: "İnsan kalbinin dakikada kaç kez attığı normaldir?",
          options: ["50-70", "60-100", "80-120", "100-140"],
          correct: 1
        },
        {
          question: "Hangi sanatçı 'Mona Lisa' tablosunu yapmıştır?",
          options: ["Michelangelo", "Picasso", "Leonardo da Vinci", "Van Gogh"],
          correct: 2
        },
        {
          question: "Türkiye hangi kıtada yer alır?",
          options: ["Sadece Avrupa", "Sadece Asya", "Avrupa ve Asya", "Avrupa ve Afrika"],
          correct: 2
        },
        {
          question: "Hangi besin grubunda en çok protein bulunur?",
          options: ["Meyveler", "Sebzeler", "Et ve baklagiller", "Tahıllar"],
          correct: 2
        }
      ]
    },
    personality: {
      title: "Kişilik Analizi Testi",
      icon: <User className="w-8 h-8" />,
      questions: [
        {
          question: "Yeni insanlarla tanışmayı nasıl karşılarsınız?",
          options: ["Heyecanla beklerim", "Biraz gerilirim ama uyum sağlarım", "Oldukça gerilirim", "Mümkün olduğunca kaçınırım"],
          correct: 1
        },
        {
          question: "Stresli durumlarda nasıl davranırsınız?",
          options: ["Paniklerim", "Sakin kalmaya çalışırım", "Çözüm odaklı yaklaşırım", "Kaçar giderim"],
          correct: 2
        },
        {
          question: "Takım çalışmasında hangi rolü tercih edersiniz?",
          options: ["Lider olmak", "Destekleyici olmak", "Yaratıcı fikirler sunmak", "Tek başıma çalışmak"],
          correct: 1
        },
        {
          question: "Boş zamanınızda ne yapmayı seversiniz?",
          options: ["Sosyal aktiviteler", "Okumak/öğrenmek", "Spor yapmak", "Sanat/müzik"],
          correct: 1
        },
        {
          question: "Önemli kararları nasıl verirsiniz?",
          options: ["Hızlıca, sezgilerimle", "Uzun süre düşünerek", "Başkalarına danışarak", "Mantıklı analiz yaparak"],
          correct: 3
        },
        {
          question: "Eleştiriye nasıl tepki verirsiniz?",
          options: ["Alınganlık yaparım", "Yapıcı olanı dinlerim", "Saldırgan davranırım", "Görmezden gelirim"],
          correct: 1
        },
        {
          question: "Yeni projeler karşısında nasıl hissedersiniz?",
          options: ["Heyecanlanırım", "Endişelenirim", "Temkinli yaklaşırım", "Kayıtsız kalırım"],
          correct: 0
        },
        {
          question: "Çatışma durumlarında ne yaparsınız?",
          options: ["Saldırgan davranırım", "Uzlaşma ararım", "Kaçınırım", "Durumu büyütürüm"],
          correct: 1
        },
        {
          question: "Hedeflerinize ulaşmak için nasıl çalışırsınız?",
          options: ["Aceleci davranırım", "Planlı ve sabırlı olurum", "Başkalarına güvenirim", "Şansa bırakırım"],
          correct: 1
        },
        {
          question: "İnsan ilişkilerinde en önemli bulduğunuz değer nedir?",
          options: ["Güven", "Eğlence", "Fayda", "Popülerlik"],
          correct: 0
        },
        {
          question: "Hata yaptığınızda nasıl davranırsınız?",
          options: ["Inkâr ederim", "Kabul eder, düzeltirim", "Başkasını suçlarım", "Üzülür, çökkerim"],
          correct: 1
        },
        {
          question: "Değişime nasıl yaklaşırsınız?",
          options: ["Karşı çıkarım", "Uyum sağlarım", "Liderlik ederim", "Endişelenirim"],
          correct: 1
        },
        {
          question: "Başarı sizin için ne ifade eder?",
          options: ["Para kazanmak", "Kişisel gelişim", "Tanınmak", "Güç elde etmek"],
          correct: 1
        },
        {
          question: "Zor görevler karşısında ne hissedersiniz?",
          options: ["Kaçınma isteği", "Meydan okuma heyecanı", "Stres ve endişe", "Kayıtsızlık"],
          correct: 1
        },
        {
          question: "İletişimde hangi tarzı benimsersiniz?",
          options: ["Doğrudan ve net", "Diplomatik", "Saldırgan", "Pasif"],
          correct: 1
        },
        {
          question: "Motivasyonunuzu ne sağlar?",
          options: ["Rekabet", "İş birliği", "Tanınma", "Öğrenme"],
          correct: 3
        },
        {
          question: "Risk almak konusunda nasılsınız?",
          options: ["Çok riskli", "Hesaplı riskler alırım", "Riskten kaçınırım", "Umursamam"],
          correct: 1
        },
        {
          question: "Zamanlama konusunda nasılsınız?",
          options: ["Hep geç kalırım", "Dakik olurum", "Çok erken gelirim", "Umursamam"],
          correct: 1
        },
        {
          question: "Sorunları nasıl çözersiniz?",
          options: ["Duygusal yaklaşırım", "Mantıklı analiz yaparım", "Başkalarına danışırım", "Ertelemeyi tercih ederim"],
          correct: 1
        },
        {
          question: "Gelecek planları yaparken nasıl davranırsınız?",
          options: ["Detaylı planlar yaparım", "Genel hedefler belirlerim", "Akışına bırakırım", "Plan yapmam"],
          correct: 1
        }
      ]
    },
    computer: {
      title: "Bilgisayar Kullanım Testi",
      icon: <Monitor className="w-8 h-8" />,
      questions: [
        {
          question: "Windows'da bir dosyayı kopyalamak için hangi kısayol tuşunu kullanırsınız?",
          options: ["Ctrl+X", "Ctrl+C", "Ctrl+V", "Ctrl+Z"],
          correct: 1
        },
        {
          question: "E-posta adresinde '@' işaretinin anlamı nedir?",
          options: ["Özel karakter", "Kullanıcı adı ile domain'i ayırır", "Şifre göstergesi", "Spam işareti"],
          correct: 1
        },
        {
          question: "Bir web sitesinin güvenli olduğunu nasıl anlarsınız?",
          options: ["Renkli tasarım", "HTTPS ile başlayması", "Çok reklam olması", "Hızlı açılması"],
          correct: 1
        },
        {
          question: "PDF dosyası ne tür bir dosya formatıdır?",
          options: ["Resim dosyası", "Müzik dosyası", "Döküman dosyası", "Video dosyası"],
          correct: 2
        },
        {
          question: "Bilgisayarınızı virüslerden korumak için ne yaparsınız?",
          options: ["Sadece pahalı siteleri ziyaret ederim", "Antivirüs programı kullanırım", "Internete girmem", "Hiçbir şey yapmam"],
          correct: 1
        },
        {
          question: "Excel'de hücreleri toplamak için hangi fonksiyon kullanılır?",
          options: ["COUNT", "SUM", "AVERAGE", "MAX"],
          correct: 1
        },
        {
          question: "Şifre oluştururken hangisi en güvenlidir?",
          options: ["123456", "isim+doğum tarihi", "Büyük/küçük harf+sayı+özel karakter", "Aynı harf tekrarı"],
          correct: 2
        },
        {
          question: "Cloud (bulut) depolama neye yarar?",
          options: ["Bilgisayarı hızlandırır", "Dosyaları internette saklar", "Virüs temizler", "Oyun oynamaya yarar"],
          correct: 1
        },
        {
          question: "Ctrl+Alt+Del tuş kombinasyonu Windows'da ne işe yarar?",
          options: ["Kopyalama", "Yapıştırma", "Görev yöneticisini açar", "Kaydetme"],
          correct: 2
        },
        {
          question: "Spam e-postalar ile ne yapmalısınız?",
          options: ["Hemen açar okurım", "Spam klasörüne atarım", "Arkadaşlarıma yönlendiririm", "Cevap yazarım"],
          correct: 1
        },
        {
          question: "Wi-Fi şifresi ne işe yarar?",
          options: ["İnterneti hızlandırır", "Yetkisiz erişimi engeller", "Bilgisayarı korur", "Daha çok web sitesi açar"],
          correct: 1
        },
        {
          question: "Bir dosyayı kalıcı olarak silmek için ne yaparsınız?",
          options: ["Delete tuşuna basarım", "Çöp kutusunu boşaltırım", "Shift+Delete kullanırım", "Kapatırım"],
          correct: 2
        },
        {
          question: "Tarayıcıda (browser) gizli mod ne işe yarar?",
          options: ["Daha hızlı internete çıkar", "Geçmiş kaydetmez", "Virüs engeller", "Daha güzel görünür"],
          correct: 1
        },
        {
          question: "Bir dosyanın uzantısı (.doc, .pdf vb.) neyi gösterir?",
          options: ["Dosya boyutu", "Dosya türü", "Oluşturulma tarihi", "Sahip bilgisi"],
          correct: 1
        },
        {
          question: "İnternet bağlantı hızı hangi birimle ölçülür?",
          options: ["GB", "MB", "Mbps", "Hz"],
          correct: 2
        },
        {
          question: "Sosyal medyada gizlilik ayarları neden önemlidir?",
          options: ["Daha çok takipçi için", "Kişisel bilgileri korumak için", "Daha hızlı paylaşım için", "Reklam görmemek için"],
          correct: 1
        },
        {
          question: "Backup (yedekleme) ne demektir?",
          options: ["Dosyaları silmek", "Dosyaları kopyalamak", "Bilgisayarı kapatmak", "Program güncellemek"],
          correct: 1
        },
        {
          question: "USB bellek nedir?",
          options: ["İnternet bağlantısı", "Taşınabilir depolama", "Ekran kartı", "Hoparlör"],
          correct: 1
        },
        {
          question: "Video konferans programlarında mikrofonu kapatmak neden önemlidir?",
          options: ["Daha az elektrik harcar", "Gürültü kirliliğini önler", "Daha hızlı bağlanır", "Görüntü kalitesini artırır"],
          correct: 1
        },
        {
          question: "Bir web sitesini favorilere (bookmark) eklemenin faydası nedir?",
          options: ["Daha hızlı yükler", "Kolay erişim sağlar", "Güvenliği artırır", "Reklam engellez"],
          correct: 1
        }
      ]
    },
    psychology: {
      title: "Temel Psikoloji Testi",
      icon: <Brain className="w-8 h-8" />,
      questions: [
        {
          question: "Stres yönetiminde en etkili yöntem hangisidir?",
          options: ["Problemden kaçmak", "Nefes egzersizleri yapmak", "Sürekli endişelenmek", "Hiçbir şey yapmamak"],
          correct: 1
        },
        {
          question: "Empati ne demektir?",
          options: ["Acıma duymak", "Başkasının yerine koyabilmek", "Yargılamak", "Tavuk ödüllendirmek"],
          correct: 1
        },
        {
          question: "Pozitif düşünmenin faydası nedir?",
          options: ["Gerçekleri inkâr etmek", "Mental sağlığı destekler", "Sorumluluktan kaçmak", "Başkalarını kandırmak"],
          correct: 1
        },
        {
          question: "Motivasyon kaybı yaşadığınızda ne yaparsınız?",
          options: ["Pes ederim", "Küçük hedefler koyarım", "Sürekli şikâyet ederim", "Başkalarını suçlarım"],
          correct: 1
        },
        {
          question: "Sağlıklı iletişimin temel unsuru nedir?",
          options: ["Haklı çıkmak", "Aktif dinleme", "Eleştirmek", "Susarak geçmek"],
          correct: 1
        },
        {
          question: "Öfke kontrolü için en iyi yaklaşım nedir?",
          options: ["Bağırmak", "Nefes alıp sakinleşmek", "Saldırgan davranmak", "İçine atmak"],
          correct: 1
        },
        {
          question: "Özgüven geliştirmenin yolu nedir?",
          options: ["Başkalarıyla sürekli karşılaştırma", "Kendini kabul etme", "Mükemmeliyetçilik", "Başkalarını eleştirme"],
          correct: 1
        },
        {
          question: "Depresif duygular yaşadığınızda ne yapmalısınız?",
          options: ["İzole olmalı", "Profesyonel yardım almalı", "İnkâr etmeli", "Alkol kullanmalı"],
          correct: 1
        },
        {
          question: "Sağlıklı bir ilişkide olması gereken temel özellik nedir?",
          options: ["Kontrol", "Karşılıklı saygı", "Bağımlılık", "Rekabet"],
          correct: 1
        },
        {
          question: "Travmatik bir yaşantı sonrası ne yapılmalı?",
          options: ["Unutmaya çalışmak", "Profesyonel destek almak", "Alkole başvurmak", "İzole olmak"],
          correct: 1
        },
        {
          question: "Başarısızlık korkusu ile nasıl başa çıkılır?",
          options: ["Hiç risk almamak", "Başarısızlığı öğrenme fırsatı görmek", "Sürekli endişelenmek", "Başkalarını taklit etmek"],
          correct: 1
        },
        {
          question: "Mental sağlığı korumak için ne önemlidir?",
          options: ["Sürekli çalışmak", "Düzenli uyku ve beslenme", "Sosyal medyada çok vakit geçirmek", "Tek başına olmak"],
          correct: 1
        },
        {
          question: "Çocuk gelişiminde en kritik dönem hangisidir?",
          options: ["Ergenlik", "İlk 3 yaş", "Okul çağı", "Yetişkinlik"],
          correct: 1
        },
        {
          question: "Öğrenme güçlüğü yaşayan birine nasıl yaklaşılmalı?",
          options: ["Eleştirmek", "Sabırlı ve destekleyici olmak", "Karşılaştırmak", "Baskı yapmak"],
          correct: 1
        },
        {
          question: "Sosyal kaygı ile başa çıkmanın yolu nedir?",
          options: ["Sosyal ortamlardan tamamen kaçınmak", "Kademeli olarak sosyal durumlarla yüzleşmek", "Sürekli endişelenmek", "Başkalarından onay beklemek"],
          correct: 1
        },
        {
          question: "Güçlü bir karakterin özelliği nedir?",
          options: ["Asla hata yapmamak", "Hatalarından öğrenmek", "Her zaman haklı olmak", "Başkalarını ezm"],
          correct: 1
        },
        {
          question: "Yaşam boyu öğrenmenin psikolojik faydası nedir?",
          options: ["Başkalarından üstün olmak", "Mental aktiviteyi sürdürme", "Gösteriş yapmak", "Zaman öldürmeı"],
          correct: 1
        },
        {
          question: "Sağlıklı sınır koymanın önemi nedir?",
          options: ["Başkalarını uzaklaştırmak", "Kendi değerlerini korumak", "Egoist görünmek", "Kontrolcü olmak"],
          correct: 1
        },
        {
          question: "Grup dinamiklerinde liderlik yapmak için ne gerekir?",
          options: ["Otoriter olmak", "Empati ve vizyon", "Agresif davranmak", "Tek karar vermek"],
          correct: 1
        },
        {
          question: "Mental esneklik ne demektir?",
          options: ["Kararsız olmak", "Değişen koşullara uyum sağlamak", "Prensipsiz olmak", "Başkalarını taklit etmek"],
          correct: 1
        }
      ]
    },
    ai: {
      title: "Yapay Zeka Temelleri Testi",
      icon: <Zap className="w-8 h-8" />,
      questions: [
        {
          question: "Yapay Zeka (AI) ne demektir?",
          options: ["Gerçek zeka", "Makine öğrenmesi", "İnsan zekasını taklit eden teknoloji", "Robot teknolojisi"],
          correct: 2
        },
        {
          question: "Makine öğrenmesi nasıl çalışır?",
          options: ["Programcı her şeyi kodlar", "Verilerden örüntüler öğrenir", "Rastgele tahmin yapar", "İnternet aramak yapar"],
          correct: 1
        },
        {
          question: "Chatbot nedir?",
          options: ["Video oyunu", "Metin tabanlı sohbet programı", "Sosyal medya uygulaması", "Müzik programı"],
          correct: 1
        },
        {
          question: "Yapay zekanın günlük hayatta kullanım alanı hangisidir?",
          options: ["Sadece fabrikalar", "Sadece üniversiteler", "Akıllı telefon, navigasyon, arama motorları", "Sadece askeri amaçlar"],
          correct: 2
        },
        {
          question: "Büyük dil modeli (LLM) ne yapar?",
          options: ["Sadece çeviri", "Dil çeviri ve metinleriyle ilgili görevler", "Sadece matematik", "Sadece resim çizme"],
          correct: 1
        },
        {
          question: "Algoritma nedir?",
          options: ["Bilgisayar markası", "Problem çözme adımları", "İnternet sitesi", "Oyun programı"],
          correct: 1
        },
        {
          question: "Veri ne için önemlidir AI'da?",
          options: ["Dekorasyon için", "Öğrenme ve gelişme için", "Yer kaplamak için", "Hiçbir önemi yok"],
          correct: 1
        },
        {
          question: "Yapay zeka etik sorunları nelerdir?",
          options: ["Hiç problem yok", "Gizlilik, önyargı, iş kaybı", "Sadece maliyet", "Sadece hız problemi"],
          correct: 1
        },
        {
          question: "Otonom araç nasıl çalışır?",
          options: ["Tamamen şans", "Sensörler ve AI ile çevre algılama", "Sadece GPS", "İnsan kontrolü"],
          correct: 1
        },
        {
          question: "Yapay zeka hangi alanda KULLANILMIYOR?",
          options: ["Tıp tanısı", "Finansal analiz", "Hava durumu tahmini", "Hepsi kullanılıyor"],
          correct: 3
        },
        {
          question: "Deepfake teknolojisi nedir?",
          options: ["Derin kazı", "Yapay video/ses üretimi", "Deniz araştırması", "Maden çıkarma"],
          correct: 1
        },
        {
          question: "AI asistanları nasıl öğrenir?",
          options: ["Hiç öğrenmez", "Etkileşimlerden ve verilerden", "Sadece programcıdan", "Tesadüfen"],
          correct: 1
        },
        {
          question: "Yapay zeka sınırlamaları nelerdir?",
          options: ["Hiç sınırı yok", "Yaratıcılık eksikliği, önyargı, veri bağımlılığı", "Sadece hız", "Sadece maliyet"],
          correct: 1
        },
        {
          question: "Neural network (sinir ağı) neyi taklit eder?",
          options: ["Kalp", "Beyin nöronları", "Karaciğer", "Akciğer"],
          correct: 1
        },
        {
          question: "AI'da 'training' (eğitim) ne demektir?",
          options: ["Spor yapmak", "Modeli verilerle öğretmek", "Oyun oynamak", "Dinlenmek"],
          correct: 1
        },
        {
          question: "Yapay zeka gelecekte hangi mesleği en çok etkileyebilir?",
          options: ["Hiç etkilemez", "Rutin veri işleme işleri", "Yaratıcı sanatlar", "Spor"],
          correct: 1
        },
        {
          question: "AI'nın tıptaki kullanımı nedir?",
          options: ["Hiç kullanımı yok", "Tanı koyma ve görüntü analizi", "Sadece fatura kesme", "Sadece temizlik"],
          correct: 1
        },
        {
          question: "Prompt nedir (AI bağlamında)?",
          options: ["Hızlı olmak", "AI'ya verilen talimat/soru", "Bilgisayar programı", "İnternet sitesi"],
          correct: 1
        },
        {
          question: "AI editasyon önyargısının sebebi nedir?",
          options: ["Tesadüf", "Eğitim verilerindeki önyargı", "Programcı hatası", "Donanım sorunu"],
          correct: 1
        },
        {
          question: "Yapay zeka şu anda en iyi olduğu alan hangisidir?",
          options: ["İnsan duygularını anlama", "Örüntü tanıma ve veri analizi", "Sezgisel düşünme", "Yaratıcı sanat"],
          correct: 1
        }
      ]
    }
  };

  const calculateScore = () => {
    const currentTestData = tests[currentTest];
    if (!currentTestData) return 0;
    
    let correctAnswers = 0;
    currentTestData.questions.forEach((question, index) => {
      if (answers[index] === question.correct) {
        correctAnswers++;
      }
    });
    
    return Math.round((correctAnswers / currentTestData.questions.length) * 100);
  };

  const handleAnswer = (questionIndex, answerIndex) => {
    setAnswers(prev => ({
      ...prev,
      [questionIndex]: answerIndex
    }));
  };

  const nextQuestion = () => {
    if (currentQuestion < tests[currentTest].questions.length - 1) {
      setCurrentQuestion(currentQuestion + 1);
    } else {
      const finalScore = calculateScore();
      setScore(finalScore);
      setTestCompleted(true);
    }
  };

  const startTest = (testId) => {
    setCurrentTest(testId);
    setCurrentPage('test');
    setCurrentQuestion(0);
    setAnswers({});
    setTestCompleted(false);
    setScore(0);
  };

  const backToHome = () => {
    setCurrentPage('home');
    setCurrentTest(null);
    setCurrentQuestion(0);
    setAnswers({});
    setTestCompleted(false);
    setScore(0);
  };

  const restartTest = () => {
    setCurrentQuestion(0);
    setAnswers({});
    setTestCompleted(false);
    setScore(0);
  };

  if (currentPage === 'home') {
    return (
      <div className="min-h-screen bg-gradient-to-br from-red-50 to-red-100">
        {/* Header */}
        <div className="bg-white shadow-lg border-b-4 border-red-600">
          <div className="max-w-6xl mx-auto px-6 py-8">
            <div className="flex items-center justify-center space-x-4">
              <div className="w-16 h-16 bg-gradient-to-br from-red-600 to-red-800 rounded-lg flex items-center justify-center shadow-lg transform perspective-1000 rotate-y-12">
                <span className="text-white font-bold text-2xl">H</span>
              </div>
              <div>
                <h1 className="text-4xl font-bold text-red-800">Harvard Test Platformu</h1>
                <p className="text-red-600 text-lg mt-2">Akademik Mükemmellik ve Değerlendirme Merkezi</p>
              </div>
            </div>
          </div>
        </div>

        {/* Hero Section */}
        <div className="max-w-6xl mx-auto px-6 py-12">
          <div className="text-center mb-12">
            <h2 className="text-3xl font-bold text-red-800 mb-4">Kapsamlı Yetenek Değerlendirme Sistemi</h2>
            <p className="text-red-700 text-lg max-w-3xl mx-auto">
              Her test 20 soru içermektedir ve başvuru yapabilmek için %50 başarı barajını geçmeniz gerekmektedir. 
              Testler farklı yetenek alanlarınızı ölçer ve gelişim fırsatlarınızı belirler.
            </p>
          </div>

          {/* Test Grid */}
          <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            {Object.entries(tests).map(([testId, test]) => (
              <div key={testId} className="bg-white rounded-xl shadow-lg hover:shadow-2xl transition-all duration-300 transform hover:-translate-y-2 border border-red-100">
                <div className="p-8">
                  <div className="flex items-center justify-center w-20 h-20 bg-gradient-to-br from-red-500 to-red-700 rounded-full mb-6 mx-auto shadow-xl">
                    <div className="text-white">
                      {test.icon}
                    </div>
                  </div>
                  
                  <h3 className="text-xl font-bold text-red-800 text-center mb-4">
                    {test.title}
                  </h3>
                  
                  <div className="space-y-3 mb-6">
                    <div className="flex items-center justify-between text-sm text-red-600">
                      <span>Soru Sayısı:</span>
                      <span className="font-semibold">20 Soru</span>
                    </div>
                    <div className="flex items-center justify-between text-sm text-red-600">
                      <span>Geçme Puanı:</span>
                      <span className="font-semibold">%50</span>
                    </div>
                    <div className="flex items-center justify-between text-sm text-red-600">
                      <span>Süre:</span>
                      <span className="font-semibold">Sınırsız</span>
                    </div>
                  </div>
                  
                  <button
                    onClick={() => startTest(testId)}
                    className="w-full bg-gradient-to-r from-red-600 to-red-800 text-white font-bold py-4 px-6 rounded-lg 
                             shadow-lg hover:shadow-xl transform hover:scale-105 transition-all duration-200 
                             border-2 border-red-700 hover:border-red-500"
                    style={{
                      boxShadow: '0 8px 15px rgba(164, 30, 34, 0.3), inset 0 2px 4px rgba(255,255,255,0.1)',
                    }}
                  >
                    Teste Başla
                  </button>
                </div>
              </div>
            ))}
          </div>

          {/* Footer Info */}
          <div className="mt-16 bg-white rounded-xl shadow-lg p-8 border border-red-100">
            <div className="text-center">
              <h3 className="text-2xl font-bold text-red-800 mb-4">Test Hakkında Önemli Bilgiler</h3>
              <div className="grid grid-cols-1 md:grid-cols-3 gap-6 text-red-700">
                <div className="flex items-center space-x-3">
                  <CheckCircle className="w-6 h-6 text-red-600" />
                  <span>Her test bağımsız olarak değerlendirilir</span>
                </div>
                <div className="flex items-center space-x-3">
                  <CheckCircle className="w-6 h-6 text-red-600" />
                  <span>Başarısız olunan testler tekrar alınabilir</span>
                </div>
                <div className="flex items-center space-x-3">
                  <CheckCircle className="w-6 h-6 text-red-600" />
                  <span>Sonuçlar anlık olarak gösterilir</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    );
  }

  if (currentPage === 'test' && currentTest) {
    const currentTestData = tests[currentTest];
    const progress = ((currentQuestion + 1) / currentTestData.questions.length) * 100;

    if (testCompleted) {
      const passed = score >= 50;
      return (
        <div className="min-h-screen bg-gradient-to-br from-red-50 to-red-100 flex items-center justify-center">
          <div className="bg-white rounded-xl shadow-2xl p-8 max-w-2xl w-full mx-4 border border-red-100">
            <div className="text-center">
              <div className={`w-24 h-24 rounded-full mx-auto mb-6 flex items-center justify-center ${
                passed ? 'bg-green-100 text-green-600' : 'bg-red-100 text-red-600'
              }`}>
                {passed ? (
                  <CheckCircle className="w-12 h-12" />
                ) : (
                  <span className="text-4xl">✗</span>
                )}
              </div>
              
              <h2 className="text-3xl font-bold text-red-800 mb-4">
                {currentTestData.title}
              </h2>
              
              <div className="text-6xl font-bold mb-4" style={{
                color: score >= 50 ? '#059669' : '#DC2626'
              }}>
                %{score}
              </div>
              
              <p className={`text-xl font-semibold mb-6 ${
                passed ? 'text-green-600' : 'text-red-600'
              }`}>
                {passed ? 'Tebrikler! Testi Başarıyla Geçtiniz!' : 'Maalesef, Barajı Geçemediniz'}
              </p>
              
              <div className="bg-gray-50 rounded-lg p-6 mb-6">
                <div className="grid grid-cols-2 gap-4 text-center">
                  <div>
                    <div className="text-2xl font-bold text-red-800">
                      {Math.round((score / 100) * 20)}/20
                    </div>
                    <div className="text-sm text-red-600">Doğru Cevap</div>
                  </div>
                  <div>
                    <div className="text-2xl font-bold text-red-800">
                      {passed ? 'BAŞARILI' : 'BAŞARISIZ'}
                    </div>
                    <div className="text-sm text-red-600">Durum</div>
                  </div>
                </div>
              </div>
              
              <div className="space-y-4">
                <button
                  onClick={restartTest}
                  className="w-full bg-gradient-to-r from-red-600 to-red-800 text-white font-bold py-3 px-6 rounded-lg 
                           shadow-lg hover:shadow-xl transform hover:scale-105 transition-all duration-200"
                >
                  Testi Tekrar Al
                </button>
                
                <button
                  onClick={backToHome}
                  className="w-full bg-gradient-to-r from-gray-500 to-gray-700 text-white font-bold py-3 px-6 rounded-lg 
                           shadow-lg hover:shadow-xl transform hover:scale-105 transition-all duration-200"
                >
                  Ana Sayfaya Dön
                </button>
              </div>
            </div>
          </div>
        </div>
      );
    }

    const currentQuestionData = currentTestData.questions[currentQuestion];

    return (
      <div className="min-h-screen bg-gradient-to-br from-red-50 to-red-100">
        {/* Header */}
        <div className="bg-white shadow-lg border-b-4 border-red-600">
          <div className="max-w-4xl mx-auto px-6 py-4">
            <div className="flex items-center justify-between">
              <div>
                <h1 className="text-2xl font-bold text-red-800">{currentTestData.title}</h1>
                <p className="text-red-600">Soru {currentQuestion + 1} / {currentTestData.questions.length}</p>
              </div>
              
              <button
                onClick={backToHome}
                className="bg-gray-500 text-white px-4 py-2 rounded-lg hover:bg-gray-600 transition-colors"
              >
                Ana Sayfa
              </button>
            </div>
            
            {/* Progress Bar */}
            <div className="mt-4">
              <div className="bg-red-200 rounded-full h-3">
                <div 
                  className="bg-gradient-to-r from-red-500 to-red-700 h-3 rounded-full transition-all duration-300"
                  style={{ width: `${progress}%` }}
                ></div>
              </div>
            </div>
          </div>
        </div>

        {/* Question */}
        <div className="max-w-4xl mx-auto px-6 py-12">
          <div className="bg-white rounded-xl shadow-lg p-8 border border-red-100">
            <h2 className="text-2xl font-bold text-red-800 mb-8 leading-relaxed">
              {currentQuestionData.question}
            </h2>
            
            <div className="space-y-4">
              {currentQuestionData.options.map((option, index) => (
                <button
                  key={index}
                  onClick={() => handleAnswer(currentQuestion, index)}
                  className={`w-full text-left p-6 rounded-lg border-2 transition-all duration-200 ${
                    answers[currentQuestion] === index
                      ? 'border-red-600 bg-red-50 shadow-lg'
                      : 'border-gray-200 hover:border-red-300 hover:bg-red-50'
                  }`}
                >
                  <div className="flex items-center space-x-4">
                    <div className={`w-8 h-8 rounded-full border-2 flex items-center justify-center ${
                      answers[currentQuestion] === index
                        ? 'border-red-600 bg-red-600 text-white'
                        : 'border-gray-300'
                    }`}>
                      {answers[currentQuestion] === index && <span className="text-sm font-bold">✓</span>}
                    </div>
                    <span className="text-lg text-gray-800">{option}</span>
                  </div>
                </button>
              ))}
            </div>
            
            <div className="mt-8 flex justify-end">
              <button
                onClick={nextQuestion}
                disabled={answers[currentQuestion] === undefined}
                className={`px-8 py-3 rounded-lg font-bold transition-all duration-200 ${
                  answers[currentQuestion] !== undefined
                    ? 'bg-gradient-to-r from-red-600 to-red-800 text-white shadow-lg hover:shadow-xl transform hover:scale-105'
                    : 'bg-gray-300 text-gray-500 cursor-not-allowed'
                }`}
              >
                {currentQuestion === currentTestData.questions.length - 1 ? 'Testi Tamamla' : 'Sonraki Soru'}
              </button>
            </div>
          </div>
        </div>
      </div>
    );
  }

  return null;
};

export default TestPlatform;
