---
title: Database.PopulatePartial Method (DAO)
TOCTitle: PopulatePartial Method
ms:assetid: fa3227a2-c961-6a98-32b3-5b6e5329a21d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837034(v=office.15)
ms:contentKeyID: 48548834
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101186
f1_categories:
- Office.Version=v15
ms.openlocfilehash: fa52050e91c1a291dd59f9cde1ea36c320406dd6
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860265"
---
# <a name="databasepopulatepartial-method-dao"></a><span data-ttu-id="a277e-102">Database.PopulatePartial Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="a277e-102">Database.PopulatePartial Method (DAO)</span></span>


<span data-ttu-id="a277e-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a277e-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="a277e-p101">Synchronise les modifications d'un réplica partiel avec le réplica complet, efface tous les enregistrements du réplica partiel, puis remplit à nouveau ce dernier en fonction des filtres de réplica actifs. (Bases de données du moteur de base de données Microsoft Access uniquement.)</span><span class="sxs-lookup"><span data-stu-id="a277e-p101">Synchronizes any changes in a partial replica with the full replica, clears all records in the partial replica, and then repopulates the partial replica based on the current replica filters. (Microsoft Access database engine databases only.).</span></span>

## <a name="syntax"></a><span data-ttu-id="a277e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a277e-106">Syntax</span></span>

<span data-ttu-id="a277e-107">*expression* . PopulatePartial (***NomCheminBaseDeDonnées***)</span><span class="sxs-lookup"><span data-stu-id="a277e-107">*expression* .PopulatePartial(***DbPathName***)</span></span>

<span data-ttu-id="a277e-108">*expression* Variable qui représente un objet de **base de données** .</span><span class="sxs-lookup"><span data-stu-id="a277e-108">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="a277e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a277e-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a277e-110">Name</span><span class="sxs-lookup"><span data-stu-id="a277e-110">Name</span></span></p></th>
<th><p><span data-ttu-id="a277e-111">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="a277e-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="a277e-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="a277e-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="a277e-113">Description</span><span class="sxs-lookup"><span data-stu-id="a277e-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a277e-114">NomCheminBaseDeDonnées</span><span class="sxs-lookup"><span data-stu-id="a277e-114">DbPathName</span></span></p></td>
<td><p><span data-ttu-id="a277e-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a277e-115">Required</span></span></p></td>
<td><p><span data-ttu-id="a277e-116"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="a277e-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="a277e-117">Chemin d'accès et nom du réplica complet à partir duquel les enregistrements sont remplis.</span><span class="sxs-lookup"><span data-stu-id="a277e-117">The path and name of the full replica from which to populate records.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a277e-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="a277e-118">Remarks</span></span>

<span data-ttu-id="a277e-119">Lorsque vous synchronisez un réplica partiel avec un réplica complet, il est possible de créer des enregistrements « orphelins » dans le réplica partiel.</span><span class="sxs-lookup"><span data-stu-id="a277e-119">When you synchronize a partial replica with a full replica, it is possible to create "orphaned" records in the partial replica.</span></span> <span data-ttu-id="a277e-120">Par exemple, supposons que vous possédez une table clients avec ses **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** la valeur « Region = 'CA' ».</span><span class="sxs-lookup"><span data-stu-id="a277e-120">For example, suppose you have a Customers table with its **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** set to "Region = 'CA'".</span></span> <span data-ttu-id="a277e-121">Si un utilisateur modifie la région d'un client en remplaçant CA par NY dans le réplica partiel, puis qu'une synchronisation est conduite via la méthode **[Synchronize](database-synchronize-method-dao.md)**, la modification est propagée dans le réplica complet, mais l'enregistrement contenant NY dans le réplica partiel devient orphelin, car il ne correspond plus aux critères du filtre de réplica.</span><span class="sxs-lookup"><span data-stu-id="a277e-121">If a user changes a customer's region from CA to NY in the partial replica, and then a synchronization occurs via the **[Synchronize](database-synchronize-method-dao.md)** method, the change is propagated to the full replica but the record containing NY in the partial replica is orphaned because it now doesn't meet the replica filter criteria.</span></span>

<span data-ttu-id="a277e-p103">Pour résoudre le problème des enregistrements orphelins, vous pouvez utiliser la méthode **PopulatePartial**. La méthode **PopulatePartial** est similaire à la méthode **Synchronize**, à ceci près qu'elle synchronise les modifications avec le réplica complet, qu'elle supprime tous les enregistrements dans le réplica partiel, puis qu'elle remplit à nouveau le réplica partiel en fonction des filtres de réplica actifs. Même si vos filtres de réplica n'ont pas changé, **PopulatePartial** efface invariablement l'ensemble des enregistrements du réplica partiel et le remplit à nouveau en fonction des filtres actifs.</span><span class="sxs-lookup"><span data-stu-id="a277e-p103">To solve the problem of orphaned records, you can use the **PopulatePartial** method. The **PopulatePartial** method is similar to the **Synchronize** method, but it synchronizes any changes with the full replica, removes all records in the partial replica, and then repopulates the partial replica based on the current replica filters. Even if your replica filters have not changed, **PopulatePartial** will always clear all records in the partial replica and repopulate it based on the current filters.</span></span>

