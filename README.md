# Otc.Networking
[![Build Status](https://travis-ci.org/OleConsignado/otc-networking.svg?branch=master)](https://travis-ci.org/OleConsignado/otc-networking)

This package provides a [HttpClientFactory](https://github.com/OleConsignado/otc-networking/blob/master/Source/Otc.Networking.Http.Client.AspNetCore/HttpClientFactory.cs) to create instances of standard [System.Net.HttpClient](https://docs.microsoft.com/dotnet/api/system.net.http.httpclient?view=netframework-4.8) configured to embed HTTP Request Headers with information to track requests between it backend.

|Header Key             | Content |         
|-----------------------|--------------------------------------------------
|X-Root-Correlation-Id |	Identifier of the request starting the flow. |
|X-Correlation-Id       |	Idetifier of the direct consumer request. |
|X-Root-Consumer-Name   | The name of the application (machine/container) starting the flow. |
|X-Consumer-Name	      | The name of the direct consumer. |
|X-Full-Trace	          | Request full track in format “ID1 (NAME1); ID2 (NAME2); ...” |
