---
title: RTF_WCSRETINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62561d8d-33cb-e482-7fa0-132afe2b464a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: cfa18c215fc98610b836db31e2a07581291910be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315784"
---
# <a name="rtfwcsretinfo"></a><span data-ttu-id="88523-103">RTF_WCSRETINFO</span><span class="sxs-lookup"><span data-stu-id="88523-103">RTF_WCSRETINFO</span></span>

<span data-ttu-id="88523-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88523-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88523-105">Cette structure fournit des informations sur un flux au format natif renvoyé par la décompression du corps d'un message encapsulé en format RTF compressé.</span><span class="sxs-lookup"><span data-stu-id="88523-105">This structure provides information about a stream in native format returned from decompressing the body of a message that is encapsulated in compressed Rich Text Format (RTF).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="88523-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="88523-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a><span data-ttu-id="88523-107">Membres</span><span class="sxs-lookup"><span data-stu-id="88523-107">Members</span></span>

<span data-ttu-id="88523-108">_size_</span><span class="sxs-lookup"><span data-stu-id="88523-108">_size_</span></span>
  
> <span data-ttu-id="88523-109">Taille de la structure **RTF_WCSRETINFO** en nombre d'octets.</span><span class="sxs-lookup"><span data-stu-id="88523-109">The size of the **RTF_WCSRETINFO** structure in number of bytes.</span></span> 
    
<span data-ttu-id="88523-110">_ulStreamFlags_</span><span class="sxs-lookup"><span data-stu-id="88523-110">_ulStreamFlags_</span></span>
  
> <span data-ttu-id="88523-111">Il s'agit d'une valeur qui indique le format du corps natif.</span><span class="sxs-lookup"><span data-stu-id="88523-111">This is a value that indicates the format of the native body.</span></span> <span data-ttu-id="88523-112">Cette valeur est valide uniquement si l'indicateur **MAPI_NATIVE_BODY** est transmis dans le paramètre _ulFlags_ de la structure [RTF_WCSINFO](rtf_wcsinfo.md) qui est transmise à la fonction [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="88523-112">This value is only valid if the **MAPI_NATIVE_BODY** flag is passed in the  _ulFlags_ parameter of the [RTF_WCSINFO](rtf_wcsinfo.md) structure that is passed to the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="88523-113">Il peut s'agir de l'une des valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="88523-113">This can be one of the following values:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="88523-114">MAPI_NATIVE_BODY_TYPE_RTF</span><span class="sxs-lookup"><span data-stu-id="88523-114">MAPI_NATIVE_BODY_TYPE_RTF</span></span>  <br/> |<span data-ttu-id="88523-115">Cette valeur est utilisée uniquement si _ulFlags_ inclut l'indicateur **MAPI_NATIVE_BODY** et si le corps est au format RTF.</span><span class="sxs-lookup"><span data-stu-id="88523-115">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is RTF.</span></span>  <br/> |
|<span data-ttu-id="88523-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span><span class="sxs-lookup"><span data-stu-id="88523-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span></span>  <br/> |<span data-ttu-id="88523-117">Cette valeur est utilisée uniquement si _ulFlags_ inclut l'indicateur **MAPI_NATIVE_BODY** et si le corps est au format de texte brut.</span><span class="sxs-lookup"><span data-stu-id="88523-117">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is plain text format.</span></span>  <br/> |
|<span data-ttu-id="88523-118">MAPI_NATIVE_BODY_TYPE_HTML</span><span class="sxs-lookup"><span data-stu-id="88523-118">MAPI_NATIVE_BODY_TYPE_HTML</span></span>  <br/> |<span data-ttu-id="88523-119">Cette valeur est utilisée uniquement si _ulFlags_ inclut l'indicateur **MAPI_NATIVE_BODY** et si le corps est au format html (Hypertext Markup Language).</span><span class="sxs-lookup"><span data-stu-id="88523-119">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is Hypertext Markup Language (HTML) format.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="88523-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88523-120">See also</span></span>

- [<span data-ttu-id="88523-121">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="88523-121">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

