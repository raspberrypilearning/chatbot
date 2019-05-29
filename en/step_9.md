## Test yourself

<html>
<head>
	<meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta http-equiv="content-type" content="text/html; charset=utf-8">
	<meta name="viewport" content="initial-scale=1.0">
    <title>Quiz</title>
    <!-- jquery for maximum compatibility -->
	<link type="text/css" rel="stylesheet" href="https://stackpath.bootstrapcdn.com/twitter-bootstrap/2.2.1/css/bootstrap-combined.min.css">
    <!--<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>-->
	<script src="https://code.jquery.com/jquery-1.11.1.min.js" integrity="sha256-VAvG3sHdS5LqTT+5A/aeq/bZGa/Uj04xKxY8KM/w9EE=" crossorigin="anonymous"></script>
	<script src="https://stackpath.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js"></script>
    <script>

    var quiztitle// = "Bobby's Sample Quiz";

    /**
    * Set the information about your questions here. The correct answer string needs to match
    * the correct choice exactly, as it does string matching. (case sensitive)
    *
    */

/**
*Let's create the randomization of the questions!
*/

function shuffle(array) {
  var currentIndex = array.length, temporaryValue, randomIndex;

  // While there remain elements to shuffle...
  while (0 !== currentIndex) {

    // Pick a remaining element...
    randomIndex = Math.floor(Math.random() * currentIndex);
    currentIndex -= 1;

    // And swap it with the current element.
    temporaryValue = array[currentIndex];
    array[currentIndex] = array[randomIndex];
    array[randomIndex] = temporaryValue;
  }

  return array;
}
	    
if (!("scramble" in Array.prototype)) {
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
}		
	    
    var quiz = [
        {
            "question"      :   "Which script would cause the sprite to say 'Hello Izzy'?",
            "image"         :   "images/montage-1.png",
            "choices"       :   [
                                    "A",
                                    "B",
                                    "C",
                                    "D"
                                ],
            "correct"       :   "C",
            "explanation"   :   "You need to join the 'Hello ' string to the `name` variable",
        },
        {
            "question"      :   "Which script would ask the user for their first name and last name and then output their full name?",
            "image"         :   "images/montage-2.png",
            "choices"       :   [
                                    "A",
                                    "B",
                                    "C",
                                    "D"
                                ],
            "correct"       :   "D",
            "explanation"   :   "The question must be asked first, and then the answer stored as a variable."
        },
        {
            "question"      :   "Which script will move the sprite left when the user types 'left' and right when the user types anything else?",
            "image"         :   "images/montage-3.png",
            "choices"       :   [
                                    "A",
                                    "B",
                                    "C",
                                    "D"
                                ],
            "correct"       :   "A",
            "explanation"   :   "The if condition should check if left has been typed and then move in the negative x. Otherwise the sprite should always move in the positive x",
        },

    ];

//use this for IE syntax error at => : ECMA script 6 not supported in IE 11 :(
//quiz.forEach(function(q){ return q.choices.scramble()});

//use this for ECMA script 6
//quiz.forEach(q => q.choices.scramble());
//console.log(quiz[0].choices);
		
