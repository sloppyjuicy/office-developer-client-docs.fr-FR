---
title: AbsolutePosition et CursorLocation, propriétés – Exemple (VJ++)
TOCTitle: AbsolutePosition and CursorLocation properties example (VJ++)
ms:assetid: 38872022-8a65-680f-20af-086e4d9d7b6a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249137(v=office.15)
ms:contentKeyID: 48544223
ms.date: 10/17/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c5ba3f385efeeee7dd90d72970f12550284aafab
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569635"
---
# <a name="absoluteposition-and-cursorlocation-properties-example-vj"></a>AbsolutePosition et CursorLocation, propriétés – Exemple (VJ++)

**S’applique à** : Access 2013, Office 2013

Cet exemple montre comment la propriété [AbsolutePosition](absoluteposition-property-ado.md) peut effectuer un suivi de la progression d'une boucle qui énumère tous les enregistrements d'un objet [Recordset](recordset-object-ado.md). Il utilise la propriété [CursorLocation](cursorlocation-property-ado.md) pour activer la propriété **AbsolutePosition** en définissant le curseur sur un curseur client.

```java 
 
// BeginAboslutePositionJ 
import com.ms.wfc.data.*; 
import java.io.*; 
 
public class AbsolutePositionX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 AbsolutePositionX(); 
 System.exit(0); 
 } 
 
 //.AbsolutePositionX function 
 
 static void AbsolutePositionX() 
 { 
 
 // define ADO Objects. 
 Recordset rstEmployees = null; 
 
 // Declarations. 
 BufferedReader in = 
 new BufferedReader(new InputStreamReader(System.in)); 
 String line = null; 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" + 
 "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 
 String strLName; 
 String strMessage; 
 String strAbsolutePosition,strRecordCount; 
 int intAbsolutePosition; 
 int intRecordCount; 
 int intChoice; 
 
 try 
 { 
 
 rstEmployees = new Recordset(); 
 
 // Use client cursor to enable AbsolutePosition property. 
 rstEmployees.setCursorLocation( AdoEnums.CursorLocation.CLIENT); 
 
 // Open a recordset for Employees table using a client cursor. 
 rstEmployees.open("employee", strCnn, 
 AdoEnums.CursorType.FORWARDONLY , 
 AdoEnums.LockType.READONLY, 
 AdoEnums.CommandType.TABLE); 
 
 // Enumerate Recordset. 
 while ( !rstEmployees.getEOF()) // continuous loop 
 { 
 intRecordCount = rstEmployees.getRecordCount(); 
 strRecordCount = Integer.toString(intRecordCount); 
 
 // Read data field in the variables. 
 strLName = rstEmployees.getField("lname").getString(); 
 intAbsolutePosition = rstEmployees.getAbsolutePosition(); 
 strAbsolutePosition = Integer.toString(intAbsolutePosition); 
 
 // Display current record information. 
 strMessage = "\nEmployee: " + strLName + "\n" + "(Record " + 
 strAbsolutePosition + " of " +strRecordCount + " )"; 
 System.out.println(strMessage); 
 System.out.println( 
 "\nDo you want to continue (1 -> Yes / 2 -> No)?"); 
 //user types a number followed by enter (cr-lf). 
 line = in.readLine().trim(); 
 intChoice = Integer.parseInt(line); 
 if ( intChoice != 1) 
 break; 
 rstEmployees.moveNext(); 
 } 
 } 
 
 catch( NumberFormatException ne) 
 { 
 System.out.println("\nException : Integer Input required."); 
 System.exit(0); 
 } 
 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // Check for null pointer for connection object. 
 if (rstEmployees.getActiveConnection()== null) 
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
 
// EndAbsolutePositionJ 
```

