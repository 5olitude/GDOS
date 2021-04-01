# GDDOS
Denial Of Service attack in GO using TOR 

* EDUCATIONAL PURPOSE ONLY


 * CODE DESCRIPTION
  
     * ddos.go  
     
          --Its  the  modification Konstantin8105/DDoS attack  using tor
          
     * simpleddos.go  
     
          --Minimal code of line ddos attack not banging into a server at once
          
     * simpletorddos.go 
     
          --Minimal code using tor connection
          
          
     * testtor.go 
     
          --Simple script to check the tor connectivity
          
          *********************************************************************************************

* ddos.go  explanation 

             Concurrency is not  parallelism
             ********************************
             In this code section we are defining the workers
             
             
	           for i := 0; i < d.amountWorkers; i++ {
		             go func() {
                 
                 
                 }
		 
                 
            - Upto a certain limit the no of workers decides the code result .Incresaing the no of workers may help but there is not point in increasing beyond a               limit
            
            - This same concept is applicable for time.Sleep too
  
  
     * Code Execution  
          
	  go run ddos.go -workers=200 -url=http://somekejfjejf4chan.kjd:80 (no of worker in default set to 100)
	  
	  If you want to dive into the  code just change the time.sleep(1 *time.Second) and amount of workers just play around 😊
	  
	  
     *  Did we forget something ?
         
	  consider you play around the code into someones server the situation may be worse its a good practice to establish a tor connection
	  
	  first ensure that tor is running in your system and note the port number normally tor runs in 9050 and change the code
	  torcon, _ :=        url.Parse("socks5://127.0.0.1:9050")
	  
	  
 * simpletorddos.go
  
           This is the implementation of minimal code ddos attack logic is same as above not messing up with channels cool 😊
	   
	   
	   
 * tortester.go 
        
	checks the ip addr 
	  

    


