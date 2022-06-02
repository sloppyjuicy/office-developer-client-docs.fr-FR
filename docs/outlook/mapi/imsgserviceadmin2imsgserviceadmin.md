---
title: IMsgServiceAdmin2 IMsgServiceAdmin
description: Décrit les propriétés et l’ordre de tableau virtuel des membres pour IMsgServiceAdmin2 IMsgServiceAdmin, qui apporte des modifications à un service de message dans un profil.
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
ms.openlocfilehash: 78ba700364a732cfbe5d5edd649e9d0f81f17ef2
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828030"
---
# <a name="imsgserviceadmin2--imsgserviceadmin"></a>IMsgServiceAdmin2 : IMsgServiceAdmin

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Apporte des modifications à un service de message dans un profil.
  
|Propriété|Valeur|
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiaux.h  <br/> |
|Exposé par :  <br/> |Objets d’administration du service de message  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur d’interface :  <br/> |IID_IMsgServiceAdmin2  <br/> |
|Type de pointeur :  <br/> |LPSERVICEADMIN2  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member|Description|
|:-----|:-----|
|[CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) <br/> |Ajoute un service de message au profil actuel et retourne cet UID de service nouvellement ajouté. |
   
## <a name="remarks"></a>Remarques

L’interface **IMsgServiceAdmin2** est exposée par les mêmes objets que l’interface [IMsgServiceAdmin](imsgserviceadminiunknown.md) et est disponible à l’aide de l’implémentation de Outlook du sous-système MAPI depuis Microsoft Outlook 2003. 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

