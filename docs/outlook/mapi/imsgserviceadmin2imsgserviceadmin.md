---
title: IMsgServiceAdmin2 IMsgServiceAdmin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin2
api_type:
- COM
ms.assetid: 14654259-e884-46bf-84ff-9e3c1a8cd60d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ad056a9915ed72c0a972c9fa5c7fe6daef617265
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63782600"
---
# <a name="imsgserviceadmin2--imsgserviceadmin"></a>IMsgServiceAdmin2 : IMsgServiceAdmin

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Modifie un service de message dans un profil.
  
|Propriété|Valeur|
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiaux.h  <br/> |
|Exposé par :  <br/> |Objets d’administration de service de message  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur d’interface :  <br/> |IID_IMsgServiceAdmin2  <br/> |
|Type de pointeur :  <br/> |LPSERVICEADMIN2  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|Member|Description|
|:-----|:-----|
|[CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) <br/> |Ajoute un service de message au profil actuel et renvoie l’UID du service nouvellement ajouté. |
   
## <a name="remarks"></a>Remarques

L’interface **IMsgServiceAdmin2** est exposée par les mêmes objets qui exposent l’interface [IMsgServiceAdmin](imsgserviceadminiunknown.md) et est disponible à l’aide de l’implémentation de Outlook du sous-système MAPI depuis Microsoft Outlook 2003. 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

