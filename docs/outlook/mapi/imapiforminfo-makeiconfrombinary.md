---
title: IMAPIFormInfoMakeIconFromBinary
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.MakeIconFromBinary
api_type:
- COM
ms.assetid: 4daeddd7-3f0c-4178-ae8d-f74814090d40
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 418056f7222d5ab05f43a3661c1811bf2ae15be8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342111"
---
# <a name="imapiforminfomakeiconfrombinary"></a><span data-ttu-id="5809c-103">IMAPIFormInfo::MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="5809c-103">IMAPIFormInfo::MakeIconFromBinary</span></span>

  
  
<span data-ttu-id="5809c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5809c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5809c-105">Génère une icône à partir de l'une des propriétés d'icône d'un formulaire.</span><span class="sxs-lookup"><span data-stu-id="5809c-105">Builds an icon from one of the icon properties of a form.</span></span>
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a><span data-ttu-id="5809c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5809c-106">Parameters</span></span>

 <span data-ttu-id="5809c-107">_nPropID_</span><span class="sxs-lookup"><span data-stu-id="5809c-107">_nPropID_</span></span>
  
> <span data-ttu-id="5809c-108">dans Identificateur de propriété d'une propriété d'icône.</span><span class="sxs-lookup"><span data-stu-id="5809c-108">[in] A property identifier for an icon property.</span></span>
    
 <span data-ttu-id="5809c-109">_phicon_</span><span class="sxs-lookup"><span data-stu-id="5809c-109">_phicon_</span></span>
  
> <span data-ttu-id="5809c-110">remarquer Pointeur vers l'icône renvoyée.</span><span class="sxs-lookup"><span data-stu-id="5809c-110">[out] A pointer to the returned icon.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5809c-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5809c-111">Return value</span></span>

<span data-ttu-id="5809c-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="5809c-112">S_OK</span></span> 
  
> <span data-ttu-id="5809c-113">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="5809c-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5809c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5809c-114">Remarks</span></span>

<span data-ttu-id="5809c-115">Les applications clientes appellent la méthode **IMAPIFormInfo:: MakeIconFromBinary** pour créer une icône à partir de l'une des propriétés d'icône d'un formulaire.</span><span class="sxs-lookup"><span data-stu-id="5809c-115">Client applications call the **IMAPIFormInfo::MakeIconFromBinary** method to build an icon from one of the icon properties of a form.</span></span> <span data-ttu-id="5809c-116">Dans le paramètre _nPropID_ , **MakeIconFromBinary** prend l'identificateur de propriété de l'une des propriétés d'icône d'un formulaire.</span><span class="sxs-lookup"><span data-stu-id="5809c-116">In the  _nPropID_ parameter, **MakeIconFromBinary** takes the property identifier of one of the icon properties of a form.</span></span> <span data-ttu-id="5809c-117">À l'aide de cet identificateur de propriété, il génère une icône qui peut être affichée dans les vues de tableau qui incluent des colonnes de propriétés pour les icônes.</span><span class="sxs-lookup"><span data-stu-id="5809c-117">Using this property identifier, it builds an icon that can be displayed in table views that include property columns for icons.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5809c-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5809c-118">See also</span></span>



[<span data-ttu-id="5809c-119">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5809c-119">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

