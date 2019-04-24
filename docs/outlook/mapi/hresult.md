---
title: HRESULT
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
ms.assetid: b248ed11-3d8a-4d4c-9b84-fa5bee7979c7
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 64fcbebbd71bc3f478f36c711e49db9a3518ef9a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347795"
---
# <a name="hresult"></a><span data-ttu-id="42f70-103">HRESULT</span><span class="sxs-lookup"><span data-stu-id="42f70-103">HRESULT</span></span>

  
  
<span data-ttu-id="42f70-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42f70-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42f70-105">Valeur 32 bits utilisée pour décrire une erreur ou un avertissement.</span><span class="sxs-lookup"><span data-stu-id="42f70-105">A 32-bit value that is used to describe an error or warning.</span></span>
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a><span data-ttu-id="42f70-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="42f70-106">Remarks</span></span>

<span data-ttu-id="42f70-107">Le type de données **HRESULT** est le même que le type de données [SCODE](scode.md) .</span><span class="sxs-lookup"><span data-stu-id="42f70-107">The **HRESULT** data type is the same as the [SCODE](scode.md) data type.</span></span> 
  
<span data-ttu-id="42f70-108">Une valeur **HRESULT** se compose des champs suivants:</span><span class="sxs-lookup"><span data-stu-id="42f70-108">An **HRESULT** value consists of the following fields:</span></span> 
  
- <span data-ttu-id="42f70-109">Code à 1 bit indiquant la gravité, où zéro représente la réussite et 1 représente échec.</span><span class="sxs-lookup"><span data-stu-id="42f70-109">A 1-bit code indicating severity, where zero represents success and 1 represents failure.</span></span>
    
- <span data-ttu-id="42f70-110">Valeur réservée 4 bits.</span><span class="sxs-lookup"><span data-stu-id="42f70-110">A 4-bit reserved value.</span></span>
    
- <span data-ttu-id="42f70-111">Code 11 bits indiquant la responsabilité de l'erreur ou de l'avertissement, également appelé code de fonction.</span><span class="sxs-lookup"><span data-stu-id="42f70-111">An 11-bit code indicating responsibility for the error or warning, also known as a facility code.</span></span>
    
- <span data-ttu-id="42f70-112">Code 16 bits décrivant l'erreur ou l'avertissement.</span><span class="sxs-lookup"><span data-stu-id="42f70-112">A 16-bit code describing the error or warning.</span></span>
    
<span data-ttu-id="42f70-113">La plupart des méthodes et fonctions de l'interface MAPI renvoient des valeurs **HRESULT** pour fournir des causes détaillées.</span><span class="sxs-lookup"><span data-stu-id="42f70-113">Most MAPI interface methods and functions return **HRESULT** values to provide detailed cause formation.</span></span> <span data-ttu-id="42f70-114">Les valeurs **HRESULT** sont également largement utilisées dans les méthodes d'interface OLE.</span><span class="sxs-lookup"><span data-stu-id="42f70-114">**HRESULT** values are also used widely in OLE interface methods.</span></span> <span data-ttu-id="42f70-115">OLE fournit plusieurs macros pour la conversion entre des valeurs **HRESULT** et des valeurs **SCODE** , un autre type de données commun pour la gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="42f70-115">OLE provides several macros for converting between **HRESULT** values and **SCODE** values, another common data type for error handling.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="42f70-116">Dans MAPI 64 bits, **HRESULT** est toujours une valeur 32 bits.</span><span class="sxs-lookup"><span data-stu-id="42f70-116">In 64-bit MAPI, **HRESULT** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="42f70-117">Pour plus d'informations sur l'utilisation OLE des valeurs **HRESULT** , consultez le *Guide de référence du programmeur OLE* .</span><span class="sxs-lookup"><span data-stu-id="42f70-117">For information about the OLE use of **HRESULT** values, see the  *OLE Programmer's Reference*  .</span></span> <span data-ttu-id="42f70-118">Pour plus d'informations sur l'utilisation de ces valeurs dans MAPI, consultez la rubrique [gestion des erreurs](error-handling-in-mapi.md) et l'une des méthodes d'interface suivantes:</span><span class="sxs-lookup"><span data-stu-id="42f70-118">For more information about the use of these values in MAPI, see [Error Handling](error-handling-in-mapi.md) and any of the following interface methods:</span></span> 
  
[<span data-ttu-id="42f70-119">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="42f70-119">IABLogon::GetLastError</span></span>](iablogon-getlasterror.md)
  
[<span data-ttu-id="42f70-120">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="42f70-120">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="42f70-121">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="42f70-121">IMAPIControl::GetLastError</span></span>](imapicontrol-getlasterror.md)
  
[<span data-ttu-id="42f70-122">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="42f70-122">IMAPITable::GetLastError</span></span>](imapitable-getlasterror.md)
  
[<span data-ttu-id="42f70-123">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="42f70-123">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="42f70-124">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="42f70-124">IMAPIViewAdviseSink::OnPrint</span></span>](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a><span data-ttu-id="42f70-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42f70-125">See also</span></span>



[<span data-ttu-id="42f70-126">SCODE</span><span class="sxs-lookup"><span data-stu-id="42f70-126">SCODE</span></span>](scode.md)


[<span data-ttu-id="42f70-127">Types de donn�es MAPI</span><span class="sxs-lookup"><span data-stu-id="42f70-127">MAPI Data Types</span></span>](mapi-data-types.md)

