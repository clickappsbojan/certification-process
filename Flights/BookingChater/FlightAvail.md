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
       </Routes>
      </SearchSegmentFlight>
     </SearchSegmentsFlight>
     <RelPaxesDist>
      <RelPaxDist>
       <RelPaxes>
        <RelPax IdPax="1"/>
        <RelPax IdPax="2"/>
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
### Response

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <soap:Body>
        <FlightAvailResponse xmlns="http://www.juniper.es/webservice/2007/">
            <AvailabilityRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-31T17:37:39.6921927+02:00" IntCode="QjrwJzNGIzw73AXf/Xv6nYOf+C52sSCqFYPrtxm8Hzg=">
                <Results>
                    <FlightResult FareType="CHA" AvailableSeats="58" Number="1" Direction="Outbound" LowCost="false" RatePlanCode="7Vor0/GRKZ31Va+BuE1WMFvq/9heAul4psoTS3hesB97bKcS8vVV8I7otP/319flrdJtWLiEoO9sY2UlyEo7AMdqzRPPN3VUEB5qpZSv9sroRDrX2gmyuCbtYSsDdhIM3MfuQp4euvTHgpS+bKiYuJGPjxmkKlBTY21XMIWDEIxbAXtzCO7hApVApxqNLUUSPhCtyYFidvysK+yqY5A7jr1nd1xWLpHUlkEVYwfp8wcFIp5hUebZe8ykxRPMcdKK/wSeTyLEJY4WiNLUSwOnUTFrG53JmjlNyM4tv4v3z7XwD0o3CBxmDNTXrQ80kJNfSPOVSsD7Wr4JRq5rhJ2REBfZ2sAqh0TXT+4XcC4i9uGmNJs3Bxta9cLg1JnempDXIjK3YcOE55e5FWgAILRPmXD1mMdk+JQgO34ubNjD8ietJ5PZQe5NWmbeI3zfQleLrTOyj+Ysb17HNqX7pBMC/n1fgr2VMbcPCc2pKrzvl4p/CJJ9ZLljj6oO74m8KAYGzvZrKjhMCUWkQEQh6ZTb2VDWDwvML6zc6VD1fROZeqWEOcBEM5Zku6FMw1A/GdAFgScu90aiNFa76Rr3v/4x6ZNDFX5IC1cDhyJWN8/RqNNgsTZjq35FJsiG4rwEPswIX6+6b1P5wWkFUE/l2xXwZjCJ6YiQ4uIhO66CI8WiC74k++SwjxsBohh2uzFP7FSel+rroCI3xGhAHFk4seVIT5Tl5I2IIVWQi6nWG2Y+j7n+ItGKWQLyq0J6F6EU7Rczj54zBNwhIHoc1g+ahR/BVuoBnUbOKwBpnKjQxl+qlma46iCon98SIOka49Q9mZlqHMjG9DlJCHNK7DWpVsOwZS+HDGBX/mUn7bwcbjZVOdQw8XDjIp79qTWpwMwP9oZuDB9sWxMdi7ZoEd2KHxY0s5jxWWepdtdpSwhtQbTl2uvQ3Abg4Ek1n0M4YiGMCHA+" Status="OK" Source="ChV2">
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
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="2" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhkeVQgCTimZz3FMF7EuhliZojJhDS9/9UvUxK2hu/Sg/oh8Dp6kCs7ZeCbWeCon8rQW+kiaIqEYRoRZAj4H9lu0onKWdL5VF+Cwj4C9efXp8N5r5QyXaLC4qEWZz3ejiNPFklSUlC3qYG+2M7LRBVDPS8s7/IehwslTf6WkfmjB7U12Z+WozP3Dq4ZEQwl2vIB+j9E5frtBRWolKUgJkk+h8NP2spvRcCtVnoTn6ga1P25en/M5YqSqAq+3GK6Z3D0mHHPFku1zDBo1pdvOQvVeyxNXuDN4DSJV2Bi4uCNlrgSv7N+GqLiv6YfOjKjb3Sw1+0jN3W3WhPSsXwYwTs802iuQHtAFNqAL9tq1epzMB6F6AoabQ67q82BhFlIAKvU0YOGPer7B1IureBaB40J7UrHija41pncVBtvNyfxQmE4M0GRfXsU0qNre8wIyqOmS1jS0fte33Xu2HMVFfKGCqrWcEdwrAmJPMhjzvz7BWAmedDvxekHJ6DFB8m5crQ+QW/sZTkBdLR5A4tlq0DZJ0wSxOeISzQ68cXbR8qbSsQYbtIy5iCctYVw1EC9T19R0ZEtI1IZT0zTRsViT+rBUxqdb1sXDeri905D/UehQLlJFUmMbA/s/bl4L0g0cxM9P73FXqGNe7O0V8W7wasRDy2d2lpJppYnvUL7Bz11xlRj9ojZocMA89UWtZl/YUktNUVCwzAgRImi9gq/QL++F0E58xu6RHUqsgDKKwIPULJ4wlZjtIS1T9/LvrrfbR5y6PmlEoppav7NKq8yCcJr1AZ9iWC6ozkbxU6wt713o2J44RXEvu4i6esbdSMhAr/GdSm8U2fyChaRZnh2NF/3d6nb9t5FZ0lMYdgiSDE9RAEFQErGxHczPqfvRA2Vwk0ene6NSYVzjo6sKJKWyfa2x3vztPWp8aJ7C60ctlFTE6riVPbbh/OWoiGwrr2IyCeOY7Gx+InV7NJ9EZoqw1/4TkqaKnZApDka2gXKexVtrzpva6Q7ARYkgpK45wKPhlYvI6V4AgPfrjC5dWG/bnEeF6b7ow9kLfqWvtDOT8jSQby5RFi91DSQNU6fdHQ5+Ram3xZKBL1FpyUBGp+k7fRjAxAiS9eXPs5laxGbdot5UlBzAdZWErCeOtlP9UH5ddVuAcl8XJQPk8wUuseWj3pXpqoo04/geBsjFC1PXe0EOgJIcXNOFRWM0hzxZG4joF2/RgI1l0fHXujW2dX0cZ3bpXt3i3kv38WKQADt3LSwCqiW6dkmUHxBBLW3dAivOO2gVDVWhzgiAleYtM/qOkz3iOluUlNKr4jJjpRz9KXeM1zFUrtz+0DqOwiezwhk9QOK6dntRpmKcRsOLObYwMpruom2MngqQdhqfAS21DrXWohsn4JEFRuGNtAzocT8K7+KOKxC6IdLS/F/vFXvFXeCHaCU9KQvLmlZZGLvXTRWbey79nRZHvTrnXJfzTsp4KltUqCggd0wZHktfrJOtSHiMlAJmSu6fhWgEjAuy89pt4SbcPUrUBd/HuYe+KX6X5sMunnSSiMGw0mWVnSiYVcQVeNEsvam5Ef4HXY6Q4mpW8NbIZ5edCsrQM5vzjrz4ztWDbNvJVivrCJGSm2zx9zA7WiYp0aIMAS//NpLWMD5vHQ==" Status="OK" Source="Amad">
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
                                <TotalFixAmounts Gross="1359.04" Nett="1359.04">
                                    <Service Amount="950" />
                                    <ServiceTaxes Included="false" Amount="409.04" />
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
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="3" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhkeVQgCTimZz3FMF7EuhliZojJhDS9/9UvUxK2hu/Sg/oh8Dp6kCs7ZeCbWeCon8rQW+kiaIqEYRoRZAj4H9lu0uf98VJHJovC/LTnbr/mpkHZDtedDn1zKcPbGVJV0m11uYML7azxiLFT8cwNrD7CaDeGhuL8GXAzaxD1me9DnDOrMlIoqyK7rFgML6NOb1kzutTcwyxuytGAq7NqkWhsBviDOHa0XVgB90mpALv1Zjsb1A8TT67FPOZ9bqBZlUMR2iaP7z6S4kAhVQI84srV3PnO0w7Vfy37FPpP3gJjCaUe33ks2BpqG4xhGEs22OwgwCcMM/oXvOGf5pgdF/8VRptpHZS9ihD1tOLYJBcLwNqgtCK6xgj1WGXmrCi7pmXo3AFJ2I4xuFTre2I+qoiX/FUW7rp+B/GMW+OhF6+UHrolPyz1oyiE8V75NwfViiJXW/SrMDtGFQ+g3CvPYAQF1/zLw1nFZwO3UknWuyFZBzGY0RdZz2PJuoeP+lcq0bQYIW7vp3i3kGKL4+MC1CG8DP1Q1NOPxTep2f7A902Mub2PkzujTmcbcWwbvbKRyOMjbNOAyO84LvJrIpFAvojZZbcn1NhtntQ6gvwnut1F0xU97kF6FWpxAjR2esnk6vqkYm7V74UMUlGmq9mPPwOA1VMdQsMkanXKxsQJfzGm7SATHv31HKDaH69NFUAcXv8sDlsQSuWVj5Qu3PZojydZbBuWgE0nI3rmYWPX/n+MDC8VD+3RWUslXbPIjpvJTZPp+pnQA5t8TYvix0GhLwV8Zlifguty0qMtZ9Mr8b/nZgGfNh9VYSGwX9Lh0zZ+x04TnLYBBAyTUaqUBudGsz31fpGVQw0GC6Kn9D0FBNEZkQL2Mxou28QD5uWXsyAFcyVPqB6D0hCQuaf5XnNj/AAvZiKN20kfYR7bOQzDafsy3bROzrhGuQuIUCe+COaeMeMBvtulIzqP3J9Zlg9PdlSwjlx9kz99++aAQJAiYulB342Fikg/rCtogaz3ytKZrvUVWkpElQuF+S0gZXf0lGeFmlEiPYB1mZcOV7UL7O/MMOMqbQAtI2J32/x9p2vXwAHtlNZOkJSEP0wplxNsoqDlS1axgKBHcikWS5egqEEq9RPb8R9CQ87Zn78NkAAUUoOufjgsuyWf5Oz0w5pC2+intBTFJOTGiKsNhIG2FOK0f6S/dMgj271jbvl4PSLd1HffUUtBzwzib3bCkIpAuM32XU+gbiwoS9GvyfwtOnegIDfr9hgQKVm0WGIdWL1GbSLKlZkqD7euze4poeTPju8AI9nab5P7JAd3D3pSUrNnFMQ1g0+/7yOd1C0mNQUoFWexQ/pAJ8yKvnLtv9NtlEY5hRBm6DDP0QoR0gm8G8oMFhHqhRBfEXuIMz/mC/dE+mLQgXf/syGVH/+8n/tXzoEK/QzWMnquh1Iy2riIlSVy1aTKfH6DlkkLoiDmJLJ+kjjajSUOzFzKZHZ2JH+0X0Btk858nkCm+iBHBebbNFERtFViKyr3HsYFd9DBESNOHctn5GpZFIp6AmeRST79UEGlNzZNT5b+FzALX534PuPB6MbCYZopr5tzpHALI6UU5n9bSNodfCHH3PiLlB+eLLGVX6xAaYkSssf+sP5MTKgWEHQ==" Status="OK" Source="Amad">
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
                                <TotalFixAmounts Gross="1359.04" Nett="1359.04">
                                    <Service Amount="950" />
                                    <ServiceTaxes Included="false" Amount="409.04" />
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
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="4" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhkeVQgCTimZz3FMF7EuhliZrDeEovOa5lBvyZgHgJ0xwwVWRgOAuKrcOpnUyJPDejnARfb77gcsEoLlZ3B7x0nflyDEn7cZ/6TUY8w2m4IHokv4lPBx9VUK2V6sePuPlRJG4Prmz1Q8KaWLl0sAFpfgQw2fJ+NOZCIVC8CoNO2dtwIeoXl4W3j4oVDyv+r+o6FMQa9gWf68URCVeC9+slsUnc35j6lg7MA8IJhLG577ja9DOW8rzphTzVcX32xb7W4EHDrkX1rALk0idFm0BVT09VCRVmPAVvq3KVDPqJ3obIpq6WuwVrxznYa6R78V8RGz/gK6Xtal5LWCY4EhvTHYWq1mgQuLsmD2JaI5EVQ1TUaF7M76uZ3zLz7S4wJnqNlTL7riHMzSh+rvT6OUBNdZggS6+1mpP8pIcxeCU5JR9bmIB96aUQAuVJHzJK9W+vxVsbaV0GhHiF/sH+SfBKpphprpGZSl0v+nPDtGiBGAZbekm3uPcZpqwiOhMaJEAL4+x6nzTxMPfFj/nfVp2eFyTmJx6b/hRJ+5QOvHPyr+Cd9gSUGC8dAqBtGn2OkXdCgWHgLoQkukSILAn3GU3NtdRULHSLp3nmKhDCVFs5uEpfVe5xVxwaHrLhRDiit3gK/An36vIwnqyQHITqoVsaKy12NdPorpPIgVQR4xj59uM6CYCq3nGRm5viAYDln6P2DuVKncehlgvaV+ovfUQLY78Ix1C6Oy5WGYD7fyQir7VsnVIp+vkAlECK+c2x2Gp05q/E5Qz+G+LUzxxVdGYrXRkfa5IQmTp/rpKgZYlKAyuKvSbR+hiJbLjTNSVsNt3tEFQCIFC90qUygHza8l4FJZbBHGyh69kh5gyy/3XBE9yLhi9rNdeTlT0fq27Aj2rQSJXY4f5enxQ6EASeb1ltyrjnvVvIkCyDSmY70uv3/FQ1oxYjDb84V1rzXLBK75RikAbpysJmrt4AkexJeZrpk+T1RsRLPnBytTEH3LugSyn3gmkMbHl8sm2HXgqpm5I3YEqyCwoM5V/HhuvrXBpSwTgDLcUKhzCjw5StvuSBhmjJl8GR094fJO0zCwGGxD+kc15kjTU6dcm8rghi6JrJDlCxr5pLBjj7DFyq1XbXin+fHZ7FHjWUkfpZHvvALnmTZZZ2GwXWaZ7VtrHn8KFqxlGWA1OCM0HdXQFo9aw1ISnB/HhydZLjV7j4S2XLL/naZs72GWyr+eT/Lq0pFYgu5QPDGt4QdNocTuw9UIBvFQSpyFtskA8vOuGyG+cdJkGcwteoFUnmgmbacJNbZsqEIsamhBkiVpcMLxVWFk2RAI7A9uBe7S+cXPjhf3MbgSmtBD8c2yzRVHl/uhd6jkZ3pNEBva+6EILLG/u7Ny8Bzhp3NkKk8AZHGUNEw3LuvPryC0VmsKAzEMJvZlYVzBvwj6oIexjJZQc9bubNgg/5iZtsify3LGNynOfYVkPio7B3DKxu2B8xGzGsL5ALVgoewk62YbVazXOjm83svcna5/65idItIVeEaMtT6s1r4TjmHbEjc6tXFG7MvepNfMcpA0iQ3JoH6On2BRPPbZmJXbwipkQXwtxCOL7qEUL93/Mg5cJoKqsfIsd3aFMTfGxSzBIzEoIDSyuAN+wYAKkqe8tw==" Status="OK" Source="Amad">
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
                                <TotalFixAmounts Gross="1361.08" Nett="1361.08">
                                    <Service Amount="950" />
                                    <ServiceTaxes Included="false" Amount="411.08" />
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
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="5" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhkFVz+ovaZye4ZbMn+UpGPbGvIX0FwvxMVutlllh1X1HRFRNaXqqevh82c2bwTEr2uKBi7SBChCVADaAQ+jxDZZY0E+oD372AOs9lDGqEt4FVosYcQ8j25GK5dbd+EioyD68vFLE5FVoId1A/3jWBYQ5A3dpQCLpVVqsGlksLAkRs+QO6KhdLNlSbMPEjPupPLKF/ASchUUiJr3jPKLpQc5ni6kfFBQedkZu/m3OkQn4Eufz4p3uW8cGpBSdCVKWl8UcwG4vqqQNNjgbitazyGnnDnR9yQBt2hVersXRIfGcWhKpUqnL4rDOvuvPko95lVyoCk6RA3ZOQx7K2x5OoZARRU64bE3B6+sUDBpm5hLNTFReCbin26CXTasiPwPJJITmKHX6wJgpBCksP7R7QTcJg/ShE82cFPSATU04qJqDLwJDWs0sxSkuQx4GwAcTOohOMePPyNBH2J6n6qx8Qj+LgfzqsRjynnlVmHK5w66YShJDtuRKobCAun1hPFkK7iIJs7kNo7h7EVRcdM5jLCSFdqkYgatikXJV9NajmZtfnmhvlua5gUczUEvPoQA9GOHfLiuT0h1sU/0zsTkGHLSZmQK7Zdgalya5xI7FXNjHS0xbkWgApEneTN2KIPxdm69v+znjULP5uax9IeIcpnOUDhyZ1f/bUgY9voJkTEKG64U5LGgDfhb1ygpXItxJ+OsKDNr9L+GN5bwQLSzYemmnAHnBvj6OPuwOjIi/9grrCtiIBytRadWK+wSlym4JW2bcfdqt3NnsHHr1rpPpPRwkL/5+MRf15CnHge22hQA07lTL90rAhbEvP4zbYi3ag6oi0fg45m8HzEKMeSyk2PxafcGgv255r4NooRBFz9WdxcskOdG+4lQoihtISV6XYAEnNMvwGMJdFbshg3FYoxj+X+SvLnWQ5oR+PfqP3KmLOGUBTPCLSoyVQ3RNVsYcv/ybx3nDhljYeoeP1dt6dZshsKg55mbM0Eb1TA6hpjgh1SHUKyXfqxLq/XXAgFXkYIhgu+nbPjUikvpNNiDpKwiZ+pCXuWO1yOqlW9FY6ZHMZqAVh6+1dU21FobdD+oyy/0WW1BJy+RS8H8XXu6a2upQBOFer7rndw2kEX7k9zkMEhPLi6BGJavc0I3DDk+wn4wEr1Nkyo2mVxHL00c3gyM1WVyh2sDbxyqjjaXpV3oMn8kxUDFoIWueShJkIdN8MkpjtaC7rq8vG+ZuAksf3yZnb/lxu+HdmmQVDEyLtOI4df/DpMZNOWjuoOQ9nRgqmMtXLD2mKifw0NiS532tdKX" Status="OK" Source="Amad">
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
                                <TotalFixAmounts Gross="1469.08" Nett="1469.08">
                                    <Service Amount="1334" />
                                    <ServiceTaxes Included="false" Amount="135.08" />
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
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="6" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG7PCkMXATwXSSIrjzq+6OUdA8ejYP3VV60wZzDxx+C+O/KUCvMPJXN7FsH/rnc6q9cfU45mXiWmGd1j95VF/BH0u2OuThIKEkz3Cka10QLQr46mR0mPkNaxe1mHu7RJ+l5yjBQdPQqv8yZJiYrwQS2QQP+lq0frQdoEoPd7he/yfd7f18lECwD1UiZ/N0D225Dz10mSMEngZeksAjytAY0iREcqdgA2Uhuapdk8FZQQFtgu+IUYtAlgiQ7cGHfemalGwIkTtx1wmv00gLzRlk0WKad7FAobzs4Dic83OQW3Orct2DnBs4FGKtnD5BQdg8pI6RgtFXA/BLHS8PVbvHmOPFb19skp2tmTZ3br1acpBvSZ/4/abDy3PDXi7hRvJVaNlK0CtqFZhGbxLE2x2OPpIoJzuPxtuDK2s+opxhnBS1iJgx4/AxIdAQ458gyf6bERj29fjROn/hbjiWUxBsZPS6RIELp7oJlzzbeI3tZpSjwJgLO7T7JvRhdrYpMPeY51hDpjlZjXxsO3hKLJU+hL7UybQ9dhbxc6v18zaG1qymA6CBZSIO0gbKSOh57D/yNCwU4AZSiZws3FY3uiRB7q7CyHkTippQD6s04qJZ0EdJLII05wk2rfl9FlDkxK8uyomTaJSUz2wnp3O2D3xwnPCQSemfsPOM2alGnyo0X97BcHXcR5jNDHRYeWpdYj3/XDqDXt23qh+BVoi6eKCJZo7YuqVzL5L7nQIgfoHbcWraQHwtp6QpKRhtY109CCc3EGFWv0P4K9KzCubS9FBGUOMv3SESUWD14W7aQN4b3KZNccwqjW8W2UZ79d+rXjJxqES7yoMDw1WClJwB9pf7+icoXAshpHFLNVbj4Ig6HH+lV1QSWm/nY6OofT3msFJKqTmNbjGI4imbbEVTcL8jM9ShXfmludVWwHMLCDpjMWp4UtHroPrFyFrLhUOPtweqK8UWhFCfXEiPfxKooe4xT7Bgw7H7mttwnKgEm16BjYkTkQ51yxg29wU7DssTgRDCAWjn4K7/sUs+uFf1bZ/qgrl8G45Gaypd7FQ0/2UyCCo53l2fU+yf9ePRhXUn5Dj/rx1Xcxndtl+hXdetzikKvROz8ixTCz+VLK/zYFxAePdc0ZD3Ac+8EtFmpkj5WQgOd19T46FyQoqNCqkfok0exjmtI0Wb8IQLJcQg0WP/Luwar7qp6Uvv48APg2+fgW/sboXUpPyQo6ciw/JpX89XdUSkbNJ1A/iF5GT4klPxzwxgDHAOuycnC0f4lr+qooc9TdZzQqyhr8qq4MVgLppFzXS89b3C6dgT+EpVA/JyhDGRB7xj20X8GC6oNh3NFJSB0FpkD+gjqNX/NPyUamU5B/6M1ZNQDqqaHuh3EaHERviRoX9FdmBGzmW4jccSW4FzkjrlUhJLWQBPAjyB38FTqI4vAI5tNpQeS7mz+qfMpw8i9IytY9n36FXQ62ZXnUnE6PysizEn2T0jz4cVvkJbRSZOab2j4SzOGoMaT31KfZC9ybnFY8NJUbdwbq8Mc8ct2w/8dfAsqkW2f75akZFx0zxgr73Oa1YRDKvyDnFt45FRieTVAlmOblIBgZ3rd7zDIBNHsFB1T69JVi2w79a6DqQ==" Status="OK" Source="Amad">
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
                                <TotalFixAmounts Gross="1632.54" Nett="1632.54">
                                    <Service Amount="1194" />
                                    <ServiceTaxes Included="false" Amount="438.54" />
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
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="7" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG7ub7FMhonV58I808JXF/hf0GEjc1GnMc6lZnL42NrZ4ptdrOQmk44n0NvXdCr+4x2RJnNe4I3Ok+27R1ngneRjg9O3ohIlu1gE3Uu10lcEmtMKQaap7leKrfcrKEsvFnE1KHn3nFRHdxJiS8qQneSOIZffp8L6vTRq4VVWM7hcBtH9+HednwDr1f2f8eUHGzHJBTemdoTi9lUBMd+9NPNVgOV9XGEUDPEUiKBjvhwkNQ53O11yTO0UDNkz7oG609JL+cOBai2Oaz734VVAa9idb43w4pxu5eR+aV3+bAVjQ5VZMON3D9xiRpvandaG16WnvE4G14hVgfH2IOdm9bsE9Y+OFDB7VrVBqlaaWnBgaeEXy5EUCzV4bRnJb+w/eXjRT+v7oFAxSt0Ie1NrHYM4LQmQU8c1Jz79fP4EpWch8AYl/zT0bFtEBYRpqyUFav8azJiS9ImgJjSdub0K0u/AYIRR6W7HSzAxC4f7VDrkIosrSl8bJXU1szpNdFY4Qj9eG0foV6QrMZ+6aT5xhUsXLMx7nOy5Px8JEd5wRtp2wgoOxCstZ8cRGqcgAfvCj4sKvjSL2jV93cD5zR4KoJ2KPJYqzPQf4HvjBB78Hybu+WNwe1f07fQTOvihqWI1T2Bx7vOOMgJ9pv4wZG8LpKo8n3sJpQC+li8FQQOcjxUA8TUp5NDEGad0DtOdIpkHMMjPuBHwzm/ltS2JOYGOixvrnhSitS1gg6TOvJPaZnxSgFIJjyX7qSpg0opWf1ky+9oKFLiNoU+ytq2n+ZEqEEqDUgk6YYo3OOMtALylWgBJCY+kSlToYQxv1hFR8AkdMl1Q7IW0t+FTKKcoPEOuvG8LTZI8eUS/ez78yemUFBktwHTlUoIdQ+seQkqtcnATrtRo7i8SUrTaihcpZO9em3HsXw5wTEQRZ2HuD8imHSYvXwYqLm/3xiJro70uEPnqNzVmp5nrypIKzbQW/ihtHhp6vuarsKVdvQI5vELBwi0kUHQKRz1JT7DxjbQ9MwrTm7Ae3evMcxxHnn5bcQwEKL9Aqtnq78WYyfvYH0roDV2Kqkmy6GBwrVDwedEUu9iunEE2aioc0qB35U+ZRU4zezOYWWg9aHAXl6OYE0SoitkNDuQmu19qZo8+W95NfDVHC7g44sk2j1ATb1KQ3MthtXarF1BW06Al8XyTl0ceNr8d9xxcF0wDOWRZRHQ8F0AadGDxziOcwqrm0PvRNInCLlne/gQCCuuCGaOELVdQ7mtivXR9E+Henh6JHgubBsziUjvawgPJKFHpdvhZjpoTa+sEA==" Status="OK" Source="Amad">
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
                                <TotalFixAmounts Gross="2130.2" Nett="2130.2">
                                    <Service Amount="1490" />
                                    <ServiceTaxes Included="false" Amount="640.2" />
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
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="8" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG7Gqr7yZ/VsWh8OWJ6eupWIuVydN5HGvUyGzW9luA6eU90/u+EVp/NfSB0Vxbw4yy8gNW07ntKrxjfhNjtfB8/V8pC04DWFgy8TLkxCtbpVJ5yk02uQRpwmA80XR7nL11+l15ImtjqBv/dmVzg1XiA8Om69EaecqkSEShfjUWwJvKmAKrpCybnQhZTxxU/TglOKKJ7TgJmP7SMc6v5bFua6RgS3Ootdcd9FH8+pNeYDMsiKnC/3ma+5yF/jO1YUOFfxmm8nwYp3Yaz6FygTnArdKYG/F6TqOmZvtrL5rxK2OeFvu/OrLvbsFqmBM+y/GxCF187OAK9Q1QaL1x0Yr9zj6rfQg21nz4MtpPn86xu/Trof2azph0irb2HD77qO+X76LGYDyb0NYgej8lie8KjJ+jibxJbio/mnWdWpRTY8I52LSBQBre4r/PbytQbtDl5JU0bdcAkBCVpPkWJcmowLShdNEMUYRW2tJ0jFesBMKqyD3x5IFpUSJj8Vp6h47CK3LVdVJdrAgwcuWCzVtMDElt7bDVla4Iykmhhy3Le9kyKcXZJvfDUU4hpCQdbBX9/sF1r9cBINKzF2cAYDtCLP+Ty2bZ+fVH0Sv422NndNsL/g/r9VNCaYriKgy4xtRHF3QD4zzx+/EigXq7QtypbTy+v9P2G3u7mMX+6PXGCa7kHkNPoVC8U5+5wFTDVEhawrWgSYqQd5htuu90TPIGnl5dWO5hqXdiD1yzVXlfZ8plOBmuyg3Z8pTTnTeM3n23fnH9t3pRQirfeB+Lvb3EQYnYYd/S+Zgz5UL9uv+U74lw79XmPZwt6/8dg0YpTCHSZaaACJh2AsHP9xYcPGc3JkE9uWlunjgqrpjEAgM1LdP7/MTJtwlMlIIzAxg/VTFKT4dnxC2XE99hH8LVN9ghedqhylwKBsmbk+lsxABT8QK7KWM5BKwarY67a0zEJIZa1+bVquIiuT9t7IT5zzrzhcnMa53oSpseoPbfivH/2vkDvwJlxprOSEwIlXxyxkAizvFp+Wf7qzRw/dU8OwIx8/XPdYHNSP/ssrrfzpTGExUr7uKBd6z80qDyp/E39cdqNjI5HUZL8Q00YIEvhfFnAc8IxOXB0j1L7I6qGUubeAGN+VZCRNUTYNZ5SBm1xsGkZkhRn6a7OIW+db585RosQIzafG2t2ofDw4iDfVEjnwQLOu2TADrAGDwISEZ6cD/hFNiMzPVavi4DBoysPRnIv74ZpSnj0PyuBuiNfz9NwXBYQujdGnv1AvEurDUi6aJ2z4uQC1Ot6JxxKoERmntE6FQymGIFscgBvujebpEnYvrd+XCx9VQ2S5//ZztQoYSTgNGJcOb3VNtfy31QAhp8H+fGps0rgDUtpom79l/2pQosxn9ihQTp4jeCe5u63B1r7am/LyN5xui6rnbLhOwTNlXJA8U0v9PE69lAb/yCED/OukPw7RS7bea9o8wG8MRm/UYILGbdc6NASYP84KztgdVwFR0Ku35nhe+aISK1r+ZkEz5nrn+zYJ29SzjLH06t56zH1fw1UcjZRfTbRmESg4Jdts7SxEyQV7uQsFxvpGBNSFYKZsU2g476HO1TPgJ5q" Status="OK" Source="Amad">
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
                                <TotalFixAmounts Gross="2649.08" Nett="2649.08">
                                    <Service Amount="2262" />
                                    <ServiceTaxes Included="false" Amount="387.08" />
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
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="9" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhkff7CWp6dtKhK6lyCdupZyyCiQbY6hR5CTU3O9A2BTPbalu2oO6HxyoBhVhOBMFkYhjEIWNkd7RoSRSK9XJt3jp+qfLknLIApcv15hv2HFG80yJJfCcynnJtgBPVzVD8nnM8UT2+2lbc/kjpfFzDyEiVjmsK+AKDT8moygvUfWf/2lL/zXXkpMVngDe73ju41tn1bnUHHqYNdChmJJlH3AawbYNccUPKRMYAnzzWCG8FWONZnkPzikWDbV7Oapolw5mXz3mleKIZNXL4Hl9z5VGj5Oh9C22ru4F+JLIlJrkmeTG5oilUpQZqHxBpzL9LvlKeAIZNRyh1iutwnZs2xe6BTEVUySNgSteDxamOYIPXQFVXdQFxG8DJgJUl0bWt4eBUavI7FbgyyJkviggvAb2I3nuINCpUuLsDvl3pRlcJN3BSE7nt9HNPYgfS+lwQ6lSjVNQ0QHrXAeTgXUA9mp14mH9MsbVYZiTxY+uLBT4Vox5pfLEvLTQGaM+4gke1MQR+2cMNLs3ul2rqyL8cTyRht7QLkyVmJ8N575yAgfjBACYXVKxmT0D1F8DC+iiq3lXaO0GoQnO8Xnz/JpOB1nsPqY/NQmsBCTeRVTC+vvW0s0i8GWnVTyoZoe4EqUgNQp6Cuz2PFnj0u98zyjIl5CA3N4lXMsVkFZ9GmPX54FhM8XSbLNa8Z7Je6IGKr/tcHGHJ87YclWf0vCGH8xHyxRZxDcCe1ZQWgKjF5Yr9jvczT1VhhTjwCE6sDzKQMXmpk5XujraUlIinER9H7N+SoeJYtlPVuTYTS346irK126Hx9ZbKO/e4UPsc5zzy8QjJQBT7V5bUKwajNCdYPTFauLie1x8CZD7mPbJrWvt4SRGarOa5JQ/yLapnkh28u2nevTp21v8NnnA0hH5RxrRnEUD+IUs59gG3yNAnaPBVh4Oy3ntZiZuuBpXenqzO63FMmPwTww77ByRIyE2q7vC7HLZo3Xk7zyjEPX440Rt0SUQGNjbolRJRwxIjwzp4XR+xFsa5FjGljxpA5zpT3iWCLSeHY718nnxxgR4rHpkJx6chwnGn4WGMxp/DLxynZ/2Fz2SzD4UXLGK/1FzvOZXw0+8z0XDSCK1puc/0ldwggcXbXKpMLNy7ZqppztfdjEpg81eNJj/zk/zY9DkpVG45DG+Mzo9l8KYBbNiiQsRqcP+aV0R2ajamGnYSD4FApXSivNFJKzLeH8GYQ+KwyuwD4qZS2m4WRsdgirb26UM+0kDsicWm78wZzBfS5Lx07FqeFuqJCl4aHcXBe+oYOkOZgQ" Status="OK" Source="Amad">
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
                                <TotalFixAmounts Gross="3489.7" Nett="3489.7">
                                    <Service Amount="3124" />
                                    <ServiceTaxes Included="false" Amount="365.7" />
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
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="10" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhkff7CWp6dtKhK6lyCdupZyyCiQbY6hR5CTU3O9A2BTPbalu2oO6HxyoBhVhOBMFka3Ik9GY8YyCDwEPxjGxoDzq2OW4FLbIDHPWJ/asHanJq5R6U1t/uRL2+G3neR7d5xDNeL0dUASNaA6ge9Xbi0MIb40bW1rv38U6bXVAT5VFBNkgunVk3qZZvufAfL54zgCn6UjLG/1wz0CElLqBVVRmwEE9/Y8QHDkUCnqPLcd3rd1htEpciMyQWp6VjRRcW4s7dno/H8W0S7Ff+EfNQqAT12wmB5/nXdvca+rgq4yoi3iHuKNsgsXh04TFvECgIMT14ytt79h/s1NrX6AuoVbbRpPyuNTjy/YD60FSDuRvnRoQ157Rb1JWVzzg0UiOMc5SPJBSIy2OPq9FijN9cueNQeQxkCfdKo03m/EzWldBEpRdHYokcGxZzCBDB19rgHJr/Q8Hk6HXU6rx+fM6Mp7A97OnfvGy34Ecx3lS+9G2J0x/ThehIxwu3RnUfrg0uCeUtFf1piVrN1TKwnpW2jtq23v19eYQFG4m0a+N2HHyzrsLWpm2se5ltUisfC1y9JH3Gqte20A60O6KRHW8++KugGfoa9Bk3IbZOSk7j6g2Wj01yoscBdMqAXh+l382V/V1iJrjJJZ9MzB5Y+ckt0osNFvjJbaOpVTe6YZ2DVjhTKLtdwhNmWLOc/vW8uDtVN/OQUoUPtxM+1sVRFZ6ycuuSX6JmzOYKdQ2ps+LI67zqHl0bBp/dfJSrR0ZERqV1hmWKr9z4bthisQbjlmm28ulGWFbPGgnSpXEbvePTUcod9Yowg0qSzOobKpcpKGrTOGcyCfJU+uEUC/tdsHCNw0XDt5kYepdmIhJ8NvPrcSwhKv4sV6fFFiFA2rA5XMw53kFcd/HWL1UvKokb9PoxAilcRWOm0Eo2H/62Dnl4cfKYM38Tjo96b9lOWb19Jg0iasl2y1p3AW8ys+ENSDsaLUXclIwZLPNpHwwuoge11zwuC0uNxsmwv7HZJb8w45r4t8oYHSQdQZ8eIMPBXFaEbbMFz+u9wfMFa+5KAxPtdoEay1hAR0muk2vxS4N7tfbgKF9ZRu7uQh5RmKEz58WBMuRLH9ejuuR4MxJix5IQe9AwCRJ56kVOizgITQ9Ast2ZcWLXQmnml9yNpcRMO1d2rPAytot+0sIhuh8kwFzNOzNdQ0WLpHzY1LI/q6fmlQYvkrqjPyknd0NoYVu5KTJM6+T9+Qxr7g/648R1/SIURJvI5eiMnEEWNdamzFE+BAXWzMivKzLR0fx12nWUNEPopR" Status="OK" Source="Amad">
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
                                <TotalFixAmounts Gross="3489.7" Nett="3489.7">
                                    <Service Amount="3124" />
                                    <ServiceTaxes Included="false" Amount="365.7" />
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
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="11" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhkff7CWp6dtKhK6lyCdupZyyCiQbY6hR5CTU3O9A2BTPbalu2oO6HxyoBhVhOBMFka9/esCxDUpkCCsiYeu9g1dt59FpEJWQ35vKwlPGJVl/s31P7sMK48H+UU4aLGkX2riAzWCdrclarEf4URyVsjEYMjg0VC4cremnMyzxxI9nv7FZ6uqc29whpDBqvD1+b1UfcrhF1vM863RqEyCqT9wxSs+n2blXRake//k1J7pHoJSUV38lYMl2qjcm4TPmph2fl01geh7YSaO/C3bd+MjT+9KwZ01/Fn7iibBl4zQSdrBvnGkhUufc/BwbKeFU+GhdDQurXw5Ymshc/tnWjLnas1P3ALY7BZInjGHPlLRO5kPJ9z7oFQ1tHNomn7+BBkVv71sw0CU25KiDgNGy9u/1GAxEX6PjcI2rJEfL5E7Swo0a89GshJohutS2ZSWPhdzMu537KZS5Yic8Jyleai2r3BzEY60DoNnLZCV/wa5IGWMhNXuuZn6xp2YXJsj1Hl+cqTaBFeX1oWJ2wrf0gUb3y5LbanU2XwZpOaQQ9m50dSeU4gyTKV7iZAm4Hx9hG+gn6YDB9kwggV/uI9uGgconqRefB1bqLPyIMf/CWM+zn69nvNIVNqb8q2yZ6YmT6khAvJQJ1f17J87qEy2Cwu1Wz0tDMmxwWKELdZQ+0MNq3YGjN3KxloUzjzgWmykwrd/wm80xKka2NyLlC0KOySGQvypFZJzSTEjO6LSLUspuTpM0yqN9wd4XJlldbVLcdiWzybObxvEciSm4/wyhNUXMqZh6uJkVu7hCW4Pz1rwTPOKx17hCfFxAml5e3vwsdwiAn5l+ovqusewWqRpiWozTKvl7HBMbAnx5A5r1QHvn1mptppx6f+9BzFc7T0ziG0fCB7llCzJpE4GeTn3j1rzD8MH+1JDyMjuSb+dCkw0ufXNYy1cWwQyvI+jwA5lvY4J7JD48x8doHx4QZoxi9+gOmcoKLGykObIHt0t3lmSsZwqq41QRWnD7JKcAZOYrtygQv9X1u4MK5+jnY9VHaaCt/WMJ18vLOnsshuU0SVldmuYOQDVIn/stlP00gJKS6RqrWAJT+1AeczlOM+CHva+ENevxMfVqA93YqE+lTeqO1v3C7nvhWGvb4twD5EOUaVHmdBYhhJvl8LilLU+s45XsfWLdmiIWCeD/8MEZwgUmysL7aCo2FP+GmhnOTl8KeUsJ2okY8CoIixZAwAfhUDfH/vr8YhSnp3HzCTVonpfhJPfzikzwXmaX7CGYf2aoGxNUmapjbsHs6a8GFlWa/yj" Status="OK" Source="Amad">
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
                                <TotalFixAmounts Gross="3489.7" Nett="3489.7">
                                    <Service Amount="3124" />
                                    <ServiceTaxes Included="false" Amount="365.7" />
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
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="12" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhkff7CWp6dtKhK6lyCdupZyyCiQbY6hR5CTU3O9A2BTPbalu2oO6HxyoBhVhOBMFkYOPRfVAkvx+unu8LfuAjIo0jiVUAGKUGSPhPE8eKoNs0ZAWs0cDhFyyd9vJG2vtMuC3mns8QvAcFFhNI2zuDE3if1PFxg5lYMhoUDsYb+o/DqBJ2IGvDHqvn4+cJ/GjEWXD/N3MdK3Yn4iStUNfe8rQeqd4XWZrl57Sw5PK9bb+Ta5KlbP8r1Gybh7ri2RTmnl0kd2c5pcMW+FOr/h0NIFqCvHK1up56oexYddWVNHINlg3AOyLoq05GKQcV8a+I9izZe90J1vwFQ+/gDCFOE+bTPty7tueYXRjIAL46fnN+nGP0XmmYq5A4twTLgTtmux8iHjeb/atTXwtm49WP2OlAbgo2gCc3xmByOwzRz9nkzyky1EqO/uGGfkGxUI8J8nmpItIrgirv4ZZgxdauYuGKJpNyPpdymbPrtYuCq1fH8QzR5QjlTRd+LTrBHnU1hUveeQyRvSp29PMFlr2Q0G49Z09OzlLZpKi0AehLsFMcWjo7ycFZiDUpWcbR6wN0mwcCip9FCxIuzfVUqlvP6MeYvf1hYF53v/i15L7UjFnLbGO5B+zRMfYPta3Ghlnm+ylV7T8TcldvEuXwAU3fdai4Mb8sBf5N6M6zVglvqSvwxP9B25+NHVEq0zs29mdX1riWuFLBbXJrh/4xFax9Tk4kHxfAP9M0HD778G2IVxV9G1xIt4AoI3SLs96DY6ehElCtv/f5ixIiPerRSd2s3WKud/TimGEKgtjY0YxOg4VVEMNi9gTGhtebhZEDeRpg4ukvIgwZBQP5vRhl2CHmxq7ViuhW3h53Lh161ntyqDW/hiQYzLGhsLmlCDIrUI54Jf2d8XzxRF1c8h49q0+Xgyeg+GX0aP62+jHLVXKIQbeWJUIxPQtoAir1aQBjU7BauvQf47dAbuO44nKI6caz6oI8JspxYExOCHMqcEYFkrTbsuwpoJpCikWqoPBGqqdkIKqzn+5bGJjrP6qn7wohyLxMGY35pc1+1LSbgdVwzIUaoTMXxcqWOJpoShfnGvUpSk62mK7os5QZeMZh8Fm4/U048bUWUwkzcs+mUR9zb4mjqJme1ZY0pGzyUR+TYO5GMgtMKayc/ow/PNyp0kRvTiyzVSrnA2NDcPXooDIqlbo8OVroybQqknrTX4gxe4qFNn6fJMvPSDuIEHLhuJBceNoWNb7EeTx9ULa0xUV0xz9cJEyvhW0xgGFfweeEPw+iwXeYvsi9+sZwgDkvSVeUFU" Status="OK" Source="Amad">
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
                                <TotalFixAmounts Gross="3489.7" Nett="3489.7">
                                    <Service Amount="3124" />
                                    <ServiceTaxes Included="false" Amount="365.7" />
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
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="13" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhkff7CWp6dtKhK6lyCdupZyfDxbZ+Ra0Mw4q87W4IMCDqJVa2AAJrtAff3ql4rapkYCKpDty4YbE9a1gboCuWi3Th1U8WJdh2l71haxe1WQcGmrTEFeoXJUXJmH4xNYGuBRsHZIYVKKGWpa8kb7FmYHiLwKKVsaHDGBsfdxlgEpa4352LJvzuw7mbnOW62oyzxgv+xHVYwAWaLLO74Wm9SsRa0qCrfxMNEhNZo1kvff+kH89WMfZxiCdZFkmbxkw0kcyW7BoDfhQx4maiHa2a+wy+rR8dmKbSpGbF2holkgQNy/NncZMVjkjR17Jl7JbCAuDwQPWlTkGg9UI6YVLS7bsTKDOG5RAIPTPv7J3Oav0OU+fxUj9wOyiINfYZQiBNOkMsRYeQQgLM14pNPFe53boVp1GE7B5XtE2/0OZJBkKn/ajLYtWB4NUag27ca9sA6HHOIHBg8mD7Lps858391FIVacJsg2V6rfEBexFeR7J7UUepOuybUaOoQU05+5zhv+b0XCQ+vduXNfTi/trNJM3A21J4TdL14cfg8VVAMX9yNz1eR3N6iJLHlbPz4sH0TokA5hSYDZJg0c3kKEzYHZl6pKJJNUA4BpiLkNSHeHnj7is5Q8GuKYx/HpP4NI9YQf+fPcQgXifA4eua/RMJFovGs2AHOGYiS3xCH3y1jkitJuda6YcXGOIHPu8lL4EXA4TgwH/+Y6xsM3fXgloYe4Iz3IHeFDtsIJQzuNAlKbA73M7MDiWsbaABEHpymFa0BHajBOda0nkGSlh7Cguu2OH7v0nxEe8X6sp5z7VcGuZmWkA4IGsdJ/Vk9SaH2LZoR5zFN/rfi40yRJNHWtFYDqYO85cMw1J6ka7F5GDcbfiSfNibv95sSYKp6we5CsDBPhlQuKf1EUdNSszVONRXuOXwJBnHMczae8yYiuCX4oWJJrw89qwoIHY4D3yQ6qtHN3AxmblrytQWMmZXEt+PRDWgZpATGJGblGPnKXJzVj5UXnsgphCGQa/RdBHCeSUlDSSY062bmedf6KAVUP7NP5269yjJFn64azXmK1VjY/OvsMfXVxb8uQWizfE6RL+4vfx8k2kqnmrVzChWLKVpduJ1SFs8UIdxfYFdLDD760l0DmVCRk8e3VjKngf94hdz4IZWFLmS3YPjQub/UBYJUzNk/LLTLF3RIOIqC5kqPCXtlnOeH0Ns9N6HdTn/C938pLt3sbj2KtzMAu0BHu841U1Hlqd3vWtlek9twmPTJK5Uob4cq7WyWuQqn9vfkliGEcfQtVP2Gn5R9oSRU9sDNo" Status="OK" Source="Amad">
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
                                <TotalFixAmounts Gross="3853.7" Nett="3853.7">
                                    <Service Amount="3488" />
                                    <ServiceTaxes Included="false" Amount="365.7" />
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
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="14" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG7qP9ah5wpqaNF33Xx/nZlty1iJi/IyLdYpNnhExGd5ZQ0RJu0zueN8cG8EYtrW0MNV0nWtyCeoh9RS3yfSOvwQY8j0hDr2UdhDI15sCmFl/SX7XDLpJnFNQOhCmRFnlIYP5vQlJ7OX6CfuJzqwbBp82iD1Y+X1KuYoIuOONocG9IHZomG2e/ZAfEFX94JW2j7eI/iVkz5taAiEsgjCdJQKHcfTzHDzveOU52fclTrJNSbETiwJWli03lAHEX25+t3h6/ctiPeyFwWW1QUeOMlZnuPwU91zhnzrE81xswQ7Pv9mxueYMJjuZHr1uWh6JK36qoX8DjcDR3y4mV2NiZmT2iy5L6u7ZJjRBwGUET+mWc+8XnJUisIYzP+hwTnz1mQnNH0zA2GMqZRmUGeX5AjMwncmnj1bLoDjFgfu9uNm7gSudqXI+UWC9oCBfxg0UZjKYolZwKHjjt5KdO19XXIzwdSPLJxEYU7HX6Sipbejjln02pHh+Cor9TAAXUsPaRsqs/0wkDtRhwWPzSZNlp8vZ5SIGtBKiUb5IGdxCUGlHw5lwW+2bTZyaYdGOkzyozAnqcQb/S36xB2fWE3SrduJHENqggyTnIRWxtCx7aWzCrOfRphuaxD1RN4fn+Cothu2GRQQU8v5E58Wpw07qxTfJW7Oo3DF3mULJxEU1M9a3iZjbp2/kZvp2yTrcfJfgkV1Q3XTsCJiBDjQN8KBroF2eZyRoK4p0u4A9Oz2INnCWGREcJNT90aI5aaHNFmuvFPs37inTwpFJ9cv8KKHO8JsziGvKZnp5o7jEr411J6ZChmVkDMg0sqIn5W82YKqd7Yr47cFJVoBaFGhwvgfvpjVt5uC3cLcdkVkbSOdaFtXCDfDtPpzuHPf53HIlCM7zpzYLtOB1vv08/Ro6ltlSyZz67Iv8oAQxHaKpcSEyz+RIBIrBy/zZy/liWNsgbcGHhxy0StF2fMPMJi6wtIKhp9JWMOTWiUT2AkQ515YrIPKhQ+H+W6X6brdyxMPBfrwKZHp6Nz5oQvp3TlgkRMD/iji5fTQGmQH8qroOU396moBo7woWNTzDCnJ0/VI7hNXCqB12fI3HfvtzlZExL7ryoAIydtt6eJO4YondeZsyfx6QHIlhHWXRj16wOnndidkgFBeYcPyy4YZ+wM8VRRPfoAjHkKPA2RlPC1+h6IIFAU0LbAxD7OmhItce+qYtyX8FZs+w3/AWH2tGeVm5FEAeIcPLrf2LEXZ7bhLosALhKNXmniTw8F/aC2Y7DTnC0xIbLu" Status="OK" Source="Amad">
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
                                <TotalFixAmounts Gross="4159.7" Nett="4159.7">
                                    <Service Amount="3794" />
                                    <ServiceTaxes Included="false" Amount="365.7" />
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
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="15" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG7qP9ah5wpqaNF33Xx/nZlty1iJi/IyLdYpNnhExGd5ZT+msYn2XJA6mp3h9z3l9qsb3OEUGQERk/PWbVwZxe0MClQSwl5m0xtaxvw8jk/sBbiguYJT8SkH3kGcEe3xW7LPOUk1A0IbUrvrCGBNoIsU8Y5pmgA7yTjaZPjyNLDZ2CC7n85tolV3/05GgD3JiA7sQTdTsktIvIqyqNxKPLdEtwLhav2SN0GTpINsJaZHxNyPeorjS1dAw/S55JkiaqlKYv4Q79U1+2O5Md6uDOwShIURrSMj71wxgzqxbtXYTkuZRaCRHTCmOtWDdlsDrtseUfCzcWacmTZ690A4xGX2/x9p56WNfwc88xufHsZcMIrQ1BFO3i/ie6RDPSkX5nInTeCPs//w30twapnIPgmQJ2zXqSNyXYj5DsOVkb2sF79cIV4H/KXWwlhIlkkuX1Aea+HXP7/2VcGN7xb6S0r0/VtGH5EJi1jbFN4v5gwn78bm3FmYy9haMEOk1LH6i1l6Vs4ZbCC1384Y5oIUwyJ/h77qJwQ67M//hzr6JE2kdYWZiy1+S6VYdEEJY2o3lbcKb1OM63WOONNsuyf7KBKOhFca/K3rsd3gc8lrFzVK+Yj+wjDQtWt5++2JDGA4M+apdKArwAndw7cboZVX3LcJ6quNjFxCJBkAoZ2rkO3Ii9NVkTp5vumt2rCozB6cRnFoI5EvP3fjGRLc83NGC1RmXSAQn71CU/Tqa95CaIHZj5oe3uxM8BZxrEwAunV9Zigp+L26bnu2mvI6yWkOA6mb+ZzLu3IZA9Q8bRvnr8Zu9lRt23AizXSoYVyV51xBF/bSHXqTaJ0EMRu9mxIrM8Z5u9u1qsUUtSugsVyQ/PKaTme5UzywE7+UPgXRBOgE8Y9IzWv1VooZMyj9UdCpvEy9IjiNvpcctsp+bn1Gd1eSkQcPqK4NADoZ9Sa+bgHgbqvr0TdDlHbryXNpggINxZh5H5w44DwMjiZa1+DBz7H/qtFIJwEtIivBuaeR9h83Js5zVPc2BvjFsKwzBXxwBM6dlKuiF357pIYmpDk1afvC8gR+a03F1fFdwnp337/w5GR9KjJs3kKwE4gP+z0DpK6D03wA3NHERWSLuhaIiLPuOlO39NqrVS68HcQiPi5gBRFTxU/35UWLl+eeEwjFp5dB5kj7CZZDHKz+3b4zqBv+g8XLxje61wUWnmzDGMfIDWZ1Iog/C+6pgbQQ5dQx/+axScNkmjWi3J6pDN7L2cCCoPf5ioSc3EXk6fy/5VnCLgs" Status="OK" Source="Amad">
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
                                <TotalFixAmounts Gross="4159.7" Nett="4159.7">
                                    <Service Amount="3794" />
                                    <ServiceTaxes Included="false" Amount="365.7" />
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
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="16" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG7qP9ah5wpqaNF33Xx/nZlty1iJi/IyLdYpNnhExGd5ZTBLGhEF6qxDJ47QvJhszmorRcceOus/ku6hwQXEAenFlzOb7Tupvrm7FPG+VDg7dTEPcmvRMrvmLE2dN5XUnl+SpkRBpEBM34pkP58iSjKtXDNrmUOLCR4VYM1PqiAVXX3QDRKp9SKdjwQ648MWGjTB/rvyHjXL8FaV9a418OTsHoVG1BsjvW41J0GK9CJWuKzh5zxiRlyq+lCfQR/U20QRiDEumUkMKwTpMl6l4mmw5b6f5MVEcwq+F6OTtdkx+nb+TcUT5fC3WSyAnOHKISLfWyuXWREbRhoWKx9ZAUDYfpe46Z2lyViuAxT5M6EuEPRjTq4qqRnKxz9Bw2pm7ir/bCFf1OPuv0uyM1sFjvkKngdQvGE63LeCdACB9zdjfYAODIHTUu85BEMf5JeGiyr2tVTZH34ahTtOHssCNHwsBBL2xlTqTy+G0vDtkajxQeMic/lt6DIy3E+g3rrq0rztlZjzyheYoQBpQ4mQn5x3hY8rMjX00Ev8skpknFtC3a7jJ4Ampuw2fDja+sShoALLhZPfpUJ3+j/4EMtdeuUlrrRtes2vlwEoV3nMDIqGnW3FOFtzQWpYp9B3BJbZkjWqyJtV0xVotONhYiWfoyeZk5Lptlr++OOm/kAlx7Y1vS3TK2bLHEfCbuYoGpua+/AsjbBU35y4Z6r2Vvl+TbLGYeQvM0MthcX7Kf8Gw5eGUoMMs47eZ1shIylIYiUf76NXI03UiI142iyH76PlV7KKqN3I0jB28QVE8fLCStNOFAjPReqE5WGNqyxy1fKBtzz62RrrZSwwi1r0zSJwj38q4rgmfI8qqYW5hj2aoJjKcfUeEnhGrSfWX407OWCFa5hKAJ+mOKD6PzT/+NEynQ9wO75QMlDrU11iR1aoMZh74IgQ1AWxex+DqlhwiPdaAP/LV0icFcXTt6mHvd79dsq94scubtb0HHkeK3X+0qNJ35U0FZLDkxUELdD+IwF86zYd+naKUbe7PEcd4T79SHCLOBou4n4pss/xQnKOEhkbeaOEqEepLulSYBja4Webxxgva2ybqpHF5T/3Wr0+gBxUHWK2elDaryFbgWPymHa72/qDZTazjXJnmfxr8OJ1PPb13I5teCW4HNFGpKS3iP1Dl2byI+joRwsk+A1lDA7Nw5V2wrrEEIwlpe8+euIRpMjrcsG7I5hDOiRiLmr2msbXawur7fSDfp4/U1bUcP1VXvuU7rzSuZgyjFAIOdQvEzC" Status="OK" Source="Amad">
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
                                <TotalFixAmounts Gross="4159.7" Nett="4159.7">
                                    <Service Amount="3794" />
                                    <ServiceTaxes Included="false" Amount="365.7" />
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
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="17" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG7jBgzGhfJT2jEcOGnLWsDur7Zm5so+dEf+y5gHdTYKmQqqKKxPqh9kGIwhZjnFMwJwjHtGcbjy5L7Td/aNRsM3DQyPCAlAB2gaZytas8W7E73pUcADIbegxHJrr1qUoThOk5kmpwSwmBx9bBn71FvLDgoyaFXihUH52WRRhz/CgY5wqg8mgWZR2EJ7GJfNJlnU5FH/vKlBPPzE8Fku2mgc+tvSIRn8+9KPHB2MwGgYta2tiPC+lpglDlMsLZXM+aGWVy2n12tdTRsEFISV5pau18ZTRKNb0dN1ceB6JPEBKFD8YTZijFxEwXA8O57/iOtGEUN7y28AxzHoy4ButT4/F/DUz5otcnHWUbX2CMe3ONiCtIVpcFGNUI/5u6wRL5COx6aZZrUuCkG4y8D21+cWprCL01LeRwnTKYcv4DvxZW0Qb4vrBqgCaZ+2vZk3uy2y3DRDUP7fsg3SuaMZipScuzZJ2/SXCgV2h7awiNKt2Frz87hxl8E6zpVhwyu+3A1uOI1je1Lfd0Nl2bBU/rROyhvUFBkfzB5qUCaB9ZIatDF++hxjYormL2nqXihXiUvIOtkH4YRxrXJ2GA4joa9L3/nDfPO1AgeDeGYDqeCFHYbbnGzeKZLLJ0n+2LlPmwADz4wZ/rVMrkbqHeq8IokpHGno5s7Nms6qvYuxPuEiLxtDD++RDtHWt3sy0hmet7M2vCZCAC3tOM3FwVL9nR/kpJ8eZBw7DggR+FtJxhVmkXTvQNncsouosCBlGMA2D+/nKtwn9BCBFgMRzTsBSlWiqnHnWmeGyglM2yNczwam3V0bi0Tyj/xB8B3Y7/h52cdu5iQXbYvV9vMNx0d2A/O2RUcyVVMoPb0pEWb4pkmbJwMAMEsXdEPW2n53I34n1QCqiZcB1LHRPrKtbAyiBRp1ivoo3eHJuJqitVG7/k2NOmZMioSgIXD7jPGrtYm//33dPFVnHCby65iEti64efOnPMR7Q0VVrKoTFDkw7JfAgFPr87y7DIKD/NlBYHrnv496HIXrFgZ/I+7KkTalRtmWvmSI6I5ddNh7oYhHt9Dz5a8GvO3RZCo8eRw7hMd5fZRPN0wI2fqGzOxlbXv+7D5jmswWdeboXTdzbyUaGHjReAkuQwfzuiZ733p8kxNF4CbI9v3RN7miOMzAseggRulFZStQDlQUQ3YjqF96CPCK47jPgpUF01yywragyWOV2tecwBleXMLT+r6hDY0iJZK1XmBNlV8j6e9LR4wE6lJEZLUBd+6zAVlbzhu/cjbFecYcWGzSfhLQQeckhDuRgRBVw==" Status="OK" Source="Amad">
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
                                <TotalFixAmounts Gross="4184.84" Nett="4184.84">
                                    <Service Amount="3794" />
                                    <ServiceTaxes Included="false" Amount="390.84" />
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
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="18" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG7jBgzGhfJT2jEcOGnLWsDur7Zm5so+dEf+y5gHdTYKmT0KjamszoL9BGCwt6y4ot8n3waqnr4ha4yduj8q1tSWuo9L1tw1nxHDGcturZE3vyv8aP02xEPT5w4Ubs2OuYUwTPQMB6HEeGt2AUQOEbKt9TtBgeBxM8PAy0fsTR2iuYrY0nDRIWkLVQDo5sXRhJj3UEPuXQSWOPXmoOg2wTPa9Vfl5nV6s1UgCVmLSsbDabplHXOnrg2LQNBl3a+ZXz+nSmooDB/zsIPXMvWzrkGRlkDcqHUOWOB9JfRHSiEBqpAPxC17aD9GVRnWYcwNcHJYUQffJ9zWirbTmorURRCTflOywckgejDh6I6W1sTnRChE99EetvXNV5GGbv6dRGRu9WKfufBESEAOK5VTkSZ8F4JnwYQnRKoENWYhwjN4Ecy4qla9OK/QJGl11DTCItTSPd1/3dFzC1cakJSFQRUhZWj8E0pbnbhD9eEsKYVK04jdLvGiFA/sVatT4cenEKWMPLdd8L3y3P9bpOV4Ww0PvItIuYWEo4T6RBRxaR624Ws0KaS8JH11+7yKtmHcF9ZJyAWLLh5ldScfVErrw6gnjtXvmRcFZHBxS3O4rjOxg1ZTU66dI0A9KznPX4aa+RhnhPftuAVnEMvF7M7sIkhb5bN9SMk6U6hxNgwlRvdMLfatVoVi8zsunGwNg2W1OCtom3CHwqM/W8Bip0azzNbvZYzCxg0gXBzMAafagX53nC5HUh6DINpygyAwzv9ZUvUNMqMINGMHBRsULwn7flbArvFiIm2yoFWz0cxZ1BF4xE+rVOfDcHDPOIRQvjDLEYMFTcUrymG6efDY8X2DxceTBxz3fFCnVKD2GjsqZwh5gXp9/BbKMYUr1ADT17BoraUx7BrqC0fflXRG87oYcLW3uOP62+qlYnopROJL1NF2t3ygaAsvWd/LOI5E0Nt0+X4emEDxajfByaOoz9MUY9qAVc8hpe0M3tJVWv81VwMX6CK0cYJJyNW5UerMDZ2Go6qylkhPl6R5R2VItYM6qpbdqrd29nXiFp+cIo3PZK4ep4ngoHAlRw54AxsuGYyS8dXc0q2f861NibRxiJNCGRmolvoKqNrJXa2KMHc8uWwHQqT48tNm10meZhFmzc3fmgQX5deAe04ghiaEvqy0gtotyJYDyWSfS757itWCf1oEBq/MK7FH1qPHVnd3DPHs2KUprtKk+Ux4ahKRjYKTbOwC5woQ9BnCqKw+STW0p4UzwskeGxyPwVjCRALbR1qJ94M" Status="OK" Source="Amad">
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
                                <TotalFixAmounts Gross="4184.84" Nett="4184.84">
                                    <Service Amount="3794" />
                                    <ServiceTaxes Included="false" Amount="390.84" />
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
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="19" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG7jBgzGhfJT2jEcOGnLWsDur7Zm5so+dEf+y5gHdTYKmTRqXkqdmHSMRrV4OJV2LSyxWaP1HCqo+DLfX9R40D5Twiz3vHaCyL/mTisoNoBrZlYnfPu+SXnAbLiPKL0tqWO2RGkvUMNvhiIyUUXyldPq8pWWz2Ph6CVs6TzDtFZMyfmmnyPpOdB0gA5wyr+wTPwZqHF94/Y0J0UjraN41k6Ndi373fviU7V4PUNnTmz5wQS74aPhKT6VvHlVTDn0F5DF3ZvDv4AykbsYPgPC80WTE236ObcS9hglrpuGpAIICLrro13XfNFPiF700+xx8+ffxt8aYue1+/0jYxTkTOyIIDrBv+Tn9zSLlKrduCMtrX/BGw6E0i92HvoYWj1rnh8yX1C4SbMzufi5AHVz6ni17AWiZ5kVoX6Up1TgpNJ1oAMqM4sMaHsaMrmb86K9mG3qDYs1zib89c8bRjyUFONf+0llkMMmAlhu6gzBdu1kyfuZ7wbsnFpB0DeoYwvrtL665JjSyFLSYCeFEyXtCY31S8TxNDNBSWa/gowOjTRuevhPuEXTlbbsQkJAUCnmaJkxRoL1a+CxJvfZwTYSCXN5lZsjDqjI9KOQWSVFo0gRQwCLd7yTtWvHu8/CHRLCoidCA/6qkCniHLlRufj80v9ezYcFR3rli8oS8FlcJ5Z3cXOFZMCv4hNNxJuOHmi63Q4rUNR+B+GkboLeG/Afif+bVigTkIzwbpq0Na3272NjuVYnAqS7GX3tCQrqpWPEcGPC9jXVCAIRgQBBLNgFUY3qnnSlNWt8VizAOUdEuqIsZ8/N5ESPVJ5IPn9bPxcr4+YJ4Ntj9ur9QtgcN2ZF9f4St2UCroxQJQ0iPc1O1QM3rr5eMcIfChhmgvUDuYzeId3bErIJrBFFyVHvA/7WeOwN0thrEwFy/zzFxzvkDsXnc0SDIdP622WOawIut/iVsRC68cY+KxahgLY0CcC3Uwy+hFGMtM3mrX9e/Qof1xE3jz7X3jNFEMn+ASwQEOe9d0gXAdR78N44kXZMFsByNW8ksnOG3dAQlInglkawL6p+upkMiVngw3LpbX75RsnF1U2zWIV5pDD9qQyPffR7o3JtUiD47Kjm+8pYNhkER3pcJvfaxq5aDZzInaaTTWGz1bhZum96WGJn75kncU08/DzR9159qGuARg6OIWvcMo9ACLGQlvlp6iIsx7swIDkYsXhc/aEK52yraNWGAVRcMXGyicXwnOu60I2XawxT37uDtYOSbVqMYj5xJhnV34JPn5nwKheG2U5UVHpksF+bJdMlA==" Status="OK" Source="Amad">
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
                                <TotalFixAmounts Gross="4184.84" Nett="4184.84">
                                    <Service Amount="3794" />
                                    <ServiceTaxes Included="false" Amount="390.84" />
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
                    <FlightResult FareType="PUB" AvailableSeats="6" Number="20" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG7m12RaLMIpcH9uf5shQ6Ij1nEWKS2nR7hD5Xqhuzb/JygIAUcS/N2z4rAwxCIC1raTvuluDH4pZH91nKZN+rHYfrx3H4ScDY62Gas6thgHIHfPtqyLwrvC5ktU/rvGKd83TQuxRyFA6Jmn2tTle/5UWCl5UpAKwLyZA1oZccK+UBPAzvmhjf9kxUdTQdB/NP39hI04Y4SqbGnxfnkORhEbRUOLlqbrPncpFv6HXaumzaWKQHyMnZ0HUncqTFOguXVHxcV7wfWibiaPn+lDJJjkPKBj6h/wNVmif1IXaGwaowUi90WaX95vkoyUSICgKD/KTpnCLv4F9ov1LpwQoY7g9ReQUxdJ6caFciL1KIDRTxlmPHDSnu6EI3gmPA2NHnU4ROomkpzG7tkppOnN173w7zSJqX8ZyQE2sFaNpRzsnr0RI1kFZJUXy2Gugdy+nNslGzKQagIp35hRpj6gHMSyfwbH64Iwk1DG7mqPiI8Y5dctLsczfWIwhFOvUa7oKW3CDgSDwW7JbVcVUzAl6gyYXn1fEhTzv5EEAxQa++VGWAhGX3Sng6I2QgINfq9iYXkJta2zkhlcD6Cm5R/1vyI9GhANXO9UAlexmaAk8OyUNyv59mtE3JbPP29aGi3un2S951RQ895uvy2zXYn55tMv3SbwlkRaEjs5cDZeUnG54wby7iIGk27ANqjxQNdX+wtVF8svVX0YIuJcViQzXQt8CbVpg600SZGBx57khM9vqR1JxHaSFTBunVRq79mjlkwpHWLxfulR+v9ZQju0UUzdZ9rai21Pb3vrTGOnahrELYBubqAieJxVk/EzI5EOY3d7EzdWwMkipBpL2kAdLZ1Run7EZF28/s26vOWc6UKgcw7MgzJcOZ3r7L7kNJ7OluqMem1ui6/FLmQGx5JPgsr/fM4QFLlWvHhq5/LcUJD8kx0EonsgppJDSzgrrbfmKsu4oMennliJetu75XSflCuPXZAQDd8SGAesD9dPq+hg9/56yJszP517tP8iNxhdLb77OOcpDIqI/9Z1s/oEiwv/vtvUSzsl4Qpy8HwsivrC2SAXMqJ56m7fWon+HahZH/wlTYAZx/idBgh460STVF7bnmr8lZNOarUkuAGCgAk+xqO9klPVK0T8427m6vRRK/AH4bKoS27KwRGw+VzTGV84l8mWXnp0cRs9/YWKcz0wyLkdW7oNKDCOXNQRYf8HC+Gz3S02HcBpLxLLGxPAAg3Ttv+YEasWs7J8uJnLaZOoLQzL0jkZVH3umeToO2qGS7A1tPirXPmzpzzVRsuDNdY8w==" Status="OK" Source="Amad">
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
                                <TotalFixAmounts Gross="4191.12" Nett="4191.12">
                                    <Service Amount="3794" />
                                    <ServiceTaxes Included="false" Amount="397.12" />
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
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="21" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG7m12RaLMIpcH9uf5shQ6Ij5eThBlNGuhZLh9qAKJ3c6fXCMedcwcYX6bGM1QTnET/RtrK/eroysLjwemoyr9nNojWE3M/b+7kcVkSH3VU0KErwEfCVgCrfF6bddsUqZ7iOoFldXOke6Nt3z/+hMjFJQVZvzuZITsTbF+VDjBdFXTvwPZa+QBSC31xgGZbtieOPL5a2XwyXH3nwoF0nRKgg4QZgA8x/lQIjGG5TST5ljO/KkXkNEO5CRKKZDLBhgNiEZoYgCs6vlrrCbWvSuVBbMScfhMUVtuPIzOZzxdQ6QVSedYQZreN6mhXThHKTQobA0mnRmIOE39zpwdD2VDFxrkwPwbMS5TB9C+xfjslQSHFrZQX7HrjBdimgJE6deXDvmgm2QU8n8frg1NyioZlUbpJYcQh9G5ADFfh2DxRnpjPMIirPq/MJF4034IiZJCLCvbWMd0FCyL0V9E/z5ls4MpQdp1g+HejOqqYqj0TIZBRuE5S6CUMkr70EtFyykBOoUbJJ+7G2sihktT0nU1KLnXT7zaRgf6QdFSh9Pl0xloaWlJJ+w3J/rrCpvbAL9B6NJQZokfMSjpR+wg6CPwG1P4ZFKcFL0CMs155BJ1Nb4oYPnt1cxd4FFf9OW914oyVixg8avnP5H+HruYWF4e/aAebJG8F8kxSqH5FsRGyKzpY55KY3KZ9nbgdxa3om2N4uk1nMyzjBuX4+Rz2ob3ISGfmk6ZXsR/fzf7pA6jcFoatrM+zgJvnFhHx4Tb3obqmv+/yKZlOHSU/jjrLLhFqscyAGKnrk8nLwaYzhpt/D1NAEP48wTC95SJ2F3O3u1PbY3S5ggNtgTwPSuQ7W9v6OwIeqYVy1dp1n+YcyfYHVfMpjFEQPPtoXSqYpZaX+esbD+GNtYySbTBddHRkuQeHfVyOTbJJzXHYgach9hEK3bSVrbomE3c6GbCMoj+8YELnzhBjU84H7wzHmd98fThHUhf1D3IaaQv4DzbpDF7i5vPEHxwWWMEWE1NFPP/4+cFKIRMOTtD+7gxKA4BRjtqBfaUWgbPL0SfYTgwModeKgL0WxBeKKkTnpVSpBmwz7v2ot1NeXANLGbXjmzLaVCzmYIhxlxdt44FnYzTNuSmNhMaeIcxFhLr2bImRWlB9n+FTDmg1dtysIp8Y53O4kYkrx/L2PhFd/ZAPsrgF1/oQNELgLYDaf2lIDZGNAjlI29VYV6fiGA8mF42zC0duWSyC+1STXuWDCJysAWf8v9ULqVu57ydyOlwJ+z5UP7NOItLguuhwqvCxF9/2eEtbLFC+3A==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="SN">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="EWR" DepartureDate="2019-10-28T17:28:00" ArrivalDate="2019-10-28T20:11:00" OperatingAirline="UA" MarquetingAirline="UA" FlightNumber="2378" JourneyDuration="P0DT10H57M0S" Class="B" Cabin="Y" AirplaneType="739" FareBasis="BN400RCE" />
                                    <Segment DepartureAirport="EWR" ArrivalAirport="MAD" DepartureDate="2019-10-28T21:15:00" ArrivalDate="2019-10-29T09:25:00" OperatingAirline="UA" MarquetingAirline="SN" FlightNumber="9027" JourneyDuration="P0DT10H57M0S" Class="B" Cabin="Y" AirplaneType="763" FareBasis="BN400RCE" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="4191.12" Nett="4191.12">
                                    <Service Amount="3794" />
                                    <ServiceTaxes Included="false" Amount="397.12" />
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
                    <FlightResult FareType="PUB" AvailableSeats="6" Number="22" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG7m12RaLMIpcH9uf5shQ6Ij1nEWKS2nR7hD5Xqhuzb/JyxQGbqHR4dWlQg/USYqsXz5cdNVHvjVFOP0ntKDD7sFsyxRNKJUY0+VBEYdY40b6kCYLPmxSETTsYUq5wH/+POGPcBrCs/q1CG1ZDeE33MnMzR0MLqS69lZwGJaKXzO4XUKbU8e+dx3thckNsXgh3UP1IFRW295eLolRb6U78fKyiKSobSXobF320vpQf49v+FH9vKIgSrQoxv1fN1xm9sG1YzaAV5AEghiOV4coNk+b1x5QVSlH9SdNsW+yAIRvxnP5XAdlMNfGFpvubCSA+EuWizHozKFbn9KPJDTFVxj9Vhn6dRbKc51oXNO8G7YCD0lpZ7LPqWNuWX64adOYIWDP42skCdnQzBRgoo0QxiT3RJROQlWm7ndE+GzNb3Zv8Q7Y62nT19gQaqSfWBds6AKDJuKJtF/wlHMLSSDv1auYDbNnb0ZUb5PSFtOLBsrBtWqmkJw6Raj1Pwr28dKN0Wa2jkcK8JisE9owH6jyxLBPtMJLW6YJ8gKl+9wonX6q5n7wGsk6B9gEwfI5Rqoz4ujsMBKNd66ObPw3NJ0F2UVgE7k7/UqSN0zEu+NIx5mGT7TJ2VUpaSI9oG7wrttlp/tcIUdO4vbxX8QJEN7dYr0/x+M7jFOPG6KBS3bV6DQmdN1GiTLRqHCgpYcdSkIuu4+ukDqwHTk83AqNlMoHWOPD27dW6MHIK386f3Nb8lsHAPHm+w728i1WhDEsnQjN0OmYT0eVQywziDhQnogDYHFvoEZRV0h8ktiHDLLlPK+FHrJrV/63lOswB4psE8g5iYYFa0SW4tzRWmWGKHMLe1WwHBuGCETbI1QfngogmxxkBz3aPSs9zd64LMZi/ACrvv9//+FNxrm3qyjRNLwFcRn7Dkp/wPtEkxajPp35jAZzWsp9R5icZcrFmME2BoyEXXetaG2k8GfZYQ81PZ8oJqewJkugkQjNrBtRV2J+PG0oKk3aBie8tO1YFwrJDVq5tzuN60KloP4qYGSMoCYjPlFZiGAI5sDnd+Py886ovSC1BgwmWblpu64OLI8hAl5+lBtcUHiZL4pXTkyKIWI26alrqaKng781/yeP5obHTkKhlxPbE2q/o8Xk9DHc6Gl8OL5W7tg5buFQCTxxK9HznTL6wJbtrOVtCyU5MTzkltHxmFpVK/GpktXHdUe27OsGpQkBdiH1A7TBD3nzjxbVGdeCfBrS0Kp3gsUsCX+eKhZk+0dC2+eFmHM8K5dOysDUvYcnlC9cqS28rvEB1pYfp3yw==" Status="OK" Source="Amad">
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
                                <TotalFixAmounts Gross="4191.12" Nett="4191.12">
                                    <Service Amount="3794" />
                                    <ServiceTaxes Included="false" Amount="397.12" />
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
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="23" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG7m12RaLMIpcH9uf5shQ6Ij5eThBlNGuhZLh9qAKJ3c6cciyVvUdFYwgKe7aPKxR6sXNCx0hmvG5lA774Vo5Xlz50/DXHhTLRA3IIK6Jsm+XPcFnw1PfQTRl3dUmhXkWqFY1rPpR56s2x0Pg0oD9hHC332Jraj4ytBAYPap7kxrG6IZJrq9ST8Asge+pUfB7CC7Jx2FIhyKObZFkkIyNr5QCv/FjMMyNsPAVDtFADNx6ZkNmeGsiJuYWvuHRd01Ih7POSO8r4H7Va8CpBGygBkLnSnPaJu5yGjPakyG29snvX+PbxqroLe3P4FGKirjHfggHBJ2nYe0zOdyS6Ix3NVadjv0fBvFwWQf8RJdEiMQWzwALt8uMwyJyQdnz+pnUeJwvs2OQX2fmTD8nIoU8MvvNK/TYDu2e6dOIquz+2Hc3gCsVFv711eHkXs5CtguTA2HWw4zMq0VtARsFJVwl5J59XnAO20bGzRBfpH17n1u9UI+HVTKoW3i6CNDkOMWRs39+FE4F0kfkzhidHbgibbqV8o0VzKNPIMcUkth8Y4bJnKMADvQ/CSkBfndSwiNuapDYo5rf0DpExToMLURU9jRn4wGmQlfGqXeqtALRZp2nL9w/SzNpa7NWn3V5TID622VWt5flPGvuGLmjIqFlHFqs8jmLWBcDpkek0OqYtH5vsFQOKgiCA9w0dlT9XzQN7QYUByiYiYPx18e5sMbBBlynnXTsa1/iqQdlm6yRngA1YAa+LBy5NVcikP8jC7ttzyDHc/P6DyaOPlaUwO+StJhAJnXRheasK6sH3VEjxmH0RpHhpgQjjM3lniEdiYi20T944+QYEcnYqFwMMdhodK+u15IadWJAF6kxYIC1bZNGoMnIkjprmNKSR640eHHsQvSNqEgmnGMkMRGxi7UQThXLTl90LKIYpuW+rGuEO+jdS2ruREuVk89IkisHDQ/ParLB6OZDiotJioYR6BqV1edcme+UMVRk+97ZI2f0kbx5l34AdaOqY7QAMWR2fGHPWsPCATB/6mQy+H64/4nNkZMnFBJFA+FnYTxcYznUlOQbe0XrWTHrQOQ70epgIXozLGM5iUgAxEVjgLNV1qPQMsDzhiHtS3PWdM7OoUDoK70Lscpx38hupWTW+LKfOijuNOTAYkvap7AIL9pYurih0yAoZ/CJNqt5ISYvC8yBuzNPfe2HFLqNsWkAgs/jAI/mD5V8QHNNfeWiXCd0UNbO7UYiNkdK5TeIngv+UvQegoQ9LDgbigbHRyjH2Pco4yaP4NhtxKxmbydq5X7jH4LaBWFA==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="SN">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="EWR" DepartureDate="2019-10-28T15:10:00" ArrivalDate="2019-10-28T18:00:00" OperatingAirline="UA" MarquetingAirline="SN" FlightNumber="8867" JourneyDuration="P0DT13H15M0S" Class="B" Cabin="Y" AirplaneType="739" FareBasis="BN400RCE" />
                                    <Segment DepartureAirport="EWR" ArrivalAirport="MAD" DepartureDate="2019-10-28T21:15:00" ArrivalDate="2019-10-29T09:25:00" OperatingAirline="UA" MarquetingAirline="SN" FlightNumber="9027" JourneyDuration="P0DT13H15M0S" Class="B" Cabin="Y" AirplaneType="763" FareBasis="BN400RCE" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="4191.12" Nett="4191.12">
                                    <Service Amount="3794" />
                                    <ServiceTaxes Included="false" Amount="397.12" />
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
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="24" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG74/MP2V238TRZ3D4IIMYK4h/OKglkiQdAvC5McToxia2/H7Beu5PiXWqS83fAI473WRfYRCNiU5qVkDTzpIAI3W4wZQ7eqlPCWtsz58ybSnR5DB1fjXKCdYLw19rkph3cB7gvMR7e5xGn6K+tgWjuPa35Y0nX5FB15Sz+yUvueBTK5j3xiWsxi9z/NExwsjMcyFlcazKnGltrX+t0shL2u0qJFvi2HaTPre8gyzby3G/0TVsHi/0LWMYPt+trq8x8baPvMaTBFBRTIv9Dk/YpzYYn0ru5eFG+NV8cFtRa5dWzSxVL7Y960o2fw7APPXc7sF2QILYWGj8OGoYV+FYYVj1H0JZcQj3IUkr1ayuGNz1PeEF7dRJT2IlCqVDeBJq1Z+D9w0f07xLNi2+F80kpyWxB5rGxoFDvWRdDcS2ylnCXy9deB7UKgMXeyRW1/TixRbQqOq3vXbRAp/Lr5x3qVXaZnDXfCXGRtg03k9sgAn8qETm4BtClgQ8NsZijj9KQdaB5uEzKDJQ715MQv2IckroHBUPa9O8Z00dG2D5DYjoyA7B141kdBNAxcmf5ZQteioRWGxNs1hOC091IzJZeo3UXc5bwN93JKX5X8lSjNIv4Eg03XNYPxb8WwC/bVC2i4/MHd2yowTfKDQyCoj+Hb1CJkBwHfuZGpBKGmm5W8djpBYfpJyTvEGYXbcw/pETFuLCMl8SrXVcHXbNWobHlEeHkDp0/n4RKKmgBIFrDg08Xas+/BC+5fR2Zlm050UDS4KXgBHG9Nmac53SadkqjtWBEIXGMP0WGJyTjaGR+P7z9udYTaw19yWd4H4QWPQ0fggkMB2Kyq3YDex9VcL/zZ01FppByZGRh1QR4Ps/+BHWNahGb70NCbS8xbd4mzFXQfRAUsE5tVRNJF0swHcYbCaXdKzP2p1bwEmQZeZDgA0LJAi0pDNJAYjU+lw/ncPJLfOKWLWhLEynhHXw7Of9BhHDHSrcbjzPuxj0AZ/6VH3/EYQy6dFBanECgVe4+OUHoFF3bsFvffR1bXqJZa60aTPsUvoQRwDD8o3uSLXPbKK6WlbGNkdS6QEjGZcljUaNB10q2DXuH+fBqS9m3H823njqnSaodN8Gv+hqGHBCX/EUB49K8TAe7sgJCKAHfl+V9/xR5GYr2PsEnvfDmt31PhQuQZyrh0NZwq92AtnETRupEGk/1Q+JJWszdeHcaOp0EI4hRd/6M0+ep/LI1U/rxoldmMcKqpxLbmbfspWI34Q074YFUWOWt3FglAA9xFVpEG9UXKWJT/9kSZ8CwJdlRt2Z6KL6YxFDO3nj3aiWyHJb98By+yJV5arZy7++D++f/opmkHBBpxPjstQDUoDlgOgY6omV4qr2qQuk2C5Sc417q8GkQfDgltd53hgt4iSU4Rg7ejwH8tK2Qc7XmhEwgA6UpFpw+/n2IRAX1yFyyUYdQXm/OZU1U/5x6LaMJNsTu8gIzOsmCuLRbe6zbEr6BFRmr9dDrC+tJHXO+jSxuSgwUUCNLT5wKKBQEaYzi7TwZr0m2xT3jOHP6xoIzgj5eQEpXf7KWh2G1ZK9z6+c8YCGWtLeVsaWzypxqId0l0wbjXh54s2sANtUatfZxxdNSdw==" Status="OK" Source="Amad">
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
                                <TotalFixAmounts Gross="4220.2" Nett="4220.2">
                                    <Service Amount="3794" />
                                    <ServiceTaxes Included="false" Amount="426.2" />
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
                    <FlightResult FareType="PUB" AvailableSeats="7" Number="25" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhnRyb7kxrpnL46R+kzNsTyxpN6r1xok59jLMa0qh6BWhzSKj1K6tDkHd4hEhEViJAULCuGlduCR6R98eAt3Jb3d2b6SCd4yqHtX1DsHJC+FdBSAOe67j6auBd/+mQXUg4MxUBeA0BxxJ8z9NW1L2QJTbeKs+4lamKiHj4A1NiTWpo34dez8KwCuC8nwCTF+7XoN0CDaC5NaZNvRuf1dKC+NfAn1CjpmAwnraPXoO9Q2Z68+xg6BdSIMNG4fpU0E6HXMKxYTMv+EGsdCvEBwNi6sUXATdo4MyMWBifFiWwa3n+xMLq7g+/la+Ez4Y+zQ7HBV/0UV2MLfAnTv4m1Ch64VGrI9ChOWy38DD0Ev8tr7/j+O9pDHJjlJ8xXQw3u1m6ucEAGF5WxhqMMI4x3xuZNsiuszQuG7oQfAGPyk4vpN2J01R41iUdxp9h7BvNOZRLMICFV8ELLNMPcDObmZZJ1ENpMUmtlPs32JEaX5F4LXaWV3Q9KCBWuyZk5RN1BzopwnUaEleeT/SvzG0nik5VY07xmgtdGP8LZZ79T16rmIRRMTrR4Cw6Yhi7/lKSsIGGsMH196nPcgYLfikYyHJku9vtxRXQbQ3qZ2MpGKrFvq5mDOlwByYLWKGloWbowQiSpgjRIerDfGierEmxo7VzzuKsbcMfhL+QOejQymi/un9V/7kCB2rJaKsTxArrZ21pnSlUtxgKUlq1TsQcZ9UcBecECJuVvoPK21jKO+K209LftvEHrpWxRr/UXFEfy8HnK6vZICRwFHIVTzr7R3NUjocMATybVtWMq35KwPnzVplohxzKJRDlIoOUjsrkhVagRzweRFAF4Unh9WLZW7GpaO/47b4KDrMeRRUjDQDyICbuGqSRHGe1jj8lXVU3XuBBqwYfNtLR0mE6ldZwOtQej1M/68+EtqFjQdyYu6mcvUDf3etFWFaBzoecHa2eNJeSk4Lx9h+bf+81OoVyQYcEcguEkQTIDZjP5ifS+a1NRo8oUtH7uddctN7E/POnMssHuUnZqmI8I2ZWExxPStdNkJVXbF3cc/RxDgMoeMX7DOJgqQcaPudO5aUxgU6VjPuFhoxdNGyDFRRqG4+BUK8XCi2VfglwznD5J1j3DkfH5AK7PYx2MpUUVUYd6JGPTZ/Ab8npcoffeuxD2KlQs9U0kkSdS1RnP5P9LDxD5mPNBJO6e9MWj8wr1AJVc0/EzXGv6OKwyyCSAaHvnOAT64cMS5wqIsGUUCFtWIV5sOOvrVofrOzHwfQPTT41xjkuac74WFn1YexnT0LMK9ou+Cr2DDuiVWp6xIOQRuXTxiO+te8w==" Status="OK" Source="Amad">
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
                                <TotalFixAmounts Gross="5605.7" Nett="5605.7">
                                    <Service Amount="5240" />
                                    <ServiceTaxes Included="false" Amount="365.7" />
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
                    <FlightResult FareType="PUB" AvailableSeats="7" Number="26" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhnRyb7kxrpnL46R+kzNsTyxpN6r1xok59jLMa0qh6BWhzSKj1K6tDkHd4hEhEViJAVa3sO0KOFqQWRYrTaXbOwN0OLFzUVo9st+0sl538WUe26bktFs3IqATQk7fAOzp1wSpBtmN35ReDxaJlAiedIHzI5q/OS0EwOAG7+QUiOKgT4YxHxVF4IIGRkmszzgdn9oiY8yut3vOCIFlF45Jubf/zRx+qw4s4adLy3s+5oB+Km9+IEPTUrYzwCmJxzM8zq5ogs2V9zZtICzw3y0VzRWZimnHyfEdhffG94o7aXqxbQzCjKPVtjDGYAq6Cs7wbwOtXj5W+ZB0sZQPR23Y1gij4SXAKTisAxVBZfONwFpKiT2Du50mhP38G67qeUrzbBiyYtS9UojONW+ILOFG+AFO1I4C52d3EGwW/f2P7nvkp2TtUha5nnQOV2NXlvrzHF3qSeiXysqwg4WhmiUHU3QEOwOqB1ULw3vCETp9tt1ua9sc4m9otC15flJMz2n2QiEeUWhAknK+sEAt43lC86QHjHQoXOJ+IBORBJXIh0jnM358LUT/KzOJ/H+DUs0gTd34A4g+0lfWwpCou3TJA2ELJ66Mu9vQEnNIuXwH5iMyknSEgiv/r0JR4ZTtl/hQfxAcySWWMcANvASFMaxkJlHKLn6yWjUTEMSRrE61fUarL1xR9L7pXkLfSXtmPi7Y90OL2hJHwGlNOVFDK+EXTWE0HIlzmcAYidUNtE6Mtx+/AbJVLAbqwEEfzMy9TVWj8/lycvxkO08hhV7DHnkSsDDZsSsKksuWRn+ce09ZsW8TmPMlzdt6RX4/isozVzrkykOuID9ei5d1smuVwI13Kax+6/AbQ/Pw0baEX42Lnd5TtP9xZ/3Q0S76+BFyfP00J3DZB5sEJL9C54QNbJqjWUaZC7H/pVXR/XS+lb9reA7I6hLL9cB5nEIQeUntEmYLsvHtB31ISppXewThM6eVjzkTgkrufUT0nQQSwrWSpN4E5VCC5GeVtCL0C3wR0ysThvXhafMPoKQ33jVdM62JJBbsKlbY570WAqI7xFaPU7ksXhMSpvKbWRfeD6vGBqD5rP8SNOFXfAaA8ZYp5PLD+TgWIjAyZ0T7TINbufzqlxjWrnzMY0Mnb7x7VTLPMXv2JnttyuqHIiKeAAne6AUXD6ufeey8kVMzo0iEyRY2hxipEy+tppVeR7ku1577T2/osKwdW7ofzZK4I3RVyeGkj6AWb9U1dIeycnGQ2HUlDdxM7IsCQPyMmR0rlhpLupTNpwja0yKvzNZs42GS8ck2Epi1LLzqg4YHMxqzsUL7gvSVw==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AY">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="MIA" DepartureDate="2019-10-28T19:35:00" ArrivalDate="2019-10-28T20:46:00" OperatingAirline="AA" MarquetingAirline="AA" FlightNumber="1194" JourneyDuration="P0DT11H45M0S" Class="Y" Cabin="Y" AirplaneType="738" FareBasis="Y1N0C9M1" />
                                    <Segment DepartureAirport="MIA" ArrivalAirport="MAD" DepartureDate="2019-10-28T22:55:00" ArrivalDate="2019-10-29T12:20:00" OperatingAirline="IB" MarquetingAirline="AY" FlightNumber="5642" JourneyDuration="P0DT11H45M0S" Class="Y" Cabin="Y" AirplaneType="333" FareBasis="Y1N0C9M1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="EUR">
                                <TotalFixAmounts Gross="5605.7" Nett="5605.7">
                                    <Service Amount="5240" />
                                    <ServiceTaxes Included="false" Amount="365.7" />
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
                    <FlightResult FareType="PUB" AvailableSeats="7" Number="27" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhnRyb7kxrpnL46R+kzNsTyxOUPlJ1lFNpAI8BHlMnX2kcj8P8SdK8pKMTYAld10bnpYE2+HoKvNT0p8DfmrH9YD31MTVVpT7GWwkd1qvFuBSQwMNDbnF5EnOKB7mVx0d3NrYJfOIjgDoNdcr+2dRkOifC0nLcDLrCMwIZKnJY6XDEe7P9zGIzfv8JVvzk6ADfQ2at1jOAqQZjOQ4ddQN5GzH7y0M0NfdB9wWQOdaNjnm1DdNRtmwmyliII9GAeraKkgKpv5nT7SMdnDyVTa4OeWNHa0kcm7oJmIK0L1zBCpbTFkyudze+S3leCo1el4TOFfV879IdRR+0RuJ7qz+7gtJxreq+7Chvx/8HjY2R8bxMHjp6rmAsb3VTzVHPdCFRJglHVgUIBr9sapUpLKzuoFGlZ9SIT3rYg9WNGCIIMDthYPRGHNY8tjUruWQwWX64BmN6rKS5uqjOu9UnivUKOc76ulnFDU+K30XG2Mi/tGtoD7IoFBpc4ilHCzFtznjgb1ZBxr4ky4dwXFwqqkPjtXNIQVUB9Z7UK2CuaBD2X3PymrSIBdBxsMPjUcZ3rpSGdPMkKLvWZwvrROSxYft4xOKRFLdx5YE1VeTrK2NgxIuTgTYyFi+WCcTnv51mugERjLPDYy7aKn8atD9WLPmocLgbH3DQLP/7zDSpKSLIJVOtqJBr0OfAHdmmfF3GC+9ab2cPQoSoalTQm6glwXtsB/XqPxpWggyP7SS/6WqCJHI1auiSUL/Ne7fN8z6Vi+wh4+OaYmKQoAuQdn9IxQ/4sEGLHuj9Yussi1bN+rtf1OkjrGJEsRFgcpl7T6Sr8VRya0S/S8zUH10cLBGHuMspfiyKwBC1r/nYGHzfb81lprD4VVnel1k8SRjzkDwWMsXN7gL978c1YTm7Og11gSEj6bT15hiFQ9sf8tkX5K9zArmZpgjOIm/UAuzx/bfLCLjowaj/R3DFv5slMu4FwRTnbW3rVOMtt9bwWI7/Ex0cR21vknUQdUwV6pWkywgIrHazJH5bVff6ilzgmsq2ATWND3zXndBej8vbBxWY7j5Hu/fyPQ5n/P3wAfHGYvFVtapMoEdU9Zom6JIFHw76vipsLrjfb+9Qw3ipZEobs2NlQq/lcK/0tZrqBk75KqvYNv/Q2h8Ws0CN775bUrpK2Fde7KAO7F4Bt0MutQVmJAZMDhBLshg5y71/A9L8t3cwToMu2RL/fFBsSQJ994U/4vTm1xd0k1ypvkt1WvTAtlC43BWmvqluZ8IfO5ol2LVsQ87rRMZiIUzYNPKMu8g68+h4ljUQmRl5jqpe+PcEHj4RbwRQ==" Status="OK" Source="Amad">
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
                                <TotalFixAmounts Gross="5629.7" Nett="5629.7">
                                    <Service Amount="5264" />
                                    <ServiceTaxes Included="false" Amount="365.7" />
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
                    <FlightResult FareType="PUB" AvailableSeats="7" Number="28" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhnRyb7kxrpnL46R+kzNsTyxOUPlJ1lFNpAI8BHlMnX2kcj8P8SdK8pKMTYAld10bnqdMcnGL/UAdOPw5/tKNDp6dRCf4V/E7sFAF5M9fIf+CfkA8wOkJ25SjCfM6ppO6jRwtzgQV36arLyEs909tZJvwwMu2omMXU/lpj+ZSCBV1/oidb1ly0yW/u1NzruNRZwj8vZavZluV9Q+RjpIyQarajN5LeQ271/DqH2Amc1emvMcqWMa5/TALwTRH1Oem/MQqSljJeSP+DJqK/RjVTK8eYlhn8EweTQYYcQVtBz2GrdnYeDUd2c1mddvkc52xgoTE++/W11ZjF7oJXwTVNNeYRFj0hoHdSCcp7flGR+cSnI74SKeIrh3vVTskpsQG+w7KXpmEa8N7cNQMfv3poKm2T6ONaG7DIKi/yK6y5AWbynaXC06jHuz0qTGz6+wx77qleGsSYr+syjDwdhZBtCHLzn7JRz2Ca2yUdgREZXxmIiR8WZ95wbNdrQLS1vw66Lyaxvx1LD3tY+Smo4IIsR4LeoumwsTKKgTbkkSreBU18TYWFlMXS9aGynUUK7nkBeNciZt5iZTo8WMRsElthSBAEmTi5h5IifyQV+hd0ejPkkfcYeVEpWHUE1RDbCPspzbxK8bozw/tCA3ACAJh97XR/mMWIC/z3v5MnWyK6ROV+IYANB+z3sCRrWY/qX1x+wLllk6hpYkoQ4aVbztGvAKZ0p5IUzXwooHy5AjQHlc5f4TJfyuU90X62kvGYPT+MNzvKWJBKkyRF210mdWbaINpPomb0FMI0vUhgT4hfxUuKW/wrIEnt8cniW2kbTrMxRhC8YMGtYj1qm89WOMe8jmmYnnjkwtN1wJ/II4yvwc5vtyPQ2qN/lQGGhTLWXmVjcGknCeWkeM+5dfmf2AkgErClbIeXjStBydcVUfg55ca8nMOp7GLVck6uwusKckQ5sAf0c756kEbSZ29jRbDMpbK8/PDoJmS68ytoxAbowly0ZSlLgtwPslAVPzQwpYVPTLT+zadSJm2qVZR7qSpL4ShoIIC+/sgF4v4+eT0vAAwI2m0NsjFHsQTDZMZu1ijXZ/biqDyJo2hNVBqpHa+6s9tRWkMmTn99c3/h8g70F6eAQ+KEIN+b9uE5cL34O2azJ9f673dGTfHEeR08ajMWa80Ozg6FyEHr99y7g1mnkVpWX2pQhu+N4UIFhl3OcpjMJkkrOGbsJvPiIVU/glhfwoqrm9LN0HTd/aoq460MPctnFTQpze36Evn+jUgPUXzMIHVhjDYw/qTL3HcvUwpdKE5mQKh4HdYvVyhngOlWKDVA==" Status="OK" Source="Amad">
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
                                <TotalFixAmounts Gross="5629.7" Nett="5629.7">
                                    <Service Amount="5264" />
                                    <ServiceTaxes Included="false" Amount="365.7" />
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
                    <FlightResult FareType="PUB" AvailableSeats="7" Number="29" Direction="Outbound" LowCost="false" RatePlanCode="yuNWU8Rez1mhN8F02g3W2IsUx7jLMkUloCyKG9cHjhk/bBBgMLZkSC8asYTFPLG7oXcvE4Znpgohcb0clQ89qosUvV/v3cc08vQZjQm4nCQncwjV8+5jPgrYfxKfYtBGqYsW8AlxfC7++PxpJwxeteYmNqgOalBEcvkBVb0Rev0fCHv74lj+B6fv7xt4amciyKofepYPE75L0cHnH7v1+NrWxPc6JkLw2QdHGkTg5GNmJuLib/OAn3Fu6UqMLCNffLFxYel1ZNweNPvgvf8c8DU1bWjdU9zwvqeUtByHM+pGqtG8KvMHvKWAc185bcw16e3AtLXFJAa/c6ZUMz1ibC32+QrI572PT9gRHFiIGgM57It9v3AAYfaPRgjn3DlQ614uSry56r+OVzxRK6DryYtiRGdwdm/h3K3Q9PAYC/a/GFRh1Uvwm2zgs2sCS9Yoq8yigIhRMYQ07+N9820uUdkywTuSPGOjE1gJ5/KSujMZqjoSNthCzk5P24ER5ch6eA10LT9T7/GjYLW1yNZlBFzcSzSf5d9LZC9ArEHBBABT7m/cabiC9KQJjQ3KAFYLMxRPCTA6TAcxg4Wtp4L7nTyEycWfGSDW29nn16P3esoBN7tzvD6RlKrHJuqwd6GXN1FaQhUasYSyzUqhwgt6ErU5GGfB3/FYHFCkD8/BwcwbK5HbUHKCJzTe0bz4BwoTAOWcztqHjV60ofuWfFjZMXO8KPBeR41e8+uwdXHqIOvRdE2OZxi+lS+DED9A409pNXLFXa0y/TutFVHk17h1HVPsizASpL+pcAYTeVh7K1hlaQZzjVAyjxzllknstz5I0k8nhb1DSBMpZkN8wa6pwPbCTbrx49NfTeG74zR5P5CBWVoNDQQz9x1eILa5RtEEqLzHDY4LumYvZ2nyZZ79+0hMMIWc0iEE++D1DLXXZfsgc/CM53xqqc9jGw52xPljV8oA/PZFl+DgIywFbN6YZKXWme+8i7kUPnPymHjYs4559qJut2GvCzVfgQnncI4UBJyGwQB3j6V/8LlfQ6mCq2VXly8KNNtwUFAPc72kr5k0b2OKHdJOiV9GGnKrMgEVk4Ell8knudX7s2huS6cXlzyCpgU1TSJiw3W0VtlZUi9e+h/Bd60HQUdB6el/MYmg6P7xYDiJvAjCRiqDasYouUH6a9xwSeqUfLP4hc9lo10RG/0OtPtmZv+SkywUOFekdtYJc6vKV/aEszTFpY4ER/4HCqFejVqBtJ9M0C1rRB5Ft9xa1DI8LOC6ZkPR8ocAozCPN2R6aAEKLT+1ZgtCmbds4e6nfKrWPtFIp4Qp9do8umnNSz6c1DqpVyeN5qbO" Status="OK" Source="Amad">
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
                                <TotalFixAmounts Gross="5845.54" Nett="5845.54">
                                    <Service Amount="5794" />
                                    <ServiceTaxes Included="false" Amount="51.54" />
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