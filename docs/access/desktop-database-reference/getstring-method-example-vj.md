---
title: GetString, méthode – Exemple (VJ++)
TOCTitle: GetString method example (VJ++)
ms:assetid: 83d5ab6d-a092-f8ed-81e7-b93922cda93d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249573(v=office.15)
ms:contentKeyID: 48546018
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2601bb4f17306294845180b47716779652673108
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618083"
---
# <a name="getstring-method-example-vj"></a>GetString, méthode – Exemple (VJ++)


**S’applique à** : Access 2013, Office 2013

Cet exemple illustre la méthode [GetString](getstring-method-ado.md).

Supposons que vous déboguez un problème d'accès aux données et que vous sounaitez un moyen rapide et simple d'imprimer le contenu actuel d'un objet [Recordset](recordset-object-ado.md) de petite taille.

```java 
 
// BeginGetStringJ 
// The WFC class includes the ADO objects. 
import com.ms.wfc.data.*; 
import java.io.* ; 
 
public class GetStringX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 GetStringX (); 
 System.exit(0); 
 } 
 
 // GetStringX function 
 static void GetStringX() 
 { 
 // Define ADO Objects. 
 Connection cnConn1 = null; 
 Recordset rstAuthors = null; 
 
 // Declarations. 
 BufferedReader in = 
 new BufferedReader (new InputStreamReader(System.in)); 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" + 
 "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 String strOutput; 
 
 try 
 { 
 // Get the user input for state. 
 System.out.println( 
 "Enter a state (CA, IN, KS, MD, MI, OR, TN, UT): "); 
 String strState = in.readLine().trim(); 
 String strQuery = 
 "SELECT au_fname, au_lname, address, city FROM Authors " + 
 "WHERE state = '" + strState + "'"; 
 
 // Open recordset with data from Authors table. 
 cnConn1 = new Connection(); 
 cnConn1.open(strCnn); 
 rstAuthors = new Recordset(); 
 rstAuthors.open(strQuery, 
 cnConn1, 
 AdoEnums.CursorType.STATIC, 
 AdoEnums.LockType.READONLY, 
 AdoEnums.CommandType.TEXT); 
 
 if (rstAuthors.getRecordCount() > 0) 
 { 
 // Use all defaults: get all rows, TAB column delimiter, 
 // CARRIAGE RETURN 
 // row delimiter, empty-string null delimiter. 
 strOutput = 
 rstAuthors.getString(AdoEnums.StringFormat.CLIPSTRING, 
 rstAuthors.getRecordCount(), 
 "\t ", 
 "\n", 
 "").trim(); 
 System.out.println("\nState = '" + strState + "'" + 
 "\n\n" + 
 "Name Address City" + 
 "\n"); 
 System.out.println(strOutput); 
 } 
 else 
 System.out.println("\nNo rows found for state = '" + 
 strState + "'\n"); 
 
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
 if (cnConn1 != null) 
 if (cnConn1.getState() == 1) 
 cnConn1.close(); 
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
// EndGetStringJ 
```

