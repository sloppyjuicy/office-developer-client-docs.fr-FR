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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321265"
---
# <a name="imapioffline--iunknown"></a>IMAPIOffline : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit des informations pour un objet hors connexion.
  
|||
|:-----|:-----|
|Fourni par :  <br/> |Requête sur [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIOffline  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|**[SetCurrentState](imapioffline-setcurrentstate.md)** <br/> |Définit l’état actuel d’un objet hors connexion sur en ligne ou hors connexion.  <br/> |
|**[GetCapabilities](imapioffline-getcapabilities.md)** <br/> |Obtient les conditions pour lesquelles les rappels sont pris en charge par un objet hors connexion.  <br/> |
|**[GetCurrentState](imapioffline-getcurrentstate.md)** <br/> |Obtient l’état actuel en ligne ou hors connexion d’un objet hors connexion.  <br/> |
| *Membre d’espace réservé*  <br/> |Ce membre est un espace réservé et n’est pas pris en charge.  <br/> |
   
## <a name="remarks"></a>Remarques

Un client utilise **[HrOpenOfflineObj](hropenofflineobj.md)** pour ouvrir et obtenir un objet hors connexion qui prend en charge **IMAPIOfflineMgr**. Étant donné que **IMAPIOfflineMgr** hérite d’IUnknown, le client peut interroger cette interface (à l’aide de [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)) pour obtenir un pointeur vers le pointeur d’interface pour **IMAPIOffline** pour l’objet hors connexion. [](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) Le client peut ensuite obtenir ou définir l’état actuel de l’objet, ou connaître les fonctionnalités de rappel de l’objet (en appelant **IMAPIOffline::GetCapabilities)** et choisir de configurer des rappels à l’aide d’IMAPIOfflineMgr . **[](imapiofflinemgrimapioffline.md)** 
  
Un membre de cette interface est un espace réservé à l’utilisation interne de Microsoft Outlook 2013 et peut faire l’objet de changements. Les autres membres de cette interface doivent être utilisés uniquement comme documentés. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[À propos de l’API d’état hors connexion](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Interfaces MAPI](mapi-interfaces.md)

