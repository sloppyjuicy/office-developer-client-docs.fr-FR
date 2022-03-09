---
title: IMAPISupportGetSvcConfigSupportObj
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.GetSvcConfigSupportObj
api_type:
- COM
ms.assetid: 56c3bdae-a3a8-4334-b6d2-a89c6820d72e
ms.openlocfilehash: cdb17eb208248ca859770d16f0c455aa2ba1005c
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63380773"
---
# <a name="imapisupportgetsvcconfigsupportobj"></a>IMAPISupport::GetSvcConfigSupportObj

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un objet de support de service de message.
  
```cpp
HRESULT GetSvcConfigSupportObj(
  ULONG ulFlags,
  LPMAPISUP FAR * lppSvcSupport
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lppSvcSupport_
  
> [out] Pointeur vers un pointeur vers le nouvel objet de support du service de message.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’objet de prise en charge de la configuration a été créé avec succès.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::GetSvcConfigSupportObj** est implémentée pour tous les objets de prise en charge. Les fournisseurs de services **appellent GetSvcConfigSupportObj** pour créer un objet de prise en charge de configuration à transmettre à une fonction de point d’entrée de service de message. 
  
Une fonction de point d’entrée de service de message est basée sur le prototype [MSGSERVICEENTRY](msgserviceentry.md) et est appelée par les méthodes de l’interface [IMsgServiceAdmin](imsgserviceadminiunknown.md) . Une fonction de point d’entrée de service de message permet aux services de message de se configurer eux-mêmes ou d’effectuer d’autres actions lorsque le profil est modifié. Les fonctions de point d’entrée de service de message peuvent prendre en charge les modifications de configuration en affichant une feuille de propriétés ou via un tableau de valeurs de propriétés transmis à la méthode [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) . 
  
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

