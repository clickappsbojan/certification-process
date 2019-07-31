### Request
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns="http://www.juniper.es/webservice/2007/">
	<soapenv:Header/>
		<soapenv:Body>
			<FlightBooking>
				<FlightBookingRQ Version="1.1" Language="en">
                 <Login Email="user@mydomain.com" Password="pass"/>
					<Paxes>
						<Pax Gender="M" IdPax="1">
							<Document Type="DNI">11111111H</Document>
							<PhoneNumbers>
							  <PhoneNumber>971000000</PhoneNumber>
							</PhoneNumbers>
							<Title>Mr</Title>
							<Name>Name A</Name>
							<Surname>Surname A</Surname>
							<Age>30</Age>
							<Email>pax@mail.com</Email>
							<BornDate>1984-01-01</BornDate>
							<Address>Gremi Fusters 33, Oficina 302</Address>
							<City>Palma</City>
							<Country>ES</Country>
							<PostalCode>07009</PostalCode>
							<Nationality>ES</Nationality>
						</Pax>
						<Pax Gender="M" IdPax="2">
							<Document Type="DNI">11111111H</Document>
							<PhoneNumbers>
							  <PhoneNumber>971000000</PhoneNumber>
							</PhoneNumbers>
							<Title>Mr</Title>
							<Name>Name B</Name>
							<Surname>Surname B</Surname>
							<Age>30</Age>
							<Email>pax@mail.com</Email>
							<BornDate>1984-01-01</BornDate>
							<Address>Gremi Fusters 33, Oficina 302</Address>
							<City>Palma</City>
							<Country>ES</Country>
							<PostalCode>07009</PostalCode>
							<Nationality>ES</Nationality>
						</Pax>
					</Paxes>
					<Holder>
				    	<RelPax IdPax="1"/>
					</Holder>
					<Elements>
						<FlightElement ElementId="1">
							<BookingCode>7Vor0/GRKZ31Va+BuE1WMFvq/9heAul4psoTS3hesB97bKcS8vVV8I7otP/319flrdJtWLiEoO9sY2UlyEo7AAymB9ND8KjSvVdFJpcmOjuKUqVr/8yLd18XaMWgIm9ykB2/2g/0Onvapv6hMcEHoXs5BhlCGUoz/Z/KXF7JNVlV+9a7KKaJiAGGLM6E4zfHVl/RdjeqUbhydDJnq5PJf2QrMA52s3SDutdI7FB7CycX6cHD5PgEgJCB5m44vLDWUcCQeNfCiFR/B4YEIPTzgKS1kABi+bohfi0PYWOea77SV4hxTqsMwzO7F6Bp5y/zODywYO553kRP+rmkAhvV8AYEgqiZU4FKMn61KyDecK/PqdNH0uxonkgFbtgia40+Ow+0to37wizUqCpOFGtGBqn19yXqdm2yiGae2e98RN8uY5RIGeCj7jsgYcAJNMEhscFdx64WTpLetI8fvoHfq5aE6u8/HgVLSucRv/4YpyIKFs7K21B5QnD7LPjf6cwsxwkITvRTRVlwI+IZNpkKqORJwvp3iJ+6rG8vtuuR0emX3GkB013iKERHjX4+PEY9iG0MbjidOWbAmeewbkPUbIGK8nAz80AP8xvhbmvXCJcThpaAmc2dTtCq1EZ+iHCyNX+3AhXWxiTaaUBkriA96MpxteElZgSefgATMQtK1OaTkUWo0vlgj2WR8lb9IZrotN4Ka7isSAPxjjrlIc6khjUsQndgVNFYgeqDuZgc0tN0I3Q1ey9YIxjH5Bu5GQ4QbVE+EQeNZq7Qs2fyMk65Aej9ZqV8WTG/K3nbZpBL+PqCPO9xSonWVOidSeWTECfcZHN32gzbzkX1fwh3rPi2/Aeq5i63z+qv5gP7Goo5ztkdd4aM5b8LXPDE+Y4kUo6Q9LQ5GxnrQzqTb7Vc5GRbZgmkBrer92mrV5Nua+b3VFu9vx1sch02kTnlrW+NTCQT</BookingCode>
							<RelPaxesDist>
								<RelPaxDist>
									<RelPaxes>
									  <RelPax IdPax="1"/>
									  <RelPax IdPax="2"/>
									</RelPaxes>
								</RelPaxDist>
							</RelPaxesDist>
							<FlightBookingInfo Start="2014-05-16" End="2015-05-17">
								<Price>
							    	<PriceRange Minimum="398.3" Maximum="398.3" Currency="EUR"/>
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
### Response

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <soap:Body>
        <FlightBookingResponse xmlns="http://www.juniper.es/webservice/2007/">
            <BookingRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-31T16:41:26.0774641+02:00" IntCode="SwWxDT3TgbG//FqeCt+yBoMFeNoej66XoWKruggEohc=">
                <Reservations>
                    <Reservation Locator="FS1ML2" Status="PAG" Language="en">
                        <Holder>
                            <RelPax IdPax="3" />
                        </Holder>
                        <Paxes>
                            <Pax IdPax="1">
                                <Document Type="DNI">11111111H</Document>
                                <PhoneNumbers>
                                    <PhoneNumber>971000000</PhoneNumber>
                                </PhoneNumbers>
                                <Title>Mr</Title>
                                <Name>Name A</Name>
                                <Surname>Surname A</Surname>
                                <Age>30</Age>
                                <Email>pax@mail.com</Email>
                                <BornDate>1984-01-01</BornDate>
                                <Address>Gremi Fusters 33, Oficina 302</Address>
                                <City>Palma</City>
                                <Country>ES</Country>
                                <PostalCode>07009</PostalCode>
                                <Nationality>ES</Nationality>
                            </Pax>
                            <Pax IdPax="2">
                                <Document Type="DNI">11111111H</Document>
                                <PhoneNumbers>
                                    <PhoneNumber>971000000</PhoneNumber>
                                </PhoneNumbers>
                                <Title>Mr</Title>
                                <Name>Name B</Name>
                                <Surname>Surname B</Surname>
                                <Age>30</Age>
                                <Email>pax@mail.com</Email>
                                <BornDate>1984-01-01</BornDate>
                                <Address>Gremi Fusters 33, Oficina 302</Address>
                                <City>Palma</City>
                                <Country>ES</Country>
                                <PostalCode>07009</PostalCode>
                                <Nationality>ES</Nationality>
                            </Pax>
                            <Pax IdPax="3">
                                <Document Type="DNI">11111111H</Document>
                                <PhoneNumbers>
                                    <PhoneNumber Type="TFN">971000000</PhoneNumber>
                                </PhoneNumbers>
                                <Title>Mr</Title>
                                <Name>Name A</Name>
                                <Surname>Surname A</Surname>
                                <Age>30</Age>
                                <Email>pax@mail.com</Email>
                                <BornDate>1984-01-01</BornDate>
                                <Address>Gremi Fusters 33, Oficina 302</Address>
                                <City>Palma</City>
                                <Country>ES</Country>
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
                            <FlightItem ItemId="132806" Status="OK">
                                <Prices>
                                    <Price Type="S" Currency="EUR">
                                        <TotalFixAmounts Gross="398.3" Nett="398.3">
                                            <Service Amount="398.3" />
                                        </TotalFixAmounts>
                                        <Breakdown>
                                            <Concepts>
                                                <Concept Type="BAS" Name="Base Coste">
                                                    <Items>
                                                        <Item Amount="199.15" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                                    </Items>
                                                </Concept>
                                                <Concept Type="BAS" Name="Base Coste">
                                                    <Items>
                                                        <Item Amount="199.15" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                                    </Items>
                                                </Concept>
                                            </Concepts>
                                        </Breakdown>
                                    </Price>
                                </Prices>
                                <Routes ValidatingCarrier="EI">
                                    <Route Origin="39681" Destination="37786">
                                        <Segments>
                                            <Segment DepartureAirport="MCO" ArrivalAirport="MAD" DepartureDate="2019-10-28T10:00:00" ArrivalDate="2019-10-28T20:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="1" Class="FT" Cabin="F">
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