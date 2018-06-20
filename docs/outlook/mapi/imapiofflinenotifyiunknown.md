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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 37f21c438a0a337eecf5c15a27a0b891d19bcfb8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783878"
---
# <a name="imapiofflinenotify--iunknown"></a>IMAPIOfflineNotify : IUnknown

  
  
**S’applique à**: Outlook 
  
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


[À propos de l’API d’état en mode hors connexion](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)

