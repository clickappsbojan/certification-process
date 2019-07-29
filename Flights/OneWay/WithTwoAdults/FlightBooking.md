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
		                 <Document Type="PAS" ExpirationDate="2024-07-04T00:00:00+02:00">1234564789</Document>
		                    <Name>Passenger name</Name>
		                    <Surname>Passenger surname</Surname>
		                    <Age>28</Age>
		                    <BornDate>1989-07-28</BornDate>
		                    <Address>Passenger address</Address>
		                    <City>Passegner city</City>
		                    <Country>Passenger country</Country>
		                    <PostalCode>00000</PostalCode>
		                    <Nationality>Passenger nationality</Nationality>
	                  </Pax>
                    </Paxes>
                    <Holder>
                        <RelPax IdPax="1"/>
                    </Holder>
                    <Elements>
                        <FlightElement ElementId="1">
                            <BookingCode>lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfy2CJXsMlg8AZ8QWudXdQvRBXIcrhVIwGOyQMhvip74kCxvpvE0RqO0v36+GaCG0cEtDB9RfX/n4K5LfeySA8wJ5fU9IZIK/Ndsa55LyOz7Y94lanmpdJXEI4dHzpIdQXSRPllWAwWTXwvq4nG4bDiCWa5ohpQQRLjjSGC7BVQb7nrohH7mcXsHkEKawlseyuVHHBoIwggS+AQlXl0gsoevkJ+bAjVmNasKI3+DiJJWK3bFOgDoqnhbYElTmTrZseePeM2r4vM24uO5UEAw2HFuOYZIHv73X/fVUHrs2Xg+cA1oXKe70W9RGiqmPYTfGVuVxurEkV7GEXl8mcVsU2Dtzqs1wnqJWjo8wkI4SeMxA46O7706BYvaEpfnTByTH4wPZhI+jDzRA+15tX61zXu6YDsKy/SFdZu5kCScqQHbhqpQwwKpwcqgC1TYSFcraDKLbjqa2uCLbiurS5syrtQ0iCP2YlRIUKpo0GJELy47i7Uvu1RcHl9ugscOCpvOVPGOeTNcs8MDSc1ydKxrt+4EyrNlKuNpTuqkZI3AvS2WEBh5e3DvsnW+c7XBgsTY9TyWlT/5lGk/99VT2EmhkZDTm00bi4ZEwULrHlHWEevd6mFTS4OdWVYXGIF2Sa0Le9z08CH6j0wP5HDF4w0HXBo9Hd7UEzSNqAol7ruk2Pi+B77y7myzm5VwHD0ss/obz8QPVEJT2v3iY+GSF9PUAqteRqPJNo1rX9z22NzEhM556myiozaWugHjrrl9KXm7GK9ySCfptuJJWxkZW6IhKbrbWO+IDwT7iYF+F87eWDfLWMYXx2pf6SCOMis9K4FmdvV/adWgnzJdkCHe0fBCfc9OZ993qbEi3MjjPIVTaink/WxIMPpvB4D8IQSw3NKkjmsOTE4mVrCONpzxobqhYLZXLthQ37Atk1+bubcAaZaTFf8hwyIny1tf1qDyq92cdkKpYpMEkKVO1P3ower9UklGjkTVjsTdNohzBAdLVK3t/68p0KBbVk1otqAmjLOQLjSHSRh7PUGP3144Wr7mPvcuaVPA0hP5xx/y3Ae2pl8pUt6u5CSX1yITf/PSkHVTgEeMtlm0EvqSda8TsTDxoZKcBZQiH7rZ9bGZavDcoVcREH+pIEyGrqY6ZbibvpjJBPalnVkucrW3vvK8SPbo5uKj5Rqqh3ZzPV8S6FYK1P46ifxpt7g2sk2yo1NiqS5gnfNzuQ4FSWGAtCdoOQQg4NihmBUuDgX2mPH7nef3w7mU8Pr2mwUHR4oXaUMlzGlzIGo=</BookingCode>
                    <RelPaxesDist>
                        <RelPaxDist>
                            <RelPaxes>
                                <RelPax IdPax="1" />
                                <RelPax IdPax="2" />
                            </RelPaxes>
                        </RelPaxDist>
                    </RelPaxesDist>
                            <FlightBookingInfo Start="2014-01-08" End="2015-01-08">
                                <Price>
                                    <PriceRange Minimum="11827.4" Maximum="11827.4" Currency="USD"/>
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
            <BookingRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-29T11:06:46.8253937+02:00" IntCode="PGXKsY0YCmnXm1W3o4vRRGDGz4H3ndl3oydIB0HhCQo=">
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
                                        <Breakdown>
                                            <Concepts>
                                                <Concept Type="BAS" Name="Base Coste">
                                                    <Items>
                                                        <Item Amount="6156" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                                    </Items>
                                                </Concept>
                                                <Concept Type="BAS" Name="Base Coste">
                                                    <Items>
                                                        <Item Amount="6156" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                                    </Items>
                                                </Concept>
                                            </Concepts>
                                            <Taxes>
                                                <Tax Name="Tasas Others" Value="582.15" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                    <TtaCodes>
                                                        <TtaCode>200</TtaCode>
                                                    </TtaCodes>
                                                    <Total Base="12312" Amount="582.15" />
                                                </Tax>
                                                <Tax Name="Tasas Qs" Value="13" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                    <TtaCodes>
                                                        <TtaCode>200</TtaCode>
                                                    </TtaCodes>
                                                    <Total Base="12312" Amount="13" />
                                                </Tax>
                                                <Tax Name="Tasas Others" Value="582.15" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                    <TtaCodes>
                                                        <TtaCode>201</TtaCode>
                                                    </TtaCodes>
                                                    <Total Base="12312" Amount="582.15" />
                                                </Tax>
                                                <Tax Name="Tasas Qs" Value="13" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                    <TtaCodes>
                                                        <TtaCode>201</TtaCode>
                                                    </TtaCodes>
                                                    <Total Base="12312" Amount="13" />
                                                </Tax>
                                            </Taxes>
                                        </Breakdown>
                                    </Price>
                                </Prices>
                                <CancellationPolicy CurrencyCode="EUR">
                                    <FirstDayCostCancellation Hour="23:50">2019-08-26</FirstDayCostCancellation>
                                    <Description>If the flight has been issued, all cancellations will incur a 100% charge. * Cancelling from 29/07/2019 at 00:00:00 to 26/08/2019 at 23:50:00: 0 &amp;euro;If the flight has been issued, all cancellations will incur a 100% charge. * Cancelling from 26/08/2019 at 23:50:00: 100.00 % of expenses</Description>
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
        </FlightBookingResponse>
    </soap:Body>
</soap:Envelope>

```