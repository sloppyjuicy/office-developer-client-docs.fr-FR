---
title: Données persistantes (référence de base de données du bureau Access)
TOCTitle: Persisting Data
ms:assetid: cb8a32f7-2cdc-26ed-c6d4-dd93c1ac37ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250010(v=office.15)
ms:contentKeyID: 48547715
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fa06693505af6f17cf2282305a9a95d20d068b8f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472107"
---
# <a name="persisting-data"></a><span data-ttu-id="3ad65-102">Données persistantes</span><span class="sxs-lookup"><span data-stu-id="3ad65-102">Persisting Data</span></span>


<span data-ttu-id="3ad65-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3ad65-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3ad65-p101">L'informatique nomade, notamment par l'utilisation d'ordinateurs portables, a généré un besoin d'applications capables d'être exécutées à la fois de manière autonome et en réseau. ADO prend désormais en charge ce phénomène en donnant la possibilité au développeur d'enregistrer un **jeu d'enregistrements** de curseur client sur un disque pour le recharger ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="3ad65-p101">Portable computing (for example, using laptops) has generated the need for applications that can run in both a connected and disconnected state. ADO has added support for this by giving the developer the ability to save a client cursor **Recordset** to disk and reload it later.</span></span>

<span data-ttu-id="3ad65-106">Divers scénarios requièrent l'utilisation de cette fonctionnalité, notamment :</span><span class="sxs-lookup"><span data-stu-id="3ad65-106">There are several scenarios in which you could use this type of feature, including the following:</span></span>

- <span data-ttu-id="3ad65-107">**Déplacements :** lorsque vous vous déplacez avec l'application, il est crucial de pouvoir effectuer des modifications et d'ajouter de nouveaux enregistrements qui peuvent ensuite être soumis à la base de données et validés.</span><span class="sxs-lookup"><span data-stu-id="3ad65-107">**Traveling:** When taking the application on the road, it is vital to supply the ability to make changes and add new records that can then be reconnected to the database later and committed.</span></span>

- <span data-ttu-id="3ad65-p102">**Tables de choix rarement mises à jour :** dans une application, les tables sont souvent utilisées comme des tables de choix  par exemple, les tables de taxes. Elles sont rarement mises à jour et en lecture seule. Au lieu de relire ces données à partir du serveur à chaque démarrage de l'application, cette dernière peut simplement les charger à partir d'un **jeu d'enregistrements** conservé localement.</span><span class="sxs-lookup"><span data-stu-id="3ad65-p102">**Infrequently updated lookups:** Often in an application, tables are used as lookups — for example, state tax tables. They are infrequently updated and are read-only. Instead of rereading this data from the server each time the application is started, the application can simply load the data from a locally persisted **Recordset**.</span></span>

<span data-ttu-id="3ad65-111">Dans ADO, pour enregistrer et charger des **jeux d'enregistrements**, utilisez les méthodes **Recordset.Save** et **Recordset.Open(,,,,adCmdFile)** sur l'objet **Recordset** ADO.</span><span class="sxs-lookup"><span data-stu-id="3ad65-111">In ADO, to save and load **Recordsets**, use the **Recordset.Save** and **Recordset.Open(,,,,adCmdFile)** methods on the ADO **Recordset** object.</span></span>

<span data-ttu-id="3ad65-p103">Vous pouvez utiliser la méthode **Recordset** **Save** pour stocker votre **jeu d'enregistrements** ADO dans un fichier sur un lecteur. (Vous pouvez également enregistrer un **jeu d'enregistrements** sur un objet **Stream** ADO. Les objets **Stream** sont abordés plus loin dans ce guide.) Vous pouvez ensuite utiliser la méthode **Open** pour rouvrir le **jeu d'enregistrements** lorsque vous voulez l'utiliser. Par défaut, ADO enregistre le **jeu d'enregistrements** au format propriétaire Microsoft Advanced Data TableGram (ADTG). Ce format binaire est spécifié à l'aide de la valeur **adPersistADTG** **PersistFormatEnum**. Vous pouvez également choisir d'enregistrer votre **jeu d'enregistrements** au format XML en utilisant **adPersistXML**. Pour en savoir plus sur l'enregistrement des jeux d'enregistrements au format XML, reportez-vous à la rubrique [Enregistrements persistants au format XML](persisting-records-in-xml-format.md).</span><span class="sxs-lookup"><span data-stu-id="3ad65-p103">You can use the **Recordset** **Save** method to persist your ADO **Recordset** to a file on a disk. (You can also save a **Recordset** to an ADO **Stream** object. **Stream** objects are discussed later in the guide.) Later, you can use the **Open** method to reopen the **Recordset** when you are ready to use it. By default, ADO saves the **Recordset** into the proprietary Microsoft Advanced Data TableGram (ADTG) format. This binary format is specified using the **adPersistADTG** **PersistFormatEnum** value. Alternatively, you may choose to save your **Recordset** out as XML instead using **adPersistXML**. For more information about saving Recordsets as XML, see [Persisting Records in XML Format](persisting-records-in-xml-format.md).</span></span>

