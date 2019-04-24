---
title: MNLS_WideCharToMultiByte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f64cde12-7ed1-444f-8ca4-51cb3ea514cf
description: 'Dernière modification: 21 février 2012'
ms.openlocfilehash: ad41f9b6060e5cfbabecfd9bb29a47815929d6b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338730"
---
# <a name="mnlswidechartomultibyte"></a><span data-ttu-id="e54e9-103">MNLS_WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="e54e9-103">MNLS_WideCharToMultiByte</span></span>

  
  
<span data-ttu-id="e54e9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e54e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e54e9-105">Cette fonction est similaire à **WideCharToMultiByte**, qui mappe une chaîne UTF-16 (caractères larges) à une nouvelle chaîne de caractères.</span><span class="sxs-lookup"><span data-stu-id="e54e9-105">This function is similar to **WideCharToMultiByte**, which maps a UTF-16 (wide character) string to a new character string.</span></span> <span data-ttu-id="e54e9-106">La nouvelle chaîne de caractères n'est pas nécessairement à partir d'un jeu de caractères codé sur plusieurs octets.</span><span class="sxs-lookup"><span data-stu-id="e54e9-106">The new character string is not necessarily from a multibyte character set.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="e54e9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e54e9-107">Parameters</span></span>

 <span data-ttu-id="e54e9-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="e54e9-108">_uCodePage_</span></span>
  
> <span data-ttu-id="e54e9-109">dans Page de codes à utiliser lors de la conversion.</span><span class="sxs-lookup"><span data-stu-id="e54e9-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="e54e9-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="e54e9-110">_dwFlags_</span></span>
  
> <span data-ttu-id="e54e9-111">dans Indicateurs indiquant le type de conversion.</span><span class="sxs-lookup"><span data-stu-id="e54e9-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="e54e9-112">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="e54e9-112">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="e54e9-113">dans Pointeur vers la chaîne Unicode à convertir.</span><span class="sxs-lookup"><span data-stu-id="e54e9-113">[in] Pointer to the Unicode string to convert.</span></span>
    
 <span data-ttu-id="e54e9-114">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="e54e9-114">_cchWideChar_</span></span>
  
> <span data-ttu-id="e54e9-115">dans Indicateurs indiquant le type de conversion.</span><span class="sxs-lookup"><span data-stu-id="e54e9-115">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="e54e9-116">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="e54e9-116">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="e54e9-117">[out] Facultatif.</span><span class="sxs-lookup"><span data-stu-id="e54e9-117">[out] Optional.</span></span> <span data-ttu-id="e54e9-118">Pointeur vers une mémoire tampon qui reçoit la chaîne convertie.</span><span class="sxs-lookup"><span data-stu-id="e54e9-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="e54e9-119">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="e54e9-119">_cchMultiByte_</span></span>
  
> <span data-ttu-id="e54e9-120">dans Taille, en octets, de la mémoire tampon indiquée par _lpMultiByteStr_.</span><span class="sxs-lookup"><span data-stu-id="e54e9-120">[in] Size, in bytes, of the buffer indicated by  _lpMultiByteStr_.</span></span>
    
 <span data-ttu-id="e54e9-121">_lpDefaultChar_</span><span class="sxs-lookup"><span data-stu-id="e54e9-121">_lpDefaultChar_</span></span>
  
> <span data-ttu-id="e54e9-122">[in] Facultatif.</span><span class="sxs-lookup"><span data-stu-id="e54e9-122">[in] Optional.</span></span> <span data-ttu-id="e54e9-123">Pointeur vers le caractère à utiliser si un caractère ne peut pas être représenté dans la page de codes spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e54e9-123">Pointer to the character to use if a character cannot be represented in the specified code page.</span></span>
    
 <span data-ttu-id="e54e9-124">_lpfUsedDefaultChar_</span><span class="sxs-lookup"><span data-stu-id="e54e9-124">_lpfUsedDefaultChar_</span></span>
  
> <span data-ttu-id="e54e9-125">[out] Facultatif.</span><span class="sxs-lookup"><span data-stu-id="e54e9-125">[out] Optional.</span></span> <span data-ttu-id="e54e9-126">Pointeur vers un indicateur qui indique si la fonction a utilisé un caractère par défaut dans la conversion.</span><span class="sxs-lookup"><span data-stu-id="e54e9-126">Pointer to a flag that indicates if the function has used a default character in the conversion.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e54e9-127">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e54e9-127">Return value</span></span>

<span data-ttu-id="e54e9-128">Renvoie le nombre d'octets écrits dans la mémoire tampon vers laquelle pointe _lpMultiByteStr_ en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="e54e9-128">Returns the number of bytes written to the buffer pointed to by  _lpMultiByteStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e54e9-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="e54e9-129">Remarks</span></span>

<span data-ttu-id="e54e9-130">Cette fonction encapsule la fonction **WideCharToMultiByte** .</span><span class="sxs-lookup"><span data-stu-id="e54e9-130">This function wraps the **WideCharToMultiByte** function.</span></span> <span data-ttu-id="e54e9-131">Pour plus d'informations, consultez la rubrique [WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e54e9-131">For more information, see [WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e54e9-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e54e9-132">See also</span></span>



[<span data-ttu-id="e54e9-133">WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="e54e9-133">WideCharToMultiByte</span></span>](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx)

