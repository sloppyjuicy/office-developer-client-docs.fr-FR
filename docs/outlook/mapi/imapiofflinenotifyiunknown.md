---
title: IMAPIOfflineNotify IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineNotify
api_type:
- COM
ms.assetid: a593d2a1-29f8-7e23-85bf-02fa3cfebe1b
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: adcb8e78d4e85e19d4102795aa4d43f06a7f86ba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568146"
---
# <a name="imapiofflinenotify--iunknown"></a>IMAPIOfflineNotify : IUnknown

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Prend en charge Microsoft Outlook 2010 et Microsoft Outlook 2013 l’envoi de rappels de notification à un client.
  
|||
|:-----|:-----|
|Fourni par :  <br/> |Client  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPIOfflineNotify  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[Avertir](imapiofflinenotify-notify.md) <br/> |Envoie des notifications à un client sur les modifications de l’état de connexion.  <br/> |
   
## <a name="remarks"></a>Remarques

Le client doit implémenter cette interface et lui passer un pointeur en tant que membre dans **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** lorsque vous configurez des rappels à l’aide de **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. Ensuite, Outlook 2010 ou Outlook 2013 sera en mesure d’utiliser cette interface pour envoyer les rappels de notification au client. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[À propos de l’API d’état hors connexion](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)

