---
title: NumericScale, propriété (ADO)
TOCTitle: NumericScale property (ADO)
ms:assetid: 51b232d2-5bfd-521c-f4e9-65655ecc7c70
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249263(v=office.15)
ms:contentKeyID: 48544824
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eb2c799fd7c9d1cc74c6081c10f7a8d356e79faf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876014"
---
# <a name="numericscale-property-ado"></a><span data-ttu-id="32d4a-102">NumericScale, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="32d4a-102">NumericScale property (ADO)</span></span>


<span data-ttu-id="32d4a-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="32d4a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="32d4a-104">Indique l'échelle des valeurs numériques possibles dans un objet [Parameter](parameter-object-ado.md) ou [Field](field-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="32d4a-104">Indicates the scale of numeric values in a [Parameter](parameter-object-ado.md) or [Field](field-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="32d4a-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="32d4a-105">Settings and return values</span></span>

<span data-ttu-id="32d4a-106">Définit ou renvoie une valeur de type **Byte** qui indique le nombre de décimales que comporteront les valeurs numériques.</span><span class="sxs-lookup"><span data-stu-id="32d4a-106">Sets or returns a **Byte** value that indicates the number of decimal places to which numeric values will be resolved.</span></span>

## <a name="remarks"></a><span data-ttu-id="32d4a-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="32d4a-107">Remarks</span></span>

<span data-ttu-id="32d4a-108">Utilisez la propriété **NumericScale** pour déterminer combien de chiffres à droite de la virgule seront utilisés pour représenter les valeurs d'un objet **Parameter** ou **Field** numérique.</span><span class="sxs-lookup"><span data-stu-id="32d4a-108">Use the **NumericScale** property to determine how many digits to the right of the decimal point will be used to represent values for a numeric **Parameter** or **Field** object.</span></span>

<span data-ttu-id="32d4a-109">Pour les objets **Parameter**, la propriété **NumericScale** est accessible en lecture et écriture.</span><span class="sxs-lookup"><span data-stu-id="32d4a-109">For **Parameter** objects, the **NumericScale** property is read/write.</span></span>

<span data-ttu-id="32d4a-p101">Pour un objet **Field**, **NumericScale** est généralement en lecture seule. Toutefois, pour les objets **Field** récemment ajoutés à la collection [Fields](fields-collection-ado.md) d'un objet [Record](record-object-ado.md), **NumericScale** est exceptionnellement accessible en lecture et en écriture après la définition de la propriété [Value](value-property-ado.md) de l'objet **Field** et une fois que le fournisseur de données a ajouté le nouvel objet **Field** en appelant la méthode [Update](update-method-ado.md)de la collection **Fields**.</span><span class="sxs-lookup"><span data-stu-id="32d4a-p101">For a **Field** object, **NumericScale** is normally read-only. However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **NumericScale** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

