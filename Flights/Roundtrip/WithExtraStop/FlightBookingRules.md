### Request
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns="http://www.juniper.es/webservice/2007/">
	<soapenv:Header/>
		<soapenv:Body>
			<FlightBookingRules>
				<FlightBookingRulesRQ Version="1.1" Language="es">
				<Login Email="user@mydomain.com" Password="pass"/>
					<FlightBookingRulesRequest>
						<FlightOption
						RatePlanCode="pR+Drc2veFAtxSETJRPPRxMSU0S+05he6M86pFU7TItH/vJd8W5itMWaHlsRgYOk8KIpooWqiz7lHZ/FsEb+bEThbOwJEFZh4ZR2foXPVbWYBI/Z7UDyz1T19d0liEnnVdqzSahTvDdTYA1RkxhF+I7ssVLC7I/p6oFOiXXsbAtDtvvLLvCXL4vcT4HFjr1kMmrjD/a//9zk59vYlm/ax7s39+vozTRintL0zNhkKXrWFNLy/Y1VCt7t7FTxcBsw1Fa2gUONK62Sen4NyqGQmaNnjpng1IOhfZvveJ5SLovEq5vBt3h2GnJ4XF32P3PaUhdo4i+MLkYW59ktxJ2MO/ZNmCKbmY2quEhTRyKh3uQYhDZloU/WUhmOngVeFwD/fiR2bfvuZXVbR2GudXE3UdNNHjUtGpFgsytHD5elukfteTKUvjWmw2iPO7Vad4YDgd5m0dOI/H90aJWq09cI3Nu45GB/TN8imJso6+BHsZ0n8EvWVTKBjyWB4iPdyKbsrCppFxYxSRNi5ojPwFzB0mWBlLw9BhQGaaliFQ0RD5DGH4wAQM8/npkazhI9DC/vbVHezeoDbHAt/qGYcoUFzO24aLaJHr7OlfFG5Irao+rDSczpwFfc5tUtcOh783jZsp3RKdBkfXuIzroNNXD5v7CrR1Dn6CXhnbb2JE2Zn7YcqtII/0eocM2oFcaoPxl8+0LWONuaMlUS5vqu1bOZVKvzrUhiVtZL27exv+89uFAvbkYcQCNdUhBspVWePy9kBPn7spvYDRPqFFF6TOSU1DTKdggL+yBhyeJqK3GFgCFSsnXSx0gSRU87SE4O8UkA9g9xKNKY/6DlbfpNR0IYx+jJz9WYCuf7q/rj6SAZeCIhgOF6BSmsYvWL05mOHx6vlekMA3HIvGKv7ABQ12/5qLgH/Hm4ktd7A7mldMbyLEWPbNYca0aBN2XgmAKFXH/7DiIYo7WZgN9bE87xdG+X8vAyxvuBqQrDkzICASESGELnyHYQ+mGONbpBy/8fU0p4mqMWbLOZ/8Sr1Z2L1ff+nKzb1gPBTtyWKSOGgIzCzg6ZdRj11NSUwUmfpONKqufmAmA/khzsctE3N4UbyiEnt6YOTlTGFNL+zoAjjxbd91yp1M9pQphdlrO6K7LuEwgt8ylteQ4tssvL/cR+kJyUIVQ9IxL5NoXnsWA3zLB91gRc59yEMPk0Baz5uaILqYGKqLvb8BRv+uskH69L2m9o7IMkTyP/h0xJEqwALFKxX+h6sgA4TIcC3DhoeE3je4/OnWDrPPqEPsdqMW6k5sinp/zDY5h2jdh5tY5KbyP/4JoHGBiKqaFM/46Z2uTgWLYHqKwOWHZcCfFpDcUFIOPppw=="/>
						</FlightBookingRulesRequest>
		      <AdvancedOptions>
                    <ShowBreakdownPrice>true</ShowBreakdownPrice>
                    <UseCurrency>USD</UseCurrency>
                </AdvancedOptions>
				</FlightBookingRulesRQ>
		</FlightBookingRules>
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
        <FlightBookingRulesResponse xmlns="http://www.juniper.es/webservice/2007/">
            <BookingRulesRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-28T15:31:07.9855476+02:00" IntCode="3PHzEHu9kVkLJAVE56xK6lMf+Sg5CbGY3UK2hpdeo70=">
                <Results>
                    <FlightResult Status="OK" Source="Amad" Direction="RoundTrip" LowCost="false">
                        <BookingCode ExpirationDate="2019-07-28T15:41:07.9855476+02:00">pR+Drc2veFAtxSETJRPPRxMSU0S+05he6M86pFU7TItH/vJd8W5itMWaHlsRgYOkrLKFwxeRkrRF9TNU+7XfF4t1t4tN7rxktDjKtrk8TNX0mOsuIUlB4wQpEw42KmRVz33zzhF7X5jdqUmu8glIhjw07iFWsjJ67QwE1B/v6Tp2bF9Ht7Mk7GYSW5n+XkVEy7mxy0WEkf28sKnQcdqQuS5BnEw5alG9/NEQgiRfRqCwZKs1U6ckI5EToVOMozuF9dm4eEALSlJzQ62u/ECGag+BEoe+5rmCGUSBdhW92G5THVsFCbr/aHov4sSWVIJ+7iUYxc6NkH6J2jKsmgkhZxJq7AIokoKzqT18vq69PEkJ53W2kXojQYsFobU7YYRw8lJKVNbygvDu9dG9wxfOz0Nqkflw2MXMY84c4pruZQ9JnRcTP5GeUaLZtAFgallHUyKdL6KxHCyF4QIxBUmLaGBk5HNsylNaIAu+KU63V3PWAjraZDBJHlxwfHQwkJAcYRGhRoC5SR0GmWQFAEc8XTbxfkoaWGwBh7XWimJtNabcZgqglQQUgJtObrNUE6EWxy5rco4MLbkdHyrgpy3y32KEC2qzbQ6pBaaC25a4hmpr2apixfw+Of/FmnmyIbrZG4+rkfnly14b3Ya0TU0BIHTvMXuWMYaiaDQHuok+Ndmzrq+tncZXmcrrAACJFUyN3VpHiqpNutuuDr5IZGecnuZx+4qxS6DtnklGlmCnODd//UJXzWOUdYFVuHmLOYMzoX1NtXr8SHG4StKbNdUy0OYXMEdhGFFhOC49IacNialU1/1m6Xjf8VtTvTAgp2rKxfy58HJWkoDIFvL6puNI9aVKJPlu8chrzLWmN3MUSAkvIfGfd0hBoa6S8XM+T6HOD35ON1Hg3uhYbB7j5h9ind1yeooUwBFn1oMiY5BUVJGaAslbDuEsAlPHDFVARxZJiliSWiN04gRsXAMIAYn6+Ke76VImaBYh9cWkDTZkAvhlJ++43xYaSo3rrHdsQYrUs9qw0p5r6pi9qAWBunWyCsFJI5ZTcEcOaSwPHkTb+KNMEtlIX7xa/uoBYdy3T6eqQQWft+AHvEsV8YslICeuL9WoZ5sDnt12wthHvnTFJLw77f4CPReUHL5k0jsdEwhqH1kv8LlW8weFHx07SgBTDyesVUcWV4ywntMvMLHhCUtW5ltxIbwGlz9ryV5tP6xbjdZmrY/WrdSJ99Cb1f2b5gafjz5omry2L6UdzzT6xWZy8t14EJlFhDiroUa/689oHo/SJ+hitS5hq8I/++URs3Maoy0ktTRElWZBedutyr0=</BookingCode>
                        <FlightRequiredFields>
                            <FlightBooking>
                                <Paxes>
                                    <Pax IdPax="1">
                                        <Name>Holder Name</Name>
                                        <Surname>Holder Surname</Surname>
                                        <Age>28</Age>
                                    </Pax>
                                    <Pax IdPax="2">
                                        <Name>Pax Name</Name>
                                        <Surname>Pax Surname</Surname>
                                        <Age>28</Age>
                                    </Pax>
                                </Paxes>
                                <Holder>
                                    <RelPax IdPax="1" />
                                </Holder>
                                <Elements>
                                    <FlightElement>
                                        <BookingCode>pR+Drc2veFAtxSETJRPPRxMSU0S+05he6M86pFU7TItH/vJd8W5itMWaHlsRgYOkrLKFwxeRkrRF9TNU+7XfF4t1t4tN7rxktDjKtrk8TNX0mOsuIUlB4wQpEw42KmRVz33zzhF7X5jdqUmu8glIhjw07iFWsjJ67QwE1B/v6Tp2bF9Ht7Mk7GYSW5n+XkVEy7mxy0WEkf28sKnQcdqQuS5BnEw5alG9/NEQgiRfRqCwZKs1U6ckI5EToVOMozuF9dm4eEALSlJzQ62u/ECGag+BEoe+5rmCGUSBdhW92G5THVsFCbr/aHov4sSWVIJ+7iUYxc6NkH6J2jKsmgkhZxJq7AIokoKzqT18vq69PEkJ53W2kXojQYsFobU7YYRw8lJKVNbygvDu9dG9wxfOz0Nqkflw2MXMY84c4pruZQ9JnRcTP5GeUaLZtAFgallHUyKdL6KxHCyF4QIxBUmLaGBk5HNsylNaIAu+KU63V3PWAjraZDBJHlxwfHQwkJAcYRGhRoC5SR0GmWQFAEc8XTbxfkoaWGwBh7XWimJtNabcZgqglQQUgJtObrNUE6EWxy5rco4MLbkdHyrgpy3y32KEC2qzbQ6pBaaC25a4hmpr2apixfw+Of/FmnmyIbrZG4+rkfnly14b3Ya0TU0BIHTvMXuWMYaiaDQHuok+Ndmzrq+tncZXmcrrAACJFUyN3VpHiqpNutuuDr5IZGecnuZx+4qxS6DtnklGlmCnODd//UJXzWOUdYFVuHmLOYMzoX1NtXr8SHG4StKbNdUy0OYXMEdhGFFhOC49IacNialU1/1m6Xjf8VtTvTAgp2rKxfy58HJWkoDIFvL6puNI9aVKJPlu8chrzLWmN3MUSAkvIfGfd0hBoa6S8XM+T6HOD35ON1Hg3uhYbB7j5h9ind1yeooUwBFn1oMiY5BUVJGaAslbDuEsAlPHDFVARxZJiliSWiN04gRsXAMIAYn6+Ke76VImaBYh9cWkDTZkAvhlJ++43xYaSo3rrHdsQYrUs9qw0p5r6pi9qAWBunWyCsFJI5ZTcEcOaSwPHkTb+KNMEtlIX7xa/uoBYdy3T6eqQQWft+AHvEsV8YslICeuL9WoZ5sDnt12wthHvnTFJLw77f4CPReUHL5k0jsdEwhqH1kv8LlW8weFHx07SgBTDyesVUcWV4ywntMvMLHhCUtW5ltxIbwGlz9ryV5tP6xbjdZmrY/WrdSJ99Cb1f2b5gafjz5omry2L6UdzzT6xWZy8t14EJlFhDiroUa/689oHo/SJ+hitS5hq8I/++URs3Maoy0ktTRElWZBedutyr0=</BookingCode>
                                        <RelPaxesDist>
                                            <RelPaxDist>
                                                <RelPaxes>
                                                    <RelPax IdPax="1" />
                                                    <RelPax IdPax="2" />
                                                </RelPaxes>
                                            </RelPaxDist>
                                        </RelPaxesDist>
                                    </FlightElement>
                                </Elements>
                            </FlightBooking>
                        </FlightRequiredFields>
                        <CancellationPolicy CurrencyCode="USD">
                            <FirstDayCostCancellation Hour="23:50">2019-07-29</FirstDayCostCancellation>
                            <Description>Si el vuelo esta emitido, tiene un 100% de gastos de cancelación. * Cancelando desde 28/07/2019 a las 00:00:00 hasta 29/07/2019 a las 23:50:00: 0 &amp;nbsp;USDSi el vuelo esta emitido, tiene un 100% de gastos de cancelación. * Cancelando desde 29/07/2019 a las 23:50:00: 100.00 % gastos</Description>
                            <PolicyRules>
                                <Rule DateFrom="2019-07-28" DateFromHour="00:00" DateTo="2019-07-29" DateToHour="23:50" Type="R" FixedPrice="0" PercentPrice="0" Nights="0" ApplicationTypeNights="Average" />
                                <Rule DateFrom="2019-07-29" DateFromHour="23:50" Type="R" FixedPrice="0" PercentPrice="100" Nights="0" ApplicationTypeNights="Average" />
                            </PolicyRules>
                        </CancellationPolicy>
                        <PriceInformation>
                            <Routes ValidatingCarrier="UX">
                                <Route Origin="40233" Destination="37786">
                                    <Segments>
                                        <Segment DepartureAirport="PMI" ArrivalAirport="MAD" DepartureDate="2019-10-16T21:10:00" ArrivalDate="2019-10-16T22:35:00" OperatingAirline="UX" MarquetingAirline="UX" FlightNumber="6096" JourneyDuration="P0DT1H25M0S" Class="Z" Cabin="Y" AirplaneType="73H" FareBasis="ZD1Y4L" />
                                    </Segments>
                                </Route>
                                <Route Origin="37786" Destination="40233">
                                    <Segments>
                                        <Segment DepartureAirport="MAD" ArrivalAirport="PMI" DepartureDate="2019-10-25T08:20:00" ArrivalDate="2019-10-25T09:45:00" OperatingAirline="UX" MarquetingAirline="UX" FlightNumber="6031" JourneyDuration="P0DT1H25M0S" Class="N" Cabin="Y" AirplaneType="E90" FareBasis="NDYY4L" />
                                    </Segments>
                                </Route>
                            </Routes>
                            <Prices>
                                <Price Type="S" Currency="USD">
                                    <TotalFixAmounts Gross="149.36" Nett="149.36">
                                        <Service Amount="82.4" />
                                        <ServiceTaxes Included="false" Amount="66.96" />
                                    </TotalFixAmounts>
                                    <Breakdown>
                                        <Concepts>
                                            <Concept Type="BAS" Name="Base Coste">
                                                <Items>
                                                    <Item Amount="41.2" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                                </Items>
                                            </Concept>
                                            <Concept Type="BAS" Name="Base Coste">
                                                <Items>
                                                    <Item Amount="41.2" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                                </Items>
                                            </Concept>
                                        </Concepts>
                                        <Taxes>
                                            <Tax Name="Tasas Others" Value="33.48" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                <TtaCodes>
                                                    <TtaCode>200</TtaCode>
                                                </TtaCodes>
                                                <Total Base="82.4" Amount="33.48" />
                                            </Tax>
                                            <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                <TtaCodes>
                                                    <TtaCode>200</TtaCode>
                                                </TtaCodes>
                                                <Total Base="82.4" Amount="0" />
                                            </Tax>
                                            <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                <TtaCodes>
                                                    <TtaCode>200</TtaCode>
                                                </TtaCodes>
                                                <Total Base="82.4" Amount="0" />
                                            </Tax>
                                            <Tax Name="Tasas Others" Value="33.48" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                <TtaCodes>
                                                    <TtaCode>201</TtaCode>
                                                </TtaCodes>
                                                <Total Base="82.4" Amount="33.48" />
                                            </Tax>
                                            <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                <TtaCodes>
                                                    <TtaCode>201</TtaCode>
                                                </TtaCodes>
                                                <Total Base="82.4" Amount="0" />
                                            </Tax>
                                            <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                <TtaCodes>
                                                    <TtaCode>201</TtaCode>
                                                </TtaCodes>
                                                <Total Base="82.4" Amount="0" />
                                            </Tax>
                                        </Taxes>
                                    </Breakdown>
                                </Price>
                            </Prices>
                        </PriceInformation>
                        <OptionalElements />
                    </FlightResult>
                </Results>
            </BookingRulesRS>
        </FlightBookingRulesResponse>
    </soap:Body>
</soap:Envelope>
```