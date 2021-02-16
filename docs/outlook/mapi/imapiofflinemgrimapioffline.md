---
title: IMAPIOfflineMgr IMAPIOffline
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr
api_type:
- COM
ms.assetid: 3e430308-190c-c9bb-fffc-c26ffecb73a5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 235c2afb20e6f36df72eac4070c1df5fd10fcce8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270090"
---
# <a name="imapiofflinemgr--imapioffline"></a>IMAPIOfflineMgr : IMAPIOffline

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Prend en charge l’inscription pour les rappels de notification concernant les changements d’état de connexion d’un compte d’utilisateur.
  
|||
|:-----|:-----|
|Exporté par :  <br/> |msmapi32.dll  <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIOfflineMgr  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[Conseiller](imapiofflinemgr-advise.md) <br/> |S’inscrit aux rappels de notification concernant les modifications de connexion.  <br/> |
|[Unadvise](imapiofflinemgr-unadvise.md) <br/> |Supprime une inscription donnée pour les rappels de notification.  <br/> |
| *Membre d’espace réservé*  <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
| *Membre d’espace réservé*  <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
| *Membre d’espace réservé*  <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
| *Membre d’espace réservé*  <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
| *Membre d’espace réservé*  <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
| *Membre d’espace réservé*  <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
| *Membre d’espace réservé*  <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
   
## <a name="remarks"></a>Remarques

Lors de l’ouverture d’un objet hors connexion pour un profil de compte d’utilisateur à l’aide de **[HrOpenOfflineObj](hropenofflineobj.md)**, un client obtient un objet hors connexion qui prend en charge **IMAPIOfflineMgr**. 
  
Étant donné que cette interface hérite **[d’IUnknown,](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)** le client peut interroger cette interface (à l’aide de **[IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)** ) pour obtenir un objet qui prend en charge **[IMAPIOffline](imapiofflineiunknown.md)**. Le client peut ensuite découvrir les fonctionnalités de rappel de l’objet hors connexion (en appelant **[IMAPIOffline::GetCapabilities),](imapioffline-getcapabilities.md)** puis choisir de configurer des rappels (à l’aide **d’IMAPIOfflineMgr::Advise** ). 
  
La plupart des membres de cette interface sont des espaces réservés réservés à l’utilisation interne d’Outlook et peuvent faire l’objet de changements. Les appelants de cette interface doivent utiliser les membres non-espace réservé uniquement comme documenté.
  
## <a name="see-also"></a>Voir aussi



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)


[À propos de l’API d’état hors connexion](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)
  
[Interfaces MAPI](mapi-interfaces.md)

