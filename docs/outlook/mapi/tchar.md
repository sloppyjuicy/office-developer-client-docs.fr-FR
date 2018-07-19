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
ms.openlocfilehash: e7b3774d8dce446f0e87f041f11dac607f464680
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787348"
---
# <a name="tchar"></a><span data-ttu-id="2c43f-103">TCHAR</span><span class="sxs-lookup"><span data-stu-id="2c43f-103">TCHAR</span></span>

  
  
<span data-ttu-id="2c43f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2c43f-104">**Applies to:** Outlook \*</span></span> 
  
<span data-ttu-id="2c43f-p101">Chaîne de caract�res Win32 qui peut �tre utilis�e pour d�crire les chaînes ANSI, DBCS ou Unicode. Pour les plateformes ANSI et DBCS, TCHAR est d�fini comme suit :</span><span class="sxs-lookup"><span data-stu-id="2c43f-p101">A Win32 character string that can be used to describe ANSI, DBCS, or Unicode strings. For ANSI and DBCS platforms, TCHAR is defined as follows:</span></span>
  
```cpp
typedef char TCHAR;

```

## <a name="remarks"></a><span data-ttu-id="2c43f-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="2c43f-107">Remarks</span></span>

<span data-ttu-id="2c43f-108">Pour les plateformes Unicode, TCHAR est défini comme synonyme du type WCHAR.</span><span class="sxs-lookup"><span data-stu-id="2c43f-108">For Unicode platforms, TCHAR is defined as synonymous with the WCHAR type.</span></span> 
  
<span data-ttu-id="2c43f-p102">Les clients MAPI peuvent utiliser le type de donn�es TCHAR pour repr�senter une cha�ne de type WCHAR ou CHAR. Veillez � bien d�finir la constante symbolique UNICODE et � limiter la plateforme lorsque cela est n�cessaire. MAPI interpr�te les informations de plateforme et traduit en interne les caract�res TCHAR dans la cha�ne appropri�e. Le type de propri�t� MAPI, PT_TSTRING, fonctionne comme le type de donn�es TCHAR. Lorsque la plateforme prend en charge le langage Unicode, le type PT_UNICODE est affect� aux propri�t�s de type PT_TSTRING lors de la compilation. Si la plateforme ne prend pas en charge le langage Unicode, ces propri�t�s ont le type PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="2c43f-p102">MAPI clients can use the TCHAR data type to represent a string of either the WCHAR or char type. Be sure to define the symbolic constant UNICODE and limit the platform when it is required. MAPI will interpret the platform information and internally translate TCHAR to the appropriate string. The MAPI property type, PT_TSTRING, works just like the TCHAR data type. When the platform supports Unicode, properties of type PT_TSTRING are assigned the type PT_UNICODE at compile time. When the platform does not support Unicode, these properties are assigned the type PT_STRING8.</span></span>
  
<span data-ttu-id="2c43f-115">Pour plus d�informations sur cette fonctionnalit�, voir [Jeux de caract�res](mapi-character-sets.md) et [Liste de types de propri�t�s](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="2c43f-115">For more information about this functionality, see [Character Sets](mapi-character-sets.md) and [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2c43f-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c43f-116">See also</span></span>



[<span data-ttu-id="2c43f-117">Types de données MAPI</span><span class="sxs-lookup"><span data-stu-id="2c43f-117">MAPI Data Types</span></span>](mapi-data-types.md)

