### Request
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns="http://www.juniper.es/webservice/2007/">
	<soapenv:Header/>
		<soapenv:Body>
			<ReadBooking>
			<ReadRQ Version="1.1" Language="es">
			<Login Email="user@mydomain.com" Password="pass"/>
			<ReadRequest ReservationLocator="NRMB75"/>
			<AdvancedOptions>
				<UseCurrency>USD</UseCurrency>
			</AdvancedOptions>
			</ReadRQ>
			</ReadBooking>
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
        <ReadBookingResponse xmlns="http://www.juniper.es/webservice/2007/">
            <BookingRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-28T14:01:31.639847+02:00" IntCode="jSlIw3AAt7Su3LBqA56RQnVxeed7rkxuFxLC301BeK4=">
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
        </ReadBookingResponse>
    </soap:Body>
</soap:Envelope>
```