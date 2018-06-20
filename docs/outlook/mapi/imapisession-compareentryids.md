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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: df6347298aab5404ec69bd9ac876863e31b741d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783944"
---
# <a name="imapisessioncompareentryids"></a>IMAPISession::CompareEntryIDs

  
  
**S’applique à**: Outlook 
  
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
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La comparaison a réussi.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Une ou les deux les identificateurs d’entrée spécifiés en tant que paramètres ne font pas référencent aux objets, éventuellement, car ces objets sont actuellement non ouverts et non disponible.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::CompareEntryIDs** compare deux identificateurs d’entrée qui appartiennent à un fournisseur de service unique pour déterminer si elles font référence au même objet. MAPI extrait la partie [MAPIUID](mapiuid.md) les identificateurs d’entrée pour déterminer le fournisseur de services responsable pour les objets et appelle ensuite la méthode **CompareEntryIDs** de l’objet de son ouverture de session pour effectuer la comparaison. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

La méthode **CompareEntryIDs** est utile car un objet peut avoir plusieurs identificateurs d’entrée valide. Cette situation peut se produire, par exemple, après avoir installé une nouvelle version d’un fournisseur de services. 
  
Si **CompareEntryIDs** renvoie une erreur, ne prend aucune action basée sur le résultat de la comparaison. Au lieu de cela, adoptez une approche plus prudente possible. **CompareEntryIDs** peut échouer si, par exemple, un ou les deux les identificateurs d’entrée contient un non valide **MAPIUID**. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CbaseDialog::OnCompareEntryIDs  <br/> |MFCMAPI utilise la méthode **IMAPISession::CompareEntryIDs** pour comparer deux identificateurs d’entrée par un utilisateur.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

