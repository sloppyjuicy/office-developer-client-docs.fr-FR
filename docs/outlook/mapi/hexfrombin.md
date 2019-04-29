---
title: HexFromBin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HexFromBin
api_type:
- COM
ms.assetid: 12b95657-1926-4a24-be63-40305ea6f990
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a1bf02de914865e27c8c018aba8695c858888ae2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412575"
---
# <a name="hexfrombin"></a><span data-ttu-id="666ae-103">HexFromBin</span><span class="sxs-lookup"><span data-stu-id="666ae-103">HexFromBin</span></span>

  
  
<span data-ttu-id="666ae-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="666ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="666ae-105">ConVertit un nombre binaire en une représentation sous forme de chaîne d'un nombre hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="666ae-105">Converts a binary number into a string representation of a hexadecimal number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="666ae-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="666ae-106">Header file:</span></span>  <br/> |<span data-ttu-id="666ae-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="666ae-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="666ae-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="666ae-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="666ae-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="666ae-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="666ae-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="666ae-110">Called by:</span></span>  <br/> |<span data-ttu-id="666ae-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="666ae-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a><span data-ttu-id="666ae-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="666ae-112">Parameters</span></span>

 <span data-ttu-id="666ae-113">_pb_</span><span class="sxs-lookup"><span data-stu-id="666ae-113">_pb_</span></span>
  
> <span data-ttu-id="666ae-114">dans Pointeur vers les données binaires à convertir.</span><span class="sxs-lookup"><span data-stu-id="666ae-114">[in] Pointer to the binary data to be converted.</span></span> 
    
 <span data-ttu-id="666ae-115">_cb_</span><span class="sxs-lookup"><span data-stu-id="666ae-115">_cb_</span></span>
  
> <span data-ttu-id="666ae-116">dans Taille, en octets, des données binaires auxquelles pointe le paramètre _PB_ .</span><span class="sxs-lookup"><span data-stu-id="666ae-116">[in] Size, in bytes, of the binary data pointed to by the  _pb_ parameter.</span></span> 
    
 <span data-ttu-id="666ae-117">_t_</span><span class="sxs-lookup"><span data-stu-id="666ae-117">_sz_</span></span>
  
> <span data-ttu-id="666ae-118">remarquer Pointeur vers une chaîne ASCII terminée par un caractère null qui représente les données binaires dans des chiffres hexadécimaux.</span><span class="sxs-lookup"><span data-stu-id="666ae-118">[out] Pointer to a null-terminated ASCII string representing the binary data in hexadecimal digits.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="666ae-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="666ae-119">Return value</span></span>

<span data-ttu-id="666ae-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="666ae-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="666ae-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="666ae-121">Remarks</span></span>

<span data-ttu-id="666ae-122">La fonction **HexFromBin** prend un pointeur vers une unité de données binaires dont la taille est indiquée par le paramètre _CB_ .</span><span class="sxs-lookup"><span data-stu-id="666ae-122">The **HexFromBin** function takes a pointer to a unit of binary data whose size is indicated by the  _cb_ parameter.</span></span> <span data-ttu-id="666ae-123">Elle retourne dans la chaîne _SZ_ , dans (2 \* _CB_) + 1 octets de mémoire, une représentation de ces informations binaires dans des nombres hexadécimaux.</span><span class="sxs-lookup"><span data-stu-id="666ae-123">It returns in the  _sz_ string, within (2\*  _cb_)+1 bytes of memory, a representation of this binary information in hexadecimal numbers.</span></span> <span data-ttu-id="666ae-124">Si la valeur Byte est de 10 décimal, par exemple, la chaîne hexadécimale sera 0A, un octet convertit en deux octets dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="666ae-124">If the byte value is decimal 10, for example, the hexadecimal string will be 0A, so one byte converts to two bytes in the string.</span></span> 
  

