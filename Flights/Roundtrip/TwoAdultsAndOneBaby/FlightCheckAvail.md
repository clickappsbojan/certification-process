### Request
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
	xmlns="http://www.juniper.es/webservice/2007/">
	<soapenv:Header/>
	<soapenv:Body>
		<FlightCheckAvail>
			<FlightCheckAvailRQ Version="1.1" Language="es">
			<Login Email="xxxxxxx" Password="xxxxxx"/>
			<FlightCheckAvailRequest>
				<FlightOption
					RatePlanCode="LF6j9ndyo/zlz9tkRLu5T4vcqg4Y3XWeGauWGUmxxJy33kAWihQpwFONCEgQgZ8jh2qgNLr3UUIh1pN4HhPScroL38KdGk2VoMaAFRpQ2UW05L1/XEaDj1FmG9l9D/hwKSuyhNJ2T0O0HcLz9ifhf0hdoihQthapHvHg5Zds3vtrEmgY/FNIUr+8F65VS2G2ZfVjGq5Cq6GcwROErkp1QmmV16nDR/1W70yzcWwKKS3OFyo7okugrkFLVkH5rN04EYLrcBcAJMDzaqJ5nE3BX7VRAukKTGniHJCcyGu/Nt10eJEjlmgLAOl/uPAe6FTfl6TIkxa1/M+M2uEaSb25zysKmKeTu8u/n8etfKy140Vv8ThRbObss7oozn0sqlhJ+1Hco+vwLKB00y6XyTVacTq+yn9RTNcgjVSHduJjFiLUE2COBVZ3FtwXBjfunKqam6cjcFiKCvAY74ffQ+t30+el8zmO4fdhNGeGFexKTkoaWk9Q9m+FTYPF5jWsImmH0mkPijtSeXXEaDsB6g4I7f+y3uE4i+PgnvHPzyl6UPddn0AbOuoJ1/8/LviVAgKpfuGR9mnnSAj7fA7H4RQxazphHaVjNO8Oy/G9qGZFMSlu3Igei8275GrsB3rQtWS9hhXwt87/wyBKXrXmsIDgym6VLuXWSgD1S6OrpRaVjwABA4CQczq8fowOGhmpXrzwxK10h12oRh8c3Gozg2Au01e96pXDizVlscsCu/lAtp5Sw2+XpMS108vj+iDHKSyOBqjkH516VzqNiEeshLCPxq5xyHJAasEY+l198aPG4HiC8aUjgNf2lNFC1mOedjykDDVoKOWm8pkgJ8+Ehzv6+kpZxi052oyNmaPKA5AlRxcYvYZHVe2CCUOxm6EZ8BvKdHQLUtE/RM5OlYDmM67q4m724JKHeBqAhurML5XVMBJDsozgq4MgvnbmV/Cle8jcbGh+BAsFE22bITKxQdzBMvBkU0z2I8rG+Tg1Qdg0+2g="/>
			</FlightCheckAvailRequest>
				<AdvancedOptions>
			     	<ShowBreakdownPrice>true</ShowBreakdownPrice>
				</AdvancedOptions>
			</FlightCheckAvailRQ>
		</FlightCheckAvail>
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
        <FlightCheckAvailResponse xmlns="http://www.juniper.es/webservice/2007/">
            <CheckAvailRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-28T13:58:25.4648755+02:00" IntCode="9tUk7D58UPTJBhM0AJQ4bfbOKC3UM6pHUKdfu8CsCCQ=">
                <Results>
                    <FlightResult Status="OK" Direction="Outbound" LowCost="false" RatePlanCode="LF6j9ndyo/zlz9tkRLu5T4vcqg4Y3XWeGauWGUmxxJy33kAWihQpwFONCEgQgZ8jh2qgNLr3UUIh1pN4HhPScgnu6ACy2Y1zX5xk57se1Wn4+hb3AMCRAJ2AcGXCD8DaqvRVjYao775Z4rITqeQEjyallvcrjwX5ajSRFyGzFERashKe3QJ2V6sFhpe0xaFsuUz0T+LSa/7lmTQP5YnAWmdlZ0+OrVbD76Q0BJYBpQzHpWM+F+Y5OCbhYoNVPiurh1OyGJdcWSg/y/Gb2VW/tTi7hJB5FP+0e3Z0fZ3lhUUrkQt0IfTIpZsRNOF+M5iMJ7FKCcrJGeB48EGZ15fEYjk+UY01gaXW4grChhd+vOE1m1pyU/QNFAtox8Up1XTYntNuM+r4dRWolFpwKvA2DDWzwOaDxUE2OOiDfzr2FCFx8SI3AENrhmLivGlOGEke+t7ji5pRgT95ONzx4bf58PrdUbrJXhMsON/bZV062Sjy8NfUetlFZX3Sy3KXQ+PXE4osEPABsGBV3HNR+9TjIZukno7yWSNxSdunFS83hIXOxOSzorSIiZKRvvlseqexY2XwrusFqqpBIntvuW5/Hm+w1QcnUl/Re7qqgFaEvG+27AO08QchGwln/qwPriuYVWmyXTOPIelGfYAXZaeH4OhiC2aSzRBIoe7VB4prBQ0mViFg4UR2i9o5h/N0GUEVuGTFcn1+vmRJliTGs7stsr5zdgoySIkzJE4stT9bT4t3chREEUxyQaqGWR+ajGNugjTIGvmWcNKvMLgHib19WnSUT3Gb0Q2j5gduRa2eyNrAcZGv54M6emAioxkoerYPLF72gXwCG8F0Wzu94xxekFoSXnNHku/g97TLsYn1LiqLH2Cdpj1KsQEH8NFovUYlvpEMqqFMyEOrC4PKhg2bLkkI9tRpGD98hoPixN3yIK1P0i1ChVjOfwid+Ok/t3LqzgZlVieAcKFYr4DQlcNQHvYjhbgbbL5MzBXPxQdLyJjF4A18xc2ZxIgaIdJ7/OUe">
                        <PriceInformation>
                            <Routes ValidatingCarrier="EI">
                                <Route Origin="37786" Destination="39681">
                                    <Segments>
                                        <Segment DepartureAirport="MAD" ArrivalAirport="MCO" DepartureDate="2019-10-16T10:00:00" ArrivalDate="2019-10-16T17:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="1234" JourneyDuration="P0DT7H0M0S" GroundDuration="P0DT7H0M0S" Class="B" Cabin="Y" FareBasis="200" />
                                    </Segments>
                                </Route>
                            </Routes>
                            <Prices>
                                <Price Type="S" Currency="EUR">
                                    <TotalFixAmounts Gross="103.99" Nett="103.99">
                                        <Service Amount="103.99" />
                                    </TotalFixAmounts>
                                    <Breakdown>
                                        <Concepts>
                                            <Concept Type="BAS" Name="Base Coste">
                                                <Items>
                                                    <Item Amount="47.27" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                                </Items>
                                            </Concept>
                                            <Concept Type="BAS" Name="Base Coste">
                                                <Items>
                                                    <Item Amount="47.27" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                                </Items>
                                            </Concept>
                                            <Concept Type="BAS" Name="Base Coste">
                                                <Items>
                                                    <Item Amount="9.45" Date="0001-01-01" Quantity="1" Days="1" PaxType="CNN" TtaCode="302" />
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
            </CheckAvailRS>
        </FlightCheckAvailResponse>
    </soap:Body>
</soap:Envelope>
```