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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 98e6331d5a9e52d5ae73ed12d8c045bdf226c2c4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783996"
---
# <a name="imapisupportmodifyprofile"></a>IMAPISupport::ModifyProfile

  
  
**S’applique à**: Outlook 
  
Modifie un message stocker la section profil définitive.
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Magasin de masque de bits d’indicateurs qui indique le type de message. Vous pouvez définir l’indicateur suivant :
    
MDB_TEMPORARY 
  
> La banque de messages est temporaire et ne doit pas être ajoutée à la table. Lorsque la valeur MDB_TEMPORARY, **ModifyProfile** renvoie S_OK immédiatement. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Les modifications apportées à la section profil ont réussi.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::ModifyProfile** est implémentée pour les objets de prise en charge de fournisseur de magasin de message. Magasin de fournisseurs appel **ModifyProfile** pour demander MAPI pour modifier leurs informations de profil du message. 
  
 **ModifyProfile** ajoute la section profil qui est associée avec le fournisseur d’appel à la liste des ressources de fournisseur de magasin de message installé. Cela entraîne la banque de messages pour être répertoriée dans le tableau de magasin de message, qui est disponible pour les clients par le biais de la méthode [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) et s’ouvre sans l’affichage d’une boîte de dialogue. 
  
Si l’indicateur MDB_TEMPORARY est défini, MAPI n’a aucun effet et la méthode retourne immédiatement à S_OK.
  
## <a name="see-also"></a>Voir aussi



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

