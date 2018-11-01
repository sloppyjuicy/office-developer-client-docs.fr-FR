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
ms.openlocfilehash: c5b2d7db745cc270c0be7ee2184e86c6a4f97aad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594298"
---
# <a name="imslogoncompareentryids"></a>IMSLogon::CompareEntryIDs

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Compare deux identificateurs d’entrée pour déterminer si elles font référence au même objet. MAPI fait référence à cet appel à un fournisseur de services uniquement si les identificateurs uniques (UID) dans les deux identificateurs d’entrée à comparer sont gérés par ce fournisseur.
  
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
  
> [in] La taille, en octets, de l’identificateur d’entrée indiqué par le paramètre _lpEntryID1_ _._
    
 _lpEntryID1_
  
> [in] Pointeur vers le premier identificateur d’entrée à comparer.
    
 _cbEntryID2_
  
> [in] La taille, en octets, de l’identificateur d’entrée indiqué par le paramètre _lpEntryID2_ _._
    
 _lpEntryID2_
  
> [in] Pointeur vers le deuxième identificateur d’entrée à comparer.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpulResult_
  
> [out] Pointeur vers le résultat de la comparaison retourné. TRUE si les identificateurs de deux entrée font référence au même objet ; Sinon, FALSE.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Fournisseurs de magasins de message implémentent la méthode **IMSLogon::CompareEntryIDs** pour comparer deux identificateurs d’entrée pour une entrée de donnée dans une banque de messages pour déterminer si elles font référence au même objet. Si les identificateurs de deux entrée font référence au même objet, **CompareEntryIDs** définit le paramètre _lpulResult_ sur TRUE. s’ils font référence à des objets différents, **CompareEntryIDs** définit _lpulResult_ sur FALSE. 
  
 **CompareEntryIDs** est utile car un objet peut avoir plusieurs identificateurs d’entrée valide. Par exemple, cela peut se produire après l’installation d’une nouvelle version d’un fournisseur de magasin de message. 
  
## <a name="see-also"></a>Voir aussi



[IMSLogon : IUnknown](imslogoniunknown.md)

