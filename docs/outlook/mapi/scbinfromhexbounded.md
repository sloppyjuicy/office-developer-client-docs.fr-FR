---
title: ScBinFromHexBounded
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScBinFromHexBounded
api_type:
- COM
ms.assetid: edac715c-6edb-4b05-82e5-c08c3c7cb6d4
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a00a9b2200f76dfd600f72bf387467b5792599c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787053"
---
# <a name="scbinfromhexbounded"></a><span data-ttu-id="6122d-103">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="6122d-103">ScBinFromHexBounded</span></span>

  
  
<span data-ttu-id="6122d-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6122d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6122d-105">Convertit la partie spécifiée d’une représentation de chaîne d’un nombre hexadécimal en nombre binaire.</span><span class="sxs-lookup"><span data-stu-id="6122d-105">Converts the specified portion of a string representation of a hexadecimal number into a binary number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6122d-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="6122d-106">Header file:</span></span>  <br/> |<span data-ttu-id="6122d-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="6122d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="6122d-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="6122d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6122d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6122d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6122d-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="6122d-110">Called by:</span></span>  <br/> |<span data-ttu-id="6122d-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="6122d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a><span data-ttu-id="6122d-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6122d-112">Parameters</span></span>

 <span data-ttu-id="6122d-113">_sz_</span><span class="sxs-lookup"><span data-stu-id="6122d-113">_sz_</span></span>
  
> <span data-ttu-id="6122d-114">[in] Pointeur vers la chaîne à convertir.</span><span class="sxs-lookup"><span data-stu-id="6122d-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="6122d-115">Caractères valides incluent les caractères hexadécimaux 0 à 9 et les deux caractères majuscules et minuscules d’a à f.</span><span class="sxs-lookup"><span data-stu-id="6122d-115">Valid characters include the hexadecimal characters 0 through 9 and both uppercase and lowercase characters a through f.</span></span>
    
 <span data-ttu-id="6122d-116">_pb_</span><span class="sxs-lookup"><span data-stu-id="6122d-116">_pb_</span></span>
  
> <span data-ttu-id="6122d-117">[out] Pointeur vers le nombre binaire renvoyé.</span><span class="sxs-lookup"><span data-stu-id="6122d-117">[out] Pointer to the returned binary number.</span></span>
    
 <span data-ttu-id="6122d-118">_cb_</span><span class="sxs-lookup"><span data-stu-id="6122d-118">_cb_</span></span>
  
> <span data-ttu-id="6122d-119">[in] Taille, en octets, du paramètre _po_ .</span><span class="sxs-lookup"><span data-stu-id="6122d-119">[in] Size, in bytes, of the  _pb_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6122d-120">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="6122d-120">Return value</span></span>

<span data-ttu-id="6122d-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="6122d-121">S_OK</span></span>
  
> <span data-ttu-id="6122d-122">Conversion a réussi.</span><span class="sxs-lookup"><span data-stu-id="6122d-122">Conversion was successful.</span></span>
    
<span data-ttu-id="6122d-123">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="6122d-123">MAPI_E_CALL_FAILED</span></span>
  
> <span data-ttu-id="6122d-124">Caractères non valides se sont produites.</span><span class="sxs-lookup"><span data-stu-id="6122d-124">Invalid characters were encountered.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6122d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6122d-125">See also</span></span>



[<span data-ttu-id="6122d-126">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="6122d-126">FBinFromHex</span></span>](fbinfromhex.md)

