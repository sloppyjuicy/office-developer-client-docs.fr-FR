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
ms.openlocfilehash: 3311b35a9d16f3553704d96ad58c34dd02671c23
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580019"
---
# <a name="imapicontrol--iunknown"></a>IMAPIControl : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Active et désactive un contrôle de bouton et effectue des tâches lorsqu’un utilisateur d’une application cliente clique sur le contrôle activé. Les fournisseurs de services implémentent des objets de contrôle pour créer des boutons personnalisés dans les boîtes de dialogue, tels que les feuilles de propriétés de configuration, qui sont définis à l’aide de tableaux d’affichage. 
  
Pour plus d’informations sur l’emploi de tableaux d’affichage et d’objets de contrôle, voir [Tableaux d’affichage.](display-tables.md)
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposé par :  <br/> |Objets de contrôle  <br/> |
|Implémenté par :  <br/> |Fournisseurs de services  <br/> |
|Appelé par :  <br/> |MAPI  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIControl  <br/> |
|Type de pointeur :  <br/> |LPMAPICONTROL  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[GetLastError](imapicontrol-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur de contrôle de bouton précédente.  <br/> |
|[Activate](imapicontrol-activate.md) <br/> |Effectue une tâche telle que l’affichage d’une boîte de dialogue ou le démarrage d’une opération par programme lorsqu’un utilisateur de l’application cliente clique sur le contrôle de bouton.  <br/> |
|[GetState](imapicontrol-getstate.md) <br/> |Extrait une valeur qui indique si le contrôle de bouton est activé ou désactivé.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

