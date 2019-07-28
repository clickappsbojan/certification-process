### Request
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns="http://www.juniper.es/webservice/2007/">
	<soapenv:Header/>
		<soapenv:Body>
			<ReadBooking>
			<ReadRQ Version="1.1" Language="es">
			<Login Email="TestXMLClickapps" Password="56pEh6uT"/>
			<ReadRequest ReservationLocator="V4W2HZ"/>
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
            <BookingRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-28T17:08:36.0101784+02:00" IntCode="wL/rum9ANsodYIxqTr22780TKZ2HZVda4b1DtDxFgNI=">
                <Reservations>
                    <Reservation Locator="V4W2HZ" Status="CAN" Language="es">
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
                                <Country>Yemen</Country>
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
                            <FlightItem ItemId="131697" Status="CA">
                                <Prices>
                                    <Price Type="S" Currency="EUR">
                                        <TotalFixAmounts Gross="134.14" Nett="134.14">
                                            <Service Amount="74" />
                                            <ServiceTaxes Included="false" Amount="60.14" />
                                        </TotalFixAmounts>
                                    </Price>
                                </Prices>
                                <CancellationPolicy CurrencyCode="EUR">
                                    <FirstDayCostCancellation Hour="23:50">2019-07-29</FirstDayCostCancellation>
                                    <Description>Si el vuelo esta emitido, tiene un 100% de gastos de cancelación. * Cancelando desde 28/07/2019 a las 00:00:00 hasta 29/07/2019 a las 23:50:00: 0 &amp;euro;Si el vuelo esta emitido, tiene un 100% de gastos de cancelación. * Cancelando desde 29/07/2019 a las 23:50:00: 100.00 % gastos</Description>
                                    <PolicyRules>
                                        <Rule DateFrom="2019-07-28" DateFromHour="00:00" DateTo="2019-07-29" DateToHour="23:50" Type="R" FixedPrice="0" PercentPrice="0" Nights="0" ApplicationTypeNights="Average" />
                                        <Rule DateFrom="2019-07-29" DateFromHour="23:50" Type="R" FixedPrice="0" PercentPrice="100" Nights="0" ApplicationTypeNights="Average" />
                                    </PolicyRules>
                                </CancellationPolicy>
                                <Routes ValidatingCarrier="UX">
                                    <Route Origin="40233" Destination="37786">
                                        <Segments>
                                            <Segment DepartureAirport="PMI" ArrivalAirport="MAD" DepartureDate="2019-10-16T21:10:00" ArrivalDate="2019-10-16T22:35:00" OperatingAirline="UX" MarquetingAirline="UX" FlightNumber="6096" Class="Z" Cabin="Y" AirplaneType="73H" FareBasis="ZD1Y4L">
                                                <TechnicalStops />
                                            </Segment>
                                        </Segments>
                                    </Route>
                                    <Route Origin="37786" Destination="40233">
                                        <Segments>
                                            <Segment DepartureAirport="MAD" ArrivalAirport="PMI" DepartureDate="2019-10-25T08:20:00" ArrivalDate="2019-10-25T09:45:00" OperatingAirline="UX" MarquetingAirline="UX" FlightNumber="6031" Class="N" Cabin="Y" AirplaneType="E90" FareBasis="NDYY4L">
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