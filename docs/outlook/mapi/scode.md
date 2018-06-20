---
title: SCODE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HRESULT
api_type:
- COM
ms.assetid: 2348cce1-07c3-49ed-ae03-79e477d3c6c2
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 6cd9dfe8fabd1ae7a4389550c628fb7ceff09ea8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787073"
---
# <a name="scode"></a><span data-ttu-id="e7b54-103">SCODE</span><span class="sxs-lookup"><span data-stu-id="e7b54-103">SCODE</span></span>

<span data-ttu-id="e7b54-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e7b54-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e7b54-105">Une valeur d’état de 32 bits qui est utilisée pour décrire une erreur ou un avertissement.</span><span class="sxs-lookup"><span data-stu-id="e7b54-105">A 32-bit status value that is used to describe an error or warning.</span></span> 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a><span data-ttu-id="e7b54-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="e7b54-106">Remarks</span></span>

<span data-ttu-id="e7b54-107">Le type de données **SCODE** est la même que le type de données [HRESULT](hresult.md) .</span><span class="sxs-lookup"><span data-stu-id="e7b54-107">The **SCODE** data type is the same as the [HRESULT](hresult.md) data type.</span></span> 
  
<span data-ttu-id="e7b54-108">Une valeur **SCODE** est divisée en quatre champs :</span><span class="sxs-lookup"><span data-stu-id="e7b54-108">An **SCODE** value is divided into four fields:</span></span> 
  
- <span data-ttu-id="e7b54-109">Un code de gravité bits unique qui est défini sur 0 pour indiquer la réussite et 1 pour indiquer l’échec.</span><span class="sxs-lookup"><span data-stu-id="e7b54-109">A single-bit severity code which is set to 0 to indicate success and 1 to indicate failure.</span></span>
    
- <span data-ttu-id="e7b54-110">Un champ réservé 11 bits</span><span class="sxs-lookup"><span data-stu-id="e7b54-110">An 11-bit reserved field</span></span>
    
- <span data-ttu-id="e7b54-111">Un code de fonction 4 bits qui indique la zone responsable de l’erreur ou avertissement.</span><span class="sxs-lookup"><span data-stu-id="e7b54-111">A 4-bit facility code which indicates the area responsible for the error or warning.</span></span>
    
- <span data-ttu-id="e7b54-112">Une erreur de 16 bits ou un code d’avertissement qui décrit le problème qui est à l’origine de l’erreur ou avertissement.</span><span class="sxs-lookup"><span data-stu-id="e7b54-112">A 16-bit error or warning code which describes the problem that is causing the error or warning.</span></span>
    
<span data-ttu-id="e7b54-113">La plupart des méthodes et fonctions MAPI renvoient des valeurs **SCODE** définis en tant que types de données **HRESULT** comme les fonctions et méthodes OLE.</span><span class="sxs-lookup"><span data-stu-id="e7b54-113">Many of the MAPI functions and methods return **SCODE** values defined as **HRESULT** data types as do the OLE methods and functions.</span></span> <span data-ttu-id="e7b54-114">OLE définit plusieurs macros qui peuvent être utilisés pour convertir les **SCODE** un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e7b54-114">OLE defines several macros that can be used to convert between an **SCODE** and an **HRESULT**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e7b54-115">64 bits, MAPI, **SCODE** est toujours une valeur 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e7b54-115">In 64-bit MAPI, **SCODE** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="e7b54-116">Pour plus d’informations sur l’utilisation de MAPI sur le type de données **SCODE** , voir [Gestion des erreurs](error-handling-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="e7b54-116">For more information about how MAPI uses the **SCODE** data type, see [Error Handling](error-handling-in-mapi.md).</span></span> <span data-ttu-id="e7b54-117">Pour plus d’informations sur OLE et le type de données **SCODE** , voir la *référence du programmeur OLE* .</span><span class="sxs-lookup"><span data-stu-id="e7b54-117">For more information about OLE and the **SCODE** data type, see the  *OLE Programmer's Reference*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e7b54-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7b54-118">See also</span></span>



<span data-ttu-id="e7b54-119">[[HRESULT]](hresult.md)</span><span class="sxs-lookup"><span data-stu-id="e7b54-119">[HRESULT](hresult.md)</span></span>


[<span data-ttu-id="e7b54-120">Types de donn�es MAPI</span><span class="sxs-lookup"><span data-stu-id="e7b54-120">MAPI Data Types</span></span>](mapi-data-types.md)

