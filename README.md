# How-to-bind-winforms-checkboxadv-to-sql-database

A concise walkthrough to bind the Syncfusion WinForms CheckBoxAdv control to a SQL Server database, including reading and updating a bit/bool field.

## Overview
This sample explains how to:
- Load a boolean/bit value from SQL Server and bind it to CheckBoxAdv
- Support two-state or three-state (Indeterminate) values
- Push user changes back to the database
- Handle DBNull and value mapping scenarios

## Notes on Binding Modes
- Two-state only (true/false):
  - Set ThreeState = false
  - Bind the "Checked" property: `checkBoxAdv.DataBindings.Add("Checked", current, "IsActive", true, DataSourceUpdateMode.OnPropertyChanged);`
- Three-state (true/false/null):
  - Set ThreeState = true
  - Bind the "CheckState" property with a null (DBNull) mapping as shown above

## Troubleshooting
- DBNull issues: Use ThreeState and bind to CheckState with a null mapping.
- Update not saving: Ensure your table has a primary key and that SqlCommandBuilder can generate commands.
- Designer toolbox: Install Syncfusion packages and rebuild the project if controls do not appear.
- Connection failures: Validate the connection string and server accessibility.

## About the sample
This sample describes how to bind Syncfusion WinForms CheckBoxAdv to a SQL database within this sample. Adjust namespaces, package versions, and connection strings based on your environment.
