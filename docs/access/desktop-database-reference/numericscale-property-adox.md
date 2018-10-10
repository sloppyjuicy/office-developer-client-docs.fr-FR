---
title: NumericScale, propriété (ADOX)
TOCTitle: NumericScale Property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4229a318c4eb855b86164f02f1075d29a915d718
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471331"
---
# <a name="numericscale-property-adox"></a><span data-ttu-id="1f6b7-102">NumericScale, propriété (ADOX)</span><span class="sxs-lookup"><span data-stu-id="1f6b7-102">NumericScale Property (ADOX)</span></span>


<span data-ttu-id="1f6b7-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f6b7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1f6b7-104">Indique l'échelle d'une valeur numérique de la colonne.</span><span class="sxs-lookup"><span data-stu-id="1f6b7-104">Indicates the scale of a numeric value in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="1f6b7-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="1f6b7-105">Settings and Return Values</span></span>

<span data-ttu-id="1f6b7-p101">Définit et renvoie une valeur de type **Byte** qui correspond à l'échelle des valeurs de données de la colonne lorsque la propriété [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) a pour valeur **adNumeric** ou **adDecimal**. **NumericScale** est ignoré pour tous les autres types de données.</span><span class="sxs-lookup"><span data-stu-id="1f6b7-p101">Sets and returns a **Byte** value that is the scale of data values in the column when the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property is **adNumeric** or **adDecimal**. **NumericScale** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f6b7-108">Notes</span><span class="sxs-lookup"><span data-stu-id="1f6b7-108">Remarks</span></span>

<span data-ttu-id="1f6b7-109">La valeur par défaut est zéro (0).</span><span class="sxs-lookup"><span data-stu-id="1f6b7-109">The default value is zero (0).</span></span>

<span data-ttu-id="1f6b7-110">**NumericScale** est en lecture seule pour les objets [Column](column-object-adox.md) déjà ajoutés à une collection.</span><span class="sxs-lookup"><span data-stu-id="1f6b7-110">**NumericScale** is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>

