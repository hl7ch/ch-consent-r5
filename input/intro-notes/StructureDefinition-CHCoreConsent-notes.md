#### Fixed values for Consent types
Each consent type has a fixed value for _category_ and for _provision.purpose_ that makes it uniquely distinguishable from other consent types and searchable by type. <br />
The following list is non-exhaustive:

##### Code Combinations
<table class="grid">
	<tr>
		<th>Consent type</th>
		<th>category</th>
        <th>provision.code</th>
	</tr>
	<tr>
		<td>General Consent</td>
		<td>LOINC | 59284-0</td>
        <td><a href="./CodeSystem-ConsentProvisionCodesCS.html">ConsentProvisionCodesCS</a> | GC</td>
	</tr>
	<tr>
		<td>Patient Portal participation Consent</td>
		<td>LOINC | 64292-6</td>
        <td><a href="./CodeSystem-ConsentProvisionCodesCS.html">ConsentProvisionCodesCS</a> | PATPORTAL</td>
	</tr>
    <tr>
		<td>...</td>
		<td>...</td> 
        <td>...</td>
	</tr>
</table>

#### Search Queries
To retrieve specific types of Consent resources, use the following query pattern:
```
[base]/Consent?patient=<patient id>&category=<system|code>&provision-code=<system|code>
```
**Note:** <br />
The parameter [_provision-code_](./SearchParameter-ConsentProvisionCodeSearch.html) is a custom SearchParameter specifically defined within the CH Core.
