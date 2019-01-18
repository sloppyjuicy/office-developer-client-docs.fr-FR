---
title: Propriété TableDef.ReplicaFilter (DAO)
TOCTitle: ReplicaFilter Property
ms:assetid: f44273de-2b6a-750f-cb7c-12c3ac2da503
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836681(v=office.15)
ms:contentKeyID: 48548683
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1055548
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ba296701faebb32696741a742b7fe01660b74c46
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722430"
---
# <a name="tabledefreplicafilter-property-dao"></a><span data-ttu-id="ce0a5-102">Propriété TableDef.ReplicaFilter (DAO)</span><span class="sxs-lookup"><span data-stu-id="ce0a5-102">TableDef.ReplicaFilter property (DAO)</span></span>

<span data-ttu-id="ce0a5-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ce0a5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ce0a5-p101">Définit ou renvoie une valeur sur un objet **[TableDef](tabledef-object-dao.md)** au sein d'un réplica partiel qui indique le sous-ensemble d'enregistrements répliqué vers cette table à partir d'un réplica complet. (Espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="ce0a5-p101">Sets or returns a value on a **[TableDef](tabledef-object-dao.md)** object within a partial replica that indicates which subset of records is replicated to that table from a full replica. (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="ce0a5-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce0a5-106">Syntax</span></span>

<span data-ttu-id="ce0a5-107">*expression* . ReplicaFilter</span><span class="sxs-lookup"><span data-stu-id="ce0a5-107">*expression* .ReplicaFilter</span></span>

<span data-ttu-id="ce0a5-108">*expression* Variable qui représente un objet **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="ce0a5-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce0a5-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="ce0a5-109">Remarks</span></span>

<span data-ttu-id="ce0a5-110">Le paramètre ou la valeur de retour est un type **String** ou **Boolean** spécifiant le sous-ensemble d'enregistrements qui est répliqué, comme indiqué dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="ce0a5-110">The setting or return value is a **String** or **Boolean** that indicates which subset of records is replicated, as specified in the following table:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ce0a5-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce0a5-111">Value</span></span></p></th>
<th><p><span data-ttu-id="ce0a5-112">Description</span><span class="sxs-lookup"><span data-stu-id="ce0a5-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ce0a5-113">Chaîne de caractères</span><span class="sxs-lookup"><span data-stu-id="ce0a5-113">A string</span></span></p></td>
<td><p><span data-ttu-id="ce0a5-114">Critère auquel un enregistrement de la table du réplica partiel doit satisfaire afin d'être répliqué à partir du réplica complet.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-114">A criteria that a record in the partial replica table must satisfy in order to be replicated from the full replica.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce0a5-115"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="ce0a5-115"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0a5-116">Réplique tous les enregistrements</span><span class="sxs-lookup"><span data-stu-id="ce0a5-116">Replicates all records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce0a5-117"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="ce0a5-117"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0a5-118">(Par défaut) Ne réplique aucun enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-118">(Default) Doesn't replicate any records.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ce0a5-119">Cette propriété est similaire à une clause SQL WHERE (sans le mot WHERE) à cette différence que vous ne pouvez pas spécifier de sous-requêtes, de fonctions d'agrégation (p.ex. **Count**) ni de fonctions définies par l'utilisateur dans les critères.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-119">This property is similar to an SQL WHERE clause (without the word WHERE), but you cannot specify subqueries, aggregate functions (such as **Count**), or user-defined functions within the criteria.</span></span>

<span data-ttu-id="ce0a5-p102">La synchronisation des données n'est possible qu'entre un réplica complet et un réplica partiel. Vous ne pouvez pas synchroniser des données entre deux réplicas partiels. En outre, avec la réplication partielle, vous pouvez définir des restrictions quant aux enregistrements à répliquer mais vous ne pouvez pas indiquer quels champs sont répliqués.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-p102">You can only synchronize data between a full replica and a partial replica. You can't synchronize data between two partial replicas. Also, with partial replication you can set restrictions on which records are replicated, but you can't indicate which fields are replicated.</span></span>