<span data-ttu-id="3ad65-119">La syntaxe de la méthode **Save** est la suivante :</span><span class="sxs-lookup"><span data-stu-id="3ad65-119">The syntax of the **Save** method is as follows:</span></span>

`recordset.Save Destination, PersistFormat`

<span data-ttu-id="3ad65-p104">La première fois que vous enregistrez le **jeu d’enregistrements**, il n’est pas nécessaire d’indiquer une *destination*. Si vous oubliez la *destination*, un nouveau fichier est créé et nommé selon la valeur de la propriété [Source](source-property-ado-recordset.md) du **jeu d’enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="3ad65-p104">The first time you save the **Recordset**, it is optional to specify *Destination*. If you omit *Destination*, a new file will be created with a name set to the value of the [Source](source-property-ado-recordset.md) property of the **Recordset**.</span></span>

<span data-ttu-id="3ad65-p105">Ne spécifiez pas de *destination* lors des prochaines invocations de **Save** après le premier enregistrement. Dans le cas contraire, une erreur d'exploitation survient. Si vous invoquez **Save** plus tard avec une nouvelle *destination*, le **jeu d'enregistrements** est enregistré dans le nouvel emplacement. Toutefois, cet emplacement et l'emplacement d'origine restent tous les deux ouverts.</span><span class="sxs-lookup"><span data-stu-id="3ad65-p105">Omit *Destination* when you subsequently call **Save** after the first save or a run-time error will occur. If you subsequently call **Save** with a new *Destination*, the **Recordset** is saved to the new destination. However, the new destination and the original destination will both be open.</span></span>

<span data-ttu-id="3ad65-p106">La méthode **Save** ne ferme pas le **jeu d'enregistrements** ni la *destination*. Vous pouvez donc continuer à utiliser le **jeu d'enregistrements** et sauvegarder vos modifications les plus récentes. La *destination* reste ouverte jusqu'à ce que le **jeu d'enregistrements** soit fermé. Pendant ce temps, les autres applications peuvent lire mais pas écrire dans la *destination*.</span><span class="sxs-lookup"><span data-stu-id="3ad65-p106">**Save** does not close the **Recordset** or *Destination*, so you can continue to work with the **Recordset** and save your most recent changes. *Destination* remains open until the **Recordset** is closed, during which time other applications can read but not write to *Destination*.</span></span>

<span data-ttu-id="3ad65-p107">Pour des raisons de sécurité, la méthode **Save** autorise uniquement l'utilisation des paramètres de sécurité faible et personnalisée d'un script exécuté par Microsoft Internet Explorer. Pour une explication plus détaillée des problèmes de sécurité, reportez-vous à l'article (en anglais) « ADO and RDS Security Issues in Microsoft Internet Explorer » dans la rubrique Microsoft Data Access Technical Articles du site MSDN.</span><span class="sxs-lookup"><span data-stu-id="3ad65-p107">For reasons of security, the **Save** method permits only the use of low and custom security settings from a script executed by Microsoft Internet Explorer. For a more detailed explanation of security issues, see "ADO and RDS Security Issues in Microsoft Internet Explorer" under ActiveX Data Objects (ADO) Technical Articles in Microsoft Data Access Technical Articles.</span></span>

<span data-ttu-id="3ad65-129">Si une méthode **Save** est invoquée alors qu'une opération asynchrone de mise à jour, d'exécution ou d'extraction d'un **jeu d'enregistrements** est en cours, la méthode **Save** attend la fin de l'opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="3ad65-129">If the **Save** method is called while an asynchronous **Recordset** fetch, execute, or update operation is in progress, **Save** waits until the asynchronous operation is complete.</span></span>

<span data-ttu-id="3ad65-p108">La sauvegarde des enregistrements s'effectue à partir de la première ligne du **jeu d'enregistrements**. À la fin de la méthode **Save**, la position de ligne active est placée sur la première ligne du **jeu d'enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="3ad65-p108">Records are saved beginning with the first row of the **Recordset**. When the **Save** method is finished, the current row position is moved to the first row of the **Recordset**.</span></span>

