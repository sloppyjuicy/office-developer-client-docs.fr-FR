---
title: Type, propriété (ADO)
TOCTitle: Type property (ADO)
ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15)
ms:contentKeyID: 48543397
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 646284877722baf9aec6bb591b071667fdf9cc1a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867726"
---
# <a name="type-property-ado"></a><span data-ttu-id="b0e3e-102">Type, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="b0e3e-102">Type property (ADO)</span></span>


<span data-ttu-id="b0e3e-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0e3e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b0e3e-104">Indique le type opérationnel ou le type de données de l'objet [Parameter](parameter-object-ado.md), [Field](field-object-ado.md) ou [Property](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b0e3e-104">Indicates the operational type or data type of a [Parameter](parameter-object-ado.md), [Field](field-object-ado.md), or [Property](property-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="b0e3e-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="b0e3e-105">Settings and return values</span></span>

<span data-ttu-id="b0e3e-106">Définit ou renvoie une valeur [DataTypeEnum](datatypeenum.md).</span><span class="sxs-lookup"><span data-stu-id="b0e3e-106">Sets or returns a [DataTypeEnum](datatypeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0e3e-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="b0e3e-107">Remarks</span></span>

<span data-ttu-id="b0e3e-p101">La propriété **Type** est en lecture/écriture pour les objets **Parameter**. Pour les nouveaux objets **Field** ayant été ajoutés à la collection [Fields](fields-collection-ado.md) d'un objet [Record](record-object-ado.md), la propriété **Type** n'est accessible en lecture et en écriture qu'une fois que la propriété [Value](value-property-ado.md) de l'objet **Field** est spécifiée et que le fournisseur de données a correctement ajouté le nouvel objet **Field** en appelant la méthode [Update](update-method-ado.md) de la collection **Fields**.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-p101">For **Parameter** objects, the **Type** property is read/write. For new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Type** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="b0e3e-110">Pour tous les autres objets, la propriété **Type** est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-110">For all other objects, the **Type** property is read-only.</span></span>

