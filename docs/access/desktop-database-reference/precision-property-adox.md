---
title: Precision, propriété (ADOX)
TOCTitle: Precision property (ADOX)
ms:assetid: 5d8ca497-572a-52e0-18aa-f82deaea0813
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249330(v=office.15)
ms:contentKeyID: 48545117
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f05f6880a9599421189519f263cfb27bf1432325
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287481"
---
# <a name="precision-property-adox"></a><span data-ttu-id="c10ba-102">Precision, propriété (ADOX)</span><span class="sxs-lookup"><span data-stu-id="c10ba-102">Precision property (ADOX)</span></span>


<span data-ttu-id="c10ba-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c10ba-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c10ba-104">Indique la précision maximale de valeurs de données de la colonne.</span><span class="sxs-lookup"><span data-stu-id="c10ba-104">Indicates the maximum precision of data values in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="c10ba-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="c10ba-105">Settings and return values</span></span>

<span data-ttu-id="c10ba-p101">Définit et renvoie une valeur de type **Long** qui correspond à la précision maximale des valeurs de données de la colonne lorsque la propriété [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) est de type numérique. La propriété **Precision** est ignorée pour tous les autres types de données.</span><span class="sxs-lookup"><span data-stu-id="c10ba-p101">Sets and returns a **Long** value that is the maximum precision of data values in the column when the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property is a numeric type. **Precision** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="c10ba-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="c10ba-108">Remarks</span></span>

<span data-ttu-id="c10ba-109">La valeur par défaut est zéro (0).</span><span class="sxs-lookup"><span data-stu-id="c10ba-109">The default value is zero (0).</span></span>

<span data-ttu-id="c10ba-110">Cette propriété est en lecture seule pour des objets [Column](column-object-adox.md) déjà ajoutés à une collection.</span><span class="sxs-lookup"><span data-stu-id="c10ba-110">This property is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>

