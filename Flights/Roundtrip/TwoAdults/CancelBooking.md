### Request
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns="http://www.juniper.es/webservice/2007/">
	<soapenv:Header/>
		<soapenv:Body>
			<CancelBooking>
				<CancelRQ Version="1.1" Language="es">
					<Login Password="xxxxx" Email="xxxxxxxx"/>
					<CancelRequest ReservationLocator="KJF18R"/>
				</CancelRQ>
			</CancelBooking>			
     	</soapenv:Body>
</soapenv:Envelope>


```

---
---
---

### Response

#### Success

```xml

```

#### Flield

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <soap:Body>
        <CancelBookingResponse xmlns="http://www.juniper.es/webservice/2007/">
            <BookingRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-28T11:49:45.6721445+02:00" IntCode="dqVp2rueg1SSHyG4I3fbPKTE4F8LzYNuDcLWUzuy0ko=">
                <Warnings>
                    <Warning Code="warnCancelledAndCancellationNotCalculated" Text="Cancellation cost could not be calculated. Reservation was cancelled and it is pending of cancellation cost." />
                </Warnings>
                <Reservations>
                    <Reservation Locator="KJF18R" Status="CAC" Language="en">
                        <Holder>
                            <RelPax IdPax="3" />
                        </Holder>
                        <Paxes>
                            <Pax IdPax="1">
                                <Document Type="PAS">123456</Document>
                                <PhoneNumbers>
                                    <PhoneNumber>+971505660000</PhoneNumber>
                                </PhoneNumbers>
                                <Title>Mr</Title>
                                <Name>Ali</Name>
                                <Surname>Al-Sheiba</Surname>
                                <Age>19</Age>
                                <Email>a@a.com</Email>
                                <BornDate>2000-01-01</BornDate>
                                <Address>Dubai</Address>
                                <City>Dubai</City>
                                <Country>AE</Country>
                                <PostalCode>00000</PostalCode>
                                <Nationality>YE</Nationality>
                            </Pax>
                            <Pax IdPax="2">
                                <Document Type="PAS">123456</Document>
                                <PhoneNumbers>
                                    <PhoneNumber>+971505660000</PhoneNumber>
                                </PhoneNumbers>
                                <Title>Mr</Title>
                                <Name>Alia</Name>
                                <Surname>aAl-Sheiba</Surname>
                                <Age>19</Age>
                                <Email>aa@a.com</Email>
                                <BornDate>2000-01-01</BornDate>
                                <Address>Dubai</Address>
                                <City>Dubai</City>
                                <Country>AE</Country>
                                <PostalCode>00000</PostalCode>
                                <Nationality>YE</Nationality>
                            </Pax>
                            <Pax IdPax="3">
                                <Document Type="PAS">123456</Document>
                                <PhoneNumbers>
                                    <PhoneNumber Type="TFN">+971505660000</PhoneNumber>
                                </PhoneNumbers>
                                <Title>Mr</Title>
                                <Name>Ali</Name>
                                <Surname>Al-Sheiba</Surname>
                                <Age>19</Age>
                                <Email>a@a.com</Email>
                                <BornDate>2000-01-01</BornDate>
                                <Address>Dubai</Address>
                                <City>Dubai</City>
                                <Country>AE</Country>
                                <PostalCode>00000</PostalCode>
                                <Nationality>YE</Nationality>
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
                            <FlightItem ItemId="131653" Status="CA">
                                <Prices>
                                    <Price Type="S" Currency="SAR">
                                        <TotalFixAmounts Gross="1666.64" Nett="1666.64">
                                            <Service Amount="1666.64" />
                                        </TotalFixAmounts>
                                    </Price>
                                </Prices>
                                <Routes ValidatingCarrier="EI">
                                    <Route Origin="39681" Destination="37786">
                                        <Segments>
                                            <Segment DepartureAirport="MCO" ArrivalAirport="MAD" DepartureDate="2019-10-25T10:00:00" ArrivalDate="2019-10-25T20:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="1" Class="FT" Cabin="F">
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
                            <FlightItem ItemId="131654" Status="CA">
                                <Prices>
                                    <Price Type="S" Currency="SAR">
                                        <TotalFixAmounts Gross="1666.64" Nett="1666.64">
                                            <Service Amount="1666.64" />
                                        </TotalFixAmounts>
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
        </CancelBookingResponse>
    </soap:Body>
</soap:Envelope>
```
