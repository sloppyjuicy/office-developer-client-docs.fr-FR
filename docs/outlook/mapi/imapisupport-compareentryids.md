---
title: IMAPISupportCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.CompareEntryIDs
api_type:
- COM
ms.assetid: be6991d9-6353-4838-bc6b-39de51a94d8d
ms.openlocfilehash: cdbfb58930887b1e20e32dde87f1233d4428953e
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379660"
---
# <a name="imapisupportcompareentryids"></a>IMAPISupport::CompareEntryIDs

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Compare deux identificateurs d’entrée pour déterminer s’ils font référence au même objet. 
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a>Paramètres

 _cbEntryID1_
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par  _le paramètre lpEntryID1_ . 
    
 _lpEntryID1_
  
> [in] Pointeur vers le premier identificateur d’entrée à comparer.
    
 _cbEntryID2_
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par  _le paramètre lpEntryID2_ . 
    
 _lpEntryID2_
  
> [in] Pointeur vers le deuxième identificateur d’entrée à comparer.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpulResult_
  
> [out] Pointeur vers le résultat de la comparaison. TRUE si les deux identificateurs d’entrée font référence au même objet ; sinon, FALSE.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La comparaison a réussi.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> L’un ou les deux identificateurs d’entrée spécifiés en tant que paramètres ne font pas référence à des objets valides, éventuellement parce qu’ils sont actuellement non ouvert et indisponibles.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::CompareEntryIDs** est implémentée pour les objets de prise en charge du carnet d’adresses et du fournisseur de magasins de messages. **CompareEntryIDs** compare deux identificateurs d’entrée qui appartiennent à un seul fournisseur de services pour déterminer s’ils font référence au même objet. MAPI extrait la partie [MAPIUID](mapiuid.md) des identificateurs d’entrée pour déterminer le fournisseur de services responsable des objets. MAPI appelle ensuite la méthode **CompareEntryIDs** de son objet d’logo pour effectuer la comparaison. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

 **CompareEntryIDs est utile** car un objet peut avoir plusieurs identificateurs d’entrée valides. Cette situation peut se produire, par exemple, après l’installation d’une nouvelle version d’un fournisseur de services. 
  
Si **CompareEntryIDs** renvoie une erreur, ne pas prendre d’action en fonction du résultat de la comparaison. Au lieu de cela, prenez l’approche la plus prudent possible. **CompareEntryIDs** peut échouer si, par exemple, l’un des identificateurs d’entrée ou les deux contiennent une structure **MAPIUID** non valide. 
  
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

