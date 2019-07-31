### Request
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns="http://www.juniper.es/webservice/2007/">
<soapenv:Header/>
<soapenv:Body>
<ReadBooking>
<ReadRQ Version="1.1" Language="en">
<Login Email="user@mydomain.com" Password="pass"/>
<ReadRequest ReservationLocator="FS1ML2"/>
</ReadRQ>
</ReadBooking>
</soapenv:Body>
</soapenv:Envelope>
```
### Response

---
---
---

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <soap:Body>
        <ReadBookingResponse xmlns="http://www.juniper.es/webservice/2007/">
            <BookingRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-31T16:42:42.1499305+02:00" IntCode="tkY/CZ6nzdY9xPtjhKOLO2GKei7Ba7hHUOFlQw6bFOA=">
                <Reservations>
                    <Reservation Locator="FS1ML2" Status="CAC" Language="en">
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
                            <FlightItem ItemId="132806" Status="CA">
                                <Prices>
                                    <Price Type="S" Currency="EUR">
                                        <TotalFixAmounts Gross="398.3" Nett="398.3">
                                            <Service Amount="398.3" />
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
        </ReadBookingResponse>
    </soap:Body>
</soap:Envelope>
```