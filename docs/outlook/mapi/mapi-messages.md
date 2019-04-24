---
title: Messages MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 417c113f-bd98-4515-85d1-09db7fc3a227
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f1d1895cc6f9e65929781cb0e966873d2bce197c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345856"
---
# <a name="mapi-messages"></a>Messages MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les messages sont des objets MAPI transmis d'une application client à une autre via le spouleur MAPI et les fournisseurs de services par le biais d'un système de messagerie. Presque tous les composants de MAPI fonctionnent avec les messages. Les clients permettent aux utilisateurs de créer, enregistrer, envoyer et supprimer des messages en plus de les copier et de les déplacer d'un dossier à un autre. Les fournisseurs de banques de messages sont responsables de la gestion des messages et de la remise des messages au spouleur MAPI ou à un fournisseur de transport. Le spouleur MAPI déplace les messages vers un fournisseur de transport approprié, tandis que les fournisseurs de transport gèrent la remise et la réception des messages vers et depuis un système de messagerie et définissent les propriétés des options de destinataire et de message. Les fournisseurs de carnet d'adresses fonctionnent indirectement avec les messages, en prenant en charge les propriétés qui décrivent les destinataires des messages.
  
Les messages sont stockés dans des dossiers d'une banque de messages, généralement des dossiers créés dans le dossier racine de message. Les messages sont généralement stockés au même niveau que les dossiers boîte de réception IPM, éléments envoyés, éléments supprimés et boîte d'envoi, ou à des niveaux inférieurs dans la hiérarchie. Toutefois, les messages peuvent également être stockés en dehors de la sous-arborescence IPM.
  
Les messages créés dans la sous-arborescence IPM standard ont un contenu standard (c'est-à-dire, le contenu qui est visible par l'utilisateur d'une application cliente). Les notes et les rapports sont des exemples de messages dont le contenu est standard. Les messages peuvent également être créés avec le contenu associé ou le contenu qui n'est pas visible dans le client classique. Les dossiers prennent en charge deux tables de contenu différentes pour contenir les différents types de messages: une table des matières standard pour les messages standard et une table des matières associée pour les messages associés. Comme MAPI ne définit pas de normes pour le contenu des messages associés, il peut contenir des informations arbitraires. 
  
Un message peut contenir des données supplémentaires (sous la forme d'un fichier, d'un autre message ou d'un objet OLE) qui lui est associée. Ces données supplémentaires, appelées pièce jointe, apparaissent sous la forme d'une icône ou, pour un message RTF, sous la forme d'un métafichier dans le texte du message. Un message peut avoir zéro, une ou plusieurs pièces jointes. Les pièces jointes sont toujours transmises avec le message.
  
Un message transmis comporte un ou plusieurs destinataires (adresses associées à un système de messagerie particulier). Certains destinataires sont des entrées dans un conteneur qui appartient à un fournisseur de carnets d'adresses dans le profil actuel; les autres destinataires sont créés uniquement pour transmettre le message. Étant donné que les destinataires et les pièces jointes doivent être accessibles par le biais du message auquel ils sont associés, les destinataires et les pièces jointes d'un message sont appelés sous-objets. 
  
Les fournisseurs de banques de messages prennent en charge les messages, les pièces jointes et les destinataires via les méthodes dans trois interfaces: 
  
|**Interface**|**Description**|
|:-----|:-----|
|[IMessage](imessageimapiprop.md) <br/> |Gère les pièces jointes et les destinataires, envoie des messages, définit l'état de lecture.  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Crée, copie et déplace les messages et sous-dossiers et gère l'état des messages.  <br/> |
|[IAttach](iattachimapiprop.md) <br/> |Gère les propriétés des pièces jointes.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[D�veloppement d'applications MAPI](mapi-application-development.md)

