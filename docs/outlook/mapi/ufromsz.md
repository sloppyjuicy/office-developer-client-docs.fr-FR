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
ms.openlocfilehash: 7513e361f4c1c1bcc93cc420f3a1987e0d817c54
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580501"
---
# <a name="ufromsz"></a><span data-ttu-id="19eea-103">UFromSz</span><span class="sxs-lookup"><span data-stu-id="19eea-103">UFromSz</span></span>

  
  
<span data-ttu-id="19eea-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19eea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19eea-105">Convertit une chaîne de chiffres décimaux en entier non signé.</span><span class="sxs-lookup"><span data-stu-id="19eea-105">Converts a null-terminated string of decimal digits into an unsigned integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="19eea-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="19eea-106">Header file:</span></span>  <br/> |<span data-ttu-id="19eea-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="19eea-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="19eea-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="19eea-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="19eea-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="19eea-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="19eea-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="19eea-110">Called by:</span></span>  <br/> |<span data-ttu-id="19eea-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="19eea-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="19eea-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19eea-112">Parameters</span></span>

 <span data-ttu-id="19eea-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="19eea-113">_lpsz_</span></span>
  
> <span data-ttu-id="19eea-114">[in] Pointeur vers la chaîne à convertir.</span><span class="sxs-lookup"><span data-stu-id="19eea-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="19eea-115">Le paramètre _lpsz_ ne doit pas dépasser 65536 caractères.</span><span class="sxs-lookup"><span data-stu-id="19eea-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="19eea-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="19eea-116">Return value</span></span>

 <span data-ttu-id="19eea-117">**UFromSz** renvoie un entier non signé.</span><span class="sxs-lookup"><span data-stu-id="19eea-117">**UFromSz** returns an unsigned integer.</span></span> <span data-ttu-id="19eea-118">Si la chaîne ne commence pas par au moins un chiffre, zéro est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="19eea-118">If the string does not begin with at least one decimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="19eea-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="19eea-119">Remarks</span></span>

<span data-ttu-id="19eea-120">La fonction **UFromSz** cesse de conversion lorsqu’elle atteint le premier caractère de la chaîne qui n’est pas un nombre décimal.</span><span class="sxs-lookup"><span data-stu-id="19eea-120">The **UFromSz** function stops converting when it reaches the first character in the string that is not a decimal digit.</span></span> <span data-ttu-id="19eea-121">Par exemple, si la chaîne « 55 », **UFromSz** renvoie la valeur d’entier 55.</span><span class="sxs-lookup"><span data-stu-id="19eea-121">For example, given the string "55", **UFromSz** returns the integer value 55.</span></span> <span data-ttu-id="19eea-122">Si la chaîne « 5a5b », la fonction renvoie la valeur entière 5.</span><span class="sxs-lookup"><span data-stu-id="19eea-122">Given the string "5a5b", the function returns the integer value 5.</span></span> <span data-ttu-id="19eea-123">Si la chaîne « a5b5 », **UFromSz** renvoie zéro.</span><span class="sxs-lookup"><span data-stu-id="19eea-123">Given the string "a5b5", **UFromSz** returns zero.</span></span> 
  
 <span data-ttu-id="19eea-124">**UFromSz** est sensible aux différences diacritiques.</span><span class="sxs-lookup"><span data-stu-id="19eea-124">**UFromSz** is sensitive to diacritical differences.</span></span> <span data-ttu-id="19eea-125">Chaînes dans les formats Unicode et DBCS sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="19eea-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="19eea-126">La limite de longueur _lpsz_ est en caractères, pas nécessairement octets.</span><span class="sxs-lookup"><span data-stu-id="19eea-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  

