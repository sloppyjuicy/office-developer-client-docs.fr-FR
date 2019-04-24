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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 4208f51af44055b03c65b51c9b3d94e947dc9b68
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351239"
---
# <a name="scode"></a><span data-ttu-id="d72d7-103">SCODE</span><span class="sxs-lookup"><span data-stu-id="d72d7-103">SCODE</span></span>

<span data-ttu-id="d72d7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d72d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d72d7-105">Valeur d'État 32 bits utilisée pour décrire une erreur ou un avertissement.</span><span class="sxs-lookup"><span data-stu-id="d72d7-105">A 32-bit status value that is used to describe an error or warning.</span></span> 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a><span data-ttu-id="d72d7-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="d72d7-106">Remarks</span></span>

<span data-ttu-id="d72d7-107">Le type de données **SCODE** est le même que le type de données [HRESULT](hresult.md) .</span><span class="sxs-lookup"><span data-stu-id="d72d7-107">The **SCODE** data type is the same as the [HRESULT](hresult.md) data type.</span></span> 
  
<span data-ttu-id="d72d7-108">Une valeur **SCODE** est divisée en quatre champs:</span><span class="sxs-lookup"><span data-stu-id="d72d7-108">An **SCODE** value is divided into four fields:</span></span> 
  
- <span data-ttu-id="d72d7-109">Code de gravité à un bit qui est défini sur 0 pour indiquer la réussite et 1 pour indiquer l'échec.</span><span class="sxs-lookup"><span data-stu-id="d72d7-109">A single-bit severity code which is set to 0 to indicate success and 1 to indicate failure.</span></span>
    
- <span data-ttu-id="d72d7-110">Un champ réservé 11 bits</span><span class="sxs-lookup"><span data-stu-id="d72d7-110">An 11-bit reserved field</span></span>
    
- <span data-ttu-id="d72d7-111">Code de fonction à 4 bits qui indique la zone responsable de l'erreur ou de l'avertissement.</span><span class="sxs-lookup"><span data-stu-id="d72d7-111">A 4-bit facility code which indicates the area responsible for the error or warning.</span></span>
    
- <span data-ttu-id="d72d7-112">Un code d'erreur ou d'avertissement 16 bits qui décrit le problème à l'origine de l'erreur ou de l'avertissement.</span><span class="sxs-lookup"><span data-stu-id="d72d7-112">A 16-bit error or warning code which describes the problem that is causing the error or warning.</span></span>
    
<span data-ttu-id="d72d7-113">De nombreuses fonctions et méthodes MAPI renvoient des valeurs **SCODE** définies en tant que types de données **HRESULT** de la même manière que les fonctions et méthodes OLE.</span><span class="sxs-lookup"><span data-stu-id="d72d7-113">Many of the MAPI functions and methods return **SCODE** values defined as **HRESULT** data types as do the OLE methods and functions.</span></span> <span data-ttu-id="d72d7-114">OLE définit plusieurs macros qui peuvent être utilisées pour effectuer une conversion entre un **SCODE** et un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d72d7-114">OLE defines several macros that can be used to convert between an **SCODE** and an **HRESULT**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d72d7-115">Dans MAPI 64 bits, **SCODE** est toujours une valeur 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d72d7-115">In 64-bit MAPI, **SCODE** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="d72d7-116">Pour plus d'informations sur la façon dont MAPI utilise le type de données **SCODE** , consultez la rubrique [gestion des erreurs](error-handling-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="d72d7-116">For more information about how MAPI uses the **SCODE** data type, see [Error Handling](error-handling-in-mapi.md).</span></span> <span data-ttu-id="d72d7-117">Pour plus d'informations sur OLE et le type de données **SCODE** , consultez le *Guide OLE programmer's Reference* .</span><span class="sxs-lookup"><span data-stu-id="d72d7-117">For more information about OLE and the **SCODE** data type, see the  *OLE Programmer's Reference*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d72d7-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d72d7-118">See also</span></span>



<span data-ttu-id="d72d7-119">[[HRESULT]](hresult.md)</span><span class="sxs-lookup"><span data-stu-id="d72d7-119">[HRESULT](hresult.md)</span></span>


[<span data-ttu-id="d72d7-120">Types de donn�es MAPI</span><span class="sxs-lookup"><span data-stu-id="d72d7-120">MAPI Data Types</span></span>](mapi-data-types.md)

