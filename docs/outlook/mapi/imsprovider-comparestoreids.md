---
title: IMSProviderCompareStoreIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSProvider.CompareStoreIDs
api_type:
- COM
ms.assetid: c3e3cfaa-9c4a-482a-9411-9c4ab01d312f
ms.openlocfilehash: 33b08428f71d22d6b4e439c879f4db739a7dfe96
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63372233"
---
# <a name="imsprovidercomparestoreids"></a>IMSProvider::CompareStoreIDs

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Compare deux identificateurs d’entrée de magasin de messages pour déterminer s’ils font référence au même objet store.
  
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

MAPI appelle la méthode **IMSProvider::CompareStoreIDs** lorsqu’elle traite un appel à la méthode [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) . **CompareStoreIDs** est appelée à ce stade pour déterminer la section de profil, le cas cas, est associée à la magasin de messages en cours d’ouverture. Un **appel CompareStoreIDs peut** être effectué lorsqu’aucune boutique de messages n’est ouverte pour un fournisseur de magasins particulier. En outre, MAPI appelle **également CompareStoreIDs** lorsqu’il traite un appel de fournisseur de magasin à la méthode [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) . 
  
Les identificateurs d’entrée **comparés par compares CompareStoreID** sont tous deux pour la bibliothèque de liens dynamiques (DLL) du fournisseur de magasins actuel et sont tous deux des identificateurs d’entrée de magasin non veloppés. Pour plus d’informations sur l’habillage des identificateurs d’entrée de magasin, voir [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).
  
La comparaison des identificateurs d’entrée est utile, car un objet peut avoir plusieurs identificateurs d’entrée valides. Cela peut se produire, par exemple, après l’installation d’une nouvelle version d’un fournisseur de magasins de messages. 
  
## <a name="see-also"></a>Voir aussi



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

