---
title: IMSProviderCompareStoreIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.CompareStoreIDs
api_type:
- COM
ms.assetid: c3e3cfaa-9c4a-482a-9411-9c4ab01d312f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 734e53c1e897c902c72319aa6f2d3d7af2d23fb6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431707"
---
# <a name="imsprovidercomparestoreids"></a>IMSProvider::CompareStoreIDs

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Compare deux identificateurs d'entrée de banque de messages pour déterminer s'ils font référence au même objet Store.
  
```cpp
HRESULT CompareStoreIDs(
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

MAPI appelle la méthode **IMSProvider:: CompareStoreIDs** lorsqu'il traite un appel à la méthode [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) . **CompareStoreIDs** est appelé à ce stade pour déterminer quelle section de profil, le cas échéant, est associée à la Banque de messages en cours d'ouverture. Un appel **CompareStoreIDs** peut être effectué lorsqu'aucun magasin de messages n'est ouvert pour un fournisseur de banque particulier. De plus, MAPI appelle également **CompareStoreIDs** lorsqu'il traite un appel de fournisseur de banque à la méthode [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) . 
  
Les identificateurs d'entrée comparés par **CompareStoreIDs** sont tous deux pour la bibliothèque de liens dynamiques (dll) du fournisseur de magasin actuel et sont tous deux des identificateurs d'entrée de magasin non enveloppés. Pour plus d'informations sur les identificateurs d'entrée de magasin de contenu, voir [IMAPISupport:: WrapStoreEntryID](imapisupport-wrapstoreentryid.md).
  
La comparaison des identificateurs d'entrée est utile, car un objet peut avoir plusieurs identificateurs d'entrée valides. Cela peut se produire, par exemple, après l'installation d'une nouvelle version d'un fournisseur de banque de messages. 
  
## <a name="see-also"></a>Voir aussi



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

