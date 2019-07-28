### Request
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns="http://www.juniper.es/webservice/2007/">
    <soapenv:Header/>
        <soapenv:Body>
            <FlightBooking>
                <FlightBookingRQ Version="1.1" Language="es">
                    <Login Email="xxxxxxxx" Password="xxxxxxxxxxxx"/>
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
		                    <Country>Yemen</Country>
		                    <PostalCode>00000</PostalCode>
		                    <Nationality>Passenger nationality</Nationality>
	                  </Pax>
	                  
	                  <Pax IdPax="3">
	                    <Name>Passenger nameA</Name>
	                    <Surname>Passenger surnameA</Surname>
	                    <Age>5</Age>
	                    <BornDate>2005-07-28</BornDate>
	                    <Address>Passenger addressA</Address>
	                    <City>Passegner city</City>
	                    <Country>Yemen</Country>
	                    <PostalCode>00000</PostalCode>
	                    <Nationality>Passenger nationality</Nationality>
                      </Pax>

	                  <Pax IdPax="4">
	                    <Name>Passenger nameAB</Name>
	                    <Surname>Passenger surnameAB</Surname>
	                    <Age>5</Age>
	                    <BornDate>2014-07-28</BornDate>
	                    <Address>Passenger addressA</Address>
	                    <City>Passegner city</City>
	                    <Country>Yemen</Country>
	                    <PostalCode>00000</PostalCode>
	                    <Nationality>Passenger nationality</Nationality>
                      </Pax>
                    </Paxes>
                    <Holder>
                        <RelPax IdPax="1"/>
                    </Holder>
                    <Elements>
                        <FlightElement ElementId="1">
                            <BookingCode>LF6j9ndyo/zlz9tkRLu5T4vcqg4Y3XWeGauWGUmxxJy33kAWihQpwFONCEgQgZ8jBiKPBLBrUDh6I2tXxLJHYih0qUE6xzVNJYVWBO6wczcZlU+YqHyh3MmG6qFQh8i4yIznbMaIMqhobyUNI3eHUy6af2uhSPp6cg5tU/bFEiT1CxT8IO2TVKLglJd98u+QwvGj/I/XzWs+Ubm6NL0B0VBt2PROOe6QmgI5bCsIFT9/o4SPfcAhuxiUS7GECZyEorM/L/ObylH0nbjofEP8nXR+scMYzkHGa7Lq3uDwSxWqWvdwM3NM18XnhIQSAxTPgG4MTAR96WSXajdRrWN1dPM4/0/kMVJLtAzRVN8W9W3Wya/z0nFPWmQH68CdQwAQ3i/JcvNMduoK20udho4wrKBw+7BdjcX8YtAYEOpJZ3OzLE+d35wZKtAH7miC4VzdnFAZKenwR7PpxH7f+zwZwSVb9h9FMekjP8EJTQ1V5sKh956UP5zIi9FBipiqjowtxpjBmNTopwKUGtrrrIpNoPcxUgm9ZUJitL6mFj7cZi7rZKcBwGTKdAlMWUjCSgkgIop9qsGMv987eTAnGQVdWM20RrTSHZQf3amREg+uDz0Nfm5U+yvkyLL+Tsz9wFOmV6hkWrI3N1eYmcNye8yPvmT19KqSohXbJJesYFz6PuccRQRSsY6Nrvl1uMyqGedrZ/9RJOlhdqbI+0zKQeXFqQohlZBNNE4gJkRCoL3MybVXV+jLjfB0jzL6le9iGOAF1EWs7YiUddbrcxCGXx6KwCQGiRagXavAyoX/yL+CYVpIo92aH+YKHHrXy6C9AYv0qOGPZwCJrn/ZZlbWkw/G47UCo/x5IP3SLwbNpiMbnJ1VbbOKpiUJg02RW9JxQYKvyvckQFT55pYe0SugOAegv4ybKNoEee6zmkEe1Xe/k37A4goNIQ/CgIGTQMDzWOQf1yqH8bTT6jBMjZ9CnkZp5gxYtmRPSmV4YK9qC7gDB4hM0vN8E6SmcSUPf6/Z4xHtGj839pmt4nXLQ4ydG2XNbg==</BookingCode>
                    <RelPaxesDist>
                        <RelPaxDist>
                            <RelPaxes>
                                <RelPax IdPax="1" />
                                <RelPax IdPax="2" />
                                <RelPax IdPax="3" />
                                <RelPax IdPax="4" />
                            </RelPaxes>
                        </RelPaxDist>
                    </RelPaxesDist>
                            <FlightBookingInfo Start="2014-01-08" End="2015-01-08">
                                <Price>
                                    <PriceRange Minimum="168.41" Maximum="168.41" Currency="USD"/>
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
            <BookingRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-28T14:24:06.5759769+02:00" IntCode="gIoQGjYkxlHtGMj32ivcnG6+kv1cyhjqQ3gzXX7p3oo=">
                <Reservations>
                    <Reservation Locator="N3QP5P" Status="PAG" Language="es">
                        <Holder>
                            <RelPax IdPax="5" />
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
                                <Country>Yemen</Country>
                                <PostalCode>00000</PostalCode>
                                <Nationality>Passenger nationality</Nationality>
                            </Pax>
                            <Pax IdPax="3">
                                <Name>Passenger nameA</Name>
                                <Surname>Passenger surnameA</Surname>
                                <Age>5</Age>
                                <BornDate>2005-07-28</BornDate>
                                <Address>Passenger addressA</Address>
                                <City>Passegner city</City>
                                <Country>Yemen</Country>
                                <PostalCode>00000</PostalCode>
                                <Nationality>Passenger nationality</Nationality>
                            </Pax>
                            <Pax IdPax="4">
                                <Name>Passenger nameAB</Name>
                                <Surname>Passenger surnameAB</Surname>
                                <Age>5</Age>
                                <BornDate>2014-07-28</BornDate>
                                <Address>Passenger addressA</Address>
                                <City>Passegner city</City>
                                <Country>Yemen</Country>
                                <PostalCode>00000</PostalCode>
                                <Nationality>Passenger nationality</Nationality>
                            </Pax>
                            <Pax IdPax="5">
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
                            <FlightItem ItemId="131686" Status="OK">
                                <Prices>
                                    <Price Type="S" Currency="EUR">
                                        <TotalFixAmounts Gross="151.26" Nett="151.26">
                                            <Service Amount="151.26" />
                                        </TotalFixAmounts>
                                        <Breakdown>
                                            <Concepts>
                                                <Concept Type="BAS" Name="Base Coste">
                                                    <Items>
                                                        <Item Amount="47.27" Date="2019-10-25" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                                    </Items>
                                                </Concept>
                                                <Concept Type="BAS" Name="Base Coste">
                                                    <Items>
                                                        <Item Amount="47.27" Date="2019-10-25" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                                    </Items>
                                                </Concept>
                                                <Concept Type="BAS" Name="Base Coste">
                                                    <Items>
                                                        <Item Amount="47.27" Date="2019-10-25" Quantity="1" Days="1" PaxType="ADT" TtaCode="202" />
                                                    </Items>
                                                </Concept>
                                                <Concept Type="BAS" Name="Base Coste">
                                                    <Items>
                                                        <Item Amount="9.45" Date="2019-10-25" Quantity="1" Days="1" PaxType="CNN" TtaCode="303" />
                                                    </Items>
                                                </Concept>
                                            </Concepts>
                                        </Breakdown>
                                    </Price>
                                </Prices>
                                <Routes ValidatingCarrier="EI">
                                    <Route Origin="37786" Destination="39681">
                                        <Segments>
                                            <Segment DepartureAirport="MAD" ArrivalAirport="MCO" DepartureDate="2019-10-25T10:00:00" ArrivalDate="2019-10-25T17:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="1234" Class="B" Cabin="Y" FareBasis="200">
                                                <TechnicalStops />
                                            </Segment>
                                        </Segments>
                                    </Route>
                                </Routes>
                                <AdditionalElements />
                                <RelPaxes>
                                    <RelPax IdPax="1" />
                                    <RelPax IdPax="2" />
                                    <RelPax IdPax="3" />
                                    <RelPax IdPax="4" />
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