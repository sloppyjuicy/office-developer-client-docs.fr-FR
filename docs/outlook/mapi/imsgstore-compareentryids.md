---
title: IMsgStoreCompareEntryIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.CompareEntryIDs
api_type:
- COM
ms.assetid: 33d70748-0d3f-4be4-bcb5-7ec048887944
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2a2439bae79b497f018391983e2c4b03a35eee70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424251"
---
# <a name="imsgstorecompareentryids"></a>IMsgStore::CompareEntryIDs

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Compare deux identificateurs d’entrée pour déterminer s’ils font référence à la même entrée dans une magasin de messages. MAPI transmet cet appel à un fournisseur de services uniquement si les identificateurs uniques (IUD) des deux identificateurs d’entrée à comparer sont gérés par ce fournisseur.
  
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

## <a name="parameters"></a>Parameters

 _cbEntryID1_
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par  _le paramètre lpEntryID1_  _._
    
 _lpEntryID1_
  
> [in] Pointeur vers le premier identificateur d’entrée à comparer.
    
 _cbEntryID2_
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par  _le paramètre lpEntryID2_  _._
    
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
  
> L’un ou les deux identificateurs d’entrée spécifiés en tant que paramètres ne font pas référence à des objets, probablement parce que les objets correspondants ne sont pas ouvert et sont actuellement indisponibles.
    
## <a name="remarks"></a>Remarques

La **méthode IMsgStore::CompareEntryIDs** compare deux identificateurs d’entrée qui appartiennent à la magasin de messages pour déterminer s’ils font référence au même objet. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

 **CompareEntryIDs est** utile car un objet peut avoir plusieurs identificateurs d’entrée valides (par exemple, après l’installation d’une nouvelle version d’un fournisseur de magasins de messages). 
  
Si **CompareEntryIDs** renvoie une erreur, ne pas prendre d’action en fonction du résultat de la comparaison. Au lieu de cela, prenez l’approche la plus prudent possible. **CompareEntryIDs peut** échouer si, par exemple, l’un des identificateurs d’entrée ou les deux contiennent un **MAPIUID non valide.** 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnCompareEntryIDs  <br/> |MFCMAPI utilise la **méthode IMsgStore::CompareEntryIDs** pour comparer les ID d’entrée.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

