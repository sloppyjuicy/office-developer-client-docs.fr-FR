---
title: UlFromSzHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlFromSzHex
api_type:
- COM
ms.assetid: e2d6b6bf-f96d-460c-859a-21961ac9237c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 950f5513696a9dd9d52db7b7ee912d3f7d12cc48
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433051"
---
# <a name="ulfromszhex"></a><span data-ttu-id="5d12e-103">UlFromSzHex</span><span class="sxs-lookup"><span data-stu-id="5d12e-103">UlFromSzHex</span></span>

  
  
<span data-ttu-id="5d12e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d12e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d12e-105">ConVertit une chaîne terminée par un caractère null de chiffres hexadécimaux en un entier long non signé.</span><span class="sxs-lookup"><span data-stu-id="5d12e-105">Converts a null-terminated string of hexadecimal digits into an unsigned long integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5d12e-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="5d12e-106">Header file:</span></span>  <br/> |<span data-ttu-id="5d12e-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5d12e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5d12e-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="5d12e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5d12e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5d12e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5d12e-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="5d12e-110">Called by:</span></span>  <br/> |<span data-ttu-id="5d12e-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="5d12e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="5d12e-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d12e-112">Parameters</span></span>

 <span data-ttu-id="5d12e-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="5d12e-113">_lpsz_</span></span>
  
> <span data-ttu-id="5d12e-114">dans Pointeur vers la chaîne terminée par un caractère null à convertir.</span><span class="sxs-lookup"><span data-stu-id="5d12e-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="5d12e-115">Le paramètre _lpsz_ ne doit pas dépasser 65536 caractères.</span><span class="sxs-lookup"><span data-stu-id="5d12e-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5d12e-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5d12e-116">Return value</span></span>

 <span data-ttu-id="5d12e-117">**UlFromSzHex** renvoie un entier long non signé.</span><span class="sxs-lookup"><span data-stu-id="5d12e-117">**UlFromSzHex** returns an unsigned long integer.</span></span> <span data-ttu-id="5d12e-118">Si la chaîne ne commence pas par au moins un chiffre hexadécimal, zéro est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="5d12e-118">If the string does not begin with at least one hexadecimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5d12e-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="5d12e-119">Remarks</span></span>

<span data-ttu-id="5d12e-120">La fonction **UlFromSzHex** arrête la conversion lorsqu'elle atteint le premier caractère de la chaîne qui n'est pas un chiffre hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="5d12e-120">The **UlFromSzHex** function stops converting when it reaches the first character in the string that is not a hexadecimal digit.</span></span> <span data-ttu-id="5d12e-121">Par exemple, en fonction de la chaîne «5a», **UlFromSzHex** renvoie la valeur entière 90.</span><span class="sxs-lookup"><span data-stu-id="5d12e-121">For example, given the string "5a", **UlFromSzHex** returns the integer value 90.</span></span> <span data-ttu-id="5d12e-122">Étant donné la chaîne «5g5h», la fonction renvoie la valeur entière 5.</span><span class="sxs-lookup"><span data-stu-id="5d12e-122">Given the string "5g5h", the function returns the integer value 5.</span></span> <span data-ttu-id="5d12e-123">Étant donné la chaîne «g5h5», **UlFromSzHex** renvoie zéro.</span><span class="sxs-lookup"><span data-stu-id="5d12e-123">Given the string "g5h5", **UlFromSzHex** returns zero.</span></span> 
  
 <span data-ttu-id="5d12e-124">**UlFromSzHex** est sensible aux différences diacritiques, mais autorise «a» à «f» et «a» À «f» pour les chiffres hexadécimaux.</span><span class="sxs-lookup"><span data-stu-id="5d12e-124">**UlFromSzHex** is sensitive to diacritical differences but allows both 'a' through 'f' and 'A' through 'F' for hexadecimal digits.</span></span> <span data-ttu-id="5d12e-125">Les chaînes au format Unicode et DBCS sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="5d12e-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="5d12e-126">La limite de longueur sur _lpsz_ est exprimée en caractères, pas nécessairement en octets.</span><span class="sxs-lookup"><span data-stu-id="5d12e-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  

