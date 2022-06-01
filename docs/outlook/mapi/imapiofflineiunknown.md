---
title: IMAPIOffline IUnknown
description: Décrit les propriétés, l’ordre des tables virtuelles et les remarques pour IMAPIOfflineIUnknown, qui fournit des informations pour un objet hors connexion.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIOffline
api_type:
- COM
ms.assetid: 211281ff-3c22-1b51-4b72-ca1e313c7202
ms.openlocfilehash: 55522e59a25e67c8c613d15431ead083d965f33b
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816618"
---
# <a name="imapioffline--iunknown"></a>IMAPIOffline : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit des informations pour un objet hors connexion.
  
|Propriété |Valeur |
|:-----|:-----|
|Fourni par :  <br/> |Requête sur [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIOffline  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Membre|Valeur |
|:-----|:-----|
|**[SetCurrentState](imapioffline-setcurrentstate.md)** <br/> |Définit l’état actuel d’un objet hors connexion sur en ligne ou hors connexion. |
|**[GetCapabilities](imapioffline-getcapabilities.md)** <br/> |Obtient les conditions pour lesquelles les rappels sont pris en charge par un objet hors connexion. |
|**[GetCurrentState](imapioffline-getcurrentstate.md)** <br/> |Obtient l’état en ligne ou hors connexion actuel d’un objet hors connexion. |
| *Membre d’espace réservé*  <br/> |Ce membre est un espace réservé et n’est pas pris en charge. |
   
## <a name="remarks"></a>Remarques

Un client utilise **[HrOpenOfflineObj](hropenofflineobj.md)** pour ouvrir et obtenir un objet hors connexion qui prend en charge **IMAPIOfflineMgr**. Étant donné **qu’IMAPIOfflineMgr** hérite [d’IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx), le client peut interroger cette interface (à l’aide [d’IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)) pour obtenir un pointeur vers le pointeur d’interface pour **IMAPIOffline** pour l’objet hors connexion. Le client peut ensuite obtenir ou définir l’état actuel de l’objet, ou découvrir les fonctionnalités de rappel de l’objet (en appelant **IMAPIOffline::GetCapabilities** ) et choisir de configurer des rappels à l’aide **[d’IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**. 
  
Un membre de cette interface est un espace réservé à l’utilisation interne de Microsoft Outlook 2013 et est susceptible d’être modifié. Les autres membres de cette interface doivent être utilisés uniquement comme documentés. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[À propos de l’API d’état hors connexion](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Interfaces MAPI](mapi-interfaces.md)

