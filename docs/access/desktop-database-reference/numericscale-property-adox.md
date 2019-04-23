---
title: NumericScale, propriété (ADOX)
TOCTitle: NumericScale property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d706bad7d1f605933a951498705657c3c454a2d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288517"
---
# <a name="numericscale-property-adox"></a><span data-ttu-id="2188c-102">NumericScale, propriété (ADOX)</span><span class="sxs-lookup"><span data-stu-id="2188c-102">NumericScale property (ADOX)</span></span>


<span data-ttu-id="2188c-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2188c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2188c-104">Indique l'échelle d'une valeur numérique de la colonne.</span><span class="sxs-lookup"><span data-stu-id="2188c-104">Indicates the scale of a numeric value in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="2188c-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="2188c-105">Settings and return values</span></span>

<span data-ttu-id="2188c-p101">Définit et renvoie une valeur de type **Byte** qui correspond à l’échelle des valeurs de données de la colonne lorsque la propriété [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) a pour valeur **adNumeric** ou **adDecimal**. **NumericScale** est ignoré pour tous les autres types de données.</span><span class="sxs-lookup"><span data-stu-id="2188c-p101">Sets and returns a **Byte** value that is the scale of data values in the column when the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property is **adNumeric** or **adDecimal**. **NumericScale** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="2188c-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="2188c-108">Remarks</span></span>

<span data-ttu-id="2188c-109">La valeur par défaut est zéro (0).</span><span class="sxs-lookup"><span data-stu-id="2188c-109">The default value is zero (0).</span></span>

<span data-ttu-id="2188c-110">**NumericScale** est en lecture seule pour les objets [Column](column-object-adox.md) déjà ajoutés à une collection.</span><span class="sxs-lookup"><span data-stu-id="2188c-110">**NumericScale** is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>

