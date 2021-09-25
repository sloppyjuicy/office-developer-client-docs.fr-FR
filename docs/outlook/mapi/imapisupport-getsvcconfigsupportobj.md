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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a7ed092639c7a0e7a6c1b1d39c01006ec87fdb85
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567444"
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
  
Une fonction de point d’entrée de service de message est basée sur le prototype [MSGSERVICEENTRY](msgserviceentry.md) et est appelée par les méthodes de l’interface [IMsgServiceAdmin.](imsgserviceadminiunknown.md) Une fonction de point d’entrée de service de message permet aux services de message de se configurer eux-mêmes ou d’effectuer d’autres actions lorsque le profil est modifié. Les fonctions de point d’entrée de service de message peuvent prendre en charge les modifications de configuration en affichant une feuille de propriétés ou via un tableau de valeurs de propriétés transmis à la méthode [IMsgServiceAdmin::ConfigureMsgService.](imsgserviceadmin-configuremsgservice.md) 
  
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

