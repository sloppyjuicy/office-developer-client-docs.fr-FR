---
title: Optimize, propriété – Exemple (VJ++)
TOCTitle: Optimize property example (VJ++)
ms:assetid: d4ac9ae3-3304-addf-0292-7af4ed4fdbc2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250067(v=office.15)
ms:contentKeyID: 48547949
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 73000f6611619cf3bb003d05401428ce8976140d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558169"
---
# <a name="optimize-property-example-vj"></a>Optimize, propriété – Exemple (VJ++)


**S’applique à** : Access 2013, Office 2013

Cet exemple illustre la propriété dynamique Optimize des objets [Field](field-object-ado.md). Le champ ***zip** _ de la table _*_Authors_*_ dans la base de données _*_Pubs_*_ n’est pas indexé. La définition [de la](optimize-property-dynamic-ado.md) propriété Optimize sur _ *True** sur le champ **_zip_** autorise ADO à créer un index qui améliore les performances de la [méthode Find.](find-method-ado.md)

```java 
 
// BeginOptimizeJ 
import com.ms.wfc.data.*; 
import java.io.* ; 
 
public class OptimizeX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 OptimizeX(); 
 System.exit(0); 
 } 
 
 // OptimizeX function 
 
 static void OptimizeX() 
 { 
 
 // Define ADO Objects. 
 Recordset rstAuthors = null; 
 
 // Declarations. 
 BufferedReader in = 
 new BufferedReader (new InputStreamReader(System.in)); 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" 
 + "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 
 try 
 { 
 rstAuthors = new Recordset(); 
 rstAuthors.setCursorLocation(AdoEnums.CursorLocation.CLIENT); 
 // Enable index creation. 
 rstAuthors.open("SELECT * FROM Authors", 
 strCnn, 
 AdoEnums.CursorType.STATIC, 
 AdoEnums.LockType.READONLY, 
 AdoEnums.CommandType.TEXT); 
 rstAuthors.getField("zip").getProperties(). 
 getItem("Optimize").setBoolean(true); // Create the index. 
 rstAuthors.find("zip = '94595'"); // Find Akiko Yokomoto. 
 System.out.println(rstAuthors.getField("au_fname").getString() + 
 " " + rstAuthors.getField("au_lname").getString() + " " + 
 rstAuthors.getField("address").getString() + " " + 
 rstAuthors.getField("city").getString() + " " + 
 rstAuthors.getField("state").getString() + " "); 
 rstAuthors.getField("zip").getProperties(). 
 getItem("Optimize").setBoolean(false); // Delete the index. 
 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // As passing a Recordset, check for null pointer first. 
 if (rstAuthors != null) 
 { 
 PrintProviderError(rstAuthors.getActiveConnection()); 
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
 if (rstAuthors != null) 
 if (rstAuthors.getState() == 1) 
 rstAuthors.close(); 
 } 
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
} 
// EndOptimizeJ 
```

