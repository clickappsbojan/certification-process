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
					RatePlanCode="LF6j9ndyo/zlz9tkRLu5T4vcqg4Y3XWeGauWGUmxxJy33kAWihQpwFONCEgQgZ8j3MYnbZCiHJVG3tYrqJx3gJshoeNGijCN4wKm8yPI+Atx2j1gmfEyA+u+xJkFUx6mv3EDM08fGg58yKNPSbfeXTIMMqH2NLlqJkZxNAWnGTz9J7WLZr6qzvfLRspkFdBYTyVc/ByVCezR4T5xbJgVJYXnjtRdXaaGh6J2QmbM+E4csFmmrbSTBdyaANDpcjU8/qyJwZf10lC1VFBacKkaUfRFYb7aXiZggMKURER7L54WUcpq021IAq9nnzIKYCsavyZBfhttJOW1igjSyg5kOoUTiRUFbInVonCXQb9bkM+jjPtH8K9CMvLFicHv6ZBpmyhUtNzeRddhQRxWeNY1YlQUFD1wq4dTWZU1UJq8LI9qfQHXt2xyrE7b6noyT4ZpE6/qjRUwlZHcGo5BQfuNTzl56pz+KcweBfYjbHm1cj7JN53qJiMBQSMrcPFT9dZiusa1Z/4C2hpw+j5UmprIT8AROpr2iRz0um4SbwdFkIZPLSu0dO5WvaYPAJK1X0H3d9m2R9KRFwjxOgf+7dwnjEbJdQxTUHXlN/kXt3Y0x0KwQjyo5Sw0yOXZXqzDoKI40bEr+aMqh/z1IHjS6xyDmLTafUoR/oO6yyl1lWGCU5vIkV8Uyfai6BgZEVk++43pn9Sc0LXq28/kiHVyb0ZedhHgSEqT3K0at+pSChQQ8HPQyfRoctdqO/yxm2Mbpgu/6VsAlH7uFfraIxO7L27A7/J7aHKkeRGIJODNWbyzB39dP0xTLFnDaGff5XeRrp2/pm2v+zj6i7t9eEIo9dI3wMrA4zM76z05Y30rhy6QymalQk0bEdtos82IelPQ82lh/R669cN3NFX1buX+KMFFbroWE6yVc8Zy/FnCgFzFfwvXhgvi02HkRt5ifLFA6z+5I8JTzafgzoVY/uAjCol9hg=="/>
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
            <CheckAvailRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-28T11:03:05.1938549+02:00" IntCode="9tUk7D58UPTJBhM0AJQ4bQKUxLE+FWligRiypveaaAk=">
                <Results>
                    <FlightResult Status="OK" Direction="Outbound" LowCost="false" RatePlanCode="LF6j9ndyo/zlz9tkRLu5T4vcqg4Y3XWeGauWGUmxxJy33kAWihQpwFONCEgQgZ8j3MYnbZCiHJVG3tYrqJx3gAyIPsnY+DOhhGz7Ik+1nzQTzrApGEUUJK7A9z7/RMxlAXjIQdmr+41fRH/qOPFm0KXw0gdKt41QpcBerqUx491fMng1ECoGnOWoccEvr4CEuMT6z+GsPBfem+5ZOPwpZYpBMoja5krJLJTg7QUbkbXmdkejUtf0JQhSuvcYja3TgQ3AAUQ3HpJAW0XzwrrFJKu2dGeZcecWZ2XLu1G6oNVLdlA3RCRuHXcCT/2IgdXsAEwRE/0pSs18w9E/t8TJCZxY4ovr6WWUp9ESTqGAOMV2qUrKDKbZ8wTqww0qOBMVk/2fah7HmeW6w4DbmQPy4e07t+v6a3NkxsQYO+mWhC9ouo2ItWsFS72oc+ZYiIENj6zy3p7s/l7fmb+DIHEn7n1zoU2uV807ZOJAd19eN5mkPJwalXfOiGkriZBGnY86wtB3ByhnX9OXzgvo2QHYssOHHVySI60WOSBd9WW13SKP4TROoZee6PWGqL0AFS7XjNxCHr6jUKK/XM4WSHgADRRfaLEIpikYcy6bog+jz5FjJA4i1vobPCm1C1VKLMcNdss6FqzSdNwq8Sg1T63gE9xcC8j928R0VHVHdkJr41reDMY62Mb2OhzULVN50/lF9qG88ECmoqmrEUR/TgS7G+czqOMDd5c5jNa5+VIAb37ftWtWyeOAfpNd1YNIKb3Ln88KYz1ohcFJ3v//316xAtDE0jT0IPw2jB0yukBmDAP7QYRvn5vLc/lh75XQH5muNGmfTgqpwob5zw2kI/n38VaX8jFkw75c5cdgDIP3WyVzkUMVYW4YsmJV2ExoVzVZdG9B/Q2CWrZZ18/NHlnvvYcA8AVz+XjiJGBicsKsOmptJ9h6GCsDg23tFa2SVsKO7ozjH1YwyecuFy0sOBBn4w==">
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
                                    <TotalFixAmounts Gross="94.54" Nett="94.54">
                                        <Service Amount="94.54" />
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