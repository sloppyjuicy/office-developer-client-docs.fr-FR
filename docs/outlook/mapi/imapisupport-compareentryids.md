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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 6c79943792c8c17ee007c39b5c5c215a6fbc0699
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331569"
---
# <a name="imapisupportcompareentryids"></a>IMAPISupport::CompareEntryIDs

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Compare deux identificateurs d'entrée pour déterminer s'ils font référence au même objet. 
  
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
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID1_ . 
    
 _lpEntryID1_
  
> dans Pointeur vers le premier identificateur d'entrée à comparer.
    
 _cbEntryID2_
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID2_ . 
    
 _lpEntryID2_
  
> dans Pointeur vers le deuxième identificateur d'entrée à comparer.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpulResult_
  
> remarquer Pointeur vers le résultat de la comparaison. TRUE si les deux identificateurs d'entrée font référence au même objet; Sinon, FALSe.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La comparaison a réussi.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> L'un des identificateurs d'entrée spécifiés en tant que paramètres ne fait pas référence à des objets valides, car ils ne sont pas actuellement ouverts et indisponibles.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport:: CompareEntryIDs** est implémentée pour les objets de prise en charge du carnet d'adresses et du fournisseur de banque de messages. **CompareEntryIDs** compare deux identificateurs d'entrée qui appartiennent à un seul fournisseur de services pour déterminer s'ils font référence au même objet. MAPI extrait la partie [MAPIUID](mapiuid.md) des identificateurs d'entrée afin de déterminer le fournisseur de services responsable des objets. MAPI appelle ensuite la méthode **CompareEntryIDs** de l'objet Logon pour effectuer la comparaison. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

 **CompareEntryIDs** est utile, car un objet peut avoir plus d'un identificateur d'entrée valide. Cette situation peut se produire, par exemple, après l'installation d'une nouvelle version d'un fournisseur de services. 
  
Si **CompareEntryIDs** renvoie une erreur, n'effectuez aucune action en fonction du résultat de la comparaison. Au lieu de cela, adoptez l'approche la plus conservatrice possible. **CompareEntryIDs** peut échouer si, par exemple, un ou les deux identificateurs d'entrée contiennent une structure **MAPIUID** incorrecte. 
  
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

