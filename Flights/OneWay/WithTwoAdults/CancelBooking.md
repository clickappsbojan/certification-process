### Request
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns="http://www.juniper.es/webservice/2007/">
	<soapenv:Header/>
		<soapenv:Body>
			<CancelBooking>
				<CancelRQ Version="1.1" Language="es">
					<Login Email="user@mydomain.com" Password="pass"/>
					<CancelRequest ReservationLocator="53FXPK"/>
				</CancelRQ>
			</CancelBooking>			
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
        <CancelBookingResponse xmlns="http://www.juniper.es/webservice/2007/">
            <BookingRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-29T15:52:05.2870634+02:00" IntCode="TgCPzJ5OMdc5jvqeyZXq6v/Wo/RBZjTJq9XJAAp/SlQ=">
                <Warnings>
                    <Warning Code="warnCancelledAndCancellationCostRetrieved" Text="Cancellation cost retrieved. Reservation was cancelled." />
                    <CancelInfo>
                        <BookingCodeState>CaC</BookingCodeState>
                        <BookingCancelCost>0</BookingCancelCost>
                        <BookingCancelCostCurrency>SAR</BookingCancelCostCurrency>
                    </CancelInfo>
                </Warnings>
                <Reservations>
                    <Reservation Locator="53FXPK" Status="CAC" Language="en">
                        <Holder>
                            <RelPax IdPax="2" />
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
                                <Country>SA</Country>
                                <PostalCode>00000</PostalCode>
                                <Nationality>SA</Nationality>
                            </Pax>
                            <Pax IdPax="2">
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
                                <Country>SA</Country>
                                <PostalCode>00000</PostalCode>
                                <Nationality>SA</Nationality>
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
                            <FlightItem ItemId="125188" Status="CA">
                                <Prices>
                                    <Price Type="S" Currency="SAR">
                                        <TotalFixAmounts Gross="849.44" Nett="849.44">
                                            <Service Amount="509.43" />
                                            <ServiceTaxes Included="false" Amount="340.01" />
                                        </TotalFixAmounts>
                                    </Price>
                                </Prices>
                                <CancellationPolicy CurrencyCode="SAR">
                                    <FirstDayCostCancellation Hour="23:50">2019-08-05</FirstDayCostCancellation>
                                    <Description>Si el vuelo esta emitido, tiene un 100% de gastos de cancelación. * Cancelando desde 08/07/2019 a las 00:00:00 hasta 05/08/2019 a las 23:50:00: 0 SARSi el vuelo esta emitido, tiene un 100% de gastos de cancelación. * Cancelando desde 05/08/2019 a las 23:50:00: 100.00 % gastos</Description>
                                    <PolicyRules>
                                        <Rule DateFrom="2019-07-08" DateFromHour="00:00" DateTo="2019-08-05" DateToHour="23:50" Type="R" FixedPrice="0" PercentPrice="0" Nights="0" ApplicationTypeNights="Average" />
                                        <Rule DateFrom="2019-08-05" DateFromHour="23:50" Type="R" FixedPrice="0" PercentPrice="100" Nights="0" ApplicationTypeNights="Average" />
                                    </PolicyRules>
                                </CancellationPolicy>
                                <Routes ValidatingCarrier="WY">
                                    <Route Origin="38638" Destination="39261">
                                        <Segments>
                                            <Segment DepartureAirport="DXB" ArrivalAirport="MCT" DepartureDate="2019-08-10T17:15:00" ArrivalDate="2019-08-10T18:30:00" OperatingAirline="WY" MarquetingAirline="WY" FlightNumber="610" Class="O" Cabin="Y" AirplaneType="788" FareBasis="OSEOWAE">
                                                <TechnicalStops />
                                            </Segment>
                                            <Segment DepartureAirport="MCT" ArrivalAirport="JED" DepartureDate="2019-08-10T21:35:00" ArrivalDate="2019-08-10T23:50:00" OperatingAirline="WY" MarquetingAirline="WY" FlightNumber="673" Class="O" Cabin="Y" AirplaneType="332" FareBasis="OSEOWAE">
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


# Other response

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <soap:Body>
        <CancelBookingResponse xmlns="http://www.juniper.es/webservice/2007/">
            <BookingRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-29T15:53:14.2148958+02:00" IntCode="7T3QcgbBQJKayizhuWIxhVVLw/OXndgLoNk2+Pkt7mQ=">
                <Errors>
                    <Error Text=" Cancellation is not possible" Code="CANCEL_NOT_POSSIBLE" />
                </Errors>
            </BookingRS>
        </CancelBookingResponse>
    </soap:Body>
</soap:Envelope>
```