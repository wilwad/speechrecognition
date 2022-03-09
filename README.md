# speechrecognition
Javascript Chrome Speech Recognition class

Sample usage

```
var phrases = 'orange|yellow|blue|green|red|black|white|pink|gold|magenta|purple|brown'.split('|')
var recog = new ChromeSpeechRecognition(phrases)

recog.onresult = function(phrase, confidence){
    phrase = phrase.toLowerCase()
    console.log( 'I heard you say:', phrase)
    
    if (phrases.indexOf(phrase) > -1) 
        document.body.style.backgroundColor = phrase
    else
        console.log('unrecognized phrase', phrase)    
}
```
