## Toets jouself

<head>
  <meta http-equiv="X-UA-Compatible" content="IE=edge" />
  
  <meta http-equiv="content-type" content="text/html; charset=utf-8" />
  
  <meta name="viewport" content="initial-scale=1.0" />
  
  <title>
    Vasvra
  </title>
  
  <!-- jquery for maximum compatibility -->
  
  <link type="text/css" rel="stylesheet" href="https://stackpath.bootstrapcdn.com/twitter-bootstrap/2.2.1/css/bootstrap-combined.min.css" />
  
  <!--<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>--> <script src="https://code.jquery.com/jquery-1.11.1.min.js" integrity="sha256-VAvG3sHdS5LqTT+5A/aeq/bZGa/Uj04xKxY8KM/w9EE=" crossorigin="anonymous"></script>
 <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js"></script>
 <script></p>

<pre><code>var quiztitle // = "Bobby's Voorbeeld Quiz";

/ **
* Stel die inligting oor jou vrae hier. Die korrekte antwoordstel moet ooreenstem met
* die regte keuse presies, aangesien dit toutjies aanpas. (hoofletter sensitief)
*
* /
</code></pre>

<p>/ **
* Kom ons skep die randomisering van die vrae!
* /</p>

<p>funksie shuffle (skikking) {
  var currentIndex = array.length, temporaryValue, randomIndex;</p>

<p>// Terwyl daar elemente bly om te skommel ...
  terwyl (0! == huidigeIndex) {</p>

<pre><code>// Kies 'n oorblywende element ...
randomIndex = Math.floor (Math.random () * currentIndex);
currentIndex - = 1;

/ / En ruil dit met die huidige element.
temporaryValue = skikking[currentIndex];
skikking[currentIndex] = skikking[randomIndex];
skikking[randomIndex] = tydelike waardes;
</code></pre>

<p>}</p>

<p>terugkeer skikking;
}</p>

<p>as (! ("scramble" in Array.prototype)) {
  Object.defineProperty (Array.prototype, "scramble", {
    enumerable: false,
    value: funksie () {
      var o, i, ln = this. lengte,
      terwyl (ln--) {
        i = Math.random () * (ln + 1) | 0;
        o = hierdie[ln];
        hierdie[ln] = hierdie[i];
        hierdie[i] = o;
      }
      retour dit;
    }
  });
}</p>

<pre><code>var quiz = [
    {
        "vraag"): "Watter script sal die sprite sê:" Hello Izzy? ",
        " image ":" beelde / montage-1.png ",
        " keuses ": [
                                " A ",
                                " B ",
                                " C ",
                                " D "
                            ],
        " korrek ":" C ",
        " verduideliking ":" Jy moet by die 'Hello'-string aansluit by die `name'-veranderlike ",
    ),
    {
        " vraag ":" Watter skrif sal die gebruiker vra vir hul voornaam en van en dan hul volle naam uitstuur? ",
        " image ":" images / montage-2.png "
        "keuses": [
                                "A",
                                "B",
                                "C",
                                "D"
                            ],
        "korrekte": "D",
        "verduideliking": "Die vraag moet eers gevra word, en dan die antwoord gestoor as 'n veranderlike. "
    },
    {
        "vraag": "Watter skrip sal die sprite beweeg wanneer die gebruiker 'links' tik en regs wanneer die gebruiker nog iets anders tik?",
        "prent": "beelde / montage-3.png" ,
        "keuses": [
                                "A",
                                "B",
                                "C",
                                "D"
                            ],
        "korrek": "A",
        "verduideliking" links is getik en beweeg dan in die negatiewe x. Andersins moet die sprite altyd in die positiewe x ",
    },

] beweeg;
</code></pre>

<p>// gebruik hierdie vir IE sintaksfout by =>: ECMA script 6 nie ondersteun in IE 11 :(
//quiz.forEach (funksie (q) {return q.choices.scramble ()});</p>

<p>// gebruik dit vir ECMA script 6
//quiz.forEach(q => q.choices.scramble ());
console.log (quiz[0]Choices);</p>

<p>quiz = shuffle (quiz);</p>

