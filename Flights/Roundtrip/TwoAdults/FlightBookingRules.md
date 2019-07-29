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
						RatePlanCode="LF6j9ndyo/zlz9tkRLu5T4vcqg4Y3XWeGauWGUmxxJy33kAWihQpwFONCEgQgZ8j3MYnbZCiHJVG3tYrqJx3gJshoeNGijCN4wKm8yPI+Atx2j1gmfEyA+u+xJkFUx6mv3EDM08fGg58yKNPSbfeXTIMMqH2NLlqJkZxNAWnGTz9J7WLZr6qzvfLRspkFdBYTyVc/ByVCezR4T5xbJgVJYXnjtRdXaaGh6J2QmbM+E4csFmmrbSTBdyaANDpcjU8/qyJwZf10lC1VFBacKkaUfRFYb7aXiZggMKURER7L54WUcpq021IAq9nnzIKYCsavyZBfhttJOW1igjSyg5kOoUTiRUFbInVonCXQb9bkM+jjPtH8K9CMvLFicHv6ZBpmyhUtNzeRddhQRxWeNY1YlQUFD1wq4dTWZU1UJq8LI9qfQHXt2xyrE7b6noyT4ZpE6/qjRUwlZHcGo5BQfuNTzl56pz+KcweBfYjbHm1cj7JN53qJiMBQSMrcPFT9dZiusa1Z/4C2hpw+j5UmprIT8AROpr2iRz0um4SbwdFkIZPLSu0dO5WvaYPAJK1X0H3d9m2R9KRFwjxOgf+7dwnjEbJdQxTUHXlN/kXt3Y0x0KwQjyo5Sw0yOXZXqzDoKI40bEr+aMqh/z1IHjS6xyDmLTafUoR/oO6yyl1lWGCU5vIkV8Uyfai6BgZEVk++43pn9Sc0LXq28/kiHVyb0ZedhHgSEqT3K0at+pSChQQ8HPQyfRoctdqO/yxm2Mbpgu/6VsAlH7uFfraIxO7L27A7/J7aHKkeRGIJODNWbyzB39dP0xTLFnDaGff5XeRrp2/pm2v+zj6i7t9eEIo9dI3wMrA4zM76z05Y30rhy6QymalQk0bEdtos82IelPQ82lh/R669cN3NFX1buX+KMFFbroWE6yVc8Zy/FnCgFzFfwvXhgvi02HkRt5ifLFA6z+5I8JTzafgzoVY/uAjCol9hg=="/>
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
            <BookingRulesRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-28T11:04:54.6908834+02:00" IntCode="3TcqBkWJhWde1j6Wm6s7V9yhe3Xf7ZPaJA8vx+ISrTQ=">
                <Results>
                    <FlightResult Status="OK" Source="ChV2" Direction="Outbound" LowCost="false">
                        <BookingCode ExpirationDate="2019-07-28T11:14:54.6908834+02:00">LF6j9ndyo/zlz9tkRLu5T4vcqg4Y3XWeGauWGUmxxJy33kAWihQpwFONCEgQgZ8j3MYnbZCiHJVG3tYrqJx3gAyIPsnY+DOhhGz7Ik+1nzThEw3mA6A87A/RmDhBHyqqzbpboirrnvwk+SWM5D/sF8MGq9HMitejzPj0cMOuzAYqXPpPUbUqXPL3khsczbISn/h7xx0P+mQAdvGtPr4US6Pz76Ru5vFqbbN+A0Pta8AAvGKtdmDm73DKZvCeVeGoP+nPYM6gfd3BJK1AS4oC+TXnT2EYHHBF1WQkkjKGe8YcRhBLykdY9wBjR+6dm/mZXNLzzwEPDtlJaY8CkVNNQNkiIM8/ewEtI79RGogoO63iPAu70UEMtXUO7atThFK09SBoaiBwOI+DC2wvEWPWk3BHgEOxxJ4f+8HyzVESs9yN7RSgJUmJYu/jRwnbmBOPzbLmZs0doXRfowx1T8D0kd3yM1Iys+2MRMoJS8iOCiFU93IGldQwlYDh1tFRR3OBHqrw4ALkcNqU2x29CqTWLxGLXDod9H9iNPPPL2H708d8x2MTYhGOyOeib50BVWd8pbstvyJunaYgOO0oSAcjE2lVCwhpiR/835mKp36Gbi3EzAirFI4ptBb1CUkPyAJqxHUFiGbLGUfT0IB67G59HJXmAyLWuEHgi53IFKiUBqe8slmTkGaf8SKjHxL8CFWDhRDfaBX6pS2se6FEINNP4DP0V0nrqSQfNoUjUZQM2LKe5E110D70yPuCnoeKUppcmDiETigODi5PcCFywoT4E5f9x7AjpVu8GDifDIGaLAiLI7/W0rLK8wvtgiLpojBrDR/q8A37eJdPa+1WHQCkDJeyv9KUSxtAqj/0sA51dlU9V2OnT7FYIGM3iV53E9Ndm5nK5vK9jTmQnKWTIGDWQ/F+efr7aKpOpjKvVyD1JS/KLeRax4Wwy8hUQeHtPH+Mj6dbPQrmf/Jk4SpwGSNlVQ==</BookingCode>
                        <FlightRequiredFields>
                            <FlightBooking>
                                <Paxes>
                                    <Pax IdPax="1">
                                        <Name>Holder Name</Name>
                                        <Surname>Holder Surname</Surname>
                                        <Age>28</Age>
                                        <BornDate>1989-07-28</BornDate>
                                        <Address>Passenger address</Address>
                                        <City>Passegner city</City>
                                        <Country>Passenger country</Country>
                                        <PostalCode>Passenger postal code</PostalCode>
                                        <Nationality>Passenger nationality</Nationality>
                                    </Pax>
                                    <Pax IdPax="2">
                                        <Name>Passenger name</Name>
                                        <Surname>Passenger surname</Surname>
                                        <Age>28</Age>
                                        <BornDate>1989-07-28</BornDate>
                                        <Address>Passenger address</Address>
                                        <City>Passegner city</City>
                                        <Country>Passenger country</Country>
                                        <PostalCode>Passenger postal code</PostalCode>
                                        <Nationality>Passenger nationality</Nationality>
                                    </Pax>
                                </Paxes>
                                <Holder>
                                    <RelPax IdPax="1" />
                                </Holder>
                                <Elements>
                                    <FlightElement>
                                        <BookingCode>LF6j9ndyo/zlz9tkRLu5T4vcqg4Y3XWeGauWGUmxxJy33kAWihQpwFONCEgQgZ8j3MYnbZCiHJVG3tYrqJx3gAyIPsnY+DOhhGz7Ik+1nzThEw3mA6A87A/RmDhBHyqqzbpboirrnvwk+SWM5D/sF8MGq9HMitejzPj0cMOuzAYqXPpPUbUqXPL3khsczbISn/h7xx0P+mQAdvGtPr4US6Pz76Ru5vFqbbN+A0Pta8AAvGKtdmDm73DKZvCeVeGoP+nPYM6gfd3BJK1AS4oC+TXnT2EYHHBF1WQkkjKGe8YcRhBLykdY9wBjR+6dm/mZXNLzzwEPDtlJaY8CkVNNQNkiIM8/ewEtI79RGogoO63iPAu70UEMtXUO7atThFK09SBoaiBwOI+DC2wvEWPWk3BHgEOxxJ4f+8HyzVESs9yN7RSgJUmJYu/jRwnbmBOPzbLmZs0doXRfowx1T8D0kd3yM1Iys+2MRMoJS8iOCiFU93IGldQwlYDh1tFRR3OBHqrw4ALkcNqU2x29CqTWLxGLXDod9H9iNPPPL2H708d8x2MTYhGOyOeib50BVWd8pbstvyJunaYgOO0oSAcjE2lVCwhpiR/835mKp36Gbi3EzAirFI4ptBb1CUkPyAJqxHUFiGbLGUfT0IB67G59HJXmAyLWuEHgi53IFKiUBqe8slmTkGaf8SKjHxL8CFWDhRDfaBX6pS2se6FEINNP4DP0V0nrqSQfNoUjUZQM2LKe5E110D70yPuCnoeKUppcmDiETigODi5PcCFywoT4E5f9x7AjpVu8GDifDIGaLAiLI7/W0rLK8wvtgiLpojBrDR/q8A37eJdPa+1WHQCkDJeyv9KUSxtAqj/0sA51dlU9V2OnT7FYIGM3iV53E9Ndm5nK5vK9jTmQnKWTIGDWQ/F+efr7aKpOpjKvVyD1JS/KLeRax4Wwy8hUQeHtPH+Mj6dbPQrmf/Jk4SpwGSNlVQ==</BookingCode>
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
                        <PriceInformation>
                            <Routes ValidatingCarrier="EI">
                                <Route Origin="37786" Destination="39681">
                                    <Segments>
                                        <Segment DepartureAirport="MAD" ArrivalAirport="MCO" DepartureDate="2019-10-16T10:00:00" ArrivalDate="2019-10-16T17:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="1234" JourneyDuration="P0DT7H0M0S" GroundDuration="P0DT7H0M0S" Class="B" Cabin="Y" FareBasis="200" />
                                    </Segments>
                                </Route>
                            </Routes>
                            <Prices>
                                <Price Type="S" Currency="USD">
                                    <TotalFixAmounts Gross="105.26" Nett="105.26">
                                        <Service Amount="105.26" />
                                    </TotalFixAmounts>
                                    <Breakdown>
                                        <Concepts>
                                            <Concept Type="BAS" Name="Base Coste">
                                                <Items>
                                                    <Item Amount="52.63" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                                </Items>
                                            </Concept>
                                            <Concept Type="BAS" Name="Base Coste">
                                                <Items>
                                                    <Item Amount="52.63" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                                </Items>
                                            </Concept>
                                        </Concepts>
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