---
title: MAPI Messages
description: Fournit une vue d’ensemble détaillée des messages MAPI et de la transmission d’une application cliente à une autre via le spouleur MAPI et les fournisseurs de services.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 417c113f-bd98-4515-85d1-09db7fc3a227
ms.openlocfilehash: 1ae510a72b3a3917c1c2a63f48c1f7bd1ec697cd
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812053"
---
# <a name="mapi-messages"></a>MAPI Messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les messages sont des objets MAPI transmis d’une application cliente à une autre par le biais du spouleur MAPI et des fournisseurs de services via un système de messagerie. Presque tous les composants de MAPI fonctionnent avec des messages. Les clients permettent aux utilisateurs de créer, d’enregistrer, d’envoyer et de supprimer des messages en plus de les copier et de les déplacer d’un dossier à un autre. Les fournisseurs de magasins de messages sont responsables de la gestion des messages et de la remise des messages au spouleur MAPI ou à un fournisseur de transport. Le spouleur MAPI déplace les messages vers un fournisseur de transport approprié, tandis que les fournisseurs de transport gèrent la remise et la réception des messages vers et à partir d’un système de messagerie et définissent les propriétés d’option de destinataire et de message. Les fournisseurs de carnets d’adresses fonctionnent indirectement avec les messages, ce qui prend en charge les propriétés qui décrivent les destinataires des messages.
  
Les messages sont stockés dans des dossiers dans un magasin de messages, généralement des dossiers créés dans le dossier racine des messages interpersonnels (IPM). Les messages sont généralement stockés au même niveau que la boîte de réception IPM standard, les éléments envoyés, les éléments supprimés et les dossiers Outbox, ou à des niveaux inférieurs dans la hiérarchie. Toutefois, les messages peuvent également être stockés en dehors de la sous-arborescence IPM.
  
Les messages créés dans la sous-arborescence IPM standard ont un contenu standard (autrement dit, un contenu visible par l’utilisateur d’une application cliente). Les notes et les rapports sont des exemples de messages qui ont un contenu standard. Les messages peuvent également être créés avec le contenu associé ou le contenu qui ne sont pas visibles dans le client standard. Les dossiers prennent en charge deux tables de contenu différentes pour contenir les différents types de messages : une table de contenu standard pour les messages standard et une table de contenu associée pour les messages associés. Étant donné que MAPI ne définit pas de normes pour le contenu des messages associés, ils peuvent contenir des informations arbitraires. 
  
Un message peut avoir des données supplémentaires ( sous la forme d’un fichier, d’un autre message ou d’un objet OLE ) qui lui sont associées. Ces données supplémentaires, appelées pièces jointes, apparaissent sous la forme d’une icône ou, pour un message RTF, sous la forme d’un métafichier dans le texte du message. Un message peut avoir zéro, une ou plusieurs pièces jointes. Les pièces jointes sont toujours transmises avec le message.
  
Un message transmis a un ou plusieurs destinataires (adresses associées à un système de messagerie particulier). Certains destinataires sont des entrées dans un conteneur qui appartient à un fournisseur de carnet d’adresses dans le profil actuel ; d’autres destinataires sont créés uniquement pour transmettre le message. Étant donné que les destinataires et les pièces jointes doivent être accessibles via le message auquel ils sont associés, les destinataires et pièces jointes d’un message sont appelés ses sous-objets. 
  
Les fournisseurs de magasins de messages prennent en charge les messages, les pièces jointes et les destinataires par le biais de méthodes dans trois interfaces : 
  
|**Interface**|**Description**|
|:-----|:-----|
|[Imessage](imessageimapiprop.md) <br/> |Gère les pièces jointes et les destinataires, envoie des messages, définit l’état de lecture. |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Crée, copie et déplace des messages et des sous-dossiers, et gère l’état des messages. |
|[IAttach](iattachimapiprop.md) <br/> |Gère les propriétés des pièces jointes. |
   
## <a name="see-also"></a>Voir aussi



[D�veloppement d'applications MAPI](mapi-application-development.md)

