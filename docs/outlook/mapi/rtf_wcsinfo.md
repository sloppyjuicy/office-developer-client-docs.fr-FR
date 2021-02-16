---
title: RTF_WCSINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c94501e-0ec7-e836-33a7-adcf5a61b375
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6bec29aa0e88e0224f9cd6049553f2df6379e23d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430531"
---
# <a name="rtf_wcsinfo"></a><span data-ttu-id="7db0b-103">RTF_WCSINFO</span><span class="sxs-lookup"><span data-stu-id="7db0b-103">RTF_WCSINFO</span></span>

  
  
<span data-ttu-id="7db0b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7db0b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7db0b-105">Cette structure vous permet de spécifier des informations pour décompresser le corps d’un message au format RTF (Compressed Rich Text Format) et, éventuellement, de renvoyer le flux de corps dans son format natif.</span><span class="sxs-lookup"><span data-stu-id="7db0b-105">This structure enables you to specify information to decompress the body of a message in compressed Rich Text Format (RTF) and, optionally, return the body stream in its native format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7db0b-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="7db0b-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size; 
    ULONG ulFlags; 
    ULONG ulInCodePage; 
    ULONG ulOutCodePage; 
} RTF_WCSINFO;

```

## <a name="members"></a><span data-ttu-id="7db0b-107">Membres</span><span class="sxs-lookup"><span data-stu-id="7db0b-107">Members</span></span>

 <span data-ttu-id="7db0b-108">_size_</span><span class="sxs-lookup"><span data-stu-id="7db0b-108">_size_</span></span>
  
> <span data-ttu-id="7db0b-109">Taille de la structure **RTF_WCSINFO** en nombre d’octets.</span><span class="sxs-lookup"><span data-stu-id="7db0b-109">The size of the **RTF_WCSINFO** structure in number of bytes.</span></span> 
    
 <span data-ttu-id="7db0b-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7db0b-110">_ulFlags_</span></span>
  
> <span data-ttu-id="7db0b-111">Il s’agit du masque de bits des indicateurs d’option pour la [fonction WrapCompressedRTFStreamEx.](wrapcompressedrtfstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="7db0b-111">This is the bitmask of option flags for the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="7db0b-112">Les indicateurs d’option pris en charge sont les :</span><span class="sxs-lookup"><span data-stu-id="7db0b-112">The supported option flags are:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="7db0b-113">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="7db0b-113">MAPI_MODIFY</span></span>  <br/> |<span data-ttu-id="7db0b-114">Cela indique si le client a l’intention d’écrire l’interface de flux wrapped renvoyée.</span><span class="sxs-lookup"><span data-stu-id="7db0b-114">This indicates whether the client intends to write the wrapped stream interface that is returned.</span></span>  <br/> |
|<span data-ttu-id="7db0b-115">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="7db0b-115">STORE_UNCOMPRESSED_RTF</span></span>  <br/> |<span data-ttu-id="7db0b-116">Cela indique si le RTF décompressé est supposé être écrit dans le flux vers qui pointe le pointeur _lpCompressedRTFStream_ de la fonction [WrapCompressedRTFStreamEx.](wrapcompressedrtfstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="7db0b-116">This indicates whether the decompressed RTF is supposed to be written to the stream that is pointed to by the  _lpCompressedRTFStream_ pointer of the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span>  <br/> |
|<span data-ttu-id="7db0b-117">MAPI_NATIVE_BODY</span><span class="sxs-lookup"><span data-stu-id="7db0b-117">MAPI_NATIVE_BODY</span></span>  <br/> |<span data-ttu-id="7db0b-118">Cela indique si le flux décompressé est également converti en corps natif avant de renvoyer le flux.</span><span class="sxs-lookup"><span data-stu-id="7db0b-118">This indicates whether the decompressed stream is also converted to the native body before returning the stream.</span></span> <span data-ttu-id="7db0b-119">Cet indicateur ne peut pas être combiné avec **l’MAPI_MODIFY’indicateur.**</span><span class="sxs-lookup"><span data-stu-id="7db0b-119">This flag cannot be combined with the **MAPI_MODIFY** flag.</span></span>  <br/> |
   
 <span data-ttu-id="7db0b-120">_ulInCodePage_</span><span class="sxs-lookup"><span data-stu-id="7db0b-120">_ulInCodePage_</span></span>
  
> <span data-ttu-id="7db0b-121">Il s’agit de la valeur de page de code du message.</span><span class="sxs-lookup"><span data-stu-id="7db0b-121">This is the code page value of the message.</span></span> <span data-ttu-id="7db0b-122">En règle générale, cette valeur est obtenue à partir de la propriété canonique [PidTagInternetCodepage](pidtaginternetcodepage-canonical-property.md) sur le message.</span><span class="sxs-lookup"><span data-stu-id="7db0b-122">Typically, this value is obtained from the [PidTagInternetCodepage Canonical Property](pidtaginternetcodepage-canonical-property.md) on the message.</span></span> <span data-ttu-id="7db0b-123">Cette valeur est utilisée uniquement lorsque **l’indicateur MAPI_NATIVE_BODY** est transmis  _dans ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="7db0b-123">This value is only used when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_.</span></span> <span data-ttu-id="7db0b-124">Sinon, cette valeur est ignorée.</span><span class="sxs-lookup"><span data-stu-id="7db0b-124">Otherwise, this value is ignored.</span></span>
    
 <span data-ttu-id="7db0b-125">_ulOutCodePage_</span><span class="sxs-lookup"><span data-stu-id="7db0b-125">_ulOutCodePage_</span></span>
  
> <span data-ttu-id="7db0b-126">Il s’agit de la valeur de page de code du flux décompressé renvoyé que vous souhaitez.</span><span class="sxs-lookup"><span data-stu-id="7db0b-126">This is the code page value of the returned decompressed stream that you want.</span></span> <span data-ttu-id="7db0b-127">Si elle est définie sur une valeur non nulle, la fonction [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) convertit le flux en page de code spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7db0b-127">If this is set to a non-zero value, the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function converts the stream to the specified code page.</span></span> <span data-ttu-id="7db0b-128">Si cette valeur est définie sur zéro, MAPI décide de la page de code à utiliser.</span><span class="sxs-lookup"><span data-stu-id="7db0b-128">If this is set to a zero value, MAPI decides which code page to use.</span></span> <span data-ttu-id="7db0b-129">Cette valeur est utilisée uniquement lorsque **l’indicateur MAPI_NATIVE_BODY** est transmis dans  _ulFlags_ et que le format du corps n’est pas RTF.</span><span class="sxs-lookup"><span data-stu-id="7db0b-129">This value is used only when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_, and the body format is not RTF.</span></span> <span data-ttu-id="7db0b-130">Sinon, cette valeur est ignorée.</span><span class="sxs-lookup"><span data-stu-id="7db0b-130">Otherwise, this value is ignored.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7db0b-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7db0b-131">See also</span></span>



[<span data-ttu-id="7db0b-132">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="7db0b-132">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

