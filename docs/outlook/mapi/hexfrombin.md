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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c1d333c7c019c30c3f6c6b3567453f2f022d4b5d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783482"
---
# <a name="hexfrombin"></a><span data-ttu-id="eb98d-103">HexFromBin</span><span class="sxs-lookup"><span data-stu-id="eb98d-103">HexFromBin</span></span>

  
  
<span data-ttu-id="eb98d-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eb98d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eb98d-105">Convertit un nombre binaire en une représentation de chaîne d’un nombre hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="eb98d-105">Converts a binary number into a string representation of a hexadecimal number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eb98d-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="eb98d-106">Header file:</span></span>  <br/> |<span data-ttu-id="eb98d-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="eb98d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="eb98d-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="eb98d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="eb98d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="eb98d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="eb98d-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="eb98d-110">Called by:</span></span>  <br/> |<span data-ttu-id="eb98d-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="eb98d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a><span data-ttu-id="eb98d-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb98d-112">Parameters</span></span>

 <span data-ttu-id="eb98d-113">_pb_</span><span class="sxs-lookup"><span data-stu-id="eb98d-113">_pb_</span></span>
  
> <span data-ttu-id="eb98d-114">[in] Pointeur vers les données binaires à convertir.</span><span class="sxs-lookup"><span data-stu-id="eb98d-114">[in] Pointer to the binary data to be converted.</span></span> 
    
 <span data-ttu-id="eb98d-115">_cb_</span><span class="sxs-lookup"><span data-stu-id="eb98d-115">_cb_</span></span>
  
> <span data-ttu-id="eb98d-116">[in] Taille, en octets, des données binaires vers laquelle pointe le paramètre _po_ .</span><span class="sxs-lookup"><span data-stu-id="eb98d-116">[in] Size, in bytes, of the binary data pointed to by the  _pb_ parameter.</span></span> 
    
 <span data-ttu-id="eb98d-117">_sz_</span><span class="sxs-lookup"><span data-stu-id="eb98d-117">_sz_</span></span>
  
> <span data-ttu-id="eb98d-118">[out] Pointeur vers une chaîne qui représente les données binaires de chiffres hexadécimaux ASCII terminée.</span><span class="sxs-lookup"><span data-stu-id="eb98d-118">[out] Pointer to a null-terminated ASCII string representing the binary data in hexadecimal digits.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="eb98d-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="eb98d-119">Return value</span></span>

<span data-ttu-id="eb98d-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="eb98d-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eb98d-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="eb98d-121">Remarks</span></span>

<span data-ttu-id="eb98d-122">La fonction **HexFromBin** prend un pointeur vers une unité de données binaires dont la taille est indiquée par le paramètre _cb_ .</span><span class="sxs-lookup"><span data-stu-id="eb98d-122">The **HexFromBin** function takes a pointer to a unit of binary data whose size is indicated by the  _cb_ parameter.</span></span> <span data-ttu-id="eb98d-123">Elle renvoie au sein de la chaîne _sz_ , (2 \* _cb_) + 1 octets de mémoire, une représentation de ces informations binaires en nombre hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="eb98d-123">It returns in the  _sz_ string, within (2\*  _cb_)+1 bytes of memory, a representation of this binary information in hexadecimal numbers.</span></span> <span data-ttu-id="eb98d-124">Si la valeur d’octet est 10 décimal, par exemple, la chaîne hexadécimale sera 0, 1 octet tel convertit sur deux octets dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="eb98d-124">If the byte value is decimal 10, for example, the hexadecimal string will be 0A, so one byte converts to two bytes in the string.</span></span> 
  

