---
title: RTF_WCSINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c94501e-0ec7-e836-33a7-adcf5a61b375
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c328e79b7e474369f11f8a4002e00137659db3c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787052"
---
# <a name="rtfwcsinfo"></a><span data-ttu-id="ed7e0-103">RTF_WCSINFO</span><span class="sxs-lookup"><span data-stu-id="ed7e0-103">RTF_WCSINFO</span></span>

  
  
<span data-ttu-id="ed7e0-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ed7e0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ed7e0-105">Cette structure vous permet de spécifier des informations pour décompresser le corps d’un message dans compressé texte enrichi (RTF) et, éventuellement, retourner le flux de corps dans son format natif.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-105">This structure enables you to specify information to decompress the body of a message in compressed Rich Text Format (RTF) and, optionally, return the body stream in its native format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ed7e0-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="ed7e0-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size; 
    ULONG ulFlags; 
    ULONG ulInCodePage; 
    ULONG ulOutCodePage; 
} RTF_WCSINFO;

```

## <a name="members"></a><span data-ttu-id="ed7e0-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ed7e0-107">Members</span></span>

 <span data-ttu-id="ed7e0-108">_taille_</span><span class="sxs-lookup"><span data-stu-id="ed7e0-108">_size_</span></span>
  
> <span data-ttu-id="ed7e0-109">La taille de la structure **RTF_WCSINFO** en nombre d’octets.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-109">The size of the **RTF_WCSINFO** structure in number of bytes.</span></span> 
    
 <span data-ttu-id="ed7e0-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ed7e0-110">_ulFlags_</span></span>
  
> <span data-ttu-id="ed7e0-111">Il s’agit de masque de bits d’indicateurs d’option de la fonction [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="ed7e0-111">This is the bitmask of option flags for the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="ed7e0-112">Les indicateurs d’option prise en charge sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="ed7e0-112">The supported option flags are:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="ed7e0-113">N'</span><span class="sxs-lookup"><span data-stu-id="ed7e0-113">MAPI_MODIFY</span></span>  <br/> |<span data-ttu-id="ed7e0-114">Indique si le client a l’intention d’écrire l’interface flux encapsulé qui est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-114">This indicates whether the client intends to write the wrapped stream interface that is returned.</span></span>  <br/> |
|<span data-ttu-id="ed7e0-115">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="ed7e0-115">STORE_UNCOMPRESSED_RTF</span></span>  <br/> |<span data-ttu-id="ed7e0-116">Indique si le format RTF décompressé est supposé être écrits dans le flux est indiqué par le pointeur _lpCompressedRTFStream_ de la fonction [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="ed7e0-116">This indicates whether the decompressed RTF is supposed to be written to the stream that is pointed to by the  _lpCompressedRTFStream_ pointer of the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span>  <br/> |
|<span data-ttu-id="ed7e0-117">MAPI_NATIVE_BODY</span><span class="sxs-lookup"><span data-stu-id="ed7e0-117">MAPI_NATIVE_BODY</span></span>  <br/> |<span data-ttu-id="ed7e0-118">Cela indique si le flux décompressé est également converti au corps natif avant de retourner le flux.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-118">This indicates whether the decompressed stream is also converted to the native body before returning the stream.</span></span> <span data-ttu-id="ed7e0-119">Cet indicateur ne peut être combiné avec l’indicateur **ne** .</span><span class="sxs-lookup"><span data-stu-id="ed7e0-119">This flag cannot be combined with the **MAPI_MODIFY** flag.</span></span>  <br/> |
   
 <span data-ttu-id="ed7e0-120">_ulInCodePage_</span><span class="sxs-lookup"><span data-stu-id="ed7e0-120">_ulInCodePage_</span></span>
  
> <span data-ttu-id="ed7e0-121">Il s’agit de la valeur de page de code du message.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-121">This is the code page value of the message.</span></span> <span data-ttu-id="ed7e0-122">En règle générale, cette valeur est obtenue à partir de la [Propriété canonique PidTagInternetCodepage](pidtaginternetcodepage-canonical-property.md) dans le message.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-122">Typically, this value is obtained from the [PidTagInternetCodepage Canonical Property](pidtaginternetcodepage-canonical-property.md) on the message.</span></span> <span data-ttu-id="ed7e0-123">Cette valeur est uniquement utilisée lors de l’indicateur **MAPI_NATIVE_BODY** est passé dans _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-123">This value is only used when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_.</span></span> <span data-ttu-id="ed7e0-124">Dans le cas contraire, cette valeur est ignorée.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-124">Otherwise, this value is ignored.</span></span>
    
 <span data-ttu-id="ed7e0-125">_ulOutCodePage_</span><span class="sxs-lookup"><span data-stu-id="ed7e0-125">_ulOutCodePage_</span></span>
  
> <span data-ttu-id="ed7e0-126">Il s’agit de la valeur de page de code du flux décompressé renvoyée que vous souhaitez.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-126">This is the code page value of the returned decompressed stream that you want.</span></span> <span data-ttu-id="ed7e0-127">Si cela est défini sur une valeur différente de zéro, la fonction [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) convertit le flux de la page de code spécifié.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-127">If this is set to a non-zero value, the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function converts the stream to the specified code page.</span></span> <span data-ttu-id="ed7e0-128">Si cela est défini sur une valeur nulle, MAPI décide de page de codes à utiliser.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-128">If this is set to a zero value, MAPI decides which code page to use.</span></span> <span data-ttu-id="ed7e0-129">Cette valeur est utilisée uniquement lorsque l’indicateur **MAPI_NATIVE_BODY** est passé dans _ulFlags_, et le format du corps n’est pas au format RTF.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-129">This value is used only when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_, and the body format is not RTF.</span></span> <span data-ttu-id="ed7e0-130">Dans le cas contraire, cette valeur est ignorée.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-130">Otherwise, this value is ignored.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ed7e0-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed7e0-131">See also</span></span>



[<span data-ttu-id="ed7e0-132">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="ed7e0-132">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

