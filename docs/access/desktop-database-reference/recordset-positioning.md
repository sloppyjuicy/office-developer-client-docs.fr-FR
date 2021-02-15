---
title: Positionnement du recordset
TOCTitle: Recordset positioning
ms:assetid: 1b8b08d5-a11c-ec6e-201c-1405171a1264
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248955(v=office.15)
ms:contentKeyID: 48543546
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cffb5adce1266bd7fdd08989e9f92110f4829ba0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284503"
---
# <a name="recordset-positioning"></a><span data-ttu-id="cd021-102">Positionnement du recordset</span><span class="sxs-lookup"><span data-stu-id="cd021-102">Recordset positioning</span></span>

<span data-ttu-id="cd021-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cd021-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cd021-p101">La propriété **AbsolutePosition** permet d'accéder à un enregistrement donné, en fonction de sa position ordinale dans l'objet **Recordset** ou de déterminer la position ordinale de l'enregistrement actif. Le fournisseur doit prendre en charge les fonctionnalités requises pour que cette propriété soit disponible.</span><span class="sxs-lookup"><span data-stu-id="cd021-p101">Use the **AbsolutePosition** property to move to a record, based on its ordinal position in the **Recordset** object, or to determine the ordinal position of the current record. The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="cd021-p102">**AbsolutePosition** utilise des nombres en base 1 et est égale à 1 lorsque l'enregistrement actif est le premier de l'objet **Recordset**. Comme nous l'avons mentionné, la propriété **RecordCount** permet de déterminer le nombre d'enregistrements de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="cd021-p102">**AbsolutePosition** is 1-based and equals 1 when the current record is the first record in the **Recordset**. As mentioned previously, you can obtain the total number of records in the **Recordset** object from the **RecordCount** property.</span></span>

<span data-ttu-id="cd021-p103">Lorsque vous définissez la propriété **AbsolutePosition**, même si elle s'applique à un enregistrement stocké dans le cache actuel, ADO recharge le cache avec un nouveau groupe d'enregistrements, en commençant par l'enregistrement spécifié. La propriété **CacheSize** détermine, quant à elle, la taille de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="cd021-p103">When you set the **AbsolutePosition** property, even if it is to a record in the current cache, ADO reloads the cache with a new group of records starting with the record you specified. The **CacheSize** property determines the size of this group.</span></span>

> [!NOTE]
> <span data-ttu-id="cd021-p104">[!REMARQUE] Vous ne pouvez pas utiliser la propriété **AbsolutePosition** en tant que numéro d'enregistrement de substitution. En effet, la position d'un enregistrement change lorsque vous supprimez l'enregistrement précédent et rien ne garantit que la valeur de la propriété **AbsolutePosition** restera identique si l'objet **Recordset** est rouvert ou fait l'objet d'une nouvelle requête. L'utilisation des signets est recommandée pour conserver ou revenir à une position donnée. En outre, ils constituent le seul moyen de se positionner dans tous les types d'objets **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="cd021-p104">You should not use the **AbsolutePosition** property as a surrogate record number. The position of a given record changes when you delete a preceding record. There also is no assurance that a given record will have the same **AbsolutePosition** if the **Recordset** object is requeried or reopened. Bookmarks are the recommended way of retaining and returning to a given position and are the only way of positioning across all types of **Recordset** objects.</span></span>


