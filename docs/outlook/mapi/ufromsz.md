---
title: UFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UFromSz
api_type:
- COM
ms.assetid: 4a67faa2-8c2e-49a7-8c92-690a0a65c8f7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9947558975098316a547abfaefcdf5e7d4cd2f41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439008"
---
# <a name="ufromsz"></a><span data-ttu-id="30011-103">UFromSz</span><span class="sxs-lookup"><span data-stu-id="30011-103">UFromSz</span></span>

  
  
<span data-ttu-id="30011-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30011-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30011-105">Convertit une chaîne de chiffres décimales terminée par null en un nombre non signé.</span><span class="sxs-lookup"><span data-stu-id="30011-105">Converts a null-terminated string of decimal digits into an unsigned integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="30011-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="30011-106">Header file:</span></span>  <br/> |<span data-ttu-id="30011-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="30011-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="30011-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="30011-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="30011-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="30011-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="30011-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="30011-110">Called by:</span></span>  <br/> |<span data-ttu-id="30011-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="30011-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="30011-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30011-112">Parameters</span></span>

 <span data-ttu-id="30011-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="30011-113">_lpsz_</span></span>
  
> <span data-ttu-id="30011-114">[in] Pointeur vers la chaîne terminée par null à convertir.</span><span class="sxs-lookup"><span data-stu-id="30011-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="30011-115">Le  _paramètre lpsz_ ne doit pas dépasser 65 536 caractères.</span><span class="sxs-lookup"><span data-stu-id="30011-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="30011-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="30011-116">Return value</span></span>

 <span data-ttu-id="30011-117">**UFromSz** renvoie un integer non signé.</span><span class="sxs-lookup"><span data-stu-id="30011-117">**UFromSz** returns an unsigned integer.</span></span> <span data-ttu-id="30011-118">Si la chaîne ne commence pas par au moins un chiffre décimal, zéro est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="30011-118">If the string does not begin with at least one decimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="30011-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="30011-119">Remarks</span></span>

<span data-ttu-id="30011-120">La **fonction UFromSz** cesse de se convertir lorsqu’elle atteint le premier caractère de la chaîne qui n’est pas un chiffre décimal.</span><span class="sxs-lookup"><span data-stu-id="30011-120">The **UFromSz** function stops converting when it reaches the first character in the string that is not a decimal digit.</span></span> <span data-ttu-id="30011-121">Par exemple, étant donné la chaîne « 55 », **UFromSz** renvoie la valeur d’ensemble 55.</span><span class="sxs-lookup"><span data-stu-id="30011-121">For example, given the string "55", **UFromSz** returns the integer value 55.</span></span> <span data-ttu-id="30011-122">Étant donné la chaîne « 5a5b », la fonction renvoie la valeur d’ensemble 5.</span><span class="sxs-lookup"><span data-stu-id="30011-122">Given the string "5a5b", the function returns the integer value 5.</span></span> <span data-ttu-id="30011-123">Étant donné la chaîne « a5b5 », **UFromSz** renvoie zéro.</span><span class="sxs-lookup"><span data-stu-id="30011-123">Given the string "a5b5", **UFromSz** returns zero.</span></span> 
  
 <span data-ttu-id="30011-124">**UFromSz est** sensible aux différences diacritiques.</span><span class="sxs-lookup"><span data-stu-id="30011-124">**UFromSz** is sensitive to diacritical differences.</span></span> <span data-ttu-id="30011-125">Les chaînes aux formats Unicode et DBCS sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="30011-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="30011-126">La limite de longueur sur  _lpsz est_ en caractères, pas nécessairement en octets.</span><span class="sxs-lookup"><span data-stu-id="30011-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  