<span data-ttu-id="a277e-p104">En règle générale, le recours à la méthode **PopulatePartial** s'avère judicieux dans le cadre de la création d'un réplica partiel et chaque fois que les filtres de réplica sont modifiés. Si votre application modifie les filtres de réplica, il est conseillé d'exécuter la procédure suivante :</span><span class="sxs-lookup"><span data-stu-id="a277e-p104">Generally, you should use the **PopulatePartial** method when you create a partial replica and whenever you change your replica filters. If your application changes replica filters, you should follow these steps:</span></span>

1.  <span data-ttu-id="a277e-127">Synchronisez votre réplica complet avec le réplica partiel dont les filtres sont modifiés.</span><span class="sxs-lookup"><span data-stu-id="a277e-127">Synchronize your full replica with the partial replica in which the filters are being changed.</span></span>

2.  <span data-ttu-id="a277e-128">Utilisez les propriétés **ReplicaFilter** et **[PartialReplica](relation-partialreplica-property-dao.md)** pour apporter les modifications souhaitées au filtre de réplica.</span><span class="sxs-lookup"><span data-stu-id="a277e-128">Use the **ReplicaFilter** and **[PartialReplica](relation-partialreplica-property-dao.md)** properties to make the desired changes to the replica filter.</span></span>

3.  <span data-ttu-id="a277e-129">Appelez la méthode **PopulatePartial** pour supprimer tous les enregistrements du réplica partiel et transférer tous ceux du réplica complet correspondant aux nouveaux critères du filtre de réplica.</span><span class="sxs-lookup"><span data-stu-id="a277e-129">Call the **PopulatePartial** method to remove all records from the partial replica and transfer all records from the full replica that meet the new replica filter criteria.</span></span>

<span data-ttu-id="a277e-130">Si vous modifiez un filtre de réplica et que la méthode **Synchronize** est appelée sans que la méthode **PopulatePartial** ait été d'abord appelée, une erreur interceptable se produit.</span><span class="sxs-lookup"><span data-stu-id="a277e-130">If a replica filter has changed, and the **Synchronize** method is invoked without first invoking **PopulatePartial**, a trappable error occurs.</span></span>

<span data-ttu-id="a277e-p105">La méthode **PopulatePartial** ne peut être appelée que sur un réplica partiel ouvert dans le cadre d'un accès exclusif. De plus, vous ne pouvez pas appeler la méthode **PopulatePartial** à partir du code s'exécutant à l'intérieur du réplica partiel proprement dit. Au lieu de cela, ouvrez le réplica partiel en mode exclusif à partir du réplica complet ou d'une autre base de données, puis appelez **PopulatePartial**.</span><span class="sxs-lookup"><span data-stu-id="a277e-p105">The **PopulatePartial** method can only be invoked on a partial replica that has been opened for exclusive access. Furthermore, you can't call the **PopulatePartial** method from code running within the partial replica itself. Instead, open the partial replica exclusively from the full replica or another database, then call **PopulatePartial**.</span></span>


> [!NOTE]
> <span data-ttu-id="a277e-p106">[!REMARQUE] Même si **PopulatePartial** effectue une synchronisation unidirectionnelle avant d'effacer et de remplir à nouveau le réplica partiel, il est judicieux d'appeler **Synchronize** avant **PopulatePartial**. En effet, si l'appel de **Synchronize** échoue, une erreur interceptable se produit. Cette erreur peut vous être utile pour décider s'il convient ou non de poursuivre avec la méthode **PopulatePartial** (laquelle supprime tous les enregistrements du réplica partiel). Si **PopulatePartial** s'appelle elle-même et qu'une erreur se produit alors que les enregistrements sont en cours de synchronisation, les enregistrements du réplica partiel sont quand même effacés, ce qui peut ne pas correspondre au résultat souhaité.</span><span class="sxs-lookup"><span data-stu-id="a277e-p106">Although **PopulatePartial** performs a one-way synchronization before clearing and repopulating the partial replica, it is still a good idea to call **Synchronize** before calling **PopulatePartial**. This is because if the call to **Synchronize** fails, a trappable error occurs. You can use this error to decide whether or not to proceed with the **PopulatePartial** method (which removes all records in the partial replica). If **PopulatePartial** is called by itself and an error occurs while records are being synchronized, records in the partial replica will still be cleared, which may not be the desired result.</span></span>



## <a name="example"></a><span data-ttu-id="a277e-138">Exemple</span><span class="sxs-lookup"><span data-stu-id="a277e-138">Example</span></span>

<span data-ttu-id="a277e-139">L'exemple de code suivant montre comment utiliser la méthode **PopulatePartial** après avoir modifié un filtre de réplica.</span><span class="sxs-lookup"><span data-stu-id="a277e-139">The following example uses the **PopulatePartial** method after changing a replica filter.</span></span>

```vb 
Sub PopulatePartialX() 
 
 Dim tdfCustomers As TableDef 
 Dim strFilter As String 
 Dim dbsTemp As Database 
 
 ' Open the partial replica in exclusive mode. 
 Set dbsTemp = OpenDatabase("F:\SALES\FY96CA.MDB", True) 
 
 With dbsTemp 
 Set tdfCustomers = .TableDefs("Customers") 
 
 ' Synchronize with full replica 
 ' before setting replica filter. 
 .Synchronize "C:\SALES\FY96.MDB" 
 
 strFilter = "Region = 'CA'" 
 tdfCustomers.ReplicaFilter = strFilter 
 
 ' Populate records from the full replica. 
 .PopulatePartial "C:\SALES\FY96.MDB" 
 
 .Close 
 End With 
 
End Sub 
 
```