<span data-ttu-id="ce0a5-p103">En général vous redéfinissez un filtre de réplica lorsque vous souhaitez répliquer un autre jeu d'enregistrements. Par exemple, lorsqu'un représentant commercial reprend provisoirement le territoire de vente d'un autre représentant, l'application de base de données peut répliquer temporairement les données pour les deux régions puis revenir au filtre précédent. Dans ce scénario, l'application redéfinit la propriété **ReplicaFilter** puis remplit à nouveau le réplica partiel.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-p103">Usually, you reset a replica filter when you want to replicate a different set of records. For example, when a sales representative temporarily takes over another sales representative's region, the database application can temporarily replicate data for both regions and then return to the previous filter. In this scenario, the application resets the **ReplicaFilter** property and then repopulates the partial replica.</span></span>

<span data-ttu-id="ce0a5-126">Si votre application modifie les filtres de réplica, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="ce0a5-126">If your application changes replica filters, you should follow these steps:</span></span>

1.  <span data-ttu-id="ce0a5-127">Appelez la méthode **[Synchronize](database-synchronize-method-dao.md)** pour synchroniser votre réplica complet avec le réplica partiel dans lequel les filtres sont modifiés.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-127">Use the **[Synchronize](database-synchronize-method-dao.md)** method to synchronize your full replica with the partial replica in which the filters are being changed.</span></span>

2.  <span data-ttu-id="ce0a5-128">Utilisez la propriété **ReplicaFilter** pour apporter les modifications requises au filtre de réplica.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-128">Use the **ReplicaFilter** property to make the desired changes to the replica filter.</span></span>

3.  <span data-ttu-id="ce0a5-129">Appelez la méthode **[PopulatePartial](database-populatepartial-method-dao.md)** pour supprimer tous les enregistrement du réplica partiel et transférer tous les enregistrements du réplica complet correspondant aux nouveaux critères de filtre de réplica.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-129">Use the **[PopulatePartial](database-populatepartial-method-dao.md)** method to remove all records from the partial replica and transfer all records from the full replica that meet the new replica filter criteria.</span></span>

<span data-ttu-id="ce0a5-p104">Pour supprimer un filtre, affectez à la propriété **ReplicaFilter** la valeur **False**. Si vous supprimez tous les filtres et que vous appelez la méthode **PopulatePartial**, aucun enregistrement n'apparaîtra dans les tables répliquées du réplica partiel.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-p104">To remove a filter, set the **ReplicaFilter** property to **False**. If you remove all filters and invoke the **PopulatePartial** method, no records will appear in any replicated tables in the partial replica.</span></span>

> [!NOTE]
> <span data-ttu-id="ce0a5-132">[!REMARQUE] Si un filtre de réplica a été modifié et que la méthode **Synchronize** est exécutée sans avoir préalablement appelé la méthode **PopulatePartial**, une erreur piégeable se produit.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-132">If a replica filter has changed, and the **Synchronize** method is invoked without first invoking **PopulatePartial**, a trappable error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="ce0a5-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="ce0a5-133">Example</span></span>

<span data-ttu-id="ce0a5-134">L'exemple suivant utilise la propriété **ReplicaFilter** pour répliquer uniquement les enregistrements clients de Californie.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-134">The following example uses the **ReplicaFilter** property to replicate only customer records from the California region.</span></span>

```vb 
Sub ReplicaFilterX() 
 
 ' This example assumes the current open database 
 ' is the replica. 
 Dim tdfCustomers As TableDef 
 Dim strFilter As String 
 Dim dbsTemp As Database 
 
 Set dbsTemp = OpenDatabase("Northwind.mdb") 
 Set tdfCustomers = dbsTemp.TableDefs("Customers") 
 
 ' Synchronize with full replica 
 ' before setting replica filter. 
 dbsTemp.Synchronize "C:\SALES\FY96.MDB" 
 
 strFilter = "Region = 'CA'" 
 tdfCustomers.ReplicaFilter = strFilter 
 dbsTemp.PopulatePartial "C:\SALES\FY96.MDB" 
 
 ' Now remove the replica filter (for example purposes 
 ' only). 
 tdfCustomers.ReplicaFilter = False 
 ' Repopulate the database. 
 dbsTemp.PopulatePartial "C:\SALES\DATA96.MDB" 
 
End Sub 
 
```

