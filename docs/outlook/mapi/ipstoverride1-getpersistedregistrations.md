---
title: IPSTOVERRIDE1GetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1.GetPersistedRegistrations
api_type:
- COM
ms.assetid: 027092f0-f2d6-49e8-a8d0-8926824953a2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 822b4164737aa6010ccce108b544410104ac023d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415130"
---
# <a name="ipstoverride1getpersistedregistrations"></a>IPSTOVERRIDE1::GetPersistedRegistrations

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Extrait la liste des inscriptions pour le fichier de dossiers personnels (.pst).
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a>Parameters

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

