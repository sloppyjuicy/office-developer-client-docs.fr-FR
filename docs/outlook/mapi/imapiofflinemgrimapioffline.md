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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397050"
---
# <a name="imapiofflinemgr--imapioffline"></a>IMAPIOfflineMgr : IMAPIOffline

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Prend en charge l’inscription pour les rappels de notification des changements d’état de connexion d’un compte d’utilisateur.
  
|||
|:-----|:-----|
|Exportés par :  <br/> |Msmapi32.dll  <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPIOfflineMgr  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[Conseiller](imapiofflinemgr-advise.md) <br/> |Enregistre les rappels de notification sur les modifications de connexion.  <br/> |
|[L’avertissement](imapiofflinemgr-unadvise.md) <br/> |Supprime un enregistrement donné pour les rappels de notification.  <br/> |
| *Membres de l’espace réservé*  <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
| *Membres de l’espace réservé*  <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
| *Membres de l’espace réservé*  <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
| *Membres de l’espace réservé*  <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
| *Membres de l’espace réservé*  <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
| *Membres de l’espace réservé*  <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
| *Membres de l’espace réservé*  <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
   
## <a name="remarks"></a>Remarques

À l’ouverture d’un objet en mode hors connexion pour un profil de compte d’utilisateur à l’aide de **[HrOpenOfflineObj](hropenofflineobj.md)**, un client obtient un objet en mode hors connexion qui prend en charge **IMAPIOfflineMgr**. 
  
Étant donné que cette interface hérite de **[IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)**, le client peut interroger cette interface (à l’aide de **[IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)** ) pour obtenir un objet qui prend en charge **[IMAPIOffline](imapiofflineiunknown.md)**. Le client peut savoir plus sur les fonctions de rappel de l’objet en mode hors connexion (en appelant **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** ), puis choisir de configurer des rappels (en utilisant **IMAPIOfflineMgr::Advise** ). 
  
La plupart des membres de cette interface est des espaces réservés réservé à un usage interne d’Outlook et est sujettes à modification. Les appelants de cette interface doivent utiliser les membres de l’espace non réservé uniquement comme indiqué.
  
## <a name="see-also"></a>Voir aussi



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)


[À propos de l’API d’état hors connexion](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)
  
[Interfaces MAPI](mapi-interfaces.md)

