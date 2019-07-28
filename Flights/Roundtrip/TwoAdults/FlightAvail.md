### Request
```xml
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns="http://www.juniper.es/webservice/2007/">
    <soap:Header/>
    <soap:Body>
        <FlightAvail>
            <FlightAvailRQ Version="1.1" Language="en">
                <Login Password="56pEh6uT" Email="TestXMLClickapps"/>
               
                <Paxes>
               	   
               	    <Pax IdPax="1">
               	    	<Age>28</Age>
               	    </Pax>
               	    
               	    <Pax IdPax="2">
               	    	<Age>28</Age>
               	    </Pax>
               	</Paxes>
                
                <FlightRequest>
                    <SearchSegmentsFlight>
                        <SearchSegmentFlight>
                            
                            <CountryOfResidence>SA</CountryOfResidence>
                            <Routes>
                                <Route Origin="39681" Destination="37786" Date="2019-10-16"/>
                                <Route Origin="37786" Destination="39681" Date="2019-10-16"/>
                            </Routes>
                        </SearchSegmentFlight>
                    </SearchSegmentsFlight>
                    <RelPaxesDist>
                        <RelPaxDist>
                            <RelPaxes>
                                <RelPax IdPax="1"/>
                                <RelPax IdPax="2"/>
                            </RelPaxes>
                        </RelPaxDist>
                    </RelPaxesDist>
                </FlightRequest>
                <AdvancedOptions>
                    <CalendarSearch>true</CalendarSearch>
                    <ShowBreakdownPrice>true</ShowBreakdownPrice>
                    <UseCurrency>USD</UseCurrency>
                </AdvancedOptions>
            </FlightAvailRQ>
        </FlightAvail>
    </soap:Body>
</soap:Envelope>
```
### Response

```xml
## Code
```