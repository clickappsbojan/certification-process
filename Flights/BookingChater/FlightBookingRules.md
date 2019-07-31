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
						RatePlanCode="7Vor0/GRKZ31Va+BuE1WMFvq/9heAul4psoTS3hesB97bKcS8vVV8I7otP/319flrdJtWLiEoO9sY2UlyEo7AMdqzRPPN3VUEB5qpZSv9sroRDrX2gmyuCbtYSsDdhIM3MfuQp4euvTHgpS+bKiYuJGPjxmkKlBTY21XMIWDEIxbAXtzCO7hApVApxqNLUUSPhCtyYFidvysK+yqY5A7jr1nd1xWLpHUlkEVYwfp8wcFIp5hUebZe8ykxRPMcdKK/wSeTyLEJY4WiNLUSwOnUTFrG53JmjlNyM4tv4v3z7XwD0o3CBxmDNTXrQ80kJNfSPOVSsD7Wr4JRq5rhJ2REBfZ2sAqh0TXT+4XcC4i9uGmNJs3Bxta9cLg1JnempDXIjK3YcOE55e5FWgAILRPmXD1mMdk+JQgO34ubNjD8ietJ5PZQe5NWmbeI3zfQleLrTOyj+Ysb17HNqX7pBMC/n1fgr2VMbcPCc2pKrzvl4p/CJJ9ZLljj6oO74m8KAYGzvZrKjhMCUWkQEQh6ZTb2VDWDwvML6zc6VD1fROZeqWEOcBEM5Zku6FMw1A/GdAFgScu90aiNFa76Rr3v/4x6ZNDFX5IC1cDhyJWN8/RqNNgsTZjq35FJsiG4rwEPswIX6+6b1P5wWkFUE/l2xXwZjCJ6YiQ4uIhO66CI8WiC74k++SwjxsBohh2uzFP7FSel+rroCI3xGhAHFk4seVIT5Tl5I2IIVWQi6nWG2Y+j7n+ItGKWQLyq0J6F6EU7Rczj54zBNwhIHoc1g+ahR/BVuoBnUbOKwBpnKjQxl+qlma46iCon98SIOka49Q9mZlqHMjG9DlJCHNK7DWpVsOwZS+HDGBX/mUn7bwcbjZVOdQw8XDjIp79qTWpwMwP9oZuDB9sWxMdi7ZoEd2KHxY0s5jxWWepdtdpSwhtQbTl2uvQ3Abg4Ek1n0M4YiGMCHA+"/>
						</FlightBookingRulesRequest>
				</FlightBookingRulesRQ>
		</FlightBookingRules>
	</soapenv:Body>
