---
title: IMAPIControl IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl
api_type:
- COM
ms.assetid: 5a647e15-ba22-4a7c-b235-75cd76b77c1a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 395e44c2ea54816fab9f29dbedfe5e165e98c7b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783699"
---
# <a name="imapicontrol--iunknown"></a>IMAPIControl : IUnknown

  
  
**S’applique à**: Outlook 
  
Permet de désactive un contrôle bouton et effectue des tâches lorsqu’un utilisateur d’une application cliente clique sur le contrôle activé. Fournisseurs de services implémentent des objets de contrôle pour créer des boutons personnalisés dans les boîtes de dialogue, tels que des feuilles de propriétés de configuration, qui sont définies à l’aide de tables de l’affichage. 
  
Pour plus d’informations sur la façon de travailler avec les tables d’affichage et de contrôler les objets, voir [Afficher les Tables](display-tables.md).
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposés par :  <br/> |Objets de contrôle  <br/> |
|Implémentée par :  <br/> |Fournisseurs de services  <br/> |
|Appelée par :  <br/> |MAPI  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPIControl  <br/> |
|Type de pointeur :  <br/> |LPMAPICONTROL  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[GetLastError](imapicontrol-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur de contrôle de bouton précédent.  <br/> |
|[Activate](imapicontrol-activate.md) <br/> |Effectue une tâche telle que l’affichage d’une boîte de dialogue ou le démarrage d’une opération de programmation lorsqu’un utilisateur de l’application client clique sur le contrôle bouton.  <br/> |
|[GetState](imapicontrol-getstate.md) <br/> |Récupère une valeur qui indique si le contrôle bouton est activé ou désactivé.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

