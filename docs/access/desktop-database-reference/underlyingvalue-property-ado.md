---
title: UnderlyingValue, propriété (ADO)
TOCTitle: UnderlyingValue property (ADO)
ms:assetid: f84f4c1c-2bd4-a725-3575-ed063ead13c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250262(v=office.15)
ms:contentKeyID: 48548782
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6d1618a0cb310c1e564fe18289da6a2d35e91d0b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313999"
---
# <a name="underlyingvalue-property-ado"></a><span data-ttu-id="babf6-102">UnderlyingValue, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="babf6-102">UnderlyingValue property (ADO)</span></span>


<span data-ttu-id="babf6-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="babf6-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="babf6-104">Indique la valeur actuelle d'un objet [Field](field-object-ado.md) dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="babf6-104">Indicates a [Field](field-object-ado.md) object's current value in the database.</span></span>

## <a name="return-value"></a><span data-ttu-id="babf6-105">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="babf6-105">Return value</span></span>

<span data-ttu-id="babf6-106">Renvoie une valeur **Variant** qui indique la valeur de l'objet **Field**.</span><span class="sxs-lookup"><span data-stu-id="babf6-106">Returns a **Variant** value that indicates the value of the **Field**.</span></span>

## <a name="remarks"></a><span data-ttu-id="babf6-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="babf6-107">Remarks</span></span>

<span data-ttu-id="babf6-p101">Utilisez la propriété **UnderlyingValue** pour renvoyer la valeur actuelle du champ de la base de données. La valeur du champ dans la propriété **UnderlyingValue** est celle qui est visible pour votre transaction et peut résulter d'une mise à jour récente effectuée par une autre transaction. Elle peut être différente de la propriété [OriginalValue](originalvalue-property-ado.md), qui reflète la valeur renvoyée à l'origine à l'objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="babf6-p101">Use the **UnderlyingValue** property to return the current field value from the database. The field value in the **UnderlyingValue** property is the value that is visible to your transaction and may be the result of a recent update by another transaction. This may differ from the [OriginalValue](originalvalue-property-ado.md) property, which reflects the value that was originally returned to the [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="babf6-p102">Cette procédure est similaire à la méthode [Resync](resync-method-ado.md), mais la propriété **UnderlyingValue** renvoie uniquement la valeur d'un champ spécifique de l'enregistrement actuel. C'est cette valeur que la méthode [Resync](resync-method-ado.md) utilise pour remplacer la propriété [Value](value-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="babf6-p102">This is similar to using the [Resync](resync-method-ado.md) method, but the **UnderlyingValue** property returns only the value for a specific field from the current record. This is the same value that the [Resync](resync-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.</span></span>

<span data-ttu-id="babf6-113">Lorsque vous utilisez cette propriété en association avec la propriété **OriginalValue**, vous pouvez résoudre les conflits générés par les mises à jour par lot.</span><span class="sxs-lookup"><span data-stu-id="babf6-113">When you use this property with the **OriginalValue** property, you can resolve conflicts that arise from batch updates.</span></span>

## <a name="record"></a><span data-ttu-id="babf6-114">Record</span><span class="sxs-lookup"><span data-stu-id="babf6-114">Record</span></span>

<span data-ttu-id="babf6-115">Pour les objets [Record](record-object-ado.md), cette propriété est vide pour les champs ajoutés avant l’appel de la méthode [Update](update-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="babf6-115">For [Record](record-object-ado.md) objects, this property will be empty for fields added before [Update](update-method-ado.md) is called.</span></span>

