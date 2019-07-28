### Request
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns="http://www.juniper.es/webservice/2007/">
    <soapenv:Header/>
        <soapenv:Body>
            <FlightBooking>
                <FlightBookingRQ Version="1.1" Language="es">
                    <Login Email="TestXMLClickapps" Password="56pEh6uT"/>
                    <Paxes>
	                     <Pax Gender="M" IdPax="1">
	                         <Document Type="PAS" ExpirationDate="2024-07-04T00:00:00+02:00">123456789</Document>
	                         <Name>A</Name>
	                         <Surname>B</Surname>
	                         <Age>25</Age>
	                         <BornDate>1984-01-01</BornDate>
	                         <PostalCode>07009</PostalCode>
	                         <Nationality>ES</Nationality>
                             <Address>Almukalla</Address>
                            <City>Almukalla</City>
                            <Country>Passenger country</Country>
                            <PostalCode>0000</PostalCode>
	                     </Pax>
	                    
		                  <Pax IdPax="2">
		                    <Name>Passenger name</Name>
		                    <Surname>Passenger surname</Surname>
		                    <Age>28</Age>
		                    <BornDate>1989-07-28</BornDate>
		                    <Address>Passenger address</Address>
		                    <City>Passegner city</City>
		                    <Country>Passenger country</Country>
		                    <PostalCode>00000</PostalCode>
		                    <Nationality>Passenger nationality</Nationality>
	                  </Pax>
                    </Paxes>
                    <Holder>
                        <RelPax IdPax="1"/>
                    </Holder>
                    <Elements>
                        <FlightElement ElementId="1">
                            <BookingCode>LF6j9ndyo/zlz9tkRLu5T4vcqg4Y3XWeGauWGUmxxJy33kAWihQpwFONCEgQgZ8j3MYnbZCiHJVG3tYrqJx3gAyIPsnY+DOhhGz7Ik+1nzThEw3mA6A87A/RmDhBHyqqzbpboirrnvwk+SWM5D/sF8MGq9HMitejzPj0cMOuzAYqXPpPUbUqXPL3khsczbISn/h7xx0P+mQAdvGtPr4US6Pz76Ru5vFqbbN+A0Pta8AAvGKtdmDm73DKZvCeVeGoP+nPYM6gfd3BJK1AS4oC+TXnT2EYHHBF1WQkkjKGe8YcRhBLykdY9wBjR+6dm/mZXNLzzwEPDtlJaY8CkVNNQNkiIM8/ewEtI79RGogoO63iPAu70UEMtXUO7atThFK09SBoaiBwOI+DC2wvEWPWk3BHgEOxxJ4f+8HyzVESs9yN7RSgJUmJYu/jRwnbmBOPzbLmZs0doXRfowx1T8D0kd3yM1Iys+2MRMoJS8iOCiFU93IGldQwlYDh1tFRR3OBHqrw4ALkcNqU2x29CqTWLxGLXDod9H9iNPPPL2H708d8x2MTYhGOyOeib50BVWd8pbstvyJunaYgOO0oSAcjE2lVCwhpiR/835mKp36Gbi3EzAirFI4ptBb1CUkPyAJqxHUFiGbLGUfT0IB67G59HJXmAyLWuEHgi53IFKiUBqe8slmTkGaf8SKjHxL8CFWDhRDfaBX6pS2se6FEINNP4DP0V0nrqSQfNoUjUZQM2LKe5E110D70yPuCnoeKUppcmDiETigODi5PcCFywoT4E5f9x7AjpVu8GDifDIGaLAiLI7/W0rLK8wvtgiLpojBrDR/q8A37eJdPa+1WHQCkDJeyv9KUSxtAqj/0sA51dlU9V2OnT7FYIGM3iV53E9Ndm5nK5vK9jTmQnKWTIGDWQ/F+efr7aKpOpjKvVyD1JS/KLeRax4Wwy8hUQeHtPH+Mj6dbPQrmf/Jk4SpwGSNlVQ==</BookingCode>
                    <RelPaxesDist>
                        <RelPaxDist>
                            <RelPaxes>
                                <RelPax IdPax="1" />
                                <RelPax IdPax="2" />
                            </RelPaxes>
                        </RelPaxDist>
                    </RelPaxesDist>
                            <FlightBookingInfo Start="2014-01-08" End="2015-01-08">
                                <Price>
                                    <PriceRange Minimum="105.26" Maximum="105.26" Currency="USD"/>
                                </Price>
                            </FlightBookingInfo>
                        </FlightElement>
                    </Elements>
                    <AdvancedOptions>
                        <ShowBreakdownPrice>true</ShowBreakdownPrice>
                    </AdvancedOptions>
                </FlightBookingRQ>
            </FlightBooking>
        </soapenv:Body>
