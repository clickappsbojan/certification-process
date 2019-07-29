### Request
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
	xmlns="http://www.juniper.es/webservice/2007/">
	<soapenv:Header/>
	<soapenv:Body>
		<FlightCheckAvail>
			<FlightCheckAvailRQ Version="1.1" Language="es">
			<Login Email="user@mydomain.com" Password="pass"/>
			<FlightCheckAvailRequest>
				<FlightOption
					RatePlanCode="LF6j9ndyo/zlz9tkRLu5T4vcqg4Y3XWeGauWGUmxxJy33kAWihQpwFONCEgQgZ8jBiKPBLBrUDh6I2tXxLJHYiZ4wWOqeXQPYYzEOwPVmVCPY8gME6dN0Vi66OuicoOrZHEuDowMEsdviZOg/p03oUeun54AEuonN1tCNLT1tPuTZmJERKlgk/KRZXmbRhM2rqS75XOGl/HMseg4YAcpxieQm1kQ7Uc2xckf2kbb64BKiPStM7UL7DGT2xf3MquEJSUsehJ0NaUp2LqkLo3aHNa1SgtFpX0/jVd1wO65dZOLnOR/4sxXWkzKO79UAgSEVLZbLmLIYo/ldlqIuQG11btFECVAmC7H5rlXhaI+mI6tgdaXLnYdwlP0J3P7MwjAbSGl8z/cWySX/i+vzgLXeRnVbfNWCRw5NqkssoUtfFE6kuu5fPnBiNQaUHZDAWzqwzUBWq59LnaHpwlnaOvbaYPqS0ASg7B+QnZ1UheSotxhRSur8JpTYygmKv2RFQxpSjCQ5as/F9E/GSlw4YCSyQO5IPrLrlk3pprP6SErbnMMdNwJA17TICbMYT4k5s2wz1gEABCLLghXRAvCWhfSaUpAzp26iulGe3f/BSBB6mpdSaIAZe+7BbUSgKb7b3V01Tsk6ivH6AAyFnIQ/kZkO+Lck4Y4AOhBqqgIKqWm7KXxzfx4VLkBwPNSt+td9n8F4P1MqtJ/fbnkgRTdg/VCW9ih4pWG+aLn7TNypfhFm1voYQMrPhRxL9iEdR3cDsZkFlBlylfUFLRFTQU19mZBWyLlXxJYdvuIZtNpPPE1uU3fbLfIukT8D2sOp7CH77/N8Ny47x9zUjX3n7Iwkuk0Gr98SMGz3j8liTnONOIcMGiyTsvPel2KgKhspD5LcDnzt7GV6mJPuQmSNQEhwwrbJKb9HU/IeA5WyqXkB5IzrYDDCzelH72/kWEgdHYIgpF+VfBlRPEr7Qf2hvLmnYj/CQYzcC2aEAaN5N2x3C6EOhyNAsrCsZPz+uf5EFf5v+MppynkG0uYVYhwV3uG5/gggg=="/>
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
            <CheckAvailRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-28T14:22:44.5346343+02:00" IntCode="Q16tod6BNP4NEK/tqPTEprK/4/VpKo0s/TSUhMHwddg=">
                <Results>
                    <FlightResult Status="OK" Direction="Outbound" LowCost="false" RatePlanCode="LF6j9ndyo/zlz9tkRLu5T4vcqg4Y3XWeGauWGUmxxJy33kAWihQpwFONCEgQgZ8jBiKPBLBrUDh6I2tXxLJHYih0qUE6xzVNJYVWBO6wczf6gY1JjYy8HTeVrmDDDJLmY1w+EGWVAg7GWsr2pmnaWk77j3ZX4l/uOh8twNf/M6flhyZwmayjqtZwibB41cpKIKQO2J4y83wgX7iN6SFpZmsHH4P7TM8mdM6qOzSYO1S3BrK9AosZKLc7L1yoGpE6j1HycFtXYKhw9G8iKgoBuw0Jc6cpNuQMgjXvIxOKkfWcR1H/WI7FOoi/B7CP7Sl+xjAD4kydEJmuqnK2qyVNzl5yfbDGojq+KvW9YgSXbRHoC69tTTADBA5bFNMFMsbGReNuBJQTC4oorGHR74V7bW82a5kmeo3B9eRdnqUGjDgaGC1oxKG3eV8LuHtMbFaGmuYQLN1RjOtbnEE7WcYfuejRara4HWhhBsLYpMNCqj0jYGKZm6HVGXaYze3Y0FeNEgjzYw8oZ+t2evUYZKzATJUP+AqwwqNzgd3UG44bseunONK4LMlfO79nC3o/vsdUwiVmb8OynRiRASqHpWAPp0mUVgZ4bcAd46oCo4iEWuf85oBsIqu6Gzq/4lc4Oi+2XIyJr5mrK2/twWXZRcHT/568PBVVfVjhnuDVWUXgtNWbG6T6C/6iyiMa/rVRadG959ABknxCUYAlDRti5mfAsLkVASQ4qgE4dRvVrzhHreJAOqFRtLTq/9giSxQ8IYF52z+mL3SFcIg3IvJbThQhPR5QJOLy2rAzrZkZD3TgMAdtVZh2ZvT//frEiiJ3Jn6upWv1eQ4KsBV8HNY4QnoRq2R52BHfFx7b6j+se9cXZDKuflhIJNf7hdUbVPIAm/k7uw2f1aPTrffBLDtdsSxxC+V0+pz0cjJ+MKzyN/6SP0h+XGj7SPifbIo5VB96rfm4IE9EXnY6QkpvLsYjdib/MVe/QPrOIr3Dg0WsP98BdtXUy7Y9iUnftGUtCyWorUuPpoKIxL37OjFRSyQxGK7bKg==">
                        <PriceInformation>
                            <Routes ValidatingCarrier="EI">
                                <Route Origin="37786" Destination="39681">
                                    <Segments>
                                        <Segment DepartureAirport="MAD" ArrivalAirport="MCO" DepartureDate="2019-10-25T10:00:00" ArrivalDate="2019-10-25T17:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="1234" JourneyDuration="P0DT7H0M0S" GroundDuration="P0DT7H0M0S" Class="B" Cabin="Y" FareBasis="200" />
                                    </Segments>
                                </Route>
                            </Routes>
                            <Prices>
                                <Price Type="S" Currency="EUR">
                                    <TotalFixAmounts Gross="151.26" Nett="151.26">
                                        <Service Amount="151.26" />
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
                                                    <Item Amount="47.27" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="202" />
                                                </Items>
                                            </Concept>
                                            <Concept Type="BAS" Name="Base Coste">
                                                <Items>
                                                    <Item Amount="9.45" Date="0001-01-01" Quantity="1" Days="1" PaxType="CNN" TtaCode="303" />
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