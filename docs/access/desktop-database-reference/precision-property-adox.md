---
title: Precision, propriété (ADOX)
TOCTitle: Precision Property (ADOX)
ms:assetid: 5d8ca497-572a-52e0-18aa-f82deaea0813
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249330(v=office.15)
ms:contentKeyID: 48545117
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5fab2a7dc7a2d9f05e22b064acfaeabf93106a3e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469503"
---
# <a name="precision-property-adox"></a><span data-ttu-id="09f24-102">Precision, propriété (ADOX)</span><span class="sxs-lookup"><span data-stu-id="09f24-102">Precision Property (ADOX)</span></span>


<span data-ttu-id="09f24-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="09f24-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="09f24-104">Indique la précision maximale de valeurs de données de la colonne.</span><span class="sxs-lookup"><span data-stu-id="09f24-104">Indicates the maximum precision of data values in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="09f24-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="09f24-105">Settings and Return Values</span></span>

<span data-ttu-id="09f24-p101">Définit et renvoie une valeur de type **Long** qui correspond à la précision maximale des valeurs de données de la colonne lorsque la propriété [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) est de type numérique. La propriété **Precision** est ignorée pour tous les autres types de données.</span><span class="sxs-lookup"><span data-stu-id="09f24-p101">Sets and returns a **Long** value that is the maximum precision of data values in the column when the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property is a numeric type. **Precision** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="09f24-108">Notes</span><span class="sxs-lookup"><span data-stu-id="09f24-108">Remarks</span></span>

<span data-ttu-id="09f24-109">La valeur par défaut est zéro (0).</span><span class="sxs-lookup"><span data-stu-id="09f24-109">The default value is zero (0).</span></span>

<span data-ttu-id="09f24-110">Cette propriété est en lecture seule pour des objets [Column](column-object-adox.md) déjà ajoutés à une collection.</span><span class="sxs-lookup"><span data-stu-id="09f24-110">This property is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>

