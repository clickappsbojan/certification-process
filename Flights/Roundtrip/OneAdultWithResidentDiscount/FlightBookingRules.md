### Request
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns="http://www.juniper.es/webservice/2007/">
	<soapenv:Header/>
		<soapenv:Body>
			<FlightBookingRules>
				<FlightBookingRulesRQ Version="1.1" Language="en">
                <Login Email="user@mydomain.com" Password="pass"/>
					<FlightBookingRulesRequest>
						<FlightOption
						RatePlanCode="LF6j9ndyo/zlz9tkRLu5T4vcqg4Y3XWeGauWGUmxxJy33kAWihQpwFONCEgQgZ8jfv40vfGcKGOk7ka1rxIDEXg7QesDFSWc5nEa0vDCS1/LFsyseCHitlCr7+pLnA322h8INjUBcByLNL7bj0G2UKVPv52hDqhjPJT6UH7Mi6JKN54NMQkBkHq6Ob1kiTayBGCdDZtka5GLp6NIxlK/pHnaopzhK9A/deyntKap/qlA4mAi+7tJif6Fvt7K6/JoOCaT/aCphk+xb4kOwv3xUKUvmCxOwPQPuWB4fcub+U7VrtTx74QGQvzO1jnZkHTh6T7nFCM8V6htmVJp36+OJaHXSA0zBl0m7Rb70WbLEAM5tk9PkoKrwheJbPKmjrImQ5VMYRNGZ4lQdEMKVxGTntPJI2fuIOX2rOrxrRYCguLKGOYMZFzWf8Uxf0AxPOn4NbOsme1fBHZiCx5FCdiZdFD84tQOEtVxy+DaJ6F1ng6QR8o6HqGTtAOReJNbUNS+SLcJ8ON9+JkajjlzqORg0C6mPC/bcgDt1h70oIs4q/oWdjQvaONiAeBcI0xx8uXrg8axpZyEG+iCEvB8WR/FJuSwtceXVAP+aZbhr53/PFtkU3q9UH+DFQO47mkRzlI+Ij58m8A8ur/jIxTpUJbVWggQIJc/51A+Ww8/6bhb42dzxF1vpyOvc5qaEEBvGYIVs9CyKkfR9pTreOF2obH05bEVd+n1fLY5cwyEyJy0yxgismMDZO+q4Bh7nOiPgzCOI7E2cSuzyyMZv/2lBBT+BfA9yJawF74Has8jGfeblllWXtL+l2Npyh8v0Vo4+a0WXwXcR41pxt2FTs5OIbUuiwfqDP0rKkb9Y90GVPmxdRZKmmSsyeyiVugC2F8ykijtGvoMQmuChTbyeQ5UWwiJ7JrD7w1UFMG8vnJeNjIZ6Yo="/>
						</FlightBookingRulesRequest>
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
            <BookingRulesRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-31T15:49:15.3207342+02:00" IntCode="SuP8LSJw2P6tdHnTxWwu75qxLpf2mFyF6BiibJeBYAg=">
                <Results>
                    <FlightResult Status="OK" Source="ChV2" Direction="Outbound" LowCost="false">
                        <BookingCode ExpirationDate="2019-07-31T15:59:15.3051092+02:00">LF6j9ndyo/zlz9tkRLu5T4vcqg4Y3XWeGauWGUmxxJy33kAWihQpwFONCEgQgZ8jfv40vfGcKGOk7ka1rxIDEShQwvSyC/AJ5kriJ8gXxU6jPCpYeknGTdX+bkRTr2yg+0lc7DSgURATgRif4hZ7QMFn7PfViq6/SGkFNHK+xOGxEXejKwY5Up/bhfKBkPQoPpkvoWzwoKUU5K221DXmh7kpSe97zGk2oghzXWFRUdtDrV3ux2NFKDEv6D6blThwhwc2+PkIq2M55NmTMJzUqHHtv9wIgUnOw+JBazUQH5i5HwbdeuxQxVOGR24W9u1wZWVnK4EZxideITCpcY5badZIAxqMssyjixvisy72yumlG5fYJlODVMC37onojTqBAeaM9GIx8D6nPPdfyEnaO/OFCS+3H15uPjj02xTUD+jdkXV3cmz8Ao6+Jsp1AxSbuBKLER0kXl9mNGQC9zKHz4jhcQs5CY5rEl9lILsPzxq6a3lONoro6Ro/ge/4H/Nxa5MwucDpadcKMRUx8tjI2KrOBigCol4PLyGPD29TEyRY0uPnxGw1lGDB0eeevSttvm3VO91cKuQD9PzRHWymuNXaTLbnh78qEV6sqVS+kWWJ/r7TaCecUVQiQO2dDE/p7pLGxjwn6MFPH/Vwlw10koBN2Vz/WcBCcCRp5s16oWT4owzwivnVabJYPquAOAxIApyDXtrTo5MmE4PiL5ciwDlOOXYyH+tzGC+E+KAMKz+KkV1soZCSbhmfkKnCpeG+K13TIBeAavyaj5S23rYG/T31EQUlR/bDrstJ0BVp++tJgxxyiJ0Qlfmur536aJ7j9V9KqMzW7LcbjqipE3J3SQ1d7u0WdadjkomAMYHR/P6j560Wsb+RJFdSBFSjx+SGqIkooO0GAt3Oo/vaaEehTnu57xQb8iqaoIM2+lz79nJOBjDvWYBzLPBb1zmaCZcc</BookingCode>
                        <FlightRequiredFields>
                            <FlightBooking>
                                <Paxes>
                                    <Pax IdPax="1">
                                        <Name>Holder Name</Name>
                                        <Surname>Holder Surname</Surname>
                                        <Age>28</Age>
                                        <BornDate>1989-07-31</BornDate>
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
                                        <BookingCode>LF6j9ndyo/zlz9tkRLu5T4vcqg4Y3XWeGauWGUmxxJy33kAWihQpwFONCEgQgZ8jfv40vfGcKGOk7ka1rxIDEShQwvSyC/AJ5kriJ8gXxU6jPCpYeknGTdX+bkRTr2yg+0lc7DSgURATgRif4hZ7QMFn7PfViq6/SGkFNHK+xOGxEXejKwY5Up/bhfKBkPQoPpkvoWzwoKUU5K221DXmh7kpSe97zGk2oghzXWFRUdtDrV3ux2NFKDEv6D6blThwhwc2+PkIq2M55NmTMJzUqHHtv9wIgUnOw+JBazUQH5i5HwbdeuxQxVOGR24W9u1wZWVnK4EZxideITCpcY5badZIAxqMssyjixvisy72yumlG5fYJlODVMC37onojTqBAeaM9GIx8D6nPPdfyEnaO/OFCS+3H15uPjj02xTUD+jdkXV3cmz8Ao6+Jsp1AxSbuBKLER0kXl9mNGQC9zKHz4jhcQs5CY5rEl9lILsPzxq6a3lONoro6Ro/ge/4H/Nxa5MwucDpadcKMRUx8tjI2KrOBigCol4PLyGPD29TEyRY0uPnxGw1lGDB0eeevSttvm3VO91cKuQD9PzRHWymuNXaTLbnh78qEV6sqVS+kWWJ/r7TaCecUVQiQO2dDE/p7pLGxjwn6MFPH/Vwlw10koBN2Vz/WcBCcCRp5s16oWT4owzwivnVabJYPquAOAxIApyDXtrTo5MmE4PiL5ciwDlOOXYyH+tzGC+E+KAMKz+KkV1soZCSbhmfkKnCpeG+K13TIBeAavyaj5S23rYG/T31EQUlR/bDrstJ0BVp++tJgxxyiJ0Qlfmur536aJ7j9V9KqMzW7LcbjqipE3J3SQ1d7u0WdadjkomAMYHR/P6j560Wsb+RJFdSBFSjx+SGqIkooO0GAt3Oo/vaaEehTnu57xQb8iqaoIM2+lz79nJOBjDvWYBzLPBb1zmaCZcc</BookingCode>
                                        <RelPaxesDist>
                                            <RelPaxDist>
                                                <RelPaxes>
                                                    <RelPax IdPax="1" />
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
                                        <Segment DepartureAirport="MAD" ArrivalAirport="MCO" DepartureDate="2019-10-28T10:00:00" ArrivalDate="2019-10-28T17:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="1234" JourneyDuration="P0DT7H0M0S" GroundDuration="P0DT7H0M0S" Class="B" Cabin="Y" FareBasis="200" />
                                    </Segments>
                                </Route>
                            </Routes>
                            <Prices>
                                <Price Type="S" Currency="EUR">
                                    <TotalFixAmounts Gross="47.17" Nett="47.17">
                                        <Service Amount="47.17" />
                                    </TotalFixAmounts>
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