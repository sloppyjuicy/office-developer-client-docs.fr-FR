---
title: IProviderAdminDeleteProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProviderAdmin.DeleteProvider
api_type:
- COM
ms.assetid: 0065b50f-95f6-4af1-81c2-a73e5111eecf
ms.openlocfilehash: 05f8ece81cc99fcaead01b4da9eeaeb7ee44af9a
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379142"
---
# <a name="iprovideradmindeleteprovider"></a>IProviderAdmin::DeleteProvider

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime un fournisseur de services du service de messagerie.
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a>Paramètres

 _lpUID_
  
> [in, out] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique qui représente le fournisseur à supprimer. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le fournisseur a été supprimé du service de messagerie.
    
MAPI_E_NOT_FOUND 
  
> Le **MAPIUID pointé** par le  _paramètre lpUID_ n’a pas été reconnu. 
    
## <a name="remarks"></a>Remarques

La **méthode IProviderAdmin::D eleteProvider** supprime un fournisseur de services du service de messagerie. **DeleteProvider** détermine le fournisseur de services à supprimer en faisant correspondre la structure **MAPIUID** pointée par  _lpUID avec l’ensemble_ d’identificateurs enregistrés par les fournisseurs de services actifs. 
  
La plupart des services de messagerie n’autorisent pas la suppression des fournisseurs pendant l’utilisation du profil. Si le fournisseur à supprimer est en cours d’utilisation, **DeleteProvider** le marque pour suppression au lieu de le supprimer immédiatement et renvoie S_OK. Lorsque le fournisseur n’est plus utilisé, il est supprimé. 
  
 **DeleteProvider appelle** la fonction de point d’entrée du service de message avant que le fournisseur ne soit supprimé du service. Le  _paramètre ulContext_ est MSG_SERVICE_PROVIDER_DELETE. La fonction de point d’entrée du service de message effectue les tâches suivantes : 
  
- Supprime le fournisseur de services.
    
- Supprime la section de profil du fournisseur de services.
    
La fonction de point d’entrée du service de messagerie n’est pas rappelée après la suppression du fournisseur.
  
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)

