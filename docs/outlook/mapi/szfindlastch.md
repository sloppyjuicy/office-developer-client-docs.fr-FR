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
# <a name="szfindlastch"></a><span data-ttu-id="89027-103">SzFindLastCh</span><span class="sxs-lookup"><span data-stu-id="89027-103">SzFindLastCh</span></span>

  
  
<span data-ttu-id="89027-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89027-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89027-105">Recherche la dernière occurrence d’un caractère dans une chaîne terminée par null.</span><span class="sxs-lookup"><span data-stu-id="89027-105">Searches for the last occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="89027-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="89027-106">Header file:</span></span>  <br/> |<span data-ttu-id="89027-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="89027-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="89027-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="89027-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="89027-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="89027-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="89027-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="89027-110">Called by:</span></span>  <br/> |<span data-ttu-id="89027-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="89027-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindLastCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="89027-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="89027-112">Parameters</span></span>

 <span data-ttu-id="89027-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="89027-113">_lpsz_</span></span>
  
> <span data-ttu-id="89027-114">[in] Pointeur vers la chaîne terminée par null à rechercher.</span><span class="sxs-lookup"><span data-stu-id="89027-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
 <span data-ttu-id="89027-115">_ch_</span><span class="sxs-lookup"><span data-stu-id="89027-115">_ch_</span></span>
  
> <span data-ttu-id="89027-116">[in] Caractère à rechercher.</span><span class="sxs-lookup"><span data-stu-id="89027-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="89027-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="89027-117">Return value</span></span>

 <span data-ttu-id="89027-118">**SzFindLastCh** renvoie un pointeur vers la dernière occurrence du caractère dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="89027-118">**SzFindLastCh** returns a pointer to the last occurrence of the character in the string.</span></span> <span data-ttu-id="89027-119">Si le caractère ne se produit nulle part dans la chaîne, ou si le paramètre  _lpsz_ est NULL, une valeur NULL est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="89027-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="89027-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="89027-120">Remarks</span></span>

<span data-ttu-id="89027-121">La **fonction SzFindLastCh** recherche uniquement une correspondance exacte . il est sensible aux différences diacritiques et de cas.</span><span class="sxs-lookup"><span data-stu-id="89027-121">The **SzFindLastCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="89027-122">Les recherches dans les formats Unicode et DBCS sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="89027-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

