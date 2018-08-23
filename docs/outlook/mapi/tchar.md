---
title: TCHAR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.TCHAR
api_type:
- COM
ms.assetid: 7a92060b-4c30-4eba-993f-36f5f9231a4b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 357ace3267f22d751a20a12c96f108ee2f8ae1e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595201"
---
# <a name="tchar"></a><span data-ttu-id="fdc8d-103">TCHAR</span><span class="sxs-lookup"><span data-stu-id="fdc8d-103">TCHAR</span></span>

  
  
<span data-ttu-id="fdc8d-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fdc8d-104">**Applies to**: Office 365 | Outlook | Outlook 2016</span></span> 
  
<span data-ttu-id="fdc8d-p101">Chaîne de caractères Win32 qui peut être utilisée pour décrire les chaînes ANSI, DBCS ou Unicode. Pour les plateformes ANSI et DBCS, TCHAR est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="fdc8d-p101">A Win32 character string that can be used to describe ANSI, DBCS, or Unicode strings. For ANSI and DBCS platforms, TCHAR is defined as follows:</span></span>
  
```cpp
typedef char TCHAR;

```

## <a name="remarks"></a><span data-ttu-id="fdc8d-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="fdc8d-107">Remarks</span></span>

<span data-ttu-id="fdc8d-108">Pour les plateformes Unicode, TCHAR est défini comme synonyme du type WCHAR.</span><span class="sxs-lookup"><span data-stu-id="fdc8d-108">For Unicode platforms, TCHAR is defined as synonymous with the WCHAR type.</span></span> 
  
<span data-ttu-id="fdc8d-p102">Les clients MAPI peuvent utiliser le type de données TCHAR pour représenter une chaîne de type WCHAR ou CHAR. Veillez à bien définir la constante symbolique UNICODE et à limiter la plateforme lorsque cela est nécessaire. MAPI interprète les informations de plateforme et traduit en interne les caractères TCHAR dans la chaîne appropriée. Le type de propriété MAPI, PT_TSTRING, fonctionne comme le type de données TCHAR. Lorsque la plateforme prend en charge le langage Unicode, le type PT_UNICODE est affecté aux propriétés de type PT_TSTRING lors de la compilation. Si la plateforme ne prend pas en charge le langage Unicode, ces propriétés ont le type PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="fdc8d-p102">MAPI clients can use the TCHAR data type to represent a string of either the WCHAR or char type. Be sure to define the symbolic constant UNICODE and limit the platform when it is required. MAPI will interpret the platform information and internally translate TCHAR to the appropriate string. The MAPI property type, PT_TSTRING, works just like the TCHAR data type. When the platform supports Unicode, properties of type PT_TSTRING are assigned the type PT_UNICODE at compile time. When the platform does not support Unicode, these properties are assigned the type PT_STRING8.</span></span>
  
<span data-ttu-id="fdc8d-115">Pour plus d’informations sur cette fonctionnalité, voir [Jeux de caractères](mapi-character-sets.md) et [Liste de types de propriétés](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="fdc8d-115">For more information about this functionality, see [Character Sets](mapi-character-sets.md) and [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fdc8d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fdc8d-116">See also</span></span>



[<span data-ttu-id="fdc8d-117">Types de données MAPI</span><span class="sxs-lookup"><span data-stu-id="fdc8d-117">MAPI Data Types</span></span>](mapi-data-types.md)

