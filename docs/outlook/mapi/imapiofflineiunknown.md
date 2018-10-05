---
title: IMAPIOffline IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline
api_type:
- COM
ms.assetid: 211281ff-3c22-1b51-4b72-ca1e313c7202
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 20d8c39765b0dbbfdde530361894d0a27876010a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401278"
---
# <a name="imapioffline--iunknown"></a>IMAPIOffline : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit des informations pour un objet en mode hors connexion.
  
|||
|:-----|:-----|
|Fourni par :  <br/> |Requête sur [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPIOffline  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|**[SetCurrentState](imapioffline-setcurrentstate.md)** <br/> |Définit l’état actuel d’un objet en mode hors connexion en ligne ou hors connexion.  <br/> |
|**[GetCapabilities](imapioffline-getcapabilities.md)** <br/> |Obtient les conditions pour lequel les rappels sont pris en charge par un objet en mode hors connexion.  <br/> |
|**[GetCurrentState](imapioffline-getcurrentstate.md)** <br/> |Obtient l’état en ligne ou hors connexion en cours d’un objet en mode hors connexion.  <br/> |
| *Membres de l’espace réservé*  <br/> |Ce membre est un espace réservé et n’est pas pris en charge.  <br/> |
   
## <a name="remarks"></a>Remarques

Un client utilise **[HrOpenOfflineObj](hropenofflineobj.md)** pour ouvrir et obtenir un objet en mode hors connexion qui prend en charge **IMAPIOfflineMgr**. Étant donné que **IMAPIOfflineMgr** hérite de [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx), le client de requête cette interface (à l’aide de [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)) pour obtenir un pointeur vers le pointeur d’interface de **IMAPIOffline** pour l’objet en mode hors connexion. Le client peut ensuite obtenir ou définir l’état actuel de l’objet, ou Découvrez les fonctionnalités de rappel de l’objet (en appelant **IMAPIOffline::GetCapabilities** ) et choisissez configurer des rappels à l’aide de **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**. 
  
Un membre de cette interface est un espace réservé réservé à un usage interne de Microsoft Outlook 2013 et sujette à modification. Les autres membres de cette interface doivent être utilisés uniquement comme indiqué. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[À propos de l’API d’état hors connexion](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Interfaces MAPI](mapi-interfaces.md)

