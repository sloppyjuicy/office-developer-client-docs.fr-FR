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
ms.openlocfilehash: 640923511241b08e5a86e9733aab5cc2e9237c23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576574"
---
# <a name="imsgstorecompareentryids"></a>IMsgStore::CompareEntryIDs

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Compare deux identificateurs d’entrée pour déterminer si elles font référence à la même entrée dans une banque de messages. MAPI passe cet appel à un fournisseur de services uniquement si les identificateurs uniques (UID) dans les deux identificateurs d’entrée à comparer sont gérés par ce fournisseur.
  
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
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID1_ _._
    
 _lpEntryID1_
  
> [in] Pointeur vers le premier identificateur d’entrée à comparer.
    
 _cbEntryID2_
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID2_ _._
    
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
  
> Un ou les deux les identificateurs d’entrée spécifiés comme paramètres ne font pas référence aux objets, éventuellement, car les objets correspondants sont non ouverts et non à présentent.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgStore::CompareEntryIDs** compare deux identificateurs d’entrée qui appartiennent à la banque de messages pour déterminer si elles font référence au même objet. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

 **CompareEntryIDs** est utile car un objet peut avoir plusieurs identificateurs d’entrée valide (par exemple, après avoir installé une nouvelle version d’un fournisseur de magasin de message). 
  
Si **CompareEntryIDs** renvoie une erreur, ne prend aucune action basée sur le résultat de la comparaison. Au lieu de cela, adoptez une approche plus prudente possible. **CompareEntryIDs** peut échouer si, par exemple, un ou les deux les identificateurs d’entrée contient un non valide **MAPIUID**. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnCompareEntryIDs  <br/> |MFCMAPI utilise la méthode **IMsgStore::CompareEntryIDs** pour comparer les identificateurs d’entrée.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

