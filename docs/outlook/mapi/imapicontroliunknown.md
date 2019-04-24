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
ms.openlocfilehash: 8dce1415ef8d18f4b786e92324c888f9a0845162
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280140"
---
# <a name="imapicontrol--iunknown"></a>IMAPIControl : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Active et désactive un contrôle de bouton et exécute des tâches lorsqu'un utilisateur d'une application cliente clique sur le contrôle activé. Les fournisseurs de services implémentent les objets de contrôle pour créer des boutons personnalisés dans les boîtes de dialogue, telles que les feuilles de propriétés de configuration, qui sont définies à l'aide de tables d'affichage. 
  
Pour plus d'informations sur l'utilisation des tables d'affichage et des objets de contrôle, consultez la rubrique [afficher les tables](display-tables.md).
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Exposé par:  <br/> |Objets de contrôle  <br/> |
|Implémenté par :  <br/> |Fournisseurs de services  <br/> |
|Appelé par :  <br/> |MAPI  <br/> |
|Identificateur de l'interface:  <br/> |IID_IMAPIControl  <br/> |
|Type de pointeur:  <br/> |LPMAPICONTROL  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[Généré](imapicontrol-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur de contrôle de bouton précédente.  <br/> |
|[Activate](imapicontrol-activate.md) <br/> |Effectue une tâche telle que l'affichage d'une boîte de dialogue ou le lancement d'une opération par programme lorsqu'un utilisateur d'application cliente clique sur le contrôle de bouton.  <br/> |
|[GetState](imapicontrol-getstate.md) <br/> |Récupère une valeur qui indique si le contrôle de bouton est activé ou désactivé.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

