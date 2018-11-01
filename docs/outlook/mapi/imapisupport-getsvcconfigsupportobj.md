---
title: IMAPISupportGetSvcConfigSupportObj
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetSvcConfigSupportObj
api_type:
- COM
ms.assetid: 56c3bdae-a3a8-4334-b6d2-a89c6820d72e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1c48ceefa84658b236b8dfa4e10df18c175d920e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595159"
---
# <a name="imapisupportgetsvcconfigsupportobj"></a>IMAPISupport::GetSvcConfigSupportObj

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un objet de prise en charge de service de message.
  
```cpp
HRESULT GetSvcConfigSupportObj(
  ULONG ulFlags,
  LPMAPISUP FAR * lppSvcSupport
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lppSvcSupport_
  
> [out] Pointeur vers un pointeur vers le nouvel objet de prise en charge de service de message.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’objet de prise en charge de configuration a été créé avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::GetSvcConfigSupportObj** est implémentée pour tous les objets de prise en charge. Fournisseurs de services d’appel **GetSvcConfigSupportObj** pour créer un objet de prise en charge de configuration pour passer à une fonction de point d’entrée de message service. 
  
Une fonction de point d’entrée de message service est basée sur le prototype [MSGSERVICEENTRY](msgserviceentry.md) et est appelée par les méthodes de l’interface [IMsgServiceAdmin](imsgserviceadminiunknown.md) . Une fonction de point d’entrée de message service permet de services de messagerie configurer eux-mêmes ou effectuer d’autres actions lorsque le profil est modifié. Point d’entrée de service Message fonctions peuvent prendre en charge les modifications de configuration en affichant une feuille de propriétés ou via un tableau de valeurs de propriété est transmis à la méthode [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) . 
  
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

