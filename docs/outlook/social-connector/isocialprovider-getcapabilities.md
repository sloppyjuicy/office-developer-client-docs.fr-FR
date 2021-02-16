---
title: ISocialProviderGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f40d5405-12e3-475b-b731-d2223ab70c1d
description: Obtient une chaîne qui décrit les fonctionnalités du fournisseur.
ms.openlocfilehash: cf3d1418ac0ecbfc3f67bb550a24ec71781f2637
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408102"
---
# <a name="isocialprovidergetcapabilities"></a><span data-ttu-id="64d59-103">ISocialProvider::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="64d59-103">ISocialProvider::GetCapabilities</span></span>

<span data-ttu-id="64d59-104">Obtient une chaîne qui décrit les fonctionnalités du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="64d59-104">Gets a string that describes provider capabilities.</span></span>
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="64d59-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64d59-105">Parameters</span></span>

<span data-ttu-id="64d59-106">_result_</span><span class="sxs-lookup"><span data-stu-id="64d59-106">_result_</span></span>
  
> <span data-ttu-id="64d59-107">[out] Chaîne XML qui représente les fonctionnalités d’un fournisseur Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="64d59-107">[out] An XML string that represents the capabilities of an Outlook Social Connector (OSC) provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="64d59-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="64d59-108">Remarks</span></span>

<span data-ttu-id="64d59-109">La  _chaîne_ XML de résultat renvoyée doit être conforme à la définition de schéma de l’élément **capabilities,** tel que défini dans le schéma XML pour l’extensibilité du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="64d59-109">The returned  _result_ XML string must comply with the schema definition for the **capabilities** element, as defined in the XML schema for OSC provider extensibility.</span></span> 
  
<span data-ttu-id="64d59-110">Le fournisseur doit retourner une chaîne  _de_ résultats pour permettre aux appels ultérieurs de l’OSC au fournisseur de fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="64d59-110">The provider must return a  _result_ string to enable subsequent calls from the OSC to the provider to operate correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="64d59-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64d59-111">See also</span></span>

- [<span data-ttu-id="64d59-112">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="64d59-112">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

