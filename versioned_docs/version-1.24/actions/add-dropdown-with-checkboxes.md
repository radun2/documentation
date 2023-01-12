---
id: add-dropdown-with-checkboxes
title: Add Dropdown with Checkboxes
sidebar_label: Add Dropdown with Checkboxes
---


This action will add a Dropdown with Checkboxes to the specified dynamic container.

## Parameter Reference
| Parameter | Description | Supports Tokens | Default |
| -- | -- | -- | -- |
| Container Id | This is the Container Id to place this Dropdown with Checkboxes into. Eg. Add a Dynamic Field Container having id DynamicFieldContainer. "DynamicFieldContainer" is the ID of the field. Supports Tokens. | No | None |
| Field Id | Required. Give this field an id so you can reference it later. Supports Tokens. | No | None |
| Field Title | Give this field an title/name which is a label. Supports Tokens. | No | None |
| Field Description | Give this field a description. Supports Tokens. | No | None |
| Initial Value | Give this field an initial value. Supports Tokens. | No | None |
| Link To | Link this to another multi-select field that when changed will cause this control to update with different items. For example, imagine Category and Subcategory selection. When this option is used, prefix each item below with the name of the parent category like this: "Value Of Parent Item/This Item"Also, you can input more field IDs separated by comma in order to link this to multiple multi-select fields.Supports Tokens. | No | None |
| Data Source | Required. Choose from existing data sources to bring items from | No | None |
| Tokenize Datasource Parameters | Tokenize the parameters of the datasource when generating the field. (Otherwise the tokenization happens when the initialization process ends.) If you are generating fields using tokens from an 'Execute Actions for each List Entry' the token replacement will happen after all initialization actions so tokens used in datasource parameters (eg. SQL Query with a query containing tokens from current context) might not be replaced correctly. | No | True |
| Count Selections | Checked(input '1' or 'true' - case insensitive) - The input will show the number of selected items. Unchecked(input '0' or 'false' - case insensitive) - The input will show the text of the selected items, separated by comma.Supports Tokens. | No | None |
| Maximum Number of Selections |  If this option is set, the user will be able to select this maximum number of checkboxes.Supports Tokens. | No | None |
| Bind Expression - Show | Dynamically show or hide this field. This must be a boolean expression. Use standard javascript boolean operators (==, !=, &#x3C;,&#x3E; , !). For example, use [PaymentMethod] == &#x27;CreditCard&#x27; to show the credit card field only when the Payment Method is set accordingly. Supports Tokens. | No | None |
| Preserve Layout? | Check this box in order to make sure hiding/showing fields will not affect the layout of the form. | No | None |
| Bind Expression - Value | Dynamically compute the value of this field. So when other fields change this fields updates automatically. Use standard javascript operators where needed (+, -, *, /). For example, use [FirstName] &#x27; &#x27; [LastName] to automatically fill the Display Name field. Note that once the value is edited manually, the automatic synchronization stops. Supports Tokens. | No | None |
| Bind Expression - On Change/Click | Bind some javascript code to execute when the value in this field changes or when a button is clicked. Access the form fields by using syntax [FieldId] which maps to the js object form.fields.FieldId.value. For buttons, you can &#x22;return false;&#x22; to prevent the form from submitting. Supports Tokens. | No | None |
| Tokenize Bind Expressions? | Check this box in order to tokenize the Bind Expressions fields. This is useful when you dynamically compute the id values so you need to tokenize and obtain the real IDs first. | No | None |
| CSS Class | Set CSS classes on the input control. This is appended to the container's UI settings! Supports Tokens. | No | None |
| CSS Styles | Set inline styles on the input control. This is appended to the container's UI settings! Supports Tokens. | No | None |
| Label CSS Class | Set CSS classes on the input label. This is appended to the container's UI settings! Supports Tokens. | No | None |
| Label CSS Styles | Set inline styles on the input label. This is appended to the container's UI settings! Supports Tokens. | No | None |
| Is Required | Specify if this field is required. Supports Tokens. | No | None |
| Validation Condition | This boolean expression is used to determine if this field validation will execute. It supports C# syntax. A common example is [SomeField] == "Some Value" or [SomeField].IndexOf("something") == 0. This field supports Tokens. Note that the tokenization will take place when you submit the form and you have access to the values of the submitted fields. | No | None |
| Custom Validator #1 |  | No | None |
| Custom Validator #2 |  | No | None |
| Tokenize Validators? | Check this box in order to tokenize the Validator fields and the Validation Condition field. This is useful when you need to use tokens for validation at Form Initialization. | No | True |
| Field ID Token Name | Similarly to normal fields, the ID is the name/inputted id sanitized. This means that if you dynamically generate id's, they might contain spaces or other invalid characters. For this, we output the sanitized id of the field. Give a name to this token which holds the sanitized ID. | No | None |