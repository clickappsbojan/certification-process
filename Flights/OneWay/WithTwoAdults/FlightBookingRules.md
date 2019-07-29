### Request
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns="http://www.juniper.es/webservice/2007/">
	<soapenv:Header/>
		<soapenv:Body>
			<FlightBookingRules>
				<FlightBookingRulesRQ Version="1.1" Language="es">
				<Login Email="user@mydomain.com" Password="pass"/>
					<FlightBookingRulesRequest>
						
						<FlightOption RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfy2CJXsMlg8AZ8QWudXdQvR9kB8RTt8XqUXB6MVcS+Yk5gowgUrx96qgPtoA5OYl9gIMY+VbYEsomATRIAmxx1nlQTZMvoQORFisnHWnf4XHiU3CjE4BWKVgDVL/cVoVdyoCbzZNPYTK3Wx4Kx1EGVueDOtqN6EtN2Y2sYP2ZNFQFIqkxu8onxgxCK7T7X3aSbha1DNyReqxuUpdCt6VOW37TZUXncuEHMQdOuY5/nWMndup1cedBe3hNBwz11mgx46twPpW5b7S9po3ZV0WFToKdjfi0LQ5rFGPBUqYoRtdBdtb7DSzPPjdu6OL6e/uG0qm9zRFEAzP+2fMzQhGWUNINCypTjlRNvW3EX4JRnx7mEyFfYF+Arpvs3axQq2upsyuWg/t5AmOKKN9f/R6xMTvUA+Oq8WXo67evNTpPjDuOaLUB56dywxrTkjc0GRCZLkiOECcJ6CTNqeksU2LqwfCKvTCxHc7tFPLwwFdQtwRRuyv+u27iztDnPaUa8lYT0qqqpThUoKrNoW6cz0bpwaR7x1E04Jj5CSNE/wLZ7vJIsQO8/AA8qmspeIjqFu4BLXHP4hsy48S1ufPyZAETCI/oYezH4TVgfL/nup+nJgu3DRExLKs4r8HC0w7g5+QJ3dOZTVuH9P3d9nGzNyfbqbpRCoqeXkmhlAcvrqy/5TCrx9frIbUGPztkBCI0KYxJGpZ6h45pemc6HYPDK/xU48P6kLODGTATCbqFkzB299r9w+xhQRmAVWjC7CjNO1LoHMTPe6fG5uf+q+Kspgq30NM8TP/sQw9CLQeAfMG5NG7bmb003Z3lDj5JHtx2oMSaqkTXTDq1AdqzJGgiFtgkwLnTJbg9Pj9Aq0pT3ESX55ktcvBLGJMWx7rKz0h1ohiyM8RL34phd27JXyz2ARGabqBV0bQIy1cpMVH0LJtvnjSpXsFakzpTGQlpHBZ/6Ij84KuVcioKgNM2onhmMa31Wnvx+a6lKg45kn39J7aQLjEP5SQmIx0mHCWTN89zGHNXKIqoJUzGRkfzZWPqqSuhhs7axD1ezo2nLf8aYjFWD4AadLNUAVXKSIZYR54w8CC6OOeahWGjRhR7nKoP9JWyRHig92PumeSVUBbIoV5xPlaIsSbMy3EqWF/3gJCPSWr2FNmEPYbYdAG9WB30k5q3mI9cUqIzb3A4RSYHHj8MU/f5sPhT5xoTq3HuHST4lE8nMagL5Rg7wKaa0e9pdi2QIrQow7e6gH5BoeOFnBOOonr5RkT1YBi50MVgZ3bbUNt39mutrwh5WuVxnMS/vs3MPngSWnCOvxQiTQz++abtqVxA=="/>
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
            <BookingRulesRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-29T15:45:08.1527358+02:00" IntCode="eWnS3/atN70/cG3DnM5kp/WIFq2KEmkIMaDstpfP/3g=">
                <Results>
                    <FlightResult Status="OK" Source="Amad" Direction="Outbound" LowCost="false">
                        <BookingCode ExpirationDate="2019-07-29T15:55:08.1371118+02:00">lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfy2CJXsMlg8AZ8QWudXdQvRBXIcrhVIwGOyQMhvip74kCxvpvE0RqO0v36+GaCG0cEtDB9RfX/n4K5LfeySA8wJ5fU9IZIK/Ndsa55LyOz7Y94lanmpdJXEI4dHzpIdQXSRPllWAwWTXwvq4nG4bDiCWa5ohpQQRLjjSGC7BVQb7nrohH7mcXsHkEKawlseyuVHHBoIwggS+AQlXl0gsoevkJ+bAjVmNasKI3+DiJJWK3bFOgDoqnhbYElTmTrZseePeM2r4vM24uO5UEAw2HFuOYZIHv73X/fVUHrs2Xg+cA1oXKe70W9RGiqmPYTfGVuVxurEkV7GEXl8mcVsU2Dtzqs1wnqJWjo8wkI4SeMxA46O7706BYvaEpfnTByTH4wPZhI+jDzRA+15tX61zXu6YDsKy/SFdZu5kCScqQHbhqpQwwKpwcqgC1TYSFcraDKLbjqa2uCLbiurS5syrtQ0iCP2YlRIUKpo0GJELy47i7Uvu1RcHl9ugscOCpvOVPGOeTNcs8MDSc1ydKxrt+4EyrNlKuNpTuqkZI3AvS2WEBh5e3DvsnW+c7XBgsTY9TyWlT/5lGk/99VT2EmhkZDTm00bi4ZEwULrHlHWEevd6mFTS4OdWVYXGIF2Sa0Le9z08CH6j0wP5HDF4w0HXBo9Hd7UEzSNqAol7ruk2Pi+B77y7myzm5VwHD0ss/obz8QPVEJT2v3iY+GSF9PUAqteRqPJNo1rX9z22NzEhM556myiozaWugHjrrl9KXm7GK9ySCfptuJJWxkZW6IhKbrbWO+IDwT7iYF+F87eWDfLWMYXx2pf6SCOMis9K4FmdvV/adWgnzJdkCHe0fBCfc9OZ993qbEi3MjjPIVTaink/WxIMPpvB4D8IQSw3NKkjmsOTE4mVrCONpzxobqhYLZXLthQ37Atk1+bubcAaZaTFf8hwyIny1tf1qDyq92cdkKpYpMEkKVO1P3ower9UklGjkTVjsTdNohzBAdLVK3t/68p0KBbVk1otqAmjLOQLjSHSRh7PUGP3144Wr7mPvcuaVPA0hP5xx/y3Ae2pl8pUt6u5CSX1yITf/PSkHVTgEeMtlm0EvqSda8TsTDxoZKcBZQiH7rZ9bGZavDcoVcREH+pIEyGrqY6ZbibvpjJBPalnVkucrW3vvK8SPbo5uKj5Rqqh3ZzPV8S6FYK1P46ifxpt7g2sk2yo1NiqS5gnfNzuQ4FSWGAtCdoOQQg4NihmBUuDgX2mPH7nef3w7mU8Pr2mwUHR4oXaUMlzGlzIGo=</BookingCode>
                        <FlightRequiredFields>
                            <FlightBooking>
                                <Paxes>
                                    <Pax IdPax="1">
                                        <Document Type="PAS">Pax Document Number</Document>
                                        <Name>Holder Name</Name>
                                        <Surname>Holder Surname</Surname>
                                        <Age>28</Age>
                                        <BornDate>1989-07-29</BornDate>
                                    </Pax>
                                    <Pax IdPax="2">
                                        <Document Type="PAS">Pax Document Number</Document>
                                        <Name>Pax Name</Name>
                                        <Surname>Pax Surname</Surname>
                                        <Age>28</Age>
                                        <BornDate>1989-07-29</BornDate>
                                    </Pax>
                                </Paxes>
                                <Holder>
                                    <RelPax IdPax="1" />
                                </Holder>
                                <Elements>
                                    <FlightElement>
                                        <BookingCode>lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfy2CJXsMlg8AZ8QWudXdQvRBXIcrhVIwGOyQMhvip74kCxvpvE0RqO0v36+GaCG0cEtDB9RfX/n4K5LfeySA8wJ5fU9IZIK/Ndsa55LyOz7Y94lanmpdJXEI4dHzpIdQXSRPllWAwWTXwvq4nG4bDiCWa5ohpQQRLjjSGC7BVQb7nrohH7mcXsHkEKawlseyuVHHBoIwggS+AQlXl0gsoevkJ+bAjVmNasKI3+DiJJWK3bFOgDoqnhbYElTmTrZseePeM2r4vM24uO5UEAw2HFuOYZIHv73X/fVUHrs2Xg+cA1oXKe70W9RGiqmPYTfGVuVxurEkV7GEXl8mcVsU2Dtzqs1wnqJWjo8wkI4SeMxA46O7706BYvaEpfnTByTH4wPZhI+jDzRA+15tX61zXu6YDsKy/SFdZu5kCScqQHbhqpQwwKpwcqgC1TYSFcraDKLbjqa2uCLbiurS5syrtQ0iCP2YlRIUKpo0GJELy47i7Uvu1RcHl9ugscOCpvOVPGOeTNcs8MDSc1ydKxrt+4EyrNlKuNpTuqkZI3AvS2WEBh5e3DvsnW+c7XBgsTY9TyWlT/5lGk/99VT2EmhkZDTm00bi4ZEwULrHlHWEevd6mFTS4OdWVYXGIF2Sa0Le9z08CH6j0wP5HDF4w0HXBo9Hd7UEzSNqAol7ruk2Pi+B77y7myzm5VwHD0ss/obz8QPVEJT2v3iY+GSF9PUAqteRqPJNo1rX9z22NzEhM556myiozaWugHjrrl9KXm7GK9ySCfptuJJWxkZW6IhKbrbWO+IDwT7iYF+F87eWDfLWMYXx2pf6SCOMis9K4FmdvV/adWgnzJdkCHe0fBCfc9OZ993qbEi3MjjPIVTaink/WxIMPpvB4D8IQSw3NKkjmsOTE4mVrCONpzxobqhYLZXLthQ37Atk1+bubcAaZaTFf8hwyIny1tf1qDyq92cdkKpYpMEkKVO1P3ower9UklGjkTVjsTdNohzBAdLVK3t/68p0KBbVk1otqAmjLOQLjSHSRh7PUGP3144Wr7mPvcuaVPA0hP5xx/y3Ae2pl8pUt6u5CSX1yITf/PSkHVTgEeMtlm0EvqSda8TsTDxoZKcBZQiH7rZ9bGZavDcoVcREH+pIEyGrqY6ZbibvpjJBPalnVkucrW3vvK8SPbo5uKj5Rqqh3ZzPV8S6FYK1P46ifxpt7g2sk2yo1NiqS5gnfNzuQ4FSWGAtCdoOQQg4NihmBUuDgX2mPH7nef3w7mU8Pr2mwUHR4oXaUMlzGlzIGo=</BookingCode>
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
                            <FirstDayCostCancellation Hour="23:50">2019-10-16</FirstDayCostCancellation>
                            <Description>Si el vuelo esta emitido, tiene un 100% de gastos de cancelación. * Cancelando desde 29/07/2019 a las 00:00:00 hasta 16/10/2019 a las 23:50:00: 0 &amp;nbsp;USDSi el vuelo esta emitido, tiene un 100% de gastos de cancelación. * Cancelando desde 16/10/2019 a las 23:50:00: 100.00 % gastos</Description>
                            <PolicyRules>
                                <Rule DateFrom="2019-07-29" DateFromHour="00:00" DateTo="2019-10-16" DateToHour="23:50" Type="R" FixedPrice="0" PercentPrice="0" Nights="0" ApplicationTypeNights="Average" />
                                <Rule DateFrom="2019-10-16" DateFromHour="23:50" Type="R" FixedPrice="0" PercentPrice="100" Nights="0" ApplicationTypeNights="Average" />
                            </PolicyRules>
                        </CancellationPolicy>
                        <PriceInformation>
                            <Routes ValidatingCarrier="UX">
                                <Route Origin="39681" Destination="37786">
                                    <Segments>
                                        <Segment DepartureAirport="MCO" ArrivalAirport="JFK" DepartureDate="2019-10-16T11:57:00" ArrivalDate="2019-10-16T14:30:00" OperatingAirline="DL" MarquetingAirline="UX" FlightNumber="3394" JourneyDuration="P0DT15H18M0S" Class="J" Cabin="C" AirplaneType="321" FareBasis="JYYOAE" />
                                        <Segment DepartureAirport="JFK" ArrivalAirport="MAD" DepartureDate="2019-10-16T19:38:00" ArrivalDate="2019-10-17T09:15:00" OperatingAirline="DL" MarquetingAirline="UX" FlightNumber="3392" JourneyDuration="P0DT15H18M0S" Class="J" Cabin="C" AirplaneType="764" FareBasis="JYYOAE" />
                                    </Segments>
                                </Route>
                            </Routes>
                            <Prices>
                                <Price Type="S" Currency="USD">
                                    <TotalFixAmounts Gross="11827.4" Nett="11827.4">
                                        <Service Amount="10675.24" />
                                        <ServiceTaxes Included="false" Amount="1152.16" />
                                    </TotalFixAmounts>
                                    <Breakdown>
                                        <Concepts>
                                            <Concept Type="BAS" Name="Base Coste">
                                                <Items>
                                                    <Item Amount="5337.62" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                                </Items>
                                            </Concept>
                                            <Concept Type="BAS" Name="Base Coste">
                                                <Items>
                                                    <Item Amount="5337.62" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                                </Items>
                                            </Concept>
                                        </Concepts>
                                        <Taxes>
                                            <Tax Name="Tasas Others" Value="576.08" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                <TtaCodes>
                                                    <TtaCode>200</TtaCode>
                                                </TtaCodes>
                                                <Total Base="10675.24" Amount="576.08" />
                                            </Tax>
                                            <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                <TtaCodes>
                                                    <TtaCode>200</TtaCode>
                                                </TtaCodes>
                                                <Total Base="10675.24" Amount="0" />
                                            </Tax>
                                            <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                <TtaCodes>
                                                    <TtaCode>200</TtaCode>
                                                </TtaCodes>
                                                <Total Base="10675.24" Amount="0" />
                                            </Tax>
                                            <Tax Name="Tasas Others" Value="576.08" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                <TtaCodes>
                                                    <TtaCode>201</TtaCode>
                                                </TtaCodes>
                                                <Total Base="10675.24" Amount="576.08" />
                                            </Tax>
                                            <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                <TtaCodes>
                                                    <TtaCode>201</TtaCode>
                                                </TtaCodes>
                                                <Total Base="10675.24" Amount="0" />
                                            </Tax>
                                            <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                <TtaCodes>
                                                    <TtaCode>201</TtaCode>
                                                </TtaCodes>
                                                <Total Base="10675.24" Amount="0" />
                                            </Tax>
                                        </Taxes>
                                    </Breakdown>
                                </Price>
                            </Prices>
                        </PriceInformation>
                        <OptionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </OptionalElements>
                    </FlightResult>
                </Results>
            </BookingRulesRS>
        </FlightBookingRulesResponse>
    </soap:Body>
</soap:Envelope>
```