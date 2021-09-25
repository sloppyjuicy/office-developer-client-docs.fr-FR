---
title: Value, propriété – Exemple (VJ++)
TOCTitle: Value property example (VJ++)
ms:assetid: 1894c483-f5b0-c83e-35fb-c975ca867fc9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248934(v=office.15)
ms:contentKeyID: 48543474
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 351805bae3dd5c4bf897fefed543ccba27ae1376
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572640"
---
# <a name="value-property-example-vj"></a>Value, propriété – Exemple (VJ++)


**S’applique à** : Access 2013, Office 2013

Cet exemple illustre la propriété [Value](value-property-ado.md) avec les objets [Field](field-object-ado.md) et [Property](property-object-ado.md) en affichant les valeurs de champ et de propriété de la table ***Employees***.

```java 
 
// BeginValueJ 
import java.io.*; 
import com.ms.wfc.data.*; 
import com.ms.com.*; 
 
public class ValueX 
{ 
 // Main Function 
 public static void main (String[] args) 
 { 
 ValueX(); 
 System.exit(0); 
 } 
 static void ValueX() 
 { 
 // Define ADO Objects. 
 Recordset rstEmployees = null; 
 Field fldLoop = null; 
 AdoProperty prpLoop = null; 
 
 // Declarations. 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" + 
 "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 int intLoop; 
 BufferedReader in = new 
 BufferedReader(new InputStreamReader(System.in)); 
 Variant varPropertyValue; 
 String strMessage; 
 
 try 
 { 
 // Open a Recordset with data from Employees table. 
 rstEmployees = new Recordset(); 
 rstEmployees.open("employee", strCnn, 
 AdoEnums.CursorType.FORWARDONLY, AdoEnums.LockType.READONLY, 
 AdoEnums.CommandType.TABLE); 
 
 System.out.println("Field values in rstEmployees\n"); 
 
 // Enumerate the Fields collection of the Employees 
 // table. 
 for(intLoop = 0; 
 intLoop<rstEmployees.getFields().getCount();intLoop++) 
 { 
 fldLoop = rstEmployees.getFields().getItem(intLoop); 
 // Because Value is the default property of a 
 // Field object, the use of the actual keyword 
 // here is optional. 
 System.out.println("\t" + fldLoop.getName() + " = " + 
 fldLoop.getValue()); 
 } 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 System.out.println("Property values in rstEmployees\n"); 
 
 // Enumerate the Properties collection of the 
 // Recordset object. 
 int intCount = 0; 
 for(intLoop = 0; 
 intLoop<rstEmployees.getProperties().getCount();intLoop++) 
 { 
 prpLoop = rstEmployees.getProperties().getItem(intLoop); 
 // Because Value is the default property of a 
 // Field object, the use of the actual keyword 
 // here is optional. 
 strMessage = "\t" + prpLoop.getName() + " = "; 
 varPropertyValue = prpLoop.getValue(); 
 short vttype =varPropertyValue.getvt(); 
 switch (vttype) 
 { 
 case Variant.VariantBoolean : 
 { 
 if (varPropertyValue.getBoolean()) 
 strMessage +="True"; 
 else 
 strMessage +="False"; 
 } 
 break; 
 case Variant.VariantInt : 
 strMessage += varPropertyValue.getInt(); 
 break; 
 default : 
 break; 
 } 
 System.out.println(strMessage); 
 intCount++; 
 // Loop used to display records 
 if (intCount % 15 == 0) 
 { 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 intCount = 0; 
 } 
 
 } 
 // Cleanup objects before exit. 
 rstEmployees.close(); 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 } 
 // System read requires this catch. 
 catch(java.io.IOException je) 
 { 
 PrintIOError(je); 
 } 
 catch(AdoException ae) 
 { 
 // Notify the user of any errors that result from ADO. 
 
 // As passing a recordset, check for null pointer first. 
 if(rstEmployees != null) 
 { 
 PrintProviderError(rstEmployees.getActiveConnection()); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 } 
 
 finally 
 { 
 // Cleanup objects before exit. 
 if (rstEmployees != null) 
 if (rstEmployees.getState() == 1) 
 rstEmployees.close(); 
 } 
 
 } 
 // PrintProviderError Function 
 static void PrintProviderError(Connection cnn1) 
 { 
 // Print Provider Errors from Connection Object. 
 // ErrItem is an item object in the Connections Errors Collection. 
 com.ms.wfc.data.Error ErrItem = null; 
 long nCount = 0; 
 int i = 0; 
 
 nCount = cnn1.getErrors().getCount(); 
 
 // If there are any errors in the collection, print them. 
 if ( nCount > 0) 
 { 
 // Collection ranges from 0 to nCount-1. 
 for ( i=0;i<nCount; i++) 
 { 
 ErrItem = cnn1.getErrors().getItem(i); 
 System.out.println("\t Error Number: " + ErrItem.getNumber() 
 + "\t" + ErrItem.getDescription()); 
 } 
 } 
 } 
 // PrintIOError Function 
 static void PrintIOError(java.io.IOException je) 
 { 
 System.out.println("Error: \n"); 
 System.out.println("\t Source: " + je.getClass() + "\n"); 
 System.out.println("\t Description: "+ je.getMessage() + "\n"); 
 } 
} 
// EndValueJ 
```

