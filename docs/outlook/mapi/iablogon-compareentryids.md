---
title: IABLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: cb4a38ff-2fdd-40ac-a613-12c3f11a1df9
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ca5474e56a1a72124e6d49bc67329994e6eec04f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571919"
---
# <a name="iablogoncompareentryids"></a>IABLogon::CompareEntryIDs

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Compare deux identificateurs d’entrée pour déterminer s’ils font référence au même objet.
  
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
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID1._ 
    
 _lpEntryID1_
  
> [in] Pointeur vers le premier identificateur d’entrée à comparer.
    
 _cbEntryID2_
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID2._ 
    
 _lpEntryID2_
  
> [in] Pointeur vers le deuxième identificateur d’entrée à comparer.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpulRet_
  
> [out] Pointeur vers le résultat de la comparaison. TRUE pour indiquer que les deux identificateurs d’entrée font référence au même objet ; sinon, FALSE.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les identificateurs d’entrée ont été comparés.
    
MAPI_E_INVALID_ENTRYID 
  
> L’un des identificateurs d’entrée ou les deux n’appartiennent pas au fournisseur de carnet d’adresses.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de carnets d’adresses implémentent la méthode **CompareEntryIDs** pour comparer deux identificateurs d’entrée afin de déterminer s’ils font référence au même objet. 
  
 **CompareEntryIDs est utile** car un objet peut avoir plusieurs identificateurs d’entrée valides ; Une telle situation peut se produire, par exemple, lorsque vous comparez un identificateur d’entrée à court terme à un identificateur d’entrée à long terme. 
  
Pour plus d’informations sur la création d’identificateurs d’entrée, voir identificateurs d’entrée [MAPI.](mapi-entry-identifiers.md)
  
## <a name="see-also"></a>Voir aussi



[IABLogon : IUnknown](iablogoniunknown.md)

