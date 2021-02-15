---
title: DateModified, propriété (ADOX)
TOCTitle: DateModified property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: daf72804d51c18b5875e607ce5fdb0dfe20f406c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294406"
---
# <a name="datemodified-property-adox"></a><span data-ttu-id="ba458-102">DateModified, propriété (ADOX)</span><span class="sxs-lookup"><span data-stu-id="ba458-102">DateModified property (ADOX)</span></span>


<span data-ttu-id="ba458-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ba458-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ba458-104">Indique à la date de la dernière modification de l'objet.</span><span class="sxs-lookup"><span data-stu-id="ba458-104">Indicates the date the object was last modified.</span></span>

## <a name="return-values"></a><span data-ttu-id="ba458-105">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="ba458-105">Return values</span></span>

<span data-ttu-id="ba458-106">Renvoie une valeur de type **Variant** en spécifiant la date de la modification.</span><span class="sxs-lookup"><span data-stu-id="ba458-106">Returns a **Variant** value specifying the date modified.</span></span> <span data-ttu-id="ba458-107">La valeur est Null si la propriété **DateModified** n’est pas prise en charge par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ba458-107">The value is null if **DateModified** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba458-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="ba458-108">Remarks</span></span>

<span data-ttu-id="ba458-p102">La propriété **DateModified** a la valeur Null pour les objets récemment ajoutés. Après avoir ajouté un nouvel objet [View](view-object-adox.md) ou [Procedure](procedure-object-adox.md), vous devez appeler la méthode [Refresh](refresh-method-ado.md) de la collection [Views](views-collection-adox.md) ou [Procedures](procedures-collection-adox.md) afin d’obtenir les valeurs de la propriété **DateModified**.</span><span class="sxs-lookup"><span data-stu-id="ba458-p102">The **DateModified** property is null for newly appended objects. After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateModified** property.</span></span>

