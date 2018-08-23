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
ms.openlocfilehash: 548ec33e39e181aba8a72b5325f3f426b9d51762
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575867"
---
# <a name="ipstoverride1getpersistedregistrations"></a>IPSTOVERRIDE1::GetPersistedRegistrations

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Récupère la liste des enregistrements pour le fichier de dossiers personnels (.pst).
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a>Paramètres

 _ppmval_
  
> [in] Pointeur vers un pointeur vers une structure [SPropValue](spropvalue.md) . Le membre ulPropTag de cette structure est du type PT_MV_UNICODE, et le membre de la valeur MVszW sera un tableau de chaînes Unicode. Ces chaînes sont des chemins d’accès aux fichiers DLL pour laquelle l’enregistrement a été conservée. 
    
> [!NOTE]
> prise en charge .pst ANSI n’est pas implémenté. 
  
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’appel de fonction a réussi.
    
## <a name="see-also"></a>Voir aussi



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

