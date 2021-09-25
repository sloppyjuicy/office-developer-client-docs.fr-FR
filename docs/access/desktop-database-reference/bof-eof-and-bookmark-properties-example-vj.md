---
title: BOF, EOF et Bookmark, propriétés – Exemple (VJ++)
TOCTitle: BOF, EOF, and Bookmark properties example (VJ++)
ms:assetid: 68e6fcc5-506a-9064-3e7c-9ce3d64371aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249412(v=office.15)
ms:contentKeyID: 48545400
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5ba975fa75495a66260acd01f38ede60b92091ba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602940"
---
# <a name="bof-eof-and-bookmark-properties-example-vj"></a>BOF, EOF et Bookmark, propriétés – Exemple (VJ++)


**S’applique à** : Access 2013, Office 2013

Cet exemple utilise les propriétés [BOF](bof-eof-properties-ado.md) et [EOF](bof-eof-properties-ado.md) pour afficher un message si un utilisateur tente d'aller au-delà du premier ou du dernier enregistrement d'un objet [Recordset](recordset-object-ado.md). Il utilise la propriété [Bookmark](bookmark-property-ado.md) pour permettre à l'utilisateur de marquer un enregistrement dans un objet **Recordset** et d'y revenir ultérieurement.

```java 
 
// BeginBOFEOFJ 
import com.ms.wfc.data.*; 
import java.io.*; 
import com.ms.com.*; 
 
public class BOFEOFBookmark 
{ 
 Variant varBookmark; 
 BufferedReader in = 
 new BufferedReader(new InputStreamReader(System.in)); 
 String line = null; 
 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 BOFEOFBookmark b1 = new BOFEOFBookmark (); 
 b1.BOFX(); 
 b1.BOFX2(); 
 System.exit(0); 
 try 
 { 
 b1.finalize(); 
 } 
 catch(Throwable te) 
 { 
 System.out.println("Exception: " + te.getMessage()); 
 } 
 } 
 
 // The main entry point for the application. 
 
 public void BOFX() 
 { 
 // Declarations. 
 Recordset rstPublishers = null; 
 String strCnn; 
 String strMessage; 
 int intCommand = 0; 
 
 strCnn = "Provider='sqloledb';Data Source='MySqlServer';" 
 + "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 try 
 { 
 // Open a recordset with data from Publishers table. 
 rstPublishers = new Recordset(); 
 rstPublishers.setCursorType(AdoEnums.CursorType.STATIC ); 
 rstPublishers.setCursorLocation( 
 AdoEnums.CursorLocation.CLIENT); 
 
 // Use client cursor to enable AbsolutePosition property. 
 
 rstPublishers.open(new String( 
 "SELECT pub_id,pub_name FROM Publishers ORDER BY pub_name"), 
 strCnn, AdoEnums.CursorType.STATIC , 
 AdoEnums.LockType.BATCHOPTIMISTIC, 
 AdoEnums.CommandType.TEXT ); 
 rstPublishers.moveFirst(); 
 
 //Display information about current record and get user input. 
 while ( true) 
 { 
 strMessage = "\nPublisher :" + 
 rstPublishers.getField("pub_name").getString() + "\n" 
 + " (Record " + rstPublishers.getAbsolutePosition() 
 + " of " + rstPublishers.getRecordCount() + ")" + "\n\n" 
 + "Enter command : " + "\n" 
 + "[1 - next / 2 - previous /" + "\n" 
 + "3 - set bookmark / 4 - go to bookmark] / 5 - quit]" ; 
 System.out.println (strMessage); 
 line = in.readLine(); 
 //No entry exits loop. 
 if (line.length() == 0) 
 break; 
 //convert string entry to int. 
 intCommand = Integer.parseInt(line); 
 //out of range entry exits loop. 
 if ((intCommand < 1) || (intCommand > 4)) break ; 
 
 //Call method based on user's validated selection. 
 MoveAny(intCommand, rstPublishers); 
 } 
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
 
 // This catch is required if input string cannot be converted to 
 // Integer data type. "TCS[VSD]" 
 
 catch ( java.lang.NumberFormatException ne) 
 { 
 System.out.println("\nException: Integer Input required." ); 
 } 
 
 // System Read requires this catch. 
 catch( java.io.IOException je ) 
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
 
 // MoveAny Function 
 
 public void MoveAny(int intChoice, Recordset rsTemp) 
 { 
 // Move Forward or backword per selection from user, 
 // trapping for BOF and EOF. 
 try 
 { 
 switch(intChoice) 
 { 
 case 1: // Equals char of 1. 
 rsTemp.moveNext(); 
 if (rsTemp.getEOF()) 
 { 
 System.out.println ( 
 "\nMoving past the last record \nTry again." ); 
 rsTemp.moveLast(); 
 } 
 break; 
 case 2: // Equals char of 2. 
 rsTemp.movePrevious(); 
 if (rsTemp.getBOF()) 
 { 
 System.out.println ( 
 "\nMoving past the first record \nTry again." ); 
 rsTemp.moveFirst(); 
 } 
 break; 
 case 3: // Equals char of 3. 
 // Store the bookmark of the current record. 
 varBookmark = (Variant)rsTemp.getBookmark(); 
 break; 
 case 4: // Equals char of 4. 
 // Go to the record indicated by the stored bookmark. 
 if (varBookmark == null) 
 System.out.println ("\nNo bookmark set!"); 
 else 
 rsTemp.setBookmark((Object)varBookmark); 
 break; 
 default: 
 break; 
 } 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // As passing a Recordset, check for null pointer first. 
 if (rsTemp != null) 
 { 
 PrintProviderError(rsTemp.getActiveConnection()); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
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
 
 //////////////////////////////////////////// 
 // BOFX2() Function. // 
 //////////////////////////////////////////// 
 
 public void BOFX2() 
 { 
 Recordset rs = null ; 
 
 try 
 { 
 // Declarations. 
 rs = new Recordset(); 
 Variant[] arrbmk = new Variant[11]; 
 rs.setCursorLocation( AdoEnums.CursorLocation.CLIENT); 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" 
 + "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 rs.setActiveConnection (strCnn); 
 // Open recorset with data from authors table. 
 rs.open((new String("SELECT * FROM authors")),strCnn,AdoEnums.CursorType.STATIC ,AdoEnums.LockType.BATCHOPTIMISTIC,AdoEnums.CommandType.TEXT ); 
 System.out.println ("\nNumber of records before filtering : " + rs.getRecordCount() ); 
 int ii = 0; 
 
 // Create array of bookmarks. 
 while (rs.getEOF() != true && ii < 11) 
 { 
 arrbmk[ii] = (Variant)rs.getBookmark(); 
 ii++; 
 rs.move (2); 
 } 
 
 // set Filter to recordset. 
 Variant bmk=new Variant(); 
 bmk.putVariantArray(arrbmk); 
 rs.setFilter(bmk); 
 System.out.println ("\nNumber of records after filtering : " + rs.getRecordCount() ); 
 
 // Dislay the records after filtering. 
 rs.moveFirst(); 
 while (!rs.getEOF()) 
 { 
 System.out.println ("\t" +rs.getAbsolutePosition() + " " +rs.getField("au_lname").getString()); 
 rs.moveNext(); 
 } 
 rs.close(); 
 System.out.println ("\n\nPress <Enter> key to continue."); 
 in.readLine(); 
 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // As passing a Recordset, check for null pointer first. 
 if (rs != null) 
 { 
 PrintProviderError(rs.getActiveConnection()); 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 } 
 // System Read requires this catch. 
 catch( java.io.IOException je ) 
 { 
 PrintIOError(je); 
 } 
 } 
} 
 
 
// EndBOFEOFJ 
```

