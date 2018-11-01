---
title: CompareBookmarks, méthode (ADO)
TOCTitle: CompareBookmarks Method (ADO)
ms:assetid: 826cb3c7-2f5c-284f-421d-6b7b07f14dec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249564(v=office.15)
ms:contentKeyID: 48545977
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 26f8cb17473daf21be3769f6f48a3bb368c1d082
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876973"
---
# <a name="comparebookmarks-method-ado"></a><span data-ttu-id="cc349-102">CompareBookmarks, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="cc349-102">CompareBookmarks Method (ADO)</span></span>


<span data-ttu-id="cc349-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cc349-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cc349-104">Compare deux signets et retourne une indication de leurs valeurs relatives.</span><span class="sxs-lookup"><span data-stu-id="cc349-104">Compares two bookmarks and returns an indication of their relative values.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc349-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc349-105">Syntax</span></span>

<span data-ttu-id="cc349-106">*résultat* = *jeu d’enregistrements*. CompareBookmarks (*Bookmark1*, *Bookmark2*)</span><span class="sxs-lookup"><span data-stu-id="cc349-106">*result* = *recordset*.CompareBookmarks(*Bookmark1*, *Bookmark2*)</span></span>

## <a name="return-value"></a><span data-ttu-id="cc349-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cc349-107">Return value</span></span>

<span data-ttu-id="cc349-108">Retourne une valeur [CompareEnum](compareenum.md) qui indique la position de ligne relative de deux enregistrements représentée par leur signet.</span><span class="sxs-lookup"><span data-stu-id="cc349-108">Returns a [CompareEnum](compareenum.md) value that indicates the relative row position of two records represented by their bookmarks.</span></span>

## <a name="parameters"></a><span data-ttu-id="cc349-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc349-109">Parameters</span></span>

  - <span data-ttu-id="cc349-110">*Bookmark1*</span><span class="sxs-lookup"><span data-stu-id="cc349-110">*Bookmark1*</span></span>

  - <span data-ttu-id="cc349-111">Signet de la première ligne.</span><span class="sxs-lookup"><span data-stu-id="cc349-111">The bookmark of the first row.</span></span>

  - <span data-ttu-id="cc349-112">*Bookmark2*</span><span class="sxs-lookup"><span data-stu-id="cc349-112">*Bookmark2*</span></span>

  - <span data-ttu-id="cc349-113">Signet de la seconde ligne.</span><span class="sxs-lookup"><span data-stu-id="cc349-113">The bookmark of the second row.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc349-114">Notes</span><span class="sxs-lookup"><span data-stu-id="cc349-114">Remarks</span></span>

<span data-ttu-id="cc349-p101">Les signets doivent s'appliquer au même objet [Recordset](recordset-object-ado.md) ou à un objet **Recordset** et à son [clone](clone-method-ado.md). Vous ne pouvez pas comparer correctement des signets issus d'objets **Recordset** différents, même s'ils ont été créés à partir de la même source ou commande. Vous ne pouvez pas non plus comparer des signets d'un objet **Recordset** dont le fournisseur sous-jacent ne prend pas en charge les comparaisons.</span><span class="sxs-lookup"><span data-stu-id="cc349-p101">The bookmarks must apply to the same [Recordset](recordset-object-ado.md) object, or a **Recordset** object and its [clone](clone-method-ado.md). You cannot reliably compare bookmarks from different **Recordset** objects, even if they were created from the same source or command. Nor can you compare bookmarks for a **Recordset** object whose underlying provider does not support comparisons.</span></span>

<span data-ttu-id="cc349-p102">Un signet constitue l'identification unique d'une ligne dans un objet **Recordset**. Utilisez la propriété [Bookmark](bookmark-property-ado.md) de la ligne active pour obtenir son signet.</span><span class="sxs-lookup"><span data-stu-id="cc349-p102">A bookmark uniquely identifies a row in a **Recordset** object. Use the current row's [Bookmark](bookmark-property-ado.md) property to obtain its bookmark.</span></span>

<span data-ttu-id="cc349-120">Comme le type de données d'un signet est propre au fournisseur, ADO l'expose en tant que type Variant.</span><span class="sxs-lookup"><span data-stu-id="cc349-120">Because the data type of a bookmark is provider specific, ADO exposes it as a Variant.</span></span> <span data-ttu-id="cc349-121">Par exemple, les signets SQL Server sont de type DBTYPE\_R8 (Double).</span><span class="sxs-lookup"><span data-stu-id="cc349-121">For example, SQL Server bookmarks are of type DBTYPE\_R8 (Double).</span></span> <span data-ttu-id="cc349-122">ADO l'expose en tant que type Variant avec le sous-type Double.</span><span class="sxs-lookup"><span data-stu-id="cc349-122">ADO would expose this type as a Variant with a subtype of Double.</span></span>

<span data-ttu-id="cc349-p104">Lorsqu'il compare des signets, ADO ne tente aucune forme de conversion forcée. Les valeurs sont tout simplement passées au fournisseur lors de la comparaison. Si les signets passés à la méthode **CompareBookmarks** sont stockés dans des variables de types différents, cela peut générer une erreur d'incompatibilité de type indiquant que les arguments n'ont pas le type approprié, qu'ils sont en dehors de la plage acceptable ou qu'ils sont en conflit.</span><span class="sxs-lookup"><span data-stu-id="cc349-p104">When comparing bookmarks, ADO does not attempt any type of coercion. The values are simply passed to the provider where the compare occurs. If bookmarks passed to the **CompareBookmarks** method are stored in variables of differing types, it can generate the type mismatch error, "Arguments are of the wrong type, are out of the acceptable range, or are in conflict with each other."</span></span>

<span data-ttu-id="cc349-126">Un signet qui n'est pas valide ni correctement formé génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="cc349-126">A bookmark that is not valid or incorrectly formed will cause an error.</span></span>

