### Request
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns="http://www.juniper.es/webservice/2007/">
	<soapenv:Header/>
		<soapenv:Body>
			<ReadBooking>
			<ReadRQ Version="1.1" Language="es">
			<Login Email="user@mydomain.com" Password="pass"/>
			<ReadRequest ReservationLocator="H52HT7"/>
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
            <BookingRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-29T15:53:45.0447723+02:00" IntCode="tkY/CZ6nzdY9xPtjhKOLOxy00m7JLcwxwwhWB5RdKeU=">
                <Reservations>
                    <Reservation Locator="H52HT7" Status="PAG" Language="en">
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
                            <Pax IdPax="2">
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
                            <Pax IdPax="3">
                                <Document Type="DNI">11111111H</Document>
                                <PhoneNumbers>
                                    <PhoneNumber Type="TFN">971000000</PhoneNumber>
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
                            <FlightItem ItemId="131860" Status="OK">
                                <Prices>
                                    <Price Type="S" Currency="EUR">
                                        <TotalFixAmounts Gross="13502.3" Nett="13502.3">
                                            <Service Amount="12312" />
                                            <ServiceTaxes Included="false" Amount="1190.3" />
                                        </TotalFixAmounts>
                                    </Price>
                                </Prices>
                                <CancellationPolicy CurrencyCode="EUR">
                                    <FirstDayCostCancellation Hour="23:50">2019-08-26</FirstDayCostCancellation>
                                    <Description>Si el vuelo esta emitido, tiene un 100% de gastos de cancelación. * Cancelando desde 29/07/2019 a las 00:00:00 hasta 26/08/2019 a las 23:50:00: 0 &amp;euro;Si el vuelo esta emitido, tiene un 100% de gastos de cancelación. * Cancelando desde 26/08/2019 a las 23:50:00: 100.00 % gastos</Description>
                                    <PolicyRules>
                                        <Rule DateFrom="2019-07-29" DateFromHour="00:00" DateTo="2019-08-26" DateToHour="23:50" Type="R" FixedPrice="0" PercentPrice="0" Nights="0" ApplicationTypeNights="Average" />
                                        <Rule DateFrom="2019-08-26" DateFromHour="23:50" Type="R" FixedPrice="0" PercentPrice="100" Nights="0" ApplicationTypeNights="Average" />
                                    </PolicyRules>
                                </CancellationPolicy>
                                <Routes ValidatingCarrier="BA">
                                    <Route Origin="39681" Destination="37786">
                                        <Segments>
                                            <Segment DepartureAirport="MCO" ArrivalAirport="LGW" DepartureDate="2019-10-28T19:25:00" ArrivalDate="2019-10-29T07:30:00" OperatingAirline="BA" MarquetingAirline="BA" FlightNumber="2036" Class="J" Cabin="C" AirplaneType="777" FareBasis="J1N0C9S1" VendorLocator="SFO3YM">
                                                <TechnicalStops />
                                            </Segment>
                                            <Segment DepartureAirport="LHR" ArrivalAirport="MAD" DepartureDate="2019-10-29T10:40:00" ArrivalDate="2019-10-29T14:10:00" OperatingAirline="IB" MarquetingAirline="BA" FlightNumber="7055" Class="J" Cabin="C" AirplaneType="321" FareBasis="J1N0C9S1" VendorLocator="SFO3YM">
                                                <TechnicalStops />
                                            </Segment>
                                        </Segments>
                                    </Route>
                                </Routes>
                                <AdditionalElements>
                                    <Bags>
                                        <Bag BaggageType="holdBaggage" Quantity="2" />
                                    </Bags>
                                </AdditionalElements>
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