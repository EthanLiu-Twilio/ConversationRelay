This is a minimal version of the components that you can quickly confirm/check for the Twilio ConversationRelay feature. Enjoy!

Steps
------
1. Download Source<br/>
   .env file, update openai-api-key<br/>
   npm install<br/>
   node --env-file=.env index.js<br/>
   ngrok http 3001 ( memo the public address )<br/>
2. Console -> Voice<br/>
   select General under Settings,<br/>
   and enable the [Predictive and Generative AI/ML] Features Addendum in order to use ConversationRelay<br/>
3. Console -> TwiML Bin<br/>
   create a new Twiml Bin<br/>
     \<Response\><br/>
        \<Connect\><br/>
         \<ConversationRelay url="wss://[your ngrok public address domain, remove the https part]" <br/>
            welcomeGreeting="This is a ConversationRelay test, tell me how can I help you." /\><br/>
        \</Connect\><br/>
    \</Response\><br/>
4. Console -> Phone Numbers<br/>
   assign Twiml Bin(step3) to the phone number<br/>

5. make a call to your Twilio number ( step4 )
