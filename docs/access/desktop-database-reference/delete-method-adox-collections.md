---
title: DELETE, méthode (Collections ADOX)
TOCTitle: Delete method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a429c18890125f1c047c6356d250713ea5ea817
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944899"
---
# <a name="delete-method-adox-collections"></a><span data-ttu-id="67fb2-102">DELETE, méthode (Collections ADOX)</span><span class="sxs-lookup"><span data-stu-id="67fb2-102">Delete method (ADOX Collections)</span></span>


<span data-ttu-id="67fb2-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="67fb2-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="67fb2-104">Supprime un objet d'une collection.</span><span class="sxs-lookup"><span data-stu-id="67fb2-104">Removes an object from a collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="67fb2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67fb2-105">Syntax</span></span>

<span data-ttu-id="67fb2-106">La *collection*. Supprimer le*nom*</span><span class="sxs-lookup"><span data-stu-id="67fb2-106">*Collection*.Delete*Name*</span></span>

## <a name="parameters"></a><span data-ttu-id="67fb2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67fb2-107">Parameters</span></span>

- <span data-ttu-id="67fb2-108">*Name*</span><span class="sxs-lookup"><span data-stu-id="67fb2-108">*Name*</span></span>

  - <span data-ttu-id="67fb2-109">Valeur de type **Variant** qui spécifie le nom ou la position ordinale (index) de l'objet à supprimer.</span><span class="sxs-lookup"><span data-stu-id="67fb2-109">A **Variant** that specifies the name or ordinal position (index) of the object to delete.</span></span>

## <a name="remarks"></a><span data-ttu-id="67fb2-110">Notes</span><span class="sxs-lookup"><span data-stu-id="67fb2-110">Remarks</span></span>

<span data-ttu-id="67fb2-111">Une erreur se produit si le *nom* n’existe pas dans la collection.</span><span class="sxs-lookup"><span data-stu-id="67fb2-111">An error will occur if the *Name* does not exist in the collection.</span></span>

<span data-ttu-id="67fb2-p101">Pour les collections [Tables](tables-collection-adox.md) et [Users](users-collection-adox.md), une erreur se produit si le fournisseur ne prend pas en charge la suppression respective des tables ou des utilisateurs. Pour les collections [Procedures](procedures-collection-adox.md) et [Views](views-collection-adox.md), la méthode **Delete** échoue si le fournisseur ne prend pas en charge les commandes persistantes.</span><span class="sxs-lookup"><span data-stu-id="67fb2-p101">For [Tables](tables-collection-adox.md) and [Users](users-collection-adox.md) collections, an error will occur if the provider does not support deleting tables or users, respectively. For [Procedures](procedures-collection-adox.md) and [Views](views-collection-adox.md) collections, **Delete** will fail if the provider does not support persisting commands.</span></span>

