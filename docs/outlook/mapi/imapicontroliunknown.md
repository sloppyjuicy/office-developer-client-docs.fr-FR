---
title: IMAPIControl IUnknown
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 56d89141b333a70e4c45fdc6375b16e25ea96f94
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63626275"
---
# <a name="imapicontrol--iunknown"></a>IMAPIControl : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Active et désactive un contrôle de bouton et effectue des tâches lorsqu’un utilisateur d’une application cliente clique sur le contrôle activé. Les fournisseurs de services implémentent des objets de contrôle pour créer des boutons personnalisés dans les boîtes de dialogue, tels que les feuilles de propriétés de configuration, qui sont définis à l’aide de tableaux d’affichage. 
  
Pour plus d’informations sur l’emploi des tableaux d’affichage et des objets de contrôle, voir [Tableaux d’affichage](display-tables.md).
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposé par :  <br/> |Objets de contrôle  <br/> |
|Implémenté par :  <br/> |Fournisseurs de services  <br/> |
|Appelé par :  <br/> |MAPI  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIControl  <br/> |
|Type de pointeur :  <br/> |LPMAPICONTROL  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|Member |Description |
|:-----|:-----|
|[GetLastError](imapicontrol-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur de contrôle de bouton précédente. |
|[Activate](imapicontrol-activate.md) <br/> |Effectue une tâche telle que l’affichage d’une boîte de dialogue ou le démarrage d’une opération par programme lorsqu’un utilisateur de l’application cliente clique sur le contrôle de bouton. |
|[GetState](imapicontrol-getstate.md) <br/> |Extrait une valeur qui indique si le contrôle de bouton est activé ou désactivé. |
   
## <a name="see-also"></a>Consultez aussi



[Interfaces MAPI](mapi-interfaces.md)

