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
ms.openlocfilehash: 3a38a4604230c0aa3f5b0d104ae3b838f544b31d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787034"
---
# <a name="rtfwcsretinfo"></a><span data-ttu-id="38964-103">RTF_WCSRETINFO</span><span class="sxs-lookup"><span data-stu-id="38964-103">RTF_WCSRETINFO</span></span>

<span data-ttu-id="38964-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="38964-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="38964-105">Cette structure fournit des informations sur un flux de données au format natif renvoyé à partir de décompresser le corps d’un message est encapsulé dans compressé texte enrichi (RTF).</span><span class="sxs-lookup"><span data-stu-id="38964-105">This structure provides information about a stream in native format returned from decompressing the body of a message that is encapsulated in compressed Rich Text Format (RTF).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="38964-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="38964-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a><span data-ttu-id="38964-107">Membres</span><span class="sxs-lookup"><span data-stu-id="38964-107">Members</span></span>

<span data-ttu-id="38964-108">_taille_</span><span class="sxs-lookup"><span data-stu-id="38964-108">_size_</span></span>
  
> <span data-ttu-id="38964-109">La taille de la structure **RTF_WCSRETINFO** en nombre d’octets.</span><span class="sxs-lookup"><span data-stu-id="38964-109">The size of the **RTF_WCSRETINFO** structure in number of bytes.</span></span> 
    
<span data-ttu-id="38964-110">_ulStreamFlags_</span><span class="sxs-lookup"><span data-stu-id="38964-110">_ulStreamFlags_</span></span>
  
> <span data-ttu-id="38964-111">Il s’agit d’une valeur qui indique le format du corps natif.</span><span class="sxs-lookup"><span data-stu-id="38964-111">This is a value that indicates the format of the native body.</span></span> <span data-ttu-id="38964-112">Cette valeur est valide uniquement si l’indicateur **MAPI_NATIVE_BODY** est passé dans le paramètre _ulFlags_ de la structure [RTF_WCSINFO](rtf_wcsinfo.md) qui est transmis à la fonction [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="38964-112">This value is only valid if the **MAPI_NATIVE_BODY** flag is passed in the  _ulFlags_ parameter of the [RTF_WCSINFO](rtf_wcsinfo.md) structure that is passed to the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="38964-113">Cela peut être une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="38964-113">This can be one of the following values:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="38964-114">MAPI_NATIVE_BODY_TYPE_RTF</span><span class="sxs-lookup"><span data-stu-id="38964-114">MAPI_NATIVE_BODY_TYPE_RTF</span></span>  <br/> |<span data-ttu-id="38964-115">Cette valeur est uniquement utilisée si _ulFlags_ inclut l’indicateur **MAPI_NATIVE_BODY** , et le corps est au format RTF.</span><span class="sxs-lookup"><span data-stu-id="38964-115">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is RTF.</span></span>  <br/> |
|<span data-ttu-id="38964-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span><span class="sxs-lookup"><span data-stu-id="38964-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span></span>  <br/> |<span data-ttu-id="38964-117">Cette valeur est uniquement utilisée si _ulFlags_ inclut l’indicateur **MAPI_NATIVE_BODY** , et le corps est au format texte brut.</span><span class="sxs-lookup"><span data-stu-id="38964-117">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is plain text format.</span></span>  <br/> |
|<span data-ttu-id="38964-118">MAPI_NATIVE_BODY_TYPE_HTML</span><span class="sxs-lookup"><span data-stu-id="38964-118">MAPI_NATIVE_BODY_TYPE_HTML</span></span>  <br/> |<span data-ttu-id="38964-119">Cette valeur est uniquement utilisée si _ulFlags_ inclut l’indicateur **MAPI_NATIVE_BODY** , et le corps est au format HTML Hypertext Markup Language ().</span><span class="sxs-lookup"><span data-stu-id="38964-119">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is Hypertext Markup Language (HTML) format.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="38964-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38964-120">See also</span></span>

- [<span data-ttu-id="38964-121">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="38964-121">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

