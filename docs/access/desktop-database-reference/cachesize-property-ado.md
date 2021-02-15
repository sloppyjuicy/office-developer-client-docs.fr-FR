---
title: CacheSize, propriété (ADO)
TOCTitle: CacheSize property (ADO)
ms:assetid: 42f86cc0-30dc-669b-9e65-5e7ecd52c4d7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249200(v=office.15)
ms:contentKeyID: 48544491
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 725c2f81b3f3bce05a3007c50705e9cf35f7008f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296744"
---
# <a name="cachesize-property-ado"></a><span data-ttu-id="d32c5-102">CacheSize, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="d32c5-102">CacheSize property (ADO)</span></span>


<span data-ttu-id="d32c5-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d32c5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d32c5-104">Indique le nombre d'enregistrements dans un objet [Recordset](recordset-object-ado.md), placés dans la mémoire cache locale.</span><span class="sxs-lookup"><span data-stu-id="d32c5-104">Indicates the number of records from a [Recordset](recordset-object-ado.md) object that are cached locally in memory.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="d32c5-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="d32c5-105">Settings and return values</span></span>

<span data-ttu-id="d32c5-106">Définit ou renvoie une valeur de type **Long** qui doit être supérieure à 0.</span><span class="sxs-lookup"><span data-stu-id="d32c5-106">Sets or returns a **Long** value that must be greater than 0.</span></span> <span data-ttu-id="d32c5-107">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="d32c5-107">Default is 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="d32c5-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="d32c5-108">Remarks</span></span>

<span data-ttu-id="d32c5-p102">Utilisez la propriété **CacheSize** pour contrôler le nombre d'enregistrements à récupérer simultanément à partir du fournisseur pour les insérer dans la mémoire locale. Par exemple, si **CacheSize** a pour valeur 10, après la première ouverture de l'objet **Recordset**, le fournisseur extrait les dix premiers enregistrements pour les insérer dans la mémoire locale. À mesure que vous parcourez l'objet **Recordset**, le fournisseur retourne les données du tampon de mémoire local. Dès que vous avez dépassé le dernier enregistrement du cache, le fournisseur récupère les dix enregistrements suivants de la source de données pour les insérer dans le cache.</span><span class="sxs-lookup"><span data-stu-id="d32c5-p102">Use the **CacheSize** property to control how many records to retrieve at one time into local memory from the provider. For example, if the **CacheSize** is 10, after first opening the **Recordset** object, the provider retrieves the first 10 records into local memory. As you move through the **Recordset** object, the provider returns the data from the local memory buffer. As soon as you move past the last record in the cache, the provider retrieves the next 10 records from the data source into the cache.</span></span>

> [!NOTE]
> <span data-ttu-id="d32c5-p103">[!REMARQUE] **CacheSize** est basé sur la propriété spécifique au fournisseur, **Maximum Open Rows**, (dans la collection **Properties** de l'objet **Recordset** ). Vous ne pouvez pas affecter à **CacheSize** une valeur supérieure à celle de la propriété **Maximum Open Rows**. Pour modifier le nombre de lignes que le fournisseur peut ouvrir, définissez **Maximum Open Rows**.</span><span class="sxs-lookup"><span data-stu-id="d32c5-p103">**CacheSize** is based on the **Maximum Open Rows** provider-specific property (in the **Properties** collection of the **Recordset** object). You cannot set **CacheSize** to a value greater than **Maximum Open Rows**. To modify the number of rows which can be opened by the provider, set **Maximum Open Rows**.</span></span>

<span data-ttu-id="d32c5-p104">La valeur de **CacheSize** peut être ajustée au cours de la durée de vie de l'objet **Recordset**, mais si vous modifiez cette valeur, cela n'affecte que le nombre d'enregistrements présents en mémoire cache après plusieurs extractions successives de la source de données. La seule modification de la valeur de la propriété ne modifie pas le contenu actuel du cache.</span><span class="sxs-lookup"><span data-stu-id="d32c5-p104">The value of **CacheSize** can be adjusted during the life of the **Recordset** object, but changing this value only affects the number of records in the cache after subsequent retrievals from the data source. Changing the property value alone will not change the current contents of the cache.</span></span>

<span data-ttu-id="d32c5-118">Si le nombre d'enregistrements à récupérer est inférieur à la valeur de **CacheSize** spécifiée, le fournisseur retourne les enregistrements restants sans qu'aucune erreur ne se produise.</span><span class="sxs-lookup"><span data-stu-id="d32c5-118">If there are fewer records to retrieve than **CacheSize** specifies, the provider returns the remaining records and no error occurs.</span></span>

<span data-ttu-id="d32c5-119">Vous ne pouvez pas utiliser un paramètre **CacheSize** de valeur zéro. Dans ce cas, une erreur est générée.</span><span class="sxs-lookup"><span data-stu-id="d32c5-119">A **CacheSize** setting of zero is not allowed and returns an error.</span></span>

<span data-ttu-id="d32c5-p105">Les enregistrements extraits du cache ne reflètent pas les modifications simultanées apportées aux données sources par d'autres utilisateurs. Pour forcer la mise à jour de toutes les données mises en cache, utilisez la méthode [Resync](resync-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d32c5-p105">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data. To force an update of all the cached data, use the [Resync](resync-method-ado.md) method.</span></span>

<span data-ttu-id="d32c5-p106">Si **CacheSize** a une valeur supérieure à 1, les méthodes de navigation ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext et MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) peuvent parfois accéder à un enregistrement supprimé, si une suppression a lieu après l’extraction des enregistrements. Après l’extraction initiale, les suppressions suivantes ne sont pas reflétées dans le cache de données tant que vous ne tentez pas d’accéder à une valeur de donnée d’une ligne supprimée. Cependant, si vous attribuez la valeur 1 à **CacheSize**, le problème ne se pose pas puisque les lignes supprimées ne peuvent pas être extraites.</span><span class="sxs-lookup"><span data-stu-id="d32c5-p106">If **CacheSize** is set to a value greater than one, the navigation methods ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext, and MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) may result in navigation to a deleted record, if deletion occurs after the records were retrieved. After the initial fetch, subsequent deletions will not be reflected in your data cache until you attempt to access a data value from a deleted row. However, setting **CacheSize** to one eliminates this issue since deleted rows cannot be fetched.</span></span>

