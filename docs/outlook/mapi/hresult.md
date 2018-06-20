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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 5bacf3c73ba7f9a7720586c77ee520d289c40e11
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783528"
---
# <a name="hresult"></a><span data-ttu-id="b1239-103">HRESULT</span><span class="sxs-lookup"><span data-stu-id="b1239-103">HRESULT</span></span>

  
  
<span data-ttu-id="b1239-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b1239-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b1239-105">Une valeur de 32 bits qui est utilisée pour décrire une erreur ou un avertissement.</span><span class="sxs-lookup"><span data-stu-id="b1239-105">A 32-bit value that is used to describe an error or warning.</span></span>
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a><span data-ttu-id="b1239-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="b1239-106">Remarks</span></span>

<span data-ttu-id="b1239-107">Le type de données **HRESULT** est la même que le type de données [SCODE](scode.md) .</span><span class="sxs-lookup"><span data-stu-id="b1239-107">The **HRESULT** data type is the same as the [SCODE](scode.md) data type.</span></span> 
  
<span data-ttu-id="b1239-108">Une valeur **HRESULT** comprend les champs suivants :</span><span class="sxs-lookup"><span data-stu-id="b1239-108">An **HRESULT** value consists of the following fields:</span></span> 
  
- <span data-ttu-id="b1239-109">Un code de 1 bit qui indique le niveau de gravité, où zéro réussite 1 représente et échec.</span><span class="sxs-lookup"><span data-stu-id="b1239-109">A 1-bit code indicating severity, where zero represents success and 1 represents failure.</span></span>
    
- <span data-ttu-id="b1239-110">Une valeur réservée 4 bits.</span><span class="sxs-lookup"><span data-stu-id="b1239-110">A 4-bit reserved value.</span></span>
    
- <span data-ttu-id="b1239-111">Un code 11 bits indiquant la responsabilité de l’erreur ou avertissement, également connu sous le nom d’un code de fonction.</span><span class="sxs-lookup"><span data-stu-id="b1239-111">An 11-bit code indicating responsibility for the error or warning, also known as a facility code.</span></span>
    
- <span data-ttu-id="b1239-112">Un code décrivant l’erreur ou avertissement de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="b1239-112">A 16-bit code describing the error or warning.</span></span>
    
<span data-ttu-id="b1239-113">La plupart des fonctions et les méthodes d’interface MAPI retournent les valeurs **HRESULT** pour fournir la formation cause détaillée.</span><span class="sxs-lookup"><span data-stu-id="b1239-113">Most MAPI interface methods and functions return **HRESULT** values to provide detailed cause formation.</span></span> <span data-ttu-id="b1239-114">Les valeurs **HRESULT** sont également utilisés largement dans les méthodes d’interface OLE.</span><span class="sxs-lookup"><span data-stu-id="b1239-114">**HRESULT** values are also used widely in OLE interface methods.</span></span> <span data-ttu-id="b1239-115">OLE fournit plusieurs macros pour la conversion entre les valeurs **HRESULT** et **SCODE** , des types de données communes une autre pour la gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="b1239-115">OLE provides several macros for converting between **HRESULT** values and **SCODE** values, another common data type for error handling.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b1239-116">64 bits, MAPI, **HRESULT** est toujours une valeur 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b1239-116">In 64-bit MAPI, **HRESULT** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="b1239-117">Pour plus d’informations sur l’utilisation OLE de valeurs **HRESULT** , voir la *référence du programmeur OLE* .</span><span class="sxs-lookup"><span data-stu-id="b1239-117">For information about the OLE use of **HRESULT** values, see the  *OLE Programmer's Reference*  .</span></span> <span data-ttu-id="b1239-118">Pour plus d’informations sur l’utilisation de ces valeurs dans MAPI, voir [Gestion des erreurs](error-handling-in-mapi.md) et une des méthodes d’interface suivantes :</span><span class="sxs-lookup"><span data-stu-id="b1239-118">For more information about the use of these values in MAPI, see [Error Handling](error-handling-in-mapi.md) and any of the following interface methods:</span></span> 
  
[<span data-ttu-id="b1239-119">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b1239-119">IABLogon::GetLastError</span></span>](iablogon-getlasterror.md)
  
[<span data-ttu-id="b1239-120">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b1239-120">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="b1239-121">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b1239-121">IMAPIControl::GetLastError</span></span>](imapicontrol-getlasterror.md)
  
[<span data-ttu-id="b1239-122">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b1239-122">IMAPITable::GetLastError</span></span>](imapitable-getlasterror.md)
  
[<span data-ttu-id="b1239-123">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b1239-123">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="b1239-124">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="b1239-124">IMAPIViewAdviseSink::OnPrint</span></span>](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a><span data-ttu-id="b1239-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1239-125">See also</span></span>



[<span data-ttu-id="b1239-126">SCODE</span><span class="sxs-lookup"><span data-stu-id="b1239-126">SCODE</span></span>](scode.md)


[<span data-ttu-id="b1239-127">Types de donn�es MAPI</span><span class="sxs-lookup"><span data-stu-id="b1239-127">MAPI Data Types</span></span>](mapi-data-types.md)

