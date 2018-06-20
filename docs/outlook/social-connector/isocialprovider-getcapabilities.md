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
ms.openlocfilehash: 54e28f22f2dc8fdbe19821d8188087b78c327518
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787598"
---
# <a name="isocialprovidergetcapabilities"></a><span data-ttu-id="a469c-103">ISocialProvider::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="a469c-103">ISocialProvider::GetCapabilities</span></span>

<span data-ttu-id="a469c-104">Obtient une chaîne qui décrit les fonctionnalités du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="a469c-104">Gets a string that describes provider capabilities.</span></span>
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="a469c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a469c-105">Parameters</span></span>

<span data-ttu-id="a469c-106">_résultat_</span><span class="sxs-lookup"><span data-stu-id="a469c-106">_result_</span></span>
  
> <span data-ttu-id="a469c-107">[out] Chaîne XML qui représente les fonctionnalités d’un fournisseur Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="a469c-107">[out] An XML string that represents the capabilities of an Outlook Social Connector (OSC) provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a469c-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="a469c-108">Remarks</span></span>

<span data-ttu-id="a469c-109">La chaîne XML renvoyée _résultat_ doit être conformes à la définition de schéma pour l’élément de **fonctionnalités** , comme défini dans le schéma XML d’extensibilité du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="a469c-109">The returned  _result_ XML string must comply with the schema definition for the **capabilities** element, as defined in the XML schema for OSC provider extensibility.</span></span> 
  
<span data-ttu-id="a469c-110">Le fournisseur doit renvoyer une chaîne de _résultat_ pour activer les appels suivants à partir de l’OSC au fournisseur fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="a469c-110">The provider must return a  _result_ string to enable subsequent calls from the OSC to the provider to operate correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a469c-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a469c-111">See also</span></span>

- [<span data-ttu-id="a469c-112">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a469c-112">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

