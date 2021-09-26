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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 97383721fd1c9c2d8481f8c9b6fde37768555af6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630676"
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

La **méthode IMAPISupport::ModifyProfile** est implémentée pour les objets de prise en charge du fournisseur de magasins de messages. Les fournisseurs de magasins de messages **appellent ModifyProfile pour** demander à MAPI de modifier leurs informations de profil. 
  
 **ModifyProfile ajoute la** section de profil associée au fournisseur appelant à la liste des ressources de fournisseur de magasins de messages installées. Cela entraîne la liste de la magasin de messages dans la table de la boutique de messages, accessible aux clients via la méthode [IMAPISession::GetMsgStoresTable,](imapisession-getmsgstorestable.md) et ouverte sans l’affichage d’une boîte de dialogue. 
  
Si l’MDB_TEMPORARY est définie, MAPI ne fait rien et la méthode est immédiatement S_OK.
  
## <a name="see-also"></a>Voir aussi



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

