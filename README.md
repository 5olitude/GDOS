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
                 
             Upto a certain limit the no of workers decides the code flow .Incresaing the no of wor

    


