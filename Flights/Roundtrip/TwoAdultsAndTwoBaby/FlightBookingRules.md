### Request

```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns="http://www.juniper.es/webservice/2007/">
	<soapenv:Header/>
		<soapenv:Body>
			<FlightBookingRules>
				<FlightBookingRulesRQ Version="1.1" Language="es">
				<Login Password="xxxxxxxxx" Email="xxxxxxx"/>
					<FlightBookingRulesRequest>
						<FlightOption
						RatePlanCode="LF6j9ndyo/zlz9tkRLu5T4vcqg4Y3XWeGauWGUmxxJy33kAWihQpwFONCEgQgZ8jBiKPBLBrUDh6I2tXxLJHYiZ4wWOqeXQPYYzEOwPVmVCPY8gME6dN0Vi66OuicoOrZHEuDowMEsdviZOg/p03oUeun54AEuonN1tCNLT1tPuTZmJERKlgk/KRZXmbRhM2rqS75XOGl/HMseg4YAcpxieQm1kQ7Uc2xckf2kbb64BKiPStM7UL7DGT2xf3MquEJSUsehJ0NaUp2LqkLo3aHNa1SgtFpX0/jVd1wO65dZOLnOR/4sxXWkzKO79UAgSEVLZbLmLIYo/ldlqIuQG11btFECVAmC7H5rlXhaI+mI6tgdaXLnYdwlP0J3P7MwjAbSGl8z/cWySX/i+vzgLXeRnVbfNWCRw5NqkssoUtfFE6kuu5fPnBiNQaUHZDAWzqwzUBWq59LnaHpwlnaOvbaYPqS0ASg7B+QnZ1UheSotxhRSur8JpTYygmKv2RFQxpSjCQ5as/F9E/GSlw4YCSyQO5IPrLrlk3pprP6SErbnMMdNwJA17TICbMYT4k5s2wz1gEABCLLghXRAvCWhfSaUpAzp26iulGe3f/BSBB6mpdSaIAZe+7BbUSgKb7b3V01Tsk6ivH6AAyFnIQ/kZkO+Lck4Y4AOhBqqgIKqWm7KXxzfx4VLkBwPNSt+td9n8F4P1MqtJ/fbnkgRTdg/VCW9ih4pWG+aLn7TNypfhFm1voYQMrPhRxL9iEdR3cDsZkFlBlylfUFLRFTQU19mZBWyLlXxJYdvuIZtNpPPE1uU3fbLfIukT8D2sOp7CH77/N8Ny47x9zUjX3n7Iwkuk0Gr98SMGz3j8liTnONOIcMGiyTsvPel2KgKhspD5LcDnzt7GV6mJPuQmSNQEhwwrbJKb9HU/IeA5WyqXkB5IzrYDDCzelH72/kWEgdHYIgpF+VfBlRPEr7Qf2hvLmnYj/CQYzcC2aEAaN5N2x3C6EOhyNAsrCsZPz+uf5EFf5v+MppynkG0uYVYhwV3uG5/gggg=="/>
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
            <BookingRulesRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-28T14:22:29.3639436+02:00" IntCode="Z7fzkv9VSAztTEDob/zqE01fBiVc720KE7D3FN7RTqs=">
                <Results>
                    <FlightResult Status="OK" Source="ChV2" Direction="Outbound" LowCost="false">
                        <BookingCode ExpirationDate="2019-07-28T14:32:29.3326961+02:00">LF6j9ndyo/zlz9tkRLu5T4vcqg4Y3XWeGauWGUmxxJy33kAWihQpwFONCEgQgZ8jBiKPBLBrUDh6I2tXxLJHYih0qUE6xzVNJYVWBO6wczcZlU+YqHyh3MmG6qFQh8i4yIznbMaIMqhobyUNI3eHUy6af2uhSPp6cg5tU/bFEiT1CxT8IO2TVKLglJd98u+QwvGj/I/XzWs+Ubm6NL0B0VBt2PROOe6QmgI5bCsIFT9/o4SPfcAhuxiUS7GECZyEorM/L/ObylH0nbjofEP8nXR+scMYzkHGa7Lq3uDwSxWqWvdwM3NM18XnhIQSAxTPgG4MTAR96WSXajdRrWN1dPM4/0/kMVJLtAzRVN8W9W3Wya/z0nFPWmQH68CdQwAQ3i/JcvNMduoK20udho4wrKBw+7BdjcX8YtAYEOpJZ3OzLE+d35wZKtAH7miC4VzdnFAZKenwR7PpxH7f+zwZwSVb9h9FMekjP8EJTQ1V5sKh956UP5zIi9FBipiqjowtxpjBmNTopwKUGtrrrIpNoPcxUgm9ZUJitL6mFj7cZi7rZKcBwGTKdAlMWUjCSgkgIop9qsGMv987eTAnGQVdWM20RrTSHZQf3amREg+uDz0Nfm5U+yvkyLL+Tsz9wFOmV6hkWrI3N1eYmcNye8yPvmT19KqSohXbJJesYFz6PuccRQRSsY6Nrvl1uMyqGedrZ/9RJOlhdqbI+0zKQeXFqQohlZBNNE4gJkRCoL3MybVXV+jLjfB0jzL6le9iGOAF1EWs7YiUddbrcxCGXx6KwCQGiRagXavAyoX/yL+CYVpIo92aH+YKHHrXy6C9AYv0qOGPZwCJrn/ZZlbWkw/G47UCo/x5IP3SLwbNpiMbnJ1VbbOKpiUJg02RW9JxQYKvyvckQFT55pYe0SugOAegv4ybKNoEee6zmkEe1Xe/k37A4goNIQ/CgIGTQMDzWOQf1yqH8bTT6jBMjZ9CnkZp5gxYtmRPSmV4YK9qC7gDB4hM0vN8E6SmcSUPf6/Z4xHtGj839pmt4nXLQ4ydG2XNbg==</BookingCode>
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
                                    <Pax IdPax="3">
                                        <Name>Passenger name</Name>
                                        <Surname>Passenger surname</Surname>
                                        <Age>5</Age>
                                        <BornDate>1989-07-28</BornDate>
                                        <Address>Passenger address</Address>
                                        <City>Passegner city</City>
                                        <Country>Passenger country</Country>
                                        <PostalCode>Passenger postal code</PostalCode>
                                        <Nationality>Passenger nationality</Nationality>
                                    </Pax>
                                    <Pax IdPax="4">
                                        <Name>Passenger name</Name>
                                        <Surname>Passenger surname</Surname>
                                        <Age>15</Age>
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
                                        <BookingCode>LF6j9ndyo/zlz9tkRLu5T4vcqg4Y3XWeGauWGUmxxJy33kAWihQpwFONCEgQgZ8jBiKPBLBrUDh6I2tXxLJHYih0qUE6xzVNJYVWBO6wczcZlU+YqHyh3MmG6qFQh8i4yIznbMaIMqhobyUNI3eHUy6af2uhSPp6cg5tU/bFEiT1CxT8IO2TVKLglJd98u+QwvGj/I/XzWs+Ubm6NL0B0VBt2PROOe6QmgI5bCsIFT9/o4SPfcAhuxiUS7GECZyEorM/L/ObylH0nbjofEP8nXR+scMYzkHGa7Lq3uDwSxWqWvdwM3NM18XnhIQSAxTPgG4MTAR96WSXajdRrWN1dPM4/0/kMVJLtAzRVN8W9W3Wya/z0nFPWmQH68CdQwAQ3i/JcvNMduoK20udho4wrKBw+7BdjcX8YtAYEOpJZ3OzLE+d35wZKtAH7miC4VzdnFAZKenwR7PpxH7f+zwZwSVb9h9FMekjP8EJTQ1V5sKh956UP5zIi9FBipiqjowtxpjBmNTopwKUGtrrrIpNoPcxUgm9ZUJitL6mFj7cZi7rZKcBwGTKdAlMWUjCSgkgIop9qsGMv987eTAnGQVdWM20RrTSHZQf3amREg+uDz0Nfm5U+yvkyLL+Tsz9wFOmV6hkWrI3N1eYmcNye8yPvmT19KqSohXbJJesYFz6PuccRQRSsY6Nrvl1uMyqGedrZ/9RJOlhdqbI+0zKQeXFqQohlZBNNE4gJkRCoL3MybVXV+jLjfB0jzL6le9iGOAF1EWs7YiUddbrcxCGXx6KwCQGiRagXavAyoX/yL+CYVpIo92aH+YKHHrXy6C9AYv0qOGPZwCJrn/ZZlbWkw/G47UCo/x5IP3SLwbNpiMbnJ1VbbOKpiUJg02RW9JxQYKvyvckQFT55pYe0SugOAegv4ybKNoEee6zmkEe1Xe/k37A4goNIQ/CgIGTQMDzWOQf1yqH8bTT6jBMjZ9CnkZp5gxYtmRPSmV4YK9qC7gDB4hM0vN8E6SmcSUPf6/Z4xHtGj839pmt4nXLQ4ydG2XNbg==</BookingCode>
                                        <RelPaxesDist>
                                            <RelPaxDist>
                                                <RelPaxes>
                                                    <RelPax IdPax="1" />
                                                    <RelPax IdPax="2" />
                                                    <RelPax IdPax="3" />
                                                    <RelPax IdPax="4" />
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
                                        <Segment DepartureAirport="MAD" ArrivalAirport="MCO" DepartureDate="2019-10-25T10:00:00" ArrivalDate="2019-10-25T17:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="1234" JourneyDuration="P0DT7H0M0S" GroundDuration="P0DT7H0M0S" Class="B" Cabin="Y" FareBasis="200" />
                                    </Segments>
                                </Route>
                            </Routes>
                            <Prices>
                                <Price Type="S" Currency="USD">
                                    <TotalFixAmounts Gross="168.41" Nett="168.41">
                                        <Service Amount="168.41" />
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
                                            <Concept Type="BAS" Name="Base Coste">
                                                <Items>
                                                    <Item Amount="52.63" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="202" />
                                                </Items>
                                            </Concept>
                                            <Concept Type="BAS" Name="Base Coste">
                                                <Items>
                                                    <Item Amount="10.52" Date="0001-01-01" Quantity="1" Days="1" PaxType="CNN" TtaCode="303" />
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