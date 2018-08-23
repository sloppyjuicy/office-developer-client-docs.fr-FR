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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 30f55044327eecee3ab0d8ee2509d7132ab6e8ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570127"
---
# <a name="imapiforminfomakeiconfrombinary"></a><span data-ttu-id="37aec-103">IMAPIFormInfo::MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="37aec-103">IMAPIFormInfo::MakeIconFromBinary</span></span>

  
  
<span data-ttu-id="37aec-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37aec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37aec-105">Crée une icône à partir d’une des propriétés d’icône d’un formulaire.</span><span class="sxs-lookup"><span data-stu-id="37aec-105">Builds an icon from one of the icon properties of a form.</span></span>
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a><span data-ttu-id="37aec-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37aec-106">Parameters</span></span>

 <span data-ttu-id="37aec-107">_nPropID_</span><span class="sxs-lookup"><span data-stu-id="37aec-107">_nPropID_</span></span>
  
> <span data-ttu-id="37aec-108">[in] Un identificateur de propriété pour une propriété d’icône.</span><span class="sxs-lookup"><span data-stu-id="37aec-108">[in] A property identifier for an icon property.</span></span>
    
 <span data-ttu-id="37aec-109">_phicon_</span><span class="sxs-lookup"><span data-stu-id="37aec-109">_phicon_</span></span>
  
> <span data-ttu-id="37aec-110">[out] Pointeur vers l’icône renvoyée.</span><span class="sxs-lookup"><span data-stu-id="37aec-110">[out] A pointer to the returned icon.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="37aec-111">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="37aec-111">Return value</span></span>

<span data-ttu-id="37aec-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="37aec-112">S_OK</span></span> 
  
> <span data-ttu-id="37aec-113">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="37aec-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="37aec-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="37aec-114">Remarks</span></span>

<span data-ttu-id="37aec-115">Applications clientes appellent la méthode **IMAPIFormInfo::MakeIconFromBinary** pour créer une icône de l’une des propriétés d’icône d’un formulaire.</span><span class="sxs-lookup"><span data-stu-id="37aec-115">Client applications call the **IMAPIFormInfo::MakeIconFromBinary** method to build an icon from one of the icon properties of a form.</span></span> <span data-ttu-id="37aec-116">Dans le paramètre _nPropID_ , **MakeIconFromBinary** est l’identificateur de propriété d’une des propriétés d’icône d’un formulaire.</span><span class="sxs-lookup"><span data-stu-id="37aec-116">In the  _nPropID_ parameter, **MakeIconFromBinary** takes the property identifier of one of the icon properties of a form.</span></span> <span data-ttu-id="37aec-117">À l’aide de l’identificateur de cette propriété, il crée une icône qui peut être affichée dans les tableaux qui contiennent des colonnes de propriété pour les icônes.</span><span class="sxs-lookup"><span data-stu-id="37aec-117">Using this property identifier, it builds an icon that can be displayed in table views that include property columns for icons.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="37aec-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37aec-118">See also</span></span>



[<span data-ttu-id="37aec-119">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="37aec-119">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