</soapenv:Envelope>
```

---
---
---

### Response

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <soap:Body>
        <FlightBookingResponse xmlns="http://www.juniper.es/webservice/2007/">
            <BookingRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-28T11:07:29.3370956+02:00" IntCode="Ra4b0zVYUITjRO5W7KntHlWlQqoHNhB/cZMizWDKjQU=">
                <Reservations>
                    <Reservation Locator="5H7452" Status="PAG" Language="es">
                        <Holder>
                            <RelPax IdPax="3" />
                        </Holder>
                        <Paxes>
                            <Pax IdPax="1">
                                <Document Type="PAS">123456789</Document>
                                <Name>A</Name>
                                <Surname>B</Surname>
                                <Age>25</Age>
                                <BornDate>1984-01-01</BornDate>
                                <Address>Almukalla</Address>
                                <City>Almukalla</City>
                                <Country>Passenger country</Country>
                                <PostalCode>07009</PostalCode>
                                <Nationality>ES</Nationality>
                            </Pax>
                            <Pax IdPax="2">
                                <Name>Passenger name</Name>
                                <Surname>Passenger surname</Surname>
                                <Age>28</Age>
                                <BornDate>1989-07-28</BornDate>
                                <Address>Passenger address</Address>
                                <City>Passegner city</City>
                                <Country>Passenger country</Country>
                                <PostalCode>00000</PostalCode>
                                <Nationality>Passenger nationality</Nationality>
                            </Pax>
                            <Pax IdPax="3">
                                <Document Type="PAS">123456789</Document>
                                <Name>A</Name>
                                <Surname>B</Surname>
                                <Age>25</Age>
                                <BornDate>1984-01-01</BornDate>
                                <Address>Almukalla</Address>
                                <City>Almukalla</City>
                                <Country>Passenger country</Country>
                                <PostalCode>07009</PostalCode>
                                <Nationality>ES</Nationality>
                            </Pax>
                        </Paxes>
                        <AgenciesData>
                            <AgencyData>
                                <ReferencedAgency>false</ReferencedAgency>
                                <AgencyCode>1042</AgencyCode>
                                <AgencyName>Test XML Clickapps</AgencyName>
                                <AgencyHandledBy>Test XML Clickapps</AgencyHandledBy>
                                <AgencyEmail>amyalbooking@gmail.com</AgencyEmail>
                            </AgencyData>
                            <AgencyData>
                                <ReferencedAgency>true</ReferencedAgency>
                                <AgencyCode>0</AgencyCode>
                            </AgencyData>
                        </AgenciesData>
                        <Items>
                            <FlightItem ItemId="131633" Status="OK">
                                <Prices>
                                    <Price Type="S" Currency="EUR">
                                        <TotalFixAmounts Gross="94.54" Nett="94.54">
                                            <Service Amount="94.54" />
                                        </TotalFixAmounts>
                                        <Breakdown>
                                            <Concepts>
                                                <Concept Type="BAS" Name="Base Coste">
                                                    <Items>
                                                        <Item Amount="47.27" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                                    </Items>
                                                </Concept>
                                                <Concept Type="BAS" Name="Base Coste">
                                                    <Items>
                                                        <Item Amount="47.27" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                                    </Items>
                                                </Concept>
                                            </Concepts>
                                        </Breakdown>
                                    </Price>
                                </Prices>
                                <Routes ValidatingCarrier="EI">
                                    <Route Origin="37786" Destination="39681">
                                        <Segments>
                                            <Segment DepartureAirport="MAD" ArrivalAirport="MCO" DepartureDate="2019-10-16T10:00:00" ArrivalDate="2019-10-16T17:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="1234" Class="B" Cabin="Y" FareBasis="200">
                                                <TechnicalStops />
                                            </Segment>
                                        </Segments>
                                    </Route>
                                </Routes>
                                <AdditionalElements />
                                <RelPaxes>
                                    <RelPax IdPax="1" />
                                    <RelPax IdPax="2" />
                                </RelPaxes>
                            </FlightItem>
                        </Items>
                    </Reservation>
                </Reservations>
            </BookingRS>
        </FlightBookingResponse>
    </soap:Body>
</soap:Envelope>
```