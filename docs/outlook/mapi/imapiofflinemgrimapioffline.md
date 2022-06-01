---
title: IMAPIOfflineMgr IMAPIOffline
description: IMAPIOfflineMgrIMAPIOffline prend en charge l’inscription aux rappels de notification concernant les changements d’état de connexion d’un compte d’utilisateur.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIOfflineMgr
api_type:
- COM
ms.assetid: 3e430308-190c-c9bb-fffc-c26ffecb73a5
ms.openlocfilehash: ced26f1fdf7b375b6c190102fd3c5fd312cdf5dd
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816303"
---
# <a name="imapiofflinemgr--imapioffline"></a>IMAPIOfflineMgr : IMAPIOffline

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Prend en charge l’inscription aux rappels de notification concernant les changements d’état de connexion d’un compte d’utilisateur.
  
|Propriété|Valeur|
|:-----|:-----|
|Exporté par :  <br/> |msmapi32.dll  <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIOfflineMgr  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member|Description|
|:-----|:-----|
|[Conseiller](imapiofflinemgr-advise.md) <br/> |S’inscrit aux rappels de notification concernant les modifications de connexion. |
|[Non-surveillance](imapiofflinemgr-unadvise.md) <br/> |Supprime une inscription donnée pour les rappels de notification. |
| *Membre d’espace réservé*  <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
| *Membre d’espace réservé*  <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
| *Membre d’espace réservé*  <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
| *Membre d’espace réservé*  <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
| *Membre d’espace réservé*  <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
| *Membre d’espace réservé*  <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
| *Membre d’espace réservé*  <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
   
## <a name="remarks"></a>Remarques

Lors de l’ouverture d’un objet hors connexion pour un profil de compte d’utilisateur à l’aide de **[HrOpenOfflineObj](hropenofflineobj.md)**, un client obtient un objet hors connexion qui prend en charge **IMAPIOfflineMgr**. 
  
Étant donné que cette interface hérite **[d’IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)**, le client peut interroger cette interface (à l’aide **[d’IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)** ) pour obtenir un objet qui prend **[en charge IMAPIOffline](imapiofflineiunknown.md)**. Le client peut ensuite découvrir les fonctionnalités de rappel de l’objet hors connexion (en appelant **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** ) et choisir de configurer des rappels (à l’aide **d’IMAPIOfflineMgr::Advise** ). 
  
La plupart des membres de cette interface sont des espaces réservés à l’utilisation interne de Outlook et sont susceptibles d’être modifiés. Les appelants de cette interface doivent utiliser des membres non réservés uniquement comme documentés.
  
## <a name="see-also"></a>Voir aussi



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)


[À propos de l’API d’état hors connexion](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)
  
[Interfaces MAPI](mapi-interfaces.md)

