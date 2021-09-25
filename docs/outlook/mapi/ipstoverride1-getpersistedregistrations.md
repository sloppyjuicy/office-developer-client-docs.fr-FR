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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 397eb3ecfeb245a6afe91be98a5def4c35ba4873
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579753"
---
# <a name="ipstoverride1getpersistedregistrations"></a>IPSTOVERRIDE1::GetPersistedRegistrations

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Extrait la liste des inscriptions pour le fichier de dossiers personnels (.pst).
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a>Paramètres

 _ppmval_
  
> [in] Pointeur vers un pointeur vers une structure [SPropValue.](spropvalue.md) Le membre ulPropTag de cette structure est de type PT_MV_UNICODE et le membre de valeur MVszW sera un tableau de chaînes Unicode terminées par null. Ces chaînes sont des chemins d’accès aux DLLs pour lesquelles l’inscription a été persistante. 
    
> [!NOTE]
> La prise en charge de .pst pour ANSI n’est pas implémentée. 
  
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel de fonction a réussi.
    
## <a name="see-also"></a>Voir aussi



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

