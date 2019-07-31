### Request
```xml
<soap:Envelope
 xmlns:soap="http://www.w3.org/2003/05/soap-envelope"
 xmlns="http://www.juniper.es/webservice/2007/">
 <soap:Header/>
 <soap:Body>
  <FlightAvail>
   <FlightAvailRQ Version="1.1" Language="en">
<Login Email="user@mydomain.com" Password="pass"/>
    <Paxes>
     <Pax IdPax="1">
      <Age>28</Age>
     </Pax>
     <Pax IdPax="2">
      <Age>28</Age>
     </Pax>
    </Paxes>
    <FlightRequest>
     <SearchSegmentsFlight>
      <SearchSegmentFlight>
       <CountryOfResidence>SA</CountryOfResidence>
       <Routes>
        <Route Origin="39681" Destination="37786" Date="2019-10-28"/>
        <Route Origin="37786" Destination="39681" Date="2019-10-28"/>
        <Discount Resident='true'></Discount>
       </Routes>
      </SearchSegmentFlight>
     </SearchSegmentsFlight>
     <RelPaxesDist>
      <RelPaxDist>
       <RelPaxes>
        <RelPax IdPax="1"/>
       </RelPaxes>
      </RelPaxDist>
     </RelPaxesDist>
    </FlightRequest>
    <AdvancedOptions>
     <ShowBreakdownPrice>false</ShowBreakdownPrice>
     <UseCurrency>EUR</UseCurrency>
     <CalendarSearch>false</CalendarSearch>
    </AdvancedOptions>
   </FlightAvailRQ>
  </FlightAvail>
 </soap:Body>
</soap:Envelope>
```
---
---
---

