## Kendinizi test edin

<head>
  <meta http-equiv="X-UA-Compatible" content="IE=edge" />
  
  <meta http-equiv="content-type" content="text/html; charset=utf-8" />
  
  <meta name="viewport" content="initial-scale=1.0" />
  
  <title>
    Kısa sınav
  </title>
  
  <!-- jquery for maximum compatibility -->
  
  <link type="text/css" rel="stylesheet" href="https://stackpath.bootstrapcdn.com/twitter-bootstrap/2.2.1/css/bootstrap-combined.min.css" />
  
  <!--<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>--> <script src="https://code.jquery.com/jquery-1.11.1.min.js" integrity="sha256-VAvG3sHdS5LqTT+5A/aeq/bZGa/Uj04xKxY8KM/w9EE=" crossorigin="anonymous"></script>
 <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js"></script>
 <script></p>

<pre><code>var quiztitle // = "Bobby'nin Örnek Sınavı";

/ **
* Sorularınızla ilgili bilgileri burada ayarlayın. Doğru cevap dizgisinin, dize eşlemesinde olduğu gibi, tam olarak
* doğru seçimi eşleştirmesi gerekir. (büyük / küçük harfe duyarlı)
*
* /
</code></pre>

<p>/ **
* Soruların rastgeleleşmesini yaratalım!
* /</p>

<p>işlev karışık (dizi) {
  var currentIndex = array.length, temporaryValue, randomIndex;</p>

<p>// Karıştırılacak öğeler kalırken...
  while (0! == currentIndex) {</p>

<pre><code>// Kalan bir eleman seçin...
randomIndex = Math.floor (Math.random () * currentIndex);
currentIndex - = 1;

// Ve onu geçerli elemanla değiştir.
temporaryValue = dizi[currentIndex];
dizi[currentIndex] = dizi[randomIndex];
dizi[randomIndex] = temporaryValue;
</code></pre>

<p>}</p>

<p>dönüş dizisi;
}</p>

<p>if (! (Array.prototype içindeki "scramble")) {
  Object.defineProperty (Array.prototype, "scramble", {
    numaralandırılabilir: false,
    value: function () {
      var o, i, ln = this. uzunluk;
      iken (ln--) {
        i = Math.random () * (ln + 1) | 0;
        o = bu[ln];
        bu[ln] = bu[i];
        bu[i] = o;
      }
      dönüş bu;
    }
  });
}</p>

<pre><code>var quiz = [
    {
        "question": "Hangi komut dosyası sprite 'Hello Izzy' demesine neden olur?",
        "image": "images / montage-1.png",
        "choices": [
                                " A ",
                                " B ",
                                " C ",
                                " D "
                            ],
        " doğru ":" C ",
        " açıklama ":" 'Merhaba' dizgesini `name` değişkenine eklemelisiniz ",
    },
    {
        " soru ":" Hangi komut dosyası, kullanıcının adını ve soyadını sorar ve sonra tam adını yazar? ",
        " image ":" images / montage-2.png ",
        "seçimler": [
                                "A",
                                "B",
                                "C",
                                "D"
                            ],
        "doğru": "D",
        "açıklama": "Önce soru sorulmalı, ve sonra değişken olarak saklanan cevap. "
    },
    {
        "question": "Kullanıcı 'sol' yazdığında sprite sola, kullanıcı başka bir şey yazdığında sağa ne kadar hareket eder?",
        "image": "images / montage-3.png" ,
        "seçimler": [
                                "A",
                                "B",
                                "C",
                                "D"
                            ],
        "doğru": "A",
        "açıklama": "Durumun doğru olup olmadığını kontrol etmeli Sola yazıldı ve sonra negatif x içinde hareket ettirin. Aksi halde sprite daima "x",
    },

] pozitifinde hareket etmelidir;
</code></pre>

<p>// bunu IE sözdizimi hatası için => olarak kullan: ECMA komut dosyası 6, IE 11'de desteklenmiyor:
//quiz.forEach (function (q) {return q.choices.scramble ()});</p>

<p>//use this for ECMA script 6
//quiz.forEach(q => q.choices.scramble());
//console.log(quiz[0].choices);</p>

<p>sınav = shuffle (sınav);</p>

<pre><code>/ ******* Bu satırın altında düzenleme yapmanıza gerek yok ********* /
var currentquestion = 0, score = 0, submt = true, picked;

