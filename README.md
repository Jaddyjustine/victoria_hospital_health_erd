# victoria_hospital_health_erd
<mxfile>
  <diagram name="ERD - Health Facility Database">
    <mxGraphModel dx="1780" dy="1350" grid="1" gridSize="10" guides="1" tooltips="1" connect="1" arrows="1" fold="1" page="1" pageScale="1" pageWidth="850" pageHeight="1100" math="0" shadow="0">
      <root>
        <mxCell id="0" />
        <mxCell id="1" parent="0" />

        <!-- Malaria Cases by Region Table -->
        <mxCell id="malaria_cases" value="Malaria_Cases_by_Region\nCase_ID (PK)\nRegion\nYear\nNumber_of_Cases" style="swimlane" vertex="1" parent="1">
          <mxGeometry x="50" y="50" width="160" height="100" as="geometry" />
        </mxCell>

        <!-- User Table -->
        <mxCell id="user" value="User\nUser_ID (PK)\nRole_ID (FK)\nFirst_Name\nLast_Name\nPassword\nUpdate_Date" style="swimlane" vertex="1" parent="1">
          <mxGeometry x="250" y="50" width="160" height="120" as="geometry" />
        </mxCell>

        <!-- User Role Table -->
        <mxCell id="user_role" value="User_Role\nRole_ID (PK)\nRole_Name\nDescription\nDate_Added" style="swimlane" vertex="1" parent="1">
          <mxGeometry x="50" y="200" width="160" height="100" as="geometry" />
        </mxCell>

        <!-- Patient Data Table -->
        <mxCell id="patient_data" value="Patient_Data\nPatient_ID (PK)\nFirst_Name\nLast_Name\nDate_of_Birth\nGender\nPhone_Number\nAddress\nUpdate_Date" style="swimlane" vertex="1" parent="1">
          <mxGeometry x="250" y="200" width="180" height="140" as="geometry" />
        </mxCell>

        <!-- Visit Record Table -->
        <mxCell id="visit_record" value="Visit_Record\nVisit_ID (PK)\nPatient_ID (FK)\nFacility_ID (FK)\nDate_of_Visit\nReason_for_Visit\nUpdate_Date" style="swimlane" vertex="1" parent="1">
          <mxGeometry x="500" y="200" width="200" height="120" as="geometry" />
        </mxCell>

        <!-- Health Facility Table -->
        <mxCell id="health_facility" value="Health_Facility\nFacility_ID (PK)\nFacility_Name\nLocation_ID (FK)\nFacility_Type_ID (FK)\nUpdate_Date" style="swimlane" vertex="1" parent="1">
          <mxGeometry x="750" y="200" width="200" height="120" as="geometry" />
        </mxCell>

        <!-- Geographical Location Table -->
        <mxCell id="geographical_location" value="Geographical_Location\nLocation_ID (PK)\nVillage\nParish\nCounty\nSubcounty\nDistrict\nRegion\nLatitude\nLongitude\nITN_Coverage\nReported_Cases" style="swimlane" vertex="1" parent="1">
          <mxGeometry x="1050" y="50" width="200" height="180" as="geometry" />
        </mxCell>

        <!-- Relationships -->
        <mxCell id="rel1" edge="1" source="user_role" target="user">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="rel2" edge="1" source="patient_data" target="visit_record">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="rel3" edge="1" source="visit_record" target="health_facility">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="rel4" edge="1" source="geographical_location" target="health_facility">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
      </root>
    </mxGraphModel>
  </diagram>
</mxfile>