<pre><code>/ ******* Moet nie hierdie lyn hieronder wysig nie ********* /
var currentquestion = 0, telling = 0, submt = waar, gekies;

jQuery (dokument) .ready (funksie ($) {

    / **
     * HTML-kodering funksie vir alt-tags en eienskappe om rotse
     * -data te voorkom wat binne-in-eienskappe verskyn.
     * /
    funksie htmlEncode (waarde) {
      retour $ (document.createElement ('div')). Teks (waarde). Html ();
    }

    / **
     * Dit sal die individuele keuses te voeg vir elke vraag aan die ul # keuse-blok
     *
     * param {choices} array Die keuses van elke vraag
     * /
    funksie addChoices (keuses) {
        if ( tipe keuses! == "undefined" &amp;&amp; $ .type (keuses) == "array") {
            $ ('# keuse blok'). leeg ();
            vir (var i = 0; i&lt;choices.length; i++){
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
                return (text.length &gt; 0? "&lt;span class='number'&gt;" + eerste + "&lt;/span&gt; ": eerste) + text.join ("");
            });

            $ ( 'p.pager') elk (funksie () {.
                var text = $(this).text () verdeel ( '.');
                as (text.length &lt; 2)
                    terugkeer;

                teks[1] = '&lt;span class="qnumber"&gt;'+ teks[1]+'&lt;/span&gt;';
                $(this)html (
                    text.join (' ')
                );
            });

        });

    }

    / **
     * Nadat 'n seleksie ingedien is, kontroleer of dit die regte antwoord is
     *
     * @param {choice} nommer Die li nul-gebaseerde indeks van die keuse gekies
     * /
    funksieprosesQuestion (keuse) {
        indien (quiz[currentquestion][ 'keuses'][choice] == quiz[currentquestion][ "korrekte"]) {
            $ ( 'n keuse. ") EQ (keuse) .addClass ( 'bTN-sukses') css (..{'font-weight':'bold', 'border-color':'#51a351', 'color':'#fff'});
            $ ( '# verduideliking') html ( '.&lt;span class="correct"&gt;KORREKTE!&lt;/span&gt; "+ htmlEncode (quiz[currentquestion][ 'n verduideliking']));
            telling ++;
        } anders (
            $ ('keuse'). Eq (keuse). AddClass ('btn-gevaar'). Css ({'font-weight':'bold', 'border-color':'#f93939', 'color':'#fff'});
            $ ( '# verduideliking') html ( '.&lt;span class="incorrect"&gt;VERKEERDE!&lt;/span&gt; "+ htmlEncode (quiz[currentquestion][ 'n verduideliking']));
        }
        huidige kwessie ++;

        if (currentquestion == quiz.length) {
            $ ( '# submitbutton'). Html ( 'kry quiz resultate). RemoveClass (' BTN-sukses '). AddClass (' BTN-info '). Css ({'border-color':'#3a87ad', 'color':'#fff'}). ('Klik', funksie () (
                $(this).text ('KWALIFISEER RESULTATE') op ('kliek');
                endQuiz ();
            })

        } anders as (huidige vraag &lt; quiz.length) {
            $ ('# submitbutton'). Html ('VOLGENDE VRAAG &amp;raquo;') verwyderClass ('btn-sukses'). AddClass ('btn-waarskuwing') .css ({'font-weight':'bold', 'border-color':'#faa732', 'color':'#fff'}) .on funksie () (
                $(this).text ('- CHECK ANSWER -'). RemoveClass ('btn-waarskuwing'). addClass ('btn-sukses'). css ({'font-weight':'bold', 'border-color':'#51a351', 'color':'#fff'}) .on ('click');
                nextQuestion );
            })
        } anders {
            // $ ( '# submitbutton') html ( 'Volgende vraag. &amp;raquo; ".) op (' kliek ', funksie () {
            //      $(this).text (' - KONTROLE ANTWOORD - '). Css ({'color':'inherit'}) .on (' kliek ');
            //})
        }


    }

    / **
     * Stel die gebeurtenis luisteraars vir elke knoppie op.
     * /
    funksie setupButtons () (
        $ ('keuse'). Op ('kliek', funksie () {
            gekies = $(this).attr ('data-indeks');
            $ ('keuse'). removeAttr ( 'styl') af ( 'mouseout mouse over ");.
            $(this)Css ({'font-weight':'bold', 'border-color':'#51a351', 'color':'#51a351'});
            as (submt) {
                submt = vals,
                . $ (' # submitbutton ') css ({'color':'#fff','cursor':'pointer'}) feestelijke ( 'kliek', funksie () (
                    $ ('keuse'). af ('kliek');
                    $(this).off ('kliek');
                    kwessie (gekies);
                });
            }
        })
    }

    / **
     * Quiz eindig, vertoon 'n boodskap.
     * /
    funksie endQuiz () {
        $ ('# explanation'). Leeg ();
        $ ('# vraag'). Leeg ();
        $ ('# keuse blok'). Leeg ();
        $ ('# submitbutton'). Verwyder ();
        $ ('. Rsform-block-submit'). AddClass ('show');
        $ ('# vraag'). Teks ("U het + + telling +" uit "+ quiz.length +" korrek. ");
        $ (document.createElement ('h4')). AddClass ('score'). Teks (Math.round (telling / quiz.length * 100) + '%'). VoegAfter ('# vraag');         
    }

    / **
     * Begin die eerste keer en skep al die elemente vir die vasvra
     * /
    funksie init () {
        // voeg titel
        as (soort van kwistitel! == "ongedefinieerde" &amp;&amp; $. type (quiztitle) === "string") {
            $ (document.createElement ('h2')). teks (quiztitle) .appendTo ('# frame');
        } // else {
            //$(document.createElement('h2')).text ("Quiz").appendTo('#frame ');
</code></pre>

<p>//}</p>

<pre><code>        / / Voeg pager en vrae
        as (soort van quiz! == "undefined" &amp;&amp; $. tipe (quiz) === "array") {
            // voeg pager
            $ (document.createElement ('p')) . AddClass ('pager'). Attr ('id', 'pager'). teks ('Vraag 1 van' + quiz.length) .appendTo ('# frame');
            // Voeg eerste vraag
            $ (document.createElement ('h3')) addClass ('vraag'). Attr ('id', 'vraag'). Teks (quiz[0]['vraag']). '#frame');
            // Voeg prent by indien dit is
            indien (quiz[0].hasOwnProperty ('image') &amp;&amp; quiz[0]['image']! = "") {
                $ (document.createElement ('img')) query[0]['image']). Attr ('alt', htmlEncode (quiz[0]['vraag']) ) .appendTo ( '# raam);
            }

            $ (document.createElement ('p')) addClass ('verduideliking'). Attr ('id', 'verduideliking'). Html (''). AppendTo ('# frame');

            // vrae houer
            $ (document.createElement ('ul')). Attr ('id', 'keuse-blok'). AppendTo ('# frame');

            // voeg keuses by
            Kodes (vasvra[0]['keuses']);

            / add submit knoppie
            $ (document.createElement ('div')). AddClass ('btn-sukses keuse-boks'). Attr ('id', 'submitbutton'). ). css ('' font-weight ':' bold ',' color ':' # fff ',' padding ':' 30px 0 ',' border-radius ':' 10px '}). ');

            setupButtons ();
        }
    }

    init ();

});