jQuery (document).ready (function ($) {

    / **
     * Etiket özniteliklerinde karışık
     * verilerin görünmesini önlemek için alt etiketleri ve öznitelikleri için HTML Kodlama işlevi.
     * /
    işlevi htmlEncode (value) {
      return $ (document.createElement ('div')). Text (value) .html ();
    }

    / **
     * Bu ul # seçimi bloğuna her soru için ayrı ayrı seçimler katacak
     *
     * @param {choices} dizisi, her bir soru ile ilgili seçenekler
     * /
    işlev addChoices (seçenek) {
        (eğer typeof choices! == "undefined" &amp;&amp; $ .type (choices) == "dizi") {
            $ ('# choice-block'). empty ();
            için (var i = 0? "&lt;span class='number'&gt;" + ilk + " &lt;/span&gt; ": ilk) + text.join (" ");
            });

            $ ('p.pager'). her (işlev () {
                var text = $(this).text (). split ('');
                if (text.length &lt; 2)
                    return;

                metin[1] = '&lt;span class="qnumber"&gt;' + metin[1]+ ' &lt;/span&gt; ';
                $(this)Html (
                    text.join ('')
                );
            });

        });

    }

    / **
     * Bir seçim yapıldıktan sonra, doğru cevabın olup olmadığını kontrol eder
     *
     * @ param {choice} sayı Seçimin li sıfır bazlı indeksi seçildi
     * /
    fonksiyon processQuestion (seçenek) {
        ise (sınav[currentquestion]['seçimler'][choice] == sınav[currentquestion]['doğru']) {
            $ ('. seçim'). eq (seçim) .addClass ('btn-success'). css ({'font-weight':'bold', 'border-color':'#51a351', 'color':'#fff'});
            $ ('# açıklama'). Html ('&lt;span class="correct"&gt; DOĞRU! &lt;/span&gt; '+ htmlEncode (bilgi yarışması[currentquestion][' açıklama ']));
            puan ++;
        } else {
            $ ('seçim'). Eq (seçim) .addClass ('btn-tehlike'). Css ({'font-weight':'bold', 'border-color':'#f93939', 'color':'#fff'});
            $ ('# açıklama'). Html ('&lt;span class="incorrect"&gt; YANLIŞ! &lt;/span&gt; '+ htmlEncode (bilgi yarışması[currentquestion][' açıklama ']));
        }
        akım sorgulaması ++;

        if (currentquestion == quiz.length) {
            $ ( '# submitbutton'). Html ( 'QUİZ SONUCU ELDE'). RemoveClass ( 'btn-başarı'). AddClass ( 'btn-info'). Css ({'border-color':'#3a87ad', 'color':'#fff'}) .on ('click', function () {
                $(this).text ('QUIZ SONUÇLARINI ALIN'). on ('click');
                endQuiz ();
            })

        } else eğer (currentquestion &lt; quiz.length) {
            $ ('# requestbutton'). Html ('SONRAKİ SORU &amp;raquo;'). RemoveClass ('btn-success'). AddClass ('btn-warning'). Css ({'font-weight':'bold', 'border-color':'#faa732', 'color':'#fff'}) .on ('klike', function () {
                $(this).text ('- CEVAP KONTROLÜ -'). removeClass ('btn-warning'). addClass ('btn-success'). css ({'font-weight':'bold', 'border-color':'#51a351', 'color':'#fff'}) .on ('click');
                nextQuestion ( );
            })
        } else {
            // $ ('# requestbutton'). Html ('SONRAKİ SORU &amp;raquo;'). On ('click', function () {
            //      $(this).text ('- CEVAP KONTROLÜ - ') css ({'color':'inherit'}) .on (' klik ');
            //})
        }


    }

    / **
     * Her düğme için olay dinleyicilerini ayarlar.
     * /
    function setupButtons () {
        $ ('. Choice'). On ('click', function () {
            seçildi = $(this).attr ('data-index');
            $ ('. Choice'). removeAttr ('style'). off ('musus mouseover');
            $(this).css ({'font-weight':'bold', 'border-color':'#51a351', 'color':'#51a351'});
            eğer (submt) {
                submt = false;
                $ ('# yerde)'. css ({'color':'#fff','cursor':'pointer'}) .on ( 'click', function () {
                    $ ('. choice'). off ('click');
                    $(this).off ('click');
                    processQuestion (seçildi);
                });
            }
        })
    }

    / **
     * Sınav sona erer, bir mesaj görüntüler.
     * /
    işlevi endQuiz () {
        $ ('# açıklama'). Empty ();
        $ ('# soru'). Empty ();
        $ ('# choice-block'). Empty ();
        $ ('# isteği gönder)' remove. ();
        $ ('. Rsform-blok-Gönder'). AddClass ('show');
        $ ('# question') metin ("+" dışında "+ puan +" aldın + quiz.length + "doğru.");
        $ (document.createElement ('h4')). AddClass ('score'). Text (Math.round (score / quiz.length * 100) + '%'). İnsertAfter ('# question');         
    }

    / **
     * İlk kez çalıştırır ve
     * /
    testinin tüm elemanlarını yaratır. İnit () {
        // eğer varsa başlık
        eklenir (typeof quiztitle! == "undefined" &amp;&amp; $. type (quiztitle) === "string") {
            $ (document.createElement ('h2')). text (quiztitle) .appendTo ('# frame');
        } // else {
            //$(document.createElement('h2')).text("Quiz").appendTo('#frame ');
</code></pre>

<p>//}</p>

<pre><code>        // çağrı cihazı ve soru
        eklenirse (typeof quiz! == "undefined" &amp;&amp; $ .type (quiz) === "array") {
            // çağrı cihazı
            $ ekleyin (document.createElement ('p')) .addClass ('pager'). attr ('id', 'pager'). text ('+ 1' quiz.length 'in 1. sorusu) .appendTo (' # frame ');
            // ilk soruyu ekleyiniz
            $ (document.createElement ('h3')). AddClass ('question'). Attr ('id', 'question'). Text (test[0]['question']). AppendTo ( '#frame');
            // varsa resim ekle
            eğer (quiz[0].hasOwnProperty ('image') &amp;&amp; quiz[0]['image']! = "") {
                $ (document.createElement ('img')). AddClass (' soru-görüntü '). attr (' id ',' soru-görüntü '). attr (' src ', sınav[0][' image ']). attr (' alt ', htmlEncode (sınav[0][' soru ']) ) .appendTo ( '# çerçeve');
            }

            $ (document.createElement ('p')). AddClass ('açıklama'). Attr ('id', 'açıklama'). Html (''). AppendTo ('# frame');

            // soru sahibi
            $ (document.createElement ('ul')). Attr ('id', 'choice-block'). AppendTo ('# frame');

            // seçenek ekle
            addChoices (quiz[0]['choices']);

            // gönder butonu ekle
            $ (document.createElement ('div'))) addClass ('btn-başarı seçim kutusu'). Attr ('id', 'gönder' düğmesi)) text ('- CHECK CEVAP -' ) .css ({'font-ağırlık': 'kalın', 'renk': '# fff', 'dolgu': '30px 0', 'kenarlık yarıçapı': '10px'}). appendTo ('# frame ');

            kurulumButtons ();
        }
    }

    init ();

});

