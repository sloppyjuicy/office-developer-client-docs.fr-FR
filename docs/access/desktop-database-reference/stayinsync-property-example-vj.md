---
<span data-ttu-id="262b9-101"><<<<<<< Titre tête : TOCTitle StayInSync, propriété-Exemple (VJ ++) : StayInSync, propriété-Exemple (VJ ++) === titre : StayInSync, propriété-Exemple (VJ ++) TOCTitle : StayInSync, propriété-Exemple (VJ ++)</span><span class="sxs-lookup"><span data-stu-id="262b9-101"><<<<<<< HEAD title: StayInSync Property Example (VJ++) TOCTitle: StayInSync Property Example (VJ++) ======= title: StayInSync property example (VJ++) TOCTitle: StayInSync property example (VJ++)</span></span>
>>>>>>> <span data-ttu-id="262b9-102">Master ms:assetid : e9e0fcc7-07b6-c433-7c4c-478fc69eacaf ms:mtpsurl : https://msdn.microsoft.com/library/JJ250184(v=office.15) ms:contentKeyID : ms.date 48548448 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="262b9-102">master ms:assetid: e9e0fcc7-07b6-c433-7c4c-478fc69eacaf ms:mtpsurl: https://msdn.microsoft.com/library/JJ250184(v=office.15) ms:contentKeyID: 48548448 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="262b9-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="262b9-103"><<<<<<< HEAD</span></span>
# <a name="stayinsync-property-example-vj"></a><span data-ttu-id="262b9-104">StayInSync, propriété - Exemple (VJ++)</span><span class="sxs-lookup"><span data-stu-id="262b9-104">StayInSync Property Example (VJ++)</span></span>
=======
# <a name="stayinsync-property-example-vj"></a><span data-ttu-id="262b9-105">StayInSync, propriété-Exemple (VJ ++)</span><span class="sxs-lookup"><span data-stu-id="262b9-105">StayInSync property example (VJ++)</span></span>
>>>>>>> <span data-ttu-id="262b9-106">master</span><span class="sxs-lookup"><span data-stu-id="262b9-106">master</span></span>


<span data-ttu-id="262b9-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="262b9-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="262b9-108">Cet exemple montre comment la propriété [StayInSync](stayinsync-property-ado.md) facilite l'accès aux lignes d'un objet [Recordset](recordset-object-ado.md) hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="262b9-108">This example demonstrates how the [StayInSync](stayinsync-property-ado.md) property facilitates accessing rows in a hierarchical [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="262b9-p101">La boucle externe affiche le nom et le prénom, l'état et l'identification de chaque auteur. Le **Recordset** ajouté pour chaque ligne est extrait de la collection [Fields](fields-collection-ado.md) et automatiquement attribué à **rstTitleAuthor** par la propriété **StayInSync** chaque fois que le parent **Recordset** change de ligne. La boucle interne affiche quatre champs de chaque ligne dans le jeu d'enregistrements ajouté.</span><span class="sxs-lookup"><span data-stu-id="262b9-p101">The outer loop displays each author's first and last name, state, and identification. The appended **Recordset** for each row is retrieved from the [Fields](fields-collection-ado.md) collection and automatically assigned to **rstTitleAuthor** by the **StayInSync** property whenever the parent **Recordset** moves to a new row. The inner loop displays four fields from each row in the appended recordset.</span></span>

```java 
 
// BeginStayInSyncJ 
import com.ms.wfc.data.*; 
import java.io.* ; 
import com.ms.com.*; 
 
public class StayInSyncX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 StayInSyncX(); 
 System.exit(0); 
 } 
 
 // StayInSyncX function 
 
 static void StayInSyncX() 
 { 
 
 // Define ADO Objects. 
 Connection cnConn1 = null; 
 Recordset rstAuthors = null; 
 Recordset rstTitleAuthor = null; 
 
 // Declarations. 
 BufferedReader in = new 
 BufferedReader (new InputStreamReader(System.in)); 
 String strCnn = "Provider=MSDataShape;" + 
 "Data Provider='sqloledb';Data Source='MySqlServer';" + 
 "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 
 
 try 
 { 
 cnConn1 = new Connection(); 
 cnConn1.open(strCnn); 
 rstAuthors = new Recordset(); 
 rstAuthors.setStayInSync(true); 
 rstAuthors.open("SHAPE {select * from Authors} " + 
 "APPEND ({select * from titleauthor}" + 
 "RELATE au_id TO au_id) AS chapTitleAuthor", 
 cnConn1, 
 AdoEnums.CursorType.STATIC, 
 AdoEnums.LockType.READONLY, 
 AdoEnums.CommandType.TEXT); 
 
 Variant varRstTitleAuthor = rstAuthors.getFields(). 
 getItem("chapTitleAuthor").getValue(); 
 rstTitleAuthor =new Recordset(varRstTitleAuthor.toObject()); 
 int intCount =0; 
 while(!rstAuthors.getEOF()) 
 { 
 System.out.println("\n" + 
 rstAuthors.getField("au_fname").getString() + " " + 
 rstAuthors.getField("au_lname").getString() + " " + 
 rstAuthors.getField("state").getString() + " " + 
 rstAuthors.getField("au_id").getString()); 
 while(!rstTitleAuthor.getEOF()) 
 { 
 System.out.println(rstTitleAuthor.getField(0). 
 getString() + " " + 
 rstTitleAuthor.getField(1).getString() + " " + 
 rstTitleAuthor.getField(2).getString() + " " + 
 rstTitleAuthor.getField(3).getString()); 
 rstTitleAuthor.moveNext(); 
 } 
 if(++intCount % 5 == 0) 
 { 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 } 
 rstAuthors.moveNext(); 
 } 
 
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
 if (rstTitleAuthor != null) 
 if (rstTitleAuthor.getState() == 1) 
 rstTitleAuthor.close(); 
 if (rstAuthors != null) 
 if (rstAuthors.getState() == 1) 
 rstAuthors.close(); 
 if (cnConn1 != null) 
 if (cnConn1.getState() == 1) 
 cnConn1.close(); 
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
// EndStayInSyncJ 
```

