### Request
```xml
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns="http://www.juniper.es/webservice/2007/">
    <soap:Header/>
    <soap:Body>
        <FlightAvail>
            <FlightAvailRQ Version="1.1" Language="en">
                <Login Password="xxxxxxx" Email="xxxxxxxxxxx"/>
               
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
---
---
---

### Response

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <soap:Body>
        <FlightAvailResponse xmlns="http://www.juniper.es/webservice/2007/">
            <AvailabilityRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-28T10:47:42.5493433+02:00" IntCode="2lAhrSptUsj0rZ8QD8WV9JMnbIe461xEGbMuIv5KZ7E=">
                <Results>
                    <FlightResult FareType="CHA" AvailableSeats="20" Number="1" Direction="Inbound" LowCost="false" RatePlanCode="LF6j9ndyo/zlz9tkRLu5T4vcqg4Y3XWeGauWGUmxxJy33kAWihQpwFONCEgQgZ8j3MYnbZCiHJVG3tYrqJx3gJshoeNGijCN4wKm8yPI+Atx2j1gmfEyA+u+xJkFUx6mv3EDM08fGg58yKNPSbfeXTIMMqH2NLlqJkZxNAWnGTz9J7WLZr6qzvfLRspkFdBYTyVc/ByVCezR4T5xbJgVJYXnjtRdXaaGh6J2QmbM+E4csFmmrbSTBdyaANDpcjU8/qyJwZf10lC1VFBacKkaUfRFYb7aXiZggMKURER7L54WUcpq021IAq9nnzIKYCsavyZBfhttJOW1igjSyg5kOoUTiRUFbInVonCXQb9bkM+jjPtH8K9CMvLFicHv6ZBpmyhUtNzeRddhQRxWeNY1YlQUFD1wq4dTWZU1UJq8LI9qfQHXt2xyrE7b6noyT4ZpE6/qjRUwlZHcGo5BQfuNTzl56pz+KcweBfYjbHm1cj7JN53qJiMBQSMrcPFT9dZiusa1Z/4C2hpw+j5UmprIT8AROpr2iRz0um4SbwdFkIZPLSu0dO5WvaYPAJK1X0H3d9m2R9KRFwjxOgf+7dwnjEbJdQxTUHXlN/kXt3Y0x0KwQjyo5Sw0yOXZXqzDoKI40bEr+aMqh/z1IHjS6xyDmLTafUoR/oO6yyl1lWGCU5vIkV8Uyfai6BgZEVk++43pn9Sc0LXq28/kiHVyb0ZedhHgSEqT3K0at+pSChQQ8HPQyfRoctdqO/yxm2Mbpgu/6VsAlH7uFfraIxO7L27A7/J7aHKkeRGIJODNWbyzB39dP0xTLFnDaGff5XeRrp2/pm2v+zj6i7t9eEIo9dI3wMrA4zM76z05Y30rhy6QymalQk0bEdtos82IelPQ82lh/R669cN3NFX1buX+KMFFbroWE6yVc8Zy/FnCgFzFfwvXhgvi02HkRt5ifLFA6z+5I8JTzafgzoVY/uAjCol9hg==" Status="OK" Source="ChV2">
                        <Routes ValidatingCarrier="EI">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="MCO" DepartureDate="2019-10-16T10:00:00" ArrivalDate="2019-10-16T17:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="1234" JourneyDuration="P0DT7H0M0S" GroundDuration="P0DT7H0M0S" Class="B" Cabin="Y" FareBasis="200" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="105.26" Nett="105.26">
                                    <Service Amount="105.26" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="52.63" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="52.63" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                </Breakdown>
                            </Price>
                        </Prices>
                    </FlightResult>
                    <FlightResult FareType="CHA" AvailableSeats="10" Number="2" Direction="Inbound" LowCost="false" RatePlanCode="LF6j9ndyo/zlz9tkRLu5T4vcqg4Y3XWeGauWGUmxxJy33kAWihQpwFONCEgQgZ8jY0a8Z5rhqEnnWlXMMza8L9bgsKc6j6ib8esQUjPeDM4hPljwtwUuZp3KqRyw/WQwExpyNL0bKwZybRJ15Vl6fQnTYOSAMgnsCeO3aOiCiHlFokEQOIU+kgkxDn1S5kok4YSYBxJO3S69B/9ar8Yeoa/+T+EA2FI/aQURkY61+18ovvNZOkOPQ9lPU6REhlf4vQIAjXjxGBcS7b+hAq/5fdIWKiKxSTwS12+boN7Fu6OGjs/LFm7ptB+bwsYqFrnwVg3iKmMijUcZzg80CocAqj9BGXo65lZUpSzJMnNd+ljW31kvuZLKaNHysGTJef7cd/hvh6HzPSRyghIZz0LsVvRsM4+QScQhE8yQSZtvby9VdYoyVOqnNVW8eMrMEKX4RwsiGdn6y35msky/Kjf152FjTId4Z7nUGN/CmKJ2y1QIwwj9gW2dGIXtomA9l8GPHQoQt6rsi0tgg5wydk86WlcvGxOzcpvQYXaeGNN5g3Exq6LkSlCHJxMxNkwCVc1zl8Gki8r6o1HSlJ4mAsmrqaVNLPa67hHAnIlDEDzc/2EkS3AjCiEQeLQMYwh3gJ/h/mV/Ba0V3V7z9hUzxe/QvNEDluKeBdDcSl4qeRV9x7iAPyWlJhvRZB5D/PQNdbTKl0nAJgVmRRUPuJFcxXcJE6euPUf9j478ZD/10bS17PK0jVxNWZsBXoFzR/LbaiULFhAoNh6xjOdoC1geF7UFOdktM9K3D3ykT4BzSMc1TpAsFJEOACiDD3Z7zO8rIsUwguV4ayTTlrJnXm2IdhwsSl5eGbB/DWxiYhHPkM34pDAFo11zdGavb9zcHn7LmKj2p+RHD6ktS7ug3GskGkpzXu9bWpEvPCr1aDJj5YJDYD/br8/vRYotNnmboFXN0D9Jo991dqTqYzc4msYqaeWvvA==" Status="OK" Source="ChV2">
                        <Routes ValidatingCarrier="EI">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="MCO" DepartureDate="2019-10-16T10:00:00" ArrivalDate="2019-10-16T17:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="1234" JourneyDuration="P0DT7H0M0S" GroundDuration="P0DT7H0M0S" Class="A" Cabin="F" FareBasis="300" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="210.52" Nett="210.52">
                                    <Service Amount="210.52" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="105.26" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="105.26" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                </Breakdown>
                            </Price>
                        </Prices>
                    </FlightResult>
                    <FlightResult FareType="CHA" AvailableSeats="95" Number="3" Direction="Outbound" LowCost="false" RatePlanCode="7Vor0/GRKZ31Va+BuE1WMFvq/9heAul4psoTS3hesB97bKcS8vVV8I7otP/319flrdJtWLiEoO9sY2UlyEo7APHFZiZMluWNxBk88NMkmKnixQx8gXkxdGDFx6/M2WEKJN5ElaKVisxaoP7McBaePT2KLiMKE+pmeObeflYXK71r4Hq5gJVQFfBZ5x8QDr+X0kwlL17pkitjc3yZBaRbby0gGMOZ81xta3lcbu6Nhs1uxlyxqP4WwwT5r7WUc1Xk5oQd1QmyefM8Fc2ViwJ/MxiqqXuFRrytdjDUc+/pnL9LDqnPgqPZXs+hAi3va3UhBJLq7l/we+nBxI7lHynl8KNTQCZwQT/R6PmhAe4Vlf8a2ES0mDqS1oQUZwJa7/msrl1tAJbUtlHFeEt+fm25PmvL6r6ot6k0gN3tyNfys8o9GyT0c2OFJNYE9O0DBSzKRuk0eyBh3ASS8er8Iyh//t0wsrYX1lAX4cffNmUi/LwjK6qUWW6Xv2+qZyewhXKjiX73OHKWra/LOgJrAhUbZWzeQ0b+ONr9pAN5sktAy+/uQPJ5Y5l5MxXsjULKbxPoQ3kPpNPedrEI6gw+2KQ8irKEWHZg1upO7R7soJqQhQDKgRi4OiNcInAkHEL0hQMzIOo+raYjitM6G6EyI2ih05buuTb+fZAI2TDeBBbDezZVk/On/nNZSJ4eqmLp8M4pzGt8h3Ulkc3QL1y7SdjvH1mCbzdlcBP/oje9u1m38XAp02UbzgHQjfQPWxdvxAxDzzQIdcVTs3kuEUMpKF40Hsa8CCs8qIKIUqxJyYWcLHOU8N8HSZtAcub0mA2koxmFtYPvq04GcErjQbn9+eeBGdUfinIj4Pi194O+NnTutsFzh3E7ncSyesfhauDxgW8n3iZJSYbtkpQ0wWHhVrBfQuqMW9GeOiTSuQC1uKiNibaUPThj14ig1kTrmcKZzsKC" Status="OK" Source="ChV2">
                        <Routes ValidatingCarrier="EI">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="MAD" DepartureDate="2019-10-16T10:00:00" ArrivalDate="2019-10-16T20:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="1" JourneyDuration="P0DT8H0M0S" GroundDuration="P0DT8H0M0S" Class="FT" Cabin="F" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="444.44" Nett="444.44">
                                    <Service Amount="444.44" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="222.22" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="222.22" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                </Breakdown>
                            </Price>
                        </Prices>
                    </FlightResult>
                    <FlightResult FareType="CMB" Number="4" Direction="RoundTrip" LowCost="false" RatePlanCode="7Vor0/GRKZ31Va+BuE1WMFvq/9heAul4psoTS3hesB97bKcS8vVV8I7otP/319flrdJtWLiEoO9sY2UlyEo7APHFZiZMluWNxBk88NMkmKnixQx8gXkxdGDFx6/M2WEKJN5ElaKVisxaoP7McBaePT2KLiMKE+pmeObeflYXK71r4Hq5gJVQFfBZ5x8QDr+X0kwlL17pkitjc3yZBaRbby0gGMOZ81xta3lcbu6Nhs1uxlyxqP4WwwT5r7WUc1Xk5oQd1QmyefM8Fc2ViwJ/MxiqqXuFRrytdjDUc+/pnL9LDqnPgqPZXs+hAi3va3UhBJLq7l/we+nBxI7lHynl8KNTQCZwQT/R6PmhAe4Vlf8a2ES0mDqS1oQUZwJa7/msrl1tAJbUtlHFeEt+fm25PmvL6r6ot6k0gN3tyNfys8o9GyT0c2OFJNYE9O0DBSzKRuk0eyBh3ASS8er8Iyh//t0wsrYX1lAX4cffNmUi/LwjK6qUWW6Xv2+qZyewhXKjiX73OHKWra/LOgJrAhUbZdiVRiTYmLur09FG0NI8lNVrh9hZ/eT7NvcBeR6cCR9LVbOKL/EgiRy0uu8tkH7OsZ3xDNf9Qo5grcsDF8A1+ALMmSC2Cp6LGGJqGDvXrEezmhclC0k12IqQtDVfnIKjNpz/3BHZJ7WcC5ArbvLrJciEOa5HDuPfzuRV1CQPT/ywv2RI9NokDOOQksXhmbmdt/vgjn+g48l/cnBAePTvd1YQNSffgt0qzdjLUrJruYD8He6ZKGu/m6JKgwY3VyQYDcxfmUp8WXhVNIyvMpLVK6hDA6c8Qvm/8uAUR8lVzRbohGekvlD4+A00TNbI2NdGDhG+SzS4FOO6MOLL9gAEFdi5rffyq7aqBh+wELw79KiHAXAomRMdxqAfagBXhEF2PRP286A0fsJMYVTowAiLkoafH3Kt7iThaeuSi1gGh7t8h88YU+ArCL2PK5kAHZespkTDR7iMgUfMPBE7t4CAV8d1bW3oV2/RpQRLR0zkCdTOq808qdh6HB7WISmtQ/8eO6esGLlif5ldRAwuhAQJTxsD7ppbWfs9WWoWrpwldRH+lbXnLKCBsF1HDPOWViDlLO3cbdqWpo9He1NFxar37vhA7jWEilZ2NNZKJsQn7VFkPE5ftiEtdmqiKuMiEOO0QCJlQoCUf+T/8NfuNvNPRUOeIYatysv8aY8ujLPMpCQBEjs0gMct7e/X9yNZmbUeKTdunOF//aBGkv6/dh0njMUewTr7c8ukiq/7415SfqYPz7cVjHPgv9NkUbpQdfh1zzjlD4ufCEn+FxHZhPZvW4aASE9L9m2PU4FP+D6Eq6yNuPNyozljuda/dQ+OTGy9MQphiIFzIl9kLjk6KS/Ck+nyw0KUiwkPbP5ahuv7VuSdWKqSQHwzjzwe1EnnJCvewQIl/YSRcLlEDwYCvJutX5GwAs2GGSEfm8k/8lReHyYmVv2Crgpts/x80AjntFg2dKgZXpGHFZMn2EwlbpPaWSPI0G2Vkd7nfcpBHPGzO9tNcXrZsFNdy4gOznbM6mqDGe9hS5AJXgXizuRpI4BALEe5qkWUTaLRyj0eNLhI3Mh/pMNTg0p5KiGS1SKJFSvI3YfWyp13M+CpQ7ep4cepia4RvZ4MHRvcbOzq0qeZBs5EmHhcTC8W0KxO/HMADsoDRzhsXbvjbjlRW69Mhg1QAKYW0hhdrcBPmZhzpADBNKaEXECn7FInJvthEAE0V7I7sRUqmiXX7qY4VZrdCmZ9oUOkNXHVLGTs92S8p+AOuPv/i8iYtVePevhsHrtfelcqpA0bL+g18SVyF2w0DZjlQJ8yRwYmHJoKpDy+f5FGVgtrB4lkv7e9/7oPU4pLRg9MgToKKCBktrmUWbqX5FzDs9VnhXcsRIxyQRVjTG9xili6" Status="OK" Source="ChV2">
                        <Routes ValidatingCarrier="EI">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="MAD" DepartureDate="2019-10-16T10:00:00" ArrivalDate="2019-10-16T20:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="1" JourneyDuration="P0DT8H0M0S" GroundDuration="P0DT8H0M0S" Class="FT" Cabin="F" />
                                </Segments>
                            </Route>
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="MCO" DepartureDate="2019-10-16T10:00:00" ArrivalDate="2019-10-16T17:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="1234" JourneyDuration="P0DT7H0M0S" GroundDuration="P0DT7H0M0S" Class="B" Cabin="Y" FareBasis="200" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Recommended="0" Gross="549.7" Nett="549.7">
                                    <Service Amount="549.7" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="222.22" Quantity="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="222.22" Quantity="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="52.63" Quantity="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="52.63" Quantity="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                </Breakdown>
                            </Price>
                        </Prices>
                    </FlightResult>
                </Results>
            </AvailabilityRS>
        </FlightAvailResponse>
    </soap:Body>
</soap:Envelope>
```