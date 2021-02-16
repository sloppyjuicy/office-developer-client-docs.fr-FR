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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4208f51af44055b03c65b51c9b3d94e947dc9b68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430132"
---
# <a name="scode"></a><span data-ttu-id="e1fef-103">SCODE</span><span class="sxs-lookup"><span data-stu-id="e1fef-103">SCODE</span></span>

<span data-ttu-id="e1fef-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1fef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1fef-105">Valeur d’état 32 bits utilisée pour décrire une erreur ou un avertissement.</span><span class="sxs-lookup"><span data-stu-id="e1fef-105">A 32-bit status value that is used to describe an error or warning.</span></span> 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a><span data-ttu-id="e1fef-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="e1fef-106">Remarks</span></span>

<span data-ttu-id="e1fef-107">Le type de données **SCODE** est identique au type de données [HRESULT.](hresult.md)</span><span class="sxs-lookup"><span data-stu-id="e1fef-107">The **SCODE** data type is the same as the [HRESULT](hresult.md) data type.</span></span> 
  
<span data-ttu-id="e1fef-108">Une **valeur SCODE** est divisée en quatre champs :</span><span class="sxs-lookup"><span data-stu-id="e1fef-108">An **SCODE** value is divided into four fields:</span></span> 
  
- <span data-ttu-id="e1fef-109">Code de gravité à bit unique qui est définie sur 0 pour indiquer la réussite et 1 pour indiquer l’échec.</span><span class="sxs-lookup"><span data-stu-id="e1fef-109">A single-bit severity code which is set to 0 to indicate success and 1 to indicate failure.</span></span>
    
- <span data-ttu-id="e1fef-110">Champ réservé 11 bits</span><span class="sxs-lookup"><span data-stu-id="e1fef-110">An 11-bit reserved field</span></span>
    
- <span data-ttu-id="e1fef-111">Code d’installation 4 bits qui indique la zone responsable de l’erreur ou de l’avertissement.</span><span class="sxs-lookup"><span data-stu-id="e1fef-111">A 4-bit facility code which indicates the area responsible for the error or warning.</span></span>
    
- <span data-ttu-id="e1fef-112">Erreur 16 bits ou code d’avertissement qui décrit le problème à l’origine de l’erreur ou de l’avertissement.</span><span class="sxs-lookup"><span data-stu-id="e1fef-112">A 16-bit error or warning code which describes the problem that is causing the error or warning.</span></span>
    
<span data-ttu-id="e1fef-113">De nombreuses fonctions et méthodes MAPI retournent des valeurs **SCODE** définies en tant que types de données **HRESULT,** tout comme les méthodes et fonctions OLE.</span><span class="sxs-lookup"><span data-stu-id="e1fef-113">Many of the MAPI functions and methods return **SCODE** values defined as **HRESULT** data types as do the OLE methods and functions.</span></span> <span data-ttu-id="e1fef-114">OLE définit plusieurs macros qui peuvent être utilisées pour convertir entre **un SCODE** et un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e1fef-114">OLE defines several macros that can be used to convert between an **SCODE** and an **HRESULT**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e1fef-115">Dans MAPI 64 bits, **SCODE** est toujours une valeur 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e1fef-115">In 64-bit MAPI, **SCODE** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="e1fef-116">Pour plus d’informations sur la façon dont MAPI utilise le type de données **SCODE,** voir [Gestion des erreurs.](error-handling-in-mapi.md)</span><span class="sxs-lookup"><span data-stu-id="e1fef-116">For more information about how MAPI uses the **SCODE** data type, see [Error Handling](error-handling-in-mapi.md).</span></span> <span data-ttu-id="e1fef-117">Pour plus d’informations sur OLE et le type de données **SCODE,** voir la *référence du programmeur OLE.*</span><span class="sxs-lookup"><span data-stu-id="e1fef-117">For more information about OLE and the **SCODE** data type, see the  *OLE Programmer's Reference*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e1fef-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1fef-118">See also</span></span>



<span data-ttu-id="e1fef-119">[[HRESULT]](hresult.md)</span><span class="sxs-lookup"><span data-stu-id="e1fef-119">[HRESULT](hresult.md)</span></span>


[<span data-ttu-id="e1fef-120">Types de données MAPI</span><span class="sxs-lookup"><span data-stu-id="e1fef-120">MAPI Data Types</span></span>](mapi-data-types.md)

