---
title: IMAPISupportModifyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyProfile
api_type:
- COM
ms.assetid: 33bef4ea-d6c0-4455-b95d-4b29edb9c0bc
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 4c296b12d2dc98c4ff8d94349298e9dda0fb9409
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316601"
---
# <a name="imapisupportmodifyprofile"></a>IMAPISupport::ModifyProfile

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Apporte des modifications permanentes à une section de profil de banque de messages.
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Masque de des indicateurs qui indique le type de banque de messages. L'indicateur suivant peut être défini:
    
MDB_TEMPORARY 
  
> La Banque de messages est temporaire et ne doit pas être ajoutée à la table de banque de messages. Lorsque MDB_TEMPORARY est défini, **ModifyProfile** renvoie S_OK immédiatement. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les modifications apportées à la section Profil ont réussi.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport:: ModifyProfile** est implémentée pour les objets de prise en charge du fournisseur de banque de messages. Les fournisseurs de banques de messages appellent **ModifyProfile** pour inviter MAPI à modifier les informations de leur profil. 
  
 **ModifyProfile** ajoute la section de profil associée au fournisseur appelant à la liste des ressources du fournisseur de banque de messages installé. Cela entraîne l'affichage de la Banque de messages dans la table de banque de messages, accessible aux clients par le biais de la méthode [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) , et à ouvrir sans l'affichage d'une boîte de dialogue. 
  
Si l'indicateur MDB_TEMPORARY est défini, MAPI ne fait rien et la méthode est renvoyée immédiatement avec S_OK.
  
## <a name="see-also"></a>Voir aussi



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

