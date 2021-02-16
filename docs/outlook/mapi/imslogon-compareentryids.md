---
title: IMSLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: 481812d6-8e94-4510-b288-55501dd5757c
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4196ed8b949ecb9e23c4bd34380db9cc5a369e23
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410132"
---
# <a name="imslogoncompareentryids"></a>IMSLogon::CompareEntryIDs

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Compare deux identificateurs d’entrée pour déterminer s’ils font référence au même objet. MAPI fait référence à cet appel à un fournisseur de services uniquement si les identificateurs uniques (IUD) des deux identificateurs d’entrée à comparer sont gérés par ce fournisseur.
  
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
  
> [in] Taille, en octets, de l’identificateur d’entrée pointé par  _le paramètre lpEntryID1_  _._
    
 _lpEntryID1_
  
> [in] Pointeur vers le premier identificateur d’entrée à comparer.
    
 _cbEntryID2_
  
> [in] Taille, en octets, de l’identificateur d’entrée pointé par  _le paramètre lpEntryID2_  _._
    
 _lpEntryID2_
  
> [in] Pointeur vers le deuxième identificateur d’entrée à comparer.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpulResult_
  
> [out] Pointeur vers le résultat renvoyé de la comparaison. TRUE si les deux identificateurs d’entrée font référence au même objet ; sinon, FALSE.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de magasins de messages implémentent la méthode **IMSLogon::CompareEntryIDs** pour comparer deux identificateurs d’entrée pour une entrée donnée dans une magasin de messages afin de déterminer s’ils font référence au même objet. Si les deux identificateurs d’entrée font référence au même objet, **CompareEntryIDs** définit le paramètre  _lpulResult_ sur TRUE ; S’ils font référence à différents objets, **CompareEntryIDs** définit  _lpulResult_ sur FALSE. 
  
 **CompareEntryIDs est utile** car un objet peut avoir plusieurs identificateurs d’entrée valides. Cela peut se produire, par exemple, après l’installation d’une nouvelle version d’un fournisseur de magasins de messages. 
  
## <a name="see-also"></a>Voir aussi



[IMSLogon : IUnknown](imslogoniunknown.md)

