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
# <a name="hexfrombin"></a><span data-ttu-id="23a98-103">HexFromBin</span><span class="sxs-lookup"><span data-stu-id="23a98-103">HexFromBin</span></span>

  
  
<span data-ttu-id="23a98-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23a98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23a98-105">Convertit un nombre binaire en une représentation sous forme de chaîne d’un nombre hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="23a98-105">Converts a binary number into a string representation of a hexadecimal number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="23a98-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="23a98-106">Header file:</span></span>  <br/> |<span data-ttu-id="23a98-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="23a98-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="23a98-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="23a98-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="23a98-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="23a98-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="23a98-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="23a98-110">Called by:</span></span>  <br/> |<span data-ttu-id="23a98-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="23a98-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a><span data-ttu-id="23a98-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23a98-112">Parameters</span></span>

 <span data-ttu-id="23a98-113">_pb_</span><span class="sxs-lookup"><span data-stu-id="23a98-113">_pb_</span></span>
  
> <span data-ttu-id="23a98-114">[in] Pointeur vers les données binaires à convertir.</span><span class="sxs-lookup"><span data-stu-id="23a98-114">[in] Pointer to the binary data to be converted.</span></span> 
    
 <span data-ttu-id="23a98-115">_cb_</span><span class="sxs-lookup"><span data-stu-id="23a98-115">_cb_</span></span>
  
> <span data-ttu-id="23a98-116">[in] Taille, en octets, des données binaires pointées par le _paramètre pb._</span><span class="sxs-lookup"><span data-stu-id="23a98-116">[in] Size, in bytes, of the binary data pointed to by the  _pb_ parameter.</span></span> 
    
 <span data-ttu-id="23a98-117">_sz_</span><span class="sxs-lookup"><span data-stu-id="23a98-117">_sz_</span></span>
  
> <span data-ttu-id="23a98-118">[out] Pointeur vers une chaîne ASCII terminée par null représentant les données binaires en chiffres hexadécimals.</span><span class="sxs-lookup"><span data-stu-id="23a98-118">[out] Pointer to a null-terminated ASCII string representing the binary data in hexadecimal digits.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="23a98-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="23a98-119">Return value</span></span>

<span data-ttu-id="23a98-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="23a98-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="23a98-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="23a98-121">Remarks</span></span>

<span data-ttu-id="23a98-122">La **fonction HexFromBin** prend un pointeur vers une unité de données binaires dont la taille est indiquée par le _paramètre cb._</span><span class="sxs-lookup"><span data-stu-id="23a98-122">The **HexFromBin** function takes a pointer to a unit of binary data whose size is indicated by the  _cb_ parameter.</span></span> <span data-ttu-id="23a98-123">Elle renvoie dans la chaîne  _sz,_ dans (2\*  _cb_)+1 octets de mémoire, une représentation de ces informations binaires en nombres hexadécimals.</span><span class="sxs-lookup"><span data-stu-id="23a98-123">It returns in the  _sz_ string, within (2\*  _cb_)+1 bytes of memory, a representation of this binary information in hexadecimal numbers.</span></span> <span data-ttu-id="23a98-124">Si la valeur d’octet est décimale 10, par exemple, la chaîne hexadécimale sera 0A, de sorte qu’un octet est converti en deux octets dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="23a98-124">If the byte value is decimal 10, for example, the hexadecimal string will be 0A, so one byte converts to two bytes in the string.</span></span> 
  

