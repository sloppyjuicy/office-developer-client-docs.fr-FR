---
title: AbsolutePage, PageCount et PageSize, propriétés – Exemple (VJ++)
TOCTitle: AbsolutePage, PageCount, and PageSize properties example (VJ++)
ms:assetid: 6cdf3880-1d77-5826-1d7b-7bf61a886d1b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249431(v=office.15)
ms:contentKeyID: 48545480
ms.date: 10/17/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5564f5549d160bd664059c0c7e00747b9db631f1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586403"
---
# <a name="absolutepage-pagecount-and-pagesize-properties-example-vj"></a>AbsolutePage, PageCount et PageSize, propriétés – Exemple (VJ++)

**S’applique à** : Access 2013, Office 2013

Cet exemple utilise les propriétés [AbsolutePage](absolutepage-property-ado.md), [PageCount](pagecount-property-ado.md) et [PageSize](pagesize-property-ado.md) pour afficher des noms et des dates d’embauche à partir de la table ***Employees***, cinq enregistrements à la fois.

```java 
 
// BeginAbsolutePageJ 
// The WFC class includes the ADO objects. 
 
import com.ms.wfc.data.*; 
import java.io.* ; 
 
public class AbsolutePageX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 AbsolutePageX(); 
 System.exit(0); 
 } 
 
 // AbsolutePageX function 
 
 static void AbsolutePageX() 
 { 
 // Define ADO Objects. 
 Recordset rstEmployees = null; 
 
 // Declarations. 
 BufferedReader in = new BufferedReader (new 
 InputStreamReader(System.in)); 
 String line = null; 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" 
 + "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 
 String strName; 
 String strFName; 
 String strLName; 
 String strHDate; 
 int intPage; 
 int intRecord; 
 
 try 
 { 
 rstEmployees = new Recordset(); 
 
 // Use client cursor to enable AbsolutePosition property. 
 rstEmployees.setCursorLocation( AdoEnums.CursorLocation.CLIENT); 
 
 // Open a recordset using client cursor for the Employees table. 
 rstEmployees.open("employee", strCnn, 
 AdoEnums.CursorType.FORWARDONLY, 
 AdoEnums.LockType.READONLY, 
 AdoEnums.CommandType.TABLE); 
 
 // Display names and hire dates, five records at a time. 
 
 rstEmployees.setPageSize(5); 
 int intPageCount = rstEmployees.getPageCount(); 
 for ( intPage = 1; intPage <= intPageCount; intPage++) 
 { 
 strName = ""; 
 rstEmployees.setAbsolutePage(intPage); 
 for ( intRecord = 1; intRecord <= rstEmployees.getPageSize(); 
 intRecord++) 
 { 
 strFName = rstEmployees.getField("fname").getString(); 
 strLName = rstEmployees.getField("lname").getString(); 
 strHDate = rstEmployees.getField("hire_date").getString(); 
 
 strHDate = strHDate.substring(5,7) + "/" + 
 strHDate.substring(8,10) + 
 "/" + strHDate.substring(2,4); 
 
 strName = strName + "\n" + strFName + " " + strLName + 
 " " + strHDate; 
 rstEmployees.moveNext(); 
 if ( rstEmployees.getEOF()) 
 break; 
 } 
 System.out.println(strName); 
 // Get user input to display next records. 
 
 System.out.println("\n\nPress <Enter> key to Continue."); 
 line = in.readLine(); 
 } 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // Check for null pointer for connection object. 
 if (rstEmployees.getActiveConnection()==null) 
 System.out.println("Exception: " + ae.getMessage()); 
 
 // As passing a Recordset, check for null pointer first. 
 if (rstEmployees != null) 
 { 
 PrintProviderError(rstEmployees.getActiveConnection()); 
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
 if (rstEmployees != null) 
 if (rstEmployees.getState() == 1) 
 rstEmployees.close(); 
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
 
 //.PrintIOError Function 
 
 static void PrintIOError( java.io.IOException je) 
 { 
 System.out.println("Error \n"); 
 System.out.println("\tSource = " + je.getClass() + "\n"); 
 System.out.println("\tDescription = " + je.getMessage() + "\n"); 
 } 
} 
// EndAbsolutePageJ 
```

