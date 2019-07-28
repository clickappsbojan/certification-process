### Request
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns="http://www.juniper.es/webservice/2007/">
    <soapenv:Header/>
        <soapenv:Body>
            <FlightBooking>
                <FlightBookingRQ Version="1.1" Language="es">
                    <Login Email="xxxxxx" Password="xxxxxxxx"/>
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
	                 
                    </Paxes>
                    <Holder>
                        <RelPax IdPax="1"/>
                    </Holder>
                    <Elements>
                        <FlightElement ElementId="1">
                            <BookingCode>pR+Drc2veFAtxSETJRPPRxMSU0S+05he6M86pFU7TItH/vJd8W5itMWaHlsRgYOkrLKFwxeRkrRF9TNU+7XfF4t1t4tN7rxktDjKtrk8TNX0mOsuIUlB4wQpEw42KmRVz33zzhF7X5jdqUmu8glIhjw07iFWsjJ67QwE1B/v6Tp2bF9Ht7Mk7GYSW5n+XkVEy7mxy0WEkf28sKnQcdqQuS5BnEw5alG9/NEQgiRfRqCwZKs1U6ckI5EToVOMozuF9dm4eEALSlJzQ62u/ECGag+BEoe+5rmCGUSBdhW92G5THVsFCbr/aHov4sSWVIJ+7iUYxc6NkH6J2jKsmgkhZxJq7AIokoKzqT18vq69PEkJ53W2kXojQYsFobU7YYRw8lJKVNbygvDu9dG9wxfOz0Nqkflw2MXMY84c4pruZQ9JnRcTP5GeUaLZtAFgallHUyKdL6KxHCyF4QIxBUmLaGBk5HNsylNaIAu+KU63V3PWAjraZDBJHlxwfHQwkJAcYRGhRoC5SR0GmWQFAEc8XTbxfkoaWGwBh7XWimJtNabcZgqglQQUgJtObrNUE6EWxy5rco4MLbkdHyrgpy3y32KEC2qzbQ6pBaaC25a4hmpr2apixfw+Of/FmnmyIbrZG4+rkfnly14b3Ya0TU0BIHTvMXuWMYaiaDQHuok+Ndmzrq+tncZXmcrrAACJFUyN3VpHiqpNutuuDr5IZGecnuZx+4qxS6DtnklGlmCnODd//UJXzWOUdYFVuHmLOYMzoX1NtXr8SHG4StKbNdUy0OYXMEdhGFFhOC49IacNialU1/1m6Xjf8VtTvTAgp2rKxfy58HJWkoDIFvL6puNI9aVKJPlu8chrzLWmN3MUSAkvIfGfd0hBoa6S8XM+T6HOD35ON1Hg3uhYbB7j5h9ind1yeooUwBFn1oMiY5BUVJGaAslbDuEsAlPHDFVARxZJiliSWiN04gRsXAMIAYn6+Ke76VImaBYh9cWkDTZkAvhlJ++43xYaSo3rrHdsQYrUs9qw0p5r6pi9qAWBunWyCsFJI5ZTcEcOaSwPHkTb+KNMEtlIX7xa/uoBYdy3T6eqQQWft+AHvEsV8YslICeuL9WoZ5sDnt12wthHvnTFJLw77f4CPReUHL5k0jsdEwhqH1kv8LlW8weFHx07SgBTDyesVUcWV4ywntMvMLHhCUtW5ltxIbwGlz9ryV5tP6xbjdZmrY/WrdSJ99Cb1f2b5gafjz5omry2L6UdzzT6xWZy8t14EJlFhDiroUa/689oHo/SJ+hitS5hq8I/++URs3Maoy0ktTRElWZBedutyr0=</BookingCode>
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
                                    <PriceRange Minimum="149.36" Maximum="149.36" Currency="USD"/>
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
            <BookingRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-28T15:33:15.2753789+02:00" IntCode="jPtxKMX9DraPNrU5OAm3duXKvpqQdgKo92gjgrepb4c=">
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
                                        <Breakdown>
                                            <Concepts>
                                                <Concept Type="BAS" Name="Base Coste">
                                                    <Items>
                                                        <Item Amount="37" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                                    </Items>
                                                </Concept>
                                                <Concept Type="BAS" Name="Base Coste">
                                                    <Items>
                                                        <Item Amount="37" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                                    </Items>
                                                </Concept>
                                            </Concepts>
                                            <Taxes>
                                                <Tax Name="Tasas Others" Value="30.07" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                    <TtaCodes>
                                                        <TtaCode>200</TtaCode>
                                                    </TtaCodes>
                                                    <Total Base="74" Amount="30.07" />
                                                </Tax>
                                                <Tax Name="Tasas Others" Value="30.07" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                    <TtaCodes>
                                                        <TtaCode>201</TtaCode>
                                                    </TtaCodes>
                                                    <Total Base="74" Amount="30.07" />
                                                </Tax>
                                            </Taxes>
                                        </Breakdown>
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
        </FlightBookingResponse>
    </soap:Body>
</soap:Envelope>
```