jQuery (document) .ready (function ($) {         
    $ ("# question"). Html (function () {
    var text = $(this).text (). Trim (). Split ("");
    var first = text.shift ();
        return (text.length &gt; 0? "&lt;span class='number'&gt;" + ilk + " &lt;/span&gt; ": ilk) + text.join (" ");
    });

    $ ('p.pager'). her (işlev () {
        var text = $(this).text (). split ('');
        if (text.length &lt; 2)
            return;

        metin[1] = '&lt;span class="qnumber"&gt;' + metin[1]+ ' &lt;/span&gt; ';
        $(this)Html (
            text.join ('')
        );
    });

}); 

    işlevi copyText () {
        var output = document.getElementById ("frame").
        document.getElementById ("placecontent"). Value = çıktı;
    }

&lt;/script&gt;
&lt;style type="text/css" media="all"&gt;
    giriş {yükseklik: 30 piksel! Önemli; }
    giriş [tür = onay kutusu] {yükseklik: 30 piksel! Önemli; marj-top: -3px! önemli; kenar boşluğu: 5px! önemli; kutu gölge: none; Arka plan renkli: #ffffff; pozisyon: göreceli! önemli; }
    textarea {genişlik:% 90; marj: 0 otomatik; Ekran bloğu; }
    giriş [tür = radyo] {yükseklik: 30 piksel! Önemli; marj-top: -3px! önemli; kenar boşluğu: 5px! önemli; kutu gölge: none; Arka plan renkli: #ffffff; pozisyon: göreceli! önemli; }
    .form grubu girişi, .form grubu seçimi {height: 30px; dolgu maddesi: 0px 12px; }
    .form-yatay .form-grup {marj: 10 piksel; }
    .formContainer .formControlLabel {width: auto! İmportant; dakika-genişliği: 150px; marjı: 0; dolgu: 0; }
    .formControls {width: 100%; dolgu: 0; marj: 10 piksel 0 20 piksel otomatik; }
    .radio {padding-top: 0! Önemli; sol-sol: 8px! önemli; }
    .radio-satır içi {marj-sağ: 
 piksel; dolgu malzemesi: 0! önemli; görüntü: içi; }
    .bold {font-ağırlık: kalın; }
    .italic {font-style: italic; }
    Temiz {genişlik:% 100; marj: 0! önemli; }
    .rsform-block -ule {görüntüleme: yok; }
    .show {görüntüleme: blok! Önemli; }
</code></pre>

<p>/ * .rsform-block-placecontent {ekran: yok; } * /
        #submit {margin: 0 otomatik; Ekran bloğu; }</p>

<pre><code>    / * QUIZ STYLES * /
    ol {list-style: none; }
    ul # choice-block {sütunlar: 4; -webkit-sütunları: 4; -moz-sütunlar: 4;}
    güçlü {font-ağırlık: 700; }
    #frame {width: auto; maksimum genişlik: 800px; Arka plan: transparent; marj: 3 piksel otomatik; dolgu: 10px; renk: # 333 önemli; }
    div # kare h2 {width: auto; sınır-alt: 1px katı #bdbdbd; dolgu maddesi: 0 0 5 piksel 0; yazı tipi boyutu: 30px; }
    h3.question {font-weight: normal; marj: 20 piksel 0; dolgu: 0; font-style: italic; Ekran bloğu; }
    p.pager {marj: 
 piksel 0 
 piksel; color: # 999; text-align: right; }
    .qnumber {font-size: 25px; yazı-ağırlık: koyu; font-style: italic; dikey hizalama: alt; }
</code></pre>

<p>/ * .number {font-size: 25px; yazı-ağırlık: koyu; font-style: normal; dikey hizalama: miras; padding-right: 10px; } * /</p>

<pre><code>    Skor {genişlik:% 100; Ekran: sıralı blok; marj: 30 piksel 0; yazı tipi boyutu: 100 piksel; text-align: center; }
    img.question-image {width: 100%; yüksekliği: otomatik; Ekran bloğu; maksimum genişlik: 705px; marj: 10 piksel otomatik; sınır: 1px katı #ccc; }
* / # choice-block {görüntüleme: blok; list-style: none; marjı: 0; dolgu: 0; imleç: işaretçi; }
    #submitbutton {imleç: pointer; -webkit-border-radius: 5px; -moz-sınır yarıçapı: 5px; sınır yarıçapı: 5 piksel; } * /
/ * #submitbutton: hover {background: # 7b8da6; } * /
    # açıklama {width: auto; dakika-yüksekliği: 100 piksel; marj: 0 otomatik; dolgu maddesi: 20px 0; text-align: center; }
    # açıklama süresi {font-weight: bold; padding-right: 8px; }
    seçim kutusu {genişlik:% 50; Ekran bloğu; text-align: center; marj: 5 piksel otomatik! önemli; dolgu maddesi: 10px 0! önemli; sınır: 1px katı #bdbdbd; }
    Doğru {renk: # 51a351; yazı tipi boyutu: 20 piksel; Ekran bloğu; marj-alt: 5 piksel; sınır-alt: 1px # 51a351 katı; alt dolgu: 5px; }
    yanlış {renk: # f93939; yazı tipi boyutu: 20 piksel; Ekran bloğu; marj-alt: 5 piksel; sınır-alt: 1px # f93939 katı; alt dolgu: 5px;
&lt;/style&gt;
</code></pre>

<p></head>
<body></p>

<div class="form-group rsform-block rsform-block-framecontent">
    <div id="frame" role="content"></div>
</div>

<hr>

<!--<div class="form-group rsform-block rsform-block-placecontent">
    <label class="col-sm-3 control-label formControlLabel" data-toggle="tooltip" title="" for="placecontent"></label>
    <div class="col-sm-6 formControls">
        <textarea cols="50" rows="5" name="form[placecontent]" id="placecontent" readonly="" class="rsform-text-box form-control rsform-text-box"></textarea>           
    </div>
</div>  -->

<p><!--<div class="col-sm-6 formControls rsform-block-submit">
    <button type="submit" name="form[submit]" id="submit" onclick="copyText()" class="rsform-submit-button  btn btn-primary">Submit Quiz</button>           
</div> -->
</body>
</html></p>

<p><em>Bu sınav Internet Explorer’da çalışmayabilir. Sınavı göremiyorsanız, lütfen başka bir tarayıcı kullanmayı deneyin.</em></p>
</script>