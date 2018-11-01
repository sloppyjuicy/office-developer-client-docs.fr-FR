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
ms.openlocfilehash: 57b8438d655b3bc5b708fd7ed6734554a3a23ac4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585989"
---
# <a name="imsprovidercomparestoreids"></a>IMSProvider::CompareStoreIDs

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Compare deux messages magasin identificateurs d’entrée pour déterminer si elles font référence au même objet store.
  
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

MAPI appelle la méthode **IMSProvider::CompareStoreIDs** lors du traitement d’un appel à la méthode [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) . **CompareStoreIDs** est appelée à ce stade pour déterminer quelle section du profil, le cas échéant, est associé à la banque de messages en cours d’ouverture. Un appel **CompareStoreIDs** peut être effectué lorsque aucune banque de messages n’est ouverts pour un fournisseur de magasin particulier. En outre, MAPI appelle également **CompareStoreIDs** lors du traitement d’un appel du fournisseur de magasin à la méthode [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) . 
  
Les identificateurs d’entrée par rapport à **CompareStoreIDs** sont à la fois en cours stockent la bibliothèque de liens dynamiques du fournisseur (DLL) et sont tous deux identificateurs d’entrée non magasin. Pour plus d’informations sur les identificateurs d’entrée de magasin d’habillage, voir [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).
  
Comparaison des identificateurs d’entrée est utile, car un objet peut avoir plusieurs identificateurs d’entrée valide. Par exemple, cela peut se produire après l’installation d’une nouvelle version d’un fournisseur de magasin de message. 
  
## <a name="see-also"></a>Voir aussi



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

