### Request
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns="http://www.juniper.es/webservice/2007/">
    <soapenv:Header/>
        <soapenv:Body>
            <FlightBooking>
                <FlightBookingRQ Version="1.1" Language="es">
                    <Login Email="user@mydomain.com" Password="pass"/>
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
                            <BookingCode>LF6j9ndyo/zlz9tkRLu5T4vcqg4Y3XWeGauWGUmxxJy33kAWihQpwFONCEgQgZ8jh2qgNLr3UUIh1pN4HhPScgnu6ACy2Y1zX5xk57se1WmQzVivCicyxC4QtRadlYH3MHutZDy4r21/hua6VvkNNiOHdg82Q+i4acEVOVXbHI7wQPb+W30kIdASPPA659TznXCo0gePlvzhNjJQFb7XJqoLpFzbfD6i4u7HmrUVkjwmOuOKoX931NZYr27f28RCXkQLQ+FkYYLA9FpKne8iVC9DaVsBhSQ4naUH3OdyMBqEFav/iOQVI1uznUNlz74/U6EDmIiQbslAJ7AiJlqG7clfZ76gZdx1CT9Hh54lBFKeuCkEfZC+XkHV5784swD8VdpxxLkfOiJHxbnKF5HRKj6LyxfsL/mXMfhxZ/1sh75EkTdUhcHFp7UXBoYZyq6GQnZdIPuuKP6kUKpyGZs42OyuefLMtEzPZFt21UbpdGK0eRNfS/Gd0jgJCtamw8wUstBn9e6NIshZYeAF/H3rV0ae4QT5p7Sfr8RFF1txE9Mc/OtZNBUMHHAZU4mcW1KL5advMCHSHUkSKeJhQg3LPgJmKpPzKGFw5fB6zBtWypmiSTBI7qZL9jVn7Rz3vYEIrV5I80QANj3fOjpkbKtk7I61xzaKV0SeQWmuYuADrh3k9AvVX5CbwILZkaFUooSrPp8KV22jWglZn3elFFbu+Ns0XzHfgE/uEU9GsTZST1b7FI6TKg/blS8bhyZT94b/c+Q/xr3IcVVRz37hCwheLJtMNmG3TFEOXD4D+tkQRc87vNN4QYRwr4g0HnuWRulJy5sSqoY741yP82ZN2lb/dSsWMBek8U48bVbndoVpcWSw69HT89tqBQ7XfGTdcmYtsmNwxtP3OGCHY1F9+ffyjwQaIg3ACh5tCNSWAoISYWSwE5z99MNY+AFO9goY1XXAw9Ff3g+H0tvN2jgjvLiWn1euw2hRVmv0Aefagsu29pcWCaT2xVawqAfh+SSldqrI</BookingCode>
                    <RelPaxesDist>
                        <RelPaxDist>
                            <RelPaxes>
                                <RelPax IdPax="1" />
                                <RelPax IdPax="2" />
                                <RelPax IdPax="3" />
                            </RelPaxes>
                        </RelPaxDist>
                    </RelPaxesDist>
                            <FlightBookingInfo Start="2014-01-08" End="2015-01-08">
                                <Price>
                                    <PriceRange Minimum="115.78" Maximum="115.78" Currency="USD"/>
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
            <BookingRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-28T14:01:08.1885549+02:00" IntCode="0PoY1pFc7ulrrO3/IPAww6Tj/8wWPXPIBFWXzSJtRJ8=">
                <Reservations>
                    <Reservation Locator="NRMB75" Status="PAG" Language="es">
                        <Holder>
                            <RelPax IdPax="4" />
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
                                <BornDate>2014-07-28</BornDate>
                                <Address>Passenger addressA</Address>
                                <City>Passegner city</City>
                                <Country>Yemen</Country>
                                <PostalCode>00000</PostalCode>
                                <Nationality>Passenger nationality</Nationality>
                            </Pax>
                            <Pax IdPax="4">
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
                            <FlightItem ItemId="131684" Status="OK">
                                <Prices>
                                    <Price Type="S" Currency="EUR">
                                        <TotalFixAmounts Gross="103.99" Nett="103.99">
                                            <Service Amount="103.99" />
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
                                                <Concept Type="BAS" Name="Base Coste">
                                                    <Items>
                                                        <Item Amount="9.45" Quantity="1" Days="1" PaxType="CNN" TtaCode="302" />
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
                                    <RelPax IdPax="3" />
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