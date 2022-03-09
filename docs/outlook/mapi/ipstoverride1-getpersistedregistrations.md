---
title: IPSTOVERRIDE1GetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPSTOVERRIDE1.GetPersistedRegistrations
api_type:
- COM
ms.assetid: 027092f0-f2d6-49e8-a8d0-8926824953a2
ms.openlocfilehash: 29c0eb0cad8861e3f1d1dd80f3b431fc68a5cd3d
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63375635"
---
# <a name="ipstoverride1getpersistedregistrations"></a>IPSTOVERRIDE1::GetPersistedRegistrations

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Extrait la liste des inscriptions pour le fichier de dossiers personnels (.pst).
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a>Paramètres

 _ppmval_
  
> [in] Pointeur vers un pointeur vers une structure [SPropValue](spropvalue.md) . Le membre ulPropTag de cette structure est du type PT_MV_UNICODE et le membre de valeur MVszW sera un tableau de chaînes Unicode terminées par null. Ces chaînes sont des chemins d’accès aux DLL pour lesquelles l’inscription a été persistante. 
    
> [!NOTE]
> La prise en charge de .pst pour ANSI n’est pas implémentée. 
  
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel de fonction a réussi.
    
## <a name="see-also"></a>Voir aussi



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

