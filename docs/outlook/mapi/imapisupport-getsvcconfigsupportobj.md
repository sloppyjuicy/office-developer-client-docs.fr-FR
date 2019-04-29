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
ms.openlocfilehash: 6de0fed4df9d23e67c3520ffb019a961b890f988
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411308"
---
# <a name="imapisupportgetsvcconfigsupportobj"></a>IMAPISupport::GetSvcConfigSupportObj

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un objet de prise en charge du service de messagerie.
  
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
  
> remarquer Pointeur vers un pointeur vers le nouvel objet de prise en charge du service de messagerie.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'objet de prise en charge de la configuration a été correctement créé.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport:: GetSvcConfigSupportObj** est implémentée pour tous les objets de prise en charge. Les fournisseurs de services appellent **GetSvcConfigSupportObj** pour créer un objet de prise en charge de configuration à transmettre à une fonction de point d'entrée de service de messagerie. 
  
Une fonction de point d'entrée de service de messagerie est basée sur le prototype [MSGSERVICEENTRY](msgserviceentry.md) et est appelée par les méthodes de l'interface [IMsgServiceAdmin](imsgserviceadminiunknown.md) . Une fonction de point d'entrée de service de messagerie permet aux services de message de se configurer eux-mêmes ou d'effectuer d'autres actions lorsque le profil est modifié. Les fonctions de point d'entrée de service de messagerie peuvent prendre en charge les modifications de configuration en affichant une feuille de propriétés ou via un tableau de valeurs de propriété passé à la méthode [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) . 
  
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

