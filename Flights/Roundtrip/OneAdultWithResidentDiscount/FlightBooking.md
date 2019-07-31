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
					</Paxes>
					<Holder>
				    	<RelPax IdPax="1"/>
					</Holder>
					<Elements>
						<FlightElement ElementId="1">
							<BookingCode>LF6j9ndyo/zlz9tkRLu5T4vcqg4Y3XWeGauWGUmxxJy33kAWihQpwFONCEgQgZ8jfv40vfGcKGOk7ka1rxIDEShQwvSyC/AJ5kriJ8gXxU6jPCpYeknGTdX+bkRTr2yg+0lc7DSgURATgRif4hZ7QMFn7PfViq6/SGkFNHK+xOGxEXejKwY5Up/bhfKBkPQoPpkvoWzwoKUU5K221DXmh7kpSe97zGk2oghzXWFRUdtDrV3ux2NFKDEv6D6blThwhwc2+PkIq2M55NmTMJzUqHHtv9wIgUnOw+JBazUQH5i5HwbdeuxQxVOGR24W9u1wZWVnK4EZxideITCpcY5badZIAxqMssyjixvisy72yumlG5fYJlODVMC37onojTqBAeaM9GIx8D6nPPdfyEnaO/OFCS+3H15uPjj02xTUD+jdkXV3cmz8Ao6+Jsp1AxSbuBKLER0kXl9mNGQC9zKHz4jhcQs5CY5rEl9lILsPzxq6a3lONoro6Ro/ge/4H/Nxa5MwucDpadcKMRUx8tjI2KrOBigCol4PLyGPD29TEyRY0uPnxGw1lGDB0eeevSttvm3VO91cKuQD9PzRHWymuNXaTLbnh78qEV6sqVS+kWWJ/r7TaCecUVQiQO2dDE/p7pLGxjwn6MFPH/Vwlw10koBN2Vz/WcBCcCRp5s16oWT4owzwivnVabJYPquAOAxIApyDXtrTo5MmE4PiL5ciwDlOOXYyH+tzGC+E+KAMKz+KkV1soZCSbhmfkKnCpeG+K13TIBeAavyaj5S23rYG/T31EQUlR/bDrstJ0BVp++tJgxxyiJ0Qlfmur536aJ7j9V9KqMzW7LcbjqipE3J3SQ1d7u0WdadjkomAMYHR/P6j560Wsb+RJFdSBFSjx+SGqIkooO0GAt3Oo/vaaEehTnu57xQb8iqaoIM2+lz79nJOBjDvWYBzLPBb1zmaCZcc</BookingCode>
							<RelPaxesDist>
								<RelPaxDist>
									<RelPaxes>
									  <RelPax IdPax="1"/>
									</RelPaxes>
								</RelPaxDist>
							</RelPaxesDist>
							<FlightBookingInfo Start="2014-05-16" End="2015-05-17">
								<Price>
							    	<PriceRange Minimum="47.17" Maximum="47.17" Currency="EUR"/>
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
            <BookingRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-31T15:50:44.1262216+02:00" IntCode="8MmVmqDi3Ls4i+2Njrck1O1t4QRIf0fwrR9/8jZ/5sI=">
                <Reservations>
                    <Reservation Locator="KG7NY5" Status="PAG" Language="en">
                        <Holder>
                            <RelPax IdPax="2" />
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
                            <FlightItem ItemId="132798" Status="OK">
                                <Prices>
                                    <Price Type="S" Currency="EUR">
                                        <TotalFixAmounts Gross="47.17" Nett="47.17">
                                            <Service Amount="47.17" />
                                        </TotalFixAmounts>
                                        <Breakdown>
                                            <Concepts>
                                                <Concept Type="BAS" Name="Base Coste">
                                                    <Items>
                                                        <Item Amount="47.17" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                                    </Items>
                                                </Concept>
                                            </Concepts>
                                        </Breakdown>
                                    </Price>
                                </Prices>
                                <Routes ValidatingCarrier="EI">
                                    <Route Origin="37786" Destination="39681">
                                        <Segments>
                                            <Segment DepartureAirport="MAD" ArrivalAirport="MCO" DepartureDate="2019-10-28T10:00:00" ArrivalDate="2019-10-28T17:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="1234" Class="B" Cabin="Y" FareBasis="200">
                                                <TechnicalStops />
                                            </Segment>
                                        </Segments>
                                    </Route>
                                </Routes>
                                <AdditionalElements />
                                <RelPaxes>
                                    <RelPax IdPax="1" />
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