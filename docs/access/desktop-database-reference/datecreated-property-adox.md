---
title: DateCreated, propriété (ADOX)
TOCTitle: DateCreated property (ADOX)
ms:assetid: ee975bf5-7d44-a993-d1c0-077993515698
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250209(v=office.15)
ms:contentKeyID: 48548564
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 344b193b3ab8d6800fcf81b6bb2d184b1104f9d3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923098"
---
# <a name="datecreated-property-adox"></a><span data-ttu-id="7c024-102">DateCreated, propriété (ADOX)</span><span class="sxs-lookup"><span data-stu-id="7c024-102">DateCreated property (ADOX)</span></span>


<span data-ttu-id="7c024-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7c024-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7c024-104">Indique la date de création de l'objet.</span><span class="sxs-lookup"><span data-stu-id="7c024-104">Indicates the date the object was created.</span></span>

## <a name="return-values"></a><span data-ttu-id="7c024-105">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="7c024-105">Return values</span></span>

<span data-ttu-id="7c024-p101">Renvoie une valeur de type **Variant** spécifiant la date de la création. La valeur est Null si la propriété **DateCreated** n'est pas prise en charge par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="7c024-p101">Returns a **Variant** value specifying the date created. The value is null if **DateCreated** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c024-108">Notes</span><span class="sxs-lookup"><span data-stu-id="7c024-108">Remarks</span></span>

<span data-ttu-id="7c024-p102">La propriété **DateCreated** a la valeur Null pour les objets récemment ajoutés. Après avoir ajouté un nouvel objet [View](view-object-adox.md) ou [Procedure](procedure-object-adox.md), vous devez appeler la méthode [Refresh](refresh-method-ado.md) de la collection [Views](views-collection-adox.md) ou [Procedures](procedures-collection-adox.md) afin d'obtenir les valeurs de la propriété **DateCreated**.</span><span class="sxs-lookup"><span data-stu-id="7c024-p102">The **DateCreated** property is null for newly appended objects. After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateCreated** property.</span></span>

