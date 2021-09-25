---
title: MAPI Messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 417c113f-bd98-4515-85d1-09db7fc3a227
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e6c716595819e4f51d540d88cf528e0ac88313d6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610292"
---
# <a name="mapi-messages"></a>MAPI Messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les messages sont des objets MAPI transmis d’une application cliente à une autre via le fournisseur de services et lepooler MAPI via un système de messagerie. Presque tous les composants de MAPI fonctionnent avec les messages. Les clients peuvent créer, enregistrer, envoyer et supprimer des messages en plus de les copier et de les déplacer d’un dossier à un autre. Les fournisseurs de magasins de messages sont responsables de la gestion des messages et de la livraison des messages aupooler MAPI ou à un fournisseur de transport. Lepooler MAPI déplace les messages vers un fournisseur de transport approprié, tandis que les fournisseurs de transport gèrent la remise et la réception des messages vers et depuis un système de messagerie et définissent les propriétés des options de destinataire et de message. Les fournisseurs de carnets d’adresses fonctionnent indirectement avec les messages, en prendre en charge les propriétés qui décrivent les destinataires du message.
  
Les messages sont stockés dans des dossiers dans l’ensemble d’une magasin de messages, généralement des dossiers créés dans le dossier racine de message interpersonnel (IPM). Les messages sont généralement stockés au même niveau que la boîte de réception IPM standard, les éléments envoyés, les éléments supprimés et les dossiers boîte d’envoi, ou à des niveaux inférieurs dans la hiérarchie. Toutefois, les messages peuvent également être stockés en dehors de la sous-arbre IPM.
  
Les messages créés dans la sous-arbre IPM standard ont un contenu standard (autrement dit, le contenu visible par l’utilisateur d’une application cliente). Les notes et les rapports sont des exemples de messages qui ont un contenu standard. Les messages peuvent également être créés avec le contenu associé ou le contenu qui ne sont pas visibles dans le client classique. Les dossiers peuvent contenir les différents types de messages à l’aide de deux tables de contenu différentes : une table des matières standard pour les messages standard et une table des matières associée pour les messages associés. Étant donné que MAPI ne fixe pas de normes pour le contenu des messages associés, ils peuvent contenir des informations arbitraires. 
  
Un message peut être associé à des données supplémentaires, sous la forme d’un fichier, d’un autre message ou d’un objet OLE. Ces données supplémentaires, appelées pièces jointes, apparaissent sous forme d’icône ou, pour un message RTF, sous forme de métafichier dans le texte du message. Un message peut avoir zéro, une ou plusieurs pièces jointes. Les pièces jointes sont toujours transmises avec le message.
  
Un message transmis a un ou plusieurs destinataires (adresses associées à un système de messagerie particulier). Certains destinataires sont des entrées dans un conteneur qui appartient à un fournisseur de carnet d’adresses dans le profil actuel ; d’autres destinataires sont créés uniquement pour transmettre le message. Étant donné que les destinataires et les pièces jointes doivent être accessibles via le message auquel ils sont associés, les destinataires et pièces jointes d’un message sont appelés ses sous-objets. 
  
Les fournisseurs de magasins de messages supportent les messages, les pièces jointes et les destinataires par le biais de méthodes dans trois interfaces : 
  
|**Interface**|**Description**|
|:-----|:-----|
|[IMessage](imessageimapiprop.md) <br/> |Gère les pièces jointes et les destinataires, envoie des messages, définit l’état de lecture.  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Crée, copie et déplace les messages et les sous-foldeurs, et gère l’état des messages.  <br/> |
|[IAttach](iattachimapiprop.md) <br/> |Gère les propriétés des pièces jointes.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[D�veloppement d'applications MAPI](mapi-application-development.md)

