---
title: DateCreated, propriété (ADOX)
TOCTitle: DateCreated property (ADOX)
ms:assetid: ee975bf5-7d44-a993-d1c0-077993515698
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250209(v=office.15)
ms:contentKeyID: 48548564
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 59b19ab3be6633daf7295a63a33a31a34b64fbd7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712616"
---
# <a name="datecreated-property-adox"></a><span data-ttu-id="c5a9d-102">DateCreated, propriété (ADOX)</span><span class="sxs-lookup"><span data-stu-id="c5a9d-102">DateCreated property (ADOX)</span></span>


<span data-ttu-id="c5a9d-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c5a9d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c5a9d-104">Indique la date de création de l'objet.</span><span class="sxs-lookup"><span data-stu-id="c5a9d-104">Indicates the date the object was created.</span></span>

## <a name="return-values"></a><span data-ttu-id="c5a9d-105">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="c5a9d-105">Return values</span></span>

<span data-ttu-id="c5a9d-p101">Renvoie une valeur de type **Variant** spécifiant la date de la création. La valeur est Null si la propriété **DateCreated** n'est pas prise en charge par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c5a9d-p101">Returns a **Variant** value specifying the date created. The value is null if **DateCreated** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5a9d-108">Notes</span><span class="sxs-lookup"><span data-stu-id="c5a9d-108">Remarks</span></span>

<span data-ttu-id="c5a9d-p102">La propriété **DateCreated** a la valeur Null pour les objets récemment ajoutés. Après avoir ajouté un nouvel objet [View](view-object-adox.md) ou [Procedure](procedure-object-adox.md), vous devez appeler la méthode [Refresh](refresh-method-ado.md) de la collection [Views](views-collection-adox.md) ou [Procedures](procedures-collection-adox.md) afin d'obtenir les valeurs de la propriété **DateCreated**.</span><span class="sxs-lookup"><span data-stu-id="c5a9d-p102">The **DateCreated** property is null for newly appended objects. After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateCreated** property.</span></span>

