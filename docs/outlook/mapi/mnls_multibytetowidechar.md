---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: 'Dernière modification : 21 février 2012'
ms.openlocfilehash: 66e8c3b61caac6fb8d8b57d74ade6fa8aac3a9dd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571704"
---
# <a name="mnlsmultibytetowidechar"></a><span data-ttu-id="f3549-103">MNLS_MultiByteToWideChar</span><span class="sxs-lookup"><span data-stu-id="f3549-103">MNLS_MultiByteToWideChar</span></span>

  
  
<span data-ttu-id="f3549-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3549-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3549-105">Semblable à **MultiByteToWideChar**qui mappe une chaîne de caractères en une chaîne UTF-16 (caractères étendus).</span><span class="sxs-lookup"><span data-stu-id="f3549-105">Similar to **MultiByteToWideChar**, which maps a character string to a UTF-16 (wide character) string.</span></span> <span data-ttu-id="f3549-106">La chaîne de caractères est pas nécessairement à partir d’un caractère multi-octets définie.</span><span class="sxs-lookup"><span data-stu-id="f3549-106">The character string is not necessarily from a multibyte character set.</span></span>
  
```cpp
int MNLS_MultiByteToWideChar(
  UINT uCodePage,
  DWORD dwFlags,
  LPCSTR lpMultiByteStr,
  int cchMultiByte,
  LPWSTR lpWideCharStr,
  int cchWideChar);
```

## <a name="parameters"></a><span data-ttu-id="f3549-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3549-107">Parameters</span></span>

 <span data-ttu-id="f3549-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="f3549-108">_uCodePage_</span></span>
  
> <span data-ttu-id="f3549-109">[in] Page de codes à utiliser lors de la conversion.</span><span class="sxs-lookup"><span data-stu-id="f3549-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="f3549-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="f3549-110">_dwFlags_</span></span>
  
> <span data-ttu-id="f3549-111">[in] Indicateurs indiquant le type de conversion.</span><span class="sxs-lookup"><span data-stu-id="f3549-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="f3549-112">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="f3549-112">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="f3549-113">[in] Pointeur vers la chaîne de caractères à convertir.</span><span class="sxs-lookup"><span data-stu-id="f3549-113">[in] Pointer to the character string to convert.</span></span>
    
 <span data-ttu-id="f3549-114">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="f3549-114">_cchMultiByte_</span></span>
  
> <span data-ttu-id="f3549-115">[in] Taille, en octets, de la chaîne indiquée par le paramètre _lpMultiByteStr_ .</span><span class="sxs-lookup"><span data-stu-id="f3549-115">[in] Size, in bytes, of the string indicated by the  _lpMultiByteStr_ parameter.</span></span> 
    
 <span data-ttu-id="f3549-116">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="f3549-116">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="f3549-117">[out] Facultatif.</span><span class="sxs-lookup"><span data-stu-id="f3549-117">[out] Optional.</span></span> <span data-ttu-id="f3549-118">Pointeur vers un tampon qui reçoit la chaîne convertie.</span><span class="sxs-lookup"><span data-stu-id="f3549-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="f3549-119">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="f3549-119">_cchWideChar_</span></span>
  
> <span data-ttu-id="f3549-120">[in] Taille, en caractères, de la mémoire tampon indiquée par _lpWideCharStr_.</span><span class="sxs-lookup"><span data-stu-id="f3549-120">[in] Size, in characters, of the buffer indicated by  _lpWideCharStr_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f3549-121">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="f3549-121">Return value</span></span>

<span data-ttu-id="f3549-122">Renvoie le nombre de caractères écrits dans la mémoire tampon de la mention _lpWideCharStr_ si l’opération réussit.</span><span class="sxs-lookup"><span data-stu-id="f3549-122">Returns the number of characters written to the buffer indicated by  _lpWideCharStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f3549-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="f3549-123">Remarks</span></span>

<span data-ttu-id="f3549-124">Cette fonction encapsule la fonction **MultiByteToWideChar** .</span><span class="sxs-lookup"><span data-stu-id="f3549-124">This function wraps the **MultiByteToWideChar** function.</span></span> <span data-ttu-id="f3549-125">Pour plus d’informations, voir [MultiByteToWideChar](http://msdn.microsoft.com/en-us/library/dd319072%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f3549-125">For more information, see [MultiByteToWideChar](http://msdn.microsoft.com/en-us/library/dd319072%28VS.85%29.aspx).</span></span>
  