quiz = shuffle(quiz);
	    
    /******* No need to edit below this line *********/
    var currentquestion = 0, score = 0, submt=true, picked;

    jQuery(document).ready(function($){

        /**
         * HTML Encoding function for alt tags and attributes to prevent messy
         * data appearing inside tag attributes.
         */
        function htmlEncode(value){
          return $(document.createElement('div')).text(value).html();
        }

        /**
         * This will add the individual choices for each question to the ul#choice-block
         *
         * @param {choices} array The choices from each question
         */
		function addChoices(choices){
			if(typeof choices !== "undefined" && $.type(choices) == "array"){
				$('#choice-block').empty();
				for(var i=0;i<choices.length; i++){
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
			if(quiz[currentquestion].hasOwnProperty('image') && quiz[currentquestion]['image'] != ""){
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
					return (text.length > 0 ? "<span class='number'>"+ first +"</span> " : first) + text.join(" ");
				});
				
				$('p.pager').each(function(){
					var text = $(this).text().split(' ');
					if(text.length < 2)
						return;
					
					text[1] = '<span class="qnumber">'+text[1]+'</span>';
					$(this).html(
						text.join(' ')
					);
				});
				
			});
			
        }

        /**
         * After a selection is submitted, checks if its the right answer
         *
         * @param {choice} number The li zero-based index of the choice picked
         */
        function processQuestion(choice){
            if(quiz[currentquestion]['choices'][choice] == quiz[currentquestion]['correct']){
				$('.choice').eq(choice).addClass('btn-success').css({'font-weight':'bold', 'border-color':'#51a351', 'color':'#fff'});
				$('#explanation').html('<span class="correct">CORRECT!</span> ' + htmlEncode(quiz[currentquestion]['explanation']));
				score++;
			} else {
                $('.choice').eq(choice).addClass('btn-danger').css({'font-weight':'bold', 'border-color':'#f93939', 'color':'#fff'});
                $('#explanation').html('<span class="incorrect">INCORRECT!</span> ' + htmlEncode(quiz[currentquestion]['explanation']));
            }
            currentquestion++;

			if(currentquestion == quiz.length){
				$('#submitbutton').html('GET QUIZ RESULTS').removeClass('btn-success').addClass('btn-info').css({'border-color':'#3a87ad', 'color':'#fff'}).on('click', function(){
					$(this).text('GET QUIZ RESULTS').on('click');
					endQuiz();
				})
				
			} else if (currentquestion < quiz.length){
				$('#submitbutton').html('NEXT QUESTION &raquo;').removeClass('btn-success').addClass('btn-warning').css({'font-weight':'bold', 'border-color':'#faa732', 'color':'#fff'}).on('click', function(){
					$(this).text('- CHECK ANSWER -').removeClass('btn-warning').addClass('btn-success').css({'font-weight':'bold', 'border-color':'#51a351', 'color':'#fff'}).on('click');
					nextQuestion();
				})
			} else {
				//	$('#submitbutton').html('NEXT QUESTION &raquo;').on('click', function(){
				//		$(this).text('- CHECK ANSWER -').css({'color':'inherit'}).on('click');
				//	})
			}

			
		}

        /**
         * Sets up the event listeners for each button.
         */
		function setupButtons(){
			$('.choice').on('click', function(){
				picked = $(this).attr('data-index');
				$('.choice').removeAttr('style').off('mouseout mouseover');
				$(this).css({'font-weight':'bold', 'border-color':'#51a351', 'color':'#51a351'});
				if(submt){
					submt=false;
					$('#submitbutton').css({'color':'#fff','cursor':'pointer'}).on('click', function(){
						$('.choice').off('click');
						$(this).off('click');
						processQuestion(picked);
					});
				}
			})
		}
        
        /**
         * Quiz ends, display a message.
         */
		function endQuiz(){
			$('#explanation').empty();
			$('#question').empty();
			$('#choice-block').empty();
			$('#submitbutton').remove();
			$('.rsform-block-submit').addClass('show');
			$('#question').text("You got " + score + " out of " + quiz.length + " correct.");
			$(document.createElement('h4')).addClass('score').text(Math.round(score/quiz.length * 100) + '%').insertAfter('#question');			
		}

        /**
         * Runs the first time and creates all of the elements for the quiz
         */
		function init(){
			//add title
			if(typeof quiztitle !== "undefined" && $.type(quiztitle) === "string"){
				$(document.createElement('h2')).text(quiztitle).appendTo('#frame');
			} //else {
				//$(document.createElement('h2')).text("Quiz").appendTo('#frame');
//			}
			
			//add pager and questions
			if(typeof quiz !== "undefined" && $.type(quiz) === "array"){
				//add pager
				$(document.createElement('p')).addClass('pager').attr('id','pager').text('Question 1 of ' + quiz.length).appendTo('#frame');
				//add first question
				$(document.createElement('h3')).addClass('question').attr('id', 'question').text(quiz[0]['question']).appendTo('#frame');
				//add image if present
				if(quiz[0].hasOwnProperty('image') && quiz[0]['image'] != ""){
					$(document.createElement('img')).addClass('question-image').attr('id', 'question-image').attr('src', quiz[0]['image']).attr('alt', htmlEncode(quiz[0]['question'])).appendTo('#frame');
				}
				
				$(document.createElement('p')).addClass('explanation').attr('id','explanation').html('').appendTo('#frame');
				
				//questions holder
				$(document.createElement('ul')).attr('id', 'choice-block').appendTo('#frame');
				
				//add choices
				addChoices(quiz[0]['choices']);
				
				//add submit button
				$(document.createElement('div')).addClass('btn-success choice-box').attr('id', 'submitbutton').text('- CHECK ANSWER -').css({'font-weight':'bold', 'color':'#fff','padding':'30px 0', 'border-radius':'10px'}).appendTo('#frame');
				
				setupButtons();
			}
		}
	
		init();
	
	});
		
	jQuery(document).ready(function($){			
		$("#question").html(function(){
		var text= $(this).text().trim().split(" ");
		var first = text.shift();
			return (text.length > 0 ? "<span class='number'>"+ first +"</span> " : first) + text.join(" ");
		});
		
		$('p.pager').each(function(){
			var text = $(this).text().split(' ');
			if(text.length < 2)
				return;
			
			text[1] = '<span class="qnumber">'+text[1]+'</span>';
			$(this).html(
				text.join(' ')
			);
		});

	});	

		function copyText() {
			var output = document.getElementById("frame").innerHTML;
			document.getElementById("placecontent").value = output;
		}
	    
    </script>
    <style type="text/css" media="all">
		input 													{ height:30px !important; }
		input[type=checkbox]									{ height:30px !important; margin-top:-3px !important; margin-right:5px !important; box-shadow:none; background-color:#ffffff; position:relative !important; }
		textarea												{ width: 90%; margin: 0 auto; display: block; }
		input[type=radio]										{ height:30px !important; margin-top:-3px !important; margin-right:5px !important; box-shadow:none; background-color:#ffffff; position:relative !important; }
		.form-group input, .form-group select 					{ height:30px; padding: 0px 12px; }
		.form-horizontal .form-group							{ margin:10px; }
		.formContainer .formControlLabel 						{ width:auto !important; min-width:150px; margin:0; padding:0; }
		.formControls											{ width:100%; padding:0; margin: 10px 0 20px auto; }
		.radio 													{ padding-top:0 !important; padding-left:8px !important; }
		.radio-inline											{ margin-right:10px; padding-top:0 !important; display:inline; }
		.bold													{ font-weight:bold; }
		.italic 												{ font-style:italic; }
		.clear					 								{ width:100%; margin:0 !important; }
		.rsform-block-submit 									{ display:none; }
		.show 													{ display: block !important; }
/*		.rsform-block-placecontent 								{ display:none; } */
		#submit													{ margin:0 auto; display:block; }

		/* QUIZ STYLES */
		ol							{ list-style:none; }
		ul#choice-block  {columns: 4; -webkit-columns: 4; -moz-columns: 4;}
		strong 													{ font-weight:700; }
		#frame 													{ width:auto; max-width: 800px; background:transparent; margin:3px auto; padding:10px; color:#333 !important; }
		div#frame h2 											{ width:auto; border-bottom:1px solid #bdbdbd; padding:0 0 5px 0; font-size:30px; }
		h3.question 											{ font-weight:normal; margin:20px 0; padding:0; font-style:italic; display:block; }
		p.pager 												{ margin:5px 0 5px; color:#999; text-align:right; }
		.qnumber 												{ font-size:25px; font-weight:bold; font-style:italic; vertical-align:bottom; }
/*		.number                                 { font-size:25px; font-weight:bold; font-style:normal; vertical-align:inherit; padding-right:10px; } */

		.score 					{ width:100%; display:inline-block; margin:30px 0; font-size:100px; text-align:center; }
		img.question-image 										{ width:100%; height:auto; display:block; max-width:705px; margin:10px auto; border:1px solid #ccc; }
	*/	#choice-block 				{ display:block; list-style:none; margin:0; padding:0; cursor: pointer; }
		#submitbutton 				{ cursor:pointer; -webkit-border-radius: 5px; -moz-border-radius: 5px; border-radius: 5px; } */
	/*	#submitbutton:hover 									{ background:#7b8da6; } */
		#explanation 				{ width:auto; min-height:100px; margin:0 auto; padding:20px 0; text-align:center; }
		#explanation span 			{ font-weight:bold; padding-right:8px; }
		.choice-box 				{ width:50%;  display:block;  text-align:center;  margin:5px auto !important; padding:10px 0 !important; border:1px solid #bdbdbd; }
		.correct 				{ color:#51a351; font-size: 20px; display: block; margin-bottom: 5px; border-bottom: 1px #51a351 solid; padding-bottom: 5px; }
		.incorrect 				{ color:#f93939; font-size: 20px; display: block; margin-bottom: 5px; border-bottom: 1px #f93939 solid; padding-bottom: 5px; }
    </style>
</head>
<body>
<div class="form-group rsform-block rsform-block-framecontent">
    <div id="frame" role="content"></div>
</div>
<hr>
<!--<div class="form-group rsform-block rsform-block-placecontent">
	<label class="col-sm-3 control-label formControlLabel" data-toggle="tooltip" title="" for="placecontent"></label>
	<div class="col-sm-6 formControls">
		<textarea cols="50" rows="5" name="form[placecontent]" id="placecontent" readonly="" class="rsform-text-box form-control rsform-text-box"></textarea>			
	</div>
</div>	-->
	
<!--<div class="col-sm-6 formControls rsform-block-submit">
	<button type="submit" name="form[submit]" id="submit" onclick="copyText()" class="rsform-submit-button  btn btn-primary">Submit Quiz</button>			
</div> -->
</body>
</html>

*This quiz may not work in Internet Explorer. If you can't see the quiz then please try using another browser.*
