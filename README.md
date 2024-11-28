Steps
------
1. Download Source
   .env file, update openai-api-key<br/>
   npm install<br/>
   node --env-file=.env index.js<br/>
   ngrok http 3001 ( memo the public address )<br/>
2. Console -> Voice
   select General under Settings,<br/>
   and enable the [Predictive and Generative AI/ML] Features Addendum in order to use ConversationRelay<br/>
3. Console -> TwiML Bin, create a new Twiml Bin<br/>
     \<Response\><br/>
        \<Connect\><br/>
         \<ConversationRelay url="wss://[your ngrok public address]" <br/>
            welcomeGreeting="This is a ConversationRelay test, tell me how can I help you." /\><br/>
        \</Connect\><br/>
    \</Response\><br/>
4. Console -> Phone Numbers
   assign Twiml Bin(step3) to the phone number<br/>

5. make a call to your Twilio number ( step4 )
