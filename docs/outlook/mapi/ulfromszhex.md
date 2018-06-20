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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d5ba7e7bc52ba041e9fe6c9a01b35dc91d3b947b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787409"
---
# <a name="ulfromszhex"></a><span data-ttu-id="c9134-103">UlFromSzHex</span><span class="sxs-lookup"><span data-stu-id="c9134-103">UlFromSzHex</span></span>

  
  
<span data-ttu-id="c9134-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c9134-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c9134-105">Convertit une chaîne de chiffres hexadécimaux en entier long non signé.</span><span class="sxs-lookup"><span data-stu-id="c9134-105">Converts a null-terminated string of hexadecimal digits into an unsigned long integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c9134-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="c9134-106">Header file:</span></span>  <br/> |<span data-ttu-id="c9134-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c9134-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c9134-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="c9134-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c9134-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c9134-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c9134-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="c9134-110">Called by:</span></span>  <br/> |<span data-ttu-id="c9134-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="c9134-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="c9134-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9134-112">Parameters</span></span>

 <span data-ttu-id="c9134-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="c9134-113">_lpsz_</span></span>
  
> <span data-ttu-id="c9134-114">[in] Pointeur vers la chaîne à convertir.</span><span class="sxs-lookup"><span data-stu-id="c9134-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="c9134-115">Le paramètre _lpsz_ ne doit pas dépasser 65536 caractères.</span><span class="sxs-lookup"><span data-stu-id="c9134-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c9134-116">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="c9134-116">Return value</span></span>

 <span data-ttu-id="c9134-117">**UlFromSzHex** renvoie un entier long non signé.</span><span class="sxs-lookup"><span data-stu-id="c9134-117">**UlFromSzHex** returns an unsigned long integer.</span></span> <span data-ttu-id="c9134-118">Si la chaîne ne commence pas par au moins un chiffre hexadécimal, zéro est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="c9134-118">If the string does not begin with at least one hexadecimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c9134-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="c9134-119">Remarks</span></span>

<span data-ttu-id="c9134-120">La fonction **UlFromSzHex** cesse de conversion lorsqu’elle atteint le premier caractère de la chaîne n’est pas un chiffre hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="c9134-120">The **UlFromSzHex** function stops converting when it reaches the first character in the string that is not a hexadecimal digit.</span></span> <span data-ttu-id="c9134-121">Par exemple, si la chaîne « 5 », **UlFromSzHex** renvoie la valeur d’entier 90.</span><span class="sxs-lookup"><span data-stu-id="c9134-121">For example, given the string "5a", **UlFromSzHex** returns the integer value 90.</span></span> <span data-ttu-id="c9134-122">Si la chaîne « 5g5h », la fonction renvoie la valeur entière 5.</span><span class="sxs-lookup"><span data-stu-id="c9134-122">Given the string "5g5h", the function returns the integer value 5.</span></span> <span data-ttu-id="c9134-123">Si la chaîne « g5h5 », **UlFromSzHex** renvoie zéro.</span><span class="sxs-lookup"><span data-stu-id="c9134-123">Given the string "g5h5", **UlFromSzHex** returns zero.</span></span> 
  
 <span data-ttu-id="c9134-124">**UlFromSzHex** est sensible aux différences diacritiques mais « a » à « f » et « A » à « F » pour les chiffres hexadécimaux.</span><span class="sxs-lookup"><span data-stu-id="c9134-124">**UlFromSzHex** is sensitive to diacritical differences but allows both 'a' through 'f' and 'A' through 'F' for hexadecimal digits.</span></span> <span data-ttu-id="c9134-125">Chaînes dans les formats Unicode et DBCS sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c9134-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="c9134-126">La limite de longueur _lpsz_ est en caractères, pas nécessairement octets.</span><span class="sxs-lookup"><span data-stu-id="c9134-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  

