# OData Service Creation using CDS View with `@OData.publish: true`

## 1. Define the CDS View in Eclipse 📋

- Create or open your CDS view (ex. `ZDD_EXEMPLO`).
- Add the following annotation to expose the view as an OData service:
   ```abap
   @OData.publish: true

- Activate the CDS view.

## 2. Register the OData Service ⚙️
Open SAP GUI and run the following transaction:

**Copiar código**
```abap
/IWFND/MAINT_SERVICE
```


**Add the Service:**

- Click on Add Service in the toolbar.
- Select the System Alias where the service will be published.
- Search for the service name based on your CDS View (ZDD_WORKFLOW_CDS).
- Select the service from the search results.
- Click Add Selected Services.
**Assign the Service:**

- Choose a Package or Local Object (if it’s a test service).
- Confirm the registration by saving.

## 3. Test the OData Service 🛠️
Open the Gateway Client by running the following transaction:

```abap
/IWFND/GW_CLIENT
```
Enter the Service URL:

**Use the following format:**
```abap
/sap/opu/odata/sap/ZDD_WORKFLOW_CDS/
```
**Select the HTTP Method:**

Choose GET for testing the data retrieval. </br>
**Execute the Request:**

Click Execute and review the response.
Verify the service response in the Response Body section to ensure the service works as expected.


## 4. Expose the OData Service to External Systems 🔩
**Share the Service URL with consumers:**
```abap
/sap/opu/odata/sap/ZDD_WORKFLOW_CDS/
```
- Ensure to copy the proper protocol.
- Be tuned, the URL to be copy it's inside the tags and order following:
  <atom:link href="" rel="latest-version"/></br></br>
**Example for localization**</br>
![image](https://github.com/user-attachments/assets/b983fbd1-81bc-4b4f-993f-9250297db653)
</br>

### 5. Excel OData Consume

**Step to Access:**
Open an Excel file and follow the steps:
- Data
- Get Data
- From Other Sources
- From OData Feed</br>

![image](https://github.com/user-attachments/assets/19701e29-600a-4fd6-aa16-7e80b0172c87)</br>

**Example of display:**</br>

![image](https://github.com/user-attachments/assets/e1553f6f-de78-4b86-a9f0-9aace552ede2)

