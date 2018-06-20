---
title: IProviderAdminDeleteProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.DeleteProvider
api_type:
- COM
ms.assetid: 0065b50f-95f6-4af1-81c2-a73e5111eecf
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: e0f8dc1beeb669532e3731b38a4f03966403f76c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784388"
---
# <a name="iprovideradmindeleteprovider"></a>IProviderAdmin::DeleteProvider

  
  
**S’applique à**: Outlook 
  
Supprime un fournisseur de services à partir du service de message.
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a>Paramètres

 _lpUID_
  
> [entrée, sortie] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique qui représente le fournisseur à supprimer. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le fournisseur a été supprimé du service de message.
    
MAPI_E_NOT_FOUND 
  
> Le **MAPIUID** désignés par le paramètre _lpUID_ n’a pas été reconnue. 
    
## <a name="remarks"></a>Remarques

La méthode **IProviderAdmin::DeleteProvider** supprime un fournisseur de services à partir du service de message. **DeleteProvider** détermine le fournisseur de service à supprimer en faisant correspondre la structure **MAPIUID** désignée par _lpUID_ avec l’ensemble des identificateurs enregistré par les fournisseurs de service active. 
  
La plupart des services de messagerie ne permettent pas de fournisseurs d’être supprimée alors que le profil est en cours d’utilisation. Si le fournisseur à supprimer est en cours d’utilisation, **DeleteProvider** la marque pour suppression et non immédiatement et renvoie S_OK. Lorsque le fournisseur est n’est plus utilisé, il est supprimé. 
  
 **DeleteProvider** appelle la fonction de point d’entrée du message service avant que le fournisseur est supprimé à partir du service. Le paramètre _ulContext_ est défini à MSG_SERVICE_PROVIDER_DELETE. La fonction de point d’entrée de message service effectue les tâches suivantes : 
  
- Supprime le fournisseur de services.
    
- Supprime la section de profil du fournisseur de services.
    
La fonction de point d’entrée de message service n’est pas encore appelée une fois que le fournisseur a été supprimé.
  
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)

