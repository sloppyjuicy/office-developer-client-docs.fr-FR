---
title: Item, propriété (ADO)
TOCTitle: Item Property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 29453ac2801f606640fd6d9506a8ee1ee8625396
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469361"
---
# <a name="item-property-ado"></a><span data-ttu-id="30b90-102">Item, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="30b90-102">Item Property (ADO)</span></span>

<span data-ttu-id="30b90-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="30b90-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="30b90-104">Indique membre spécifique d'une collection, par son nom ou son nombre ordinal.</span><span class="sxs-lookup"><span data-stu-id="30b90-104">Indicates a specific member of a collection, by name or ordinal number.</span></span>

## <a name="syntax"></a><span data-ttu-id="30b90-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30b90-105">Syntax</span></span>

<span data-ttu-id="30b90-106">Définir*l’objet* = *collection*. Item (Index)</span><span class="sxs-lookup"><span data-stu-id="30b90-106">Set*object* = *collection*.Item ( Index )</span></span>

## <a name="return-value"></a><span data-ttu-id="30b90-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="30b90-107">Return Value</span></span>

<span data-ttu-id="30b90-108">Renvoie une référence à un objet.</span><span class="sxs-lookup"><span data-stu-id="30b90-108">Returns an object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="30b90-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30b90-109">Parameters</span></span>

- <span data-ttu-id="30b90-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="30b90-110">*Index*</span></span>

- <span data-ttu-id="30b90-111">Une expression **Variant** qui correspond soit au nom, soit au nombre ordinal d'un objet dans une collection.</span><span class="sxs-lookup"><span data-stu-id="30b90-111">A **Variant** expression that evaluates either to the name or to the ordinal number of an object in a collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="30b90-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="30b90-112">Remarks</span></span>

<span data-ttu-id="30b90-113">Utilisez la propriété **Item** pour renvoyer un objet spécifique dans une collection.</span><span class="sxs-lookup"><span data-stu-id="30b90-113">Use the **Item** property to return a specific object in a collection.</span></span> <span data-ttu-id="30b90-114">Si **l’élément** ne peut pas trouver un objet dans la collection correspondant à l’argument *Index* , une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="30b90-114">If **Item** cannot find an object in the collection corresponding to the *Index* argument, an error occurs.</span></span> <span data-ttu-id="30b90-115">Si la collection ne prend pas en charge les objets nommés, utilisez des nombres ordinaux comme références.</span><span class="sxs-lookup"><span data-stu-id="30b90-115">Also, some collections don't support named objects; for these collections, you must use ordinal number references.</span></span>

<span data-ttu-id="30b90-116">La propriété **Item** est la propriété par défaut de toutes les collections ; les formes de syntaxe suivantes sont donc interchangeables :</span><span class="sxs-lookup"><span data-stu-id="30b90-116">The **Item** property is the default property for all collections; therefore, the following syntax forms are interchangeable:</span></span>

```vb
    collection.Item (Index)
    collection (Index)
```
