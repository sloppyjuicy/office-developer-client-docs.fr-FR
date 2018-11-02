---
title: DateModified, propriété (ADOX)
TOCTitle: DateModified property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 447b7c609dd122d825d97a7430349eb88f8f7b0b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923951"
---
# <a name="datemodified-property-adox"></a><span data-ttu-id="68727-102">DateModified, propriété (ADOX)</span><span class="sxs-lookup"><span data-stu-id="68727-102">DateModified property (ADOX)</span></span>


<span data-ttu-id="68727-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="68727-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="68727-104">Indique à la date de la dernière modification de l'objet.</span><span class="sxs-lookup"><span data-stu-id="68727-104">Indicates the date the object was last modified.</span></span>

## <a name="return-values"></a><span data-ttu-id="68727-105">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="68727-105">Return values</span></span>

<span data-ttu-id="68727-p101">Renvoie une valeur de type **Variant** en spécifiant la date de la modification. La valeur est Null si la propriété **DateModified** n'est pas prise en charge par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="68727-p101">Returns a **Variant** value specifying the date modified. The value is null if **DateModified** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="68727-108">Notes</span><span class="sxs-lookup"><span data-stu-id="68727-108">Remarks</span></span>

<span data-ttu-id="68727-p102">La propriété **DateModified** a la valeur Null pour les objets récemment ajoutés. Après avoir ajouté un nouvel objet [View](view-object-adox.md) ou [Procedure](procedure-object-adox.md), vous devez appeler la méthode [Refresh](refresh-method-ado.md) de la collection [Views](views-collection-adox.md) ou [Procedures](procedures-collection-adox.md) afin d'obtenir les valeurs de la propriété **DateModified**.</span><span class="sxs-lookup"><span data-stu-id="68727-p102">The **DateModified** property is null for newly appended objects. After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateModified** property.</span></span>

