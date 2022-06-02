---
title: IMsgStoreCompareEntryIDs
description: IMsgStore CompareEntryIDs compare deux identificateurs d’entrée pour déterminer s’ils font référence à la même entrée dans un magasin de messages.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.CompareEntryIDs
api_type:
- COM
ms.assetid: 33d70748-0d3f-4be4-bcb5-7ec048887944
ms.openlocfilehash: 0c794853bf00d9c6eb7b950bed2d8d681200a486
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828552"
---
# <a name="imsgstorecompareentryids"></a>IMsgStore::CompareEntryIDs

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Compare deux identificateurs d’entrée pour déterminer s’ils font référence à la même entrée dans un magasin de messages. MAPI transmet cet appel à un fournisseur de services uniquement si les identificateurs uniques (IUD) des deux identificateurs d’entrée à comparer sont gérés par ce fournisseur.
  
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
  
> [in] Nombre d’octets dans l’identificateur d’entrée pointé par le paramètre  _lpEntryID1_  _._
    
 _lpEntryID1_
  
> [in] Pointeur vers le premier identificateur d’entrée à comparer.
    
 _cbEntryID2_
  
> [in] Nombre d’octets dans l’identificateur d’entrée pointé par le paramètre  _lpEntryID2_  _._
    
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
  
> Un ou les deux identificateurs d’entrée spécifiés en tant que paramètres ne font pas référence aux objets, peut-être parce que les objets correspondants ne sont pas ouverts et non disponibles actuellement.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgStore::CompareEntryIDs** compare deux identificateurs d’entrée qui appartiennent au magasin de messages pour déterminer s’ils font référence au même objet. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

 **CompareEntryIDs** est utile, car un objet peut avoir plusieurs identificateurs d’entrée valides (par exemple, après l’installation d’une nouvelle version d’un fournisseur de magasin de messages). 
  
Si **CompareEntryIDs** retourne une erreur, n’effectuez aucune action en fonction du résultat de la comparaison. Au lieu de cela, adopter l’approche la plus conservatrice possible. **CompareEntryIDs** peut échouer si, par exemple, un ou les deux identificateurs d’entrée contiennent un **MAPIUID** non valide. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnCompareEntryIDs  <br/> |MFCMAPI utilise la méthode **IMsgStore::CompareEntryIDs** pour comparer les ID d’entrée. |
   
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

