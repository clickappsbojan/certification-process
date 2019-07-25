# FlightAvail
### Request

```
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

```

<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <soap:Body>
        <FlightAvailResponse xmlns="http://www.juniper.es/webservice/2007/">
            <AvailabilityRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-24T16:32:24.2600276+02:00" IntCode="ldIoA1cTvSs/aX07fx7NK6WzSYl72PfmbrzQI/1Ayj8=">
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
                    <FlightResult FareType="PUB" AvailableSeats="7" Number="73" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhkmBeb1H1TKRI1r+4gsiP82u5FT/XX3hzyqFFwwowg3CQpScS/2026puSf+hI/iAplkOj/rEPXy09TX/hL7J455T3BrL6pmNuWVfAXdBvRFqNFpMwCA34L2qmKI5/kIdx+W6U6/+md6OfGhJJUoc9Axw7I7REXXWkZmjDW6VAuS1vqxDrQr3uQc/PbbmOb3Qzdd9q/eHkbRhWoWG1a/KPYKi7RLx1PMqlSvW1L9hak+DoF+44kD/dAmlQbRViMIF0esRpsFPySchxARSoIjMvwYiI3odZOydPWT6BKbmL4fVs2AewgsTIpHqzt/7I48wjs9YlOjYaC2/TpmL4DAM4ZriMxPB1XxzaZlG8slLJ9ltCuneFlKZsZ97PqJWGIEUIS1PV3++InY34wHn+h1uKzxt8BWYcmyhCCFdpfTid0AraMyow0guUgOW+7lIeuhXBmFK7cvzIxRanDP+cPvPxN905gOKu//jYIxwQBw7hjIUlk4iBC9Iok9LI1HTKIKFv+/dA6GISHj9VnTd2iIR6OTAPV8H+8D34SbNH9puKkfJ7EWgPFwKG6fu5OnT+mRsUlRoLulUGVmpZVzRpgBh33CIR9AGIMUH2TndY2rF3fp+vtiKKX3s+aLRdSEZHbcXpsfF3ZfVKuVFhf8ADCln7K8CAW5PKdbXgR1LIqlm13eNtSuSvrH/GfrtWTmqlqAD1iNYmLTI7ZsBF9G9OiKpKsv6SgeQt9n5Km1yXRPjYgO7h5OYpd7vbs5k2uqib83ioYx0RQTzw6DHiqUeeHozcfidYX5JmLHEoNP4Ns+0jpXO/FuF64yvbuTE887ky+EtG+yGwTsTlXnCFkIlY/L4dTA/8AvkNeSRoUBD9PL7sDOLNdTsYTVxoZQizlFC4KCC00lkkR4D42Cw4yAo74KB/yu4I0KPSCflF4DGQsXHNd0L6drGj46e9g6FbSYgnIbLkhUAyUzYOUjy+3n2MPv1+IGy4RqgMFV1UZy6HBCsMon6zJrayKPlgH4Zp3qQovNQjdOySuQnT5T+0D9jI6UOdfqt+58rxYHrRFhIIsVyeOoIAt5vvdVXdcK9MMmfl18dLMJdz2h//Xl7fAcPxmrwd/TuXPnckkUiBR+WKSyIeQNKNCNH4W7ZxkO5NDeCQ3pk5oxfUHZ8XKBWW7dLfAqknI88B8TDDuwLqPIa6913Ip+ajPTwn6pHxdow6Igwfnzdpb5ZOjBSmye7vcsdsD9NQiE1J189WAV06Ho2oc7aQF1wKEdVd5bolaHG++ZVEKCgg/1S4nH8zmd9kZRZGdboIJ4" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AM">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="MEX" DepartureDate="2019-10-16T14:40:00" ArrivalDate="2019-10-16T17:35:00" OperatingAirline="AM" MarquetingAirline="AM" FlightNumber="435" JourneyDuration="P0DT21H15M0S" Class="H" Cabin="Y" AirplaneType="7S8" FareBasis="HKNN0XCB" />
                                    <Segment DepartureAirport="MEX" ArrivalAirport="MAD" DepartureDate="2019-10-16T23:55:00" ArrivalDate="2019-10-17T17:55:00" OperatingAirline="AM" MarquetingAirline="AM" FlightNumber="21" JourneyDuration="P0DT21H15M0S" Class="H" Cabin="Y" AirplaneType="789" FareBasis="HKNN0XCB" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="6462.08" Nett="6462.08">
                                    <Service Amount="6405.1" />
                                    <ServiceTaxes Included="false" Amount="56.98" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="3202.55" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="3202.55" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="28.49" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="6405.1" Amount="28.49" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="6405.1" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="6405.1" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="28.49" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="6405.1" Amount="28.49" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="6405.1" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="6405.1" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-07-27</Rule>
                        </Rules>
                    </FlightResult>
                </Results>
            </AvailabilityRS>
        </FlightAvailResponse>
    </soap:Body>
</soap:Envelope>
```

# FlightCheckAvail (if applicable)
### Request
```
## Code
```
### Response

```
## Code
```
# FlightBookingRules
### Request
### Response

# FlightBooking
### Request
### Response

# FlightTicketing

### Request
### Response


# ReadBooking
### Request
### Response

# CancelBooking
### Request
### Response