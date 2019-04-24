---
title: Delete, méthode (collections ADOX)
TOCTitle: Delete method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54c67848d321125af44d9f5bf50f3aa582b043bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294077"
---
# <a name="delete-method-adox-collections"></a><span data-ttu-id="14d31-102">Delete, méthode (collections ADOX)</span><span class="sxs-lookup"><span data-stu-id="14d31-102">Delete method (ADOX Collections)</span></span>

<span data-ttu-id="14d31-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="14d31-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="14d31-104">Supprime un objet d'une collection.</span><span class="sxs-lookup"><span data-stu-id="14d31-104">Removes an object from a collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="14d31-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14d31-105">Syntax</span></span>

<span data-ttu-id="14d31-106">*Collection*. Supprimer le*nom*</span><span class="sxs-lookup"><span data-stu-id="14d31-106">*Collection*.Delete*Name*</span></span>

## <a name="parameters"></a><span data-ttu-id="14d31-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14d31-107">Parameters</span></span>

|<span data-ttu-id="14d31-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="14d31-108">Parameter</span></span>|<span data-ttu-id="14d31-109">Description</span><span class="sxs-lookup"><span data-stu-id="14d31-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="14d31-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="14d31-110">*Name*</span></span> |<span data-ttu-id="14d31-111">Valeur de type **Variant** qui spécifie le nom ou la position ordinale (index) de l'objet à supprimer.</span><span class="sxs-lookup"><span data-stu-id="14d31-111">A **Variant** that specifies the name or ordinal position (index) of the object to delete.</span></span>|

## <a name="remarks"></a><span data-ttu-id="14d31-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="14d31-112">Remarks</span></span>

<span data-ttu-id="14d31-113">Une erreur se produit si le paramètre *Name* n'existe pas dans la collection.</span><span class="sxs-lookup"><span data-stu-id="14d31-113">An error will occur if the *Name* does not exist in the collection.</span></span>

<span data-ttu-id="14d31-p101">Pour les collections [Tables](tables-collection-adox.md) et [Users](users-collection-adox.md), une erreur se produit si le fournisseur ne prend pas en charge la suppression respective des tables ou des utilisateurs. Pour les collections [Procedures](procedures-collection-adox.md) et [Views](views-collection-adox.md), la méthode **Delete** échoue si le fournisseur ne prend pas en charge les commandes persistantes.</span><span class="sxs-lookup"><span data-stu-id="14d31-p101">For [Tables](tables-collection-adox.md) and [Users](users-collection-adox.md) collections, an error will occur if the provider does not support deleting tables or users, respectively. For [Procedures](procedures-collection-adox.md) and [Views](views-collection-adox.md) collections, **Delete** will fail if the provider does not support persisting commands.</span></span>

