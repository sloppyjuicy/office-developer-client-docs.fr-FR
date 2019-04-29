---
title: IMAPISessionCompareEntryIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.CompareEntryIDs
api_type:
- COM
ms.assetid: 319f10e9-db8d-4d16-aa1f-6cf5fef493eb
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4dfde82aa843072168288f4e0b0084dfccd5cd2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427814"
---
# <a name="imapisessioncompareentryids"></a>IMAPISession::CompareEntryIDs

  
  
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
  
> L'un des identificateurs d'entrée spécifiés comme paramètres ne fait pas référence à des objets, probablement parce que ces objets ne sont pas ouverts et ne sont pas disponibles actuellement.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession:: CompareEntryIDs** compare deux identificateurs d'entrée qui appartiennent à un seul fournisseur de services pour déterminer s'ils font référence au même objet. MAPI extrait la partie [MAPIUID](mapiuid.md) des identificateurs d'entrée afin de déterminer le fournisseur de services responsable des objets, puis appelle la méthode **CompareEntryIDs** de l'objet Logon pour effectuer la comparaison. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

La méthode **CompareEntryIDs** est utile, car un objet peut avoir plusieurs identificateurs d'entrée valides. Cette situation peut se produire, par exemple, après l'installation d'une nouvelle version d'un fournisseur de services. 
  
Si **CompareEntryIDs** renvoie une erreur, n'effectuez aucune action en fonction du résultat de la comparaison. Au lieu de cela, adoptez l'approche la plus conservatrice possible. **CompareEntryIDs** peut échouer si, par exemple, un ou les deux identificateurs d'entrée contiennent un **MAPIUID**non valide. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|BaseDialog. cpp  <br/> |CbaseDialog:: OnCompareEntryIDs  <br/> |MFCMAPI utilise la méthode **IMAPISession:: CompareEntryIDs** pour comparer deux ID d'entrée entrés par un utilisateur.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

