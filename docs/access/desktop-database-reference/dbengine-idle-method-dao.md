---
title: Méthode DBEngine.Idle (DAO)
TOCTitle: Idle Method
ms:assetid: c90b565e-626e-139d-102a-0386601ce0c8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823202(v=office.15)
ms:contentKeyID: 48547666
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052978
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 68c0e6d246370f9c4f0c241195fb19c241ca49e5
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949718"
---
# <a name="dbengineidle-method-dao"></a><span data-ttu-id="b63ba-102">Méthode DBEngine.Idle (DAO)</span><span class="sxs-lookup"><span data-stu-id="b63ba-102">DBEngine.Idle method (DAO)</span></span>

<span data-ttu-id="b63ba-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b63ba-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b63ba-104">Suspend le traitement des données, ce qui permet au moteur de base de données Microsoft Access de terminer les tâches en cours, telles que l'optimisation de la mémoire ou les expirations de délai des pages (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="b63ba-104">Suspends data processing, enabling the Microsoft Access database engine to complete any pending tasks, such as memory optimization or page timeouts (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="b63ba-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b63ba-105">Syntax</span></span>

<span data-ttu-id="b63ba-106">*expression* . Inactivité (***Action***)</span><span class="sxs-lookup"><span data-stu-id="b63ba-106">*expression* .Idle(***Action***)</span></span>

<span data-ttu-id="b63ba-107">*expression* Variable qui représente un objet **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="b63ba-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="b63ba-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b63ba-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b63ba-109">Name</span><span class="sxs-lookup"><span data-stu-id="b63ba-109">Name</span></span></p></th>
<th><p><span data-ttu-id="b63ba-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="b63ba-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="b63ba-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="b63ba-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="b63ba-112">Description</span><span class="sxs-lookup"><span data-stu-id="b63ba-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b63ba-113"><em>Action</em></span><span class="sxs-lookup"><span data-stu-id="b63ba-113"><em>Action</em></span></span></p></td>
<td><p><span data-ttu-id="b63ba-114">Facultatif</span><span class="sxs-lookup"><span data-stu-id="b63ba-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="b63ba-115"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="b63ba-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b63ba-p101">Spécifie l’action à effectuer. Il peut s’agir de l’une des constantes <strong><a href="idleenum-enumeration-dao.md">IdleEnum</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="b63ba-p101">Specifies the action to take. Can be one of the <strong><a href="idleenum-enumeration-dao.md">IdleEnum</a></strong> constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b63ba-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="b63ba-118">Remarks</span></span>

<span data-ttu-id="b63ba-p102">La méthode **Idle** permet au moteur de base de données Microsoft Access d'effectuer des tâches en arrière-plan qui peuvent ne pas être à jour en raison de l'intensité du traitement des données. Cela est souvent le cas dans les environnements multi-utilisateur et multitâches qui ne disposent pas d'un délai de traitement en arrière-plan suffisant pour tenir à jour tous les enregistrements d'un objet **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="b63ba-p102">The **Idle** method allows the Microsoft Access database engine to perform background tasks that may not be up-to-date because of intense data processing. This is often true in multiuser, multitasking environments that don't have enough background processing time to keep all records in a **[Recordset](recordset-object-dao.md)** current.</span></span>

<span data-ttu-id="b63ba-p103">Habituellement, les verrous en lecture sont supprimés et les données présentes dans les objets **Recordset** de type feuille de réponse dynamique ne sont mises à jour qu'à partir du moment où aucune autre action (y compris les déplacements de souris) ne se produit. Si vous utilisez périodiquement la méthode **Idle**, le moteur de base de données Microsoft Access peut se consacrer au traitement des tâches en arrière-plan en supprimant les verrous en lecture inutiles.</span><span class="sxs-lookup"><span data-stu-id="b63ba-p103">Usually, read locks are removed and data in local dynaset-type **Recordset** objects are updated only when no other actions (including mouse movements) occur. If you periodically use the **Idle** method, the Microsoft Access database engine can catch up on background processing tasks by releasing unneeded read locks.</span></span>

<span data-ttu-id="b63ba-123">Une fois spécifié, l'argument facultatif **dbRefreshCache** actualise la mémoire à partir uniquement des données de la base de données les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="b63ba-123">Specifying the optional **dbRefreshCache** argument refreshes memory with only the most current data from the database.</span></span>

<span data-ttu-id="b63ba-p104">Vous n'avez pas besoin d'utiliser cette méthode dans les environnements mono-utilisateur à moins que plusieurs instances d'une même application soient exécutées. La méthode **Idle** est propre à accroître les performances dans un environnement mono-utilisateur dans la mesure où elle force le moteur de base de données à écrire les données sur disque, ce qui supprime les verrous au niveau de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="b63ba-p104">You don't need to use this method in single-user environments unless multiple instances of an application are running. The **Idle** method may increase performance in a multiuser environment because it forces the database engine to write data to disk, releasing locks on memory.</span></span>


> [!NOTE]
> <span data-ttu-id="b63ba-126">[!REMARQUE] Vous pouvez également supprimer les verrous en lecture en intégrant les opérations à une transaction.</span><span class="sxs-lookup"><span data-stu-id="b63ba-126">You can also release read locks by making operations part of a transaction.</span></span>

## <a name="example"></a><span data-ttu-id="b63ba-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="b63ba-127">Example</span></span>

<span data-ttu-id="b63ba-p105">Cet exemple de code montre comment utiliser la méthode **Idle** pour s'assurer qu'une procédure de sortie accède aux données les plus récentes à disposition dans la base de données. La procédure IdleOutput est nécessaire à l'exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="b63ba-p105">This example uses the **Idle** method to ensure that an output procedure is accessing the most current data available from the database. The IdleOutput procedure is required for this procedure to run.</span></span>

```vb 
Sub IdleX() 
 
 Dim dbsNorthwind As Database 
 Dim strCountry As String 
 Dim strSQL As String 
 Dim rstOrders As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 ' Get name of country from user and build SQL statement 
 ' with it. 
 strCountry = Trim(InputBox("Enter country:")) 
 strSQL = "SELECT * FROM Orders WHERE ShipCountry = '" & _ 
 strCountry & "' ORDER BY OrderID" 
 
 ' Open Recordset object with SQL statement. 
 Set rstOrders = dbsNorthwind.OpenRecordset(strSQL) 
 
 ' Display contents of Recordset object. 
 IdleOutput rstOrders, strCountry 
 
 rstOrders.Close 
 dbsNorthwind.Close 
 
End Sub 
 
Sub IdleOutput(rstTemp As Recordset, strTemp As String) 
 
 ' Call the Idle method to release unneeded locks, force 
 ' pending writes, and refresh the memory with the current 
 ' data in the .mdb file. 
 DBEngine.Idle dbRefreshCache 
 
 ' Enumerate the Recordset object. 
 With rstTemp 
 Debug.Print "Orders from " & strTemp & ":" 
 Debug.Print , "OrderID", "CustomerID", "OrderDate" 
 Do While Not .EOF 
 Debug.Print , !OrderID, !CustomerID, !OrderDate 
 .MoveNext 
 Loop 
 End With 
 
End Sub 
 
```

