---
title: Item, propriété (ADO)
TOCTitle: Item property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9cc38101cb17c52bf2c8c08c08c14163c3772b2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290792"
---
# <a name="item-property-ado"></a><span data-ttu-id="d2f9e-102">Item, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="d2f9e-102">Item property (ADO)</span></span>

<span data-ttu-id="d2f9e-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2f9e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d2f9e-104">Indique membre spécifique d'une collection, par son nom ou son nombre ordinal.</span><span class="sxs-lookup"><span data-stu-id="d2f9e-104">Indicates a specific member of a collection, by name or ordinal number.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2f9e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2f9e-105">Syntax</span></span>

<span data-ttu-id="d2f9e-106">Définir la collection  =  *d’objets*. Item ( Index )</span><span class="sxs-lookup"><span data-stu-id="d2f9e-106">Set *object* = *collection*.Item ( Index )</span></span>

## <a name="return-value"></a><span data-ttu-id="d2f9e-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d2f9e-107">Return value</span></span>

<span data-ttu-id="d2f9e-108">Renvoie une référence à un objet.</span><span class="sxs-lookup"><span data-stu-id="d2f9e-108">Returns an object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="d2f9e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2f9e-109">Parameters</span></span>

|<span data-ttu-id="d2f9e-110">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d2f9e-110">Parameter</span></span>|<span data-ttu-id="d2f9e-111">Description</span><span class="sxs-lookup"><span data-stu-id="d2f9e-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d2f9e-112">*Index*</span><span class="sxs-lookup"><span data-stu-id="d2f9e-112">*Index*</span></span> |<span data-ttu-id="d2f9e-113">Une expression **Variant** qui correspond soit au nom, soit au nombre ordinal d'un objet dans une collection.</span><span class="sxs-lookup"><span data-stu-id="d2f9e-113">A **Variant** expression that evaluates either to the name or to the ordinal number of an object in a collection.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d2f9e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d2f9e-114">Remarks</span></span>

<span data-ttu-id="d2f9e-p101">Utilisez la propriété **Item** pour renvoyer un objet spécifique dans une collection. Si **Item** ne parvient pas à trouver un objet dans la collection correspondant à l'argument *Index*, une erreur est générée. Si la collection ne prend pas en charge les objets nommés, utilisez des nombres ordinaux comme références.</span><span class="sxs-lookup"><span data-stu-id="d2f9e-p101">Use the **Item** property to return a specific object in a collection. If **Item** cannot find an object in the collection corresponding to the *Index* argument, an error occurs. Also, some collections don't support named objects; for these collections, you must use ordinal number references.</span></span>

<span data-ttu-id="d2f9e-118">La propriété **Item** est la propriété par défaut de toutes les collections ; par conséquent, les formes syntaxiques suivantes sont interchangeables :</span><span class="sxs-lookup"><span data-stu-id="d2f9e-118">The **Item** property is the default property for all collections; therefore, the following syntax forms are interchangeable:</span></span>

```vb
    collection.Item (Index)
    collection (Index)
```
