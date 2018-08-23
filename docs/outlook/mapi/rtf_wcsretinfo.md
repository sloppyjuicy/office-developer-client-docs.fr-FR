---
title: RTF_WCSRETINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62561d8d-33cb-e482-7fa0-132afe2b464a
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: bf8cf115c6188b5058717437c470e11797ff5b9a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564961"
---
# <a name="rtfwcsretinfo"></a><span data-ttu-id="eb2dc-103">RTF_WCSRETINFO</span><span class="sxs-lookup"><span data-stu-id="eb2dc-103">RTF_WCSRETINFO</span></span>

<span data-ttu-id="eb2dc-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb2dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb2dc-105">Cette structure fournit des informations sur un flux de données au format natif renvoyé à partir de décompresser le corps d’un message est encapsulé dans compressé texte enrichi (RTF).</span><span class="sxs-lookup"><span data-stu-id="eb2dc-105">This structure provides information about a stream in native format returned from decompressing the body of a message that is encapsulated in compressed Rich Text Format (RTF).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="eb2dc-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="eb2dc-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a><span data-ttu-id="eb2dc-107">Members</span><span class="sxs-lookup"><span data-stu-id="eb2dc-107">Members</span></span>

<span data-ttu-id="eb2dc-108">_size_</span><span class="sxs-lookup"><span data-stu-id="eb2dc-108">_size_</span></span>
  
> <span data-ttu-id="eb2dc-109">La taille de la structure **RTF_WCSRETINFO** en nombre d’octets.</span><span class="sxs-lookup"><span data-stu-id="eb2dc-109">The size of the **RTF_WCSRETINFO** structure in number of bytes.</span></span> 
    
<span data-ttu-id="eb2dc-110">_ulStreamFlags_</span><span class="sxs-lookup"><span data-stu-id="eb2dc-110">_ulStreamFlags_</span></span>
  
> <span data-ttu-id="eb2dc-111">Il s’agit d’une valeur qui indique le format du corps natif.</span><span class="sxs-lookup"><span data-stu-id="eb2dc-111">This is a value that indicates the format of the native body.</span></span> <span data-ttu-id="eb2dc-112">Cette valeur est valide uniquement si l’indicateur **MAPI_NATIVE_BODY** est passé dans le paramètre _ulFlags_ de la structure [RTF_WCSINFO](rtf_wcsinfo.md) qui est transmis à la fonction [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="eb2dc-112">This value is only valid if the **MAPI_NATIVE_BODY** flag is passed in the  _ulFlags_ parameter of the [RTF_WCSINFO](rtf_wcsinfo.md) structure that is passed to the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="eb2dc-113">Cela peut être une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="eb2dc-113">This can be one of the following values:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="eb2dc-114">MAPI_NATIVE_BODY_TYPE_RTF</span><span class="sxs-lookup"><span data-stu-id="eb2dc-114">MAPI_NATIVE_BODY_TYPE_RTF</span></span>  <br/> |<span data-ttu-id="eb2dc-115">Cette valeur est uniquement utilisée si _ulFlags_ inclut l’indicateur **MAPI_NATIVE_BODY** , et le corps est au format RTF.</span><span class="sxs-lookup"><span data-stu-id="eb2dc-115">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is RTF.</span></span>  <br/> |
|<span data-ttu-id="eb2dc-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span><span class="sxs-lookup"><span data-stu-id="eb2dc-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span></span>  <br/> |<span data-ttu-id="eb2dc-117">Cette valeur est uniquement utilisée si _ulFlags_ inclut l’indicateur **MAPI_NATIVE_BODY** , et le corps est au format texte brut.</span><span class="sxs-lookup"><span data-stu-id="eb2dc-117">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is plain text format.</span></span>  <br/> |
|<span data-ttu-id="eb2dc-118">MAPI_NATIVE_BODY_TYPE_HTML</span><span class="sxs-lookup"><span data-stu-id="eb2dc-118">MAPI_NATIVE_BODY_TYPE_HTML</span></span>  <br/> |<span data-ttu-id="eb2dc-119">Cette valeur est uniquement utilisée si _ulFlags_ inclut l’indicateur **MAPI_NATIVE_BODY** , et le corps est au format HTML Hypertext Markup Language ().</span><span class="sxs-lookup"><span data-stu-id="eb2dc-119">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is Hypertext Markup Language (HTML) format.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb2dc-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb2dc-120">See also</span></span>

- [<span data-ttu-id="eb2dc-121">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="eb2dc-121">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

