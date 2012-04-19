flex-form-generator
===================

Dynamically generate flex form  based on metadata

Generate flex form UI based on class or xml metadata

--- class metadata ---
package model
{
  [Bindable]
	public dynamic class ModelBase
	{
		[Column(name="ID", editable="false")]
		public var id:Number;
		[Column(name="Version", visible="false")]
		public var version:Number;
		[Column(name="Is Active", display="dropdown", validValues="[{label:'yes',value:true},{label:'no',value:false}]")]//JSON for 'VV' (Valid Values)
		public var isActive:Boolean;
		public var lastModifiedDate:Date;

	}
}


--xml metadata ---

<Type id="com.entity.Person" label="Person">
   <Property name="dob" label="Dob" editable="true" required="false" type="Date" nestedType="false" javaType="java.util.Date" /> 
  <Property name="firstName" label="First Name" editable="true" required="false" type="String" nestedType="false" javaType="java.lang.String" /> 
  <Property name="gender" label="Gender" editable="true" required="false" type="char" nestedType="false" javaType="char" /> 
  <Property name="lastName" label="Last Name" editable="true" required="false" type="String" nestedType="false" javaType="java.lang.String" /> 
  <Property name="middleName" label="Middle Name" editable="true" required="false" type="String" nestedType="false" javaType="java.lang.String" /> 
  <Property name="personAddressList" label="Person Address List" editable="true" required="false" type="java.util.List" nestedType="false" javaType="java.util.List" internalType="com.pci.entity.PersonAddress" /> 
  <Property name="personId" label="Person Id" editable="false" required="false" type="Number" nestedType="false" javaType="long" /> 
  <Property name="prefix" label="Prefix" editable="true" required="false" type="String" nestedType="false" javaType="java.lang.String" /> 
  <Property name="ssn" label="SSN" editable="true" required="false" type="String" nestedType="false" javaType="java.lang.String" /> 
  <Property name="suffix" label="Suffix" editable="true" required="false" type="String" nestedType="false" javaType="java.lang.String" /> 
  <Property name="title" label="Title" editable="true" required="false" type="String" nestedType="false" javaType="java.lang.String" /> 
</Type>