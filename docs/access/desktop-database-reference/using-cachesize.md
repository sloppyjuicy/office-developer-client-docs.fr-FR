---
title: Utilisation de CacheSize (référence de base de données de bureau Access)
TOCTitle: Using CacheSize
ms:assetid: b1677a9f-f22f-9456-0d2a-1ef7cf81bbdf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249846(v=office.15)
ms:contentKeyID: 48547148
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 94e84ad8c8a87a6537c1abefe12427ecad0c0187
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312123"
---
# <a name="using-cachesize"></a><span data-ttu-id="9eba7-102">Utilisation de CacheSize</span><span class="sxs-lookup"><span data-stu-id="9eba7-102">Using CacheSize</span></span>

<span data-ttu-id="9eba7-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9eba7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9eba7-p101">Utilisez la propriété **CacheSize** pour contrôler le nombre d'enregistrements à récupérer simultanément à partir du fournisseur pour les insérer dans la mémoire locale. Par exemple, si **CacheSize** a pour valeur 10, après la première ouverture de l'objet **Recordset**, le fournisseur extrait les dix premiers enregistrements pour les insérer dans la mémoire locale. À mesure que vous parcourez l'objet **Recordset**, le fournisseur retourne les données du tampon de mémoire local. Dès que vous avez dépassé le dernier enregistrement du cache, le fournisseur récupère les dix enregistrements suivants de la source de données pour les insérer dans le cache.</span><span class="sxs-lookup"><span data-stu-id="9eba7-p101">Use the **CacheSize** property to control how many records to retrieve at one time into local memory from the provider. For example, if the **CacheSize** is 10, after first opening the **Recordset** object, the provider retrieves the first 10 records into local memory. As you move through the **Recordset** object, the provider returns the data from the local memory buffer. As soon as you move past the last record in the cache, the provider retrieves the next 10 records from the data source into the cache.</span></span>

> [!NOTE]
> <span data-ttu-id="9eba7-p102">[!REMARQUE] **CacheSize** dépend de la propriété **Maximum Open Rows** spécifique au fournisseur (dans la collection **Properties** de l'objet **Recordset** ). Vous ne pouvez pas attribuer à **CacheSize** une valeur supérieure à celle de **Maximum Open Rows**. Pour modifier le nombre de lignes que le fournisseur peut ouvrir, définissez la valeur de **Maximum Open Rows**.</span><span class="sxs-lookup"><span data-stu-id="9eba7-p102">**CacheSize** is based on the **Maximum Open Rows** provider-specific property (in the **Properties** collection of the **Recordset** object). You cannot set **CacheSize** to a value greater than **Maximum Open Rows**. To modify the number of rows that can be opened by the provider, set **Maximum Open Rows**.</span></span>

<span data-ttu-id="9eba7-p103">La valeur de **CacheSize** peut être modifiée pendant la durée de vie de l'objet **Recordset** mais sa modification affecte uniquement le nombre d'enregistrements dans le cache après des extractions successives de la source des données. La modification de la seule valeur de la propriété ne suffira pas à modifier le contenu actuel du cache.</span><span class="sxs-lookup"><span data-stu-id="9eba7-p103">The value of **CacheSize** can be adjusted during the life of the **Recordset** object, but changing this value only affects the number of records in the cache after subsequent retrievals from the data source. Changing the property value alone will not change the current contents of the cache.</span></span>

<span data-ttu-id="9eba7-113">Si le nombre d'enregistrements à récupérer est inférieur à la valeur de **CacheSize** spécifiée, le fournisseur retourne les enregistrements restants sans qu'aucune erreur ne se produise.</span><span class="sxs-lookup"><span data-stu-id="9eba7-113">If there are fewer records to retrieve than **CacheSize** specifies, the provider returns the remaining records and no error occurs.</span></span>

<span data-ttu-id="9eba7-114">L'affectation de la valeur zéro à **CacheSize** est interdite et se traduit par une erreur.</span><span class="sxs-lookup"><span data-stu-id="9eba7-114">A **CacheSize** setting of zero is not allowed and returns an error.</span></span>

<span data-ttu-id="9eba7-p104">Les enregistrements extraits du cache ne reflètent pas les modifications apportées simultanément par d'autres utilisateurs aux données source. Pour forcer une mise à jour de toutes les données mises en cache, utilisez la méthode [Resync ](resync-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9eba7-p104">Records retrieved from the cache do not reflect concurrent changes that other users made to the source data. To force an update of all the cached data, use the [Resync](resync-method-ado.md) method.</span></span>

<span data-ttu-id="9eba7-p105">Si  **CacheSize** a une valeur supérieure à 1, les méthodes de navigation ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext et MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) risquent d’accéder à un enregistrement supprimé si la suppression a lieu après la récupération des enregistrements. Après l’extraction initiale, les suppressions suivantes ne sont pas répercutées dans votre cache de données tant que vous n’avez pas tenté d’accéder à une valeur de données d’une ligne supprimée. Toutefois, ce problème est résolu si vous affectez la valeur 1 à **CacheSize** car les lignes supprimées ne peuvent pas être extraites.</span><span class="sxs-lookup"><span data-stu-id="9eba7-p105">If **CacheSize** is set to a value greater than 1, the navigation methods ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext, and MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) may result in navigation to a deleted record, if deletion occurs after the records were retrieved. After the initial fetch, subsequent deletions will not be reflected in your data cache until you attempt to access a data value from a deleted row. However, setting **CacheSize** to 1 eliminates this issue because deleted rows cannot be fetched.</span></span>

