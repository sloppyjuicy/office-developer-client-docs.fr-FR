---
title: SzFindLastCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindLastCh
api_type:
- COM
ms.assetid: 7c3e5a71-7b78-4328-b8ee-265cc4da4be5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f22d30c1bc7c797834f58bcd1306b14ac2542c6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421255"
---
# <a name="szfindlastch"></a><span data-ttu-id="089dd-103">SzFindLastCh</span><span class="sxs-lookup"><span data-stu-id="089dd-103">SzFindLastCh</span></span>

  
  
<span data-ttu-id="089dd-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="089dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="089dd-105">Recherche la dernière occurrence d'un caractère dans une chaîne terminée par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="089dd-105">Searches for the last occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="089dd-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="089dd-106">Header file:</span></span>  <br/> |<span data-ttu-id="089dd-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="089dd-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="089dd-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="089dd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="089dd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="089dd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="089dd-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="089dd-110">Called by:</span></span>  <br/> |<span data-ttu-id="089dd-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="089dd-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindLastCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="089dd-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="089dd-112">Parameters</span></span>

 <span data-ttu-id="089dd-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="089dd-113">_lpsz_</span></span>
  
> <span data-ttu-id="089dd-114">dans Pointeur vers la chaîne terminée par un caractère null à rechercher.</span><span class="sxs-lookup"><span data-stu-id="089dd-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
 <span data-ttu-id="089dd-115">_ch_</span><span class="sxs-lookup"><span data-stu-id="089dd-115">_ch_</span></span>
  
> <span data-ttu-id="089dd-116">dans Caractère à rechercher.</span><span class="sxs-lookup"><span data-stu-id="089dd-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="089dd-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="089dd-117">Return value</span></span>

 <span data-ttu-id="089dd-118">**SzFindLastCh** renvoie un pointeur vers la dernière occurrence du caractère dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="089dd-118">**SzFindLastCh** returns a pointer to the last occurrence of the character in the string.</span></span> <span data-ttu-id="089dd-119">Si le caractère ne se produit nulle part dans la chaîne, ou si le paramètre _lpsz_ est null, la valeur null est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="089dd-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="089dd-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="089dd-120">Remarks</span></span>

<span data-ttu-id="089dd-121">La fonction **SzFindLastCh** recherche une correspondance exacte uniquement; elle est sensible à la casse et aux différences diacritiques.</span><span class="sxs-lookup"><span data-stu-id="089dd-121">The **SzFindLastCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="089dd-122">Les recherches dans les formats Unicode et DBCS sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="089dd-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

