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
  
Compare deux identificateurs d'entrée pour déterminer s'ils font référence au même objet. MAPI renvoie cet appel à un fournisseur de services uniquement si les identificateurs uniques (UID) dans les deux identificateurs d'entrée à comparer sont gérés par ce fournisseur.
  
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
  
> dans Taille, en octets, de l'identificateur d'entrée pointé par le paramètre _lpEntryID1_ _._
    
 _lpEntryID1_
  
> dans Pointeur vers le premier identificateur d'entrée à comparer.
    
 _cbEntryID2_
  
> dans Taille, en octets, de l'identificateur d'entrée pointé par le paramètre _lpEntryID2_ _._
    
 _lpEntryID2_
  
> dans Pointeur vers le deuxième identificateur d'entrée à comparer.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpulResult_
  
> remarquer Pointeur vers le résultat renvoyé de la comparaison. TRUE si les deux identificateurs d'entrée font référence au même objet; Sinon, FALSe.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de banque de messages implémentent la méthode **IMSLogon:: CompareEntryIDs** pour comparer deux identificateurs d'entrée pour une entrée donnée dans une banque de messages afin de déterminer s'ils font référence au même objet. Si les deux identificateurs d'entrée font référence au même objet, **CompareEntryIDs** définit le paramètre _lpulResult_ sur true; s'ils font référence à des objets différents, **CompareEntryIDs** définit _lpulResult_ sur false. 
  
 **CompareEntryIDs** est utile, car un objet peut avoir plus d'un identificateur d'entrée valide. Cela peut se produire, par exemple, après l'installation d'une nouvelle version d'un fournisseur de banque de messages. 
  
## <a name="see-also"></a>Voir aussi



[IMSLogon : IUnknown](imslogoniunknown.md)

