## Sprawdź się

<head>
  <meta http-equiv="X-UA-Compatible" content="IE=edge" />
  
  <meta http-equiv="content-type" content="text/html; charset=utf-8" />
  
  <meta name="viewport" content="initial-scale=1.0" />
  
  <title>
    Zgadywanka
  </title>
  
  <!-- jquery for maximum compatibility -->
  
  <link type="text/css" rel="stylesheet" href="https://stackpath.bootstrapcdn.com/twitter-bootstrap/2.2.1/css/bootstrap-combined.min.css" />
  
  <!--<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>--> <script src="https://code.jquery.com/jquery-1.11.1.min.js" integrity="sha256-VAvG3sHdS5LqTT+5A/aeq/bZGa/Uj04xKxY8KM/w9EE=" crossorigin="anonymous"></script>
 <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js"></script>
 <script></p>

<pre><code>var nazwalamiglowki // = "Przykładowa łamigłowka";

/ **
* Tutaj wpisz informacje o swoich pytaniach. Prawidłowy ciąg odpowiedzi musi dokładnie odpowiadać
* prawidłowemu wyborowi, ponieważ sprawdza, czy ciągi pasują do siebie. (wielkość liter ma znaczenie)
*
*/
</code></pre>

<p>/**
*Utwórzmy losowe pytania!
* /</p>

<p>function shuffle(array) {
  var currentIndex = array.length, temporaryValue, randomIndex;</p>

<p>// Podczas gdy zostają elementy do przetasowania...
  while (0 !== currentIndex) {</p>

<pre><code>// Wybierz pozostały element...
randomIndex = Math.floor (Math.random () * currentIndex);
currentIndex -= 1;

// I zamień go z bieżącym elementem.
temporaryValue = array[currentIndex];
array[currentIndex] = array[randomIndex];
array[randomIndex] = temporaryValue;
</code></pre>

<p>}</p>

<p>return array;
}</p>

<p>if (!("scramble" in Array.prototype)) {
  Object.defineProperty(Array.prototype, "scramble", {
    enumerable: false,
    value: function() {
      var o, i, ln = this.length;
      while (ln--) {
        i = Math.random() * (ln + 1) | 0;
        o = this[ln];
        this[ln] = this[i];
        this[i] = o;
      }
      return this;
    }
  });
}</p>

<pre><code>var quiz = [
    {
        "pytanie": "Który skrypt sprawiłby, że duszek powiedziałby 'Hello Izzy'?",
        „zdjęcie”: „images / montage-1.png”,
        „do wyboru”: [
                                ” A ”,
                                „ B ”,
                                „ C ”,
                                „ D ”
                            ],
        „poprawne ”:„ C ”,
        „objaśnienie ”:„ Musisz dołączyć ciąg 'Hello' do zmiennej 'name' ",
    },
    {
        " pytanie ":" Który skrypt zapyta użytkownika o imię i nazwisko, a następnie wyświetli pełne imię i nazwisko? ",
        " image ":" images / montage-2.png ",
        „wybór”: [
                                „A”,
                                „B”,
                                „C”,
                                „D”
                            ],
        „poprawnych”: „D”,
        „objaśnienie”: „Najpierw należy zadać pytanie, a następnie odpowiedź zapisana jako zmienna. ”
    },
    {
        „pytanie”: „Który skrypt przeniesie duszka w lewo, gdy użytkownik wpisze„ w lewo ”, a w prawo, gdy użytkownik wpisze coś innego?”,
        „image”: „images / montage-3.png” ,
        „wybor”: [
                                „A”,
                                „B”,
                                „C”,
                                „D”
                            ],
        „poprawnych”: „A”,
        „objaśnień”: „Warunek„ if ”powinien sprawdzić, czy lewy został wpisany, a następnie przesuń w ujemnym x. W przeciwnym razie duszek powinien zawsze poruszać się w dodatnim x ",
    },

];
</code></pre>

<p>// użyj tego dla błędu składni IE w =>: skrypt ECMA 6 nie jest obsługiwany w IE 11 :(
//quiz.forEach (funkcja (q) {return q.choices.scramble ()});</p>

<p>// użyj tego dla skryptu ECMA 6
//quiz.forEach(q => q.choices.scramble ());
//console.log(quiz[0].choices);</p>

<p>quiz = shuffle(quiz);</p>

<pre><code>/ ******* Nie trzeba edytować poniżej tego wiersza ********* /
var currentquestion = 0, score = 0, submt = true, picked;

jQuery (dokument).ready (funkcja ($) {

    / **
     * Funkcja kodowania HTML znaczników alt i atrybutów, aby zapobiec pojawianiu się niechcianych
     * danych wewnątrz atrybutów znacznika.
     * /
    funkcja htmlEncode (wartość) {
      return $ (document.createElement ('div')). Text (wartość) .html ();
    }

    / **
     * Spowoduje to dodanie indywidualnych wyborów dla każdego pytania do bloku ul #
     *
     * @param {choices} tablica Wybory z każdego pytania
     * /
    funkcja addChoices (wybory) {
        if ( typeof options! == "undefined" &amp;&amp; $ .type (options) == "array") {
            $ ('# choice-block'). empty ();
            dla (var i = 0; i &lt;choices.length; i++){
            $(document.createElement('li')).addClass('choice choice-box btn').attr('data-index', i).text(choices[i]).appendTo('#choice-block');
            }
        }
    }

    /**
     * Resets all of the fields to prepare for next question
     */
    function nextQuestion(){
        submt = true;
        $('#explanation').empty();
        $('#question').text(quiz[currentquestion]['question']);
        $('#pager').text('Question ' + Number(currentquestion + 1) + ' of ' + quiz.length);
        if(quiz[currentquestion].hasOwnProperty('image') &amp;&amp; quiz[currentquestion]['image'] != ""){
            if($('#question-image').length == 0){
                $(document.createElement('img')).addClass('question-image').attr('id', 'question-image').attr('src', quiz[currentquestion]['image']).attr('alt', htmlEncode(quiz[currentquestion]['question'])).insertAfter('#question');
            } else {
                $('#question-image').attr('src', quiz[currentquestion]['image']).attr('alt', htmlEncode(quiz[currentquestion]['question']));
            }
        } else {
            $('#question-image').remove();
        }
        addChoices(quiz[currentquestion]['choices']);
        setupButtons();

        jQuery(document).ready(function($){
            $("#question").html(function(){
                var text= $(this).text().trim().split(" ");
                var first = text.shift();
                return (text.length &gt;? „&lt;span class='number'&gt;” + pierwszy + ” &lt;/span&gt; ": first) + text.join (" ");
            });

            $ ('p.pager'). each (function () {
                var text = $(this).text (). split ('');
                if (długość tekstu &lt; 2)
                    return;

                text[1] = „&lt;span class="qnumber"&gt;” + text[1]+ ” &lt;/span&gt; „;
                $(this).html (
                    text.join ('')
                );
            });

        });

    }

    / **
     * Po przesłaniu selekcji sprawdza, czy jest poprawna odpowiedź
     *
     * @param {choice} liczba Indeks liczony od zera li wybrany wybór
     * /
    funkcja proces Pytanie (wybór) {
        jeśli (quiz[currentquestion][„wybory”][choice] == quiz[currentquestion][„poprawny”]) {
            $ („. wybór”). eq (wybór) .addClass („btn-sukces”). css ({'font-weight':'bold', 'border-color':'#51a351', 'color':'#fff'});
            $ („# objaśnienie”). Html („&lt;span class="correct"&gt; PRAWIDŁOWO! &lt;/span&gt; „+ htmlEncode (quiz[currentquestion][„ wyjaśnienie ”]));
            wynik ++;
        } else {
            $ ('. Choice'). Eq (choice) .addClass ('btn-danger'). Css ({'font-weight':'bold', 'border-color':'#f93939', 'color':'#fff'});
            $ („# wyjaśnienie”). Html („&lt;span class="incorrect"&gt; NIEPRAWIDŁOWY! &lt;/span&gt; „+ htmlEncode (quiz[currentquestion][„ wyjaśnienie ”]));
        }
        currentquestion ++;

        if (currentquestion == quiz.length) {
            $ ('# submbutton'). Html ('GET QUIZ RESULTS'). RemoveClass ('btn-success'). AddClass ('btn-info'). Css ({'border-color':'#3a87ad', 'color':'#fff'}) .on ('click', function () {
                $(this).text ('GET QUIZ RESULTS'). on ('click');
                endQuiz ();
            })

        } else if (currentquestion &lt; quiz.length) {
            $ („# submbutton”). Html („NASTĘPNE PYTANIE &amp;raquo;”). RemoveClass („btn-success”). AddClass („btn-warning”). Css ({'font-weight':'bold', 'border-color':'#faa732', 'color':'#fff'}) .on („click”, function () {
                $(this).text ('- CHECK ANSWER -'). removeClass ('btn-warning'). addClass ('btn-success'). css ({'font-weight':'bold', 'border-color':'#51a351', 'color':'#fff'}) .on ('click');
                nextQuestion ( );
            })
        } else {
            // $ ('# submbutton'). Html ('NEXT QUESTION &amp;raquo;'). On ('click', function () {
            //      $(this).text ('- SPRAWDŹ ODPOWIEDŹ - ”). Css ({'color':'inherit'}) .on („ kliknij ”);
            //})
        }


    }

    / **
     * Ustawia detektory zdarzeń dla każdego przycisku.
     * /
    setup setup Przyciski () {
        $ ('. Wybór'). On ('click', function () {
            picked = $(this).attr ('data-index');
            $ ('. Choice'). removeAttr ('style'). off ('mouseout mouseover');
            $(this).css ({'font-weight':'bold', 'border-color':'#51a351', 'color':'#51a351'});
            if (submt) {
                submt = false;
                $ ('# submbutton'). css ({'color':'#fff','cursor':'pointer'}) .on ( „kliknięcie”, funkcja () {
                    $ („. wybór”). wyłączony („kliknięcie”);
                    $(this).wyłączony („kliknięcie”);
                    proces Pytanie (wybrany);
                });
            }
        })
    }

    / **
     * Quiz kończy się, wyświetl wiadomość.
     * /
    funkcja endQuiz () {
        $ ('# wyjaśnienie'). Empty ();
        $ („# pytanie”). Empty ();
        $ ('# choice-block'). Empty ();
        $ („# Submitbutton”). Remove ();
        $ ('. Rsform-block-upload'). AddClass ('show');
        $ („# pytanie”). Tekst („Masz” + wynik + „poza” + quiz. Długość + „poprawne”);
        $ (document.createElement ('h4')). AddClass ('score'). Text (Math.round (score / quiz.length * 100) + '%'). InsertAfter ('# question');         
    }

    / **
     * Uruchamia się po raz pierwszy i tworzy wszystkie elementy dla quizu
     * /
    funkcja init () {
        // dodaj tytuł
        if (typeof quiztitle! == "undefined" &amp;&amp; $. type (quiztitle) === "string") {
            $ (document.createElement ('h2')). text (quiztitle) .appendTo ('# frame');
        } // else {
            //$(document.createElement('h2')).text("Quiz").appendTo('#frame ');
</code></pre>

<p>//}</p>

<pre><code>        // dodaj pager i pytania
        if (typeof quiz! == "undefined" &amp;&amp; $ .type (quiz) === "array") {
            // dodaj pager
            $ (document.createElement ('p')) .addClass („pager”). attr („id”, „pager”). tekst („Pytanie 1 z” + długość quizu) .appendTo („# frame”);
            // dodaj pierwsze pytanie
            $ (document.createElement („h3”)). AddClass („pytanie”). Attr („id”, „pytanie”). Tekst (quiz[0][„pytanie”]). AppendTo ( '#rama');
            // dodaj obraz, jeśli jest obecny
            if (quiz[0].hasOwnProperty ('image') &amp;&amp; quiz[0]['image']! = "") {
                $ (document.createElement ('img')). AddClass (' pytanie-obraz ”). attr („ id ”,„ pytanie-obraz ”). attr („ src ”, quiz[0][„ obraz ”]). attr („ alt ”, htmlEncode (quiz[0][„ pytanie ”]) ) .appendTo ('# frame');
            }

            $ (document.createElement ('p')). AddClass ('wyjaśnienie'). Attr ('id', 'wyjaśnienie'). Html (''). AppendTo ('# frame');

            // posiadacz pytania
            $ (document.createElement ('ul')). Attr ('id', 'choice-block'). AppendTo ('# frame');

            // dodaj wybory
            addChoices (quiz[0][„options”]);

            // dodaj przycisk wysyłania
            $ (document.createElement ('div')). AddClass ('btn-success choice-box'). Attr ('id', 'submbutton'). Tekst ('- SPRAWDŹ ODPOWIEDŹ -' ) .css ({'font-weight': 'bold', 'color': '# fff', 'padding': '30px 0', 'border-radius': '10px'}). appendTo ('# frame ”);

            setupButtons ();
        }
    }

    init ();

});

jQuery (dokument) .ready (funkcja ($) {         
    $ ("# pytanie"). Html (funkcja () {
    var text = $(this).text (). Trim (). Split ("");
    var first = text.shift ();
        return (text.length &gt; 0? „&lt;span class='number'&gt;” + pierwszy + ” &lt;/span&gt; ": first) + text.join (" ");
    });

    $ ('p.pager'). each (function () {
        var text = $(this).text (). split ('');
        if (długość tekstu &lt; 2)
            return;

        text[1] = „&lt;span class="qnumber"&gt;” + text[1]+ ” &lt;/span&gt; „;
        $(this).html (
            text.join ('')
        );
    });

}); 

    funkcji copyText () {
        var output = document.getElementById ("frame"). InnerHTML;
        document.getElementById („placecontent”). Wartość = wynik;
    }

&lt;/script&gt;
&lt;style type="text/css" media="all"&gt;
    dane wejściowe {wysokość: 30 pikseli! Ważne; }
    dane wejściowe [typ = pole wyboru] {wysokość: 30 pikseli! Ważne; margin-top: -3px! ważne; margines z prawej: 5px! ważne; box-shadow: brak; kolor tła: #ffffff; pozycja: względna! ważna; }
    textarea {szerokość: 90%; margines: 0 auto; Blok wyświetlacza; }
    input [type = radio] {wysokość: 30 pikseli! Ważne; margin-top: -3px! ważne; margines z prawej: 5px! ważne; box-shadow: brak; kolor tła: #ffffff; pozycja: względna! ważna; }
    .form-group input, .form-group select {height: 30px; wypełnienie: 0px 12px; }
    .form-horizontal .form-group {margin: 10px; }
    .formContainer .formControlLabel {szerokość: auto! Ważne; min-szerokość: 150px; margines: 0; wypełnienie: 0; }
    .formControls {szerokość: 100%; wypełnienie: 0; margines: 10px 0 20px auto; }
    .radio {padding-top: 0! Ważne; padding-left: 8px! ważne; }
    .radio-inline {margin-right: 10px; padding-top: 0! ważne; display: inline; }
    .bold {font-weight: bold; }
    .italic {font-style: italic; }
    .clear {szerokość: 100%; margines: 0! ważne; }
    .rsform-block-upload {display: none; }
    .show {display: blok! Ważne; }
</code></pre>

<p>/*      .rsform-block-placecontent                              { display:none; } */
        #submit                                                 { margin:0 auto; display:block; }</p>

<pre><code>    /* QUIZ STYLES */
    ol                          { list-style:none; }
    ul#choice-block  {columns: 4; -webkit-columns: 4; -moz-columns: 4;}
    strong                                                  { font-weight:700; }
    #frame                                                  { width:auto; max-width: 800px; background:transparent; margin:3px auto; padding:10px; color:#333 !important; }
    div#frame h2                                            { width:auto; border-bottom:1px solid #bdbdbd; padding:0 0 5px 0; font-size:30px; }
    h3.question                                             { font-weight:normal; margin:20px 0; padding:0; font-style:italic; display:block; }
    p.pager                                                 { margin:5px 0 5px; color:#999; text-align:right; }
    .qnumber                                                { font-size:25px; font-weight:bold; font-style:italic; vertical-align:bottom; }
</code></pre>

<p>/*      .number                                 { font-size:25px; font-weight:bold; font-style:normal; vertical-align:inherit; padding-right:10px; } */</p>

<pre><code>    .score                  { width:100%; display:inline-block; margin:30px 0; font-size:100px; text-align:center; }
    img.question-image                                      { width:100%; height:auto; display:block; max-width:705px; margin:10px auto; border:1px solid #ccc; }
*/  #choice-block               { display:block; list-style:none; margin:0; padding:0; cursor: pointer; }
    #submitbutton               { cursor:pointer; -webkit-border-radius: 5px; -moz-border-radius: 5px; border-radius: 5px; } */
/*  #submitbutton:hover                                     { background:#7b8da6; } */
    #explanation                { width:auto; min-height:100px; margin:0 auto; padding:20px 0; text-align:center; }
    #explanation span           { font-weight:bold; padding-right:8px; }
    .choice-box                 { width:50%;  display:block;  text-align:center;  margin:5px auto !important; padding:10px 0 !important; border:1px solid #bdbdbd; }
    .correct                { color:#51a351; font-size: 20px; display: block; margin-bottom: 5px; border-bottom: 1px #51a351 solid; padding-bottom: 5px; }
    .incorrect              { color:#f93939; font-size: 20px; display: block; margin-bottom: 5px; border-bottom: 1px #f93939 solid; padding-bottom: 5px; }
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

<p><em>Ten quiz może nie działać w przeglądarce Internet Explorer. Jeśli nie widzisz quizu, spróbuj użyć innej przeglądarki.</em></p>
</script>