<span data-ttu-id="3ad65-p109">Pour obtenir de meilleurs résultats, affectez à la propriété [CursorLocation](cursorlocation-property-ado.md) la valeur **adUseClient** avec la méthode **Save**. Si votre fournisseur ne prend pas en charge toutes les fonctionnalités nécessaires à l'enregistrement des objets **Recordset**, le service de curseur les fournira.</span><span class="sxs-lookup"><span data-stu-id="3ad65-p109">For best results, set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient** with **Save**. If your provider does not support all of the functionality necessary to save **Recordset** objects, the Cursor Service will provide that functionality.</span></span>

<span data-ttu-id="3ad65-134">Lorsqu'un objet **Recordset** est conservé avec la propriété **CursorLocation** affectée de la valeur **adUseServer**, les fonctionnalités de mise à jour de l'objet **Recordset** sont limitées.</span><span class="sxs-lookup"><span data-stu-id="3ad65-134">When a **Recordset** is persisted with the **CursorLocation** property set to **adUseServer**, the update capability for the **Recordset** is limited.</span></span> <span data-ttu-id="3ad65-135">En règle générale, seules les mises à jour de la table unique, des insertions et suppressions sont autorisées (dépendantes de la fonctionnalité du fournisseur).</span><span class="sxs-lookup"><span data-stu-id="3ad65-135">Typically, only single-table updates, insertions, and deletions are allowed (dependent on provider functionality).</span></span> <span data-ttu-id="3ad65-136">La méthode [Resync](resync-method-ado.md) n'est pas non plus disponible avec une telle configuration.</span><span class="sxs-lookup"><span data-stu-id="3ad65-136">The [Resync](resync-method-ado.md) method is also unavailable in this configuration.</span></span>

<span data-ttu-id="3ad65-137">Étant donné que le paramètre *Destination* accepte tout objet qui prend en charge l’interface OLE DB **IStream** , vous pouvez enregistrer un **objet Recordset** directement dans l’objet ASP **Response** .</span><span class="sxs-lookup"><span data-stu-id="3ad65-137">Because the *Destination* parameter can accept any object that supports the OLE DB **IStream** interface, you can save a **Recordset** directly to the ASP **Response** object.</span></span>

<span data-ttu-id="3ad65-138">Dans l'exemple suivant, les méthodes **Save** et **Open** sont utilisées pour conserver un **jeu d'enregistrements** et le rouvrir plus tard :</span><span class="sxs-lookup"><span data-stu-id="3ad65-138">In the following example, the **Save** and **Open** methods are used to persist a **Recordset** and later reopen it:</span></span>

```vb 
 
'BeginPersist 
 conn.ConnectionString = _ 
 "Provider='SQLOLEDB';Data Source='MySqlServer';" _ 
 & "Integrated Security='SSPI';Initial Catalog='pubs'" 
 conn.Open 
 
 conn.Execute "create table testtable (dbkey int " & _ 
 "primary key, field1 char(10))" 
 conn.Execute "insert into testtable values (1, 'string1')" 
 
 Set rst.ActiveConnection = conn 
 rst.CursorLocation = adUseClient 
 
 rst.Open "select * from testtable", conn, adOpenStatic, _ 
 adLockBatchOptimistic 
 
 'Change the row on the client 
 rst!field1 = "NewValue" 
 
 'Save to a file--the .dat extension is an example; choose 
 'your own extension. The changes will be saved in the file 
 'as well as the original data. 
 MyFile = Dir("c:\temp\temptbl.dat") 
 If MyFile <> "" Then 
 Kill "c:\temp\temptbl.dat" 
 End If 
 
 rst.Save "c:\temp\temptbl.dat", adPersistADTG 
 rst.Close 
 Set rst = Nothing 
 
 'Now reload the data from the file 
 Set rst = New ADODB.Recordset 
 rst.Open "c:\temp\temptbl.dat", , adOpenStatic, _ 
 adLockBatchOptimistic, adCmdFile 
 
 Debug.Print "After Loading the file from disk" 
 Debug.Print " Current Edited Value: " & rst!field1.Value 
 Debug.Print " Value Before Editing: " & rst!field1.OriginalValue 
 
 'Note that you can reconnect to a connection and 
 'submit the changes to the data source 
 Set rst.ActiveConnection = conn 
 rst.UpdateBatch 
'EndPersist 
```

