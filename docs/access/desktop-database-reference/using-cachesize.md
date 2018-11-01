---
title: À l’aide de la propriété CacheSize (référence de base de données du bureau Access)
TOCTitle: Using CacheSize
ms:assetid: b1677a9f-f22f-9456-0d2a-1ef7cf81bbdf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249846(v=office.15)
ms:contentKeyID: 48547148
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aa624c545d17ef0d56a076b3d30326bacd2c6edf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871961"
---
# <a name="using-cachesize"></a><span data-ttu-id="2b1fb-102">Utilisation de CacheSize</span><span class="sxs-lookup"><span data-stu-id="2b1fb-102">Using CacheSize</span></span>


<span data-ttu-id="2b1fb-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2b1fb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2b1fb-p101">Utilisez la propriété **CacheSize** pour contrôler le nombre d'enregistrements à récupérer simultanément à partir du fournisseur pour les insérer dans la mémoire locale. Par exemple, si **CacheSize** a pour valeur 10, après la première ouverture de l'objet **Recordset**, le fournisseur extrait les dix premiers enregistrements pour les insérer dans la mémoire locale. À mesure que vous parcourez l'objet **Recordset**, le fournisseur retourne les données du tampon de mémoire local. Dès que vous avez dépassé le dernier enregistrement du cache, le fournisseur récupère les dix enregistrements suivants de la source de données pour les insérer dans le cache.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-p101">Use the **CacheSize** property to control how many records to retrieve at one time into local memory from the provider. For example, if the **CacheSize** is 10, after first opening the **Recordset** object, the provider retrieves the first 10 records into local memory. As you move through the **Recordset** object, the provider returns the data from the local memory buffer. As soon as you move past the last record in the cache, the provider retrieves the next 10 records from the data source into the cache.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2b1fb-p102">[!REMARQUE] <STRONG>CacheSize</STRONG> dépend de la propriété <STRONG>Maximum Open Rows</STRONG> spécifique au fournisseur (dans la collection <STRONG>Properties</STRONG> de l'objet <STRONG>Recordset</STRONG> ). Vous ne pouvez pas attribuer à <STRONG>CacheSize</STRONG> une valeur supérieure à celle de <STRONG>Maximum Open Rows</STRONG>. Pour modifier le nombre de lignes que le fournisseur peut ouvrir, définissez la valeur de <STRONG>Maximum Open Rows</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-p102"><STRONG>CacheSize</STRONG> is based on the <STRONG>Maximum Open Rows</STRONG> provider-specific property (in the <STRONG>Properties</STRONG> collection of the <STRONG>Recordset</STRONG> object). You cannot set <STRONG>CacheSize</STRONG> to a value greater than <STRONG>Maximum Open Rows</STRONG>. To modify the number of rows that can be opened by the provider, set <STRONG>Maximum Open Rows</STRONG>.</span></span></P>



<span data-ttu-id="2b1fb-p103">La valeur de **CacheSize** peut être modifiée pendant la durée de vie de l'objet **Recordset** mais sa modification affecte uniquement le nombre d'enregistrements dans le cache après des extractions successives de la source des données. La modification de la seule valeur de la propriété ne suffira pas à modifier le contenu actuel du cache.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-p103">The value of **CacheSize** can be adjusted during the life of the **Recordset** object, but changing this value only affects the number of records in the cache after subsequent retrievals from the data source. Changing the property value alone will not change the current contents of the cache.</span></span>

<span data-ttu-id="2b1fb-113">S'il y a moins d'enregistrements à récupérer que ne l'indique la propriété **CacheSize**, le fournisseur renvoie les enregistrements restants et aucune erreur n'est générée.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-113">If there are fewer records to retrieve than **CacheSize** specifies, the provider returns the remaining records and no error occurs.</span></span>

<span data-ttu-id="2b1fb-114">L'affectation de la valeur zéro à **CacheSize** est interdite et se traduit par une erreur.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-114">A **CacheSize** setting of zero is not allowed and returns an error.</span></span>

<span data-ttu-id="2b1fb-p104">Les enregistrements extraits du cache ne reflètent pas les modifications apportées simultanément par d'autres utilisateurs aux données source. Pour forcer une mise à jour de toutes les données mises en cache, utilisez la méthode [Resync ](resync-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="2b1fb-p104">Records retrieved from the cache do not reflect concurrent changes that other users made to the source data. To force an update of all the cached data, use the [Resync](resync-method-ado.md) method.</span></span>

<span data-ttu-id="2b1fb-p105">Si  \*\*CacheSize \*\* a une valeur supérieure à 1, les méthodes de navigation ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext et MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) risquent d’accéder à un enregistrement supprimé si la suppression a lieu après la récupération des enregistrements. Après l’extraction initiale, les suppressions suivantes ne sont pas répercutées dans votre cache de données tant que vous n’avez pas tenté d’accéder à une valeur de données d’une ligne supprimée. Toutefois, ce problème est résolu si vous affectez la valeur 1 à \*\*CacheSize \*\* car les lignes supprimées ne peuvent pas être extraites.</span><span class="sxs-lookup"><span data-stu-id="2b1fb-p105">If **CacheSize** is set to a value greater than 1, the navigation methods ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext, and MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) may result in navigation to a deleted record, if deletion occurs after the records were retrieved. After the initial fetch, subsequent deletions will not be reflected in your data cache until you attempt to access a data value from a deleted row. However, setting **CacheSize** to 1 eliminates this issue because deleted rows cannot be fetched.</span></span>

