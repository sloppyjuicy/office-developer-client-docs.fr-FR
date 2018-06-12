---
title: LISTSHEETREF, fonction
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ddbc35-8577-0a96-20b8-aa7734764c5b
description: Renvoie une référence de feuille à la forme conteneur de liste qui contient la forme.
ms.openlocfilehash: 75c765fab2d287c2da83a659dbbf070d29a9d325
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788996"
---
# <a name="listsheetref-function"></a><span data-ttu-id="e57b4-103">LISTSHEETREF, fonction</span><span class="sxs-lookup"><span data-stu-id="e57b4-103">LISTSHEETREF Function</span></span>

<span data-ttu-id="e57b4-104">Renvoie une référence de feuille à la forme conteneur de liste qui contient la forme.</span><span class="sxs-lookup"><span data-stu-id="e57b4-104">Returns a sheet reference to the list container shape that contains the shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="e57b4-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="e57b4-105">Version Information</span></span>

<span data-ttu-id="e57b4-106">Version ajoutée : Visio 2010</span><span class="sxs-lookup"><span data-stu-id="e57b4-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e57b4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e57b4-107">Syntax</span></span>

<span data-ttu-id="e57b4-108">LISTMEMBERCOUNT()</span><span class="sxs-lookup"><span data-stu-id="e57b4-108">LISTMEMBERCOUNT()</span></span>
  
### <a name="return-value"></a><span data-ttu-id="e57b4-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="e57b4-109">Return value</span></span>

<span data-ttu-id="e57b4-110">Référence ShapeSheet</span><span class="sxs-lookup"><span data-stu-id="e57b4-110">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e57b4-111">Note</span><span class="sxs-lookup"><span data-stu-id="e57b4-111">Remarks</span></span>

<span data-ttu-id="e57b4-112">Si la forme n’est pas un membre de la liste, la fonction LISTSHEETREF renvoie #REF!.</span><span class="sxs-lookup"><span data-stu-id="e57b4-112">If the shape is not a list member, the LISTSHEETREF function returns #REF!.</span></span>
  
## <a name="example"></a><span data-ttu-id="e57b4-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="e57b4-113">Example</span></span>

<span data-ttu-id="e57b4-114">LISTSHEETREF(1)!Height</span><span class="sxs-lookup"><span data-stu-id="e57b4-114">LISTSHEETREF(1)!Height</span></span> 
  
<span data-ttu-id="e57b4-115">Renvoie la valeur de la cellule Height de la forme conteneur de liste qui contient la forme.</span><span class="sxs-lookup"><span data-stu-id="e57b4-115">Returns the value in the Height cell of the list container shape that contains the shape.</span></span> 
  

