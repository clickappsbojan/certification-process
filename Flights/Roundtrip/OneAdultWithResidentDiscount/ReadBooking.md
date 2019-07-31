### Request
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns="http://www.juniper.es/webservice/2007/">
<soapenv:Header/>
<soapenv:Body>
<ReadBooking>
<ReadRQ Version="1.1" Language="en">
<Login Email="user@mydomain.com" Password="pass"/>
<ReadRequest ReservationLocator="KG7NY5"/>
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
            <BookingRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-31T16:04:47.1322979+02:00" IntCode="7rIYj7OG8D36YymrYVrX47ErXFa5oPN4Cvq8EwM8+XQ=">
                <Reservations>
                    <Reservation Locator="KG7NY5" Status="CAC" Language="en">
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
                            <FlightItem ItemId="132798" Status="CA">
                                <Prices>
                                    <Price Type="S" Currency="EUR">
                                        <TotalFixAmounts Gross="47.17" Nett="47.17">
                                            <Service Amount="47.17" />
                                        </TotalFixAmounts>
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
        </ReadBookingResponse>
    </soap:Body>
</soap:Envelope>
```