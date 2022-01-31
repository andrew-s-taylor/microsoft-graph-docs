---
description: "Automatically generated file. DO NOT MODIFY"
---

```powershell

Import-Module Microsoft.Graph.Education

$params = @{
	DisplayName = "Dion Matheson"
	GivenName = "Dion"
	MiddleName = $null
	Surname = "Matheson"
	Mail = "DionM@contoso.com"
	MobilePhone = "+1 (253) 555-0101"
	CreatedBy = @{
		User = @{
			DisplayName = "Susana Rocha"
			Id = "14012"
		}
	}
	ExternalSource = "sis"
	MailingAddress = @{
		City = "Los Angeles"
		CountryOrRegion = "United States"
		PostalCode = "98055"
		State = "CA"
		Street = "12345 Main St."
	}
	PrimaryRole = "student"
	ResidenceAddress = @{
		City = "Los Angeles"
		CountryOrRegion = "United States"
		PostalCode = "98055"
		State = "CA"
		Street = "12345 Main St."
	}
}

New-MgEducationUser -BodyParameter $params

```