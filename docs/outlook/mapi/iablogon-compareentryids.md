---
title: IABLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: cb4a38ff-2fdd-40ac-a613-12c3f11a1df9
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 03256f2dec62d0228c4d5456dcd1b60f66b13ad2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783597"
---
# <a name="iablogoncompareentryids"></a>IABLogon::CompareEntryIDs

  
  
**S’applique à**: Outlook 
  
Compare deux identificateurs d’entrée pour déterminer si elles font référence au même objet.
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulRet
);
```

## <a name="parameters"></a>Paramètres

 _cbEntryID1_
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID1_ . 
    
 _lpEntryID1_
  
> [in] Pointeur vers le premier identificateur d’entrée à comparer.
    
 _cbEntryID2_
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID2_ . 
    
 _lpEntryID2_
  
> [in] Pointeur vers le deuxième identificateur d’entrée à comparer.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpulRet_
  
> [out] Pointeur vers le résultat de la comparaison. TRUE pour indiquer que les identificateurs de deux entrée font référence au même objet ; Sinon, FALSE.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Les identificateurs d’entrée ont été comparées avec succès.
    
MAPI_E_INVALID_ENTRYID 
  
> Une ou les deux les identificateurs d’entrée n’appartiennent pas au fournisseur de carnet d’adresses.
    
## <a name="remarks"></a>Remarques

Fournisseurs de carnet d’adresses implémentent la méthode **CompareEntryIDs** pour comparer deux identificateurs d’entrée pour déterminer si elles font référence au même objet. 
  
 **CompareEntryIDs** est utile car un objet peut avoir plusieurs identificateurs d’entrée valide ; Cette situation peut se produire, par exemple, lorsque vous comparez un identificateur d’entrée à court terme avec un identificateur d’entrée à long terme. 
  
Pour plus d’informations sur la création d’identificateurs d’entrée, voir [Identificateurs d’entrée MAPI](mapi-entry-identifiers.md).
  
## <a name="see-also"></a>Voir aussi



[IABLogon : IUnknown](iablogoniunknown.md)

