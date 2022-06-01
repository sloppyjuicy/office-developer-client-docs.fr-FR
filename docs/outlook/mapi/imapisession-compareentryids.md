---
title: IMAPISessionCompareEntryIDs
description: IMAPISessionCompareEntryIDs compare deux identificateurs d’entrée pour déterminer s’ils font référence au même objet.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.CompareEntryIDs
api_type:
- COM
ms.assetid: 319f10e9-db8d-4d16-aa1f-6cf5fef493eb
ms.openlocfilehash: 218d79092489c1d8d0c21e0c324c99c2fc8818ba
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817703"
---
# <a name="imapisessioncompareentryids"></a>IMAPISession::CompareEntryIDs

  
  
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
  
> [in] Nombre d’octets dans l’identificateur d’entrée pointé par le paramètre  _lpEntryID1_ . 
    
 _lpEntryID1_
  
> [in] Pointeur vers le premier identificateur d’entrée à comparer.
    
 _cbEntryID2_
  
> [in] Nombre d’octets dans l’identificateur d’entrée pointé par le paramètre  _lpEntryID2_ . 
    
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
  
> Un ou les deux identificateurs d’entrée spécifiés en tant que paramètres ne font pas référence à des objets, peut-être parce que ces objets sont actuellement non ouverts et indisponibles.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::CompareEntryIDs** compare deux identificateurs d’entrée qui appartiennent à un seul fournisseur de services pour déterminer s’ils font référence au même objet. MAPI extrait la partie [MAPIUID](mapiuid.md) des identificateurs d’entrée pour déterminer le fournisseur de services responsable des objets, puis appelle la méthode **CompareEntryIDs** de son objet d’ouverture de session pour effectuer la comparaison. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

La méthode **CompareEntryIDs** est utile, car un objet peut avoir plusieurs identificateurs d’entrée valides. Cette situation peut se produire, par exemple, après l’installation d’une nouvelle version d’un fournisseur de services. 
  
Si **CompareEntryIDs** retourne une erreur, n’effectuez aucune action en fonction du résultat de la comparaison. Au lieu de cela, adopter l’approche la plus conservatrice possible. **CompareEntryIDs** peut échouer si, par exemple, un ou les deux identificateurs d’entrée contiennent un **MAPIUID** non valide. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CbaseDialog::OnCompareEntryIDs  <br/> |MFCMAPI utilise la méthode **IMAPISession::CompareEntryIDs** pour comparer deux ID d’entrée qu’un utilisateur entre. |
   
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

