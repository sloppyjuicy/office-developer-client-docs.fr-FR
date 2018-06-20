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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 56aaf5caf93f90f54d152ab3684ca592cd45cd1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784409"
---
# <a name="ipstoverride1getpersistedregistrations"></a>IPSTOVERRIDE1::GetPersistedRegistrations

  
  
**S’applique à**: Outlook 
  
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

