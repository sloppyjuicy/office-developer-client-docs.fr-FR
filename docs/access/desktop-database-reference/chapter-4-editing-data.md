---
title: 'Chapitre 4 : Modification des données'
TOCTitle: 'Chapter 4: Editing data'
ms:assetid: 822b7365-0926-6411-6fb4-30de032570f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249563(v=office.15)
ms:contentKeyID: 48545974
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b954cf8b730a74fb7e630fbafb96c046491c6f46
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296436"
---
# <a name="chapter-4-editing-data"></a><span data-ttu-id="9eb70-102">Chapitre 4 : Modification des données</span><span class="sxs-lookup"><span data-stu-id="9eb70-102">Chapter 4: Editing data</span></span>

<span data-ttu-id="9eb70-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9eb70-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9eb70-p101">Les deux chapitres précédents ont expliqué comment utiliser ADO pour se connecter à une source de données, exécuter une commande, afficher les résultats dans un objet **Recordset** et naviguer dans le **jeu d'enregistrements**. Ce chapitre traite de la prochaine opération ADO fondamentale : la modification des données.</span><span class="sxs-lookup"><span data-stu-id="9eb70-p101">The preceding two chapters explained how use ADO to connect to a data source, execute a command, get the results in a **Recordset** object, and navigate within the **Recordset**. This chapter focuses on the next fundamental ADO operation: editing data.</span></span>

<span data-ttu-id="9eb70-p102">Ce chapitre continue d'utiliser l'exemple du **jeu d'enregistrements** présenté dans le chapitre 3  avec un changement important. Le code suivant est utilisé pour ouvrir le **jeu d'enregistrements**:</span><span class="sxs-lookup"><span data-stu-id="9eb70-p102">This chapter continues to use the sample **Recordset** introduced in Chapter 3 — with one important change. The following code is used to open the **Recordset**:</span></span>

```vb 
 
 . . . 
'BeginEditIntro 
 Dim strSQL As String 
 Dim objRs1 As ADODB.Recordset 
 
 strSQL = "SELECT * FROM Shippers" 
 
 Set objRs1 = New ADODB.Recordset 
 
 objRs1.Open strSQL, GetNewConnection, adOpenStatic, _ 
 adLockBatchOptimistic, adCmdText 
 
 ' Disconnect the Recordset from the Connection object. 
 Set objRs1.ActiveConnection = Nothing 
'EndEditIntro 
 
 
 . . . 
```

<span data-ttu-id="9eb70-p103">Le changement important du code implique de définir la propriété **CursorLocation** de l'objet **Connection** sur **adUseClient** dans la fonction GetNewConnection (mentionnée ci-après), ce qui indique l'utilisation d'un curseur client. Pour en savoir plus sur les différences entre les curseurs côté client et côté serveur, reportez-vous au [Chapitre 8 : Présentation des curseurs et des verrous](chapter-8-understanding-cursors-and-locks.md).</span><span class="sxs-lookup"><span data-stu-id="9eb70-p103">The important change to the code involves setting the **Connection** object's **CursorLocation** property equal to **adUseClient** in the GetNewConnection function (shown below), which indicates the use of a client cursor. For more information about the differences between client-side and server-side cursors, see [Chapter 8: Understanding Cursors and Locks](chapter-8-understanding-cursors-and-locks.md).</span></span>

<span data-ttu-id="9eb70-p104">Le paramètre **adUseClient** de la propriété **CursorLocation** déplace l'emplacement du curseur de la source de données (dans ce cas, le serveur SQL) vers l'emplacement du code client (la station de travail). Ce paramètre force ADO à invoquer le moteur de curseur client pour OLE DB du client pour créer et gérer le curseur.</span><span class="sxs-lookup"><span data-stu-id="9eb70-p104">The **CursorLocation** property's **adUseClient** setting moves the location of the cursor from the data source (the SQL Server, in this case) to the location of the client code (the desktop workstation). This setting forces ADO to invoke the Client Cursor Engine for OLE DB on the client in order to create and manage the cursor.</span></span>

<span data-ttu-id="9eb70-p105">Vous avez probablement aussi remarqué que le paramètre **LockType** de la méthode **Open** a désormais la valeur **adLockBatchOptimistic**. Ceci permet d'ouvrir le curseur en mode par lots. (Le fournisseur met plusieurs changements en cache et les écrit dans la source de données sous-jacente uniquement lorsque vous utilisez la méthode **UpdateBatch**.) Les modifications apportées au **jeu d'enregistrements** ne sont pas prises en compte dans la base de données tant que la méthode **UpdateBatch** n'est pas invoquée.</span><span class="sxs-lookup"><span data-stu-id="9eb70-p105">You might also have noticed that the **LockType** parameter of the **Open** method changed to **adLockBatchOptimistic**. This opens the cursor in batch mode. (The provider caches multiple changes and writes them to the underlying data source only when you call the **UpdateBatch** method.) Changes made to the **Recordset** will not be updated in the database until the **UpdateBatch** method is called.</span></span>

<span data-ttu-id="9eb70-p106">Enfin, le code de ce chapitre utilise une version modifiée de la fonction GetNewConnection, présentée au chapitre 2. Cette version de la fonction renvoie désormais un curseur côté client. La fonction est représentée comme suit :</span><span class="sxs-lookup"><span data-stu-id="9eb70-p106">Finally, the code in this chapter uses a modified version of the GetNewConnection function, introduced in Chapter 2. This version of the function now returns a client-side cursor. The function looks like this:</span></span>

```vb 
 
'BeginNewConnection 
Public Function GetNewConnection() As ADODB.Connection 
 Dim objConn1 As ADODB.Connection 
 Set objConn1 = New ADODB.Connection 
 
 strConnStr = "Provider=SQLOLEDB;Initial Catalog=Northwind;" & _ 
 "Data Source=MySrvr;Integrated Security=SSPI;" 
 
 objConn1.ConnectionString = strConnStr 
 objConn1.CursorLocation = adUseClient 
 objConn1.Open 
 
 Set GetNewConnection = objConn1 
End Function 
'EndNewConnection 
```

<span data-ttu-id="9eb70-118">Ce chapitre présente les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="9eb70-118">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="9eb70-119">Modification d’enregistrements existants</span><span class="sxs-lookup"><span data-stu-id="9eb70-119">Editing existing records</span></span>](editing-existing-records.md)
- [<span data-ttu-id="9eb70-120">Identification des éléments pris en charge</span><span class="sxs-lookup"><span data-stu-id="9eb70-120">Determining what is supported</span></span>](determining-what-is-supported.md)
- [<span data-ttu-id="9eb70-121">Suppression des enregistrements à l’aide de la méthode Delete</span><span class="sxs-lookup"><span data-stu-id="9eb70-121">Deleting records using the Delete method</span></span>](deleting-records-using-the-delete-method.md)
- [<span data-ttu-id="9eb70-122">Alternatives : utilisation d’SQL instructions</span><span class="sxs-lookup"><span data-stu-id="9eb70-122">Alternatives: using SQL statements</span></span>](alternatives-using-sql-statements.md)
- [<span data-ttu-id="9eb70-123">Ajout d’enregistrements (ADO)</span><span class="sxs-lookup"><span data-stu-id="9eb70-123">Adding records (ADO)</span></span>](adding-records.md)
