---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: 'Last modified: February 21, 2012'
ms.openlocfilehash: 1f137aba40703fe84e5753ee6e370262f780f0a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338240"
---
# <a name="mnls_multibytetowidechar"></a><span data-ttu-id="1a452-103">MNLS_MultiByteToWideChar</span><span class="sxs-lookup"><span data-stu-id="1a452-103">MNLS_MultiByteToWideChar</span></span>

  
  
<span data-ttu-id="1a452-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a452-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a452-105">Similaire à **MultiByteToWideChar**, qui mappé une chaîne de caractères à une chaîne UTF-16 (caractère large).</span><span class="sxs-lookup"><span data-stu-id="1a452-105">Similar to **MultiByteToWideChar**, which maps a character string to a UTF-16 (wide character) string.</span></span> <span data-ttu-id="1a452-106">La chaîne de caractères n’est pas nécessairement un jeu de caractères multioctets.</span><span class="sxs-lookup"><span data-stu-id="1a452-106">The character string is not necessarily from a multibyte character set.</span></span>
  
```cpp
int MNLS_MultiByteToWideChar(
  UINT uCodePage,
  DWORD dwFlags,
  LPCSTR lpMultiByteStr,
  int cchMultiByte,
  LPWSTR lpWideCharStr,
  int cchWideChar);
```

## <a name="parameters"></a><span data-ttu-id="1a452-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="1a452-107">Parameters</span></span>

 <span data-ttu-id="1a452-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="1a452-108">_uCodePage_</span></span>
  
> <span data-ttu-id="1a452-109">[in] Page de code à utiliser lors de la conversion.</span><span class="sxs-lookup"><span data-stu-id="1a452-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="1a452-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="1a452-110">_dwFlags_</span></span>
  
> <span data-ttu-id="1a452-111">[in] Indicateurs indiquant le type de conversion.</span><span class="sxs-lookup"><span data-stu-id="1a452-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="1a452-112">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="1a452-112">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="1a452-113">[in] Pointeur vers la chaîne de caractères à convertir.</span><span class="sxs-lookup"><span data-stu-id="1a452-113">[in] Pointer to the character string to convert.</span></span>
    
 <span data-ttu-id="1a452-114">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="1a452-114">_cchMultiByte_</span></span>
  
> <span data-ttu-id="1a452-115">[in] Taille, en octets, de la chaîne indiquée par le paramètre _lpMultiByteStr._</span><span class="sxs-lookup"><span data-stu-id="1a452-115">[in] Size, in bytes, of the string indicated by the  _lpMultiByteStr_ parameter.</span></span> 
    
 <span data-ttu-id="1a452-116">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="1a452-116">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="1a452-117">[out] Facultatif.</span><span class="sxs-lookup"><span data-stu-id="1a452-117">[out] Optional.</span></span> <span data-ttu-id="1a452-118">Pointeur vers une mémoire tampon qui reçoit la chaîne convertie.</span><span class="sxs-lookup"><span data-stu-id="1a452-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="1a452-119">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="1a452-119">_cchWideChar_</span></span>
  
> <span data-ttu-id="1a452-120">[in] Taille, en caractères, de la mémoire tampon indiquée par  _lpWideCharStr_.</span><span class="sxs-lookup"><span data-stu-id="1a452-120">[in] Size, in characters, of the buffer indicated by  _lpWideCharStr_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1a452-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1a452-121">Return value</span></span>

<span data-ttu-id="1a452-122">Renvoie le nombre de caractères écrits dans la mémoire tampon indiquée par  _lpWideCharStr_ en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="1a452-122">Returns the number of characters written to the buffer indicated by  _lpWideCharStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1a452-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="1a452-123">Remarks</span></span>

<span data-ttu-id="1a452-124">Cette fonction encapsule **la fonction MultiByteToWideChar.**</span><span class="sxs-lookup"><span data-stu-id="1a452-124">This function wraps the **MultiByteToWideChar** function.</span></span> <span data-ttu-id="1a452-125">Pour plus d’informations, [voir MultiByteToWideChar](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="1a452-125">For more information, see [MultiByteToWideChar](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx).</span></span>
  