### Response

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <soap:Body>
        <FlightAvailResponse xmlns="http://www.juniper.es/webservice/2007/">
            <AvailabilityRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-31T17:32:09.2338093+02:00" IntCode="frZoA95VzHgWEpq+cG+bm5Hm0QxcB62WxVIHJsnSBcI=">
                <Results>
                    <FlightResult FareType="CHA" AvailableSeats="20" Number="1" Direction="Inbound" LowCost="false" RatePlanCode="LF6j9ndyo/zlz9tkRLu5T4vcqg4Y3XWeGauWGUmxxJy33kAWihQpwFONCEgQgZ8jfv40vfGcKGOk7ka1rxIDEXg7QesDFSWc5nEa0vDCS1/LFsyseCHitlCr7+pLnA322h8INjUBcByLNL7bj0G2UKVPv52hDqhjPJT6UH7Mi6JKN54NMQkBkHq6Ob1kiTayBGCdDZtka5GLp6NIxlK/pHnaopzhK9A/deyntKap/qlA4mAi+7tJif6Fvt7K6/JoOCaT/aCphk+xb4kOwv3xUKUvmCxOwPQPuWB4fcub+U7VrtTx74QGQvzO1jnZkHTh6T7nFCM8V6htmVJp36+OJaHXSA0zBl0m7Rb70WbLEAM5tk9PkoKrwheJbPKmjrImQ5VMYRNGZ4lQdEMKVxGTntPJI2fuIOX2rOrxrRYCguLKGOYMZFzWf8Uxf0AxPOn4NbOsme1fBHZiCx5FCdiZdFD84tQOEtVxy+DaJ6F1ng6QR8o6HqGTtAOReJNbUNS+SLcJ8ON9+JkajjlzqORg0C6mPC/bcgDt1h70oIs4q/oWdjQvaONiAeBcI0xx8uXrg8axpZyEG+iCEvB8WR/FJuSwtceXVAP+aZbhr53/PFtkU3q9UH+DFQO47mkRzlI+Ij58m8A8ur/jIxTpUJbVWggQIJc/51A+Ww8/6bhb42dzxF1vpyOvc5qaEEBvGYIVs9CyKkfR9pTreOF2obH05bEVd+n1fLY5cwyEyJy0yxgismMDZO+q4Bh7nOiPgzCOI7E2cSuzyyMZv/2lBBT+BfA9yJawF74Has8jGfeblllWXtL+l2Npyh8v0Vo4+a0WXwXcR41pxt2FTs5OIbUuiwfqDP0rKkb9Y90GVPmxdRZKmmSsyeyiVugC2F8ykijtGvoMQmuChTbyeQ5UWwiJ7JrD7w1UFMG8vnJeNjIZ6Yo=" Status="OK" Source="ChV2">
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
                    </FlightResult>
                    <FlightResult FareType="CHA" AvailableSeats="10" Number="2" Direction="Inbound" LowCost="false" RatePlanCode="LF6j9ndyo/zlz9tkRLu5T4vcqg4Y3XWeGauWGUmxxJy33kAWihQpwFONCEgQgZ8j3MYnbZCiHJVG3tYrqJx3gAPosmPBzsVI5OIzpAvkiulB6nGVAalWgl5mPQSB8OIia6OLPjVQcXnEW0L2qRv8BWW7jHBvzSls/GDusnFwkIEumIKE1fbipUafvcKQVBj+MNIRMp0FVMspq9s0mRHKctCrSQJ9TJSww8OsFi0RXJbfewB86icH2bzmogtgmzvzfz4c0U9eQhb6nThIhWY0TkR4/ILN2hN7TiNjyd2GnTuxI0dJEIx12lEcjocAC7Kg93brzi0eB2XqnF8pCwocO9fgkml9qTA+LHI08Jlp1KyvnQN9IxA4w3X9vT0HV3sNIi9ulvLOZLGSqLCtpWPP3iUBx9JOfAYewvKf8Iy9Kx5SmNpvcZh0lZLP51u69CsAY/D06gAmf/3qHTr3/GK/NuMUHCS7IGzKVVfE2/1zwAVp6GrUob969rUxlM6JohV+l7vvMbk7EE7Qg+qCSZ9XGwLHaCzG5zNFdWgE+9Dq8xbzwZzQCU3BG1Tmv8ij1+k+nJcMWwxEKUxRfL8dGS1/a4WBQsZs6UfGQlY2YqnxgYpxDvkiu9+/nAKjEvm1dM4z1WTbf/7zac4b4Tf8J+W1727tMyMLn/M8l2GQQm+vSNm2+tzj1DxOzSj/m47SoHLDDwnBcz6X2wASWDgxuuAfGOh+k+fVkRq8OFtrrjD38JKAb+BWonF1Znt6Lum21Nd0ZCzEbu6bPsJoRqbemj7dEmeAHt+Z/s6TzoMoaGgosQ7lshidaPgZKNCS5BtLR2v8CZ9/4FAc4HokLMVoyuaAmqNf7iYClPiRvWhhF60+kLE8kKqrLwZhUznQj1DqkgaD5NXcOE4jrWMfk7e7KKlh595Y2YY/+O4CHv512ji/6hw=" Status="OK" Source="ChV2">
                        <Routes ValidatingCarrier="EI">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="MCO" DepartureDate="2019-10-28T10:00:00" ArrivalDate="2019-10-28T17:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="1234" JourneyDuration="P0DT7H0M0S" GroundDuration="P0DT7H0M0S" Class="A" Cabin="F" FareBasis="300" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="94.33" Nett="94.33">
                                    <Service Amount="94.33" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                    </FlightResult>
                    <FlightResult FareType="CHA" AvailableSeats="58" Number="3" Direction="Outbound" LowCost="false" RatePlanCode="7Vor0/GRKZ31Va+BuE1WMFvq/9heAul4psoTS3hesB97bKcS8vVV8I7otP/319fl6BC6vvGMUPLaXp8off+mHe55hHlztUr+XO41PpShQY9twXRcaNMtyL/W0gwalo98cRThqH47vVoOlNpIO5qqhLjd4qB9do8m+pSjgiicEbsagH73p5yo1j4/jKrTF+a8Qqo/VJsW4TCiL6CoHKUTdO3LjzjHuULW++rIhIhjGPgoJ0/lHSfOnTsbt1cguoJcNg4iEtar/JEznuCsg9Zbq1a9WbCFQhYO2ucYuIguoj7IApfoV/TOaU0HHGlUNYzMEtWFterVEf8rzuMs2lTZOAb+u0kgVHwYdE9nrHxTwErKBAnVwW0RItkVzrJ3kKV4F0MKlmnWyl4oZo/aU98TPa9u0uWxa9bLvd7yopbKDMRquCId5psBxbnhgeMoznMyh91ghDnkWr1XdfqR42vH14Xv2dXMSHA2tpCAf1Ei1S588+VeuOeBf2nE/OVdDoCefZCIhNb72L5t8sL7mA1dJm9bHgbT67IU4gmiP4YGugbwNQ0Brh9RXmjU5OVi57ebo34Hlwle7sBaruzgnNNJhaP4aYawqhMfeyaco5HRP7dotRVatmcK3JZ5Z41WORJT2cVSSUQlDDT1MZuqvXGCFYePkn4g5EYOOZ1cYzU0yw+2MUZnWWsJiSKf2MzAiK0L+lBSfNbsPdWn/WGD8ACX8T+4REO6mCW/PQSb5Sm5EWT4octxIO1ozMXFtqIRUH9BNUN/5T2iVtKFhVTa2KmmrnaVy6VFEjD/lC/FqdRQqE3ztREMHeXOEiKqz9XOlRWopqtsu7qpuysbIYBYBd79dArSe8Tn5l7BS+8XeQI58+Yc/Kv5YBG7e4iW7QrrtTCXv6SqZ336lxU0Sx4yXIklmQ==" Status="OK" Source="ChV2">
                        <Routes ValidatingCarrier="EI">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="MAD" DepartureDate="2019-10-28T10:00:00" ArrivalDate="2019-10-28T20:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="1" JourneyDuration="P0DT8H0M0S" GroundDuration="P0DT8H0M0S" Class="FT" Cabin="F" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="199.15" Nett="199.15">
                                    <Service Amount="199.15" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                    </FlightResult>
                    <FlightResult FareType="CMB" Number="4" Direction="RoundTrip" LowCost="false" RatePlanCode="7Vor0/GRKZ31Va+BuE1WMFvq/9heAul4psoTS3hesB97bKcS8vVV8I7otP/319fl6BC6vvGMUPLaXp8off+mHe55hHlztUr+XO41PpShQY9twXRcaNMtyL/W0gwalo98cRThqH47vVoOlNpIO5qqhLjd4qB9do8m+pSjgiicEbsagH73p5yo1j4/jKrTF+a8Qqo/VJsW4TCiL6CoHKUTdO3LjzjHuULW++rIhIhjGPgoJ0/lHSfOnTsbt1cguoJcNg4iEtar/JEznuCsg9Zbq1a9WbCFQhYO2ucYuIguoj7IApfoV/TOaU0HHGlUNYzMEtWFterVEf8rzuMs2lTZOAb+u0kgVHwYdE9nrHxTwErKBAnVwW0RItkVzrJ3kKV4F0MKlmnWyl4oZo/aU98TPa9u0uWxa9bLvd7yopbKDMRquCId5psBxbnhgeMoznMyh91ghDnkWr1XdfqR42vH14Xv2dXMSHA2tpCAf1Ei1S588+VeuOeBf2nE/OVdDoCefZCIhNb72L5t8sL7mA1dJuU8Xu8yGnyyNU2vE7ylYQ6PiU1Gc5YrrdAxq6SyTBWV7Bmst+pwo9P8sCqjSn2D1T1u9ASaSkr7NKzvhq8erJLRMdDucnSu85fMaacYyaaMHyX4iV6gP8+mDYFXe4mRxYZxW3g6OAiY4jvQiugO3PPNWk6ED/nBFrsHcAHEKFuqaNF4/QAn6Cq/+m2sWQUN4fq3q+6BNkUg//jgNAHB/HCPFF1YSLJDrYssFBiLwLS2Hn1k6Bt78kmy5nx4B2rNxeUQ3A/EHk0xGISfzW7VMOi1/H6AMt54m/Qb/zfB5bH7ISA7Vcv8v+2OuWYE0y1OMurf9e1ZIEI/sQVmJwpF3mowUdamo2nayH2kfRudaYPBMR2rOwNHP5ciWSDJM3tz1rPNFLQEK5U9ija+sxaGUXM9kaC8/HPz1TGd3I/4xKnvEELlgypqapXwmgTGyp85Ue2A9OD+ae12YA10TtdBrRsMMdkmKjSpJlCxu66X+OFJzH66K9msSsOFxnAtrn9M9FTveVCcP/PHeZrzFtNz/xXh7gue4VIHOCiQHo578MPVDuJuXtxR5RAOTA4FigjhjojavYHBnS+XGxn23U33UUWEBIlG0LZI1fua0SC3Bf41geyeQK8iK/MJqh744Xc7CiKAlfcgXeFXQyQ1Cg2lV4V4Qju6NhX9dYBrhMadf1E8xE6jKaXKnElrnIEZCBM1dpuOOIWBLPk2nKgJ8ls4v6SyQN7/QnSBfCbwk0IDXp5dQvrbOkpIkYnc6M13iwl+QUypGtJqpay9ixfOffbYEbBpd92i3dUA1eCEd1/zqokq13djntKotOZtQw5zAIbuw7A1MFCH5uZZ7P2cncsCb1pbzLUJ5RxFLsh1WW1iuw2uejiswdxFnclB2x4E21Hs171jLJO7PoZK+MiLMbqmvENNnbW3Bg4Y1WmqJOZ6Tw3kAayRwLu+9+i5osDNci7y1AbbdMg4N3hvVJW42+ap8BN5F2vkgvgBexa9t0FM9VjQsf2xPEzbEyUysOnaqnFXr7uavCBMsHEWo16qgcVCIPUp29lGuX4n/HYwE+5RUFiz/4J0RQbg2JF0ITvUA7HF7le8+UQTUhrMcWRtW7yMKJz49GQfUUA56zEUP7NLbBdam0ADPfO8UhJSEkdSq7sPfsfU2jAbMQq3qtR/7IkPVI1oM+TSJa+CASn0QDvOvhLUE9GN5ePY+5GlqHx8U4tdmdtIqqQ3uL05amQBuc0ZwCr505zWJkBn/uiTuv7Tnhvf5s+q1ZhwCFxz8pU1J2qq+sSspFXlwERhh4gSeI1G/N7JNI+Q3GrJjnv0cu5AZh1f" Status="OK" Source="ChV2">
                        <Routes ValidatingCarrier="EI">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="MAD" DepartureDate="2019-10-28T10:00:00" ArrivalDate="2019-10-28T20:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="1" JourneyDuration="P0DT8H0M0S" GroundDuration="P0DT8H0M0S" Class="FT" Cabin="F" />
                                </Segments>
                            </Route>
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="MCO" DepartureDate="2019-10-28T10:00:00" ArrivalDate="2019-10-28T17:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="1234" JourneyDuration="P0DT7H0M0S" GroundDuration="P0DT7H0M0S" Class="B" Cabin="Y" FareBasis="200" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Recommended="0" Gross="246.32" Nett="246.32">
                                    <Service Amount="246.32" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                    </FlightResult>
                    <FlightResult FareType="CMB" Number="5" Direction="RoundTrip" LowCost="false" RatePlanCode="7Vor0/GRKZ31Va+BuE1WMFvq/9heAul4psoTS3hesB97bKcS8vVV8I7otP/319fl6BC6vvGMUPLaXp8off+mHe55hHlztUr+XO41PpShQY9twXRcaNMtyL/W0gwalo98cRThqH47vVoOlNpIO5qqhLjd4qB9do8m+pSjgiicEbsagH73p5yo1j4/jKrTF+a8Qqo/VJsW4TCiL6CoHKUTdO3LjzjHuULW++rIhIhjGPgoJ0/lHSfOnTsbt1cguoJcNg4iEtar/JEznuCsg9Zbq1a9WbCFQhYO2ucYuIguoj7IApfoV/TOaU0HHGlUNYzMEtWFterVEf8rzuMs2lTZOAb+u0kgVHwYdE9nrHxTwErKBAnVwW0RItkVzrJ3kKV4F0MKlmnWyl4oZo/aU98TPa9u0uWxa9bLvd7yopbKDMRquCId5psBxbnhgeMoznMyh91ghDnkWr1XdfqR42vH14Xv2dXMSHA2tpCAf1Ei1S588+VeuOeBf2nE/OVdDoCefZCIhNb72L5t8sL7mA1dJuU8Xu8yGnyyNU2vE7ylYQ6PiU1Gc5YrrdAxq6SyTBWV7Bmst+pwo9P8sCqjSn2D1T1u9ASaSkr7NKzvhq8erJLRMdDucnSu85fMaacYyaaMHyX4iV6gP8+mDYFXe4mRxYZxW3g6OAiY4jvQiugO3PPNWk6ED/nBFrsHcAHEKFuqaNF4/QAn6Cq/+m2sWQUN4fq3q+6BNkUg//jgNAHB/HCPFF1YSLJDrYssFBiLwLS2Hn1k6Bt78kmy5nx4B2rNxeUQ3A/EHk0xGISfzW7VMOi1/H6AMt54m/Qb/zfB5bH7ISA7Vcv8v+2OuWYE0y1OMurf9e1ZIEI/sQVmJwpF3mowUdamo2nayH2kfRudaYPBMR2rOwNHP5ciWSDJM3tz1rPNFLQEK5U9ija+sxaGUXM9kaC8/HPz1TGd3I/4xKnvEELlgypqapXwmgTGyp85UTK3aMCzgBfOrSK7XEeBa6N8IpJ6wLGLHpUgaNty4OEv2tkpGEPRQntncnvmtZ1u9w3wvj8axeJijZmMRC/PhxWy/5wohcq65uQTRUHifGjlV97d+OuBahVRQaR+2uaJe4IyDUCog1BuznfoueHMkcUb57rfyhOPogEtricbrw3AWn/9pfFkNUX/LohI+MFcEBEMyTmGygegIsvijYRIPyvXBj/mmYNCNDdCVlqnWoAEA6nmnZEpu068mMcCcTl+BWCt7lNVkStGFZvB01ZdlH77HgLrDqAkPFD4J37qHocd907D6x218Lh8wYEwNaH/T4iCAMIKDvewRE30maAcmvZRoaW5O2DAzs1T0Hi9ERbT+8HAVM8Zzvc7IVIqNbdXTynA/eWCyRcSUH3gtl+eWidXZWYsywfX/wmTELUmkf3rLtuU5VmIww47Lcr3BYdOofCckezbWeRY7DmAWIqO/d86lGHoxoZF7dSKpKazB0r80k6FEolMzW+6QMfnFG8lF3uyXzi+AeyRvHGsTxlc6wL8p+n582RyiYAaQIOUJZbQBpnx8QrYUJVFpbPh+JgWyBTnuhvEk0+p+YlYzmAOpZ4OaYIt/HYW8d24g6Z9KzFtkXB6U6c+mGJwMzyM59vReqn6NoJrj2IxHy+HS0aH85Qtya8wPAmw7S3wzUTrTFiYVuorlYc8FIPuS44oVoy4zRBNDriRW8LjbK8BjPUJoYDICzoz08nLllNGnj4dMdMtolbwH3uGom2Pgges+ieQUrFWaN49ekmQpHipI0anlcHmGe/0XmgIl3wth0MJc13vv8MYb025ut01FlWOOeiKuS/3h1WMUB8hK3CP9mYOC2pmErAZ2aRHE6LfTrYwKa2n" Status="OK" Source="ChV2">
                        <Routes ValidatingCarrier="EI">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="MAD" DepartureDate="2019-10-28T10:00:00" ArrivalDate="2019-10-28T20:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="1" JourneyDuration="P0DT8H0M0S" GroundDuration="P0DT8H0M0S" Class="FT" Cabin="F" />
                                </Segments>
                            </Route>
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="MCO" DepartureDate="2019-10-28T10:00:00" ArrivalDate="2019-10-28T17:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="1234" JourneyDuration="P0DT7H0M0S" GroundDuration="P0DT7H0M0S" Class="A" Cabin="F" FareBasis="300" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Recommended="0" Gross="293.48" Nett="293.48">
                                    <Service Amount="293.48" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="6" Direction="Inbound" LowCost="false" RatePlanCode="Ffa1q3POCcyi2Rus2m2aUvvI4k+C7do73FaJXFWc2Tn+QvDhv+mN5m0dR9RZVrSWhmmot1bmMGB3tNGJ0lxtjEObdTuW28HdkC7Szlutfj3pnZAO+gGWdUqB4zusCHSUNBdbYc1pgK65h7ktntehyX+unm/BsDgW+j7X/eh5ZDVzAA8v2d//2OYZKvxKVaqj/8M+9vO97BxVM1tK3rHylhojfrd/msaOwshiQZyhsySXEbPTN1ie7LnI8gIdV/kbEaoWgPl5c3SNIu7GCHN1KIMz+4gEaeA8nysrRo9gRQlLv9Y92+hIo3lmm+Gr9gtaThCok+F0+PZ2TIFYGKfjxK2o/hiPz26TEj7Kpqc7a+qnrkdKxcY42DZ1k5kYaJBbFlYjI7YmLpB2/EqLN0d/8TNWCbJ8PNFKGoodt1PT2zh4QbZjrL9awqjW7ctdZR9e+IwRi9wI4hn9m9/T9iO0tVP3OZ+hlUdGBXzv7skxLX5CJS+BSCAmJB8eFXwpIEskIr6l9xZEI9rOJ13uzRIzPI0cjITq/BhaOkYRbYupoZfbZvhSGOl9dMtVEjY/RNFher5TEC1zzPqVqhgs2jlw5285YFHWX0wUlVP3BzPcbAxoZjtCJJbuSrG1a9UgTD/OOeymRVeB852MwX+JUq1aHuqGKORyuA9VoWh7u7AYcMSIEuPEp7r2AUDKJ47a13uLIB2isr8qf5woLZuAzWPrL26G2tKtH48wTmswMlpd8ThB5zFYJtAxj70y1cWP0vbEOSxRVHD36HuMi3OUTCgllzCnP5lGxfWuFhjkJUjuu5yS0dTC8LcQvyxZWynUSjKS/iFOscjTGft0nAUcPM2yrTGz4Z/KuEspQf+ntHpBJ/elpghQS2TIE4qtKnuhU/D4xJOFRHFZrIDPmfJq0iH9V2i2YqNLFb0H50mT0TRhUXS5jOx+572jqTuKFmZ8U3+SYqXj9esg//zhDJMct7f1t2MuaWUVlOtoKIwjTHKQLyeHXjGLbjNFz0kIS9geKbnM28ljVzJyHhVdfaEGS0w5I+1vdoBApd1vegcaZf6Ry3JHZDnTvN/OonsvlH3yhwTkXjUmtI7mb+jS3pwrBdMmh4BwtjJ66jtpqEHsKs/TXCxA52xxMCIDAFrNASJoKTDzT5DOqr+0I7Z5kq1B3JpzxnpnNOe02JOAXX8eNRpfWjXpxmokXVWCJ2JkViRinJcNlIaGcyV3XtE7wdzklgiKnjBP6vs0EUQfuZcf4ZGp28vGikfklHBvrMxPL75gMqepNh9o0sw+WPBcV5/HAU7DwSaf0EVfpd2diAhNObwoPSTHhQSxy9f8EXDqFUrndi2V9aR5P8VXmDvmn5R2GkZvSrlq0lVzrEFUXTt04jPmRCk7tECqNorQEimg2dINWkR3jegD7As/iZAhs0/CHDKoZzFPdgGlJ0ctm7y+JdlTs+/IWdH7ArRJqJ/jJHmwS77oi++IBaW+sNc+TQNr5RRLYZMJYFshi03JfGrs/NRv5fVPVfk/SRHpBejGIgBwd2/g+W17gsPUL5tMAkZP3pqBLzQFRiVvEQV/rBWaTltQGQYRr3KlYXDPtDhrCPvizQgMXWFVG4BCAENLt94Pmipa9M1ix+EDGzNHm0HR/ogN3mgqcre4tUY0nnE13rT3WoS5" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="TP">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="LIS" DepartureDate="2019-10-28T10:05:00" ArrivalDate="2019-10-28T10:20:00" OperatingAirline="TP" MarquetingAirline="TP" FlightNumber="1011" JourneyDuration="P0DT17H40M0S" Class="U" Cabin="Y" AirplaneType="319" FareBasis="UESBSI0D" />
                                    <Segment DepartureAirport="LIS" ArrivalAirport="EWR" DepartureDate="2019-10-28T12:50:00" ArrivalDate="2019-10-28T17:05:00" OperatingAirline="TP" MarquetingAirline="TP" FlightNumber="201" JourneyDuration="P0DT17H40M0S" Class="U" Cabin="Y" AirplaneType="332" FareBasis="UESBSI0D" />
                                    <Segment DepartureAirport="EWR" ArrivalAirport="MCO" DepartureDate="2019-10-28T19:53:00" ArrivalDate="2019-10-28T22:45:00" OperatingAirline="B6" MarquetingAirline="TP" FlightNumber="4333" JourneyDuration="P0DT17H40M0S" Class="U" Cabin="Y" AirplaneType="320" FareBasis="UESBSI0D" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="477.49" Nett="477.49">
                                    <Service Amount="297" />
                                    <ServiceTaxes Included="false" Amount="180.49" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-10-28</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="7" Direction="Inbound" LowCost="false" RatePlanCode="Ffa1q3POCcyi2Rus2m2aUvvI4k+C7do73FaJXFWc2Tn+QvDhv+mN5m0dR9RZVrSWhmmot1bmMGB3tNGJ0lxtjEObdTuW28HdkC7Szlutfj0yx862kvRQrQCdjJ/MMmY42oIKRYB8ZzV5SxyG1LABf23JMzCOPAmPxagp0RFYzXrEnWplSAAX7+GIwvQBFInUsRIOHBQm2b5Dgp8h5V8fSaQBtAMB6ywDmds26vJKuqOIORFtYYPj7pGW+F21sGNP/AA2LFZQFdcSFra9xVZi8ix+IUGL/VMFuyzMbnC9J+kkkrRtCheayd2XqhxnfDO1nPRUHwXq/DegGq+xhh/yIrujPvJLyUrCbDlJq0NFKSnF0dcA7JeSAfYzAtxEZcwsao/Pt72Y4IiO2HEue3sbr5a5v9CBgCJIyRvletMFNMIOZZE7Yjm6+Wou4pH/s0OL6s+AGv3+D70ms2VHkq3HHH/J37A9pg5Wg/Oyn2Rkdj4BZoeuYoGy4k0HiUged7Fx4yg0r8qylI8w3awY4BmfNS3cy0fT76JI97VwUA1mHCpZq71P+t+t0VoPTR18+4Ga6IcDiZQ/87sBtmQ8MUEFjUHjDbOA820OTIfsCoX+7jkKPTrMttLmojgxtehg08yiINm+IbhkNgkJUoh8EM8e4xunzH8QIDdz099zBD0I2rUGQ7Fg++dfeoiObkUQmcNK/hgMP/si6lTVkBhKc5AAyjoIVS3hwDKGuDZv8wuOl72QaAySIFo/GE8S/3jfMzc05dvdTzsCOrVT28hIhm+akHK3azsWNJXsk/e9Pt1OtPAWXO1xNa1dDz0VRMtDqR1RubYQOsUrrTIond6TrAfF+JIjBmLq5RdO/kM7RbDZ87UPbbGoXCLpIgyqGXmdCuNndHjmOtA8AoBR9AKeVTvFXKhj4ibuVYcevWOtEpL4TgwOU+2MppEsL8seSYSPOVZXsV+CjFU35M3GgY/knrFZj3NLVESOzPwXOxpdjewvZLLVtrsYZBo9SjpigwwfCbXarFvYVLFQBNSvSIoXCVfzu+NGWz/uWbfyi5fTWaPlf4GVuGRaiTYIx5ZF/L89jsk+b/ijZxemswwvUI659hrJ/uOddwwJtrdz3gAmJj6ape5oVsknBM+c3EOOzAtmgqa15IXTjesIOU2RDXUN8y+bDZlQfGoWhxqWdjSJFZLPilz5z1qI6Q+HNwUxmL8+Ka7uckYfuryb0YCcul8G8SzynVMJXRXtch/pyF0UfOsLocdJwMS5w2qo1pNzziZHaj1fzsXQlMdt2sIxNCAa4stn+KLM0C00o1urlDyHvIsjyufCz+wlrLpPhC0+BX32ix7x7RncRVTdByVLERMXjHDdWlk0dqjYb7votrHPrEJU2yNgiX5139ZrXLBtGIwhi2mTH22GuKctQdyhz0qYpX+Y6yKp/A3X3Kw/ti6oluVpCXD2QOpJlFRfyEglBrq2yYKqvsEsRwmoOSjbQeWPgqU6VPLLiNK4lTVo0UBPZjmno9MZPCZbkhw3PoW13dmkRMHyhEGOh50uNd3WBbAcq2CxrHomrej2V+Ilg4sIMFzjFLpHhfHpQzyw6IHDabkAihJMfJOdT9bnZwxTR3kYm0ndv1GLAE9db4emPrBkOUvS+Kj8D0wiNGd91U2VSxo4TB1C" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="TP">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="LIS" DepartureDate="2019-10-28T07:25:00" ArrivalDate="2019-10-28T07:40:00" OperatingAirline="NI" MarquetingAirline="TP" FlightNumber="1023" JourneyDuration="P0DT20H20M0S" Class="U" Cabin="Y" AirplaneType="E90" FareBasis="UESBSI0D" />
                                    <Segment DepartureAirport="LIS" ArrivalAirport="EWR" DepartureDate="2019-10-28T12:50:00" ArrivalDate="2019-10-28T17:05:00" OperatingAirline="TP" MarquetingAirline="TP" FlightNumber="201" JourneyDuration="P0DT20H20M0S" Class="U" Cabin="Y" AirplaneType="332" FareBasis="UESBSI0D" />
                                    <Segment DepartureAirport="EWR" ArrivalAirport="MCO" DepartureDate="2019-10-28T19:53:00" ArrivalDate="2019-10-28T22:45:00" OperatingAirline="B6" MarquetingAirline="TP" FlightNumber="4333" JourneyDuration="P0DT20H20M0S" Class="U" Cabin="Y" AirplaneType="320" FareBasis="UESBSI0D" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="477.49" Nett="477.49">
                                    <Service Amount="297" />
                                    <ServiceTaxes Included="false" Amount="180.49" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-10-28</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="8" Direction="Inbound" LowCost="false" RatePlanCode="Ffa1q3POCcyi2Rus2m2aUvvI4k+C7do73FaJXFWc2Tn+QvDhv+mN5m0dR9RZVrSWhmmot1bmMGB3tNGJ0lxtjEObdTuW28HdkC7Szlutfj3pnZAO+gGWdUqB4zusCHSUn9paWjujwKOWapmEj0xJvvm9wh8ARs827VStMXEbfi/w6NgVQoj9h4L2Bble010Safr6TMJBFL1bfw2kTLAUK7ESORjkScKXkSwKiLtYLVTJQ1QnuOX7sXlmri9RH1bwUbhm5qdSQGNSObAWrAObX/ixZQFI8mVkdxXv1vm0wDPiEhFQECArkdFJivDxFd+/lSIfrnK9UaWmhrG+hJ1MRArinTjrbf7LWrlIReWzGvF+AcInGGk3YzmAcvdaifPPl7mH3HYUH9WLSBABq2wvz0zqwsMEfxZMd1ZSondcjAnGL8wOPkUlPCbG+R66wFZjnC6yjL5tXHOC8NAcQlNpVmX5NL35x7X2y+Z5rxcKqyzg22kCeqkOcbQe+6oHl/MpvR18HzraEuOyHj9BynChsIFMf5GZ2hNEflLQFluHTKlL90OUy061YOaFGa/dPKq+qOgZzNeY9BoVLYbqbcQcPMfm8RzfDPYVixSzd5Jby5Z5vnoOCuqsCRPLFIeXXHTTA7CTy9wicTrWv9sp7nJdCsZD8fHuMKL/ELLZIjUKC4ZZ71OcvKVFLCoQQmJN8tD/O0VX88Cz+hXQ75H5QcG1TNu7RV2EO8I7YRgpgQLbsUkXHYjnwhQN8JKbNWrIQE6Lq7+wtvHaWYPctzuav11UwcuXFh/0SeQrd1d9RyvaYpH3lZlSKBHvfRb1UZe1aZe6QiusbsfNG8jMxh+ucgu0sKYiUV7CA7sSqwAwbv6YARhc3VbNiXvfoj0j+ZoFiFcL3l2xsN6SDZrvyOkfppqufv4AC3XvCq8y3Y4IKzSpi4/yky2ZSXYswUdFMiWUL918TNtrMLRqlNHyTIlp93937kPrkYJ6Yv6sc/xz1TGnNsdIfU4bL4PC4KuEtxDOcjGfyeOkBnI+PHfJdDCXXP3cB9+FuAg87pyRR0IundupxLGsiJLWVKFxYoKC2t1QqxNyuPPfWdwo1F8iyyvy6me6nC5O2DXyD1sRm3e+XcT5KW63CSdhCd2O3ljrERZNE504vbTilxXdUX8wwM6NBAyPsyfPXFFt9mLUHqYaKcZ8cHmiuI7GM5vDOGNpcqUaiXdUaWo63Z70g2m+4rpixmFdztASIxqnLRffjtg2f9gHbxnt/Vsqc+IYhuWUUf7s8NgaMf3s+fsFzHPpV6M3bFlGI8GWraJeQX/lbi9hpHZrKI3/1ZCRzDFW0W6eAh/xqZ8k/2tVH91wGFX8eAbL7JBAKBmxER1XTqnfjiirNEX3reRzTtXUVL0Q0oaID9SBa2RrxcN/5yoIod7j+9LflKdmovyPLhQeGmeNn9/WwQzyUpU0PGII8ug/7myllGZvdVGnSRbXjbY20KTqmlje4Dkg3i0Vwhg39rra5+6aaBwCc8XIMIJZWXLWB5hA0IZd8FCGerSa2+TFLnka48uADDGYZdBm3M+K0sGP3tPGkAuOFkjFCeYFH+cwWeVoM5jrKSuK6mNrwhvLO4MLTxDNpPsz+Mcy33krwlzwaiwKXaf8Nru0Ww21ZLiNbkzvOLI6j/VM" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="TP">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="LIS" DepartureDate="2019-10-28T10:05:00" ArrivalDate="2019-10-28T10:20:00" OperatingAirline="TP" MarquetingAirline="TP" FlightNumber="1011" JourneyDuration="P1DT3H48M0S" Class="U" Cabin="Y" AirplaneType="319" FareBasis="UESBSI0D" />
                                    <Segment DepartureAirport="LIS" ArrivalAirport="EWR" DepartureDate="2019-10-28T12:50:00" ArrivalDate="2019-10-28T17:05:00" OperatingAirline="TP" MarquetingAirline="TP" FlightNumber="201" JourneyDuration="P1DT3H48M0S" Class="U" Cabin="Y" AirplaneType="332" FareBasis="UESBSI0D" />
                                    <Segment DepartureAirport="JFK" ArrivalAirport="MCO" DepartureDate="2019-10-29T05:59:00" ArrivalDate="2019-10-29T08:53:00" OperatingAirline="B6" MarquetingAirline="TP" FlightNumber="4335" JourneyDuration="P1DT3H48M0S" Class="U" Cabin="Y" AirplaneType="321" FareBasis="UESBSI0D" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="477.49" Nett="477.49">
                                    <Service Amount="297" />
                                    <ServiceTaxes Included="false" Amount="180.49" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-10-28</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="NET" AvailableSeats="7" Number="9" Direction="Inbound" LowCost="false" RatePlanCode="Ffa1q3POCcyi2Rus2m2aUvvI4k+C7do73FaJXFWc2TmrUuRmhwkftPZc0UYk2Gy10ARzDp+Ji4//SsrAzjEmVHW9qiZLxhKRzeFSU7EXuVwOlu+4uMV3EOiYzVl2K5yry6jNAVPcdvQsSS7wTvOHouf/5FYknFa/V6+FNGpnKT7S9fue5lCBuWmTmtHAV7nQlUcdxX9LHxUCnxKwO6iu9Wy76/rIIw2dUyZQdSujpvpFrIAZ7U+Iz9R4R275hvVyxpo9qeGqGnmL/gIsYSaOPRUq1oIJB1n+aet2gxVmuc5lgryffeFr9b5CncgHUgav/R5XXQnJt0SWo302tDLrRUd/Mp0RjYI7DImn4JBlRcgIuFuWRFyR5V8MH6wbxccK9bPF50RwodIIaIkSoRNOgJnqKUxjNP4Hoyz7EVC7Wep/K/WL5C/wbX6q5sT3rQ1v+o1oEOo5CK4mavvCuK8j1vXSIu+1WhzDSoJT+6lQiSwnP4O3+TT/U0r62KlS7j60BLa3ceTOEnXcJSwEVSI35oFMOfqqf1NLJ54+Nrc0wHMOTN/XuEgBMFFCr+ceQot5k4GGjz4eZU0vICB2B+Hpu6msHHqXwb7lEWT7yPOH/iQzkuSFANooOtHFyOmR7w8pwk6Fe60v8wMhaqgiN2rZeEe/PEyEBRYLZmBT+R06Ukp52jxaxPzYUndA+vpUdPEjpXBX+FCas8g9wQ5179zd1OkTlixoSTpzNUo4I2gkH1zEGzZKKvsX36+evwNRRaRjHSYEnqoDRbAQdoGRW5w3Jlv9gYvQobctXZ7R+cDEU/n9GGFSw5fPldrrHSVTl3td4unGIF1Qu7QiZv9I818v4qtpKcP51J0S05rKS+pcabfEpQTacdvDUCZeTqIurwFgX4XHuca9leQRRqxz7L7AGpkCTNI1YZBovpwmS3wnXHyeLl7Flof3SM6zgmlpgaFSImtxwGhg5pNjO20FVkUGUB174BOxpwoo4R0y+42LvOND/5iOnlti2EmstJrT4+ocKUPN8aP3sOvtuV/EvsXUqxwTrCEYrmCdTBDdlTSeVniY3UtgQycY0Md26/QfV12OgOCYrR/hbvXSV1XCbuVoPdV28urc6+ZUnrlD1blxqomaghCS3dU+WCPXC2jPbkEYITfQsJ3B4MBgVh0Ziz1Ch1NBgwp/ojAuey7UnITegvItRL2G9beVaBEtSLBakE8LVLQMyasUXrsLU/zxBJrQUCUcEiAVakvKRoDzebdMd1UA+KhNwMvwy7WBKTNbSLSWNirKScIJzSn01HjIdrqwSkJ8yIo1UX4Tw4KXehd4m9E=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="VS">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="LHR" DepartureDate="2019-10-28T07:00:00" ArrivalDate="2019-10-28T08:25:00" OperatingAirline="IB" MarquetingAirline="IB" FlightNumber="3170" JourneyDuration="P0DT16H35M0S" Class="V" Cabin="Y" AirplaneType="321" FareBasis="ELHF07MX" />
                                    <Segment DepartureAirport="LGW" ArrivalAirport="MCO" DepartureDate="2019-10-28T13:00:00" ArrivalDate="2019-10-28T18:35:00" OperatingAirline="VS" MarquetingAirline="VS" FlightNumber="15" JourneyDuration="P0DT16H35M0S" Class="E" Cabin="Y" AirplaneType="744" FareBasis="ELHF07MX" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="584.72" Nett="584.72">
                                    <Service Amount="416" />
                                    <ServiceTaxes Included="false" Amount="168.72" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-14</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="10" Direction="Inbound" LowCost="false" RatePlanCode="Ffa1q3POCcyi2Rus2m2aUvvI4k+C7do73FaJXFWc2Tn+QvDhv+mN5m0dR9RZVrSW1RuWfSuRHeS4rmzztPWf1Cz7YBywxXPAkbtPjdPvkG8YW/TuQymk8XEh4CuBNWt9OiBK2B8DOc0p1neNiodWBV8A5wUyC8GvD6PdPCKIHbdhY02eV16Q/ur4STS7IF3z1HjK0WUThY7AH6i2Fjk7cW+QRXkQ8ka3T1V3E8npy/qDVNaPwE4OXGh0SVPY4GQb7G8tbdl/vzPgAP/1eTEdDcv4z4liJI7WYIkHWIOZH9e7n11R2W1KolnGLdsOhrFrcjRvYtoqJJWDkOnLQ3ymaU141yx6fs7WSpy96XuPXAP6a2LaKbhZlLk/+QacpPu+clOxhWggVaDCnEJeqqqaLr8rdxnxkT5mxZaPChMY9Tsz1cT/F5isM8A/Pgw9w94LyUcCYfW50ZMBt6/mEnf3TYCxztP75qQWw0jiFF/TCJYvXZ11uHVcDsoWpkGZFw1X1ezXe5Hmn3/NrGSyVvq1nnFcUSGILcXyEVmC5ogErGuLWCXnHsHRuE0gv6yYWwclFI+f2BinxjIPno4/p0HEWMr8EKRy5K8wko2p9KMh5IeYJW9kiUt4dwRL8JxC6cmHLnYVv1BlkUtmhQGiE9M0vBLxuY/EJWje4CbRwVLfLNEizarFypAW8r1OsO9G3MTqkQEW4/daVFRJq82sSFY7fPJ3TxTUw2I5+7/AlwOLmYD1/nhxPNraSgz5Fg6s2ygWW/aqO9DCIt9jfhYYSIC7UBAcBA8ecgeZMnOGUnXXpXJS6BpQD3VRRWtrXYsU5bs71A222do/tt03LLSxKrFNtugsX+1TOyYGM3gP3uSFGWHH9iPqUsSqbnZ/rdLfuojYsIILEWC0UawYFMEOFxeA+78Nm3HB/AUQc+f/cifqOj8/QNGbKoHDonwY5SoDAa7cgWvI2IX5jiKlxdNXTAw24FajSApfopWPB9RYZqEN48iUZBgBUDCjaYcNAAMDbYNeIJRF+b00v1l32yPovWSnLbl/VCglxzSMF86vIJTNldmslWoEIbf2K/SSfymG88HrRmDG03ICLsurRu9oP82S9TojLKVmZvt4eaoumA9lCKDIVsJeN4RdSix7yGspdqO95sAGAwXXmHAzNEVT6lzl/fcJL538NDeCrzncZi/owp+6ikeomRr5EydAxuS8wzs0gbCS3X+sgH79nZonyqnM1n/gBnc2cDJ7F88cBz+CPq3Ys8qeDiVKCp009VrUC5sUeDLLP6FtZWb3YnOlOOL1tgJ54K96L3PyGK4Gn3edgZSa9cIGHteGhPUQ0JtV/sm5JbHgC+ibsQGL5Zkdryf3sWxCjvT2FUSp3ENLR4QB6162TtqD61lr+Tj6w+M0whhWSdKZ8f9Dma0drtKz4szW0YB5aVSOuMe9usB2pZB63mJhVv5I7mldl5gcVPZXlI8oslkyu0slpuxUqrUcinONQ/Fr9giZRqcVCYGTUkvAwZl+4gjZSzL8prJYEMzX6GS67/X/kz9jjAch66D8t/PasaiLJJNw3RV0saraY7FVAM9c9QT8K7tTbbT1HNJ9n7GwmwPHlkhuH9Mdu8o8TfRnvuQftrK+J6PfQ2Dxk1G5CEE=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="TK">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="IST" DepartureDate="2019-10-28T18:10:00" ArrivalDate="2019-10-29T00:25:00" OperatingAirline="TK" MarquetingAirline="TK" FlightNumber="1860" JourneyDuration="P1DT11H8M0S" Class="Q" Cabin="Y" AirplaneType="332" FareBasis="QN2PXOW" />
                                    <Segment DepartureAirport="IST" ArrivalAirport="IAD" DepartureDate="2019-10-29T15:25:00" ArrivalDate="2019-10-29T20:20:00" OperatingAirline="TK" MarquetingAirline="TK" FlightNumber="7" JourneyDuration="P1DT11H8M0S" Class="Q" Cabin="Y" AirplaneType="789" FareBasis="QN2PXOW" />
                                    <Segment DepartureAirport="IAD" ArrivalAirport="MCO" DepartureDate="2019-10-29T22:09:00" ArrivalDate="2019-10-30T00:18:00" OperatingAirline="UA" MarquetingAirline="TK" FlightNumber="8612" JourneyDuration="P1DT11H8M0S" Class="Q" Cabin="Y" AirplaneType="739" FareBasis="QN2PXOW" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="636.38" Nett="636.38">
                                    <Service Amount="378" />
                                    <ServiceTaxes Included="false" Amount="258.38" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-10-28</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="11" Direction="Inbound" LowCost="false" RatePlanCode="Ffa1q3POCcyi2Rus2m2aUvvI4k+C7do73FaJXFWc2TlJ4+rD/2KzSuxdxitOlL9ddKWWg+sJ4XvV2xAzw3QR3uSrwwTgqjPNHYYpZRO9Uut/0IXnqxxcwk4sGyXWc2NzFqlFhgz13hFPc5aAn97QjP/zo2n9lps75PCX8zapmzaGnMGvZ1C5SDoXS4qIBZf2JKhSc4p+GT133mzOTic+82/njQ3R9DzTdAdXrJ1brNJ77e4qjCvnPNY0lL/oslA+MWYMGyPvbEKnt/SFc/BtIUQCU2GEqgd8Ib5nOiAKEuraoj3j+Fx0IF30XQsOsvMrW+WPFSZ22qq8gjvhw7BdP9V1Vi9HsIU4APdCBzNqk1UCo9M/hfGCi1IPosS5+FydS2RcoCP6bOgDpdXrfC4047nq1SDnW+TumW1nJYGNAv1Vibl3bPBvpEIXYYeGq+lXdMD1FB/HECYNjW9ca4eL9jvGDnMSkZFwuIkOrNGjS7Me5y3TEmcSTeRClPHKR6PGdx+/nMSklsWEotm3LNXyXdmWaEy2SUDGn6H+S+N+pONtLbQwdzn1yDzO669HldSougl6/jlOOEgRQ7Kb10Tqr2Hgvv89c+qiupHJppr1aRm6Q96YHt6tmoEG4MmTWtiywL8eJyVKF7vE8FTO0DPbsUpjz48nfw+XoJviheS1I21UNZ+MAaEc3KjNQTwBrOmkjSA9rxSTFAxCRnuQy3KCq4F4DLJwXfX4doIVCjXtq4Dlgq7mK1N3Ei+4mxg/7WXZs2LM5w0ZxbVjhwRB8etX/792u5rGTpzvUEoN1f3L5MaWZkpDzQ8JGStSM7b3OtP9Raksy3dat8jwuuxAd0SyAkj3E8rEgrHt114kGInNteeeBmUxRq8jtbT14LMEk5dka5Prl1GW3jG4smpbhr76HMdbdbvRQDSQtQva4axljDSsbv5W1bkXRKWETtn9+6grJGp0aJqdk1RzwxsFNWI13OZym2uZLCY63G9aZABBxfk+KRoRy4hXDLxa2gUCvbNWwFo2YqkolJddEZ64IlXoluvDMqNmOkUTikT6Krf6Svvure/BtB5D4MFdzjKnU0S2sC0OKo8NiEtJBaSujCO+qH5RVDh1L3oLAdAf2QlL2OjLlkatbaksj45PJfxxuni32n296s/7jPXdXyjnXqztxXjgi4MZP6Rcq7LMZMfH1pvNM3p/XQkrzOQ/qSKajDOZYSKhw5UmS/o6IANpQ23ps24N0PmSYV16RjSH2jQS0vX4cD5umPVebT1SWG8rnfDyi7GNnMpbYGUeTrrAVUXs7iTsuGTblXiWx8R1BgvMxoU=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="EI">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="DUB" DepartureDate="2019-10-28T11:40:00" ArrivalDate="2019-10-28T13:25:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="593" JourneyDuration="P0DT15H35M0S" Class="R" Cabin="Y" AirplaneType="320" FareBasis="REUOW17G" />
                                    <Segment DepartureAirport="DUB" ArrivalAirport="MCO" DepartureDate="2019-10-28T16:30:00" ArrivalDate="2019-10-28T22:15:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="121" JourneyDuration="P0DT15H35M0S" Class="M" Cabin="Y" AirplaneType="332" FareBasis="MJOWGD26" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="674.11" Nett="674.11">
                                    <Service Amount="566" />
                                    <ServiceTaxes Included="false" Amount="108.11" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-01</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="12" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhkeVQgCTimZz3FMF7EuhliZDI3GSRQ1QhvevnPKkhQGc3r0+1eN+L9p7K6c23lz2/BuDmUb0IcPQUXhjiadPr08/N9Ae3WtjNqkS44MS4/JVsYwXJqOgiJHzYjjucpEy2asWrjW06Zan8ZugaJs7vG7FUc7aS7Mqh51GRXLpQfFxK6cU+/2zXF2mW2QKFESZb5c7rvqD+pyvy8/QlvksiAZD/gfGir+11oaU5apku5o2fRLsQ4Q5Cp3RH2C4+F6GGoo5eFCnQDaZd6UHZKnp650Gp91M9gdpFmK7cVoNbqU3mZWD0AuViaygj4jmZbRVRkt9gfmbTKcyQWBKFjqfuYLKaQUyqnQZt1cDbaaGbi/hVQwjYgsXT0+1deTcfkkQxb7+8GQ45jqiV+Rca3J8yAN2lhsj1R8BqANU2ZFXHRSus9R3nxRw56xDOTmElNJJ/xZXwZvGECmEjSZl15fc+ZNSrYSlONUU5cltxo2S4Drp6hTUJTKXmVoXqg6zQ+4jag7pSvrIbSpfytTksJTimo5YXqX2H2qjXpVegQRqtM7AwYrAdsOvEfaUIKdaHzHB+leh5lXqOVw8W8RRN+lzZq4u3WutECdlY5BmWDlN+P/fSpGg3xQKl6lmSH5LhT1bEnbPl6q/cBerZVteuQCVnVZp0Jds5QNI2WFYEOe4lrPBBifRX9gcO2ydnEOU8MgFT8UefNamf2pBcR8ngc26yL8iOG8U717h3gTqgZhHLsZ8SADyOgYinW7lgKCp1xChROFq1DUcbdO51Ftkk+L6uIpqBwojYxWOzd6DswN+VxfmUejfQO/0RxZuPKATRF9iEYmck7pcF/KR2Sx1x5RAALjvZ87Unf8dpXgEZirN1LnE8/91u2AlHXSth/6uKLbWpyq9M0tyVyCOP8mx+z9PLqclUV3RDqBDkbjLHgQLEzd0THfzPYw/l1sc54m36nCeB9TjC+TgPEHjvJzhsyKlg8gU8LTpuafsoHpTSWlJy5fhneQtEAdPNKX6jVsk4M4DGO7NVPaEI8JtRlk4Z1804YQ5odR4gksMg+wzxxjqhGVayD4TiXx/PJmlOAETYv3hM4+e7HLmC3/F31vCmZ9oZcqdsnBqiVuseUNHFxTnxGlOEeEaoYzhXUQw6gntBSMGKIcXVoeJC0TEWLU8/R6dgB1SeZzhLLxeA0z1PAvatn5LkqImahEBFyg+1vPupx8GkC4FogzGM0Ep1nYp7kI58UzStD3W63BCI6RqquV1rPLBRM0PoninJCnQZjZJrfBbAB6q1haPpkXHMbu7HclepR/mHaOMSpBP7mPrqIdF56+mAky1rknfpSkPj1DLduLD5wuxRE5LKlpca1rS0VqJJdn4MkCb1ZBgZedDK8VA5UV1UXGJ0bwwpEZ6jaySvFuyf/hsF42d4WxSSWStEA/WQtlq63ozlKmB7PTvetuv6DOSSYd2fZTde9KG5yRFJMpqMbfsUhMmKaKA4T79tjSH2F4TOCe3SKhF124te8t34u0WgojLFieJj1RAtnlkk/RbrY84HMvuqfUbpvJgSS3ATax937eu0GTgYm+Q/DPDomHxIVaVdTnbvU4NnEtgWPHOeQ=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="TP">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="JFK" DepartureDate="2019-10-28T13:07:00" ArrivalDate="2019-10-28T15:44:00" OperatingAirline="B6" MarquetingAirline="TP" FlightNumber="4328" JourneyDuration="P0DT15H53M0S" Class="K" Cabin="Y" AirplaneType="321" FareBasis="KUSBSI0E" />
                                    <Segment DepartureAirport="EWR" ArrivalAirport="OPO" DepartureDate="2019-10-28T19:20:00" ArrivalDate="2019-10-29T05:50:00" OperatingAirline="TP" MarquetingAirline="TP" FlightNumber="214" JourneyDuration="P0DT15H53M0S" Class="K" Cabin="Y" AirplaneType="332" FareBasis="KUSBSI0E" />
                                    <Segment DepartureAirport="OPO" ArrivalAirport="MAD" DepartureDate="2019-10-29T07:50:00" ArrivalDate="2019-10-29T10:00:00" OperatingAirline="NI" MarquetingAirline="TP" FlightNumber="1008" JourneyDuration="P0DT15H53M0S" Class="K" Cabin="Y" AirplaneType="E90" FareBasis="KUSBSI0E" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="679.52" Nett="679.52">
                                    <Service Amount="475" />
                                    <ServiceTaxes Included="false" Amount="204.52" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-10-28</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="13" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhkeVQgCTimZz3FMF7EuhliZDI3GSRQ1QhvevnPKkhQGc3r0+1eN+L9p7K6c23lz2/BuDmUb0IcPQUXhjiadPr08+kphO6G/GYgehHmvla/WEpbKSq1YWLUR56U8x/Ki+Uj9I6bfHdF5D53GI+BS4ST/HH24EFkzLHiFe0IDYPIDVZxyv9kB/kBxYvP93fAR4SD4FhXYMW4Qk1zDkBULfv53yAlfJJMG13PSu9VUjRula5wZ0xjlWzpsY6SVryAYQWpEwWMn0Eagnysob9ppJguzAjgpvlIRQZUL93hDejKL2bn0Wvw9DEtAjsT68OqWrCA6awS9QvJ1yq4XyZMquX3dBOoxb05BGRpJYWQ+WcWax4VvHoCKrae/HOWzi5R81UZ6SNcCWWPTS05zWvkCfKkuhKSLX/QGx0LvyfB7ax0hJ/nupDOC+gt+DsrbAm7wNJ3ymIOHIO+8e/VnF3SLlpvcRFSUUQcjLJWIKTHQrOV+nvCLAELF6NOgH/4/Hd2v8uAoMwbjSkWHtYSrcwO88CGoOoA2pNs6CVLSEcfvbZF7G2QB//tKDDRjsyNewFe1wbwDUgEc8c8DDCEY6nRp3uxk/+ZMwaZ/UXfY4b7AQ/2Gig69IJAxgQznZY7x4UAYwfDNDqIHjbxZoO1q2xURKoieA1KoVsL5gDEUS2uVtwZ44bLf9CR5OFRSsxrroVh0pFP3ejmFwkk976IQCF5j1mm77p/JblC5rn3Vuu3mmPaFhnge0Iu8QekNYZdMnFohntc69TFOdS4S81g1Xc012FYZRuXyB8aZBsVF3NanoLtUzPHYVnCRDzQcSqO+Z/Qnx8QoXrCOAENu2APCaEFUdEUc8Vk2O9bBmNTQAaYVz8g1pL/6jTbV5k65QT3blvzK+TZG6EKNMDw5ujzchbWW6rfMXt6uOOGVdgCWoSy95E2n80fevQ1wc/uxD7RlLA8HEbzEolovlMPJCt6bNp8hrhAni53kwGhCutO2IO+pv2+MJEGpiGxH8tLbDePts9LnpfkfX+acAVkiHKQ2exKDdhzNCDXAzp9M8K2I1qXOsVfqJjJPaS5jUApi2iOIWniw4jG7vRPtZt1Vy53Qt4veqfDKDIutxtwVwPb74XZayd8JcbYOYHJOmPGNSvPx4vz0a3B1/vAMhXyFX74gRCau/WnTaR9yrud/2TK/vs0indJ/FUYLZOqog2Nj4ZkJReAR/FEoOzp8UHAl3mM6UlffFTA8vPkQPbZ72BK0IAg3PJW1FCY4I/xpgE+N5OF37G4PhmFHvN3Uo6Prj2TnCz+0tHCD+KkkoBgcpjZuonrYi+FcUh6D+hh+FZ/3RGiGzNL91iAQ5PXpQsIAACTcHb5Q0mpDFESMUgeNDXYHpjDARr/SlDrH2L6dZuZCMdwaGjDCEIFl2ocMfwjBWbiGkXWCZu64Cs0LEKKQjUYn7KjUb2MfCFsFnoV9S3fMMBFcHDBV1b1enMsRIc4XN/fG6aJgevOFT1+oCxDQVx5/NFc8VDPl0RczPfJD4hgq+qN8JqyIuZ9fFZltnhqhfAeoWoZmxy58goyqXKZOzboq2Y7hehVFCaNESujH6JKe6vSTM2hGVv4=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="TP">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="JFK" DepartureDate="2019-10-28T13:07:00" ArrivalDate="2019-10-28T15:44:00" OperatingAirline="B6" MarquetingAirline="TP" FlightNumber="4328" JourneyDuration="P1DT4H23M0S" Class="K" Cabin="Y" AirplaneType="321" FareBasis="KUSBSI0E" />
                                    <Segment DepartureAirport="EWR" ArrivalAirport="OPO" DepartureDate="2019-10-28T19:20:00" ArrivalDate="2019-10-29T05:50:00" OperatingAirline="TP" MarquetingAirline="TP" FlightNumber="214" JourneyDuration="P1DT4H23M0S" Class="K" Cabin="Y" AirplaneType="332" FareBasis="KUSBSI0E" />
                                    <Segment DepartureAirport="OPO" ArrivalAirport="MAD" DepartureDate="2019-10-29T20:20:00" ArrivalDate="2019-10-29T22:30:00" OperatingAirline="NI" MarquetingAirline="TP" FlightNumber="1006" JourneyDuration="P1DT4H23M0S" Class="K" Cabin="Y" AirplaneType="E90" FareBasis="KUSBSI0E" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="679.52" Nett="679.52">
                                    <Service Amount="475" />
                                    <ServiceTaxes Included="false" Amount="204.52" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-10-28</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="14" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhkeVQgCTimZz3FMF7EuhliZ9HtZsOE5yQu3Br50PVNZh6TmXHEMwkDS02AdJ3cWfxIdVNfxZGT839cFZhUVxQsBGh5ufO3camlUCfwLoSSFeFh45keoE6loQezBM82p2Y7iS9DTi86dpXiO7vrXzZBY443KXPCX58ew7XT4kK5LLC1MA/KraHl1lLtKoOXORZDaCcmzLsvbkj1Cbp+hRjyCcDWNXJXKB7CrH1C6lRRGSG49NHBL27yzSvp212V+phXc8nHztmlTjO7QrSb8Lmc3Wa4mlUYjuEzNYtevb8yrTl+y0gcjt9haENhF7n0WhfBE7qKFozYqLMIF37zbIk2btanGbQeGipB6iIajBRPSsbRMsimw+lU6BdCqKNdQ8fkOO8fU4CTuItva7q6+9+QnjJ5QVaGAkWfM9tSrIADnVP5nz52fsreSYzb0/sYuEZ95J5DxrPLhWJVTP6EzX+nSNzJMThxP6/hUbu0Bklczl7CwRaCYDQZUJJYrgNtMx6F4dPv9XpRt6zYLW96hPhdRjM2/dY1one40JAgFVXY71I0Q5WpthQp7fv4fYDWxp/Lqhe1zWUYpaG0JgQrQiqCTmhXRRC5NNq/ZdL/D6xTQFVlTUApMsRFi0YsHSjxoqkr+B6r1bXo9asilaTJKKPXubeJpE8vVzwZCrBMRtvfDF0TueQR6pdOIK6hKvQzvFIAhiiJ2JWiOktcEKx6ikfiDwtue8O/mYOyoLzjMkP7hvWKOetVirD6UCQImZpP7N7eFnpXPae1zX1Qqy0BqzKITQBzffwfyAfgQxVQxnpm72ish35r9PMKPHzNA+KYawS9ptFz/su4e+1Bc3wJ8XCyoZSUhuY1wJmpIaXYymnGX9E/1Dt7061Lc/JuyYFYHrbtaKwPXsfr4A/O80VHs/ty1HVvjXaRG3q8SmAktWBGqUwZt8fKH230t2kJ0tFnP/xz3l77Vp0l7Ez7AQUSdX/ZxLTTUJuWonAc4MsnPlsPUrT1hPKmNk/drgaBQ8UTULFPvh719l7ZDUdr0mvKpOpgjVEv1zegFXDVvUbYsOuBlCuCvtc+XXYjPH3/MF/Q7IDwV8Zvu1AycpM64UqLzrqLiHJoJoT28hRAjTzm/Ba3xxw4fA6m6VuKj08LohD+4KsXwO07y3QqE4wLOznqXEd2X5/O6iE6Bu/Kkf2pm24hXrb2jpMbRd0byvjO/b8kqeu1UGV0+2FJFGlfV/ZCyrSgyAjwueJdqkM9hbCR7GfCUf7Q6jQXIimNmr9zxM3WRRBDfDx981zrfoQmNVJOkBm7kjczoIGl90bF5/Na3n8cjubqB2ugcTt6YMTb5GGzXTY4KkkiFMGyO7OCSlN+QBhCNS+vr4EnXQPyHXx5TBREB2KI9TbN0TqbUHnlW/LiaypZq9qSFF1zcaHRnI8FB5oxu2k9rXtyFjSYbd6TK4o6/icA5GhzsifXhASLBU7rPXXV/yYr803me8/WdFUMptPJ+ZRonLZVNMP52Hbio3QEJ/3WBVcB8yTGHZx75aFr/AVvePySv5W7CmHYVyzK0HvL4H071Th7RyLRWB5gRASTbt/hW1MSWP2DFK5j8a7xoEt5hCxAezl+uKZL1/U/Q5swu" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="TP">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="BOS" DepartureDate="2019-10-28T10:14:00" ArrivalDate="2019-10-28T13:04:00" OperatingAirline="B6" MarquetingAirline="TP" FlightNumber="4330" JourneyDuration="P0DT18H6M0S" Class="K" Cabin="Y" AirplaneType="321" FareBasis="KUSBSI0E" />
                                    <Segment DepartureAirport="BOS" ArrivalAirport="LIS" DepartureDate="2019-10-28T19:40:00" ArrivalDate="2019-10-29T06:00:00" OperatingAirline="TP" MarquetingAirline="TP" FlightNumber="218" JourneyDuration="P0DT18H6M0S" Class="K" Cabin="Y" AirplaneType="332" FareBasis="KUSBSI0E" />
                                    <Segment DepartureAirport="LIS" ArrivalAirport="MAD" DepartureDate="2019-10-29T07:05:00" ArrivalDate="2019-10-29T09:20:00" OperatingAirline="TP" MarquetingAirline="TP" FlightNumber="1024" JourneyDuration="P0DT18H6M0S" Class="K" Cabin="Y" AirplaneType="319" FareBasis="KUSBSI0E" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="680.54" Nett="680.54">
                                    <Service Amount="475" />
                                    <ServiceTaxes Included="false" Amount="205.54" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-10-28</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="15" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhkFVz+ovaZye4ZbMn+UpGPbQ9PSj+wXf89fVKxXShICdvkXnHJVq1Wh5bbIRao/zYzvrsSMZ2dtUMfarCKOwGTeaJPBlbFUtSxiIsGIfGmByNVTN5UIiUXtOhc+Bn4k4WfiwUUNPsZ1aZEgHIlLgkbavq3RjFuBkk/EFpyP2037GNE1Q6jZ62qR13BsHwpPcTupD98uQlL3BZg1xevKjsk6SUc7qz/4BvRnEaT4zCqZFeGIO741OqL1J8JO7b6Cja5v3Uek8PM69ymO0LxdDJOBMbnrbPEmbO9gmlXlXzJhF4EL4mehhZGtiPeDOzIK9J3xQjsAA8p/YlAuI4fbk522rP0Fz8GQnLVoWTOuWk2RPHUh3Hsz3cwynQapDqKlTQfZhsYJF8V/llkIYyZXS9cPR+jYxqxPyyQlfi2GZwske8GNlt7xrOKU82KunKvsBzrDtMGVAO7v+d4TW8htgt0IKW0xcVhw/6YRgmThAQcRrhTOVLv3PZHGtZzyS0PYUIDMl2in/pKqg/oAwUF9UdAKYlaLgL0NE4tsiWUMD+Wi/1uhCRUK9G/XEdq9iPasHJ+0vCs7KB+tc7UKmJD6Iv5w1xi2LxDnSz24sEw2JzSkZY96XqyQ0LV51IOFUBPBpGk9i0Fjd9+kSUS25c5tTczAGc9E5SLNxjhVTPx0jhKEaokfj6Z5ljSXgDclhW+9fpRHvS4N8kfC+28ZJHYviXTdVjQcY+BluThn+bng01uPUhhsD0Rjo9rl703SQDn/GCQoCSbAGRMhgWSQJo7UMC8KVye9JGQSdddHIGRkdktOTB0StIHqdaWumKmsr9MvXJaW1LJRIRI04fTU7jp/1i10BEQm6e51PIji92TzsDRG4md1zSggB3mILVZyvE8tPFrd71YRQ2tNrjwgyFj4gzC2CFU+jfFocQc8pSRJXrl7rQg1GZdgC1HHS1462vvNkIXOruzsc80yh+yf+u0np0h604H2lT24UI7l+/MzVRX4cArS9yLAFzOPs9RAjp95VitoCUkob/tafnmozHH1IQh3zj8u/iKacYG7NmKZXMvn+4ytLlgng3Fu+7y/O5/owIkaHYA5GgRRKZE5/HnkzVgleMJ0efMVrJFOAq6hM17aLX6cpRNZGr2GJJPcmub/vOpsTHTDh0Vmd2oZtk8o6PWXOQd87FHLBixaER47xip8Cngo9Q2+/OoyfcSwMNzz+pg1lBNS+MLLGUG9HC+AKfpwdlW+Sz3DHQiFU4tXnUpkdjwSL9EA9KjMy+/wjQRNdrE=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="EI">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="DUB" DepartureDate="2019-10-28T23:59:00" ArrivalDate="2019-10-29T12:05:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="120" JourneyDuration="P1DT6H1M0S" Class="M" Cabin="Y" AirplaneType="332" FareBasis="MT1NS" />
                                    <Segment DepartureAirport="DUB" ArrivalAirport="MAD" DepartureDate="2019-10-30T07:20:00" ArrivalDate="2019-10-30T11:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="592" JourneyDuration="P1DT6H1M0S" Class="A" Cabin="Y" AirplaneType="320" FareBasis="AOW17GDS" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="734.54" Nett="734.54">
                                    <Service Amount="667" />
                                    <ServiceTaxes Included="false" Amount="67.54" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-01</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="16" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG7oYmiMhuDoqtPZavvCJDz7GCcSu2EOT2/AZ/Q3+ctU8b8k8G8IXvp2ySSoMormvjBCgKYczRc9EMoK1lpwPW0s5hoXPQShyHx9ciS0fEhalvod+s4hO4ksu+6a69sPcaD7NVbaRYaeXt6VfOuFHb2CaZQvKbCmyXIelzBgLxG+OSCvQighxPIwKkH0J2PCMl8FeOJ9aqbhL3ZD+M+Wj/Pk4upSOszC1xzUBMTTPdoOXdfG+Xmb+Wt4a0EQk9eGaP2et/jVFeUY6IKNpwh7gcHerNjvMYMA58vhgY0w4gxoP7jvYV9WPt6AFS/odum33+VoZ/ERskBFU2hqRktPnEbBquZqQvYeymuLvCfPfpVpu9uPVKxjcHFa5JXxj8+ydfUOvntCerF25//JaPFk2+x9+iadR8OCjtCO4hKLW1jkRhsLv1cbid5bNq/056juhuBmRkQNXG+Wkk5p2hwyYpgOaG7xu17ZKpZTp2HDdGldk0yzqwgca0Jv5JJDF5EJXwpl5nidjTrpcBUagfiGTmZlrTrd4MOgMGth95TKp7RAE/0Wp7V1j1vmecTPfsWkrrSQ+BPSHuo6FcZ/6asvlX7zc1HNVpLzJkQsC9FZq0qO5HMXrTLSqYfWHO7cAGVwBkqjTALr1BSbeS0XJ6Oj/gio38xQMjGr84oRiZSL9mjpAvqwNtwxVeQVGw6PQ+rUFl1lJprlWKHvApbUnj5iAvsiGYqfAnKBTIWcuyWoJsEL5t92wQYjuQjvlT+GwwvTwgDbZudhefkidiPxkO8WR268Ryzyh4J2XAE+6Al6KcA+bu7OKTgDR7IieU78UCnMZwlWws0dw6PS51aa6Ek4l4zfQ5Y0YTo1vji9b4Y1xa2lKq64FHdfJXG5Y57beqlYlLeCwsdx+YOOp2iP5ovblv9U0tgtfwU09DVW0hywXl9QVc1WkbTbtC2TvkDGwH/eiPULGCuN4vGUqvhVokQ4BUfXYNR/DG+z+erjEyw3BKgl3MBhBDcU6dm2ftcY0WjIK7daLdJoMKlfax5boZTnVvMAsbfzfxd6Xp8bLD/fBhaEE3WTUztTs2TN9pU6P2fvillpyv9yc9gTbRpGYIL4cx2PssarT5wVKADy6S3NbC1A+BCLUAF+wdu1/cofW02Mm/HYJ0/Zpksm71Dd8FOFpjA7qaMc1DEkGX6NFrZfC7vW58vkpnctC7Vhcd9gj0G7S2lQKqnT0Q8N/cEI+qLWYhwJc+apmRZczLKMp3/qPVGKr7HLSf0/ooLeRdhlUOX+An3YlMd9JqdsSIGO5UBjHZTO2rHYViQmNZdFAez3/rnpoXAeZvyDbIsqGdEkJbN3wXnqJKwndiM7WfWaqJ6iQsrvC2R8fp4iygtLAy+8nKP30ekIUNQfXMRY96j0FVo1YG50aEsHKuyHg3IduvN8aLV/Z0Bj3zAhbJqWZxotPsy0fg1gSee7ejvRcfWr9qv/Dk6JrI5GSIiTLF5yBW4NbeHctfT9MW5d/VXHr3KLItxqePYvbRpQm73QXC5dZzontsFQfoh2UuUfRTW3a2rZxFuubdTNxilv+fz9q7bM6L1JWo=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="TK">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="IAD" DepartureDate="2019-10-28T19:08:00" ArrivalDate="2019-10-28T21:17:00" OperatingAirline="UA" MarquetingAirline="TK" FlightNumber="8613" JourneyDuration="P1DT10H37M0S" Class="O" Cabin="Y" AirplaneType="739" FareBasis="OL3XOYY1" />
                                    <Segment DepartureAirport="IAD" ArrivalAirport="IST" DepartureDate="2019-10-28T23:55:00" ArrivalDate="2019-10-29T17:00:00" OperatingAirline="TK" MarquetingAirline="TK" FlightNumber="8" JourneyDuration="P1DT10H37M0S" Class="O" Cabin="Y" AirplaneType="789" FareBasis="OL3XOYY1" />
                                    <Segment DepartureAirport="IST" ArrivalAirport="MAD" DepartureDate="2019-10-30T08:10:00" ArrivalDate="2019-10-30T10:45:00" OperatingAirline="TK" MarquetingAirline="TK" FlightNumber="1857" JourneyDuration="P1DT10H37M0S" Class="O" Cabin="Y" AirplaneType="333" FareBasis="OL3XOYY1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="816.27" Nett="816.27">
                                    <Service Amount="597" />
                                    <ServiceTaxes Included="false" Amount="219.27" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-03</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="17" Direction="Inbound" LowCost="false" RatePlanCode="Ffa1q3POCcyi2Rus2m2aUvvI4k+C7do73FaJXFWc2Tn+QvDhv+mN5m0dR9RZVrSWq644zHWZMc9GOPDVHCa5A6DB1PfJeDN14vTSa1DP3zMe6Pqbpgmm1BmQ5+/egIG3biQ0NVSglWWJK3GbMU7sJWJNBZd9F/QYoAsLtIjL2wIzpOWKMz7cx2sbfp/tjH/4Ck1JhZVyR2L8MgCMX1dhYCR6m0DVYuV8y0PhDjDkg5AhnOVgnvHHZUKAKqnIKgovIwu6ZG63+xICiR9hlPGAxpiaH0EqFbQP8Hr2fY9j+ZvXOfW2VSJbNTG7+mjZx/RcAiOuAa3VJ5Vf6qHpta7iIP2uuNBbz6+Ys5UlowJp4d57X+zomAfk9hOV0tZ75oIaI9I+xeFeN2KHSB6ZrK+tcLh7wv+xTuCcJPUVEwkfMbwmZopvyG/EZ2v2l4s+xG6/KCIwcMvTyPCzTKslYq0LU2IIssqiLSKhoC/RhzwizDoPblVciIDj7Wa0xSKZLyI45MVrNmWExFyTo6x7R6qS4io1J59/2IYDSR5bh2i6p9dzYByoVsSmygx9v1lakLUvaxKudTqJnU7ye36rLzgbNO+c7nchVC4VJ1LqupqkHtI4lM9y5r9FseNw2AnfRPAr3mf716NMiJAzKLw262P/KvY0yAyufhDkdfdldonSkRAtNW6ybzeLNGapY3hOj+QLG9nd5torUUkY6hWqiYd9D4t86y7oDZ8akiv1VMXAcUMuddFQQAy8hHrT0hlltgnFqLxPjVAlWbSVN1qD3G5FME6Dv+jEPFnoJQF4+9f5XasNnAJYUiygqPOZnteI8vW+W5ptNvcpORRhJb+IXj+yY9V0PVtJqA606E/jjynW5xfZlLjtNoTyg8ypHL3U0dbXY1JjLsqrhe/ZIzrCdwFgJ318KKIz5Iy8tWqGYs40pii7S8QK51cBRoicNiJalSTKQyhv0ziHy2pThX1efYCnQvCOJtQAff5IKIABXtSEp28MhxJS0664t+ebxUaQ4ZtOp37dz3IUPJAV/PLcvcn1OCHeiANcAc7KPlV/ZRWZX7X9Rt32fA6Zl7w0+zMUHLX32On4XbdI6MUATqWodADNrYwjems9xL06A8SYz1MLR7nnxBVLckuXdidt50W25SntQvUcEffxOG/0FB+DDyTX6CX0YAYvJRdRIkEFCV0krDzmhd6wE68v4AWqj6W2vM4gasFXGP69q8PRikHCtjjXHCx7XKRKDxDeYlFGnU/uvzM+52e6FjYmIx4rXbzv1taGvXnEK7sQnI+zUh5y8jgJemNj3lJET33lB8Gl7rRSpq2ton6Z/g1VLTSKjv0ysc72GSaDm9OK9yfQw1JjgpzmG4NMn65/T4T0mn1Ueus1+pQJu+5NmJiEhwX6AN+Isdxcjw0AzvUD5Yw5hnHLidN4YToL1rMB+pYMIsSFdJHoJOMhiCjs/j1AywHh9tmPc8wYApes3mcIDt6S64Ua8aorjEBF8aaMER54yGkEft4lYRbPRlCL6WZfMOmgo5SAN0G9ql+F9eBVp0abOR/+zJYbXG8vMIAmIpzABlnF26qpcSqYNZW5tdxOCQN858hPk7MiKz9mbSUEdQSwcXcmVgwv4JwOdNu5Lp/tI1Bs0pP4r3oZSSb+yJ0fbQDZawAH73md" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="TP">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="LIS" DepartureDate="2019-10-28T10:05:00" ArrivalDate="2019-10-28T10:20:00" OperatingAirline="TP" MarquetingAirline="TP" FlightNumber="1011" JourneyDuration="P0DT17H28M0S" Class="W" Cabin="Y" AirplaneType="319" FareBasis="WESBSI0D" />
                                    <Segment DepartureAirport="LIS" ArrivalAirport="EWR" DepartureDate="2019-10-28T12:50:00" ArrivalDate="2019-10-28T17:05:00" OperatingAirline="TP" MarquetingAirline="TP" FlightNumber="201" JourneyDuration="P0DT17H28M0S" Class="W" Cabin="Y" AirplaneType="332" FareBasis="WESBSI0D" />
                                    <Segment DepartureAirport="EWR" ArrivalAirport="MCO" DepartureDate="2019-10-28T19:45:00" ArrivalDate="2019-10-28T22:33:00" OperatingAirline="UA" MarquetingAirline="TP" FlightNumber="8574" JourneyDuration="P0DT17H28M0S" Class="W" Cabin="Y" AirplaneType="738" FareBasis="WESBSI0D" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="856.49" Nett="856.49">
                                    <Service Amount="676" />
                                    <ServiceTaxes Included="false" Amount="180.49" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-10-28</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="18" Direction="Inbound" LowCost="false" RatePlanCode="Ffa1q3POCcyi2Rus2m2aUvvI4k+C7do73FaJXFWc2Tn+QvDhv+mN5m0dR9RZVrSWq644zHWZMc9GOPDVHCa5A6DB1PfJeDN14vTSa1DP3zMe6Pqbpgmm1BmQ5+/egIG3IMf1JbTCgeOhOolyZpIW5U0qnYWkc3Lsrqu7N4ZWMGeTwbRzHUyrSSByy9EM1D8UvmAKao+OtzUjVejZ/6YiONqM7Gob396rWwwBw/u1NRUL2DWpghCh7S5MKJeVWn6ce4vxptXXPSvGR5D1m+hSVfjAgwJZtQqMQGlKfRzgUJSanKLQb6Akv/iyFPQkiABqkTnKv5erKoPScJhmw2ml0TYrfRWaIUC2x2+hHW6Nx2stdnOwDLpkZzq7/zVLOXUoDNXJlr3vJPT3NrHbGDtzVa43lU5Egr+r2R8N5Wihl9jwiddJWY7YjJWBGLRgbdI+RtYpvrKR8GnocsnCdpDBk3C7jKeoYDNM+D7w5vH68guEH8Y5vedWiQvMIs7DyAfGN69s/vzEwc6nrfP+vmRZXPkugMkxHXp0Dty2p8HGDKRad9+bk4Te4TmLveA9o/3RYEq0VA3+A/nD8i1/sdMdT8xO02B6VP1xUKesfLzGhXVuPUu7fYzCa6sXQ7Hl+efHwSduy8AHNGiQawx0fFn/pmNQHtFlyWpSI0pgWSUXY/UCJWWWZN2W4YNddSaCCQKHkAc9pYQ0TFlaYRByFzJH44U2zSCcHaDrK7iRdFSXUM2XhA+iG3gGmd/0UGGyyS2DH1m8+zzphJA0/hBhEuHSY7AHZl8lqgJLVDsJvZwXVhPRd4Ktf9aedwxXRsa7rzEoNKETsjupT4ueD88gOJraOPLt2+UO+y7/sGCDEY3RT9l6P8dVo2KpdAz4Q5rYsCbdIO/r3OZkmM/K7Pdo3v+6sJLHuO2kHaWtUL5orG6YQOzu24hemULURczjNOq396AoSFDV0lUuXpyX+i8MgMhYho2s4TsyEPN/Qu+QTPQQBb68GArMgXC3knv+V9Wd107wLJ6HVJA8NRD6ygYJaExTrOV1hcsvwaAld/7+W8hmZrXsPMH7MrTLK2D95N0i8fFJzNnmCH6+ouyotXSI7uwnOAHMinYq66A8Tg/FwAh/c1g8YGnWPZOK7pcrlddjDF7zARnBX5jFVuAEfrkZrTq8Sb2PjmVfceWKAiQfhHZ0janOY4Z7q7UGnHGt9yG2dD8zw37p7pixXS657M6Sy38k8seYRBMbDANE/vCOn5+fOe1q69vBLEc5ruoO475IGabcJ1xP8a51CIF6873Ak5WNSgAoUslGJK4lDEMOJsUO9hyq5aASx8iOjCPSFIPofQYX06uI/2C0vcQkN4zBKFylJc5raBaWdLy4csTha1eRhZgQPRNef5uJ/cdUVRGGwpjFYmM/by6It7HlSmqQj7nCStyj0qCSJMja3kYDby6iWtHk53C/DmbTowdJRimiEYMEdUasKopOH8VvejkK25/z4ausdsnV4Q9FS9ztzTkN9jwSAO4s/Ld7aSATKVM6CHLwGlWvWmEKU/rPgUUNvO/pC/w8nrAcm2IPsFjBodrS3rLoqF2LF7kRDMay/q0elyDRAwOGLbun/8VZdtwYxXZ9rLqLvD/d+mWK2MORNyHsVYsKFo0X0+scTP4etGGyJgda" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="TP">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="LIS" DepartureDate="2019-10-28T10:05:00" ArrivalDate="2019-10-28T10:20:00" OperatingAirline="TP" MarquetingAirline="TP" FlightNumber="1011" JourneyDuration="P0DT19H18M0S" Class="W" Cabin="Y" AirplaneType="319" FareBasis="WESBSI0D" />
                                    <Segment DepartureAirport="LIS" ArrivalAirport="EWR" DepartureDate="2019-10-28T12:50:00" ArrivalDate="2019-10-28T17:05:00" OperatingAirline="TP" MarquetingAirline="TP" FlightNumber="201" JourneyDuration="P0DT19H18M0S" Class="W" Cabin="Y" AirplaneType="332" FareBasis="WESBSI0D" />
                                    <Segment DepartureAirport="EWR" ArrivalAirport="MCO" DepartureDate="2019-10-28T21:35:00" ArrivalDate="2019-10-29T00:23:00" OperatingAirline="UA" MarquetingAirline="TP" FlightNumber="8596" JourneyDuration="P0DT19H18M0S" Class="W" Cabin="Y" AirplaneType="752" FareBasis="WESBSI0D" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="856.49" Nett="856.49">
                                    <Service Amount="676" />
                                    <ServiceTaxes Included="false" Amount="180.49" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-10-28</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="19" Direction="Inbound" LowCost="false" RatePlanCode="Ffa1q3POCcyi2Rus2m2aUvvI4k+C7do73FaJXFWc2Tn+QvDhv+mN5m0dR9RZVrSWwkQTVX5rEUe+BBsKQucfOU4FnAHD5QpjahM/khQXm5sEuCSvmzrOCI3CA52Lvva2y2FU1TAPwj3kzlGSWZOH/+AmzG75siWkMhV8SWrh5FTtVh94vS5rPYRyY2xN6rEnKOoINB4S3v3AWxTfNQbIO6PwPa8iyWwzchOex3H+VjWsoqba19SDs8JmSCJa/etlSnWhMvSASqzqaehi6JxM3NEgYxyBkgflzgedNpmswO8AULXjzpeGOzjhRQCq7zDmy0mIl/Ao/x8faHFHlW14obiLg8oUUVBuCViNbJBr9t6IlxIT0pSXZym9t1hL31uNLjFSmgg4bPlMDNBHSOf1GDxFuTnuVodnarfemNoztjhAJ7TxRtSBq4M5vcpXcNNPn0eaymKiVU+MayikV5v8Rx3ZWdjLk+h/1LbUqBKUHGWH0ZBFK0AElM3LXkhoZaVSewSR9o7tzN5eAGdjRn51ZdxvoH64Q8L9rPkzfHBuIJ77IzawEkgIIQmZdaHjCMEBLf3P7M3vm5WyEUJWA2Wc0b1U+z3LbA1A9Syv7pmgQVq9TLRjukIK1J2DfOh1v+CyWgKIm09Mf/MJRopoq/4OH6UUPB+rwe6CnK5gtyTA9K6VSlCiPyLKfRKaH6ciwIlDkPVWIyCc1JvOwtn+23Y9mn+Pa2sQdlOS8a0N/hX1U4IvYLHz2JlYF2vsgEHUMpAsGFP+UzgvfU3hgTwdZqxcFdDhxTBlEozfbFQS+asqI2ctsRxGY4qrDoLRsTZ+JP+hah4Yl6Ks7HEKsiqun7wUvFu4fD7oiSnNEmeMIueno4jKfsXRVr55QcYcgnKrud0cgSkuICP/7sX/sqNicVUrXy6+JnYli/MUeliupwvDzgzwBJJEdZstyGKqGUaI4Qho8Elv7lae60jV6/1GtFs19aJ0pAfOdZpMehQKy9GPTbFVBv4InOKAnzLTHqjpgsjEkEfAWGsMqJPJbcggbCSqMdlczU7Sp9U+12kETo8HHoV1w6mcA44AK4vE/tdDvc+0XhWWD0VkK99ldOSEraK8+k3UqWMvHGw038LYE+5mEnVJ1zlPUJl5y2tFsXu6O2kN+32aUYKU1zYQckdbqa1XkAPgtwEG0hKARJygvl0iql0R3w2PYxICWfmDlM3WSfFdBMwB+/k2tfmPPClSol1Quic4356TCFfOWe+juTfOR84xw2y+FIP41BiuIT4akUvIMd+dkjTn6g9tAGYsoWvtU3BgWpBxKKvpVQg7KO8BhfoWG1Zruub9oyjJ40oxwDhLvZqIxZ2HiPe4nHKxtPX23PvRjCS+es+Cmfpw4itqzy9P+KCklRJc3i8grtQX+b4FMhgYnUM70UvWtjte0mNcGNhf/LqqxWuVQLH2GJJs2Kgfa9jEtOe69D1JDngH3k83UAo2z4g8D9aub/4py3OENu656Mt+7w/nhWXeIkgg/qS+fTwStx2gow2emfvZk74W3Y2c0h0Wg5kNn11yfo1rySuIymNjRjnLNhKVd98ePpNjcBOJYOTxF0h9mIEWlNs5OSh75DGSLwFNIovLg/it0ed2C+94DptwEebvyL2JRm0=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="SQ">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="FRA" DepartureDate="2019-10-28T16:50:00" ArrivalDate="2019-10-28T19:25:00" OperatingAirline="LH" MarquetingAirline="SQ" FlightNumber="2095" JourneyDuration="P1DT7H48M0S" Class="E" Cabin="Y" AirplaneType="321" FareBasis="E11DEO" />
                                    <Segment DepartureAirport="FRA" ArrivalAirport="JFK" DepartureDate="2019-10-29T08:20:00" ArrivalDate="2019-10-29T12:15:00" OperatingAirline="SQ" MarquetingAirline="SQ" FlightNumber="26" JourneyDuration="P1DT7H48M0S" Class="E" Cabin="Y" AirplaneType="388" FareBasis="E11DEO" />
                                    <Segment DepartureAirport="JFK" ArrivalAirport="MCO" DepartureDate="2019-10-29T16:36:00" ArrivalDate="2019-10-29T19:38:00" OperatingAirline="B6" MarquetingAirline="SQ" FlightNumber="1479" JourneyDuration="P1DT7H48M0S" Class="E" Cabin="Y" AirplaneType="321" FareBasis="E11DEO" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="994.37" Nett="994.37">
                                    <Service Amount="891" />
                                    <ServiceTaxes Included="false" Amount="103.37" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-10-28</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="20" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG7wQDeW5NL307KwCeBxSqVEftXUBANSMq9cRmP1uW5j/hn4NcqdYJeBieeo/5zmnBVtEmu9G7+uUR5j8tAcPsKMqXdwTLc2B/ioRg0XYvyTRXnckCZGD6Y4ZR09dczBNXERlMSAFc4hJBs2metXO/4EIPsEdF3jlmJseKuwp+UtV6sYm7RaAgQn7lV0qK/jcfBHnYvyaQ5sXYWDi3uenQ+FIN6Gy6H57sT03ph5SBXEqgGRCDuqU55YtMinHDM4TXChDi6Ad9lk5mxS+AbJINUgToW2o/KsayGM5uGpeZCFppX6Tr2tR7q+aQheX22n5sY+Qoqhf3WZRi3dOaWxIG5884WEOxmzMaADhoFAp1HvLHKjLIE+H8s+AqVWAMGyI7yxDp2z/BhAQF5Pdc9usiWLJ75JRgpOBFDe8qhOy6MpfN0DbtqVYgsYEltwI92XPG1LPa9ues/RZKiUgRRjJcHR3FXI8tzv5pY2N7afrK2Em+x8pCaOctTpyJv54m8ROtEdQjAGZD3gXiRrQnyBqJlXyDT6fctm33OGBNn0CGFl5Hyxp/e6KTNUAc79oJR9JdUn6V6xRP8pBfEfe2GKjsdtzLNdpywZzxlwW5wXGXvZhmd+m1KScVpYOJ25V/ohEWayePCSib98lQcOOlRd8F2oh63spSFwmq23BqyXPSmwtsh2nJ/+L/1lDIToMzyUgsDCMTIMMzrttJDMPq1v1wACaYddeUewAVwdF/PWWyorcaxNTYzf1UnM0ta1SF9O+igutzjjPHjQpHVHQiuKJXA//uQ8Zy/EmKyoVCWxYMElYbZTPGP/XbBgeZuDEJ1bf5EcLOAesXM1WBA5VZYh8vTnnVcgeiIkh24ZZvFRp9frmHBibLUW1KzcMgYln0b/JNsGaPsRjlk+rrXYYqoAbOiS9o/8HiCg9nWU8P2hebuaeABUZG5BNfWPr/wqMilTmP8BboyuaEDYd9YEL2QMykPWSeuJcq/HIrA1wtSBFuQZnIWzX759fpF9N46hdE3gHamoizx2yj291WokWuAXC5ldCW8CGvtLci6YjSImHRN9XvVRwi8WiGh4bmLRQPNbiEdq45SlJPsrAUuV5bZPm3rAz+1SQT3N1rjCQX8xUrcNqFn1wE+yt3APsl8vpZh9U/Qog1E4eLbao3kJCHn8GvZ9apkj7nceuC8E94FtCV1IMCfTmky98Iq2ZLkGnNPh/+dkaWPkFCXbWyR+hA5OzLsP6H0VKcxybd4X7KZSe/hx3A=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="EK">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="DXB" DepartureDate="2019-10-28T14:10:00" ArrivalDate="2019-10-29T12:20:00" OperatingAirline="EK" MarquetingAirline="EK" FlightNumber="220" JourneyDuration="P1DT0H40M0S" Class="Q" Cabin="Y" AirplaneType="77W" FareBasis="QLSOPUS1" />
                                    <Segment DepartureAirport="DXB" ArrivalAirport="MAD" DepartureDate="2019-10-29T14:40:00" ArrivalDate="2019-10-29T19:50:00" OperatingAirline="EK" MarquetingAirline="EK" FlightNumber="143" JourneyDuration="P1DT0H40M0S" Class="Q" Cabin="Y" AirplaneType="388" FareBasis="QLSOPUS1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="1065.1" Nett="1065.1">
                                    <Service Amount="745" />
                                    <ServiceTaxes Included="false" Amount="320.1" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-03</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="21" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG7jFgbVG+a5ViIIhNWVpVIWgi8+xdo/5e19tE/BYytDx0OQpB4DHmOVR46xf1WkRXL9S/2vNHPBEqS9U/PQmGHj+bzH+BoCSQHhQoORuIcfk7snvvNJLEEfWFzAOp1EJs1ILcpt6PH3yXxIsHa4gSOn2IecnwYQrnSg26WLC33pp+axiw7Pt26zIOgrOClpGlQetd0IUCR8+dSDNop3ohgB5A5uqJI4wjzZhcN+Gs1Uc2MnSAqk02ccQqIBEs2SENgt3Ct3XxKWpS0kFbVOqcOd15lA+Iip84TxF375nhorH3UJG+yAgzUJ+B2fEOB6cYNFnKsq2YRZ5FMHPSbgD4U+YeCVDFpUStIiackDCzmRULFNtI34aFqyzPByKiBt6G1d+FVmWVGd0C1ZF2teI3/A7IjmLzDXj/nMG7+kREEqc2QSe7Eqhf21Ol8NA4zcvQW1scN9AhhUPgRiYmYsEyu2Pv/mISoTtWOnrIAkMYJViVo9G47dL5vTHsKCrQOlEgqWxKmu37Hpr/puQVmnWorrhnrmLyu0YVpt5Jbh+td74AT47RCevHiYDslzEOtOr2rAX4fmbNhwr4ZS5ka9/8rLm43kO+J9HRV7nhrbjWsjTXC1QnVZ6ZFttc0IOQrz5wyLNmwaAVap0zLVHFKQ4+2trk+v24sp56VYtMmV+UDUFuH4jPV9H3E0ABrvubC7sdb4Ow8z/YYZbuaTrQSRlMlD1B32ljuTRxcBEfgAmau2Q5w1KRPNSDvSW8gAcyBGUIeVYX/r5hdZgt1JBCIBpRSnvotwQkQ8vWTW30GI4//wXfcHZgtXTiH1vJo3Ywo7f8MZg/4kSB35Y+NDBFQNEj4WgO41cCQeaVTm7UzdnIe21Bsixqrgtq+hWAa/IYZj0b4dMTuB3VwqIk6Nngv9Jy8gFHrdpP2C0Gdonph0U4hLCCgYDQ4Ymf1qAL84OCL7f7zJlOx5b0PpM0hh2pmBTQhMSV4QdlO2gUJo26VkTBZ9Py/wkCr/8Lpnx459Jx8ynWvRoQBfloopxLRSd1piI8gWiKRmEZLRfM93q6lLqiS2rPu1cxsU9v82AWuF83iEGMO+cYGJwJo4w7O/RUxxVC3T6hCSCv5hDkTQYTDJuzLyvJewi03prfuMdFhRO7FrOpmQadO3H8F2Lh80tT2TGWqJ2ivJBJgICq7EpLow+sVAvgWbg/AuNgOgshw/nCDkBhwRhiyPUJcjyyHrOODhlRMkCeeZXgtsjbPYk4UhQAgRXmBQ3jzi2hVW6Jz6VJjV0QeHaN4pFVGZ/Nj1luxPBqE0MmKYphFS+RT8xczvEJG0TNJ4q1OUkYumtRqTurfwD75rc7XeM13rzFrdVjpOjY6MozuT6+SF9zWRAU8op5gHPPKY4do5loxyd+N5EuS726te1BnbhEy5NNqdSpZT/3MHSQ8MU0blUGzh9n+hK0nE/tHwq0PY4Zy0yY90JFrqDvs7+mN0IbF6Y+mgsalF8AetYWlOM9u2wf8ZppGJF9c1ui6DgFSIKIynvHgT++AOnc3LXL94BL6QXj+ruRcjd4aiA==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="LO">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="ORD" DepartureDate="2019-10-28T16:29:00" ArrivalDate="2019-10-28T18:30:00" OperatingAirline="UA" MarquetingAirline="LO" FlightNumber="4378" JourneyDuration="P1DT17H16M0S" Class="M" Cabin="Y" AirplaneType="739" FareBasis="M1RED" />
                                    <Segment DepartureAirport="ORD" ArrivalAirport="WAW" DepartureDate="2019-10-28T22:45:00" ArrivalDate="2019-10-29T13:40:00" OperatingAirline="LO" MarquetingAirline="LO" FlightNumber="4" JourneyDuration="P1DT17H16M0S" Class="M" Cabin="Y" AirplaneType="788" FareBasis="M1RED" />
                                    <Segment DepartureAirport="WAW" ArrivalAirport="MAD" DepartureDate="2019-10-30T10:50:00" ArrivalDate="2019-10-30T14:45:00" OperatingAirline="LO" MarquetingAirline="LO" FlightNumber="433" JourneyDuration="P1DT17H16M0S" Class="M" Cabin="Y" AirplaneType="7M8" FareBasis="M1RED" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="1324.54" Nett="1324.54">
                                    <Service Amount="1131" />
                                    <ServiceTaxes Included="false" Amount="193.54" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-03</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="22" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhkff7CWp6dtKhK6lyCdupZyjfKElJTyHV/Xu8fcY3wsfQBF77qrhsVE0AvVX79Pj5Sb4RczUmdMZjv2wpMAqNNjsff7wDVfkpeeNJBDQu6Dyxc30wPDYjxFh1WboIpzbBHO0XEeIfjX1JCGuTClUXlo+mqzAOd0MFFlE5awo5IC/15L+TRD5ohs7XfL6Vmi/RD64tjP+jw6nzXxeClwNirj37Gls2B5Qm25D6HYGDs3LGTobP/zfcvYEiYhPxmkEFwSmHvwGq9QSO/bzZS4T+/x03TLxK21WohyXWckDupxht0eKEpK27SjsTVHp0L1JahRLhZW6Sm7pQee6LBUFQfB4ofp0NxiDsf2zFVIwst69iQytlvrttKGSuAbEaJQep22gC0ca9Wrxdmyrt9tICJINwoRsSDuHRkXUCUmRFzcvISr4Rwb4T2YspYgJxnV3GMTqRXXvwMyXhsrfyFQh0IYfsiz8Tfw60isqrctbO31XjhNC+WR1Wz0FFh6hcD/1Vam3+V7+X7VXEepu0OWgWSQ5Tkvv7/wgJXiJDiuGm+r3EH4LpM3xB8An8bpjCSXsZDOFSVfhuLBG95FzDDbaua39IAGexqyeUAxVOC7/Z7BQSAULYrDpOxRWyIBA40QIeT0Vb4qbc++2w6F2T5CjQGZ83FkcTvyLoEQXhu17iWrQQyIPQPdawayTwAdJqYNDuMjVxuZk9UBEpsfSN+Epj10Q/Q7+4ubOr4bdGl7UK3c2ysbTgbGO1dKs8jNF0QHzi1WixEDuiBzHmG5KOMkai3eZxVhCJ8Iy6xLcpm+HrttsFwkoGXRp/rm8bnUYKYQob7S/U3TrQdxEkCEyI2i3YjueKxBGKUsCScM0lp0uuqx8YW94N0vHFoLC2OjS8vnCNGHfNJ1k39x2zfMAGSKJwW/PDoqILDR5HKpw/iOKgpXAENwdxarrmIskPMkiDnsfryANJsU4J8FbRQrHByAj0kE+yD84RhRgJrWQJtXmJzZj8RnZovFrCy/XS+72VV1hu8dJsm9vD8GWNY/VhvTGo8ctIVUF/unOV1cMWtg3xMTJpciWx6/hA3o8ImdKmUMNATjEKLAWOr4hzulJVPfdtFvwmz9xjLNQoai8Cn9CnaWs3HMfCfarEdEQ0x8Iz7YKwciCMLH0GwzE+ayz0SGeCXXRVuHKjqA9zF5JfJhX0XOhuYTlAcy91yCahG2hyIPRubr0/lkeOLzBod4Ac/RAAMUfxC+Rb4jXdpaXG/erH4hBo1cBYMYbVxG7iwaijlATZA=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="UX">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="JFK" DepartureDate="2019-10-28T15:10:00" ArrivalDate="2019-10-28T18:03:00" OperatingAirline="DL" MarquetingAirline="DL" FlightNumber="2634" JourneyDuration="P0DT12H45M0S" Class="K" Cabin="Y" AirplaneType="321" FareBasis="MYYOAE" />
                                    <Segment DepartureAirport="JFK" ArrivalAirport="MAD" DepartureDate="2019-10-28T20:30:00" ArrivalDate="2019-10-29T08:55:00" OperatingAirline="DL" MarquetingAirline="UX" FlightNumber="3392" JourneyDuration="P0DT12H45M0S" Class="M" Cabin="Y" AirplaneType="76W" FareBasis="MYYOAE" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="1744.85" Nett="1744.85">
                                    <Service Amount="1562" />
                                    <ServiceTaxes Included="false" Amount="182.85" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-07</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="23" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhkff7CWp6dtKhK6lyCdupZyjfKElJTyHV/Xu8fcY3wsfQBF77qrhsVE0AvVX79Pj5Twdn1IBo1WkZMED+67/G9ojGWuaPpiUkxT70AdGcir+HLle8oNgeZ0KXMnwbBZxFJkL4tFEj09Zo4eg+Sbs2+rF4XhE9wgTgnHUGmQHt22iJqg16p0NfAfHTUtSR2KKe/zcmnAg7xY9+SI+GVaio2jzGOqtj1+kXtIvgAUkD+Z085eL+h3e9oCpFYzc1QbynhoTrrHG3jgreEGkN0wzj7+oVJaQWJ0yxsaOuiYtKVkyyYRqpgeNGbsSZfr03OB8rDFddWRAEnJfIxKM9Gmk98zHx53dZxuGtVJl4pin6UTPPufq7+0Hmi8RYtxEml2iG8YnF9LUB/ThRuMnao16mSDBU26zNaQvk6EoUB3/ipAE9Y9qFRNLiq/S4ztFwdzoqjogvO7zkFIYlA5xRdSDtNGey8+ONvybGgvaXGxB2u1wuZ5wHPXLr3/XS8vVIsk4B2EEdpuULVPoJY7pc99sXGbhkFRLwGDmc+uV5vw1neRchAc4J7zh0QrfCHZ83a5HNIYj4yr9m4PuYSXqgjVXBNEAcc2HgTyPjYd68EpnKpwziTD92gI3lcOiBF0QU2oE9lE4s/PjNE6ywVEiU/l0nwlNwgIJefDERcXCcTqsYRcoYFKECLijmKw5ynAtZfWimH/O+/H+NW1XXFfrI+kxwVw5hobtHd5ViOTj/Dn6CZK/BgoNlVXcmMPnFnuQDloFEMFXW3J7Fw7QItX1Eg8diZd/IJiM8153Ycg4v/Aq4twUk7QrUF27WSB7NMnZgZ3b8fX7puYvqgJVFvQsA3I4FQyub/+uuvlvqFo98KZd7fN4TwwEEPT7B+5iUopZAiX2A3fqpCt2tP9sIOzDC8zrDFP6skO7mq+TPb8FFni4YLZ23WKlPStl1jVZtbEQe00q9tVWDTkEmC2G07z4iL3xT02mvuZo2u0GpnJ6mmHUW5jinvjUBQqNeVmyvDi5saY2aM0AtKuIPqAIxfjfVtImlyAVD1Fiay0ZavLe6wWMOkI9zcXXtL60W0nyQax94bvSX/LBA3Sgz0k5R4g2dBu/jZR9c8VXxRT+ZDBFJXzI+UJwkQsrEqjtYkucQPjtL2hvenAIdcJlIbe2TsvzudRqTw7OM2JRdwz9Y9S6oqjMDs85BKcqZ9hG9hjaR8BJwfPESVNUO+XsejvCsUG3yv4Re/ywVAs06MO5ELo8cfm4JOALF/+62J/zsZvfICtxzD/rMg=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="UX">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="JFK" DepartureDate="2019-10-28T15:10:00" ArrivalDate="2019-10-28T18:03:00" OperatingAirline="DL" MarquetingAirline="DL" FlightNumber="2634" JourneyDuration="P0DT15H15M0S" Class="K" Cabin="Y" AirplaneType="321" FareBasis="MYYOAE" />
                                    <Segment DepartureAirport="JFK" ArrivalAirport="MAD" DepartureDate="2019-10-28T23:05:00" ArrivalDate="2019-10-29T11:25:00" OperatingAirline="UX" MarquetingAirline="UX" FlightNumber="92" JourneyDuration="P0DT15H15M0S" Class="M" Cabin="Y" AirplaneType="332" FareBasis="MYYOAE" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="1744.85" Nett="1744.85">
                                    <Service Amount="1562" />
                                    <ServiceTaxes Included="false" Amount="182.85" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-07</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="24" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhkff7CWp6dtKhK6lyCdupZyjfKElJTyHV/Xu8fcY3wsfQBF77qrhsVE0AvVX79Pj5SkpV0vHjMpNYae2zOSFPbMNz9qKpbs/t4I2s53wPtMEGptad1VPj933ta3zWyU5CLlYtF0FYvBe5zm3wgsIRulzD6OGbM0/UxvkD637YwICWomeygdYOBI3K4RJY0he3NGkvsRJgBCcYKVIcv2kce5JYCqqaa1DMByUmDTcKC8c2zN+CWJ35be05ci37Oi85pSddh3qtKj/KoWrcYLIW8pFQPnYxRhP/NXzP9U5TMxyfL8J2wqnxxHBw4PDUrGLMhJZyswxiKRjw2mewFRa4RIM9bRJAEZY4DpCuwsTEQqDicP2IjnQzJ1gVmWI4kYBvwF/HHtBnUiME+VAi9AZWUFpKFX03NBU82/Dsll2HvDnK3/G0GHAa2nVBCoQWJ9d8IOgq5g6ATlo40U8luLBYVVWDCWuuI7+4ZRkD9KUMYjOrLnyxHarN+QHQyY41dFfSYy5cnH0o2Q0MxJ0XWpTiXZ+NyyfAZnHDwiIiBZjO7QeaYn2rUHjYBDraNmKeQ099NCnN0l35XA7jJTAu/EUM62I2BdrvMx44nb6iDA8EMF31AW+Cq/kKIHq5Oskna5PmO3QFCtGTOH+okWl/rPs24YEzekRTW7aJraqiGxY3hFfV6VrZctOWaFhTOQpVxbr39SQW36dTX8/5TUVyHAxxL/KTO2Msi5vOtGgxuKMcUiTn0cMpLDJGrdS0ra2Ce0+d6JEyk7zvwPgChL2iZ0GE98/ja7cbDsAcAgmOJZTJCR7+n8SMOQ20vtKKTL9Ed5nvjaNkUP9npYrMSiOvcxyy6d3w0heXShz1KklaZYhGySTrc+N86JaNsq8Ys/EvSc88+7rUMUd4hAjIBz3HQHnzg4T2hl+HCoPxBFTUTJjxYQpY/w9Kzp3Rnw1ICTICk5WpDd1sT79W+7E1QhWkALCMWeGtzHTXDunJkYkPrsQvyJ3WLNbd+G1mfEJiY+zLOSnWXSicIUz7YBR9PPaLkxrigSFjxPlIqNHV2xeRL726tWaAkUwk37eiz21NEPddnwsQSSkP2/FilXer0x754ilpOnN0300ZCKKsoZLqubi+QFrPofCCfk9Qtp2NSpZ1tTl3Fm81Btvg9YjCzBvmbhtImkdUw94tVR35QKlIC/79N1dUi8w4s3vsWCXPq4LP0D4K6CsfEo2VYsPRnHsPjrfmRvt3X7FFJp8+2P6ToDl6Y5ON9byATaRY897AMV82wd6m0=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="UX">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="LGA" DepartureDate="2019-10-28T11:44:00" ArrivalDate="2019-10-28T14:21:00" OperatingAirline="DL" MarquetingAirline="DL" FlightNumber="925" JourneyDuration="P0DT16H11M0S" Class="K" Cabin="Y" AirplaneType="321" FareBasis="MYYOAE" />
                                    <Segment DepartureAirport="JFK" ArrivalAirport="MAD" DepartureDate="2019-10-28T20:30:00" ArrivalDate="2019-10-29T08:55:00" OperatingAirline="DL" MarquetingAirline="UX" FlightNumber="3392" JourneyDuration="P0DT16H11M0S" Class="M" Cabin="Y" AirplaneType="76W" FareBasis="MYYOAE" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="1744.85" Nett="1744.85">
                                    <Service Amount="1562" />
                                    <ServiceTaxes Included="false" Amount="182.85" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-07</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="25" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhkff7CWp6dtKhK6lyCdupZyjfKElJTyHV/Xu8fcY3wsfQBF77qrhsVE0AvVX79Pj5RgRxWJjPx5ot7Ou0N3hArJpXlAL/RxLhSqzmK6ukeD+cjgQiwfQ8/5r3upWO9UTj8JroSCzIdtoyTRgnvMPm1ZBEPKOLq22sX/1SJTyQdr2lRRQ+dosuwOJfFdl3NvARri0PHYWLmI49jDNa5RKqf6aIwhnisDpWOFN4wrwyHotevHVKxcNwTixBy5VxM25o/w8ulhGn95rLwUUYouZ1wK1TFvJ7cnAps4O73mPFsMmm1pEeRGs6nAnKXB/bnpxITjs8cLgpUC1TEWoYryzuliLOE+gmGntAAP2kYBgIHRtFbpPHAbir3ZwDjdyFZBLWHnHSTf/JrXpW3Tp0ITjWDU52WEEAKOrMEypXobdmm2PJ5Z/6EJmXbLavLPxoL+jeQvQJgH28fFGz+iBLBUiYiw5bW7lqDq8IR9cUt8B03lfE71dbuI2me1gjhR2srPT+2OovZXPUBo4XnIGDH4Dz13rLPSRxfb33AezPwgGdVEXV3+QItSRcdWjB3dnWeS8PEw3kHGa0P0GGf+MxUTktkDF+ZKJ3+Dm2+2ekj1jGpG9EUCFdoTltpLyLdbl0wSaYkVj7ncKg9xcvbvt/yhr3MaDPV/46YcCNvy2ZB/ivwkadWqOXA9HoJ9aef5xEG5Ns2Wm5CqyMRgoiFd6w/ob4SGudQ0mhYecQPxW7Z4tPmSsWBTxwQfi4e0mx6yNjqWjzeUehJ7Uff6B+Jc3/aKgj9x82dO34aHxK1vzn4pg+Rcbx3jxd7WEVvEURaUP3LQ2c66rOVPhgJatxjEM3g+AdBYxGOCQPYcKw6xLcWQPek5gnwQUOjsx91cQJi2fnQRJGa42fFwDDT1kzIVVSOC87H6Y5nzIkAecg6374QoxoSV4M+ZaPUD4ebXz1qinFcRCvVZ222QQ0okrj62wNPySP1tus5AwtyCCO6ACs3cUMoT3LxAPah7kXpFFp9o5alpmRP+H6Odfp7EPv3HI552lptPLEzA6E0kozY9Fp3IG6i0xTxhAF7SotxVr6Fz76Ht3YT0nl0+MsfqfsgWXNOOY8RfPNmTG1i4DsL2yPWGz6qZsplAeqv+sex11Izwr6wGSau3hmHZ4xBm0q8PUC8F3conODo1KRel+xLKq9YUsXsSGx1N4SP/uj0cCAh6sI2CGORJpsKcBVfz9H5HTKvmUR0X7DdjjOzYv3POQH9BX46GRpVV66Z7mhRqeIJzlIe9Hts=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="UX">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="JFK" DepartureDate="2019-10-28T15:25:00" ArrivalDate="2019-10-28T18:18:00" OperatingAirline="DL" MarquetingAirline="UX" FlightNumber="3312" JourneyDuration="P0DT15H0M0S" Class="M" Cabin="Y" AirplaneType="321" FareBasis="MYYOAE" />
                                    <Segment DepartureAirport="JFK" ArrivalAirport="MAD" DepartureDate="2019-10-28T23:05:00" ArrivalDate="2019-10-29T11:25:00" OperatingAirline="UX" MarquetingAirline="UX" FlightNumber="92" JourneyDuration="P0DT15H0M0S" Class="M" Cabin="Y" AirplaneType="332" FareBasis="MYYOAE" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="1744.85" Nett="1744.85">
                                    <Service Amount="1562" />
                                    <ServiceTaxes Included="false" Amount="182.85" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-07</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="26" Direction="Inbound" LowCost="false" RatePlanCode="Ffa1q3POCcyi2Rus2m2aUvvI4k+C7do73FaJXFWc2TmrUuRmhwkftPZc0UYk2Gy1nvs2sdEfYVnE8R/DNVtRoYbKE6F1fyBtU83CM5CXwCnTUxkcAiAT63r62NJ8OHswO8g9P2qy3QD4w2zPE+ezhCakePUrmYE3b+RMzcrmO4xJxTsYA6PSpbNglO1duRqTrw2scpGFBhwMXf792UkwR+/raebxzX1XHqMAm4MpqjWf6Y1OY0wnfamtKX5vTfFw4QZZB7+5vsExHaqjOanp7Xu+Wiyep215eIOd+7aIV7YyLLoJhwzHLKKSqEo2Hgsa1ixhx4HK2uOlcrI8FjazQOzEQmccqUByigmpIta5LecOw+RiLWppmQkxIVRm5ZVn3xLz7yt3KrrvFkbkqaWHxv4Z7ePqv8uSxvH5FEPyah8+c+XgX5zMqZSWP5+qtQWIEIQQbvFPB9Rp71327MF26kFkl9L9l84+KDnXJkpwyj8ZO/BHIiWRak/w5O/XclwmpipnkXvURzVFRcVrV/iBuuxeAdI/O8sQn+i/UyWcptE8CRiyOiJH8AY0flCnRhrPEoqORV0txbrvDMxM/eJRGEIvpi5zNoG8aypu4J5gmGaPCgn/HMaQUEMW3iZkVj8oOWEMGUMdCfpeiNNg5wFjQO0+jzQQStXnRPY/Ll+HvGXk02eGcciIw5kjZQ9L/vnLEN2BqDyP852rQpPrw7o9gmk5EkHPKsgM4DFlLI4zWLstMAfOCKiC9/kjTrN/woF96zH3EoSXJzlj+f3ba1uH7rZTxsEAvoyJ8pCBV5jEoIoPi4VMwhkOSOouAY5KdFZR3I7T6i3pU7IlndYE7wbH2/HQC+2dxxc+VnzTXkytGUwj6B5CYc8xzl7mkSD1VBcvh/Q66SA2cbHSEvnA3+omZy8YnPtmE/vlTbUKBKJDW1NhDfNEP8ZBK9NCPIAiHeH3RQhZ/oLgggZ4t/qghFbCaYwGuCNqIRLCfi+jJ07iHLNjTAsxkKTfUNqcO0sfHOl5aIkAYjRFCZu4vQi4QBP9sAhOIscg3ustiNKxeHapO9qeeLYdFUK1dAfn+SoBhsC27/SinXfzURTl8xN9zCMYf2nhLD0FxUGc+x0RGLp0AzmlcBXniZ3pmvw0FxmpAoo4uCUOGXMMq11118IdydqLR31eD9Th3j9FSy+RiTLU1u3kWb30yYMByGCAc9acWONlBlfHByWC57A9upnNR8QZUBfxNS4I/jAQnXzaVSndrXK94BdBhWzg4LKWHFWRdDoV+whB0Tw9IDzFjRFkJHuqC0aHkuAz49YyKwgHn2ZS8DI=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="VS">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="LGW" DepartureDate="2019-10-28T08:50:00" ArrivalDate="2019-10-28T10:10:00" OperatingAirline="I2" MarquetingAirline="IB" FlightNumber="3714" JourneyDuration="P0DT14H45M0S" Class="L" Cabin="Y" AirplaneType="32A" FareBasis="WFHF0OMN" />
                                    <Segment DepartureAirport="LGW" ArrivalAirport="MCO" DepartureDate="2019-10-28T13:00:00" ArrivalDate="2019-10-28T18:35:00" OperatingAirline="VS" MarquetingAirline="VS" FlightNumber="15" JourneyDuration="P0DT14H45M0S" Class="W" Cabin="S" AirplaneType="744" FareBasis="WFHF0OMN" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="1857.72" Nett="1857.72">
                                    <Service Amount="1689" />
                                    <ServiceTaxes Included="false" Amount="168.72" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-14</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="27" Direction="Inbound" LowCost="false" RatePlanCode="Ffa1q3POCcyi2Rus2m2aUvvI4k+C7do73FaJXFWc2TnSKHFPmJ+91MH64DWOAC8Rh9roy9dlL3We3bIKCyIhFJWXOVhXEGIG4TcpgzL0zYh36+QjUiggoFuhDVrGOCzrWgGkwPMvqeT4UYMb2HB9z/7PGvXwfrvoyMDU6LPoXz4OnbuLHvBsSRgUWUm9wkh6fmGwTn0paEF3e3vw2vzpBgBSS7hq9JM4uiRC6UY0HFC5crvoz/XTHfb/4W9cjmUNa1inIC7zekA/9m3dSF0j5deOVW756X4YeXAwxGeS/zw6rPGQEuZUnMQsbs/JOj2qLpE1nvtD3bNbY6P3xPK8IZqbRQ16TPrJNc4G/gWu266//6dd+oPcNzPEgYmkqeL9Drb6T7mIq0TwpLlDpNTpeVl+EvXkVVzVWSIDi+4DyUKdFrgjMpfBU82vxk91cqrR2E7JyKEr8XhcGNQDffIfbEkEpEOYwLgAZStXmfD8Ss52R+8goia3C/a2bLsSvFYcUh+IlVigVxfT6p8mj3iZTB2Y+xPFLPV2t6I1wIau/FMt2aMJKAJmBc67TrJT860r8q+N69aefdfkV1t2kMALlsYBzGp6IjHa5ug4ZUGUg3exmp/Jm1lxdgfs3M+LKHhccjtGeOkKxUfDd1Qs7d05glgLObfVrL6l3DhodPhk0P9C3IoUnh7rF+z7D7OXdrk9XCcz3BsNAL9yN1v6x2JN66ukwGfdH8bTS4a2IJWxCTKU9kBRBLJAbtfx8A+lZ50PzrzZxU4kWs3XbE3FvfyN/n+o2usySyCzfMlP/rp5Vqx6ao+G//TXlFw84XBdANJvnHhtAJ4n8XcwepPFrWVx16m7VzbKBC8BtXZq9zKmhw2uh8zhds0rX20/NRXZGx0II/c8NB2QMO5Xyz20sRRPl6Y/F+WCqCAQlDyWx1osDGHLE6ZN3pnLE+xnvLgJKoYMkSIl+KkGeyaHEP5ZwyYkaagr676W3F4btxQTV6KLcud1ivQ1+Z7CXijxqTIetIWmxuHe6UlLQofi/kQpKziXvrUdpzEDi4yzO4KXmWTrE/HDwr6jYleBFCpFRRw3aUyRrG4a8E6zqbCyc0rygZnaHdeQbMf2an+nVWxI3D3OFKqOB2WjiGdsQ5QbkrdSbkWqd2YUVrv/mGAUTihJfI4T72vFfIJrMslWT8yIlku1kkZTrBGrfggp8znCQ/rweqokaB71MZm2yBaUoqQQoOX//LMOvVVg2rOjBwJRa32XMl13Q4WnNRBSpRbyLl/U+bNYax7vvW3GjKGxou4CLNdV0L7m7tf2EWeGYT95/FtYRyE=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AY">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="LGW" DepartureDate="2019-10-28T08:50:00" ArrivalDate="2019-10-28T10:10:00" OperatingAirline="I2" MarquetingAirline="IB" FlightNumber="3714" JourneyDuration="P0DT13H35M0S" Class="Y" Cabin="Y" AirplaneType="32A" FareBasis="W1N0C9S0" />
                                    <Segment DepartureAirport="LGW" ArrivalAirport="MCO" DepartureDate="2019-10-28T11:35:00" ArrivalDate="2019-10-28T17:25:00" OperatingAirline="BA" MarquetingAirline="AY" FlightNumber="5447" JourneyDuration="P0DT13H35M0S" Class="W" Cabin="Y" AirplaneType="777" FareBasis="W1N0C9S0" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="1858.22" Nett="1858.22">
                                    <Service Amount="1703" />
                                    <ServiceTaxes Included="false" Amount="155.22" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-28</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="28" Direction="Inbound" LowCost="false" RatePlanCode="Ffa1q3POCcyi2Rus2m2aUvvI4k+C7do73FaJXFWc2TnSKHFPmJ+91MH64DWOAC8Rh9roy9dlL3We3bIKCyIhFJWXOVhXEGIG4TcpgzL0zYhmVPEFA+jVFGm9bQxwPHvQ/t6cM6XfwT9/GJHIDW/OJvN/6JGRiKCOAG1mQtQFhIfaL8/EMUMaAea12Yyv6UzXt56/RXni72W1xRELW+MQILrgeemipNsoCLsF3ET44ptQzB8yLV53BOFPVD0Ng1ZfcU5Z3y45X8VtQeisdimCuHUR8ezUQCDsp189lyCEgrDA6ypjhB/8rcmafS5im61XcOkBgg7B9np2rBlC35C69LOm0kQ9MA0IbyvgIKVa1bdjX0WfbsI1d30bRkCdgsunTqoCP4zpB6u3gcyXItjpA96USPMyIvjbXpj8jagzcbNDToL179ZCsabtPquEXh5h5LRqNUQNlKAUS8MtW/8YPqVeTk5pM3hqlU2/rdHTaZSfKF0ctu9XNWo7zM057dXxZtYJlMUI/HELrq7v4Ne2tFBvnQySmVNJlUjM1YZ8h+6x+7NZdICYa8DJ9OVm5wz8ygCwV+RMwpBIO0EwXbsB/4EIcbpRuHfnjaooDNZIcqmDaltONmT0G0she/Qgy1fvJzrJP5avZ3B03+6hj/XlhpvxtwmTzY1bfxn9W2V50HkzsJ0DriB+Nm68DbMJuVsrnwA6n0a+PLhrbhsG04hcYyeYuEpNH1JQx3cDWW8/m03W8cDM9xb6TsPpv2tX+YGbP3i/P7AYJqnyoE2MiuVmKRUn0MC1JeY/EQAf8sBMlRgs/2lmTbzci7P8u6xXwB1OXoVLqhDD1xu+ufOY3+L79MYl6ETbYIZ/a3GhM8OILpB4ZLgMNG38W526fNdnl3Bg+aZAWspcnxOhzegQT67maCwvtISsCuPDamUhF+6a4t8X5VwzkhlsrYraQ14ptQ0Q+rmomjniUXey/a5/BJXJLm4OrwOtFoYrs3BadeoxTX3R8SR1F6Una+enh+baUaIg8j8+IJsl+cAayd1hD2myhC4UPqoCr3QgPQ1H2oMWg1dZnBLaOGidBSpMgzo7RUshoepzYiV6pJHU62RVKxbBAjdUTYaV94Wp/HbGOTi20cHryIgARyzIM7j5MD/e08jbys4IdjyVry3LRQAoVaiNJ4KRJS4jrAwKctmVzcTW6R5qmHr0nK0L/EQM1Yqw9iUCuoDAtsb+fFel4QOvTMq4QnIxdi1Pwmt5h/vMkz9hmRGYmPAzSVAbA/W2z4e8cyyT2QxB6gV8NAQRYtkcY4GjUYdqPm4ysrO04LefpHAdM70=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AY">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="LHR" DepartureDate="2019-10-28T07:00:00" ArrivalDate="2019-10-28T08:25:00" OperatingAirline="IB" MarquetingAirline="IB" FlightNumber="3170" JourneyDuration="P0DT15H25M0S" Class="Y" Cabin="Y" AirplaneType="321" FareBasis="W1N0C9S0" />
                                    <Segment DepartureAirport="LGW" ArrivalAirport="MCO" DepartureDate="2019-10-28T11:35:00" ArrivalDate="2019-10-28T17:25:00" OperatingAirline="BA" MarquetingAirline="AY" FlightNumber="5447" JourneyDuration="P0DT15H25M0S" Class="W" Cabin="Y" AirplaneType="777" FareBasis="W1N0C9S0" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="1858.22" Nett="1858.22">
                                    <Service Amount="1703" />
                                    <ServiceTaxes Included="false" Amount="155.22" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-28</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="29" Direction="Inbound" LowCost="false" RatePlanCode="Ffa1q3POCcyi2Rus2m2aUvvI4k+C7do73FaJXFWc2TnSKHFPmJ+91MH64DWOAC8RrhWlTuMCBD79W+u3xVg2Wzl9eYoL6YAxlEseCGDTy9ELMQhbwlgdCM3AevTshgHENbeA1SZdLdYCXeIdYz9vVaVRD++0a93RNfIPKEqTV+eGfABTLKuM0R1+WCW9jiZLvyrEGSHKxu+HDb2EAj1KGMs33LocoBCLtf3wAaw4SuVo3PDIOQyAoozBzn2pnpwizK949YtxxAZkt6oRsFPrSHqqr+NlWuHRQ/Bl9HHZSp6AdQ36FYWvLQqn4/32IhnBvM4U8ELILJnedDkc1cEhSzV1hUmZ6sAiFfjEWwSbKJvtnVD+XzjULUObN5+ByjiXZ+J4IKFg9982gA96LhUCImuQ16zwQAwrwufYqXiMAKxdaDMip46PmVfE4XizgYEENbUeARvvgg3lRjS9N0aCNarnp8hgA76HHFwXmotao7hsuhE7zanywe2B8Wd7Brow4oEI03sFxZz/r66wiB0//jaRsLCcpAxFYNx7oSlrQhUOHjTUJWvmLLRuuzzYk3PA5N3B1HhoS+iQOcFX03zV4gAnuGsIdoaMbbllixe2xZOwHGT7skhuuAsolVoH0E/62rE5dGmGvqukk9PZhPP1JpP1ZWc/CoxW4/XjiMsJIaPbbguLGnmSA4kET/b+2Z8sFQo7vKzcTRjw3xPrQOq7/8u5pFEWmMgO80s7ifizrOoYXXFeEU5OUuOu8xokjvXix93quy+oOeYcWhwizWA/Efep10Fc60aDVrJqkFd2qSHijOupE+/isdj8qUW15SJh6teInu2I+Ncfw9sn3cbWk9gRjMe25OYnoRy4OsFFCzCeb6P82qW3DoUGfK/kGviqrYFRharaTKtHFo7ALOjccIHP9sIkjENw9GXO004rL1uucbtlYyMqkpMvRPoCpSKPixxRNpZJmRc81+CP/N8TLqES4Sezue3GQ0ZHvqsjOBFQ0E4oXsA9mihXJJJlld9Tgl4bWR+1PlSvNDryOwan8Gj5can33HKFLiPaNFCj0pWZxLcZu/nuP4G9n7d7lIgvURnqjj6SXIdg2z2bc17vTE8x22FV/RdcSzZig0jSYPvV/nuGoY2fLkVQ9Uz8G9WK9vzbCknFqXTi0kzM074ro5XkY3EQkgNf3A22LSjBL39DZ2gyOcFCUp8qKZptaMipwbGranmPQ4ZvS5pssFYY7rTgokiTqUVwelnwIDzP+BfRiT0noUyMAk8ujuZokjzM5BMGi2ZEO9AzcCuZ21r1QUZruv2YiPswzVZfiKllDrA=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="IB">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="LGW" DepartureDate="2019-10-28T08:50:00" ArrivalDate="2019-10-28T10:10:00" OperatingAirline="I2" MarquetingAirline="IB" FlightNumber="3714" JourneyDuration="P0DT13H35M0S" Class="Y" Cabin="Y" AirplaneType="32A" FareBasis="W1N0C9S0" />
                                    <Segment DepartureAirport="LGW" ArrivalAirport="MCO" DepartureDate="2019-10-28T11:35:00" ArrivalDate="2019-10-28T17:25:00" OperatingAirline="BA" MarquetingAirline="IB" FlightNumber="7598" JourneyDuration="P0DT13H35M0S" Class="W" Cabin="S" AirplaneType="777" FareBasis="W1N0C9S0" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="1871.22" Nett="1871.22">
                                    <Service Amount="1716" />
                                    <ServiceTaxes Included="false" Amount="155.22" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-28</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="30" Direction="Inbound" LowCost="false" RatePlanCode="Ffa1q3POCcyi2Rus2m2aUvvI4k+C7do73FaJXFWc2TnSKHFPmJ+91MH64DWOAC8RrhWlTuMCBD79W+u3xVg2Wzl9eYoL6YAxlEseCGDTy9ES0zYmcVah/pMPhuJNGewtOwX0deDNh3g2T6rhO0tHtTAe/JhjHPWX0KUXt/9vzYFkeUUCYTAhcy1nEkxd6RgGkITQ2stzWhF1FfyJQFS8uvJ2nBpRuJJC6qIDT97FqNQP5MqT5eSCedERXTJWufQYSw//V9xmt+6tWj09+XGMzqwvxxuUZ5YyZMiqMa/VzZUufap0uoXQ110kyv7d8oEHlcoPnlZvbcrx7ukNSi2TQ2tUdEv2jSPLZWJcwJWFZnY2U1LL6uxa+zcEZD2QCitB7VMvzZVOR1LtZkrRsB3b/ZoVHlsXxosml4i6GaaJ+R068cIo255Tc7SNIluqlwH6ZfHAjQW4bfnlQLGgNVclcFxL23kvWKmUCNdMtvs51bPN620PPQXbj67vuw1P8/stAH55E8DSj+VbPspMCo76Dei7VWQIjWDY4ZhhWKHbhhtd9dymtPsLRIYis/L8N2KA/uyuhFageSQ5JUo4aeVvDl+MW5oTTnrbkmtxbgIFp+ZNHiS9bj9p1iWZ+jiYx0PeVCnBR2gO2BcPBiSdHZKYy6M0jE/xDWk9eM7EBtSRgdqUCvAxnEf9kKYPacxFJtX3fTaFa0ZixjEAYuBGbl1cj8AZh9yPPex/5Hz6jpp3F7Dxk60eYpVKjbIe0JaF+1/uRXIqrWLo0BxnNMOnVh2bCfmhvjkY9cPA4DJF6a4wPkJsUOYsE5zXkT/8+Gb7SelmMTWL4yrdwWi6U/Gw55wUOms5CT3/d7gQQ7ZNU7jGmA3M6Pr2sCcJklh8RaWDg8GMRAh5GpU0nNd7l7IpaQGDfSQdIWXxokd0/0FWZqMsagZk4CV50axu92tPlGLGHW7XAS7UtFSdARpuTmeyQ+fIYhrECuO/muHGGgqKrOFpvq3DzGxUZ7czVk7YKIavJcZLWSOnh2KVCnh59ez2C58axpcZEwViIvWymhlhyy5mIME7L2PDQZT4DySi1G5S6iuHN7lzCHMhFiGpDW65FlikJtrT6Wie4nTm/NP0xd0bx0usjdtQIVOIAI0pjoe2wHWPxX7qckNtlKME/9/rnAZQdrCiBoX5l5vYok3/wdrl828haecQWt6JqqvA1CC6vPdUR69kTASzTHUFD+f8mVPRX6GXay82E3a4v7gudku7YV69OrZF0ZOL0qsQhqZRKmDvRByoIakOJUuFMD+yTCn2wNUmnQ1iCywMkZ2UTXGKIOQ=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="IB">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="LHR" DepartureDate="2019-10-28T07:00:00" ArrivalDate="2019-10-28T08:25:00" OperatingAirline="IB" MarquetingAirline="IB" FlightNumber="3170" JourneyDuration="P0DT15H25M0S" Class="Y" Cabin="Y" AirplaneType="321" FareBasis="W1N0C9S0" />
                                    <Segment DepartureAirport="LGW" ArrivalAirport="MCO" DepartureDate="2019-10-28T11:35:00" ArrivalDate="2019-10-28T17:25:00" OperatingAirline="BA" MarquetingAirline="IB" FlightNumber="7598" JourneyDuration="P0DT15H25M0S" Class="W" Cabin="S" AirplaneType="777" FareBasis="W1N0C9S0" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="1871.22" Nett="1871.22">
                                    <Service Amount="1716" />
                                    <ServiceTaxes Included="false" Amount="155.22" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-28</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="31" Direction="Inbound" LowCost="false" RatePlanCode="Ffa1q3POCcyi2Rus2m2aUvvI4k+C7do73FaJXFWc2TnSKHFPmJ+91MH64DWOAC8RrhWlTuMCBD79W+u3xVg2Wzl9eYoL6YAxlEseCGDTy9Fa8EZzOoWu4k00z97RyYE+Ob0YHd/txZnZ/RPI0AhCMSqG/vZ76kAv4fb4MA3oqVhAMLt5RJKYqMF3mogjhLO1FhJyXKVcKM53ip0TtUW3hZ2VxgYVMgnRNCB7JRaM0PUoaX8tRxoJgJeyYVqzWUI1vNkVK7H5oxVl2vpVytPH874zVaSyg55VQbHYTifYjE7uYuq7rPwngbDj3F+2SuFLwvdBX3gh8fF1t5DFtKavEyIU7yXi00BsnNzb6jFC0r/1FX6ga7G/JJoavdnXx3pQvQnxoHEDaKC41FieSCIXSbHOOP0ywwVIUnsCeb6ddqOPEk1bf+V3/BnfjUrximZen8GGOKA9F2wj33tvBFbfpQeJpRwiqXKqzG0ia3NT+Ead7lPsLwTJFpO75utlA8UeyC2poD4DoGyCe+Eo5e/Wswn8k00s9b9sUAkvxM/ZEU3c/tqM/lSuFXROpsHHtnSCFyDE5sURLXTxuM2MPQ/3xZLG53rbYoWi7SxFL3LAxP0wvf2fTOaEs4ebN/QCVWLbsHz7taol+7y8N6JIHjN4UlUWNLQE/yjeaFyAvHsuw9BUZ3svCexHEGdTTVaJzjo9oBjkweHbL+Y479BKXf3+ihJtiMXWDHKbCpgxL3UycxWw1oyyhjQCYQTAUwkwjpXKIgjwhTMZA6YP8/I2FTLGWXRxICb0VLTX1LaFczatz9Z/ZneDJa3ZJ+IUPHU+y365e3vFwQon13eG9VtqtPD3XyaQZEaymExiCV0yZat/U85HCK39quNqRcWHlUkN35mtLh3xGSyypeTfrJQDJR+3dJqT9aIM9smbaoig1ORqBHwRSBpZXijgFEGQdidJhZlqx+VzO9mpGm0V6RUCrw7E9bOKgxyR94r0Bcbk5WCXCuDZZjz54aHFlI39hWnS+NciTJfib6OqitR06rmoalhowi8v47LFt027Ux0dY6aW9sEwBwUSQ6NrT6JZOhuBxoMs0Ap9YB2vGpMZElTafdxVsFy+QKaAHMbBhTZwTO3YwesBVStm+Z2j2sY76TD9DB8RuZFhVnyLMU6RaZ4Q/rT136frsy+Gut3jdXG3iWRRF4aYfX4dJgDr+84sii/v4DEV42nMi160d3xcVMWapT5KuFoZ/1E4NJ2mjXk9GQTj7fU3EY/pS7ya3iqin9SpZkA7pNuX85vZfcFimwIF2XJPuZpA83Wuyema80Z/HJubbW0=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="BA">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="LGW" DepartureDate="2019-10-28T08:50:00" ArrivalDate="2019-10-28T10:10:00" OperatingAirline="IB" MarquetingAirline="BA" FlightNumber="7284" JourneyDuration="P0DT13H35M0S" Class="Y" Cabin="Y" AirplaneType="320" FareBasis="W1N0C9S0" />
                                    <Segment DepartureAirport="LGW" ArrivalAirport="MCO" DepartureDate="2019-10-28T11:35:00" ArrivalDate="2019-10-28T17:25:00" OperatingAirline="BA" MarquetingAirline="BA" FlightNumber="2037" JourneyDuration="P0DT13H35M0S" Class="W" Cabin="S" AirplaneType="777" FareBasis="W1N0C9S0" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="1871.22" Nett="1871.22">
                                    <Service Amount="1716" />
                                    <ServiceTaxes Included="false" Amount="155.22" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-28</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="7" Number="32" Direction="Inbound" LowCost="false" RatePlanCode="Ffa1q3POCcyi2Rus2m2aUvvI4k+C7do73FaJXFWc2TnSKHFPmJ+91MH64DWOAC8RsTGhyob/8+ZzdKt6uAsZWsnKZWXZCExRtLqJyDtQjHyK7bTM2dyuZYFSsQzrHzmfme8GDftz0BT16riardux4HJiWJXlmmHkKAIuxyELeGDkPz6/CpRWbzLZrD59dDZ/ovINc0QaoJri+f1YJcqGAagk7+nTd9Sl0LgjCGOk7gcOroLGeDEw8zvKAEoyT4Xe3SUQtQaMxmvAKfRFdMdJMbdHibi2a5HvMHPfewnFXwbQf0LaYR/XNriKDAHDKAwwHgsanADLBao/0WMgqIv/tvzUCtfjx0EGAs/R9COwkKqFafezrkX9JiM3YOaKJDcIN5+zmEwja6e2x5+QTzfmnqqao8Hh9rbrivVFh3CpE6VYlUcMKfBj3ie/F2Lnt66WVdxMAsg4f43EYY7S46Rth4rH9CrA7CxNA+L6PlZbshJylNxs51SR55rwmYKz6GCn0GzR//gtZyWuTg1gaqXHAUhP2SeUsMgcstmXNj2ts63K2MToNvxZEEvtlqAMmfYTJtMrkFE03rWSq+hv9OvhGiQDDMuRgHdjzsN8doMnsGo0UNGvFsEHkHq+ti4sGGepON7LLneEYKdgjF8Qj0S84Gyu2wCelnRxraTE/tzUPWfA+dY26Bbr2d0sCy1rls0P4rP84sh8qwiSjBhx5w7xLrs1nxXAyq8CuBHOdJTyixpzfdbsol456+3Zv7oQFtJG3OTmlVrgnquFgc1IkgSpbb69fwTLvsPi9RwcSBOk/4FBcqJJloC7zU00uDWCCSqYk7mN+tfiyPIrIdUeknBZP0iXTPWt+fjJEzcsZFLSzxpcDPGQXnyKLN7zcKDm6lkE+UNxB702EXkbd07X3NYZacx3vuwoSLc+VlogYMyHQa2X56qSSXzzCf+Ay6u6Hp3zTXb6ZnaZmXlRSxpRT6Wl8YIUp3NU7G2CYtUJR+JZp8M3ixAgulleSBcOPVRjeNyJ6AwzkNBZhxUa2Pr/pApGE5MqkxoLo3HjFn+JsxOYe3UDkAi9bGXJpMOUzO8NTBEOChvClurPx6g+7pXpZbXn5fP/Ox7JdP9KFZqN1e7PWpXa+WJFWeeAfDNiv4fUONPb6XwY+A4eaMsRJyADGl1G93o4Wbz2jN585qnrcIktLmVsFVuEg6/gW9K4AVY8dQ4yxPNc8tjv6x99h494+y8hPL5ZkveMhP240JCULPy6jWVgjMTP9+j4d0QHELPdQMmgIw1GlC6MHEl0QNBZ0e8swSuUfyf5y1U2G2SvEIqi+zI=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AA">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="MIA" DepartureDate="2019-10-28T08:55:00" ArrivalDate="2019-10-28T13:30:00" OperatingAirline="AA" MarquetingAirline="AA" FlightNumber="69" JourneyDuration="P0DT13H4M0S" Class="W" Cabin="S" AirplaneType="772" FareBasis="W1N0C9S0" />
                                    <Segment DepartureAirport="MIA" ArrivalAirport="MCO" DepartureDate="2019-10-28T15:45:00" ArrivalDate="2019-10-28T16:59:00" OperatingAirline="AA" MarquetingAirline="AA" FlightNumber="2232" JourneyDuration="P0DT13H4M0S" Class="Y" Cabin="Y" AirplaneType="738" FareBasis="W1N0C9S0" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="1885.38" Nett="1885.38">
                                    <Service Amount="1703" />
                                    <ServiceTaxes Included="false" Amount="182.38" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-28</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="7" Number="33" Direction="Inbound" LowCost="false" RatePlanCode="Ffa1q3POCcyi2Rus2m2aUvvI4k+C7do73FaJXFWc2TnSKHFPmJ+91MH64DWOAC8RsTGhyob/8+ZzdKt6uAsZWsnKZWXZCExRtLqJyDtQjHzUBodahzL5dyRFEbMUsswkJCAyvSszJYyMFVBDXPMUi2WyRnwij0NlBZiRi+yeuY02CWuLa1soWhXyBTRohU5d3Zu/nyEJYQe3lIKvZ1easWFUNPa/5sYAnj59jjI6/WJAdZWlgq2bLiWXnPUrfHiFS39xmssHzJYWERVuf9ca/nnwAawVPaRrSA/anybO+ieFWfblDCluCXA9MYWgKpCSNNdqWg32ckbxoSmlAy7CdHCf5qznQCHcUjw4IV38evs6sDmc0KhZh8O3ER+y5/mdIRROvIcYvVfeNg/PCdtId7uk50dEjQpQA6yvV1E5d8SXbRWmwcVy92Bti0GrP+lqUdz4gT17MzYN9wCzjtIWd2U6Z+FZEj+p5mrCFGzkQREfBk54KZqArHwPaxP54EsdmTp5XzSCSH6aMywRa2pXDSQOuFOgFQkRjtU2yIftUK47TeikXbSmBUeJyKHfyT9rRsghbZHmK6bwUmkcI9lEetyZmlhPW+dfb+bhIOZBJyZsdYPUeQoHaYcC+3yJ6fMWD6D/70SfH4S95ikkJOyYsuAoXiR5h/9npmLbrKuTNENuL7/m9B7NpwTlRLc/ljTM6P3Bu2WWWq6cc7VcxhKF7rVgRlOrSv13AYO6n8pQS2IOH+eBKmeJZZkzB24obO2IoJtJ5rN5HrRNEcCghI7MJn5HU520cYUcTP6eKN09goHqngKuiuEuh+YTm1iWyy9/OAbTfS3NRB2c40oxHuR8VTBPhIHW2q9LccHV1o8Ya+OWYr1ILEkTYcMBnzQsceK2TvZOqqv1VAixIP1O0DSXyTJAUMgMZXViH+TFRYBB7VWwveoAmUGXTgS1XtOiNjqS5Bc/Ozb8KnKxfvnu0MgQxkGIjnOdTS3U3qgWvDVqH6Ln6iaetY1XHmy32ZsjtPXvZiuNGOBS7PQqxoiFEwiIi7TMarfqTMkK3rgvWvIbmiTLQwRhOzKYJ+SmTZZhniSdQQsVuC9J61lgcliqI/M8Rf1DN6L3reu7lSoU234xuWrJ0KR0M9yrj+Tv79RbJ7OJzUni27rG1G2nPIHiATsHUdavl23MOlMhLbaB9PhNfPRSApcuKC90sNi3itKB/3LkHGDDJirZ/sWx1zUJ05sqaU8rRdBYywKV1XYuOsPz++AyzPhQwjjBpwDO3QY5+WgXznAOS8CH0m2o/yrcdwDbSGXhhgwOxbaiqrYEQrZotSs=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AA">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="MIA" DepartureDate="2019-10-28T11:40:00" ArrivalDate="2019-10-28T16:35:00" OperatingAirline="IB" MarquetingAirline="AA" FlightNumber="8637" JourneyDuration="P0DT14H15M0S" Class="W" Cabin="S" AirplaneType="330" FareBasis="W1N0C9S0" />
                                    <Segment DepartureAirport="MIA" ArrivalAirport="MCO" DepartureDate="2019-10-28T19:40:00" ArrivalDate="2019-10-28T20:55:00" OperatingAirline="AA" MarquetingAirline="AA" FlightNumber="463" JourneyDuration="P0DT14H15M0S" Class="Y" Cabin="Y" AirplaneType="319" FareBasis="W1N0C9S0" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="1885.38" Nett="1885.38">
                                    <Service Amount="1703" />
                                    <ServiceTaxes Included="false" Amount="182.38" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-28</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="7" Number="34" Direction="Inbound" LowCost="false" RatePlanCode="Ffa1q3POCcyi2Rus2m2aUvvI4k+C7do73FaJXFWc2TnSKHFPmJ+91MH64DWOAC8RsTGhyob/8+ZzdKt6uAsZWsnKZWXZCExRtLqJyDtQjHy3NuL6Wz1BJ7Fb8LQqEBqGnGBjmpKJ7i4pu43MWcamOM7JS0ESPL8EQ/qwumFss2UBYbYFREVHOHuCBG+qSy78dKwRjPfXsKTdOKZ+Lhg1iDtJwmGsKeXuAKuTvM+H2TLxxluk5P5uXB0Hd/jfSCVFL+eg5W4U9UkgMT6KtUT2xA+u6yA1tXlg5yoTGaeX0A6VWgDNCSy0c7WsbfYrnDdI+qfSUuqb0DdgCVcL0Tsj/W9tyQP6feR4Lk9wEqzH96F4bXnDrWHwSKDyFb4wPX69KwwT0zT89O4GhQ37qK4DrzTWHJCSDyAlIx/wJT1Xue83LZMwFCYUojcyZE2RBVwLVBwBthKRESty7OdGFtF+8bZQWvAKmTMCpBKMWzJ4r/Fv4ATR0taFXM26MwmRcWTzqg8OvT5jZlm/X6uEOdZ8Fh/m7sfqRFiJyMagIjngfLafEVJLHSwp2iRNy1NP29APaE6uWlm9rPkds3kmooQ2oK4GX3D3CCVAWiCKRLOiQMYydMElaJPsgJ//UZ0XZ7D6VHoN8lVEzQHj/C4Bu2ulGbSNJIK2iYM22tECVvzYRHJGtld4xfQ3doh3H/1RbJYMP9WybDUh7WML5aleY05g37seyImt5K5ZFy5n/RGsaeHx1fgSs7qFtsyIQUOcI5OYfD27XGjkXikHXYEb2whfOGeDBrvONvf6EanGPIwo6aysEdNwflkezMDOwSvhXcNZNmiOAaU4PhQNoc1uZENH+TG14WnaEWLnarAYwHcakclmSpmHB6mWid9avMnr2LJySPzSKg/QgPEcyWJY8uva+ReMTituEYcPnjj09jSWBmwFNiDYm77pv4be/97ljCy/mR7mvHNAWp3ECT0ZJfkO0V4z3PLBmgM+3W911d4BYVpjcPkVU5kr9b1xMHWGK+lMVK66K+M8XuVTDwOnsG9DORZSWOqd73PGthMb3VIHfOcblSM1HxUu/kYk67KmkMzk43AdWqGRHXOrVIR7a8Yeu/YZvzKPvwBXVvwJXyFQK4jsrVFVuGu9z5Ys3BSUBe6U60bFRhAGnNIW+fJ7AAB8AXVc8gYtSdNf6OHNWBoxONNqYalv+rwTqNAoORCkDIfxS8heIHxXnRwUlMAA7Nzg0wQjUBTr+mATORNY/PgiGByjhfI+AYSY+4YOqHx1MVwXvBA0KhNT2oWxItu3bY0T5NFSAA8vnrez0Dw8TVfufI4=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AY">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="MIA" DepartureDate="2019-10-28T08:55:00" ArrivalDate="2019-10-28T13:30:00" OperatingAirline="AA" MarquetingAirline="AY" FlightNumber="4005" JourneyDuration="P0DT13H4M0S" Class="W" Cabin="Y" AirplaneType="772" FareBasis="W1N0C9S0" />
                                    <Segment DepartureAirport="MIA" ArrivalAirport="MCO" DepartureDate="2019-10-28T15:45:00" ArrivalDate="2019-10-28T16:59:00" OperatingAirline="AA" MarquetingAirline="AA" FlightNumber="2232" JourneyDuration="P0DT13H4M0S" Class="Y" Cabin="Y" AirplaneType="738" FareBasis="W1N0C9S0" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="1885.38" Nett="1885.38">
                                    <Service Amount="1703" />
                                    <ServiceTaxes Included="false" Amount="182.38" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-28</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="35" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhkff7CWp6dtKhK6lyCdupZy/4rH/zaxMAwRBBniZdomXmd99ghaBxR8Tx8Bb8P72oMuPLcBd5iTuPzuq10f53x5kZllpUSDnIRr5/b0OdfqKxSLReXbgDLZdCpuk/9QJAjWHZydbqrnb5nN6EO3wJKf6GvFnteG8GhA9kg7ZunUs9I2S1CWlnlVmg9BRwzV1kx1xp8EKdywZJBIBk0OLWtYrfiyD+/BV12mzCG7UcjxaGDV69f6YbA5YWwmJuHHUCHV/Ihh2n0y1uJk42bQa+PLphK+BObfpBCiBZIp8yd2kWInWITmbojSnMoGGsBaKxSS/f99T3Ja42Om+ROY7TrMA2HbeJytNOzoEHxnyph3ZjRiZDnS6/KsQAOgE3bhCptgzpTWYNbOVuvx4aYNgdmSiLe36gpO9dofoQCzOZE7VyLUUoJTc+8VKl4BX7yoQ4e2fmFJY3No/O0tdObwXXxnJApKTfkV6TvrnhkuQ1GouHLKI7I4zJQ8U6og4wynDyAa6kVP32p2qYNSjufregkrjj0gWygzy4qIGggQEw1AIPJFPEGFk84+VsNCrwMr3tWFRQNp3WrI3ubCCT7fmNCf9YvLccy6VgIcUxSAuNnGDkxXRIfpZJ/VLfSXW8iJKffHprO4C5VeEJCpMhNbUbj0XmBEiok5rhUhAhmozJRzLAhB8sIaYUDWemr+TCbdZJcfafhv0G8r3wFweJxJ+BKih53xSCjM3W/EaLu4VUko4dxDe3VGN3VCm5wlFXtVkzn3YMEjsDF+Eh4JJGnuMtL/rFHfQMN6MxYT2rOFbBVUNcfWOtah2XGUD5daRnRMDmSZZzXKNjZ6g+7zVAwmRAIEpX2U8oiStb9/E3Sl8BWoYPqs36zRpJfCPYSm5Eruc8hN+H3BU4vLFUVNa1MogemJAZdSGHGCD4lo6aNVDPGRS4cesMobIGNqwAICZGn6aBaiaze8tiITK5fYZvVxEmNuPV8u4TLxw8byvmogJLCpF/0HG5LiUWL8c5/+5dJ1BxHQuPMhnHVQ7G/gPIvVpATvJOBekt0NEO3FZkp1hvXK1dRVkPNRsliBdITQoSJnpWzH+dz89dSPXT7uZDLB3uthOh+Qx5yCiRK0WaIwTx/1OxTVhsbt5lHuJ1ijqq7UEx/je0cbtVakICu5/f7Q7SPfpdUVnKsWwBuQ2vNuxm5V84I33UVn9CMYi+69G/h1d3I10ei5xbfCMILyv6s7e3YQoT2im5vzhIQXhHe8FaDgAGsoV52k7e+jUGcG3MRQt6U=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="UX">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="JFK" DepartureDate="2019-10-28T15:25:00" ArrivalDate="2019-10-28T18:18:00" OperatingAirline="DL" MarquetingAirline="UX" FlightNumber="3312" JourneyDuration="P0DT12H30M0S" Class="B" Cabin="Y" AirplaneType="321" FareBasis="BYYOAE" />
                                    <Segment DepartureAirport="JFK" ArrivalAirport="MAD" DepartureDate="2019-10-28T20:30:00" ArrivalDate="2019-10-29T08:55:00" OperatingAirline="DL" MarquetingAirline="UX" FlightNumber="3392" JourneyDuration="P0DT12H30M0S" Class="B" Cabin="Y" AirplaneType="76W" FareBasis="BYYOAE" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="1926.85" Nett="1926.85">
                                    <Service Amount="1744" />
                                    <ServiceTaxes Included="false" Amount="182.85" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-07</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="1" Number="36" Direction="Inbound" LowCost="false" RatePlanCode="Ffa1q3POCcyi2Rus2m2aUvvI4k+C7do73FaJXFWc2Tn+QvDhv+mN5m0dR9RZVrSWOHj+0HSKZrKRdSB2oRFjVoyfk1fDvgCKLff8BQSt2IXPl2T5tWShDLSWLwDmaCisjJDRPLRkREvsHtfz8g9NwpOOCctGUwGU3DisHntZRd5hjHmgWJf2GzJH34XTx0ZmuF5twq2YtbuXlO35Uqy28tce66bNCmkfYk8pLy/zgDHyWXahkeZgC15CyqYVsLTbkhl2fCTIZVAXee8uNpFcG4z6NBa111a8t/lgrGCzRLwH93pJQEJ2uhRpo/OgHGrIFxx6Yfa/WDKo93+lMXX8v4RDayFzUS/dxcd6smokXk0XSfBtF54cowHwfn0MBB7V52jwgR6uMgv2sOIrW8Khv4gVBFbpr1CGxQEPL3K1Hl5ThFqxw9P+uwKdmCsRX1Fo6Cpvmlne96+YELuyPhFpkcePPltqx/GWxmsqYywuu6Q/WsIX6Tf4LFXxANyK1n31wbQZVcuI56uHqd7wpnu3FR32SJTb/qlHpeVjWn94JTl8wbJYClmvfFOH2umc23ZtGsq211M5tSuPWhGEb+pOTujOwTgNcJhcsCipAduG4tFbn5aznd7DzmAq9ldqpgz8ZPv6+XLzC3AKnhCUo4nZ3JLupedKSBfDGARa41r41pY66EHq52ZBnqZHkS3PFnSvjgvenI4qHpN+BT+70raZNySbne2101zK+TRYUUvk8g+MBePXvw43qRQ07GWfC8t30Moo9PBiytLQs5w2wJa0x3Z1b2GkmTT+jIfAT7H86x4i6/djduodqHWPR3sgZkd1Q5wcLODsnDvbZsiWS4WaO2uvpSChy6sD3EiOMVwYn3Ac5gmYeqp+XXJOS5Z2ZXr5hPoNFw/7DcqFdi1OW/V2Vz6sPg8C/dK9Tt84AS5l7G0Y0CROXB9YSU8m25IhOuK8x0RNVTCXxrM0fd+iXmI9p+uPgX0Lc9P2YCCCZVRykW5FJawvuy1NxfzaWn4VB+fOkCcSElhZ1SoSFPdyns+zDbKOur6W2ATp1dTLwmx7MzRZqoGS4sr/AU39OmBVpVC+isRVEt+410Bh/dMg/K89AjAPD1L3HyfipzoAujnZuq3/FdlrPcPYuFQMEjS3GizmKFYMk+afHCMEONBT/1DgoG2NZXuDA2SgNiG00iRO0IPTMm7hkEgxWR0nUUE0W80g6iMRn6dOpcvCbVX6E2iQSI3cb8CrEbwdbY48+pdxSqBlinKRUOqpg1JPE5P4vIXfAE3sVLj+ibbOiT1Ef3y0QLV6K4amIvYgIBWnlRTPsvM=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AC">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="YYZ" DepartureDate="2019-10-28T12:35:00" ArrivalDate="2019-10-28T16:15:00" OperatingAirline="AC" MarquetingAirline="AC" FlightNumber="837" JourneyDuration="P0DT16H11M0S" Class="O" Cabin="S" AirplaneType="333" FareBasis="OFFEU2OW" />
                                    <Segment DepartureAirport="YYZ" ArrivalAirport="MCO" DepartureDate="2019-10-28T20:50:00" ArrivalDate="2019-10-28T23:46:00" OperatingAirline="AC" MarquetingAirline="AC" FlightNumber="1676" JourneyDuration="P0DT16H11M0S" Class="P" Cabin="C" AirplaneType="320" FareBasis="OFFEU2OW" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="2009.45" Nett="2009.45">
                                    <Service Amount="1829" />
                                    <ServiceTaxes Included="false" Amount="180.45" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-10-28</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="37" Direction="Inbound" LowCost="false" RatePlanCode="Ffa1q3POCcyi2Rus2m2aUvvI4k+C7do73FaJXFWc2TmPT3BKfvjpqXftaJpZgZWzks+Q7eeziI6kJ0Tz31CPshpkg9ToIIlYerQfmUultfnsYClX8kh0fabkNl+5W87uOGNSNwJdRLWw7+26t1e40CKobAmstheIy6ByBxI52YJnrA1ECx/unA0x7VJlI8An5T77/Kvsy+1PYbpxVROumMLsUkDTQKJ6UJ5DlYl/88KQvAeVRGOd3znGx8FWhyePfpUpUhDVIT7vIWVlkrCPmEgVG9NMG1BEbN07t+ljMrAZLYqhAhrMRUqZCbtL7YMgr/EYXfepq4usQyG32zwuvM0NHQRkhFnXjeiMhqIGS4aoY5CAkTXK9RRHiW4NecZ6nkXBo+qaFoEaeF1uk6C9G/eBKJZraxkTPs59VR7BBZH2tbQty5v5wDtRZRG1TlY2bjApANHxK9xyo+bzNxG/IqM5WdphzmMmQE1LHAuo2X0hZ9gN8tsMafbzjHe4JX/20RcYLfDGQsoyxK5kQZS60XkymQoo74oOIVrK0VK0OMCCUBp/FLK+7dn+BT0r1huluZYq1mgRzvlHtlM7Zj9dxNmHULpm5qpJ9j/BUx7cKFugjdYeEl6SQm1ugcLafbn2eo2GXWIEBjFvSPFyOme62EVXvAVpkXb/qRu5tdiQGP3jxz75kmWVz0MzWvqepFjBtB/H7GNk3kc7ziZ3kprT3xodtGdCzKFa00jaFvK0LuV10yoTfeJhSXB/N6Q4vkzgUEu+YHYj7q5YXwTN4OAh+/7QW+wWA3RuYHITrKmPrTqEcb0YAqQfxXBDNbMfRIj4gZhJ3DGq4j1DNAFwZI3WOEy38II0n9C5HrLBCiA7rDBVVAVz7kLoqY1n3UdCx0BgZQ0wJZCSDpR5tyK12kuhYjFGmjzD7SdI4t/Zo0RmR8vX5lbkuR5S1LpilbFSDo1P+60eJ2ODLG/ZlLo2MBR+qJz74+8vdXZntrFzw6WZjsWnNsQN3+IRh9hWxCTmrarj2+fnWiIICOke6JgB5VyaCq4o90QwYFHvMTzXn/9wkvqx7hLYeEILVYRa/wHXXqb9Iq/7sO+pB6rbbPmjSq4OZKUqpVfNx8k2K9y5IxZO41WPhpEVq1THX39ggL5me+oki2yUYkyZi/EAAqkeJEOcAVMdHB1J+7OjB8ECECRpTOV/8gyNepBRCibErJQk8ZfzD8V6af1yH4CqcRWFxplY95igvE8iKzqkpJf2T+b9yXHBd92kK8qlhl/bcmuS8TeGiHGuOFCulfPy6aeH3+B4r2W/rrBRftmI3rJxHpFudAk=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="LH">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="FRA" DepartureDate="2019-10-28T08:10:00" ArrivalDate="2019-10-28T10:50:00" OperatingAirline="LH" MarquetingAirline="LH" FlightNumber="1123" JourneyDuration="P0DT15H20M0S" Class="Y" Cabin="Y" AirplaneType="321" FareBasis="GFFEU2OW" />
                                    <Segment DepartureAirport="FRA" ArrivalAirport="MCO" DepartureDate="2019-10-28T13:10:00" ArrivalDate="2019-10-28T18:30:00" OperatingAirline="LH" MarquetingAirline="LH" FlightNumber="464" JourneyDuration="P0DT15H20M0S" Class="G" Cabin="S" AirplaneType="744" FareBasis="GFFEU2OW" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="2019.07" Nett="2019.07">
                                    <Service Amount="1829" />
                                    <ServiceTaxes Included="false" Amount="190.07" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-10</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="38" Direction="Inbound" LowCost="false" RatePlanCode="Ffa1q3POCcyi2Rus2m2aUvvI4k+C7do73FaJXFWc2TkYoYnK8b8DuKxoOr0EEqN1PGOyE6d5cBQKQ3SJCrF+izTcGsFxQbASDnFIjhAITLDN3XrZnyDjggjjImSLV/jHVkf+Vr61gl2ml9CtaAm176xlXwhCwGlPJci/pkWcXL2wHWePA3Yth3JVFpMKnQAUwxihp9nxvPMEeqKnS71vePThvPuYtPTmqyT3RsiT1xe2DPjZDhOKa5eKwpIWEFxzqAWtxpafeo1MKbb6373cHlEnrOoQBjpyM51j7Lcm8BaxQJ6fMxybhGr4qUqHBMIh+FsKifBKgW9V8CPNfYue/ajxNXA0BIocj3+DBMKZrcc+46srt7t33Xh0CqbGiOWaGaN/MWdDn99X9ETLOXERRaUd209UBrk/Z2QhTErKzMlUzh2CyhLLwbYz3YKalFXtz/EeBwlucgUgEDhkE2TYKVZ2+ZMAyeUUhT3rYRUFGF24gebG/vWKa5EVJqiW37+fRHxV5TkRTnoXD/O3Vg9u2RY3LBeYrj4on7oKrYV6/sAQwl4lO3/qSAiKXkH4JXHi17bnFqwNaz296Y+2/vRGvgzVX1Y1A9ytmRxYsDwGqS9O6WSmKHUUc3nFWHH+2UZ9l0Ol8MNz/1Kg5t/KZPA8+9cQwSArbFIUUc6dJe0vEYao7Dl9FuqKVKqbPD/+tdYi/1JC08u4J3//arVNMGQkcG3rlru6pc67riOdvM4PpqRXEtXk51LVzv0GiLscz7pl7NUmZxRYilBiL5P3odRUqrQ1w1auwG6I7GCp3lUgcrCa2vDVtOsJzmKcAs2/UiXN7skrKCePLsfZeXSqFCgd+0NxW9XgNUCJNe0SDpv67f1WnoPiFlsgVPBfeJ1BL2VvFQvFAgHOl9NOqq4Xot1ocsUxqr0FpjCFKTb4X1wNcpme8lRoSKjDOizAA6eZewmNrUSOD575YhUWchOrx2PrHiJxTz2dAO2x43NJ+0ZfaVbTKM/jUbP+ES89iIPgyab4r8eDIWqKR2sHGnO3d3T1jgnesi2rLO6xBoIcYb9RupeuTgDw1rqDZvsJ5qS1Jmpg86BNn7NT3I1btlVfGQV0lelVVZdz6zj1rqUiAE+gXjJ9EScLw4vZgeUYlhI4m7HOsde/eybXf4MLrVrDFwxzaW8GaJ1+wxsPaTnrY2zQJ1KE3bbJ0Y0iZqES+VPC+WxJ9wrk5b2Z67P1aZHypF8XNkH1VAOIs6C6teI1+HJfuD5ZwnW0/1Nr7CUhnVt4IxbtMo2vI+mp5b6UGDhPQHkyan0tPCU+9JRi4TNTphcIa3k=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="UX">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="JFK" DepartureDate="2019-10-28T09:40:00" ArrivalDate="2019-10-28T13:30:00" OperatingAirline="DL" MarquetingAirline="UX" FlightNumber="3391" JourneyDuration="P0DT14H7M0S" Class="B" Cabin="Y" AirplaneType="76W" FareBasis="BYYOEA" />
                                    <Segment DepartureAirport="JFK" ArrivalAirport="MCO" DepartureDate="2019-10-28T15:35:00" ArrivalDate="2019-10-28T18:47:00" OperatingAirline="DL" MarquetingAirline="UX" FlightNumber="3395" JourneyDuration="P0DT14H7M0S" Class="B" Cabin="Y" AirplaneType="321" FareBasis="BYYOEA" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="2025.38" Nett="2025.38">
                                    <Service Amount="1829" />
                                    <ServiceTaxes Included="false" Amount="196.38" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-07</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="39" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG7u0zb/LrEsftJ3ZxT3KCDR1/C/mD0FgIKa1PL3XkpkOQNABAFwf8Zq+rsYWndggEUO6kvE3om/b+jGcNcFMbRX5Jl2kgUMKtJnWScXFQWb94CJBnvAeTBzT4qkwkkc5h4X3a5MQRElplc6Xmfv/zFeu81eRHxNnh7lXBb1BkV/134zqHSrzHEojqVUVIzEng0JCs5tsqtebJGmnSSAOkbi+gLKmOlI1ijQxWQyxbn65bADcMYLF4WxcDamu1Bx+5Et39SdyGzo2ktneSSfmYFyiHhf7183OVD4nR9YtpScd6WMxQCm6pVkhlBKmTV+OKcGpj1QM74g5AdrFYgOkBZ0N80qlGfJy3HBaIPXE1bl5Wq7/PlVDxd/MlRW0U3Ph14MjcEmWU54+8PfCRZ4VLDH/CQv8M9orkzHXszGay2G5fK/9lnDw+yAvcyxmefZEgBVz1xdJ+BacetSRe0oDg63pIxr5zdGXZdy+t81GOJL6tjebg6o92NU5bR50DGnybEVATgXmXlziQHnk4yCKOE9c6y+Ob+YWXE7eSdRN30pfY0XhTfryPYhQvXCVfjfuyXMsOWqrqJi+NyRkji4V0TwGlM37W1gbpglWq7jMtNK+Bf4KJR8RpE48+/XzCx/scgIdwx3yro7cn/AtHaFP+MEFx4hXZIlE1uHzRGar474dALxqT6wIvtDlQDTOOOqbar85IDXJIXLKH3m7RXZ63rhF/BuFjkFnDTWuD4AEwGJt6EyVWdK44Al8EIWEU8xLTlCpRvgbKLUVgb+DiYPzTEdjMCFtwE6pX8GLl/AxtFg+AcQGufXZ3x2q0xtnULj1FQIX+BjyusGoCrDBWMouFg5vRHBiCyt77JV8otJNzku6YksrFAUN1PJvLbEhuUYJlLQOFdmJcVq/gvZ9b5ykMklgJV8pl7sis/Cs/D8yv1mopR66qO6a93oA/MheNBpxJviDP/inbMUTWvUV+GermAUul0Wgf0Hcluwly45wwAGuowEZdE620nRqdB9s/Lg0IC2gd38jzfV8vmNEvgc2bC2+xpPkWrVE5atU0AFjYLPD9srdDD+bzU7GSdgNAw7qEGFSXind5tKFqpDMmoY7pkW6yCbtbZ4iGaCNfQco4UWsqxPP/2PwEDbu7z1IPIb907rbEPwFyf8CuORJbQpFLtorcI7jmgyJHdJ7rsdlOBB2ixps5iOPtYFz+83EmpCY1NpSh1vu1gHNeegkbZRlAveY9kfEWZxtIT3/MNRGv0N2A=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="UA">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="EWR" DepartureDate="2019-10-28T17:28:00" ArrivalDate="2019-10-28T20:11:00" OperatingAirline="UA" MarquetingAirline="UA" FlightNumber="2378" JourneyDuration="P0DT10H57M0S" Class="B" Cabin="Y" AirplaneType="739" FareBasis="BN400RCE" />
                                    <Segment DepartureAirport="EWR" ArrivalAirport="MAD" DepartureDate="2019-10-28T21:15:00" ArrivalDate="2019-10-29T09:25:00" OperatingAirline="UA" MarquetingAirline="UA" FlightNumber="51" JourneyDuration="P0DT10H57M0S" Class="B" Cabin="Y" AirplaneType="763" FareBasis="BN400RCE" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="2079.85" Nett="2079.85">
                                    <Service Amount="1897" />
                                    <ServiceTaxes Included="false" Amount="182.85" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-03</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="40" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG7u0zb/LrEsftJ3ZxT3KCDR1/C/mD0FgIKa1PL3XkpkOSpk8ocOVpx14AWCMAAgSw05k1DmtgMsv26mty0HCAjORP/iiLXmS5BQmKw4p2FfKW0rS9wNGfMD54OZei+bsY/XUDJtG8z3hTm2eKsxECfsqkxvdpka5C163CxmwcNpREDLulddPAiWo26xHDBIbFngg5T7xOH08NyhT338NmQl7/0SuFKuZS42CaRU4WfztbTrHRo0SGgLvJ0S67KcxCNcrnwGnKLuXEceA/ZNAledRKNU7JTicbFUTJ/gQPkypfK5/sx1khhtUKmerzPuzbw3gC/kQIsKBvNRIXGQA46YoMYw39JHo1nqCFPpJeklFgBMWa0suKy1XCmTjlUMdyAf+k2WLhKbhFaSArKRaZXfpIrnJo799C+3Tjt0ewrbDCo2Q6Kn8Zfn/3qkh9+8fzyNZp4w1KyYic8+7TsHq9C+4aASZmYHuiTnksv5pVLNZuKibMjiCQ2OJirx5kFmMw22RyaCBWa4Wg6R4r7mjwiodQCZRRWGc5jO91EsX1QRw+O7Jwnzyv0xlp4fuVP0Bj1OdJnxcR13nZAV6E0KTG4aoZaFiuE9oFqC66OhxETSLHC2BBG/s6UnE2E+yWdQZqzNR0tcNDm11rwpTQyobiQsmN6jEf5x7YSXV5vzCNVW2kRQWvkjUnn5SVzwrMUasq1iFqAwSjzmTut2f6i98Fjf/S1JMGE0rgUR1lLfF1CukIYNBDH9tFlCbgMOKwdoSlO5CFvyktkUvMLBfZiYGOACyNLOs7hQpT968Ry80KjEmdhPAdjK55ZacLq9asQjZpVjWND2SraN84U2gmEblv+mCqCG4Yv46DPBfej6L901oa8GTRSCeyq1Ky9APYpF60om5MOhhYWgMy0lmQ6JQjIZ+CFhrSJ7s9SOG9cT7uwQ+HdUPquPxAvdSfdHd8LRStrdzRScrL+49u1zhn6okHiGQ7M5P/q+WiuWKw9nGfLksQIymZxWpV6PUOPh7wSvLgQZIQ+5792hPbirvVuU9UDUex+cAuhZD4uSaAmVU/tfdv5ZQMWNPDtbcMFrnzr/RY6vD+mwLu9lqwsm9KJpX+s5sFwOeJDuc7dDYb6dGQswFsjtgrainG3ISb3FVGlwt7S/WOqJfa/yyS3u2FjlEVCcit6FGTS4HLR/fFxqm6TijQzBPzDYFWv3Xtg8sphAcDEXPdoV2UovPvTIC+YkMgXhVAs6yWh17cqD+ugttL/igc=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="UA">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="EWR" DepartureDate="2019-10-28T15:02:00" ArrivalDate="2019-10-28T17:45:00" OperatingAirline="UA" MarquetingAirline="UA" FlightNumber="2375" JourneyDuration="P0DT13H23M0S" Class="B" Cabin="Y" AirplaneType="739" FareBasis="BN400RCE" />
                                    <Segment DepartureAirport="EWR" ArrivalAirport="MAD" DepartureDate="2019-10-28T21:15:00" ArrivalDate="2019-10-29T09:25:00" OperatingAirline="UA" MarquetingAirline="UA" FlightNumber="51" JourneyDuration="P0DT13H23M0S" Class="B" Cabin="Y" AirplaneType="763" FareBasis="BN400RCE" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="2079.85" Nett="2079.85">
                                    <Service Amount="1897" />
                                    <ServiceTaxes Included="false" Amount="182.85" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-03</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="41" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG7u0zb/LrEsftJ3ZxT3KCDR1/C/mD0FgIKa1PL3XkpkOQJYtBaGcWFt74Dq9h4ST29xGAv1Z7e42sGrYwY1pPzINj8w2ZhVoKdWZPuwlBbOBrUP3BirrYaswvOLTGAHX0v/L6pmHJCtPB6yLbg+uImjYZ40gMWxjkei2pmydS7QH3bamOffjWMnlbVyZNXNH1eSZEAQ9iKd9j+uOjPa8/FAh+Yo/Rz7ASgv+lSj3ULFXpBEGSR2kFHOaNdBeodP64UKqr8VuwLc2T/0z9p+tLv7tLAQSIlGA6STDk8vReY6DlRuqsCpSMszbN86S+elA0xuxsE7cMqNbf9/wnCfdeaIvQV7wDkta+eKlWN45rlB+0HzY4tV1XPZwCOwVUyrVV/7Rq3y+utRoWlnwRpE9S9+6lwTqVTpJCjRU/Sq+iSRL0+NuZIkWABlhx4KcmL4gGDJj+rBjS9iq08jqOfKPtNiRzJD7aoOHckL0VZeLiElAtnASnadzGZy3/ioNrfE8NfbODFDWWjz1b8fPMxlXH0yMVFNoDm3L1EFZiI3TBN7MOBWt3IJDioyMK9rMtF5OztrsFC2a/Zhe1aD1A60XpO0fDiEn6Zz6K/y5/ncBtBmbAF3jTYgMwRbcME3Dj+jQnsWN0BFD+luSd9O6RBcXn0ALLdjdB92yJQA8P+jj+f+QF0Y8ARHdAwxQDAisZnbnTwvkLI5w3jwRDLgl7zTari0jyK9gkccNObcSeGmohZ1Ry15TlfPb8Resh1Wf0oM6W3t0BzqSt0iCu50Gb2btqFH2ONVn7vPS+VNkHO5KmeBC0Rq6PfeCkHEvqRKJv9QVY3EQLsJVYF0HLMrUZlIN+dwBxe9UWw6L/Xlujp1+H6BUknvLsVzLmqKviNo+7yA4tWlbbB57RO5Itta0GXD5YKHgpiva8sufXzghVEMDuxihYtw/J/wJgsW5NI0mx0/czrmHb2rP8+rjoEvYMsy3qp+WXElmMu/C3aDt1FbPQbAQoVRZQsagXFuBIS5Zhl88KMKJkmsUX5jUYTMsRui/9956WAl+VEvXQ38/iiLxL23oCs6xJvrWZ5UjWJ4T8OfoiChcHRLOkmQb6cM2KyPIKXS8/Y13+RHBIRcS4gxFJaBV1aFaUb4INugvuKoTuIcRDL/Vj5dogt7eQGaZQUpeN7zNaXPnXDtDzObsewqiolcYMkQREbELd/u3n+wPh0vR9+GmEn+ih4AMt/obKYHZNMxjdL+jgJCgt3vCaCpiuE30M=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="DL">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="JFK" DepartureDate="2019-10-28T15:10:00" ArrivalDate="2019-10-28T18:03:00" OperatingAirline="DL" MarquetingAirline="DL" FlightNumber="2634" JourneyDuration="P0DT11H45M0S" Class="K" Cabin="Y" AirplaneType="321" FareBasis="KN1V01M1" />
                                    <Segment DepartureAirport="JFK" ArrivalAirport="MAD" DepartureDate="2019-10-28T19:30:00" ArrivalDate="2019-10-29T07:55:00" OperatingAirline="DL" MarquetingAirline="DL" FlightNumber="126" JourneyDuration="P0DT11H45M0S" Class="K" Cabin="Y" AirplaneType="76W" FareBasis="KN1V01M1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="2079.85" Nett="2079.85">
                                    <Service Amount="1897" />
                                    <ServiceTaxes Included="false" Amount="182.85" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-03</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="42" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG7CsBr2cKoVuN/bS54g688QluxWxXUBlIiBkNc6dUxZKQL5rFw1NI2SDAyOUD3nlVO3EqA5sVzA5Q4d1dlakuFFZMo4aRl5hxQLPFe43ANeh+8mJ/Inb7N96hEAklpNHJgsrjh2gA7A24ucHHIGt7YQrAgjk2SrpKRaJExgY2wOg3IZIWsgfM7ppY5SwYIi/9S27G9Gg4B6bBBwHArce6PaPjUbmmU5ENzDtBNlgPt+IK4eHaBog+1QOHLpH1BFMFZruVQlC4tRd/Sh6rvM/GFzNfBjdpH2pliHlzxZ6O9waMIB7v1YfOdCVT5YnSGnyt6NFpzbfumB5QgQECWGPLx+6TuHtAn8EGbEfeslWvFyZP6taoAZd4IvvoJ+hvga5RwUV4/YAzBQw7XNChlY8MFRcSdyzy1OvFzDy6yCnHtsG+umXNc5iCQM21Iu0YAm/2AxUSPeRh1qarolMA6c2dM2BwujZz41kZQsYDzYgyiLIaNrUTaP6fDuQgSUsnxrkAklZtMBD6+dZnZJct2eO8DmUBZc02qwqfBoZY2kdgoCTsYpYE2RUyjLf6SUqzxsRAqX4KhFWRjCTXlzOIb9EaaCynFz4fTa4BGPD7gYxz3nhCqINsyxqFOOiSfcxAow6nZvY43dsLrYjO1LDc3xtohs9wX6wQkvjzbpnjimJFk8amu0uSgqZj1gMDLpkJepzBCD1hDHkG2NGuyJ081OCf3q/arZgI8uDmyfrNuHCPZhvG8UH4HBPw9OkqInWY5FkT1X7D0YkzFlVyTz8GeRZQZ43jfhnEMKk1RlFVN3s17WxR9vhj5oBcr5YftYRnFE8zoWH4vQX64a0EdK2E3F0ZNUjIsIOnwrFew4iro/u/AG+FX3DVi5mEHlZrlsx6IoGBQvDBHWQU7/lNIIAqPVcGGla0X3jnKSWM+0cA/xxYTbdS7HbpQiMI8vrfNrwmnkhD0PvlqNNYH2Ny/UimbyXvCLofR02XLUXKoCz24R6UWSCJNW3Qkh616Wut/kQaisimTZJIrYKG5kmBgYir1bwgaMvUs2YBeZweHfc+Trz0U0B08jWhWjVRLRiaoXd8o1rijo+sq2Xp0vfSWA/8AA87dY3cHbtksPv4MqYw+k9Nu9GIC8gnXg+lUdL3TVFuoRIDYcG6Bq5DNrK1K1iNsg1s8//oC+QKHwKOhNI3QJhkZTGTto8kebDY6QqK7eQNs13kj/4CYqoPqt4n58qe4TaO5wBaldibMKPDNmcHSvFBeGJI=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AF">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="JFK" DepartureDate="2019-10-28T15:10:00" ArrivalDate="2019-10-28T18:03:00" OperatingAirline="DL" MarquetingAirline="KL" FlightNumber="5157" JourneyDuration="P0DT11H45M0S" Class="L" Cabin="Y" AirplaneType="321" FareBasis="LN1V01M1" />
                                    <Segment DepartureAirport="JFK" ArrivalAirport="MAD" DepartureDate="2019-10-28T19:30:00" ArrivalDate="2019-10-29T07:55:00" OperatingAirline="DL" MarquetingAirline="KL" FlightNumber="6126" JourneyDuration="P0DT11H45M0S" Class="L" Cabin="Y" AirplaneType="76W" FareBasis="LN1V01M1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="2092.42" Nett="2092.42">
                                    <Service Amount="1897" />
                                    <ServiceTaxes Included="false" Amount="195.42" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-03</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="43" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG7CsBr2cKoVuN/bS54g688QluxWxXUBlIiBkNc6dUxZKThBrihHylvIxkihHO96Dz54ASUXXgjKLhAkMgXhcFO8gPwo12VyN4Jxg+eCZBaNwVRfBWGZcSuA2vSHxlzUoKdfLljmFAYQbSpNemVgUR9x/nKOffIleviYZd94lBhM108r2cA3RjOVGMbZ7jYkgUsbS4L7Iwuu8/c8Ni0FnCCD/2VQbm38ILxJ4qtIqQrMO2Vwo68l85OnvKclUXiayqDdwvpPOP/ZgYVqmpoNW6ySEgYivQC4pSB4qAXx0jNwKrX9qxRmhY9xDcjmlMGpo/GxySAtSKCXTQFC+Pq2IYcVnwHrBdcvPGSw7kfy5x/3Hw0P5xKVVGSzP3EkQRX0BHMoJy+O0kQhSEHYGGr28HTQBDx58WIyfF0v2fXkf0ehAp7G8G7lvFGj5qK7q4rdoD/u/cR/LE+HMEXudXsoIhEHwgSkg3gNQJZRKT2wVk/qjb8fb9ArFcIrJZSrE0ikZGHiN4yF+fpU2pU/v9XEUB40AFSCF6BOtob5kEcsTvvA0UTYeYzBKBWWMN2HP3SZqmlBkdyaVQF5IHfXyv4m/kkdNztlwoaZ79iKRCI/Nblr7sAv1QV+PQLa/6EC1Y7iDGZKtG0TnYN5tr3aBARkvYlayat0cwkrfFp1fvfdDpy7TjEWmah6fYcIG3hMNio6sj2caNyPz2i3pke/yOr7zgD29WJ7mbW9vtu0BGnZ3UYy5n4dqFUrrtY1ryiOuqg3SPp7pEXnPkqHKwUIMyq0zUy9I9LjaDEAAWEZZpnbB2iAdPN25c/WMWl9aWicbOypThfIxDnED4A6W0St9ECZh+S17bPwOvjSBb1ngXEIlHUjWImuownFnNss2Q6XTYe4ptZRu+SDRSz7u6DegY0OWnc94SXl0hfFqHvlfJUX0ndbA/K0oHCFEM5rc5/mOLf5al6M5OJJv+ouynvmFjvBBjlTZyqV6dfonHtUmciJGRhgopOwShxTpHqIyD/0vwJACKO1hg2GHBPA+sR6L5xIpaoCQRBvuP7PpwwElliDXh+Xgq8EU/1CoEbQapuWF2cG38NDqCURd+OLMCS61Hi9zrzhWQmSG+GR1mLhTIOSidpD3R5yAU+LhCw/9xEOXTRJnZWw1eTxWDaHiX8KsAQ0lgNw8/erOIIPMkQ+CmEgpnEbgS8M1xXc38IGzQB2OWgXkiaE3nvAmwsYbcjFFYMflUS40TyYx1Aa0Mgt8yFsErBQrM=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AF">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="ATL" DepartureDate="2019-10-28T15:15:00" ArrivalDate="2019-10-28T17:00:00" OperatingAirline="DL" MarquetingAirline="DL" FlightNumber="897" JourneyDuration="P0DT12H15M0S" Class="K" Cabin="Y" AirplaneType="757" FareBasis="LN1V01M1" />
                                    <Segment DepartureAirport="ATL" ArrivalAirport="MAD" DepartureDate="2019-10-28T19:05:00" ArrivalDate="2019-10-29T08:30:00" OperatingAirline="DL" MarquetingAirline="AF" FlightNumber="3627" JourneyDuration="P0DT12H15M0S" Class="L" Cabin="Y" AirplaneType="764" FareBasis="LN1V01M1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="2092.42" Nett="2092.42">
                                    <Service Amount="1897" />
                                    <ServiceTaxes Included="false" Amount="195.42" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-03</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="44" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG7CsBr2cKoVuN/bS54g688QluxWxXUBlIiBkNc6dUxZKTdFZ3omKV7MlyvkqDilF2yr9dx6xr2WKSlBtX21D9yFkPhIdXF3gcqDGweMcunuOlyKPrbg8x36qRGbA35VURaeumQWalkRNyuSxUjZJelTO0xbKR3FwDoBYgIcZR07CR84SQ5HFUsXImB0cLmWuQqsswm1WdOKJ04fYWkUV/tcp9ZZamX/N3qiHUU77FpQOI3vpwRjcCwjI1mPzYzyj6y4ElxktdyHV4xW9yfykdGyfFjdBh4+xQpI3o/jzV02U/vh9WsX+Sh5GPtRTQkmvkcVGliq3m37Oz7afek3JotMmU0qnL8bdxfVgIYsx7Yy3GXDoPLdJBz/C2OP8Plhr+dlaF2nJvX77Vz+YZm9uBq96OjvfINNdl4qBwHUYV4AELBkjTdCuiwiWBBjAu9Vgwkg8aWAwjZBVvWBbcUcSPa+qUMUMdsRWfP545SkjE3m4FNcokS8ARa+dE7sTPP1RdJBlbBH/kKePam9ZgJ4GCtRT3bOQhHVSvmYGcoWBOzpDOU+mLfrIzqmvBPeCOVQGtvw3QB6y76XsplvCWi+/9PZ/90qtX0BPiWvM3PimHlxBq7vFsS8wSYR4it7J+U6yfCXmqoU2i7tH73a/xrpmFingCd0EkI5MBezMgtFXUA1pmFzC0LzyXZgjsufmA8HJD75D92e4lJSImpsZ9vioRuCtV6Hitn4kxYgcuVK3ulnKCyZFGEgKqtOUvzhqXsVGhxu8XHYu/NL1ZC8XdeCiTzXNEWD52iR/393SF26PPbwUA6BzDtMy2OcLkL/rnZR8gLB2fO09Jxxbx8FU7kbhThW/3cP5EZqtX6FrvHT+b4cNGDYTALaXGuONJhOd91Iz36/1Dg6+/piKjg3waVPKrHuKCfRVLjdiltROyUh4fYfun47XkFR+VaGt50nBio1ylKL/2I23I71IUzeYmShm9XzWi+UYGlPvpmOiGf2bIC9gAZ/cOm5WwOvgh3ubUVHhWRkFD04lWvSq7VvNC+HRzSPCyO8H6o9X9xwffkm2Fm6ZeqMfltUF//tzygNZKMWdbS5WmNHiIXHp0uXXGTzu9ltxqFCTJNj9Z/wD3+LCE6O+ANNat6N2k5013qO3inl7yPVE4etNNqgn/d1nIMNIkYgByR6xbKk7v+d2lC87/LOCllNAQzIJ8XW6fXqJ9dE8KHunMTwCvfru9lP5PsfFHvxbEHCuv95IODy64FF5XaU+k=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AF">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="JFK" DepartureDate="2019-10-28T15:10:00" ArrivalDate="2019-10-28T18:03:00" OperatingAirline="DL" MarquetingAirline="AF" FlightNumber="2985" JourneyDuration="P0DT12H45M0S" Class="L" Cabin="Y" AirplaneType="321" FareBasis="LN1V01M1" />
                                    <Segment DepartureAirport="JFK" ArrivalAirport="MAD" DepartureDate="2019-10-28T20:30:00" ArrivalDate="2019-10-29T08:55:00" OperatingAirline="DL" MarquetingAirline="AF" FlightNumber="3679" JourneyDuration="P0DT12H45M0S" Class="L" Cabin="Y" AirplaneType="76W" FareBasis="LN1V01M1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="2092.42" Nett="2092.42">
                                    <Service Amount="1897" />
                                    <ServiceTaxes Included="false" Amount="195.42" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-03</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="6" Number="45" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG7IJhb4xE863hFSEWKcCYFiokFVwCYorgiTakCEhAiv7YHEMzR2RIRLtfNr/IWX3aMY/hCZ7JVlEwCZ8iTyrPVCNQI/tOZEBwfX9OZz62H07EL+7KV2vVUtthwXp1AIohnkWT0cItlQrftuOZYGMh8mVoHwYJiG18yoG8IT+4uuZM7FK8Dn1U97DHQhrc/SBDPEoYXTUnrMv/K74uhNwEEMMXUOftoWoZyI8Q0/Lfqs727+Wx3CBzW/NmxrWbQmVWO59cD8I0b4WPCQq7aEBq1UPgA8quYFKkt3+ewHHEZcRV3rZoSyi4A86Ohp1BlBZvsNREwijO64ZAzeobVWwwHNUxdHsbHg1DcbFI84zZtnFd42ZiVJvieEVWDrEzl/44kjB6QuP5L44/4GaKQA2gND/QkFCCidMBAH8fr/mntZvYK2fcOhBr1M0TZgcNOshIMsyFB0JSU2gyF74l2a3ItcXg52TSRoDPTPKWeCW5b3eNczBK59IzOxgcWth/c4edKyf19xtcYJ1AlMXApEVJkm3samTXaf13EG6r723LiijcVIqIRPnCtHgFd5eMG/FpD3F42EysTQ0cO74Vqxoc2Z01iaepIoNWYS9E3WKUgTs2tzgxeW0AWOi4qMo5DMsWFQ/pXta/9Gukdu6rz2/ZqKzMLNUwQNzIt0O19nBAjDonlTNkiHretA+CbxwwO5XOKmvxKw/9ejqtQzrgk5dmNl5U2qnOghD/S/pY0YrJozAAoln/YLbuzzCHidoPXx6tKk0IBJB1BBrg891U2hIM6K+EXWUl1uwA+w92XuDazpsNK/S8ozzGY0FJCjpu1kxa2OR5VSf4euwAqOyXJ36wAudRWYtF6d9gkwL/V1n9fRAbndp6jJzzYfg3kRXBtGqg93f4Kq3GS33ZVJhealrGhis08QYLXlWJ66WBofvcweLfTKUPSMX2RkXpANgMg/3AqLXNiBnb01iY2v+jzD8q01ZzinXzFA+2GAkAH2QgqyGoQogxcvDuB9Q5FbWYhb5+Jf9xjjHlOAO/v6HH1+uccKex1tVMH4hy6kqUK9RzrYt/JTaiDVhijRQFKvYRzNT2R28SUm9qx82U0R16SWcvXamp5T0QwtKxs3HF1d54WfOulhGVK9qhPq/HdYFgSsXA0ybj4GkdhGRm2ORfY8VFjmOHJXLblqo1NxEh/58oOiq8kp+mypgbjz9Qov1z+CHyahjEYxrNvhcCslYAN0G12bgN5R/gXok3QwAeHhbPJyVY=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="LH">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="EWR" DepartureDate="2019-10-28T17:28:00" ArrivalDate="2019-10-28T20:11:00" OperatingAirline="UA" MarquetingAirline="UA" FlightNumber="2378" JourneyDuration="P0DT10H57M0S" Class="B" Cabin="Y" AirplaneType="739" FareBasis="BN400RCE" />
                                    <Segment DepartureAirport="EWR" ArrivalAirport="MAD" DepartureDate="2019-10-28T21:15:00" ArrivalDate="2019-10-29T09:25:00" OperatingAirline="UA" MarquetingAirline="LH" FlightNumber="7970" JourneyDuration="P0DT10H57M0S" Class="B" Cabin="Y" AirplaneType="763" FareBasis="BN400RCE" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="2095.56" Nett="2095.56">
                                    <Service Amount="1897" />
                                    <ServiceTaxes Included="false" Amount="198.56" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-03</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="6" Number="46" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG7IJhb4xE863hFSEWKcCYFiokFVwCYorgiTakCEhAiv7YkGymrOurza7KCPOoQ7O3RSyNWjPkRSddRL++rGNSjsKO3z89tnIftQCFQ7frKlKP+AMMccC/pKEgerKo0t7UxHFRhoTS/360d6E7ooz4pdpuSqHn+jK5O2mY3LfLyLmnH1Y/PLqfO7QgIbPI+hVTxerMqCp0/+cJ8US6azxFGOhCA/c1mIoA9QD2XW6TiGVbz3nHRt7v+RDTeS3g3sZZ3BNuE1W6t9D+d0mpqs0EJs5r1CbrYI73GncJ4PJ70t6pwZ4p9uVPd19L3fCEB6I+YatdBoBEexMq3U2mf0MbgimRbQVQtIs0GvplQTLtnilJD97Uz16ZqWCGl0WF7f3y8JVR54568A7V427bWTMd2cu0ZZGu7eZCSRIHqYBVo9+oXhvb5VLTFJ9K7QlFBCMPIj5tsear0qEK0Ss5HMzCs3xigmZwMP+WvHk5/TPGAOt/PGNaGWqlkTWZVfKQ/c1XbY8fNfVH8EiO8TDeDtoNmQXu2Igi0rXWfxSCbQQJhsxHfwuGMCvNw46lVlpskCaXBXKukOWrrEQVqS+TNh2sBLvX4aNSK26zhext4IaglQeZjfzCekOpGQWAiUvP3hHz4NQetQsqVH5WGx7CN6BIb3raXq+8XG0ElAGk1N5jPqCksHoOXV6vOvuu0x8UAfsQ4tVd6u3E5q8HwLZhIkvUl8wRj1O6tjN1U+0RUGptL3+8j3mEtmxNjQxzjV3uibAI2ovuJ/Jiz9JLx+9OMDWT+WN9l6lUOX8VdN2IXy6szjDLzca72zzUBV+sP2BLIe3egZTtEkSkIu8W9JOGWv1uvZEzmTPcfi36uNErXDisgKAWGTHpXzkY1BY++XshE/IoIVjPmxcGx3Jcy6XuMTsCs8qf/hm+KOD1Wdk8DKxo8ep+gq8HGSottZZYPOY8vcpVXx5iRYu1t6+5CgQZcvYG22oLTaMpwkEmmKRgsSd9/71LKInIrbvyvNY0PtzkE2FqM2ksvUPvN4vRX7lEwSdCKrq6U+MKd/3MUfJ9xj6Jd3qmPZOFcRksr1AmVqtKvsgKBDzN3Lr2IMo+ysKDsltA4IWSC2CnYJ/KgC59EmhHZTVLwP0z/w/AKPcnfR2oLRNkuBIT6o0PtkCBKEkd/YWMjQ1rR0ZWpyFkGlyVv+FEwXTCEsEbrEX8eNYzXGSzHKGdomQqLiS3SGsb3gjTvbJJEZZxPpk2lq1ij6hM39jAA/pQ=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="LH">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="EWR" DepartureDate="2019-10-28T15:10:00" ArrivalDate="2019-10-28T18:00:00" OperatingAirline="UA" MarquetingAirline="LH" FlightNumber="8746" JourneyDuration="P0DT13H15M0S" Class="B" Cabin="Y" AirplaneType="739" FareBasis="BN400RCE" />
                                    <Segment DepartureAirport="EWR" ArrivalAirport="MAD" DepartureDate="2019-10-28T21:15:00" ArrivalDate="2019-10-29T09:25:00" OperatingAirline="UA" MarquetingAirline="LH" FlightNumber="7970" JourneyDuration="P0DT13H15M0S" Class="B" Cabin="Y" AirplaneType="763" FareBasis="BN400RCE" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="2095.56" Nett="2095.56">
                                    <Service Amount="1897" />
                                    <ServiceTaxes Included="false" Amount="198.56" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-03</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="47" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG7ru7QRjBHa4uBTw5fGfrHbzcAsr1HC6I7pTJ3XOge/b+19SJ95UdQt6KoK3VkzR93koGjjxyAi1ParfJzUb8EJ0uHIkvhK5rpPunCSotoOEHGECRWWA87/g6J6zIh/RNSjnEv58eg1FXlFX8iSAVaXJvGCa/xaIA1/GUgdZ/Y7b9jwkucfd9dajsdRmXXd4MW7Xu+2AwxhhI/mX8apxLByiksAponOr5qoYyqGiHX8V4vf7EIHiMwVJMlXkbM9JK4vSEmWa9gQhiRiyq9PbALC8l7re9S+tB4sHYBXX09VvfwqYTQ1J3+zSYNnEyKHU5xS27SK1gwlJy7q5LZP3xcKxUww5OrYksoYkz08efEBGtBrWM87BaeLVu6zV+FzAlkgA9xWIOGs5Oryl5H+zfBO69HuzMLeaY8WtCzTLG7lgyyFO97XAVL/Q/5WuWACk1fIjXmFcmxGwXVXHBsBLpCuyuak3rOnVQNaJGrkOfOO/yyhUlcLa9SBKHUaHMEyPE13Elf17fZEP5jAIkVMZKx8tdBGH40C4gILvDZ1q4SDavjABmqjAg4aykciOpKyxaOFCi3iMgiaJo2HxT5/o28CdwZ+druabKLelzCyMZSU/BcFc2PAuYAiUFDJFDwuU7gC/fIpmyViJuodCRxrOyoZ5lgTsAB2mt31bUFV9S0ukPrfoUbE8yHaEOT7q+QZRTSoowvvTMkWICX7H9jFHTcgQZJIGEBkNlaP/IT8wSJJSfR3ktavjsWWyjiF3PkS0E0BZTjpUgOmtb0fP719onkDjKkEVKWCMw63OP+CKu69EInDKpZRRP0JbH+hJute3WsjrMcdITjYWqHB6Jf73SS4p2kiT6K34BnHwC+f+h3DdgOSNugPOjv4n+A9o9fJTx71MNSoa4jug9ow/hvh8bC0x6MamItJHv1DtB4LstdtWcEzeTCdQiNz2nUp4ajfAH8QtlOu1+rgiJN/BQpFwvMIpZ7a3QdndA5uoFsXbIFKIkFOUc7sFq5adssFzQryV5Uv6EbkQD4Fg8jrWMnmJ+YteZz5/4QX2jTop2ZNeTTSN/3iHanJLfWag+7nqGbn/A6fFGawcB3HQYuidvAtDr4/JOZrjKV6Uer3Xlbm9VoTX+5qxDL5yYW82ICdjsAV+oErTLQTxmXOvKkdWMbfoePZTRt65831uAe/cANvlhGPUPoYC53jr6kJlacKrJHNwJ8tDXeLjcX3EcGfrbDJvAIYcO/ujFvOSrCw4Onha/WSdEK1bqH7QIyOWxURb2kJfZe1KfDph3Ky6cDG91acRVR5oAT5pvM0m+vPBK1u3dIb1L19IeXkdtgrGn0Mivmx640k35giFutP21V8iDb4lQA/xkNHGvGpLO1xoYLpBqFROdsKXAts4RZRmKHZ4h8d/heUiYgZF9VSQ0ez7iN/nmZWrArmxw6w3cJT4XRNz2llaBlyP4RUtJTa+mPvixLQ4MIcRTL2rIvQNuwo89n4EszkmEVB+aa/CD1Wi8/a7sgVaq93qOsYn+9t3he43tq0PApM0wOkfYFtuCYA+qCL+o+mDVSFm62fPpOUY4lTNbx/uo=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="LX">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="ORD" DepartureDate="2019-10-28T16:29:00" ArrivalDate="2019-10-28T18:30:00" OperatingAirline="UA" MarquetingAirline="LX" FlightNumber="3251" JourneyDuration="P0DT17H11M0S" Class="B" Cabin="Y" AirplaneType="739" FareBasis="BN400RCE" />
                                    <Segment DepartureAirport="ORD" ArrivalAirport="ZRH" DepartureDate="2019-10-28T20:20:00" ArrivalDate="2019-10-29T11:00:00" OperatingAirline="LX" MarquetingAirline="LX" FlightNumber="9" JourneyDuration="P0DT17H11M0S" Class="B" Cabin="Y" AirplaneType="333" FareBasis="BN400RCE" />
                                    <Segment DepartureAirport="ZRH" ArrivalAirport="MAD" DepartureDate="2019-10-29T12:20:00" ArrivalDate="2019-10-29T14:40:00" OperatingAirline="LX" MarquetingAirline="LX" FlightNumber="2026" JourneyDuration="P0DT17H11M0S" Class="B" Cabin="Y" AirplaneType="CS3" FareBasis="BN400RCE" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="2110.1" Nett="2110.1">
                                    <Service Amount="1897" />
                                    <ServiceTaxes Included="false" Amount="213.1" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-03</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="7" Number="48" Direction="Inbound" LowCost="false" RatePlanCode="Ffa1q3POCcyi2Rus2m2aUvvI4k+C7do73FaJXFWc2Tn8TLb19ihjxJbaX3ShvttdealO69uFcb5CIcjoaHDX9H0kfpXWM0c1VXp6bdeLPxizdWD1XpMvW1h2T3J50eSaNajmng1j6czOIwI2GEaF0qL9zJkkvgClAEEREjQr60Xd0O06d8xq4VtDC5hqDZROSOakTceMs2rqHWqyy3PrVBqgT7Z/UHVgjWYxpy7PUwVc005x4nW4e7IWFjEAiNm1MyHKgcEBarJQGGE0vyW1McpCWf3R+AFt2JP8wdPGjD4GHbk3yFy4n+V3/MP7x4wGAQTQfJNBS5VjgutSg0D1pLBiUyaM6v7p7QIZW5MK7K6HpzV+Ol7mCoxRVtM0nwqHt0XdSCmywd2KsPvCnEewXcaB7zu53XiN0sLLEhIouk0J4sOSul+siL3tzkbQmPDJDCR/+nmSf77DJ+8q4x5Q50/e7r+0C0LSzU26d5V4wZegkUhnSZbLGzm1GC9/8SvdPOBBN6V5RU2SZt4V8IZFBggLl8RGZK6JoX8irySahESOd3w/XnOcXRoV/ovM1VEP18q8Sm+JvworQivNpCOkJVc1qNefDM9V1o2xlyCadGCqamvINO2iNLlp7wDrDOUt8zNgKe9ncUAnWFzE4qAP3uBzmFgOgtwakw/oYjyt14mCjqyQoOYHpthUPEpPSSiohmXa/0mMxIrvaQr1f5rVpuWUe8ZqqwusYN/bV6jJCIih8MpBx/dWZuY1KVOZx8KbXSFqOw9hqNCQ7fVYrm6EwRaatlsFxZQnCQnTAeFFZDvdqQF5mgRGZZF4vlJQHd5BMSl6el37ZeHEv3p67n63zlHOAuw1Yg55uZtvrMOC0oVQwypurlikDh62H8c2nRJJUDHRYWhzpFRruZBCjT2daKezQnaEimS9Qx3mIycy5AjgCu0WH9MRvBwZeLCUeVSdxm/Dyl50Xb2e80yQNWN/F1LQlM59PASd+P4vXCcpwuwtoKGGz8JdbzIFTEiIxzvUs7xmF4EfoDFF2QiNPjenvd4d5AVIvs/JhQXTqU4adF96mIB6+jG5Vi9a6dzYXuln9P48vqVm5o/SsfJPootXQ0bwySE/UUg4dmlaw/35RBECnHrgLKmI/f8Dt0LAQvgPY/9VRHU7xSqfbXT/K/MSi6TQemGWDwAYfuqhaZAdzz3DXKByL/MmBRDWjX/jNhMxKgfdjgSPCVReIDma+IphgYlJjhwrZ4/gWezTPHZ81WRia9bYx0qgGJZKnreMRsR2W+Ou3SFs1RiOe+WtwcFeQ2DnM+PhFUi/WE2XcDxewV8=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AM">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="MEX" DepartureDate="2019-10-28T23:00:00" ArrivalDate="2019-10-29T05:00:00" OperatingAirline="AM" MarquetingAirline="AM" FlightNumber="22" JourneyDuration="P0DT20H25M0S" Class="H" Cabin="Y" AirplaneType="789" FareBasis="HLNN0XCB" />
                                    <Segment DepartureAirport="MEX" ArrivalAirport="MCO" DepartureDate="2019-10-29T09:00:00" ArrivalDate="2019-10-29T14:25:00" OperatingAirline="AM" MarquetingAirline="AM" FlightNumber="434" JourneyDuration="P0DT20H25M0S" Class="H" Cabin="Y" AirplaneType="737" FareBasis="HLNN0XCB" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="2296.06" Nett="2296.06">
                                    <Service Amount="2238" />
                                    <ServiceTaxes Included="false" Amount="58.06" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-03</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="49" Direction="Inbound" LowCost="false" RatePlanCode="Ffa1q3POCcyi2Rus2m2aUvvI4k+C7do73FaJXFWc2Tn+QvDhv+mN5m0dR9RZVrSW5/Pn6VcK4dqs7soZVmY+qYgCYuhe3hx+rx5ERtew0DcaD02lud+JTLBDhUcankeIyb9ij+9n23PnWsUKZ0mf1yTdfHx4DLbut0uYO4HYzPthS85druMcz7f0De0uoQb74LRzhGPsn9XPCTeUkDU7/uk+DI+30L9HaqScV6V2RSudx2hWZ6yrlfxSXqdA/obg1OojZ01aTamS+FVbUat4Z+M8fplWyFVWSj5wSiuG07Yr9gHs/doB4Yn4OdsB7P/k5en5JSY6aBT04CZ7xK3tefJ/+Q0axhTFXeoB0B7yCzYFIMBgDGzFnuwhGJK5iIOXv9C8DUGhUv9RsMd3N3KkxV9V8xZrmWUwWnxFQe+KO0hbmX58EJ0d7hQ99YGknNHirhQuZAv/z8dIjrUccZFtUXvP2ZQPkPVHx8g7jvMHNbo1SfYtdIcyuxwe2cKR+Xu5JyUxeFD/2c4ZqwLsefKikCwZ9ck5LNNuHrMo1biSVVRWg40IdhzmZfgRndcLMIaaEEQhe33NgRWoTBt5IjWjnmoSDwTlc5kjG53UDInT6WifcfrK6seRkBM77vpoGlHwyaDnWrlOdUsx1u2jh3OBLL8Y4rWXhdkg2ST/x4Zc/BZZ0reD73MtXfL2J3zndYQ/tghrL9AuASr8LI54FxxRC0oc5HQHL6x/mhgG8KeIMh6rly6vNoPOUbs5xmbMSBmP5HG8ptt8iet9ARjiYLyJg0mka1gpl51p5TNG43ztvtunqupTHW/HqUYOYZhQh5FFBfLKtNqtfzrj8BdJjfqcmMmbkTo5sTSsOjkx7CLVTmtybNiyHH7Qpz+DHbyrhmqNWEYfysHkMOnsk0oy1EwFS0kdfBsVHnALBHb6U3p0IBnNamWvdQkq3O3H7AFOKbqpZvDixNi8d/o7IyCdsOFVUC4jGWEPDTscGyMguAbzKXSmY/PwcrsViXJdylcXev9ryQlbsPIfZln8CfwauljnNwVU5cAyFsIIWyntDk6wxhJPHjNEnmXTRLmn7eqN8XITIfRcEzJ3aAGhSfdhqOcv16NGmD/bGmKDSXWjgbiP9uSDEOYVwBxsO7/ci5fuxaPZ0HzlryvQaRcVokmFbiBREOqETe8gclzj/AGBA2MPrHB5pjRt+mFbZ+rC1WUjyV4IrMDWeHEr+34wJBUzesakXrowQ820W5oColBzqpQZY2P9/EkESQvn25aeVwlMtGH4XPKABaF2gP3NlVXsBMIsLcySWOb4Ek3vvyDNEo18o+Q=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="DL">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="ATL" DepartureDate="2019-10-28T09:40:00" ArrivalDate="2019-10-28T14:37:00" OperatingAirline="DL" MarquetingAirline="DL" FlightNumber="109" JourneyDuration="P0DT13H48M0S" Class="Y" Cabin="Y" AirplaneType="76W" FareBasis="YFFW" />
                                    <Segment DepartureAirport="ATL" ArrivalAirport="MCO" DepartureDate="2019-10-28T16:55:00" ArrivalDate="2019-10-28T18:28:00" OperatingAirline="DL" MarquetingAirline="DL" FlightNumber="1118" JourneyDuration="P0DT13H48M0S" Class="Y" Cabin="Y" AirplaneType="757" FareBasis="YFFW" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="2318.38" Nett="2318.38">
                                    <Service Amount="2120" />
                                    <ServiceTaxes Included="false" Amount="198.38" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-10-28</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="50" Direction="Inbound" LowCost="false" RatePlanCode="Ffa1q3POCcyi2Rus2m2aUvvI4k+C7do73FaJXFWc2Tn+QvDhv+mN5m0dR9RZVrSWllaCXIru/bbt/vwU091kDU+vhu9S6IfJAGDf/PC3G8XwXlRTb0Xqa/2vKqyHAYGUvu+tSnoelNulbIJkCCkpNHiYs1LmO5UAU567d1Hn7fcvwjt+IXr4b6BZfjyg+ckHM7SeWNirWui4jzsly2HTVzpN8mWDOcbsAhZZXpvdYNFBMB60R0ppIY8uFL1sF90DvuXOvKYM1Biot+fwm0blSi9tWNnCnFNO9AhfavWWmhhx3IuPLRDyQN+hm9MbAEVXwdT5QgxZOXHlMckQQa/fn9/2t5z/N1wMH6XYYoh3QGhqEiAif91fdaFqcKIMt35tFrCokEN41mK0q9LdD/cLJjjgyc05H/RQNRLESMboUazJZ5/G4EKar3G3Z33QugmHDwsgfUs2tFCYNBB53esPzlSzXSHXAWcNgOby2XsIZc+sz0b7fGWSFB0hICYcpIJX0C4BSeTh8roDSXG+UbXM7/7AYlHY06bpJeIBCjDZXPoaMCC5brd6g9E/C1I0NlMcAA3GLUI4s5zbB6Jym/GHXZdgHmfGWqySq9p0Xv2+Ha85Ck8MFcC2tu/VI+9knU4VRV0YHAETT27kaxchV4zoKj7UetZcxp6EtMD2/DXiTKmGVKEketRyuBVEwQt4LTMbX5CQsC9ZZe++Y+8I4SrGH+7i9UKlSvxORcrFYKqKpCmcInXj8aiXl+F7yvfl0fXAEQ/v05XaeR3hnyHYqjwN+N5JYKvIClW5lXp4FfXl96+MuUEswQCwYXNXFGpbq5pGZVEtmIkGLFzhHPBunSnFaaxk+zXLvMZODO3CSycCEQMVYBIzOzsf3VgXKaNG+YTRyQmO5edeZ0molsKNlwsSd0vLUExczPWZ6sdA8YEUPdEF2UNlq0cCp1bYW4cEVICEdwNVnR+x29wuqqIhZHSyZt6y1EhBVo1BvXUI8ufxoihvp4TMp6A2kpYHMUhsnIkT02T/ngRbC/Uax5REDuU5oH+ZlMj0+QB8XZXawRKMLc3J5LGd0j5qSTPJsF25qlGSLCbFlzHYbOD1dJmEcZEutPQen7HXShgqx84mo7zWBFVH+BKJ3VK+Y14k6eCTnIKgjMGASYTR+yrmLl/tgWemZ3fQHMSx0rpwT3t/8xYMl/oUwKvH50ObC8Qcdl3b316QKmWBu/m1irNlrbxbbgJLlNQx7MjKDgHWFMwN5F5J1z1aglDUD7wR1aulQ1Uf4KXQt64Ucff8RrAEvB5p0E+lGqz6FPln13uSrgwQi+ClxxU=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AF">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="ATL" DepartureDate="2019-10-28T09:40:00" ArrivalDate="2019-10-28T14:37:00" OperatingAirline="DL" MarquetingAirline="AF" FlightNumber="3626" JourneyDuration="P0DT13H48M0S" Class="Y" Cabin="Y" AirplaneType="76W" FareBasis="YFFW" />
                                    <Segment DepartureAirport="ATL" ArrivalAirport="MCO" DepartureDate="2019-10-28T16:55:00" ArrivalDate="2019-10-28T18:28:00" OperatingAirline="DL" MarquetingAirline="DL" FlightNumber="1118" JourneyDuration="P0DT13H48M0S" Class="Y" Cabin="Y" AirplaneType="757" FareBasis="YFFW" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="2330.38" Nett="2330.38">
                                    <Service Amount="2120" />
                                    <ServiceTaxes Included="false" Amount="210.38" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-10-28</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="51" Direction="Inbound" LowCost="false" RatePlanCode="Ffa1q3POCcyi2Rus2m2aUvvI4k+C7do73FaJXFWc2Tn+QvDhv+mN5m0dR9RZVrSWllaCXIru/bbt/vwU091kDU+vhu9S6IfJAGDf/PC3G8X4HaIx5qSv7jaYQcQSF/79SyfIBv/BRfD+j47AB3+ivFJf5Z91cpfTE/arMSfHK001PAD8cADKBLRZmuTVbMOIurgcZVaEPKgxACeAsVX2kFUclaYtyppjhF/B59auSt0G86hP0vVm2iMaNMStXOP1NEGdu0C7m5oTDUDdgp4TQFwAsRk59/5ewja84cpY0MB+ch6Wix5IP7ortElEdh7O4NQYtN6yPORfGL2XeBFm5S+Z+8Kv0kW5FD7Cc8VT4heZ9iNKAP5ZdMBaKRNfn7lbajrguud0vDc51fbtzaksnWb0vkcTlE0HENepkQkBj6T84XubwzKaTSqcgfOILvyAEfNr0NAujab/dobYhz+06i/WXYuI151Yk9vyyCpfj6bdpsuvBHGQFMNvhxpsaYlpqdrU56qGbZiZWtZ7TrJVgTgkBtlcj0RHJoaYsRuSmIESmv//D+KBnnCRT1vZeeBWWoKYyyTccrly2h7VNQqC0HGgOrBFN9iacAWGU9GiK3twT61OPwZkmYT259eRTpFCvTmvs/dR74KZseKYCEHHLo2VOUp0Z/INBRDVXboyyayRgXSe6p8DKkcxzjjW6pbf2Y5Z0AWWJfsT5M6i2Qgl18UHyImJyYEmBbnTzAhkVsWzsMySc0iTqmpcxu3JRWQ4sc4KHeT1c/nmi3GUr9AsIUTXA/zSI4WqIdoiHw/hFXWFVyPSZ2zsq7L3R//b5EF5ohkW2ym4o3aQy22ONXlIF8j+hHnv4BtuWNJ6QSpfG/SqTN28Md4BCNl9IdBqyht734esZD+kH6ABoGmlIVw6TkYfcn/quwyBbH7MAP+pxxW9JNyHJdf39swQQAtH3GggkH6KBaH/s6JLPJoGfZObFYpNFXJNc9fZmkadvNETKAHgMPqvFnTpD551jkOGe2+LBM9AHLp6/bNIDdI2XV+CvYiOuIlJH818k9LLI/ymmzmbjgwqQVJWBjgWB2sXkElo18qGt8WVi9oL99Urx5PAt+2f/zJ8k9x9od5w+S1vbfcTzAT41hkaLb/olDrVYSfF6YKT5O0JG4yP2XR1xOu5HTaBhAhneseyZDGlzeDtxZ+TtxbLZSEXF0Nza4j+dOZlMFzYQBz3XYxH7QjDtZwIr39DSd1IP2tYZKu2ElQ4xf7i5y+h157mFBq+LZscjk9S7ZhjmNL/ZJnKBUFTFxIn1RI1y8UETsNFebES6ng9LBU=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AF">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="JFK" DepartureDate="2019-10-28T09:15:00" ArrivalDate="2019-10-28T12:54:00" OperatingAirline="DL" MarquetingAirline="AF" FlightNumber="3668" JourneyDuration="P0DT14H32M0S" Class="Y" Cabin="Y" AirplaneType="76W" FareBasis="YFFW" />
                                    <Segment DepartureAirport="JFK" ArrivalAirport="MCO" DepartureDate="2019-10-28T15:35:00" ArrivalDate="2019-10-28T18:47:00" OperatingAirline="DL" MarquetingAirline="AF" FlightNumber="9016" JourneyDuration="P0DT14H32M0S" Class="Y" Cabin="Y" AirplaneType="321" FareBasis="YFFW" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="2330.38" Nett="2330.38">
                                    <Service Amount="2120" />
                                    <ServiceTaxes Included="false" Amount="210.38" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-10-28</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="52" Direction="Inbound" LowCost="false" RatePlanCode="Ffa1q3POCcyi2Rus2m2aUvvI4k+C7do73FaJXFWc2Tn+QvDhv+mN5m0dR9RZVrSWHDBZIN0HyDdwZErxhQ8BYH9iLGwoe60eATXhV8RYDCDe6zMWojtKurV/TsXvH8CHb9Pb/X7BFxzEOqEIfx9cvMj9rvJ5AV8mu/7oXo2IxP6CDZqqVpSozxAj5YPRa0hXkz4aZ+8oTdX9MPHQvfNn5jAFTNOxTs6furEiz5umLxEUqqikVSMjYvFSuQ/RyqrQCpodm2r/ls8x5tGAs57SBJGARJMzEx1xGfPret7QwOiS+PHOyscnKf2eYpfWlBU/RT5nfQIqPWXWmNV1gBdj37qjJmNObXdXPWLw6IXF02o85Y8gb6UT8lkNJmj/G3nfPp1KynbWp5UtitgEBeOnevx+cUwMGAfMBn3D2BBmU3gsSebrIZkAm6uHeh/yORgkjyP3q4tkRWj/wAUgOQJDHqK5jQi0DOwUr78PC38R/86NGGMUvsq/HqA6CVIPJUbXQ7xuEiYrPnwto7cb+0iaqQyJwNTu6H10elKWeSNPfaCkEw+pVb+7DjQHJ4RuIv0ocRKKtKW5MnQb/T1HbUOeT+S9N3YutC3C8mAVPqgL2e4HPL2/ezk7iHE7gGMcWmvI3Uu3kdg36iN1dyqzLj6cuDd2J/ZTuE8gSTkUpN1t0grHYYA4UP4AgQNh6RFh1DNjzSY9w/RbrPuuGQFA4FGpZQ3Am+yCHj9avgZ05D8jbsjRvIuxbt7fytflvtCQoQYTM3JlwJb0bAp4INX1H+me5rYFVyNyLLBtELOw2KZ1ssJenpDSwO7JY5RGq5YYjBYsmK6JZQ5PFQzFdHrpUu4PEpIaQaSEOjBFJx6HsZ8B5u95RYllbD6vShcrSh/jlRmGaN2X59CtC3V+4VCAaOVgj7oJitjUCGbmf3p6OQ9xkb7+F8bYGu+dc+p6iW5EvfvDzroK+ZS75OwvqsYeuXE5IuilPxHb1av7xPE/p4Yt/G2VHcedD29SeFmCOZArJF259SeTXk9JYJPiyawR2lT0x1670AMLNqWVQ9uJB3Pt11rlvhVMfe4kWeCB45kkNLUqWxb4IiaMnGjycS88vG6QFVspqLhQ3OWML+hOqPfnY+KAJy8GYUrMCwzJ6mqm/jkWEF4c/Lal6khgVMzfQq0nN7wFEUv6CDlTmEPEyQ0NQxo7xAlZRoxTSfNpC2UuUnW62aHm/fkGl+fzmRimQ3y2s98ed/qKqpRdIoRntnAclajejBGoz0rvJZZXH5pScJF5pvrQsoK8xMW/KrN1Ojb62BZG69hazbDpIsH967graK8=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="UA">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="EWR" DepartureDate="2019-10-28T11:15:00" ArrivalDate="2019-10-28T15:00:00" OperatingAirline="UA" MarquetingAirline="UA" FlightNumber="50" JourneyDuration="P0DT13H43M0S" Class="Y" Cabin="Y" AirplaneType="763" FareBasis="YFFESOWW" />
                                    <Segment DepartureAirport="EWR" ArrivalAirport="MCO" DepartureDate="2019-10-28T17:05:00" ArrivalDate="2019-10-28T19:58:00" OperatingAirline="UA" MarquetingAirline="UA" FlightNumber="434" JourneyDuration="P0DT13H43M0S" Class="Y" Cabin="Y" AirplaneType="738" FareBasis="YFFESOWW" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="2477.38" Nett="2477.38">
                                    <Service Amount="2295" />
                                    <ServiceTaxes Included="false" Amount="182.38" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-10-28</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="7" Number="53" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhnRyb7kxrpnL46R+kzNsTyxFkQPOx4/ifQHt3E5Ftomw2IAhFkxpWqGuhJmN2XUxxye/mi9ZWrYVL7E+5U4BlXuKkUXHChBNK4Gp+1L9kBEhwGdhKFVLgW37lbCjwCVH8y0hWYuQoa+REYIq1QfAvVBmj1PAoYsjKQHmZ7UBGnuygsKx0/yZUn6ll2DnlU0sGWsw+rYvcfQmgacjCf8CEj9RNPpBoB0fZLt80C3IGXMn6T/rsXgTH0nGfnyIPx3cNhhSxhCvCrytywLwx9dktdbGB9/m0nPuHPzRAHriL4qb1SpQfXSGwhWkxc+5qGFEqXMmxiuowlf4YJdbf0s5/QszrLE8+tnVmwLWTLF5naxJX+k6uNipoIs193W2zDG1CM6Ka1lYHTnVD6MWBVwsHfEhi5n+QLX7ny/EYk6SolexqHcBmaUixiDYKDyg77xZWv7DI+0qL1OuMaQsOZV/W2zZwM3D2xAL00AmIuVl2BFfW+icdrioopk2TfsCgFADO1krg1RGK1XOqP5eoh/ggej4m5cUDbH6KWxnBdENkHALYsFeWJzVHJc2hJtIlIqjjbpG4DDFHh6jbF93sxi847yPQyv2YNhwBy3Er+YbUxZSNCiL5YtN9HTQaJPruLXu49d0qNeQNC1LI/AZ8UHLwsDK+pvEf5qfXmUy25XVe295FWbypXqli4Qi8ll8ha2VPX7bF4TOEWB4sAP3OkwrWXs0Awg+Vc8TNynF1ZkQCHkBcyxY5VFMN+QQITCqIguWIKhUKCOq0lTESi3HTEmVnofxrJGVsvTXxKH9q9cD6BeQQitc8lnbzttCmOdt10bZkKIQ3DpTNM376TUmcnSunmBtHBq+hEUsbhbuDtv3rbAN8h5jwxoKl0JP9rQJ0PhFmeRYQfI9NT5SA6ZJx7FzkxouQ9ouRgOWGRtHzKu0pWxjxkGldNoApWa2Jq9K7APoO109n/u6Vd+MuISB0MvXq1AeMxIMUEbspWYepr3Bj6Wb1d93iHtK3l6z+8KyNho9NhQAZVsgihj05hF5eHZlH0gHg8tFhPCG2/2mzxtZMeO/jGIVp1MuZYq2sBan22Hmiv7crjjaV1P5S+u7Is3K/PEd4qB9RXnoEE1LrJxDVT8Q8Dk/gEmQAQH7lyW/XoPj5dq4ZEd/J31SnKSDWVeZxbiCpFrkvnd2E2yEvEYrWgBDg6qPRfA16zTtFBI0wrNgbv8g2fl7YM7Zm1AG5w1l+fHhWQhhlGqAsh2B1LUhMKJ0xnRGCqlVKgFbSKSaIPG56o=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AA">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="MIA" DepartureDate="2019-10-28T19:35:00" ArrivalDate="2019-10-28T20:46:00" OperatingAirline="AA" MarquetingAirline="AA" FlightNumber="1194" JourneyDuration="P0DT11H45M0S" Class="Y" Cabin="Y" AirplaneType="738" FareBasis="Y1N0C9M1" />
                                    <Segment DepartureAirport="MIA" ArrivalAirport="MAD" DepartureDate="2019-10-28T22:55:00" ArrivalDate="2019-10-29T12:20:00" OperatingAirline="IB" MarquetingAirline="AA" FlightNumber="8636" JourneyDuration="P0DT11H45M0S" Class="Y" Cabin="Y" AirplaneType="330" FareBasis="Y1N0C9M1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="2802.85" Nett="2802.85">
                                    <Service Amount="2620" />
                                    <ServiceTaxes Included="false" Amount="182.85" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-28</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="7" Number="54" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhnRyb7kxrpnL46R+kzNsTyxz4cyLBcxXGsBQjjRqrM/PiTlZQpieCOT1p678qA5Q/3gmzLENd8Zr2a1Iuzejbo7eWDWpp0tC7uD4HHCuc5iGYT0GUZwjgH0IX+jDpF365wqw+E8EAoGPeUZ5h9IngzuiYxG2CRAB3+3/IeqaMH3ptxsSQ/dR9wZujvCwFXv0dYRkaFvNNSvOt2YIhd9R2BcpZyG67ezowugGUFXd8MmWwVRj+D4YPMzinDHXJ3ygVa1EEvu9j6eLOqDw5K4wTCxqZ3m6SXr3dAixEG21ZhT0H1bpO3UDkWC76F+pXeH0jcIVuip9iy5hSyg+/4OplyRivPzk1bDICANY3vu8j6fOIOSW7afSNKnqOgsiPwRudOLjpc0ZD3nsgJS0yk0InkTTKw/gUsQSP/iAZFEtslKHMIWfgbw5r49+n8MJIy0MdDq50Jo4qKvKIydYDCUf/XdJWTWFKxxsU9AIzCl3Ctyqezv5itg1fmotcCboMsOg6hUfR/QtkWuIkBtlwxBzACbXlncHwu2vRaXxM4pj9+J9yVkBcwhG3u0a57hTXWVQe8am9IMAKgHjq9tGOpebCBKwma07loQvbxH+f36Yg1NVPg8mpN+WtyCkYDvNSqXV2dTxhoA21D8vLNH6rmyTsq8Cp6H5DsDw/WfTCcXC2slobEp3IcvYM0hpAujKyeXtvYCBa5qjYh2WwhEQDyLsmFm/gq/1fJx7mXFzxl3Boz3PmeafQK2j5KWkQsiAIrKGAHvbsKr7IW6VFfGm90V0itjNP0O3noicymCi+kaVpZeF/1llE8SEv6Mj6DNxtXhr5N7EJmOSooPR4BZwutNzs9WHpP5DZa1fg2yGyp+phFOW1JBPWT0icEKYPmBIz6dfxpVD/74E87uiVTCRMoIowJySB4sVaywyGJCTQCw2XtV1vg62RsIGNpFQYkYWvAIURNxmTc1hLyB1eAr94IOUZYHcOFAOMw70+1ElIZ6EhegvFw2NoYXX2JQ6QnDvkQjyG7+lAPXK5nTuLKlx20kPjQ7EvkbzZqL0G+rNftgrIDFVky3i+g8cPMjWhtjjWANm7V2koZpMVA7VOK50n8RtTA7q5Lv0tpGfjbbFM8djAxUmViGGQZxA4QXJYAAux/cIW/K7uclK9bUfnebXv48UzW0iv+R9UjNuQKpVihIJefJI2d1BeWFgjC24GgAaajpBUUB9FcU3peyRQc3MAi52PWoNgnorSe9OvxNNZATcf+lSTopdbfMPo0iFeFfEDHUtSc=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="BA">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="MIA" DepartureDate="2019-10-28T19:35:00" ArrivalDate="2019-10-28T20:46:00" OperatingAirline="AA" MarquetingAirline="BA" FlightNumber="1672" JourneyDuration="P0DT11H45M0S" Class="Y" Cabin="Y" AirplaneType="738" FareBasis="Y1N0C9M1" />
                                    <Segment DepartureAirport="MIA" ArrivalAirport="MAD" DepartureDate="2019-10-28T22:55:00" ArrivalDate="2019-10-29T12:20:00" OperatingAirline="IB" MarquetingAirline="BA" FlightNumber="7260" JourneyDuration="P0DT11H45M0S" Class="Y" Cabin="Y" AirplaneType="333" FareBasis="Y1N0C9M1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="2814.85" Nett="2814.85">
                                    <Service Amount="2632" />
                                    <ServiceTaxes Included="false" Amount="182.85" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-28</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="7" Number="55" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhnRyb7kxrpnL46R+kzNsTyxz4cyLBcxXGsBQjjRqrM/PiTlZQpieCOT1p678qA5Q/0GrircJedTKKRdtslhQPjAs/demwuffuohQS0jpy9QNkkfSsk90Rd6bulVxKkmOcIRTjxtBU2xFKXrGOy1Qhz1TyKwU8UWYrEhOqZXikDzwkalrzVuhpvO18k1EA7oAg3oEnmR7gKTohfcuBtTTD02j44f+XdH4pfRZlDaI+HxyGLk6U+a9rHPdtaokukmCsbtUz45W371c6TCa859JEnn5zsGfZuyt6Rv7OER0uPj/2O1nx3RkU65Ay5BDm9/jsoGAWXVun7rLNcLLG+vXl32dHjJaoSrSdjDsSVaJ6hQLLlu9zGbnZ+f2shcPpfhUU7OpYJrrirXwn8MnZQZwCGi2/cLuFbz6WwVvIdt1u1tRUzaRJf7TUTfJJ5Al4f1UkOdrjWwqAyd9jtbPQAwALg4zfEY4q5PrenYrBy0QzzhmHdjEx4sRnLjtlHMDboh9Ndat3fJptkMx2Oh79uK+gZVA6zLNtpVyuS05vB32YsSK5dzm3X0j2Exy7Sb4OYZ12FHJhlt6SE0nvN9dANdy/CvSjwn7ijLKERsegClH/zF2IaTBhcHsGRDDvirEEeqZXdmruiQSLxof2EJ58cShHe/wx0SI66rOuWwDn5UPVCR8ZARInW/RnLqCWM7px7KMGPehS8BQf7YLVKK+5P8jFYWL6i4oJvRe9TDIt+9pB6fCKRrL5+aBGNOn+yqXqFEpvEysZnVa+3SJJtlMXH1dMUeIrvczfeLDuST9xUlGQuyhwWtlM7jF6P46DH3vVtafMmk9FgbndMf0Gt/4Cz5yOElYNhOcL1zgqM9aEgS2ox5bLMcYxw8MuySnETcZlEII0/RMUu8CCkpno3lJbFvjKr2OMx/OO5lILrAV4PurcQLxKOs4JoDIRrBaSptdNTGyxxgVqqSnz+dkG8AQwVcIlMZ3iAwigB3M+J6wezCXSMkAASdCrc908RUfMrtzHlCOhdPxT2N9gjMFqg/AQlSNNHQVaqCiFNp+JTfXYBTA/ni3qZ0i3jgdJjo8uE7Edv2cAX66EsghxjeEyjXreB4CATpbPyo4XDX4Jaq4acnIrd3P7xBwhVdMsHdYp401ewmyHpeDOQ6ZwM46vp/dkwp1l0pIRvbPaZyBQnLeeqURKu8sr6DgsS9AmsZju/U3FRo13BjBSVGgh2HTLAcC2KHFet9g1/1UkwKHCuJG21ilrrDIpQI6KPycJZJXNUffzBCGEc=" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="IB">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="ORD" DepartureDate="2019-10-28T10:25:00" ArrivalDate="2019-10-28T12:23:00" OperatingAirline="AA" MarquetingAirline="IB" FlightNumber="4103" JourneyDuration="P0DT16H20M0S" Class="Y" Cabin="Y" AirplaneType="738" FareBasis="Y1N0C9M1" />
                                    <Segment DepartureAirport="ORD" ArrivalAirport="MAD" DepartureDate="2019-10-28T17:40:00" ArrivalDate="2019-10-29T07:45:00" OperatingAirline="IB" MarquetingAirline="IB" FlightNumber="6274" JourneyDuration="P0DT16H20M0S" Class="Y" Cabin="Y" AirplaneType="330" FareBasis="Y1N0C9M1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="2814.85" Nett="2814.85">
                                    <Service Amount="2632" />
                                    <ServiceTaxes Included="false" Amount="182.85" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-28</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="7" Number="56" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG712RRtHjjccszUXBGzJEJuRjRcBLJmLsZo9oSYpp1JTnhKmEES8Kptq96Pjt5faPgGNr/hwYXlOuf8Ipv9qLralIbdfpxQukUJmHphg5iIRKK0cWOA1Tyzhs5VybTboPSgp/fASHwZl0m9yTIHIcT0RXhdJpopoYcXadphhtik3N7ZanRtEmVnFjUP1XyCHNXACVG19c3PiKKbXdVSc9EFnaeY4Y80qbkikfWODx38b9lriyLk15BLkvpIsRf2OsvssGNuLC+GZyIL+s5i1Xdy4VQWp074qGEVKvvcUYljOVAvr84WtcZ1x5gWmMLxRuO5oPwjVuCPFec/i4Ijk6uC4sGBMW8yoEAO2Ovu8i3O92fIHNcg8FCR+q42hEqBy+m1DAHaqkSaObjg/J4xmJbUcI97UAKFf99PcmeLQ8BiSVKDDh6gwO3BkZdLcvOwKlxg6tWgMgZarhDn6bNgWeUMEqfCY59JKH/1KtFEO1uvzPMY2l77bE7B7bFLRQhRv9XMlS5UaJBi3AAETTkWbv7uvyzP4dgm9kG25rsg+uCr1mPB4NSIhhEKR0qABiAGx+Lp6AR8EIcsw5Vc2fIIc4CMGJkU5quPYwCYFCbYZiVvjmUaj5XAdW/s9MQsijm6B4dYNE8jkA/OOoAwx7ut9SKpiFwoHX5k6vUPttduHviFx9YZntOumHw3Ir4JQro92IL+dR2DhzOhc21SR0osVTwI8hNhUs+n/X+b5UROCdtDKKYXOPI8idw5McKxF/6MJXs51GRMDmRDwnO+TxH2f+y8UMrKSh0dd4ejZheIuYFcL1zoUxqptUdC39FDLzxumkJN/YjB6moxrd8c8AdYOaZUck5EYws5YnCnOKfhuxHBAE/sCnWHGecOhABtErQ4Ah9sBmzyti5R4KzfHz99/H1AuZjXN+6UtB4KckTXXmTj4CE+ZMB/axMPdn2m1qT1eSXMuKhXCyVVy66HvATAwhvipuDrWcGC76usCuQlBfu1j+KKIGiftoabwdRMUidZi8AHxf+tq5QhyFkLYZJ4UeMdUuu5uen9RhYIDSF7lQj00v29lpEEpweD18K8Tmvj+8kiAI6QD0HPnwsAKfIl9fCuk9muOxeF1uBURo/aU0wXTGiybomITbWVnwVLsBU2fa2YvlPT//5mwnbfoDQaWziDQqIcxVOkgB6Ah6kvUICQyzgUyPAn60jsc39W+dA5JZRvMe7SWWyRgTxHUhPpoa0gw==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AM">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="MEX" DepartureDate="2019-10-28T15:45:00" ArrivalDate="2019-10-28T17:20:00" OperatingAirline="AM" MarquetingAirline="AM" FlightNumber="435" JourneyDuration="P0DT15H45M0S" Class="H" Cabin="Y" AirplaneType="737" FareBasis="HKNN0XCB" />
                                    <Segment DepartureAirport="MEX" ArrivalAirport="MAD" DepartureDate="2019-10-28T18:45:00" ArrivalDate="2019-10-29T12:30:00" OperatingAirline="AM" MarquetingAirline="AM" FlightNumber="1" JourneyDuration="P0DT15H45M0S" Class="H" Cabin="Y" AirplaneType="789" FareBasis="HKNN0XCB" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="2922.77" Nett="2922.77">
                                    <Service Amount="2897" />
                                    <ServiceTaxes Included="false" Amount="25.77" />
                                </TotalFixAmounts>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="1" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-03</Rule>
                        </Rules>
                    </FlightResult>
                </Results>
            </AvailabilityRS>
        </FlightAvailResponse>
    </soap:Body>
</soap:Envelope>
```