---
title: DateModified, propriété (ADOX)
TOCTitle: DateModified Property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8465f97565d8519196b8221089121670ceedb275
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469419"
---
# <a name="datemodified-property-adox"></a><span data-ttu-id="d0736-102">DateModified, propriété (ADOX)</span><span class="sxs-lookup"><span data-stu-id="d0736-102">DateModified Property (ADOX)</span></span>


<span data-ttu-id="d0736-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d0736-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d0736-104">Indique à la date de la dernière modification de l'objet.</span><span class="sxs-lookup"><span data-stu-id="d0736-104">Indicates the date the object was last modified.</span></span>

## <a name="return-values"></a><span data-ttu-id="d0736-105">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="d0736-105">Return Values</span></span>

<span data-ttu-id="d0736-p101">Renvoie une valeur de type **Variant** en spécifiant la date de la modification. La valeur est Null si la propriété **DateModified** n'est pas prise en charge par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d0736-p101">Returns a **Variant** value specifying the date modified. The value is null if **DateModified** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0736-108">Notes</span><span class="sxs-lookup"><span data-stu-id="d0736-108">Remarks</span></span>

<span data-ttu-id="d0736-p102">La propriété **DateModified** a la valeur Null pour les objets récemment ajoutés. Après avoir ajouté un nouvel objet [View](view-object-adox.md) ou [Procedure](procedure-object-adox.md), vous devez appeler la méthode [Refresh](refresh-method-ado.md) de la collection [Views](views-collection-adox.md) ou [Procedures](procedures-collection-adox.md) afin d'obtenir les valeurs de la propriété **DateModified**.</span><span class="sxs-lookup"><span data-stu-id="d0736-p102">The **DateModified** property is null for newly appended objects. After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateModified** property.</span></span>