</soapenv:Envelope>
```
### Response

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <soap:Body>
        <FlightBookingRulesResponse xmlns="http://www.juniper.es/webservice/2007/">
            <BookingRulesRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-31T16:39:55.2252533+02:00" IntCode="Q16tod6BNP4NEK/tqPTEpt1mNSPeZfbvWZQ0GjoM9yE=">
                <Results>
                    <FlightResult Status="OK" Source="ChV2" Direction="Outbound" LowCost="false">
                        <BookingCode ExpirationDate="2019-07-31T16:49:55.2096311+02:00">7Vor0/GRKZ31Va+BuE1WMFvq/9heAul4psoTS3hesB97bKcS8vVV8I7otP/319flrdJtWLiEoO9sY2UlyEo7AAymB9ND8KjSvVdFJpcmOjuKUqVr/8yLd18XaMWgIm9ykB2/2g/0Onvapv6hMcEHoXs5BhlCGUoz/Z/KXF7JNVlV+9a7KKaJiAGGLM6E4zfHVl/RdjeqUbhydDJnq5PJf2QrMA52s3SDutdI7FB7CycX6cHD5PgEgJCB5m44vLDWUcCQeNfCiFR/B4YEIPTzgKS1kABi+bohfi0PYWOea77SV4hxTqsMwzO7F6Bp5y/zODywYO553kRP+rmkAhvV8AYEgqiZU4FKMn61KyDecK/PqdNH0uxonkgFbtgia40+Ow+0to37wizUqCpOFGtGBqn19yXqdm2yiGae2e98RN8uY5RIGeCj7jsgYcAJNMEhscFdx64WTpLetI8fvoHfq5aE6u8/HgVLSucRv/4YpyIKFs7K21B5QnD7LPjf6cwsxwkITvRTRVlwI+IZNpkKqORJwvp3iJ+6rG8vtuuR0emX3GkB013iKERHjX4+PEY9iG0MbjidOWbAmeewbkPUbIGK8nAz80AP8xvhbmvXCJcThpaAmc2dTtCq1EZ+iHCyNX+3AhXWxiTaaUBkriA96MpxteElZgSefgATMQtK1OaTkUWo0vlgj2WR8lb9IZrotN4Ka7isSAPxjjrlIc6khjUsQndgVNFYgeqDuZgc0tN0I3Q1ey9YIxjH5Bu5GQ4QbVE+EQeNZq7Qs2fyMk65Aej9ZqV8WTG/K3nbZpBL+PqCPO9xSonWVOidSeWTECfcZHN32gzbzkX1fwh3rPi2/Aeq5i63z+qv5gP7Goo5ztkdd4aM5b8LXPDE+Y4kUo6Q9LQ5GxnrQzqTb7Vc5GRbZgmkBrer92mrV5Nua+b3VFu9vx1sch02kTnlrW+NTCQT</BookingCode>
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
                                    <Pax IdPax="2">
                                        <Name>Passenger name</Name>
                                        <Surname>Passenger surname</Surname>
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
                                        <BookingCode>7Vor0/GRKZ31Va+BuE1WMFvq/9heAul4psoTS3hesB97bKcS8vVV8I7otP/319flrdJtWLiEoO9sY2UlyEo7AAymB9ND8KjSvVdFJpcmOjuKUqVr/8yLd18XaMWgIm9ykB2/2g/0Onvapv6hMcEHoXs5BhlCGUoz/Z/KXF7JNVlV+9a7KKaJiAGGLM6E4zfHVl/RdjeqUbhydDJnq5PJf2QrMA52s3SDutdI7FB7CycX6cHD5PgEgJCB5m44vLDWUcCQeNfCiFR/B4YEIPTzgKS1kABi+bohfi0PYWOea77SV4hxTqsMwzO7F6Bp5y/zODywYO553kRP+rmkAhvV8AYEgqiZU4FKMn61KyDecK/PqdNH0uxonkgFbtgia40+Ow+0to37wizUqCpOFGtGBqn19yXqdm2yiGae2e98RN8uY5RIGeCj7jsgYcAJNMEhscFdx64WTpLetI8fvoHfq5aE6u8/HgVLSucRv/4YpyIKFs7K21B5QnD7LPjf6cwsxwkITvRTRVlwI+IZNpkKqORJwvp3iJ+6rG8vtuuR0emX3GkB013iKERHjX4+PEY9iG0MbjidOWbAmeewbkPUbIGK8nAz80AP8xvhbmvXCJcThpaAmc2dTtCq1EZ+iHCyNX+3AhXWxiTaaUBkriA96MpxteElZgSefgATMQtK1OaTkUWo0vlgj2WR8lb9IZrotN4Ka7isSAPxjjrlIc6khjUsQndgVNFYgeqDuZgc0tN0I3Q1ey9YIxjH5Bu5GQ4QbVE+EQeNZq7Qs2fyMk65Aej9ZqV8WTG/K3nbZpBL+PqCPO9xSonWVOidSeWTECfcZHN32gzbzkX1fwh3rPi2/Aeq5i63z+qv5gP7Goo5ztkdd4aM5b8LXPDE+Y4kUo6Q9LQ5GxnrQzqTb7Vc5GRbZgmkBrer92mrV5Nua+b3VFu9vx1sch02kTnlrW+NTCQT</BookingCode>
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
                                <Route Origin="39681" Destination="37786">
                                    <Segments>
                                        <Segment DepartureAirport="MCO" ArrivalAirport="MAD" DepartureDate="2019-10-28T10:00:00" ArrivalDate="2019-10-28T20:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="1" JourneyDuration="P0DT8H0M0S" GroundDuration="P0DT8H0M0S" Class="FT" Cabin="F" />
                                    </Segments>
                                </Route>
                            </Routes>
                            <Prices>
                                <Price Type="S" Currency="EUR">
                                    <TotalFixAmounts Gross="398.3" Nett="398.3">
                                        <Service Amount="398.3" />
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