---
title: IMAPIControl IUnknown
description: IMAPIControlIUnknown active et désactive un contrôle de bouton, et effectue des tâches lorsqu’un utilisateur d’une application cliente clique sur le contrôle activé.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIControl
api_type:
- COM
ms.assetid: 5a647e15-ba22-4a7c-b235-75cd76b77c1a
ms.openlocfilehash: 702bf550c50126525b826b8bf5d0083197a00395
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817864"
---
# <a name="imapicontrol--iunknown"></a>IMAPIControl : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Active et désactive un contrôle de bouton et effectue des tâches lorsqu’un utilisateur d’une application cliente clique sur le contrôle activé. Les fournisseurs de services implémentent des objets de contrôle pour créer des boutons personnalisés dans les boîtes de dialogue, tels que les feuilles de propriétés de configuration, qui sont définis à l’aide de tables d’affichage. 
  
Pour plus d’informations sur l’utilisation des tables d’affichage et des objets de contrôle, consultez [Tables d’affichage](display-tables.md).
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposé par :  <br/> |Objets de contrôle  <br/> |
|Implémenté par :  <br/> |Fournisseurs de services  <br/> |
|Appelé par :  <br/> |MAPI  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIControl  <br/> |
|Type de pointeur :  <br/> |LPMAPICONTROL  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member |Description |
|:-----|:-----|
|[Getlasterror](imapicontrol-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur de contrôle de bouton précédente. |
|[Activate](imapicontrol-activate.md) <br/> |Effectue une tâche telle que l’affichage d’une boîte de dialogue ou le démarrage d’une opération par programmation lorsqu’un utilisateur d’application cliente clique sur le contrôle de bouton. |
|[GetState](imapicontrol-getstate.md) <br/> |Récupère une valeur qui indique si le contrôle bouton est activé ou désactivé. |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

