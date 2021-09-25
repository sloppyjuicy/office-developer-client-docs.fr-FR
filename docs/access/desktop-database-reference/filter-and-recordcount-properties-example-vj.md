---
title: Filter et RecordCount, propriétés – Exemple (VJ++)
TOCTitle: Filter and RecordCount properties example (VJ++)
ms:assetid: cf062f99-f935-6bf3-a245-fa345ead78db
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250025(v=office.15)
ms:contentKeyID: 48547798
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 6da7bcc8c8ad49346d9d27df33ec20936648ead7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565316"
---
# <a name="filter-and-recordcount-properties-example-vj"></a>Filter et RecordCount, propriétés – Exemple (VJ++)


**S’applique à** : Access 2013, Office 2013

Cet exemple utilise la propriété [Filter](filter-property-ado.md) pour ouvrir un nouveau [Recordset](recordset-object-ado.md) sur base d'une condition spécifiée, appliquée à un objet **Recordset** existant. Il utilise la propriété [RecordCount](recordcount-property-ado.md) pour afficher le nombre d'enregistrements dans les deux **Recordsets**. La fonction FilterField est nécessaire pour que cette procédure soit exécutable.

```java 
 
// BeginFilterJ 
// The WFC class includes the ADO objects. 
 
import com.ms.wfc.data.*; 
import java.io.* ; 
 
public class FilterX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 FilterX(); 
 FilterX2(); 
 System.exit(0); 
 } 
 
 // FilterX function 
 static void FilterX() 
 { 
 
 // Define ADO Objects. 
 Recordset rstPublishers = null; 
 Recordset rstPublishersCountry = null; 
 
 // Declarations. 
 BufferedReader in = 
 new BufferedReader (new InputStreamReader(System.in)); 
 String line = null; 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" 
 + "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 
 int intPublisherCount; 
 String strCountry; 
 String strMessage; 
 
 try 
 { 
 rstPublishers = new Recordset(); 
 
 // Open recordset with data from Publishers table. 
 rstPublishers.setCursorType(AdoEnums.CursorType.STATIC); 
 rstPublishers.open("publishers", strCnn, 
 AdoEnums.CursorType.STATIC, 
 AdoEnums.LockType.READONLY, 
 AdoEnums.CommandType.TABLE); 
 
 // Populate the Recordset. 
 intPublisherCount = rstPublishers.getRecordCount(); 
 
 // Get user input. 
 System.out.println("Enter a country to filter on:"); 
 strCountry = in.readLine().trim(); 
 
 if(!strCountry.equals("")) 
 { 
 // Open a filtered Recordset object. 
 rstPublishersCountry = 
 FilterField(rstPublishers, "Country", strCountry); 
 if(rstPublishersCountry.getRecordCount()==0) 
 System.out.println("\nNo publishers from that country."); 
 else 
 { 
 // Print number of records for the original 
 // Recordset object and the filtered Recordset 
 // object. 
 strMessage = "\nOrders in original recordset: " + "\n" 
 + intPublisherCount + "\n" 
 + "Orders in filtered recordset (Country = '" 
 + strCountry + "'): \n" 
 + rstPublishersCountry.getRecordCount(); 
 System.out.println(strMessage); 
 } 
 rstPublishersCountry.close(); 
 } 
 System.out.println("\n\nPress <Enter> to continue.."); 
 in.readLine(); 
 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // As passing a Recordset, check for null pointer first. 
 if (rstPublishers != null) 
 { 
 PrintProviderError(rstPublishers.getActiveConnection()); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 
 } 
 
 // System read requires this catch. 
 catch( java.io.IOException je) 
 { 
 PrintIOError(je); 
 } 
 
 finally 
 { 
 // Cleanup objects before exit. 
 if (rstPublishers != null) 
 if (rstPublishers.getState() == 1) 
 rstPublishers.close(); 
 } 
 
 } 
 
 // FilterField Function 
 
 static Recordset FilterField(Recordset rstTemp,String strField, 
 String strFilter) 
 { 
 // Set a filter on the specified Recordset object and then 
 // open a new Recordset object. 
 rstTemp.setFilter(strField + " = '" + strFilter + "'"); 
 return rstTemp; 
 } 
 
 // PrintProviderError Function 
 
 static void PrintProviderError( Connection Cnn1 ) 
 { 
 // Print Provider errors from Connection object. 
 // ErrItem is an item object in the Connections Errors collection. 
 com.ms.wfc.data.Error ErrItem = null; 
 long nCount = 0; 
 int i = 0; 
 
 nCount = Cnn1.getErrors().getCount(); 
 
 // If there are any errors in the collection, print them. 
 if( nCount > 0); 
 { 
 // Collection ranges from 0 to nCount - 1 
 for (i = 0; i< nCount; i++) 
 { 
 ErrItem = Cnn1.getErrors().getItem(i); 
 System.out.println("\t Error number: " + ErrItem.getNumber() 
 + "\t" + ErrItem.getDescription() ); 
 } 
 } 
 
 } 
 
 // PrintIOError Function 
 
 static void PrintIOError( java.io.IOException je) 
 { 
 System.out.println("Error \n"); 
 System.out.println("\tSource = " + je.getClass() + "\n"); 
 System.out.println("\tDescription = " + je.getMessage() + "\n"); 
 } 
 
 // FilterX2 function 
 
 static void FilterX2() 
 { 
 
 // Define ADO Objects. 
 Recordset rstPublishers = null; 
 
 // Declarations. 
 BufferedReader in = 
 new BufferedReader (new InputStreamReader(System.in)); 
 String line = null; 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" 
 + "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 
 try 
 { 
 rstPublishers = new Recordset(); 
 
 // Open recordset with data from Publishers table. 
 rstPublishers.setCursorType(AdoEnums.CursorType.STATIC); 
 rstPublishers.open("SELECT * FROM publishers " + 
 "WHERE Country = 'USA'", strCnn, 
 AdoEnums.CursorType.STATIC, 
 AdoEnums.LockType.READONLY, 
 AdoEnums.CommandType.TEXT); 
 
 // Print current data in recordset. 
 rstPublishers.moveFirst(); 
 while(!rstPublishers.getEOF()) 
 { 
 System.out.println(rstPublishers.getField("pub_name").getString() 
 +", " 
 + rstPublishers.getField("country").getString()); 
 rstPublishers.moveNext(); 
 } 
 System.out.println("\n\nPress <Enter> to continue.."); 
 in.readLine(); 
 
 // Cleanup objects before exit. 
 rstPublishers.close(); 
 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // Check for null pointer for connection object. 
 if (rstPublishers.getActiveConnection()==null) 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 else 
 { 
 // As passing a Recordset, check for null pointer first. 
 if (rstPublishers != null) 
 { 
 PrintProviderError(rstPublishers.getActiveConnection()); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 } 
 } 
 
 // System read requires this catch. 
 catch( java.io.IOException je) 
 { 
 PrintIOError(je); 
 } 
 
 } 
} 
// EndFilterJ 
```

