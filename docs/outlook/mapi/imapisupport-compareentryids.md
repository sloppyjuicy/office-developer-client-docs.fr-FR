---
title: IMAPISupportCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CompareEntryIDs
api_type:
- COM
ms.assetid: be6991d9-6353-4838-bc6b-39de51a94d8d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9dbf02fc94519d40431fb6bd493ef8e68df59d11
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566543"
---
# <a name="imapisupportcompareentryids"></a>IMAPISupport::CompareEntryIDs

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Compare deux identificateurs d’entrée pour déterminer si elles font référence au même objet. 
  
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
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID1_ . 
    
 _lpEntryID1_
  
> [in] Pointeur vers le premier identificateur d’entrée à comparer.
    
 _cbEntryID2_
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID2_ . 
    
 _lpEntryID2_
  
> [in] Pointeur vers le deuxième identificateur d’entrée à comparer.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpulResult_
  
> [out] Pointeur vers le résultat de la comparaison. TRUE si les identificateurs de deux entrée font référence au même objet ; Sinon, FALSE.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La comparaison a réussi.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Une ou les deux les identificateurs d’entrée spécifiés en tant que paramètres ne font pas référencent aux objets valides, éventuellement, car ils sont en cours non ouverts et non disponible.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::CompareEntryIDs** est implémentée pour adresse livre et message fournisseur prise en charge des objets store. **CompareEntryIDs** compare deux identificateurs d’entrée qui appartiennent à un fournisseur de service unique pour déterminer si elles font référence au même objet. MAPI extrait la partie [MAPIUID](mapiuid.md) les identificateurs d’entrée pour déterminer le fournisseur de services responsable pour les objets. MAPI appelle ensuite la méthode **CompareEntryIDs** de l’objet de son ouverture de session pour effectuer la comparaison. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

 **CompareEntryIDs** est utile car un objet peut avoir plusieurs identificateurs d’entrée valide. Cette situation peut se produire, par exemple, après avoir installé une nouvelle version d’un fournisseur de services. 
  
Si **CompareEntryIDs** renvoie une erreur, ne prend aucune action basée sur le résultat de la comparaison. Au lieu de cela, adoptez une approche plus prudente possible. **CompareEntryIDs** peut échouer si, par exemple, un ou les deux les identificateurs d’entrée contient une structure **MAPIUID** non valide. 
  
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