jQuery (dokument) .ready (funksie ($) {         
    . $ ( "# Vraag") html (funksie () {
    var text = $(this). .Text () knip () verdeel ( "");.
    var eerste = text.shift ();
        retour (text.length &gt; 0? "&lt;span class='number'&gt;" + eerste + "&lt;/span&gt; ": eerste) + text.join ("");
    });

    $ ( 'p.pager') elk (funksie () {.
        var text = $(this).text () verdeel ( '.');
        as (text.length &lt; 2)
            terugkeer;

        teks[1] = '&lt;span class="qnumber"&gt;'+ teks[1]+'&lt;/span&gt;';
        $(this)html (
            text.join (' ')
        );
    });

}); 

    funksie copyText () {
        var output = document.getElementById ("raam"). InnerHTML;
        document.getElementById ("place content"). Waarde = uitvoer;
    }

&lt;/script&gt;
&lt;style type="text/css" media="all"&gt;
    invoer {hoogte: 30px! Belangrik; }
    insette [tipe = boks] {hoogte: 30px! Belangrik; marge-top: -3px! belangrik; marge-regs: 5px! belangrik; box-skaduwee: geen; agtergrond-kleur: # ffffff; posisie: relatief belangrik; }
    textarea {width: 90%; marge: 0 motor; vertoon: blok; }
    insette [tipe = radio] {hoogte: 30px! Belangrik; marge-top: -3px! belangrik; marge-regs: 5px! belangrik; box-skaduwee: geen; agtergrond-kleur: # ffffff; posisie: relatief belangrik; }
    .form-groep invoer, .form-groep kies {hoogte: 30px; opvulling: 0px 12px; }
    Vorm-horisontale .form-groep {marge: 10px; }
    FormContainer. FormControlLabel {width: auto! Important; min-width: 150px; marge: 0; padding: 0; }
    FormControls {width: 100%; padding: 0; marge: 10px 0 20px motor; }
    .radio {padding-top: 0 belangrik; padding-links: 8px! belangrik; }
    .radio-inline {margin-reg: 10px; padding-top: 0! belangrik; vertoon: inline; }
    Bold {font-weight: bold; }
    .italic {font-style: italic; }
    Duidelike {breedte: 100%; marge: 0! belangrik; }
    .rsform-blok-submit {display: none; }
    .show {vertoon: blok belangrik; }
</code></pre>

<p>/ * .rsform-block-placecontent {vertoon: geen; } * /
        #submit {marge: 0 auto; vertoon: blok; }</p>

<pre><code>    / * QUIZ STYLES * /
    ol (lys-styl: geen; }
    ul # keuse-blok {kolomme: 4; -webkit-kolomme: 4; -moz-kolomme: 4;}
    sterk (font-gewig: 700; }
    frame {width: auto; maksimum breedte: 800px; agtergrond: deursigtige; marge: 3px motor; padding: 10px; kleur: # 333! belangrik; }
    div # raam h2 {breedte: outomaties; randbodem: 1px soliede #bdbdbd; vulling: 0 0 5px 0; font-size: 30px; }
    h3.question {font-weight: normal; marge: 20px 0; padding: 0; font-style: italic; vertoon: blok; }
    p.pager (marge: 5px 0 5px; kleur: # 999; text-align: reg; }
    Qnumber (font-size: 25px; font-weight: bold; font-style: italic; vertikale-align: bodem; }
</code></pre>

<p>/ *. Number (font-size: 25px; font-weight: bold; font-style: normal; vertikale-align: beërwe; padding-reg: 10px; ) * /</p>

<pre><code>    . Score {width: 100%; vertoon: inline-blok; marge: 30px 0; font-size: 100px; text-align: center; }
    img.question-image {width: 100%; hoogte: motor; vertoon: blok; Max-width: 705px; marge: 10px outomaties; grens: 1px solid #ccc; }
* / # keuse-blok {vertoon: blok; lys-styl: geen; marge: 0; padding: 0; wyser: wyser; }
    #submitbutton {wyser: wyser; -webkit-grens-radius: 5px; -moz-grens-radius: 5px; grens radius: 5px; } * /
/ * #submitbutton: hover (agtergrond: # 7b8da6; } * /
    #explanation {width: auto; min-hoogte: 100px; marge: 0 motor; opvulling: 20px 0; text-align: center; }
    #explanation span {font-weight: bold; padding-reg: 8px; }
    Keuse-boks {breedte: 50%; vertoon: blok; text-align: center; marge: 5px outomaties! belangrik; vulling: 10px 0! belangrik; grens: 1px solide #bdbdbd; }
    Korrek {kleur: # 51a351; lettergrootte: 20px; vertoon: blok; marge-onderkant: 5px; grensbodem: 1px # 51a351 soliede; Padding-bodem: 5px; }
    Onjuist (kleur: # f93939; lettergrootte: 20px; vertoon: blok; marge-onderkant: 5px; grens-bodem: 1px # f93939 soliede; Padding-bodem: 5px; }
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

<p><em>Hierdie vasvra mag nie in Internet Explorer werk nie. As jy nie die vasvra kan sien nie, probeer asseblief om 'n ander blaaier te gebruik.</em></p>
</script>