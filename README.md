Steps
------
1. Download Source
   .env file, update openai-api-key
   npm install
   node --env-file=.env index.js
   ngrok http 3001 ( memo the public address )
   
2. Console -> Voice
   select General under Settings,
   and enable the [Predictive and Generative AI/ML] Features Addendum in order to use ConversationRelay
   
4. Console -> TwiML Bin, create a new Twiml Bin
   <Response>
      <Connect>
         <ConversationRelay url="wss:/[your ngrok public address]" 
            welcomeGreeting="This is a ConversationRelay test, tell me how can I help you." />
      </Connect>
  </Response>
  
5. Console -> Phone Numbers
   assign Twiml Bin(step3) to the phone number

6. make a call to your Twilio number ( step4 )
