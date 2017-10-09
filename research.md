## Research
İt seems that thats not so possible to send a message to user that we choose directly over whatsapp. Whatapp allow to send message to user with http request but allows user have to do one last thing.

in this page : https://faq.whatsapp.com/en/android/28000012

whatsapp says that; there is two way to send a message
 
1. With http method : https://faq.whatsapp.com/en/android/26000030/?category=5245251

   like this ;
   ```
   https://api.whatsapp.com/send?phone=15551234567&text=I'm%20interested%20in%20your%20car%20for%20sale
   ```
   I try this method but at the end of process user have to push the send button

2. With android intent system
    like this ;
    ```
    Intent sendIntent = new Intent();
    sendIntent.setAction(Intent.ACTION_SEND);
    sendIntent.putExtra(Intent.EXTRA_TEXT, "This is my text to send.");
    sendIntent.setType("text/plain");
    startActivity(sendIntent);
    
    sendIntent.setPackage("com.whatsapp");
    startActivity(sendIntent);    
    ```
    
    
    
Also there is some open source projects claim to send whatsapp messages automaticly.
  
  1.  
