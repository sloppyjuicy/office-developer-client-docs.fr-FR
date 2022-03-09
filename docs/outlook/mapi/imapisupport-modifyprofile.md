---
title: IMAPISupportModifyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.ModifyProfile
api_type:
- COM
ms.assetid: 33bef4ea-d6c0-4455-b95d-4b29edb9c0bc
ms.openlocfilehash: bbd44b75ba15875bf2cc2b7f4d430b70d653e0e4
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63381536"
---
# <a name="imapisupportmodifyprofile"></a>IMAPISupport::ModifyProfile

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Modifie définitivement une section de profil de magasin de messages.
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui indique le type de magasin de messages. L’indicateur suivant peut être définie :
    
MDB_TEMPORARY 
  
> La magasin de messages est temporaire et ne doit pas être ajoutée à la table de la boutique de messages. Lorsque MDB_TEMPORARY est définie, **ModifyProfile** S_OK immédiatement. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les modifications apportées à la section de profil ont réussi.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::ModifyProfile** est implémentée pour les objets de prise en charge du fournisseur de magasins de messages. Les fournisseurs de magasins de messages **appellent ModifyProfile** pour demander à MAPI de modifier leurs informations de profil. 
  
 **ModifyProfile ajoute la** section de profil associée au fournisseur appelant à la liste des ressources de fournisseur de magasins de messages installées. Cela entraîne la liste de la magasin de messages dans la table de la boutique de messages, accessible aux clients via la méthode [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) , et ouverte sans l’affichage d’une boîte de dialogue. 
  
Si l’MDB_TEMPORARY est définie, MAPI ne fait rien et la méthode est immédiatement S_OK.
  
## <a name="see-also"></a>Voir aussi



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

