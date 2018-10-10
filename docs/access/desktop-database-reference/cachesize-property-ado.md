---
title: CacheSize, propriété (ADO)
TOCTitle: CacheSize Property (ADO)
ms:assetid: 42f86cc0-30dc-669b-9e65-5e7ecd52c4d7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249200(v=office.15)
ms:contentKeyID: 48544491
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ed4d104dcd6d0b90e6011a305cd3502cf671175b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471732"
---
# <a name="cachesize-property-ado"></a><span data-ttu-id="7fbcc-102">CacheSize, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="7fbcc-102">CacheSize Property (ADO)</span></span>


<span data-ttu-id="7fbcc-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7fbcc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7fbcc-104">Indique le nombre d'enregistrements dans un objet [Recordset](recordset-object-ado.md), placés dans la mémoire cache locale.</span><span class="sxs-lookup"><span data-stu-id="7fbcc-104">Indicates the number of records from a [Recordset](recordset-object-ado.md) object that are cached locally in memory.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="7fbcc-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="7fbcc-105">Settings and Return Values</span></span>

<span data-ttu-id="7fbcc-p101">Définit ou renvoie une valeur de type **Long** qui doit être supérieure à 0. La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="7fbcc-p101">Sets or returns a **Long** value that must be greater than 0. Default is 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fbcc-108">Notes</span><span class="sxs-lookup"><span data-stu-id="7fbcc-108">Remarks</span></span>

<span data-ttu-id="7fbcc-p102">Utilisez la propriété **CacheSize** pour contrôler le nombre d'enregistrements à récupérer simultanément à partir du fournisseur pour les insérer dans la mémoire locale. Par exemple, si **CacheSize** a pour valeur 10, après la première ouverture de l'objet **Recordset**, le fournisseur extrait les dix premiers enregistrements pour les insérer dans la mémoire locale. À mesure que vous parcourez l'objet **Recordset**, le fournisseur retourne les données du tampon de mémoire local. Dès que vous avez dépassé le dernier enregistrement du cache, le fournisseur récupère les dix enregistrements suivants de la source de données pour les insérer dans le cache.</span><span class="sxs-lookup"><span data-stu-id="7fbcc-p102">Use the **CacheSize** property to control how many records to retrieve at one time into local memory from the provider. For example, if the **CacheSize** is 10, after first opening the **Recordset** object, the provider retrieves the first 10 records into local memory. As you move through the **Recordset** object, the provider returns the data from the local memory buffer. As soon as you move past the last record in the cache, the provider retrieves the next 10 records from the data source into the cache.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7fbcc-p103">[!REMARQUE] <STRONG>CacheSize</STRONG> est basé sur la propriété spécifique au fournisseur, <STRONG>Maximum Open Rows</STRONG>, (dans la collection <STRONG>Properties</STRONG> de l'objet <STRONG>Recordset</STRONG> ). Vous ne pouvez pas affecter à <STRONG>CacheSize</STRONG> une valeur supérieure à celle de la propriété <STRONG>Maximum Open Rows</STRONG>. Pour modifier le nombre de lignes que le fournisseur peut ouvrir, définissez <STRONG>Maximum Open Rows</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="7fbcc-p103"><STRONG>CacheSize</STRONG> is based on the <STRONG>Maximum Open Rows</STRONG> provider-specific property (in the <STRONG>Properties</STRONG> collection of the <STRONG>Recordset</STRONG> object). You cannot set <STRONG>CacheSize</STRONG> to a value greater than <STRONG>Maximum Open Rows</STRONG>. To modify the number of rows which can be opened by the provider, set <STRONG>Maximum Open Rows</STRONG>.</span></span></P>



<span data-ttu-id="7fbcc-p104">La valeur de **CacheSize** peut être ajustée au cours de la durée de vie de l'objet **Recordset**, mais si vous modifiez cette valeur, cela n'affecte que le nombre d'enregistrements présents en mémoire cache après plusieurs extractions successives de la source de données. La seule modification de la valeur de la propriété ne modifie pas le contenu actuel du cache.</span><span class="sxs-lookup"><span data-stu-id="7fbcc-p104">The value of **CacheSize** can be adjusted during the life of the **Recordset** object, but changing this value only affects the number of records in the cache after subsequent retrievals from the data source. Changing the property value alone will not change the current contents of the cache.</span></span>

<span data-ttu-id="7fbcc-118">S'il y a moins d'enregistrements à récupérer que ne l'indique la propriété **CacheSize**, le fournisseur renvoie les enregistrements restants et aucune erreur n'est générée.</span><span class="sxs-lookup"><span data-stu-id="7fbcc-118">If there are fewer records to retrieve than **CacheSize** specifies, the provider returns the remaining records and no error occurs.</span></span>

<span data-ttu-id="7fbcc-119">Vous ne pouvez pas utiliser un paramètre **CacheSize** de valeur zéro. Dans ce cas, une erreur est générée.</span><span class="sxs-lookup"><span data-stu-id="7fbcc-119">A **CacheSize** setting of zero is not allowed and returns an error.</span></span>

<span data-ttu-id="7fbcc-p105">Les enregistrements extraits du cache ne reflètent pas les modifications simultanées apportées aux données sources par d'autres utilisateurs. Pour forcer la mise à jour de toutes les données mises en cache, utilisez la méthode [Resync](resync-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="7fbcc-p105">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data. To force an update of all the cached data, use the [Resync](resync-method-ado.md) method.</span></span>

<span data-ttu-id="7fbcc-p106">Si **CacheSize** a une valeur supérieure à 1, les méthodes de navigation ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext et MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) peuvent parfois accéder à un enregistrement supprimé, si une suppression a lieu après l’extraction des enregistrements. Après l’extraction initiale, les suppressions suivantes ne sont pas reflétées dans le cache de données tant que vous ne tentez pas d’accéder à une valeur de donnée d’une ligne supprimée. Cependant, si vous attribuez la valeur 1 à **CacheSize**, le problème ne se pose pas puisque les lignes supprimées ne peuvent pas être extraites.</span><span class="sxs-lookup"><span data-stu-id="7fbcc-p106">If **CacheSize** is set to a value greater than one, the navigation methods ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext, and MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) may result in navigation to a deleted record, if deletion occurs after the records were retrieved. After the initial fetch, subsequent deletions will not be reflected in your data cache until you attempt to access a data value from a deleted row. However, setting **CacheSize** to one eliminates this issue since deleted rows cannot be fetched.</span></span>

