---
title: MNLS_WideCharToMultiByte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f64cde12-7ed1-444f-8ca4-51cb3ea514cf
description: 'Dernière modification : 21 février 2012'
ms.openlocfilehash: f5cb63ca3d421073b00a448f762ecf0137494f2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784909"
---
# <a name="mnlswidechartomultibyte"></a><span data-ttu-id="1c4a6-103">MNLS_WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="1c4a6-103">MNLS_WideCharToMultiByte</span></span>

  
  
<span data-ttu-id="1c4a6-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1c4a6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1c4a6-105">Cette fonction est similaire à **WideCharToMultiByte**qui mappe la chaîne UTF-16 (caractères étendus) avec une nouvelle chaîne de caractères.</span><span class="sxs-lookup"><span data-stu-id="1c4a6-105">This function is similar to **WideCharToMultiByte**, which maps a UTF-16 (wide character) string to a new character string.</span></span> <span data-ttu-id="1c4a6-106">La nouvelle chaîne de caractères est pas nécessairement à partir d’un caractère multi-octets définie.</span><span class="sxs-lookup"><span data-stu-id="1c4a6-106">The new character string is not necessarily from a multibyte character set.</span></span>
  
```cpp
int MNLS_WideCharToMultiByte(
  UINT uCodePage,
  DWORD dwFlags,
  LPCWSTR lpWideCharStr,
  int cchWideChar,
  LPSTR lpMultiByteStr,
  int cchMultiByte,
  LPCSTR lpDefaultChar,
  BOOL FAR *lpfUsedDefaultChar);
```

## <a name="parameters"></a><span data-ttu-id="1c4a6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c4a6-107">Parameters</span></span>

 <span data-ttu-id="1c4a6-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="1c4a6-108">_uCodePage_</span></span>
  
> <span data-ttu-id="1c4a6-109">[in] Page de codes à utiliser lors de la conversion.</span><span class="sxs-lookup"><span data-stu-id="1c4a6-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="1c4a6-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="1c4a6-110">_dwFlags_</span></span>
  
> <span data-ttu-id="1c4a6-111">[in] Indicateurs indiquant le type de conversion.</span><span class="sxs-lookup"><span data-stu-id="1c4a6-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="1c4a6-112">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="1c4a6-112">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="1c4a6-113">[in] Pointeur vers la chaîne Unicode à convertir.</span><span class="sxs-lookup"><span data-stu-id="1c4a6-113">[in] Pointer to the Unicode string to convert.</span></span>
    
 <span data-ttu-id="1c4a6-114">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="1c4a6-114">_cchWideChar_</span></span>
  
> <span data-ttu-id="1c4a6-115">[in] Indicateurs indiquant le type de conversion.</span><span class="sxs-lookup"><span data-stu-id="1c4a6-115">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="1c4a6-116">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="1c4a6-116">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="1c4a6-117">[out] Facultatif.</span><span class="sxs-lookup"><span data-stu-id="1c4a6-117">[out] Optional.</span></span> <span data-ttu-id="1c4a6-118">Pointeur vers un tampon qui reçoit la chaîne convertie.</span><span class="sxs-lookup"><span data-stu-id="1c4a6-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="1c4a6-119">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="1c4a6-119">_cchMultiByte_</span></span>
  
> <span data-ttu-id="1c4a6-120">[in] Taille, en octets, de la mémoire tampon indiquée par _lpMultiByteStr_.</span><span class="sxs-lookup"><span data-stu-id="1c4a6-120">[in] Size, in bytes, of the buffer indicated by  _lpMultiByteStr_.</span></span>
    
 <span data-ttu-id="1c4a6-121">_lpDefaultChar_</span><span class="sxs-lookup"><span data-stu-id="1c4a6-121">_lpDefaultChar_</span></span>
  
> <span data-ttu-id="1c4a6-122">[in] Facultatif.</span><span class="sxs-lookup"><span data-stu-id="1c4a6-122">[in] Optional.</span></span> <span data-ttu-id="1c4a6-123">Pointeur vers le caractère à utiliser si un caractère ne peut pas être représenté dans la page de code spécifié.</span><span class="sxs-lookup"><span data-stu-id="1c4a6-123">Pointer to the character to use if a character cannot be represented in the specified code page.</span></span>
    
 <span data-ttu-id="1c4a6-124">_lpfUsedDefaultChar_</span><span class="sxs-lookup"><span data-stu-id="1c4a6-124">_lpfUsedDefaultChar_</span></span>
  
> <span data-ttu-id="1c4a6-125">[out] Facultatif.</span><span class="sxs-lookup"><span data-stu-id="1c4a6-125">[out] Optional.</span></span> <span data-ttu-id="1c4a6-126">Pointeur vers un indicateur qui indique si la fonction a utilisé un caractère par défaut lors de la conversion.</span><span class="sxs-lookup"><span data-stu-id="1c4a6-126">Pointer to a flag that indicates if the function has used a default character in the conversion.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1c4a6-127">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="1c4a6-127">Return value</span></span>

<span data-ttu-id="1c4a6-128">Renvoie le nombre d’octets écrits dans la mémoire tampon vers laquelle pointée _lpMultiByteStr_ si l’opération réussit.</span><span class="sxs-lookup"><span data-stu-id="1c4a6-128">Returns the number of bytes written to the buffer pointed to by  _lpMultiByteStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1c4a6-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="1c4a6-129">Remarks</span></span>

<span data-ttu-id="1c4a6-130">Cette fonction encapsule la fonction **WideCharToMultiByte** .</span><span class="sxs-lookup"><span data-stu-id="1c4a6-130">This function wraps the **WideCharToMultiByte** function.</span></span> <span data-ttu-id="1c4a6-131">Pour plus d’informations, voir [WideCharToMultiByte](http://msdn.microsoft.com/fr-fr/library/dd374130%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="1c4a6-131">For more information, see [WideCharToMultiByte](http://msdn.microsoft.com/fr-fr/library/dd374130%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1c4a6-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c4a6-132">See also</span></span>



[<span data-ttu-id="1c4a6-133">WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="1c4a6-133">WideCharToMultiByte</span></span>](http://msdn.microsoft.com/fr-fr/library/dd374130%28VS.85%29.aspx)

